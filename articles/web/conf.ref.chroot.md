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

| chroot |
| [Prev](conf.ref.capabilities.php)  | 9.2. Configuration Files and Option Details |  [Next](conf.ref.clear_mail_queue_maintainers.php) |

<a name="conf.ref.chroot"></a>
## Name

chroot — chroot to a secure environment

## Synopsis

`Security { chroot = "/chroot/dir" }`

<a name="idp4528752"></a>
## Description

This security feature invokes the underlying operating system's `chroot` call to place Momentum in an alternate root directory. This can be used to limit the portions of the file system that are available to Momentum and can be an added protection should the instance be compromised.

Since Windows does not have a `chroot` system call, this option has no effect on Windows platforms.

### Note

Momentum is no longer supported on Windows.

The default value for this option is to use no chroot.

<a name="idp4533888"></a>
## Scope

chroot is valid in the security scope.

<a name="idp4535520"></a>
## See Also

[chroot](conf.ref.chroot.php "chroot"), [supplemental_groups](conf.ref.supplemental_groups.php "supplemental_groups"), [capabilities](conf.ref.capabilities.php "capabilities")

| [Prev](conf.ref.capabilities.php)  | [Up](conf.ref.files.php) |  [Next](conf.ref.clear_mail_queue_maintainers.php) |
| capabilities  | [Table of Contents](index.php) |  clear_mail_queue_maintainers |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)