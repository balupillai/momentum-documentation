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

| sieve_set_operation_complete |
| [Prev](apis.sieve_set_module_state.php)  | Chapter 44. Sieve Functions |  [Next](apis.sieve_set_response.php) |

<a name="apis.sieve_set_operation_complete"></a>
## Name

sieve_set_operation_complete — Set the action of the Sieve engine upon completion

## Synopsis

`#include "sieve/ecsieve.h"`

| `void **sieve_set_operation_complete** (` | <var class="pdparam">seng</var>, |   |
|   | <var class="pdparam">mode</var>`)`; |   |

`SENG * <var class="pdparam">seng</var>`;
`int <var class="pdparam">mode</var>`;<a name="idp33364960"></a>
## Description

Set the action of the Sieve engine upon completion.

**Parameters**

<dl class="variablelist">

<dt>seng</dt>

<dd>

The Sieve engine state.

</dd>

<dt>mode</dt>

<dd>

Set this to either `SIV_ERROR_MODE_CONTINUE` or `SIV_ERROR_MODE_FAIL`.

</dd>

</dl>

**Return Values**

This function returns void.

**Threading**

It is legal to call this function in any thread.

<a name="idp33374000"></a>
## See Also

[Section 68.73, “SENG (sieve_engine)”](structs.seng.php "68.73. SENG (sieve_engine)")

| [Prev](apis.sieve_set_module_state.php)  | [Up](sieve.php) |  [Next](apis.sieve_set_response.php) |
| sieve_set_module_state  | [Table of Contents](index.php) |  sieve_set_response |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)