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

| rfc2047_utf8_decode_to_string |
| [Prev](apis.rfc2047_utf8_decode.php)  | Chapter 40. RFC Functions |  [Next](apis.rfc2047_utf8_encode_to_string.php) |

<a name="apis.rfc2047_utf8_decode_to_string"></a>
## Name

rfc2047_utf8_decode_to_string — decodes MIME header encoding and stores the decoded result to a string

## Synopsis

`#include "misc/rfc2047.h"`

| `int **rfc2047_utf8_decode_to_string** (` | <var class="pdparam">header</var>, |   |
|   | <var class="pdparam">hdrlen</var>, |   |
|   | <var class="pdparam">out</var>`)`; |   |

`const char * <var class="pdparam">header</var>`;
`int <var class="pdparam">hdrlen</var>`;
`string * <var class="pdparam">out</var>`;<a name="idp30973056"></a>
## Description

### Note

This reference page was automatically generated from functions found in the header files in the development branch. The function described here may not exist in generally available versions of Momentum, and may change in behavior when it is generally available. Consult your vendor for definitive advice on the use of this function.

decodes MIME header encoding and stores the decoded result to a string

**Parameters**

<dl class="variablelist">

<dt>header</dt>

<dd>

the header text to be decoded

</dd>

<dt>hdrlen</dt>

<dd>

the length of the header

</dd>

<dt>out</dt>

<dd>

the destination for the decoded result.

</dd>

</dl>

The output string will receive a utf-8 encoded string.

**Return Values**

the length of the decoded string.

**Configuration Change. ** This feature is available starting from Momentum 3.0.18.

| [Prev](apis.rfc2047_utf8_decode.php)  | [Up](rfc.php) |  [Next](apis.rfc2047_utf8_encode_to_string.php) |
| rfc2047_utf8_decode  | [Table of Contents](index.php) |  rfc2047_utf8_encode_to_string |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)