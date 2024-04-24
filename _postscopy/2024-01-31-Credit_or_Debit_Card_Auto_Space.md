---
title: "Debit Or Credit Card Auto Space"
date: 2024-01-31 12:30:00 +/-0800   
categories: [Pega,Edit Input rule]
math: true
mermaid: true
tags: [Pega,Credit / Debit Card Auto Space]
# image: "/assets/img/post/LV.png"
# image:
#   path:  /assets/img/post/LV.png
#   width: 1000   # in pixels
#   height: 400   # in pixels
#   alt: Login Validation
---
## Edit Input rules
* For Auto Spacing
    * Input (Ex: `1234123412341234`)
    * Output (Ex: `1234 1234 1234 1234`)

```bash
if (theValue.length() == 16)
{
String temp=theValue.toString();
theValue= temp.substring(0,4)+" "+temp.substring(4,8)+" "+temp.substring(8,12)+" "+temp.substring(12,16);
};
```
## Reference 
[Click Here](https://docs-previous.pega.com/reference/87/about-edit-input-rules){:target="_blank"} - **More details from pega academy for Edit Input rules** 