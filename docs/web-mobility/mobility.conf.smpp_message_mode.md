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

| smpp_message_mode |
| [Prev](mobility.conf.smpp_max_sms_subject_size.php)  | 3.1. SMPP Configuration Option Details |  [Next](mobility.conf.smpp_notify_deliver_receipt.php) |

<a name="mobility.conf.smpp_message_mode"></a>
## Name

smpp_message_mode — Specifies a message mode that is to override the default message mode used by the SMSC

## Synopsis

`smpp_message_mode = "store_and_forward"`

<a name="idp1842512"></a>
## Description

Specifies a message mode that is to override the default message mode used by the SMSC.

The default value for this option is `store_and_forward`.

The legal values for this option are: `store_and_forward` | `transaction`.

<a name="idp1846704"></a>
## Scope

smpp_message_mode is valid in the binding, binding_group, domain and global scopes.

<a name="idp1848592"></a>
## See Also

[smpp_smsc_default_message_mode](mobility.conf.smpp_smsc_default_message_mode.php "smpp_smsc_default_message_mode")

| [Prev](mobility.conf.smpp_max_sms_subject_size.php)  | [Up](mobility.smpp.options.php#mobility.conf) |  [Next](mobility.conf.smpp_notify_deliver_receipt.php) |
| smpp_max_sms_subject_size  | [Table of Contents](index.php) |  smpp_notify_deliver_receipt |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)