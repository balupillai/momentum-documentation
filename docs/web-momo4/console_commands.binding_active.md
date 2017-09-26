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

| binding active |
| [Prev](console_commands.authz_roles_list.php)  | Chapter 73. Non-Module-Specific Console Commands |  [Next](console_commands.binding_delayed.php) |

<a name="console_commands.binding_active"></a>
## Name

binding active — show domains with active queue size bigger than threshold on a specified binding

## Synopsis

`binding active` { *`binding_name`* } { *`threshold`* }

<a name="idp12793024"></a>
## Description

The **binding active**        command presents information concerning the domains on a given binding with a large number of active messages in queue. The command takes a binding name and a single positive integer as an argument which specifies the threshold of interest. The output will include all domains on the given binding whose active queues exceed the integer specified.

```
10:47:35 /tmp/2025> binding active BINDING1 100
Domain:                         c4.com  C:  0  A:    104  D:     0  S:    47
Domain:                    dellnet.com  C:  0  A:    102  D:   460  S:  1540
Domain:                  earthlink.com  C: 60  A:    315  D:   192  S:  1957
Domain:                    iopener.net  C:  0  A:    124  D:   200  S:   860
Domain:                        jps.net  C: 29  A:    114  D:   471  S:  2561
Domain:                         pa.net  C: 30  A:    119  D:    31  S:   274
Domain:                   peoplepc.com  C:  0  A:    473  D:  1262  S:  7758
Domain:                 sprintmail.com  C: 32  A:    120  D:    71  S:   898
Domain:                   xoommail.com  C:  0  A:    102  D:     0  S:    55
Domain:                      yesic.com  C:  0  A:    124  D:     0  S:    56
                                Total:  C: 616  A:  22965  D: 34427  S:1954767
```

<dl class="variablelist">

<dt>C</dt>

<dd>

current number of connections

</dd>

<dt>A</dt>

<dd>

current size of the active queue

</dd>

<dt>D</dt>

<dd>

current size of the delayed queue

</dd>

<dt>S</dt>

<dd>

total messages sent during the life of the domain record

</dd>

</dl>

The row detailing the totals represents the totals across *all* domains on the given binding, not just those listed.

<a name="idp11813424"></a>
## See Also

[binding delayed](console_commands.binding_delayed.php "binding delayed")

| [Prev](console_commands.authz_roles_list.php)  | [Up](console.cmds.ref.php) |  [Next](console_commands.binding_delayed.php) |
| authz roles list  | [Table of Contents](index.php) |  binding delayed |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)