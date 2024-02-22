---
title: "Phone Number Format"
date: 2024-01-22 12:30:00 +/-0800   
categories: [Pega,Edit validate rule,Edit Input rule]
math: true
mermaid: true
tags: [Pega,Phone Number Format,Edit validate rule,Pattern Validation]
# image: "/assets/img/post/LV.png"
# image:
#   path:  /assets/img/post/LV.png
#   width: 1000   # in pixels
#   height: 400   # in pixels
#   alt: Login Validation
---
## Edit Validate rules
## Format
* Ex: `9876543210`

```bash
// regex to check Phone
String regex = ("^[6-9]{1}[0-9]{9}$");

// Compile the ReGex
  java.util.regex.Pattern p=java.util.regex.Pattern.compile(regex);

// If the string is empty, return false
if (theValue == null || theValue.trim().equals("")) return false;
theProperty.addMessage("Please enter valid indian Phone Number");

// Pattern class contains matches() method to match the given string and regular expression
java.util.regex.Matcher m = p.matcher(theValue);
return m.matches();
```

## Edit Input rules
* For Auto Spacing
    * Input (Ex: `9876543210`)
    * Output (Ex: `98765 43210`)

```bash
if (theValue.length() == 10)
{
String temp=theValue.toString();
theValue= temp.substring(0,5)+" "+temp.substring(5,10);
};
```
## Reference 
[Click Here](https://docs-previous.pega.com/reference/87/about-edit-validate-rules?){:target="_blank"} - **More details from pega academy for Edit Validate rules** 

[Click Here](https://docs-previous.pega.com/reference/87/about-edit-input-rules){:target="_blank"} - **More details from pega academy for Edit Input rules** 