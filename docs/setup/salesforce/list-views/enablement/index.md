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
![screenshot 1](/img/home.png)

1. Select **Setup** from the menu.
![screenshot 2](/img/gear_menu.png)

1. Type "Visualforce Pages" into the `Quick Find` box and then select **Visualforce Pages**.
![screenshot 3](/img/quick_find_visualforce_pages.png)

1. Click the **New** button.
![screenshot 4](/img/visualforce_pages_home.png)

1. Complete the following fields:
  - Label
  - Name
  - Available for Lightning Experience
  - Visualforce Markup
![screenshot 5](/img/visualforce_page_listview.png)

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
