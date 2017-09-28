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

| sieve_return_value_string |
| [Prev](apis.sieve_return_value_number.php)  | Chapter 44. Sieve Functions |  [Next](apis.sieve_return_value_string_list.php) |

<a name="apis.sieve_return_value_string"></a>
## Name

sieve_return_value_string — Set the return value to a string

## Synopsis

`#include "sieve/ecsieve.h"`

| `void **sieve_return_value_string** (` | <var class="pdparam">seng</var>, |   |
|   | <var class="pdparam">str</var>, |   |
|   | <var class="pdparam">len</var>`)`; |   |

`SENG * <var class="pdparam">seng</var>`;
`const char * <var class="pdparam">str</var>`;
`int <var class="pdparam">len</var>`;<a name="idp33155664"></a>
## Description

Set the return value to a string.

**Parameters**

<dl class="variablelist">

<dt>seng</dt>

<dd>

The Sieve engine state.

</dd>

<dt>str</dt>

<dd>

The string return value.

</dd>

<dt>len</dt>

<dd>

The length of the string.

</dd>

</dl>

**Return Values**

This function returns void.

**Threading**

It is legal to call this function in any thread.

<a name="idp33165600"></a>
## See Also

[Section 68.73, “SENG (sieve_engine)”](structs.seng.php "68.73. SENG (sieve_engine)")

| [Prev](apis.sieve_return_value_number.php)  | [Up](sieve.php) |  [Next](apis.sieve_return_value_string_list.php) |
| sieve_return_value_number  | [Table of Contents](index.php) |  sieve_return_value_string_list |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)