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

| mail_queue_maintain_domain |
| [Prev](hooks.core.mail_queue_insert_active.php)  | Chapter 60. Hooks in the core scope |  [Next](hooks.core.mailq_get_next_active.php) |

<a name="hooks.core.mail_queue_maintain_domain"></a>
## Name

mail_queue_maintain_domain

## Synopsis

`#include "hooks/core/mail_queue_maintain_domain.h"`

| `void **mail_queue_maintain_domain** (` | <var class="pdparam">closure</var>, |   |
|   | <var class="pdparam">dr</var>, |   |
|   | <var class="pdparam">now</var>, |   |
|   | <var class="pdparam">rv</var>`)`; |   |

`void * <var class="pdparam">closure</var>`;
`domain_record * <var class="pdparam">dr</var>`;
`struct timeval * <var class="pdparam">now</var>`;
`int * <var class="pdparam">rv</var>`;

| `int **has_core_mail_queue_maintain_domain_hook** (` | `)`; |   |

| `void **register_core_mail_queue_maintain_domain_hook_first** (` | <var class="pdparam">hook</var>, |   |
|   | <var class="pdparam">closure</var>`)`; |   |

`ec_hook_core_mail_queue_maintain_domain_func_t <var class="pdparam">hook</var>`;
`void *<var class="pdparam">closure</var>`;

| `void **register_core_mail_queue_maintain_domain_hook_last** (` | <var class="pdparam">hook</var>, |   |
|   | <var class="pdparam">closure</var>`)`; |   |

`ec_hook_core_mail_queue_maintain_domain_func_t <var class="pdparam">hook</var>`;
`void *<var class="pdparam">closure</var>`;

| `void **call_core_mail_queue_maintain_domain_hook** (` | <var class="pdparam">dr</var>, |   |
|   | <var class="pdparam">now</var>, |   |
|   | <var class="pdparam">rv</var>`)`; |   |

`domain_record * <var class="pdparam">dr</var>`;
`struct timeval * <var class="pdparam">now</var>`;
`int * <var class="pdparam">rv</var>`;<a name="idp10021088"></a>
## Description

By registering a function for this hook, Momentum's internal `mail_queue_maintain_domain` function is disabled and replaced by calls to the functions registered.

This function is responsible for putting into action any connections necessary for the delivery of messages in the active queue for the domain *`dr`* across all MultiVIP™ bindings. The number of total connections established should be placed in *`*rv`*.

| [Prev](hooks.core.mail_queue_insert_active.php)  | [Up](hooks.core.php) |  [Next](hooks.core.mailq_get_next_active.php) |
| mail_queue_insert_active  | [Table of Contents](index.php) |  mailq_get_next_active |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)