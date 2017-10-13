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

| msg_gen_data_spool |
| [Prev](hooks.php)  | Chapter 69. Hook Points and C Functions Reference |  [Next](hooks.config_rsrc_setup.php) |

<a name="hooks.msg_gen_data_spool"></a>
## Name

msg_gen_data_spool — This hook is invoked after a message has been generated by the msg_gen module

## Synopsis

`#include "hooks/msg_gen/msg_generator.h"`

| `void **msg_gen_data_spool** (` | <var class="pdparam">mess</var>`)`; |   |

`ec_message * <var class="pdparam">mess</var>`;<a name="idp6304384"></a>
## Description

This hook is invoked after the message has been generated. The pointer passed to this function points to the newly generated message.

### Warning

Messages rejected at this hook point are not reported in the UI as rejections.

**Parameters**

<dl class="variablelist">

<dt>mess</dt>

<dd>

A pointer to the new `ec_message`. For a description of this struct see [ec_message](https://support.messagesystems.com/docs/web-c-api/structs.ec_message.php).

</dd>

</dl>

**Return Values**

This hook returns void.

**Threading**

This hook will be called in any thread.

<a name="idp6302544"></a>
## See Also

[msg_gen Module](modules.msg_gen.php "71.48. msg_gen – Message Generation")

| [Prev](hooks.php)  | [Up](hooks.php) |  [Next](hooks.config_rsrc_setup.php) |
| Chapter 69. Hook Points and C Functions Reference  | [Table of Contents](index.php) |  config_rsrc_setup |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)