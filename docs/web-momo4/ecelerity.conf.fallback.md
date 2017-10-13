Logged in as: OmniTI, Inc.  ([logout](https://support.messagesystems.com/logout.php))

[![Message Systems](https://support.messagesystems.com/images/ms-white205.png)](https://support.messagesystems.com/start.php) 

*   [Changelog](https://support.messagesystems.com/start.php?show=changelog)
*   [Documentation](https://support.messagesystems.com/docs/)
*   [Downloads](https://support.messagesystems.com/start.php)

*   [Licenses](https://support.messagesystems.com/license_summary.php)
*   <a href="">Clients</a>
    *   [Support](https://support.messagesystems.com/cs.php)
    *   [Add/Edit](https://support.messagesystems.com/edit_client.php)
    *   [Legal/Products](https://support.messagesystems.com/edit_products.php)
*   [Users](https://support.messagesystems.com/edit_customer.php)

## Search Help

Search for a single word or perform multi-word searches by enclosing your search in quotation marks.

Where you have multiple words but no quotation marks, an **OR** search is performed. For example, **"REST Injection"** searches for the phrase **"REST Injection"**, and, without quotation marks, searches for **REST OR Injection**--the operator is understood.

### Warning

You must escape the following special characters: **+ - && || ! ( ) { } [ ] ^ " ~ * ? : \**. Use the **\** character as the escape character. For example: **B0/00-11719-46C328D4\:default\:**

You can also perform **AND** searches, for example, **rest AND port** (no quotation marks) finds pages where both these words occur.

Terms used in searches are case-insensitive but operators are not. Alphabetic operators **must** be in uppercase.

Other operators can also be used. For more information see "[Query Parser Syntax](https://lucene.apache.org/core/old_versioned_docs/versions/3_0_0/queryparsersyntax.html)". Use of fields in searches is not currently supported.

| 15.3. Configuration Scopes and Fallback |
| [Prev](conf.options.php)  | Chapter 15. Configuration Overview |  [Next](listeners.php) |

## 15.3. Configuration Scopes and Fallback

Momentum has a flexible configuration system that allows many options to be set to different values for different hosts, domains, bindings, and binding groups:

*   [binding_group](conf.ref.binding_group.php "binding_group") - stanza to configure binding_group-specific options

*   [binding](conf.ref.binding.php "binding") - stanza to configure binding-specific options

*   [domain](conf.ref.domain.php "domain") - stanza to configure MultiVIP© domain-specific options

*   [host](conf.ref.host.php "host") - stanza to configure host-specific options

`domain` stanzas can be nested inside a `binding` stanza, creating a per-binding, per-domain configuration. This is referred to as a `binding::domain` scope. Also, since hosts may appear within bindings, there is also a `binding::host` scope. Other permutations also apply; for example, when a domain is within a binding that is in turn a member of a binding group, the scope is `binding-group::binding::domain`.

From within the console, you can determine the value of an option within a specific scope using **config eval** .

For example, to determine the value of `Enable_Authentication` within the scope of a TCP/IP Listen stanza within a Control_Listener, issue the command:

**`config eval Control_Listener Listen 127.0.0.1:2025 Enable_Authentication`**                                                                   

If `Enable_Authentication` is set to `true` within the Control_Listener scope and not overridden in the TCP/IP Listen stanza, its value will be the fallback value of `true`.

Since options may be defined in more than one scope, it can sometimes be difficult to determine what value applies. Momentum resolves the configuration options by looking for the most specific setting it can find; if it doesn't find a precise match, it falls back to the parent level(s) and repeats this process until it reaches the globally configured value.

How this works is best demonstrated by example:

<a name="domain-scope-fallback"></a>

**Example 15.1. Domain Scope and Fallback**

```
max_outbound_connections = 40

domain "example.com" {
  max_outbound_connections = 20
}

domain "someotherexample.com" {
  max_resident_active_queue_size = 500
}
```

This configures Momentum to open no more than 40 connections to a given domain, except for the domain `example.com`, which is limited to 20 connections. The domain `someotherexample.com` does not explicitly specify a value for `max_outbound_connections`, so it falls-back to the globally configured value of 40.

A similar fallback occurs when using bindings:

<a name="binding-scope-fallback"></a>

**Example 15.2. Binding Scope and Fallback**

```
message_expiration = 86400

binding "example" {
  message_expiration = 3600
}

domain "example.com" {
  message_expiration = 120
}

binding "example2" {
  message_expiration = 7200

  domain example.com {
    message_expiration = 86400
  }

  domain "anotherexample.com" {
    max_resident_active_queue_size = 500
  }
}

binding "example3" {

  domain "example.com" {
    max_resident_active_queue_size = 500
  }

  domain "anotherexample.com" {
    message_expiration = 86400
  }
}
```

In this configuration, the message expiration time is 86400 seconds, unless the mail is attached to one of the bindings, `example`, `example2` or `example3`. Mail on binding `example` is subject to an expiration time of 3600 seconds. On binding `example2`, the expiration time is 7200 seconds except for mail destined for the domain `example.com`, which is set to 86400 seconds. Because the most specific setting for the domain `example.com` is the domain stanza within the binding stanza, this is the setting that takes effect. Outside the binding `example2`, in a global domain stanza, `message_expiration` is set to `120` for domain `example.com`, but this setting will not take effect because it is overridden by the more specific setting.

Note that because the domain `anotherexample.com` within binding `example2` does not specify a value for `message_expiration`, the effective value is taken from its parent binding, which is 7200\. The same value will be used for any other domain routed via that binding unless it is explicitly overridden.

Binding `example3` is configured similarly to binding `example2`, except that it does not specify a value for `message_expiration`. This means that mail for domain `anotherexample.com` will be subject to a message expiration of 86400, because it is explicitly configured. All other domains will fall back to the value of their parent binding, which, in this case is "unset", so the value will fall back again and look for a global domain setting. For the domain `example.com`, there is a global domain configuration that sets message expiration to 120 seconds, so this value will be used. For all other domains within this binding, there is no global domain stanza so the fallback ends up at the globally configured value of 86400.

Bindings can be nested within binding groups as shown in the following example:

<a name="binding-group-fallback"></a>

**Example 15.3. Binding_Group and Fallback**

```
max_outbound_connections = 30

binding_group "group1" {
  max_outbound_connections = 5

  binding "example" {
    bind_address = 10.10.10.10
    max_outbound_connections = 15

    domain "example.com" {
      #some other options
    }
  }
}
```

In this specific case, the value of `max_outbound_connections` for domain `example.com` will be `15` because `max_outbound_connections` is not defined within the domain `example.com`. This option then assumes the value of the binding that contains the domain. You can confirm the value by opening the console and using **config eval** . For example:

```
ecelerity(/tmp/2025)> config eval binding_group group1 binding example \
 domain example.com max_outbound_connections Max_Outbound_Connections = 15
```

If you remove `max_outbound_connections` from the binding `example`, the value of this option for the domain `example.com` becomes `5`, namely its value within the binding group that contains domain `example.com`.

In summary, the value that a configuration option assumes, in order of decreasing precedence, is as follows:

*   Value given in a domain stanza within a binding that is part of a binding group

*   Value given in a domain stanza within a binding

*   Value given in a domain stanza within a binding_group

*   Value specified within the binding stanza

*   Value specified within a global domain stanza

*   Global setting

| [Prev](conf.options.php)  | [Up](conf.overview.php) |  [Next](listeners.php) |
| 15.2. Configuration Options  | [Table of Contents](index.php) |  15.4. Listeners |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)