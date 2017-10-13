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

| Chapter 18. Configuring Inbound Mail Service Using ECStream |
| [Prev](control_authz.php)  | Part III. Configuring Momentum |  [Next](esmtp_listener.php) |

## Chapter 18. Configuring Inbound Mail Service Using ECStream

**Table of Contents**

<dl class="toc">

<dt>[18.1\. ECStream_Listener Configuration](ecstream_listener.php#ecstream_listener.config)</dt>

</dl>

The ECStream_Listener is the listener that enables you to inject message using ECStream. The ECStream protocol is a bare-bones, high performance injection mechanism. It does not support any extended properties. Momentum can listen on any number of Unix domain sockets and/or IP:port addresses for TCP/IP service.

## 18.1. ECStream_Listener Configuration

The ECStream_Listener is configured in the `ecelerity.conf` file and specifies the end-point(s) on which Momentum should listen for incoming ECStream connections. The following is an example configuration:

```
ECStream_Listener {
  Listen ":1825" {
    ECStream_Idle_Time = 300
    ECStream_Max_Batch_Size = 10000
  }
}
```

In the example, `ECStream_Idle_Time` is the number of seconds of inactivity before a client is disconnected; while `ECStream_Max_Batch_Size` specifies the maximum number of ECStream messages to accept before dropping back into the scheduler. If users are having problems with the MTA becoming unresponsive when injecting messages via ECStream, it can be useful to set this to `1`.

### Note

Use [gateway](conf.ref.gateway.php "gateway") when delivering mail via ecstream.

Not all listener options are valid within the ECStream_Listener or the Listen scope within an ECStream_Listener. For the valid options, refer to [Chapter 66, *Configuration Options Summary*](config.options.summary.php "Chapter 66. Configuration Options Summary") .

Note that the `ecstream_idle_time` and `ecstream_max_batch_size` options are only valid within the ECStream scope or a listen scope within this scope. They are also the only options valid in the ECStream::Peer scope or ECStream_Listener::Listen::Peer scopes.

For general information regarding listeners, see [Section 15.4, “Listeners”](listeners.php "15.4. Listeners").

| [Prev](control_authz.php)  | [Up](p.configuration.php) |  [Next](esmtp_listener.php) |
| 17.4. Control_Listener Authorization  | [Table of Contents](index.php) |  Chapter 19. Configuring Inbound Mail Service Using SMTP |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)