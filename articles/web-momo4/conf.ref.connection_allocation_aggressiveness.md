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

| connection_allocation_aggressiveness |
| [Prev](conf.ref.connect_timeout_to_delay.php)  | Chapter 72. Configuration Options Reference |  [Next](conf.ref.context.php) |

<a name="conf.ref.connection_allocation_aggressiveness"></a>
## Name

connection_allocation_aggressiveness — tune the aggressiveness for establishing new connections to domains

## Synopsis

`connection_allocation_aggressiveness = "normal"`

`connection_allocation_aggressiveness = "high"`

<a name="idp24045120"></a>
## Description

When set to `high`, Momentum will be more aggressive when opening up new connections to domains. Momentum achieves this by considering the max_outbound_connections setting (global or domain-specific, whichever is configured) and the size of the active queue for that domain. A setting of "normal" will produce a gradual increase in the number of connections, while "high" will result in a rapid number of new connections, up to the maximum allowed.

The following figure illustrates a typical scenario, with an active queue of 400 messages and a max_outbound_connections = 32 (the default).

<a name="conf.ref.connagg-diagram"></a>

**Figure 72.1. Connection Allocation Aggressiveness**

![](images/connagg.png)

The default value is `normal`.

<a name="idp24052608"></a>
## Scope

connection_allocation_aggressiveness is valid in the binding, binding_group, domain, and global scopes.

| [Prev](conf.ref.connect_timeout_to_delay.php)  | [Up](config.options.ref.php) |  [Next](conf.ref.context.php) |
| connect_timeout_to_delay  | [Table of Contents](index.php) |  context |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)