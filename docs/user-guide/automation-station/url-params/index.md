---
sidebar_position: 2
sidebar_label: 'URL Parameters'
---

# Automation Station URL Parameters

`autoPrint`  
Toggle the Auto Print switch to "On" by default when the page loads. Default is "Off."  

 - Accepted values:
   - 0
   - Off
   - 1
   - On
```
/apex/TSS_StickIt_MR1__StickIt_Automation_Station?autoPrint=1
```

`printLocation`  
Set the Print Location / Queue to monitor by default
 - Accepted values: Any valid StickIt Queue Print Location
```
/apex/TSS_StickIt_MR1__StickIt_Automation_Station?printLocation=001
```

`printer`  
Set the DYMO printer to use by default for incoming labels
 - Accepted values: Any valid DYMO printer name connected to the PC
```
/apex/TSS_StickIt_MR1__StickIt_Automation_Station?printer=DYMO+LabelWriter+450
```

`roll`  
For twin turbo printers, the side of the printer to print on by default
 - Accepted values:
   - L
   - Left
   - R
   - Right
```
/apex/TSS_StickIt_MR1__StickIt_Automation_Station?roll=R
```

`showPreview`  
Suppress image previews for received labels. Can help to prevent performance issues in some cases.
 - Accepted values: 
   - 0
   - Off
   - 1
   - On
```
/apex/TSS_StickIt_MR1__StickIt_Automation_Station?showPreview=Off
```

`printQuality`  
To force the print quality/speed regardless of label contents
 - Accepted values: 
   - Text
   - BarcodeAndGraphics
   - Auto
:::info
**Text** = Fast  
**BarcodeAndGraphics** = Slow  
**Auto** = Framework will decide based on label contents (default)
:::
```
/apex/TSS_StickIt_MR1__StickIt_Automation_Station?printQuality=text
```

`rateLimit`  
Used to identify how long (milliseconds) to wait between triggering print executions. Useful when multiple records are being added to the queue at once, or in rapid succession.
 - Accepted values: Any valid integer, default is 1000
```
/apex/TSS_StickIt_MR1__StickIt_Automation_Station?rateLimit=2500
```

`limit`  
Limit the number of labels that are retained on the page after receipt. Helps prevent performance issues when the list gets long.
 - Accepted values: Any valid integer
```
/apex/TSS_StickIt_MR1__StickIt_Automation_Station?limit=25
```

`printConfig`  
When it is desirable to monitor multiple locations and associate specific print locations with various printers
 - Accepted value: {"printLocation":{"printer":"printerName","roll":"L/R"}}
```
/apex/TSS_StickIt_MR1__StickIt_Automation_Station?printConfig={"001":{"printer":"DYMO LabelWriter 450","roll":""},"002":{"printer":"DYMO LabelWriter 450 Twin Turbo","roll":"L"},"003":{"printer":"DYMO LabelWriter 4XL","roll":""}}
```
**For Readability**:
```
{

    "001":{"printer":"DYMO LabelWriter 450","roll":""},

    "002":{"printer":"DYMO LabelWriter 450 Twin Turbo","roll":"L"},

    "003":{"printer":"DYMO LabelWriter 450 Twin Turbo","roll":"R"}

}
```

`pushTopic`  
When it is required to have different instances of the StickIt Automation Station subscribed to different channels (Push Topics). Useful if you are operating in multiple locations.
 - Accepted Value: Any valid Push Topic name
```
/apex/TSS_StickIt_MR1__StickIt_Automation_Station?pushTopic=MY_CUSTOM_TOPIC
```