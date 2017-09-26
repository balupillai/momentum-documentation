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

| keep_message_dicts_in_memory |
| [Prev](conf.ref.inline_transfail_processing.php)  | Chapter 72. Configuration Options Reference |  [Next](conf.ref.large_message_threshold.php) |

<a name="conf.ref.keep_message_dicts_in_memory"></a>
## Name

keep_message_dicts_in_memory — preserve memory representation of metadata when memory is low

## Synopsis

`keep_message_dicts_in_memory = false`

<a name="idp25045904"></a>
## Description

Momentum aggressively uses RAM to speed up processing, and to make that approach successful, it also needs to realize that it should reclaim and re-use memory for messages that are delayed. When a message is placed on the delayed queue, or when one of the various memory management metrics indicates that too much memory is in use, Momentum will discard the message body and the in-memory representation of the validation context dictionaries that were captured during reception.

This results in reduced memory usage, but can result in higher disk IO, and in particular, unexpected disk IO on the scheduler thread after periods of intense memory pressure if you are using validation context data to drive your binding assignment or other policy hooks.

By setting `keep_message_dicts_in_memory` to `true`, Momentum will retain the validation context dictionaries in memory when it discards the message body memory. This will prevent additional disk IO when the message is later scheduled for delivery, but at the cost of increased memory usage.

### Warning

In some circumstances, using the Lua function [msg:routing_domain](lua.ref.msg_routing_domain.php "msg:routing_domain") may cause Momentum to "watchdog" (i.e., to become unresponsive and restart). To alleviate this, set `keep_message_dicts_in_memory` to `true`.

If you change this option you must restart the ecelerity process for the change to take effect. Invoking **`config reload`**         from the system console is not sufficient.

To reduce the overall memory cost of enabling this option, make use of the `exclude_vctx_mess` and `exclude_vctx_conn` options to reduce the size of the validation context dictionaries.

The default value is `false`.

<a name="idp25056528"></a>
## Scope

keep_message_dicts_in_memory is valid in the global scope.

<a name="idp25058368"></a>
## See Also

[exclude_vctx_conn](conf.ref.exclude_vctx_conn.php "exclude_vctx_conn"), [exclude_vctx_mess](conf.ref.exclude_vctx_mess.php "exclude_vctx_mess")

| [Prev](conf.ref.inline_transfail_processing.php)  | [Up](config.options.ref.php) |  [Next](conf.ref.large_message_threshold.php) |
| inline_transfail_processing  | [Table of Contents](index.php) |  large_message_threshold |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)