---
title: "Pincode Format"
date: 2024-02-01 12:30:00 +/-0800   
categories: [Pega,Edit validate rule]
math: true
mermaid: true
tags: [Pega,Edit validate rule,Pattern Validation]
# image: "/assets/img/post/LV.png"
# image:
#   path:  /assets/img/post/LV.png
#   width: 1000   # in pixels
#   height: 400   # in pixels
#   alt: Login Validation
---
## Edit Validate rules
## Format
* Ex: `638701`

```bash
// regex to check Phone
String regex = ("^[1-9]{1}[0-9]{5}$");

// Compile the ReGex
  java.util.regex.Pattern p=java.util.regex.Pattern.compile(regex);

// If the string is empty, return false
if (theValue == null || theValue.trim().equals("")) return false;
theProperty.addMessage("Please enter valid Pin Code");

// Pattern class contains matches() method to match the given string and regular expression
java.util.regex.Matcher m = p.matcher(theValue);
return m.matches();
```

## Reference 
[Click Here](https://docs-previous.pega.com/reference/87/about-edit-validate-rules?){:target="_blank"} - **More details from pega academy for Edit Validate rules** 
