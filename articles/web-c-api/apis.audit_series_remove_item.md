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

| audit_series_remove_item |
| [Prev](apis.audit_series_item_delref.php)  | Chapter 4. Audit Series Functions |  [Next](bag.php) |

<a name="apis.audit_series_remove_item"></a>
## Name

audit_series_remove_item — Remove the item identified by key in a named series

## Synopsis

`#include "modules/validate/audit_series.h"`

| `int **audit_series_remove_item** (` | <var class="pdparam">name</var>, |   |
|   | <var class="pdparam">key</var>, |   |
|   | <var class="pdparam">ac</var>`)`; |   |

`const char * <var class="pdparam">name</var>`;
`char * <var class="pdparam">key</var>`;
`accept_construct * <var class="pdparam">ac</var>`;<a name="idp19778064"></a>
## Description

### Note

This reference page was automatically generated from functions found in the header files in the development branch. The function described here may not exist in generally available versions of Momentum, and may change in behavior when it is generally available. Consult your vendor for definitive advice on the use of this function.

Remove the item identified by key in a named series.

**Parameters**

<dl class="variablelist">

<dt>name</dt>

<dd>

- name of the series.

</dd>

<dt>key</dt>

<dd>

- the key for which the counts is desired. For series of type "cidr", key is of the form "ip/mask". to use the remote IP of current session, caller can pass in "ac" instead.

</dd>

<dt>ac</dt>

<dd>

- accept construct. This is the alternative for passing in an IP for cidr series.

</dd>

</dl>

**Return Values**

0 if successful, -1 if error.

**Configuration Change. ** This feature is available starting from Momentum 3.1.

| [Prev](apis.audit_series_item_delref.php)  | [Up](audit_series.php) |  [Next](bag.php) |
| audit_series_item_delref  | [Table of Contents](index.php) |  Chapter 5. Bag Functions |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)