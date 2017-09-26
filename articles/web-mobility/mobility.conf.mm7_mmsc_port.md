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

| mm7_mmsc_port |
| [Prev](mobility.conf.mm7_mmsc_path.php)  | 8.1. MM7 Configuration Option Details |  [Next](mobility.conf.mm7_mmsc_server.php) |

<a name="mobility.conf.mm7_mmsc_port"></a>
## Name

mm7_mmsc_port — specify the TCP port number for the target MMSC MM7 entity.

## Synopsis

`mm7_mmsc_port = "8080"`

<a name="idp2480880"></a>
## Description

Specify the TCP port number for the target MMSC MM7 entity.

The default value for this option is `8080`.

**Configuration Change. ** This option is valid in all versions of Momentum *prior* to 3.5.6 and in Momentum 3.6\. It is deprecated in Momentum version 3.5.6; use [routes](https://support.messagesystems.com/docs/web-ref/conf.ref.routes.php) instead.

<a name="idp2486592"></a>
## Scope

This option is valid in the domain and global scopes.

<a name="idp2488432"></a>
## See Also

[mm7_mmsc_server](mobility.conf.mm7_mmsc_server.php "mm7_mmsc_server")

| [Prev](mobility.conf.mm7_mmsc_path.php)  | [Up](mobility.mm7.options.php#mm7.conf) |  [Next](mobility.conf.mm7_mmsc_server.php) |
| mm7_mmsc_path  | [Table of Contents](index.php) |  mm7_mmsc_server |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)