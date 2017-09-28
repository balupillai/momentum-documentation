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

| sl_next |
| [Prev](apis.sl_insert.php)  | Chapter 45. Skiplist Functions |  [Next](apis.sl_previous.php) |

<a name="apis.sl_next"></a>
## Name

sl_next — Move iter forward a node and return the new node's data

## Synopsis

`#include "skiplist.h"`

| `void * **sl_next** (` | <var class="pdparam">sl</var>, |   |
|   | <var class="pdparam">iter</var>`)`; |   |

`Skiplist * <var class="pdparam">sl</var>`;
`skiplistnode ** <var class="pdparam">iter</var>`;<a name="idp33570048"></a>
## Description

Move iter forward a node and return the new node's data.

**Parameters**

<dl class="variablelist">

<dt>sl</dt>

<dd>

The Skiplist.

</dd>

<dt>iter</dt>

<dd>

The list iterator.

</dd>

</dl>

**Return Value**

This function returns void.

### Warning

When a value is returned, the memory is owned by the Skiplist. Your memory can become invalid if something else removes this value from the Skiplist.

**Threading**

It is legal to call this function in any thread but skiplist functions are *not* thread safe.

<a name="idp33579376"></a>
## See Also

[Section 68.77, “Skiplist”](structs.skiplist.php "68.77. Skiplist")

| [Prev](apis.sl_insert.php)  | [Up](skiplist.php) |  [Next](apis.sl_previous.php) |
| sl_insert  | [Table of Contents](index.php) |  sl_previous |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)