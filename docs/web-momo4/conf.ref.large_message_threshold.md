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

| large_message_threshold |
| [Prev](conf.ref.keep_message_dicts_in_memory.php)  | Chapter 72. Configuration Options Reference |  [Next](conf.ref.legacy_message_threshold.php) |

<a name="conf.ref.large_message_threshold"></a>
## Name

large_message_threshold — Consider a message large when its size exceeds this amount

## Synopsis

`large_message_threshold = 131072`

<a name="idp25068848"></a>
## Description

For performance reasons, Momentum prefers to keep message contents in memory. From time to time, messages that are much larger than average enter the system. Such messages may either be transiently rejected (because they cannot fit in memory) or increase demands on memory and have an adverse affect on overall system performance.

In order to avoid this, Momentum can use alternative techniques for working with messages that are larger than the `large_message_threshold`. Large messages pass through the system a little more slowly (wallclock time) than their regular counterparts, mitigating their impact on the rest of the system.

The default is 131072 bytes. If the majority of your messages are larger than the default, then you should adjust the threshold upwards so that the system will run more efficiently.

<a name="idp25072816"></a>
## Scope

large_message_threshold is valid in the global scope.

<a name="idp25074656"></a>
## See Also

[growbuf_size](conf.ref.growbuf_size.php "growbuf_size"), [legacy_message_threshold](conf.ref.legacy_message_threshold.php "legacy_message_threshold")

| [Prev](conf.ref.keep_message_dicts_in_memory.php)  | [Up](config.options.ref.php) |  [Next](conf.ref.legacy_message_threshold.php) |
| keep_message_dicts_in_memory  | [Table of Contents](index.php) |  legacy_message_threshold |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)