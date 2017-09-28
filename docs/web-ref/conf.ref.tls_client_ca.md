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

| tls_client_ca |
| [Prev](conf.ref.tls_enable_dhe_ciphers.php)  | 9.2. Configuration Files and Option Details |  [Next](conf.ref.tls_ifavailable_fallback.php) |

<a name="conf.ref.tls_client_ca"></a>
## Name

tls_client_ca — certificate authority for inbound mail

## Synopsis

`TLS_Client_Ca = "/path/to/CAlist"`

<a name="idp12121152"></a>
## Description

TLS_Client_Ca specifies a file containing a trusted certificate authority list. These certificates should be in PEM format. This CA list will be referenced if TLS_Verify is set to either `ca` or `host`.

<a name="idp12123808"></a>
## Scope

`tls_client_ca` is valid in the ecstream_listener, esmtp_listener, global, http_listener, listen, pathway, pathway_group and peer scopes.

| [Prev](conf.ref.tls_enable_dhe_ciphers.php)  | [Up](conf.ref.files.php) |  [Next](conf.ref.tls_ifavailable_fallback.php) |
| tls_enable_dhe_ciphers  | [Table of Contents](index.php) |  tls_ifavailable_fallback |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)