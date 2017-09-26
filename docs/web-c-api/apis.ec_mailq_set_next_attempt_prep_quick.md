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

| ec_mailq_set_next_attempt_prep_quick |
| [Prev](apis.ec_mailq_message_requeue.php)  | Chapter 32. Mail Queue Functions |  [Next](apis.get_global_mail_queue.php) |

<a name="apis.ec_mailq_set_next_attempt_prep_quick"></a>
## Name

ec_mailq_set_next_attempt_prep_quick — pre-calculates next attempt times

## Synopsis

`#include "mail_queue.h"`

| `void **ec_mailq_set_next_attempt_prep_quick** (` | <var class="pdparam">binding_slot</var>, |   |
|   | <var class="pdparam">dr</var>, |   |
|   | <var class="pdparam">now</var>, |   |
|   | <var class="pdparam">cdate_thresh</var>, |   |
|   | <var class="pdparam">interval</var>, |   |
|   | <var class="pdparam">max_times</var>`)`; |   |

`ec_binding_slot <var class="pdparam">binding_slot</var>`;
`domain_record * <var class="pdparam">dr</var>`;
`struct timeval * <var class="pdparam">now</var>`;
`time_t * <var class="pdparam">cdate_thresh</var>`;
`time_t * <var class="pdparam">interval</var>`;
`int * <var class="pdparam">max_times</var>`;<a name="idp27021632"></a>
## Description

### Note

This reference page was automatically generated from functions found in the header files in the development branch. The function described here may not exist in generally available versions of Momentum, and may change in behavior when it is generally available. Consult your vendor for definitive advice on the use of this function.

pre-calculates next attempt times.

| [Prev](apis.ec_mailq_message_requeue.php)  | [Up](mailq.php) |  [Next](apis.get_global_mail_queue.php) |
| ec_mailq_message_requeue  | [Table of Contents](index.php) |  __get_global_mail_queue |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)