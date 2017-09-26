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

| mail_queue_check_vm_interval |
| [Prev](conf.ref.local_changes_only.php)  | 9.2. Configuration Files and Option Details |  [Next](conf.ref.mailerdaemon.php) |

<a name="conf.ref.mail_queue_check_vm_interval"></a>
## Name

mail_queue_check_vm_interval — how often to apply memory management reduction on mail queues

## Synopsis

`mail_queue_check_vm_interval = 60`

<a name="idp10065408"></a>
## Description

How often to apply memory management reduction on mail queues, based on the configured memory utilization limits.

By default, the system checks once a minute to see if too much memory is being used and attempts to swap out messages from the queues if usage is excessive.

The default value for this option is `60`.

<a name="idp10068560"></a>
## Scope

mail_queue_check_vm_interval is valid in the global scope.

| [Prev](conf.ref.local_changes_only.php)  | [Up](conf.ref.files.php) |  [Next](conf.ref.mailerdaemon.php) |
| local_changes_only  | [Table of Contents](index.php) |  mailerdaemon |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)