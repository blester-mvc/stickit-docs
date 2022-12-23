---
sidebar_position: 2
sidebar_label: 'Create Labels with Flow'
---

# Add Labels to the StickIt Queue with Flow Actions

:::note
This tutorial assumes you have a basic understanding of how to automate business processes with Flow Builder.
:::

1. Add an **Action** element.

1. Click the **Filter By** field.

1. Select **Type** from the menu.

1. Click on the **Action** input and select `TSS_StickIt_MR1__stickItInvocableAddToQueue`.

1. Complete the following fields:
- Label
- labelName 
- orderByField _(Name)_
:::info
Some Salesforce objects do not have a **Name** field. If this flow applies to one of those objects, use any other valid Field API Name for the object.
:::
- printLocation
:::info
This value should match a valid value in the Printer picklist on the StickIt Queue object)
:::
- recordId
- templateId _(The 18-character record Id of the label template File)_