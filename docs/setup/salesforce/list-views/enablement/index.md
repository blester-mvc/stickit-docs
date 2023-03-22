---
sidebar_position: 1
sidebar_label: 'Enablement'
---

# List View Enablement

Enable StickIt for use with _most_ Standard and Custom Object **List Views** by following these steps:

:::info
StickIt is enabled for the **Account**, **Contact** and **Lead** object list views out-of-the-box.
:::

1. Click the **gear** icon.
![screenshot 1](/img/click_gear.png)

1. Select **Setup** from the menu.
![screenshot 2](/img/click_setup.png)

1. Type "Visualforce Pages" into the `Quick Find` box and then select **Visualforce Pages**.
![screenshot 3](/img/click_vf_pages.png)

1. Click the **New** button.
![screenshot 4](/img/click_new_vf_page.png)

1. Complete the following fields:
  - Label
  - Name (_should auto-populate, but spaces will need to be replaced with underscores to prevent errors when saving_)
  - Available for Lightning Experience (_checked_)
  - Visualforce Markup (_markup template below_)
![screenshot 5](/img/type_vf_page_info_listviews.png)

1. Click **Save**
![screenshot 6](/img/click_save_vf_page_listviews.png)

### Markup Template

```
<apex:page 
  standardController="OBJECT_API_NAME"
  recordSetVar="items"
  extensions="TSS_StickIt_MR1.stickItListViewControllerv2"
  standardStylesheets="false" 
  showHeader="false" 
  sidebar="false" 
  applyHtmlTag="false" 
  applyBodyTag="false" 
  docType="html-5.0"
>
  <tss_stickit_mr1:stickit_dual 
      selectedRecords="{!records}"
      order_by="Name"
  />
</apex:page>
```
:::info
Replace `OBJECT_API_NAME` with the API Name of the Object you are enabling StickIt for.
:::
