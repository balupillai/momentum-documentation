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

| Chapter 3. Mobile Momentum SMPP Options |
| [Prev](mobility.runtime.hooks.php)  | Part I. Mobile Momentum SMPP |  [Next](mobility.conf.smpp_bind_response_timer.php) |

## Chapter 3. Mobile Momentum SMPP Options

**Table of Contents**

<dl class="toc">

<dt>[3.1\. SMPP Configuration Option Details](mobility.smpp.options.php#mobility.conf)</dt>

</dl>

This table displays all the non-module-specific configuration options used in configuring SMPP—options that are valid outside the module scope.

Options are sorted alphabetically by name. If an option has a default value, this value is shown and if there are a limited number of legal values these are also shown.

<a name="table-smpp-options"></a>

**Table 3.1. smpp options**

| Option/Description | Type | Default | Legal Values | Scopes |
| --- | --- | --- | --- | --- |
| [smpp_bind_response_timer](mobility.conf.smpp_bind_response_timer.php "smpp_bind_response_timer") – SMPP_Bind_Response_Timer specifies the amount of time that SMPP will wait for a response to an SMPP BIND request. | both | 0 |   | binding, binding_group, domain, global |
| [smpp_bind_type](mobility.conf.smpp_bind_type.php "smpp_bind_type") – The type of smpp binding to be established with the Short Message Service Center, which determines the role of transmitter-only, receiver-only, or both | both | transceiver | transceiver, transmitter, receiver | binding, binding_group, domain, global |
| [smpp_command_window_size](mobility.conf.smpp_command_window_size.php "smpp_command_window_size") – Defines the maximum number of outstanding SMPP messages in the SMPP connection pipeline | both | 10 |   | binding, binding_group, domain, global |
| [smpp_csms_refnum_length](mobility.conf.smpp_csms_refnum_length.php "smpp_csms_refnum_length") – Specifies the length of the CSMS number | sending | 2 | 0, 1, 2 | binding, binding_group, domain, global |
| [smpp_default_email_address](mobility.conf.smpp_default_email_address.php "smpp_default_email_address") – Specifies a destination email address to be used during SMS-to-email translation after other methods fail | both |   |   | binding, binding_group, domain, global |
| [smpp_default_email_from_domain](mobility.conf.smpp_default_email_from_domain.php "smpp_default_email_from_domain") – Specify the domain name to use in the source email when converting SMS to email | both |   |   | binding, binding_group, domain, global |
| [smpp_delivery_receipt_message_id_format](mobility.conf.smpp_delivery_receipt_message_id_format.php "smpp_delivery_receipt_message_id_format") – Declare the representation of message IDs | both | string | string, decimal, hexadecimal | binding, binding_group, domain, global |
| [smpp_destination_flag](mobility.conf.smpp_destination_flag.php "smpp_destination_flag") – Set the destination type | both | 1 | 1, 2 | binding, binding_group, domain, global |
| [smpp_destination_numbering_plan](mobility.conf.smpp_destination_numbering_plan.php "smpp_destination_numbering_plan") – The second of two parameters that specify the destination address | both | e164 | e164, unknown | binding, binding_group, domain, global |
| [smpp_destination_type_of_number](mobility.conf.smpp_destination_type_of_number.php "smpp_destination_type_of_number") – The first of two parameters that specify the destination address | both | international | international, unknown, national, network, subscriber number, alphanumeric, abbreviated, extension | binding, binding_group, domain, global |
| [smpp_enquire_link_timer](mobility.conf.smpp_enquire_link_timer.php "smpp_enquire_link_timer") – Specifies the amount of inactivity time (in seconds) on the SMPP session prior to sending an SMPP enquire_link request | both | 60 |   | binding, binding_group, domain, global |
| [smpp_enquire_response_timer](mobility.conf.smpp_enquire_response_timer.php "smpp_enquire_response_timer") – SMPP_Enquire_Response_Timer specifies the amount of time that SMPP will wait for a response to an SMPP ENQUIRE_LINK request. | both | 0 |   | binding, binding_group, domain, global |
| [smpp_esme_address](mobility.conf.smpp_esme_address.php "smpp_esme_address") – The third of the three SMS address parameters specifying the source address for SMS messages sent with SMPP | both |   |   | binding, binding_group, domain, global |
| [smpp_esme_max_bind_retries](mobility.conf.smpp_esme_max_bind_retries.php "smpp_esme_max_bind_retries") – The maximum number of retries upon an SMPP ESME Bind request failure or timeout. | both | 1 |   | binding, binding_group, domain, global |
| [smpp_esme_max_segments](mobility.conf.smpp_esme_max_segments.php "smpp_esme_max_segments") – Define the maximum number of SMS segments allowed when converted from an email | both | 255 |   | binding, binding_group, domain, global |
| [smpp_esme_numbering_plan](mobility.conf.smpp_esme_numbering_plan.php "smpp_esme_numbering_plan") – The second of three SMS address parameters that specify the source address for SMS messages sent with SMPP | both | e164 | e164, unknown | binding, binding_group, domain, global |
| [smpp_esme_service_type](mobility.conf.smpp_esme_service_type.php "smpp_esme_service_type") – This sets the SMPP service type field in submit_sm PDUs | both |   |   | binding, binding_group, domain, global |
| [smpp_esme_submit_data_sm](mobility.conf.smpp_esme_submit_data_sm.php "smpp_esme_submit_data_sm") – Specify whether a data_sm instead of a submit_sm is expected | both | false |   | binding, binding_group, domain, global |
| [smpp_esme_submit_submit_multi](mobility.conf.smpp_esme_submit_submit_multi.php "smpp_esme_submit_submit_multi") – Specify whether a submit_multi instead of submit_sm is expected from an ESME | both | false |   | binding, binding_group, domain, global |
| [smpp_esme_throttled_timeout](mobility.conf.smpp_esme_throttled_timeout.php "smpp_esme_throttled_timeout") – How long to wait after receiving an ESME_RTHROTTLED response | sending | 0 |   | binding, binding_group, domain, global |
| [smpp_esme_type_of_number](mobility.conf.smpp_esme_type_of_number.php "smpp_esme_type_of_number") – The first of three SMS address parameters that specify the source address for SMS messages sent with SMPP | both | unknown | international, unknown, national, network, subscriber number, alphanumeric, abbreviated, extension | binding, binding_group, domain, global |
| [smpp_esme_udh_segment](mobility.conf.smpp_esme_udh_segment.php "smpp_esme_udh_segment") – This option indicates whether UDH prepends each SMS segment when converted from an email | both | false |   | binding, binding_group, domain, global |
| [smpp_esme_validity_period](mobility.conf.smpp_esme_validity_period.php "smpp_esme_validity_period") – The value of the validity_period field used in submit_sm. | sending | NULL |   | binding, binding_group, domain, global |
| [smpp_gsm_transcodes_to](mobility.conf.smpp_gsm_transcodes_to.php "smpp_gsm_transcodes_to") – What character encoding GSM0338 text will be translated to when converting to email | both | ISO-8859-1 | Ascii, US-Ascii, Latin-1, Latin1, Iso-8859-1, Latin-5, Cyrillic, Iso-8859-5, Latin-8, Latin/Hebrew, Hebrew, Iso-8859-8, UCS2, UTF-16, UTF16 | binding, binding_group, domain, global |
| [smpp_inactivity_timer](mobility.conf.smpp_inactivity_timer.php "smpp_inactivity_timer") – The amount of inactivity time (in seconds, and excluding enquire_link activity) on the SMPP session prior to initiating session shutdown operations | both | 300 |   | binding, binding_group, domain, global |
| [smpp_max_sms_from_size](mobility.conf.smpp_max_sms_from_size.php "smpp_max_sms_from_size") – Specifies the maximum size (in octets) of the source email address to be included in the outgoing MT-SMS message | sending | 0 |   | binding, binding_group, domain, global |
| [smpp_max_sms_message_size](mobility.conf.smpp_max_sms_message_size.php "smpp_max_sms_message_size") – The maximum size of outgoing MT-SMS message text in octets | sending | 140, 160 (*3.3.3*) |   | binding, binding_group, domain, global |
| [smpp_max_sms_subject_size](mobility.conf.smpp_max_sms_subject_size.php "smpp_max_sms_subject_size") – The maximum size (in octets) of the source email subject to be included in the outgoing MT-SMS message | sending | 10 |   | binding, binding_group, domain, global |
| [smpp_message_mode](mobility.conf.smpp_message_mode.php "smpp_message_mode") – Specifies a message mode that is to override the default message mode used by the SMSC | both | store_and_forward | store_and_forward, transaction | binding, binding_group, domain, global |
| [smpp_notify_deliver_receipt](mobility.conf.smpp_notify_deliver_receipt.php "smpp_notify_deliver_receipt") – When to convert an email notification from an SMPP Deliver Receipt | both |   | ALL, DELIVRD, EXPIRED, DELETED, UNDELIV, ACCEPTD, UNKNOWN, REJECTD | binding, binding_group, domain, global |
| [smpp_persistent_connections](mobility.conf.smpp_persistent_connections.php "smpp_persistent_connections") – Specifies the number of SMPP TCP connections with the smsc that Momentum attempts to keep open on the named bindings | both |   |   | domain |
| [smpp_ram_cache](mobility.conf.smpp_ram_cache.php "smpp_ram_cache") – The datasource cache name used by SMPP for reverse address mappings records. | both | ram |   | binding, binding_group, domain, global |
| [smpp_ram_expiration](mobility.conf.smpp_ram_expiration.php "smpp_ram_expiration") – Set the expiration, in minutes, for Reverse Address Mappings records used by SMPP. | both | 300 |   | binding, binding_group, domain, global |
| [smpp_ram_query_lookup](mobility.conf.smpp_ram_query_lookup.php "smpp_ram_query_lookup") – The database query string for reverse address mappings lookup. | both | SELECT email_addr FROM smpp.reverse_address_mappings WHERE domain=:domain AND sms_addr=:sms_addr AND shortcode=:shortcode |   | binding, binding_group, domain, global |
| [smpp_ram_query_new](mobility.conf.smpp_ram_query_new.php "smpp_ram_query_new") – The query string for creating a new reverse address mappings record. | both | INSERT INTO smpp.reverse_address_mappings (domain, sms_addr, shortcode, email_addr, expiration) VALUES (:domain, :sms_addr, :shortcode, :email_addr, :expiration) |   | binding, binding_group, domain, global |
| [smpp_ram_query_update](mobility.conf.smpp_ram_query_update.php "smpp_ram_query_update") – The query string for updating an existing reverse address mappings record. | both | UPDATE smpp.reverse_address_mappings SET email_addr=:email_addr, expiration=:expiration WHERE domain=:domain AND sms_addr=:sms_addr AND shortcode=:shortcode |   | binding, binding_group, domain, global |
| [smpp_registered_delivery](mobility.conf.smpp_registered_delivery.php "smpp_registered_delivery") – Use this option to turn on one or more registered delivery flags in outgoing SMS messages, causing an SMSCs that supports it to return status indications | sending |   | SMSC_Delivery_Failure, SMSC_Delivery, intermediate, SME_Delivery, SME_User | binding, binding_group, domain, global |
| [smpp_response_timer](mobility.conf.smpp_response_timer.php "smpp_response_timer") – Specifies the amount of inactivity time (in seconds) on the SMPP session prior to sending an SMPP enquire_link request | both | 300 |   | binding, binding_group, domain, global |
| [smpp_sms_data_coding](mobility.conf.smpp_sms_data_coding.php "smpp_sms_data_coding") – specifies the data encoding to be used for outbound MT-SMS messages | sending | default | Default, Ascii, US-Ascii, Latin-1, Latin1, Iso-8859-1, Latin-5, Cyrillic, Iso-8859-5, Latin-8, Latin/Hebrew, Hebrew, Iso-8859-8, UCS2, UTF-16, UTF16 | binding, binding_group, domain, global |
| [smpp_sms_data_no_bom](mobility.conf.smpp_sms_data_no_bom.php "smpp_sms_data_no_bom") – Whether sms_text should be UTF-16BE or UTF-16/UCS2 | both | false, true (*3.3.3*) |   | binding, binding_group, domain, global |
| [smpp_sms_segment_boundary](mobility.conf.smpp_sms_segment_boundary.php "smpp_sms_segment_boundary") – Whether a word boundary is used to segment a concatenated message | sending | false |   | binding, binding_group, domain, global |
| [smpp_sms_segment_size](mobility.conf.smpp_sms_segment_size.php "smpp_sms_segment_size") – Defines the maximum size of each SMS segment when converted from an email | both | 140, 160 (*3.3.3*) |   | binding, binding_group, domain, global |
| [smpp_smsc_default_alphabet](mobility.conf.smpp_smsc_default_alphabet.php "smpp_smsc_default_alphabet") – specifies the default character encoding of the SMSC | receiving | GSM | Ascii, US-Ascii, Latin-1, Latin1, Iso-8859-1, Latin-5, Cyrillic, Iso-8859-5, Latin-8, Latin/Hebrew, Hebrew, Iso-8859-8, UCS2, UTF-16, UTF16, GSM, GSM0338 | binding, binding_group, domain, global |
| [smpp_smsc_default_message_mode](mobility.conf.smpp_smsc_default_message_mode.php "smpp_smsc_default_message_mode") – Specifies the default message mode used by the SMSC. "store_and_forward" and "transaction" modes are supported | both | store_and_forward | store_and_forward, transaction | binding, binding_group, domain, global |
| [smpp_smsc_password](mobility.conf.smpp_smsc_password.php "smpp_smsc_password") – The password associated with smpp_system_id for the Short Messaging Service Center | both |   |   | binding, binding_group, domain, global |
| [smpp_smsc_port](mobility.conf.smpp_smsc_port.php "smpp_smsc_port") – The SMPP TCP port number for the target Short Messaging Service Center | both | 2775 |   | domain, global |
| [smpp_smsc_server](mobility.conf.smpp_smsc_server.php "smpp_smsc_server") – The host name or IP address of the target Short Messaging Service Center | both |   |   | domain, global |
| [smpp_smsc_system_id](mobility.conf.smpp_smsc_system_id.php "smpp_smsc_system_id") – Specifies the System Identification name of the Short Messaging Service Center | both |   |   | binding, binding_group, domain, global |
| [smpp_smsc_system_type](mobility.conf.smpp_smsc_system_type.php "smpp_smsc_system_type") – The system type used when binding to the Short Messaging Service Center | both |   |   | binding, binding_group, domain, global |
| [smpp_submit_response_message_id_format](mobility.conf.smpp_submit_response_message_id_format.php "smpp_submit_response_message_id_format") – Declare the representation of message IDs | both | string | string, decimal, hexadecimal | binding, binding_group, domain, global |
| [smpp_submit_response_timer](mobility.conf.smpp_submit_response_timer.php "smpp_submit_response_timer") – SMPP_Submit_Response_Timer specifies the amount of time that SMPP will wait for a response to an SMPP SUBMIT_SM request. | both | 0 |   | binding, binding_group, domain, global |
| [smpp_submit_tracking_cache](mobility.conf.smpp_submit_tracking_cache.php "smpp_submit_tracking_cache") – The cache used with the SMPP submissions schema | both | ecdb |   | global |
| [smpp_submit_tracking_schema](mobility.conf.smpp_submit_tracking_schema.php "smpp_submit_tracking_schema") – The database used to track SMPP submissions | both | smpp |   | global |
| [smpp_use_interworking_parse](mobility.conf.smpp_use_interworking_parse.php "smpp_use_interworking_parse") – Determine if SMS to email processing invokes 23.040 SMS/email interworking_format parsing | both | true |   | binding, binding_group, domain, global |
| [smpp_use_reverse_address_mappings](mobility.conf.smpp_use_reverse_address_mappings.php "smpp_use_reverse_address_mappings") – Determines if email to MT-SMS processing saves associated pairs of source email addresses and destination SMS addresses | both | true |   | binding, binding_group, domain, global |
| [smpp_vendor_command_status_table](mobility.conf.smpp_vendor_command_status_table.php "smpp_vendor_command_status_table") – Define the path name to the vendor-specific command status codes | both |   |   | binding, binding_group, domain, global |
| [smpp_vendor_tlv_table](mobility.conf.smpp_vendor_tlv_table.php "smpp_vendor_tlv_table") – The path to a file defining vendor-specific type length values (TLVs) | both |   |   | binding, binding_group, domain, global |

## 3.1. SMPP Configuration Option Details

Detailed descriptions of the SMPP options follow.

| [Prev](mobility.runtime.hooks.php)  | [Up](p.smpp.php) |  [Next](mobility.conf.smpp_bind_response_timer.php) |
| 2.8. SMS Conversion Hook Points  | [Table of Contents](index.php) |  smpp_bind_response_timer |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)