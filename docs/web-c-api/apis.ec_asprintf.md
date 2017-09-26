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

| ec_asprintf |
| [Prev](string.php)  | Chapter 51. String Functions |  [Next](apis.ec_snprintf.php) |

<a name="apis.ec_asprintf"></a>
## Name

ec_asprintf — Momentum asprintf function

## Synopsis

`#include "misc/ec_string.h"`

| `int **ec_asprintf** (` | <var class="pdparam">strp</var>, |   |
|   | <var class="pdparam">fmt</var>, |   |
|   | `)`; |   |

`char ** <var class="pdparam">strp</var>`;
`const char * <var class="pdparam">fmt</var>`;
`...`;<a name="idp35327664"></a>
## Description

### Note

This reference page was automatically generated from functions found in the header files in the development branch. The function described here may not exist in generally available versions of Momentum, and may change in behavior when it is generally available. Consult your vendor for definitive advice on the use of this function.

Momentum asprintf function.

Private version of asprintf() with consistent format string support and return value.

**Parameters**

<dl class="variablelist">

<dt>strp</dt>

<dd>

the newly allocated string

</dd>

<dt>fmt</dt>

<dd>

the format string

</dd>

</dl>

**Return Values**

Returns the length of the resulting string or -1 if the allocation fails.

| [Prev](string.php)  | [Up](string.php) |  [Next](apis.ec_snprintf.php) |
| Chapter 51. String Functions  | [Table of Contents](index.php) |  ec_snprintf |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)