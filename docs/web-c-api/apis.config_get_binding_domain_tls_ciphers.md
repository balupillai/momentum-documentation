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

| config_get_binding_domain_tls_ciphers |
| [Prev](apis.config_get_binding_domain_tls_cert.php)  | Chapter 11. Configuration Functions I (binding/domain) |  [Next](apis.config_get_binding_domain_tls_key.php) |

<a name="apis.config_get_binding_domain_tls_ciphers"></a>
## Name

config_get_binding_domain_tls_ciphers — Determine the value of the tls_ciphers option

## Synopsis

`#include "ec_config.h"`

| `char * **config_get_binding_domain_tls_ciphers** (` | <var class="pdparam">caller_scope</var>, |   |
|   | <var class="pdparam">binding</var>, |   |
|   | <var class="pdparam">domain</var>`)`; |   |

`generic_module_infrastructure * <var class="pdparam">caller_scope</var>`;
`int <var class="pdparam">binding</var>`;
`const * <var class="pdparam">domain</var>`;<a name="idp21215504"></a>
## Description

Determine the value of the [tls_ciphers](https://support.messagesystems.com/docs/web-ref/conf.ref.tls_ciphers.php) configuration option.

### Note

The `caller_scope` argument is virtually always `NULL`; there is no reason for a consumer to make it anything else.

**Parameters**

<dl class="variablelist">

<dt>caller_scope</dt>

<dd>

For a definition of this data type see [Section 68.53, “generic_module_infrastructure”](structs.generic_module_infrastructure.php "68.53. generic_module_infrastructure").

</dd>

<dt>binding</dt>

<dd>

The binding identifier.

</dd>

<dt>domain</dt>

<dd>

The domain name.

</dd>

</dl>

**Return Values**

This function returns the value of the `tls_ciphers` option.

See [tls_ciphers](https://support.messagesystems.com/docs/web-ref/conf.ref.tls_ciphers.php) for more information.

**Threading**

It is legal to call this function in any thread.

<a name="idp21230128"></a>
## See Also

[config_get_binding_domain_tls_cert](apis.config_get_binding_domain_tls_cert.php "config_get_binding_domain_tls_cert"), [config_get_binding_domain_tls_verify](apis.config_get_binding_domain_tls_verify.php "config_get_binding_domain_tls_verify"), [config_get_binding_domain_tls_ca](apis.config_get_binding_domain_tls_ca.php "config_get_binding_domain_tls_ca"), [config_get_binding_domain_tls_key](apis.config_get_binding_domain_tls_key.php "config_get_binding_domain_tls_key") and [config_get_binding_domain_use_tls](apis.config_get_binding_domain_use_tls.php "config_get_binding_domain_use_tls")

| [Prev](apis.config_get_binding_domain_tls_cert.php)  | [Up](config_get1.php) |  [Next](apis.config_get_binding_domain_tls_key.php) |
| config_get_binding_domain_tls_cert  | [Table of Contents](index.php) |  config_get_binding_domain_tls_key |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)