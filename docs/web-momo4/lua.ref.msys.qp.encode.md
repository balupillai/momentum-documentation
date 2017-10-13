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

| msys.qp.encode |
| [Prev](lua.ref.msys.qp.decode.php)  | Chapter 70. Lua Functions Reference |  [Next](lua.ref.msys.rfc3464.compute_delivery_status.php) |

<a name="lua.ref.msys.qp.encode"></a>
## Name

msys.qp.encode — Quoted-printable encode a string

<a name="idp18353808"></a>
## Synopsis

`msys.qp.encode(original[, charset, dotstuffing]);`

```
original: mixed
charset: string, optional
dotstuffing: boolean
```
<a name="idp18356864"></a>
## Description

`original` can be a string, `msys.core:_ec_string`, or `msys.core:_io_object`. Use `charset` to convert the text to a different character encoding before it is quoted-printable encoded. Use `dotstuffing` to specify whether or not the encoded text will be dot stuffed if qp encoding creates new line breaks. Encoded text is returned in a string.

Enable this function with the statement `require('msys.qp');`.

<a name="idp18362096"></a>
## See Also

[msys.qp.decode](lua.ref.msys.qp.decode.php "msys.qp.decode")

| [Prev](lua.ref.msys.qp.decode.php)  | [Up](lua.function.details.php) |  [Next](lua.ref.msys.rfc3464.compute_delivery_status.php) |
| msys.qp.decode  | [Table of Contents](index.php) |  msys.rfc3464.compute_delivery_status |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)