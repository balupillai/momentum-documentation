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

| 71.11. bind_address_secondary – Dual-stack IPv4/IPv6 Support |
| [Prev](modules.beik.php)  | Chapter 71. Modules Reference |  [Next](modules.bounce_classifier_override.php) |

## 71.11. bind_address_secondary – Dual-stack IPv4/IPv6 Support

<a class="indexterm" name="idp20047296"></a>

**Configuration Change. ** This feature is available in Momentum 4.2 and later.

The bind_address_secondary module allows a binding to attach itself to an ipv6 address as well as a ipv4 one, supporting multiple IP addresses for dual stack. The secondary could be ipv6 or ipv4\. In the dual stack case, it is desirable to select the appropriate address family for a given downstream destination (ie, MX). This module supports one IP address per address family per binding.

### 71.11.1. Configuration

The bind_address_secondary module is enabled as follows:

<a name="modules.bind_address_secondary.example"></a>

**Example 71.19. bind_address_secondary Configuration**

bind_address_secondary {}
binding "whatever" {
  bind_address_secondary = *`whatever`*
}

| [Prev](modules.beik.php)  | [Up](modules.php) |  [Next](modules.bounce_classifier_override.php) |
| 71.10. beik – Symantec Brightmail™ Engine Integration Kit  | [Table of Contents](index.php) |  71.12. bounce_classifier_override – Override/Augment Bounce Classifications |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)