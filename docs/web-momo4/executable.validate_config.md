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

| validate_config |
| [Prev](executable.lu_pull.php)  | Chapter 74. Executable Commands Reference |  [Next](p.appendix.php) |

<a name="executable.validate_config"></a>
## Name

validate_config — check the validity of the configuration files

## Synopsis

`/opt/msys/ecelerity/bin/validate_config`

<a name="idp12707296"></a>
## Description

This script checks the validity of configuration files. It returns the following messages:

*   `Configuration valid` - Your configuration is valid.

*   `No configuration found` - There is no configuration file.

*   *No message is displayed*                      - Your configuration is invalid.

Using the **ec_dump_config** command may provide more information.

This script is especially useful for confirming the validity of manual changes to a configuration file.

<a name="idp10882976"></a>
## See Also

[Section 15.1.4, “Changing Configuration Files”](conf.overview.php#conf.manual.changes "15.1.4. Changing Configuration Files"), [ec_dump_config](executable.ec_dump_config.php "ec_dump_config")

| [Prev](executable.lu_pull.php)  | [Up](exec.cmds.ref.php) |  [Next](p.appendix.php) |
| lu_pull  | [Table of Contents](index.php) |  Part XI. Appendix |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)