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

| Momentum 4 Reference Manual |

**List of Figures**

<dl>

<dt>1.1\. [Momentum 4 Components](components.php#architecture.image)</dt>

<dt>2.1\. [Life of A Message](loam.php#life_of_a_message.image)</dt>

<dt>5.1\. [Configuration Options](hardware.config_options.php#config_options.image)</dt>

<dt>22.1\. [DomainKeys schematic](using_domainkeys.php#figure_domainkeys_schematic)</dt>

<dt>23.1\. [DKIM schematic](using_dkim.php#figure_dkim_schematic)</dt>

<dt>43.1\. [Login](create_apikey.php#figure_admin_icon)</dt>

<dt>43.2\. [Create New API Key](create_apikey.php#figure_create_api_key)</dt>

<dt>44.1\. [admin Username](web-ui.apikeys.php#figure_username_icon)</dt>

<dt>44.2\. [API Keys Table](web-ui.apikeys.php#figure_apikeys_list)</dt>

<dt>44.3\. [Create New API Key](web-ui.apikeys.create.php#figure_create_apikey)</dt>

<dt>44.4\. [Update API Key](web-ui.apikeys.update.php#figure_update_apikey)</dt>

<dt>44.5\. [Edit API Key](web-ui.apikeys.update.php#figure_edit_apikey)</dt>

<dt>44.6\. [Delete API Key](web-ui.apikeys.delete.php#figure_delete_apikey)</dt>

<dt>44.7\. [Confirm Delete](web-ui.apikeys.delete.php#figure_confirm_delete_apikey)</dt>

<dt>48.1\. [Templates Table](web-ui.templates.php#figure_templates_list)</dt>

<dt>48.2\. [New Template](web-ui.templates.create.php#figure_new_template)</dt>

<dt>48.3\. [Template Details](web-ui.templates.create.php#figure_template_details)</dt>

<dt>48.4\. [HTML Content](web-ui.templates.create.php#figure_html_content)</dt>

<dt>48.5\. [Text Content](web-ui.templates.create.php#figure_text_content)</dt>

<dt>48.6\. [Test Data](web-ui.templates.preview.php#figure_test_data)</dt>

<dt>48.7\. [Preview Template](web-ui.templates.preview.php#figure_preview_template)</dt>

<dt>48.8\. [Preview Template Details](web-ui.templates.preview.php#figure_preview_details)</dt>

<dt>48.9\. [Send Test](web-ui.templates.preview.php#figure_select_test)</dt>

<dt>48.10\. [Send Test Form](web-ui.templates.preview.php#figure_send_test)</dt>

<dt>48.11\. [Publish Template](web-ui.templates.publish.php#figure_publish_template)</dt>

<dt>48.12\. [Delete Template](web-ui.templates.delete.php#figure_delete_template)</dt>

<dt>53.1\. [Engagement Report](complex_template.php#figure_engagement_example)</dt>

<dt>55.1\. [User Interface](web-ui.php#figure_summary_report)</dt>

<dt>55.2\. [Recipient Lists Table](web-ui.php#figure_recipient_list)</dt>

<dt>55.3\. [Upload New Recipient List](web-ui.php#figure_list_upload)</dt>

<dt>55.4\. [Example Recipient List Details](web-ui.php#figure_list_details)</dt>

<dt>55.5\. [Update Recipient List](web-ui.php#figure_list_update)</dt>

<dt>55.6\. [Confirm Delete](web-ui.php#figure_confirm_list_delete)</dt>

<dt>56.1\. [User Interface](reporting_ui.php#figure_summary)</dt>

<dt>56.2\. [Navigating the UI](reporting_ui.php#figure_navigation)</dt>

<dt>57.1\. [Navigating Reports](web-ui.reports.php#figure_navigation_menu)</dt>

<dt>57.2\. [Metrics Drop-down List](web-ui.reports.php#figure_metrics_list)</dt>

<dt>57.3\. [Summary Graph](web-ui.reports.php#figure_summary_graph)</dt>

<dt>57.4\. [Summary Table](web-ui.reports.php#figure_summary_table)</dt>

<dt>57.5\. [Time Period Drop-down List](web-ui.reports.php#figure_time)</dt>

<dt>57.6\. [Custom Range](web-ui.reports.php#figure_custom_range)</dt>

<dt>57.7\. [Node Drop-down List](web-ui.reports.php#figure_node)</dt>

<dt>57.8\. [Filter by Search](web-ui.reports.php#figure_filter_by_search)</dt>

<dt>57.9\. [Filter by Table Entry](web-ui.reports.php#figure_filter_by_entry)</dt>

<dt>57.10\. [Bounces Report](web-ui.reports.viewing.reports.php#figure_bounces_report)</dt>

<dt>57.11\. [Bounce Rates By Type and By Category](web-ui.reports.viewing.reports.php#figure_bounces_by_category)</dt>

<dt>57.12\. [Bounce Messages Table](web-ui.reports.viewing.reports.php#figure_bounce_messages)</dt>

<dt>57.13\. [Rejections Report](web-ui.reports.viewing.reports.php#figure_rejections_report)</dt>

<dt>57.14\. [Accepted Report](web-ui.reports.viewing.reports.php#figure_accepted_report)</dt>

<dt>57.15\. [Delayed Report](web-ui.reports.viewing.reports.php#figure_delayed_report)</dt>

<dt>57.16\. [Adaptive Delivery Report](web-ui.reports.adaptive.delivery.php#figure_adaptive_report)</dt>

<dt>57.17\. [Time Period Drop-down List](web-ui.reports.adaptive.delivery.php#figure_adaptive_time)</dt>

<dt>57.18\. [Adaptive Delivery Graph](web-ui.reports.adaptive.delivery.php#figure_suspension_detail)</dt>

<dt>57.19\. [Expanded View](web-ui.reports.adaptive.delivery.php#figure_suspension_detailed)</dt>

<dt>57.20\. [Adaptive Delivery Table](web-ui.reports.adaptive.delivery.php#figure_adaptive_details)</dt>

<dt>57.21\. [Engagement Report](web-ui.reports.evaluating.campaign.performance.php#figure_engagement_report)</dt>

<dt>60.1\. [Webhooks List](web-ui.webhooks.php#figure_webhooks_list)</dt>

<dt>60.2\. [Create New Webhook](web-ui.webhooks.create.php#figure_create_webhook)</dt>

<dt>60.3\. [Event Types](web-ui.webhooks.create.php#figure_event_types)</dt>

<dt>60.4\. [Test Webhook](web-ui.webhooks.test.php#figure_test_webhook)</dt>

<dt>60.5\. [Test Request](web-ui.webhooks.test.php#figure_test_request)</dt>

<dt>60.6\. [Test Response](web-ui.webhooks.test.php#figure_test_response)</dt>

<dt>60.7\. [Update Webhook](web-ui.webhooks.update.php#figure_update_webhook)</dt>

<dt>60.8\. [Edit Webhook](web-ui.webhooks.update.php#figure_edit_webhook)</dt>

<dt>60.9\. [Delete Webhook](web-ui.webhooks.delete.php#figure_delete_webhook)</dt>

<dt>60.10\. [Confirm Delete](web-ui.webhooks.delete.php#figure_confirm_delete)</dt>

<dt>61.1\. [Engagement Report](engagement_tracking_http.php#figure_engagement)</dt>

<dt>62.1\. [Momentum Policy Phases](policy.php#policy.flow-diagram)</dt>

<dt>70.1\. [Counter semantics](lua.ref.msys.counter.open.php#fig.console_command.counter)</dt>

<dt>72.1\. [Connection Allocation Aggressiveness](conf.ref.connection_allocation_aggressiveness.php#conf.ref.connagg-diagram)</dt>

</dl>

|   | [Table of Contents](index.php) |   |

Follow us on:

[![Facebook](https://support.messagesystems.com/images/icon-facebook.png)](http://www.facebook.com/messagesystems) [![Twitter](https://support.messagesystems.com/images/icon-twitter.png)](http://twitter.com/#!/MessageSystems) [![LinkedIn](https://support.messagesystems.com/images/icon-linkedin.png)](http://www.linkedin.com/company/message-systems)