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

| Part II. Command Reference |
| [Prev](sieve.ecaddons.php)  |   |  [Next](conf.ref.php) |

## Part II. Command Reference

**Table of Contents**

<dl class="toc">

<dt>[9\. Ecelerity.conf Configuration Reference](conf.ref.php)</dt>

<dd>

<dl>

<dt>[9.1\. Options Summary](options-summary.php)</dt>

<dt>[9.2\. Configuration Files and Option Details](conf.ref.files.php)</dt>

</dl>

</dd>

<dt>[10\. Cluster Configuration Reference](cluster.ref.php)</dt>

<dd>

<dl>

<dt>[eccluster.conf](eccluster.conf.php) — Momentum Cluster Manager configuration file</dt>

<dt>[eccluster-client.conf](eccluster-client.conf.php) — Momentum Cluster Messaging Bus configuration file</dt>

<dt>[mbus.conf](mbus.conf.php) — Momentum Cluster Messaging Bus configuration file</dt>

</dl>

</dd>

<dt>[11\. Momentum Command Line Reference](exe.php)</dt>

<dd>

<dl>

<dt>[11.1\. Executable Command Summary](exe.summary_table2.php)</dt>

<dt>[11.2\. Executable Commands](exe.commands.details.php)</dt>

</dl>

</dd>

<dt>[12\. Momentum System Console Commands Reference](console_commands.php)</dt>

<dd>

<dl>

<dt>[12.1\. System Console Command Summary](console_commands.summary_table2.php)</dt>

<dt>[12.2\. System Console Commands](console.commands.non-module.php)</dt>

</dl>

</dd>

<dt>[13\. Modules](modules.overview.php)</dt>

<dd>

<dl>

<dt>[13.1\. Module-Specific Console Commands](module_specific_console_commands.php)</dt>

</dl>

</dd>

<dt>[14\. Modules Reference](modules.php)</dt>

<dd>

<dl>

<dt>[14.1\. alias – Alias Expansion Module](modules.alias.php)</dt>

<dt>[14.2\. antivirus – Antivirus Modules](modules.antivirus.php)</dt>

<dt>[14.3\. as_logger – Audit series logger](modules.as_logger.php)</dt>

<dt>[14.4\. auth_ds – Datasource based SMTP Authentication](modules.auth_ds.php)</dt>

<dt>[14.5\. auth_ldap – LDAP Based SMTP Authentication](modules.auth_ldap.php)</dt>

<dt>[14.6\. auth_mysql – MySQL Based SMTP Authentication](modules.auth_mysql.php)</dt>

<dt>[14.7\. auth_radius – RADIUS based SMTP Authentication](modules.auth_radius.php)</dt>

<dt>[14.8\. beik – BEIK Module](modules.beik.php)</dt>

<dt>[14.9\. bounce_classifier – Bounce Classifier](modules.bounce_classifier.php)</dt>

<dt>[14.10\. bounce_logger – Momentum-Style Bounce Logging](modules.bounce_logger.php)</dt>

<dt>[14.11\. brightmail – Brightmail Module](modules.brightmail.php)</dt>

<dt>[14.12\. cidrdb – CIDRDB](modules.cidrdb.php)</dt>

<dt>[14.13\. clamav – ClamAV](modules.clamav.php)</dt>

<dt>[14.14\. cloudmark – Cloudmark Authority Module](modules.cloudmark.php)</dt>

<dt>[14.15\. commtouch_ctasd – Commtouch_ctasd Module](modules.commtouch.php)</dt>

<dt>[14.16\. compress_spool – Dynamic Spool Compression](modules.compress_spool.php)</dt>

<dt>[14.17\. conntrol – Fine-Grained Connection Control](modules.conntrol.php)</dt>

<dt>[14.18\. csapi – The Content Scanning API Module](modules.csapi.php)</dt>

<dt>[14.19\. custom_logger – Customizable Logging](modules.custom_logger.php)</dt>

<dt>[14.20\. delay_dsn – Delay DSN Generation](modules.delay_dsn.php)</dt>

<dt>[14.21\. disclaimer – Module](modules.disclaimer.php)</dt>

<dt>[14.22\. dkim – DomainKeys Identified Mail Signatures](modules.dkim.php)</dt>

<dt>[14.23\. dns_rbl – DNS Blocklists](modules.dns_rbl.php)</dt>

<dt>[14.24\. domainkeys – Yahoo! DomainKeys](modules.domainkeys.php)</dt>

<dt>[14.25\. ds_core – Datasource Query Core](modules.ds_core.php)</dt>

<dt>[14.26\. ec_logger – Momentum-Style Logging](modules.ec_logger.php)</dt>

<dt>[14.27\. eleven – Module](modules.eleven.php)</dt>

<dt>[14.28\. exim_logger – Exim-Compatible Logging](modules.exim_logger.php)</dt>

<dt>[14.29\. fsecure – F-Secure](modules.fsecure.php)</dt>

<dt>[14.30\. fingerprint – Host Fingerprinting](modules.host_fingerprint.php)</dt>

<dt>[14.31\. http_io – HTTP I/O Provider](modules.httpio.php)</dt>

<dt>[14.32\. icu – ICU](modules.icu.php)</dt>

<dt>[14.33\. inbound_audit – Inbound traffic analytics](modules.inbound_audit.php)</dt>

<dt>[14.34\. jlog – The jlog Module](modules.jlog.php)</dt>

<dt>[14.35\. kaspersky – Kaspersky](modules.kaspersky.php)</dt>

<dt>[14.36\. mail_loop – Mail Loop Detection](modules.mail_loop.php)</dt>

<dt>[14.37\. maildir – Maildir Delivery Support](modules.maildir.php)</dt>

<dt>[14.38\. mtamark – MTAMARK](modules.mtamark.php)</dt>

<dt>[14.39\. outbound_audit – Outbound traffic analytics](modules.outbound_audit.php)</dt>

<dt>[14.40\. persist_io – Persistent IO Wrapper](modules.persistio.php)</dt>

<dt>[14.41\. pickup – MS SMTP Service Style "Pickup" module (Windows only, now deprecated)](modules.pickup.php)</dt>

<dt>[14.42\. pipe_io – Pipe IO Wrapper](modules.pipeio.php)</dt>

<dt>[14.43\. pipe_transport – Module](modules.pipe_transport.php)</dt>

<dt>[14.44\. postfix_logger – Postfix-Compatible Logging](modules.postfix_logger.php)</dt>

<dt>[14.45\. regex_binding – Regular Expression Based Bindings](modules.regex_binding.php)</dt>

<dt>[14.46\. regex_binding2 – Regular Expression Based Bindings (II)](modules.regex_binding2.php)</dt>

<dt>[14.47\. response_transcode – Module](modules.response_transcode.php)</dt>

<dt>[14.48\. sched – The Schedule Module](modules.sched.php)</dt>

<dt>[14.49\. seedlist – Seedlist Integration](modules.seedlist.php)</dt>

<dt>[14.50\. sendmail_logger – Sendmail-Compatible Logging](modules.sendmail_logger.php)</dt>

<dt>[14.51\. sieve – The Sieve Module](modules.sieve.php)</dt>

<dt>[14.52\. sievelib – The sievelib Module](modules.sievelib.php)</dt>

<dt>[14.53\. smtp_cbv – SMTP Callback Verification](modules.smtp_cbv.php)</dt>

<dt>[14.54\. spf Modules – spf_macros, spf_v1 and senderid (SPF v2)](modules.spf.php)</dt>

<dt>[14.55\. stats_producer – Stats Producer Module](modules.stats_producer.php)</dt>

<dt>[14.56\. suppress_spool – Deferred Message Spooling](modules.suppress_spool.php)</dt>

<dt>[14.57\. syslog_io – The syslog_io Module](modules.syslog_io.php)</dt>

<dt>[14.58\. url_ripper – URL Extraction](modules.url_ripper.php)</dt>

</dl>

</dd>

<dt>[15\. Sieve++ Function Reference](sieve.ref.php)</dt>

<dd>

<dl>

<dt>[add_recipient](sieve.ref.add_recipient.php) — add a new envelope recipient to the mail</dt>

<dt>[address](sieve.ref.address.php) — return the address from a header</dt>

<dt>[advertize_esmtp_capability](sieve.ref.advertize_esmtp_capability.php) — add a string to the EHLO response</dt>

<dt>[antivirus](sieve.ref.antivirus.php) — antivirus functions for Sieve</dt>

<dt>[audit_connections_on_listener](sieve.ref.audit_connections_on_listener.php) — Return the number of connections currently established from a CIDR block</dt>

<dt>[audit_connections_on_service](sieve.ref.audit_connections_on_service.php) — Return the number of connections currently established from a CIDR block</dt>

<dt>[audit_series](sieve.ref.audit_series.php) — Return the audit series count associated with an IP address or CIDR block over a window range</dt>

<dt>[audit_series_add](sieve.ref.audit_series_add.php) — Add to a named series</dt>

<dt>[audit_service](sieve.ref.audit_service.php) — Return how many connections currently are established from a CIDR block to an arbitrary service</dt>

<dt>[brightmail](sieve.ref.brightmail.php) — brightmail functions for Sieve</dt>

<dt>[cidrdb](sieve.ref.cidrdb.php) — cidr functions for Sieve</dt>

<dt>[cloudmark_score](sieve.ref.cloudmark_score.php) — Analyze a message with Cloudmark Authority</dt>

<dt>[commtouch_scan](sieve.ref.commtouch_scan.php) — email virus scan</dt>

<dt>[disable_esmtp_capability](sieve.ref.disable_esmtp_capability.php) — remove a string from the EHLO response</dt>

<dt>[discard](sieve.ref.discard.php) — discard the current message; it will not be delivered</dt>

<dt>[disclaimer_add](sieve.ref.disclaimer_add.php) — add a disclaimer to an email</dt>

<dt>[ds_execute](sieve.ref.ds_execute.php) — execute a query on a datasource</dt>

<dt>[ds_fetch](sieve.ref.ds_fetch.php) — query and fetch a row from a datasource</dt>

<dt>[ds_fetch_flat](sieve.ref.ds_fetch_flat.php) — query and fetch all rows from a datasource</dt>

<dt>[ds_fetch_hash](sieve.ref.ds_fetch_hash.php) — query and fetch a row from a datasource, as a hash</dt>

<dt>[ec_action](sieve.ref.ec_action.php) — set SMTP status code</dt>

<dt>[ec_add](sieve.ref.ec_add.php) — perform addition of two numbers</dt>

<dt>[ec_base64_decode](sieve.ref.ec_base64_decode.php) — decode base64 encoded text</dt>

<dt>[ec_base64_encode](sieve.ref.ec_base64_encode.php) — base64 encode text</dt>

<dt>[ec_bounce_classify](sieve.ref.ec_bounce_classify.php) — perform bounce classification on the message</dt>

<dt>[ec_ceil](sieve.ref.ec_ceil.php) — round up to the nearest integer</dt>

<dt>[ec_cluster_cache_get](sieve.ref.ec_cluster_cache_get.php) — Retrieve a value from a cluster-wide replicated cache</dt>

<dt>[ec_cluster_cache_set](sieve.ref.ec_cluster_cache_set.php) — Set a value in a cluster-wide replicated cache</dt>

<dt>[ec_config](sieve.ref.ec_config.php) — get Momentum configuration from Sieve</dt>

<dt>[ec_disconnect](sieve.ref.ec_disconnect.php) — set SMTP status and close the SMTP connection</dt>

<dt>[ec_div](sieve.ref.ec_div.php) — perform division of two numbers</dt>

<dt>[ec_dk_responsible_domain](sieve.ref.ec_dk_responsible_domain.php) — Return the responsible domain for the current message</dt>

<dt>[ec_dk_sign](sieve.ref.ec_dk_sign.php) — Sign a message with the DomainKeys protocol</dt>

<dt>[ec_dkim_domains](sieve.ref.ec_dkim_domains.php) — Return a list of valid signing domains</dt>

<dt>[ec_dkim_responsible_domain](sieve.ref.ec_dkim_responsible_domain.php) — Return the responsible domain for the current message</dt>

<dt>[ec_dkim_sign](sieve.ref.ec_dkim_sign.php) — Sign a message with the DKIM protocol</dt>

<dt>[ec_dns_lookup](sieve.ref.ec_dns_lookup.php) — perform a DNS record lookup</dt>

<dt>[ec_error_mode](sieve.ref.ec_error_mode.php) — set the error mode to "fail" or "continue"</dt>

<dt>[ec_floor](sieve.ref.ec_floor.php) — round down to the nearest integer</dt>

<dt>[ec_forward](sieve.ref.ec_forward.php) — forward a message</dt>

<dt>[ec_gauge_cache](sieve.ref.ec_gauge_cache.php) — gauge cache functions for Sieve</dt>

<dt>[ec_get_message_code](sieve.ref.ec_get_message_code.php) — Returns the current SMTP status code for a message</dt>

<dt>[ec_get_message_creation_time](sieve.ref.ec_get_message_creation_time.php) — Return the creation_time of the current message.</dt>

<dt>[ec_get_message_id](sieve.ref.ec_get_message_id.php) — Returns the message's unique ID.</dt>

<dt>[ec_get_message_mailfrom](sieve.ref.ec_get_message_mailfrom.php) — Return the mailfrom of the current message.</dt>

<dt>[ec_get_message_num_retries](sieve.ref.ec_get_message_num_retries.php) — Return the num_retries of the current message.</dt>

<dt>[ec_get_message_protocol](sieve.ref.ec_get_message_protocol.php) — Return the protocol of the current message.</dt>

<dt>[ec_get_message_rcptto](sieve.ref.ec_get_message_rcptto.php) — Return the rcptto of the current message.</dt>

<dt>[ec_get_message_received_from](sieve.ref.ec_get_message_received_from.php) — Return the IP address that the message was received from</dt>

<dt>[ec_get_message_received_from_port](sieve.ref.ec_get_message_received_from_port.php) — Return the port that the message was received from.</dt>

<dt>[ec_get_message_received_via](sieve.ref.ec_get_message_received_via.php) — Return the IP address that the message was received via</dt>

<dt>[ec_get_message_received_via_port](sieve.ref.ec_get_message_received_via_port.php) — Return the local port that the message was received on.</dt>

<dt>[ec_get_message_size](sieve.ref.ec_get_message_size.php) — Return the size of the current message.</dt>

<dt>[ec_get_message_spool_name](sieve.ref.ec_get_message_spool_name.php) — Returns the message's spool filename.</dt>

<dt>[ec_header_add](sieve.ref.ec_header_add.php) — prepend a header to the current message</dt>

<dt>[ec_header_delete](sieve.ref.ec_header_delete.php) — remove a header from the current message</dt>

<dt>[ec_header_get](sieve.ref.ec_header_get.php) — obtain the values for a particular header</dt>

<dt>[ec_header_postfix](sieve.ref.ec_header_postfix.php) — append to a header of the current message</dt>

<dt>[ec_header_prefix](sieve.ref.ec_header_prefix.php) — prepend to a header in the current message</dt>

<dt>[ec_host_fingerprint](sieve.ref.ec_host_fingerprint.php) — return genre and detail of the passive host fingerprinting operation</dt>

<dt>[ec_inc_counter](sieve.ref.ec_inc_counter.php) — increment a Sieve counter</dt>

<dt>[ec_include](sieve.ref.ec_include.php) — include and run a Sieve script</dt>

<dt>[ec_interfaces](sieve.ref.ec_interfaces.php) — obtain a list of network interfaces</dt>

<dt>[ec_ip_connections](sieve.ref.ec_ip_connections.php) — Audit how many connections an IP address has made</dt>

<dt>[ec_ip_connections_cluster](sieve.ref.ec_ip_connections_cluster.php) — Audit how many connections an IP address has made cluster-wide</dt>

<dt>[ec_ip_receptions](sieve.ref.ec_ip_receptions.php) — Audit how many receptions an IP address has made</dt>

<dt>[ec_ip_receptions_cluster](sieve.ref.ec_ip_receptions_cluster.php) — Audit how many receptions an IP address has made cluster-wide</dt>

<dt>[ec_ip_rejections](sieve.ref.ec_ip_rejections.php) — Audit how many rejections an IP address has made</dt>

<dt>[ec_ip_rejections_cluster](sieve.ref.ec_ip_rejections_cluster.php) — Audit how many rejections an IP address has made cluster-wide</dt>

<dt>[ec_log](sieve.ref.ec_log.php) — log to the paniclog</dt>

<dt>[ec_log_file](sieve.ref.ec_log_file.php) — log to a file/io wrapper</dt>

<dt>[ec_maildir](sieve.ref.ec_maildir.php) — write the current message into a maildir mailbox</dt>

<dt>[ec_mem_usage](sieve.ref.ec_mem_usage.php) — Return the amount of memory used by Momentum</dt>

<dt>[ec_mime_boundary_create](sieve.ref.ec_mime_boundary_create.php) — return a string to be used as a boundary when creating a MIME message</dt>

<dt>[ec_mime_parts](sieve.ref.ec_mime_parts.php) — test against metadata for each MIME part in a message</dt>

<dt>[ec_mod](sieve.ref.ec_mod.php) — calculate the modulus of two numbers</dt>

<dt>[ec_mul](sieve.ref.ec_mul.php) — perform multiplication of two numbers</dt>

<dt>[ec_nearbyint](sieve.ref.ec_nearbyint.php) — round to the nearest integer based on rounding direction</dt>

<dt>[ec_pcre_match](sieve.ref.ec_pcre_match.php) — perform a regular expression match</dt>

<dt>[ec_rand](sieve.ref.ec_rand.php) — generate a random number no larger than max -1 or a random string from a list.</dt>

<dt>[ec_rewrite_mailfrom](sieve.ref.ec_rewrite_mailfrom.php) — change the envelope sender</dt>

<dt>[ec_rfc2047_encode_addresses](sieve.ref.ec_rfc2047_encode_addresses.php) — create an RFC2047-compliant address</dt>

<dt>[ec_rfc2047_encode_header](sieve.ref.ec_rfc2047_encode_header.php) — encode a header to be RFC2047 compliant</dt>

<dt>[ec_rfc3464_delivery_status](sieve.ref.ec_rfc3464_delivery_status.php) — return a string containing fields for a RFC3464 DSN</dt>

<dt>[ec_round](sieve.ref.ec_round.php) — round away from zero</dt>

<dt>[ec_set_binding](sieve.ref.ec_set_binding.php) — Assign a message to a MultiVIP© binding</dt>

<dt>[ec_set_routing_gateway](sieve.ref.ec_set_routing_gateway.php) — dynamically change the gateway based on recipient</dt>

<dt>[ec_shared_throttle](sieve.ref.ec_shared_throttle.php) — Shared Named Throttling</dt>

<dt>[ec_spool_space](sieve.ref.ec_spool_space.php) — Return information about the free space on the spool partition</dt>

<dt>[ec_sub](sieve.ref.ec_sub.php) — perform subtraction of two numbers</dt>

<dt>[ec_tarpit](sieve.ref.ec_tarpit.php) — impose a time penalty</dt>

<dt>[ec_test](sieve.ref.ec_test.php) — generic test</dt>

<dt>[ec_thread_pool_get_queue_size](sieve.ref.ec_thread_pool_get_queue_size.php) — get the number of jobs queued against a jobclass</dt>

<dt>[ec_throttle](sieve.ref.ec_throttle.php) — Named Throttling</dt>

<dt>[ec_tolower](sieve.ref.ec_tolower.php) — change all characters to lower case</dt>

<dt>[ec_trace_context](sieve.ref.ec_trace_context.php) — add X-Trace-Context header to the current message</dt>

<dt>[ec_trunc](sieve.ref.ec_trunc.php) — round toward zero</dt>

<dt>[ec_url_ripper](sieve.ref.ec_url_ripper.php) — Extract domains and urls for lookup in DNSBL</dt>

<dt>[ec_valid_binding](sieve.ref.ec_valid_binding.php) — Check whether a named MultiVIP© binding exists</dt>

<dt>[ec_valid_mime](sieve.ref.ec_valid_mime.php) — determine if the message is valid MIME</dt>

<dt>[envelope](sieve.ref.envelope.php) — return the envelope sender or recipient</dt>

<dt>[generate_mail_raw](sieve.ref.generate_mail_raw.php) — generate and send out a message</dt>

<dt>[hash_create](sieve.ref.hash_create.php) — create a hash</dt>

<dt>[hash_dump](sieve.ref.hash_dump.php) — dump the contents of the hash to the paniclog</dt>

<dt>[hash_get](sieve.ref.hash_get.php) — get the value associated with the specified key</dt>

<dt>[hash_keys](sieve.ref.hash_keys.php) — return all the keys of a hash as a stringlist</dt>

<dt>[hash_set](sieve.ref.hash_set.php) — set an element in a hash</dt>

<dt>[hash_values](sieve.ref.hash_values.php) — return all the string values of a hash as a stringlist</dt>

<dt>[is_true](sieve.ref.is_true.php) — test if a value is "true"</dt>

<dt>[join](sieve.ref.join.php) — join stringlist elements into a single string</dt>

<dt>[keep](sieve.ref.keep.php) — keep the current message; stop processing further rules</dt>

<dt>[qp_encode](sieve.ref.qp_encode.php) — quoted-printable encode a string</dt>

<dt>[redirect](sieve.ref.redirect.php) — change the envelope recipient</dt>

<dt>[reject](sieve.ref.reject.php) — reject the message, returning an MDN to the sender</dt>

<dt>[reverse](sieve.ref.reverse.php) — reverse a string or a stringlist</dt>

<dt>[reverse_delim](sieve.ref.reverse_delim.php) — reverse a string based on a delimiter</dt>

<dt>[smtp_callback_verify](sieve.ref.smtp_callback_verify.php) — Perform smtp callback on an email address</dt>

<dt>[snmp_trap](sieve.ref.snmp_trap.php) — Send SNMP traps from a Sieve script</dt>

<dt>[split](sieve.ref.split.php) — split a string into a stringlist</dt>

<dt>[stop](sieve.ref.stop.php) — stop processing the current script</dt>

<dt>[thread_pool_stats](sieve.ref.thread_pool_stats.php) — Obtain information about thread pools</dt>

<dt>[type](sieve.ref.type.php) — test the type of the value in a Sieve variable</dt>

<dt>[vctx_conn_delete](sieve.ref.vctx_conn_delete.php) — delete a key from the connection context</dt>

<dt>[vctx_conn_get](sieve.ref.vctx_conn_get.php) — obtain the value of a connection context key</dt>

<dt>[vctx_conn_set](sieve.ref.vctx_conn_set.php) — set a value in the connection context</dt>

<dt>[vctx_mess_delete](sieve.ref.vctx_mess_delete.php) — delete a key from the message context</dt>

<dt>[vctx_mess_get](sieve.ref.vctx_mess_get.php) — obtain the value of a message context key</dt>

<dt>[vctx_mess_set](sieve.ref.vctx_mess_set.php) — set a value in the message context</dt>

</dl>

</dd>

</dl>

| [Prev](sieve.ecaddons.php)  |   |  [Next](conf.ref.php) |
| 8.4. Sieve++, Momentum-specific extensions  | [Table of Contents](index.php) |  Chapter 9. Ecelerity.conf Configuration Reference |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)