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

| http_request_set_body |
| [Prev](apis.http_request_finalize.php)  | Chapter 27. httpclnt Functions |  [Next](apis.http_status_classifier.php) |

<a name="apis.http_request_set_body"></a>
## Name

http_request_set_body — Set the body of an HTTP request

## Synopsis

`#include "modules/delivery/http/httpclnt.h"`

| `void **http_request_set_body** (` | <var class="pdparam">sess</var>, |   |
|   | <var class="pdparam">body</var>`)`; |   |

`http_session *<var class="pdparam">sess</var>`;
`const char *<var class="pdparam">body</var>`;<a name="idp25136688"></a>
## Description

**Configuration Change. ** This function is available as of version 3.6.

Set the body of an HTTP request. After modifying an http_request you must call [http_request_finalize](apis.http_request_finalize.php "http_request_finalize").

**Parameters**

<dl class="variablelist">

<dt>sess</dt>

<dd>

The http_session. For a description of this data type see [Section 68.54, “http_session”](structs.http_session.php "68.54. http_session").

</dd>

<dt>body</dt>

<dd>

A character pointer to the body of the HTTP request.

</dd>

</dl>

**Return Values**

This function returns void.

**Threading**

It is legal to call this function in any thread.

<a name="idp25147408"></a>
## See Also

[http_request_finalize](apis.http_request_finalize.php "http_request_finalize")

| [Prev](apis.http_request_finalize.php)  | [Up](httpclnt.php) |  [Next](apis.http_status_classifier.php) |
| http_request_finalize  | [Table of Contents](index.php) |  http_status_classifier |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)