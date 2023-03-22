---
sidebar_position: 2
sidebar_label: 'Create Labels with Flow'
---

# Add Labels to the StickIt Queue with Flow Actions

:::note
This tutorial assumes you have a basic understanding of how to automate business processes with Flow Builder.
:::

1. Add an **Action** element.
![screenshot 1](/img/click_action_element.png)

1. Click the **Filter By** field.
![screenshot 2](/img/click_filter_by.png)

1. Select **Type** from the menu.
![screenshot 3](/img/click_action_type.png)

1. Click **Apex Action** from the list.
![screenshot 4](/img/click_apex_action.png)

1. Search for and select `TSS_StickIt_MR1__stickItInvocableAddToQueue`.
![screenshot 5](/img/click_invocable.png)

1. Type a label for the **Action** (_the API Name field should auto-populate_)
![screenshot 6](/img/type_action_label_name.png)

1. Enter input values for the following fields:
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
![screenshot 7](/img/type_action_inputs.png)

1. Click **Done**
![screenshot 8](/img/click_action_done.png)
