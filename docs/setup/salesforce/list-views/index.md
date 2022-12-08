---
sidebar_position: 2
---

# Configure List Views

1. Click Setup
1. Click the arrow next to Develop
1. Click Pages
1. Click New
1. Type a label for your new page in the Label field and Press Tab
1. Replace the contents of the page with the code below:
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
1. *Note: You may specify any field API name on the associated object as the field to order by.
1. Click Save
