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

| msys.policyeditor.set_variable |
| [Prev](lua.ref.msys.policyeditor.set_binding_group.php)  | 15.2. Lua Functions |  [Next](lua.ref.msys.policyeditor.vctx_mess_set.php) |

<a name="lua.ref.msys.policyeditor.set_variable"></a>
## Name

msys.policyeditor.set_variable — Set the value of a script variable

<a name="idp25086352"></a>
## Synopsis

`msys.policyeditor.set_variable(ctx, vars, params);`

```
ctx: table
vars: table
params: table
```

**Configuration Change. ** This function is deprecated. You can easily set a Lua variable as follows: `local x = y;` .

<a name="idp25091104"></a>
## Description

Set the value of a script variable

The `ctx` parameter is the context containing objects from the callout, `vars` is a table containing script variables and `params` is a table containing parameters to be passed to this routine.

Defined parameters for params are:

*   `name` the name of the variable to be set

*   `value` the value to set the variable to

<a name="idp25097936"></a>
## See Also

[msys.policyeditor.get_variable](lua.ref.msys.policyeditor.get_variable.php "msys.policyeditor.get_variable"), [Section 3.10.3, “Using Variables”](web3.policy.editor.php#web3.policy.editor.variables "3.10.3. Using Variables")

| [Prev](lua.ref.msys.policyeditor.set_binding_group.php)  | [Up](lua.function.details.php) |  [Next](lua.ref.msys.policyeditor.vctx_mess_set.php) |
| msys.policyeditor.set_binding_group  | [Table of Contents](index.php) |  msys.policyeditor.vctx_mess_set |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)