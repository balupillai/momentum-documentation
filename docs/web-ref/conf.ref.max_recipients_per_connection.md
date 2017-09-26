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

| max_recipients_per_connection |
| [Prev](conf.ref.max_recipients_per_batch.php)  | 9.2. Configuration Files and Option Details |  [Next](conf.ref.max_resident_active_queue.php) |

<a name="conf.ref.max_recipients_per_connection"></a>
## Name

max_recipients_per_connection — maximum number of recipients to send on a connection

## Synopsis

`Max_Recipients_Per_Connection = 0`

<a name="idp10255168"></a>
## Description

If set to `0` (the default), then no maximum limit will be enforced, otherwise, it specifies the maximum number of RCPT TO commands that can be used on a given connection. This is similar to `Max_Deliveries_Per_Connection` but takes into account multi-recipient outbound mail.

<a name="idp10258208"></a>
## Scope

max_recipients_per_connection is valid in the binding, binding_group, domain, listener, listen and global scopes.

<a name="idp10260624"></a>
## See Also

[max_deliveries_per_connection](conf.ref.max_deliveries_per_connection.php "max_deliveries_per_connection")

| [Prev](conf.ref.max_recipients_per_batch.php)  | [Up](conf.ref.files.php) |  [Next](conf.ref.max_resident_active_queue.php) |
| max_recipients_per_batch  | [Table of Contents](index.php) |  max_resident_active_queue |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)