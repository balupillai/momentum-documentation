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

| smpp_registered_delivery |
| [Prev](mobility.conf.smpp_ram_expiration.php)  | 3.1. SMPP Configuration Option Details |  [Next](mobility.conf.smpp_response_timer.php) |

<a name="mobility.conf.smpp_registered_delivery"></a>
## Name

smpp_registered_delivery — Use this option to turn on one or more registered delivery flags in outgoing SMS messages, causing a SMSCs that support it to return status indications

## Synopsis

smpp_registered_delivery = ( "*`value`*" )

<a name="idp1952352"></a>
## Description

Turn on one or more registered delivery flags in outgoing SMS messages, causing SMSCs that support it to return status indications. You can set this option to multiple values but SMSC_Delivery and SMSC_Delivery_Failure can not be enabled at the same time.

Legal values for this option are as follows:

*   `SMSC_Delivery_Failure`

*   `SMSC_Delivery`

*   `intermediate`

*   `SME_Delivery`

*   `SME_User`

If you wish to receive delivery receipts, consult with your carrier or provider on which classes of delivery receipts are supported in their network.

<a name="idp1962704"></a>
## Scope

smpp_registered_delivery is valid in the binding, binding_group, domain and global scopes.

| [Prev](mobility.conf.smpp_ram_expiration.php)  | [Up](mobility.smpp.options.php#mobility.conf) |  [Next](mobility.conf.smpp_response_timer.php) |
| smpp_ram_expiration  | [Table of Contents](index.php) |  smpp_response_timer |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)