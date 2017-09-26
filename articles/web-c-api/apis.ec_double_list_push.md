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

| ec_double_list_push |
| [Prev](apis.ec_double_list_pop.php)  | Chapter 22. ec_double Functions |  [Next](apis.ec_double_list_remove.php) |

<a name="apis.ec_double_list_push"></a>
## Name

ec_double_list_push — Push an item to the tail of the list

## Synopsis

`#include "misc/ec_double_list.h"`

| `void **ec_double_list_push** (` | <var class="pdparam">list</var>, |   |
|   | <var class="pdparam">data</var>`)`; |   |

`ec_double_list * <var class="pdparam">list</var>`;
`void * <var class="pdparam">data</var>`;<a name="idp23582144"></a>
## Description

Push an item to the tail of the list.

**Parameters**

<dl class="variablelist">

<dt>list</dt>

<dd>

The list.

</dd>

<dt>data</dt>

<dd>

The data that will be the new tail.

</dd>

</dl>

**Threading**

It is legal to call this function in any thread.

<a name="idp23589040"></a>
## See Also

[Section 68.29, “ec_double_list”](structs.ec_double_list.php "68.29. ec_double_list") and [ec_double_list_init](apis.ec_double_list_init.php "ec_double_list_init")

| [Prev](apis.ec_double_list_pop.php)  | [Up](double.php) |  [Next](apis.ec_double_list_remove.php) |
| ec_double_list_pop  | [Table of Contents](index.php) |  ec_double_list_remove |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)