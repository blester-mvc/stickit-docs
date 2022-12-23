---
sidebar_position: 9
sidebar_label: 'Field Update Macro'
---

# Field Update Macro

Using field macros, you can update fields as part of the printing process.

### To update a single field on a record:

Format:  
`Id->field|type|value`  

Example:  
`{Id}->Checkbox__c|Boolean|TRUE`

### To update multiple fields on a single record:

Format:  
`Id->field|type|value~field|type|val~...`  

Example:  
`{Id}->Checkbox__c|Boolean|TRUE~Received_Date__c|Date|TODAY`

### To update fields on multiple records:

Format:  
`Id->field|type|val*Id->field|type|val`  

Example:  
`{Id}->Checkbox__c|Boolean|TRUE*{Account.Id}->Info__c|Text|foobar`

:::info
Supported Types:​

- Text
- Number
- Boolean
- Date
- DateTime
:::
:::tip
 For Date and DateTime fields, you may use ADD_DAYS:N to populate a calculated value using todays date as a baseline.

 Format:  
 `Id->field|Date|ADD_DAYS:N`  
 `Id->field|DateTime|ADD_DAYS:N`  

 Example:  
 `{Id}->Expiration_Date__c|Date|ADD_DAYS:30`
:::