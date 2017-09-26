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

| authorization |
| [Prev](conf.ref.async_unlink_concurrency.php)  | 9.2. Configuration Files and Option Details |  [Next](conf.ref.bind_address.php) |

<a name="conf.ref.authorization"></a>
## Name

authorization — configure the console commands applicable to users

<a name="idp4245600"></a>
## Description

<a name="example.authorization"></a>

**Example 9.2. authorization**

```
Authorization {
  role [
    allow = "regular expression"
    allow = "another regular expression"
  ]
  username [
    allow = "regular expression"
  ]
}
```

The authorization stanza will prevent console commands from being run unless an "allow" entry is explicitly configured. The authorization process first enumerates the roles/group membership of the user by querying the authorization module configured in the listener configuration. Then the username and each role for the user are compared against the authorization rules; if the username or role name matches, then the "allow" rules are processed in the order that they are defined.

Each allow rule is a Perl compatible regular expression that will be matched against the command being executed. If the regular expression matches, then processing of authorization rules stops and the console command is allowed to execute. If no rules match, then the command is not allowed to execute and if account logging is enabled a log entry is written.

<a name="idp4251360"></a>
## Scope

authorization is valid in the Control_Listener scope.

<a name="idp4253280"></a>
## See Also

[Section 14.4, “auth_ds – Datasource based SMTP Authentication”](modules.auth_ds.php "14.4. auth_ds – Datasource based SMTP Authentication") and [Section 2.2.3, “Control Listener Authorization”](conf.aaa.php#conf.control_authz "2.2.3. Control Listener Authorization")

| [Prev](conf.ref.async_unlink_concurrency.php)  | [Up](conf.ref.files.php) |  [Next](conf.ref.bind_address.php) |
| async_unlink_concurrency  | [Table of Contents](index.php) |  bind_address |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)