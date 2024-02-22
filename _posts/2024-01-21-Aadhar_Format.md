---
title: "Aadhar Format"
date: 2024-01-21 12:30:00 +/-0800   
categories: [Pega,Edit validate rule,Edit Input rule]
math: true
mermaid: true
tags: [Pega,Aadhar Format,Edit validate rule,Pattern Validation,Edit Input Rule]
# image: "/assets/img/post/LV.png"
# image:
#   path:  /assets/img/post/LV.png
#   width: 1000   # in pixels
#   height: 400   # in pixels
#   alt: Login Validation
---
## Edit Validate rules
## Format - 1 (With Space)
* Ex: `2341 1234 1234`

```bash
// Regex to check valid Aadhaar number 
String regex= "^[2-9]{1}[0-9]{3}\\s[0-9]{4}\\s[0-9]{4}$";

// Compile the ReGex
  java.util.regex.Pattern p=java.util.regex.Pattern.compile(regex);

// If the string is empty, return false
if (theValue == null || theValue.trim().equals("")) return false;
theProperty.addMessage("Please enter valid Aadhar Number");

// Pattern class contains matches() method to match the given string and regular expression
java.util.regex.Matcher m = p.matcher(theValue);
return m.matches();
```
## Format - 2 (Without Space)
* Ex: `234112341234`

```bash
// Regex to check valid Aadhaar number 
String regex= "^[2-9]{1}[0-9]{3}[0-9]{4}[0-9]{4}$";

// Compile the ReGex
  java.util.regex.Pattern p=java.util.regex.Pattern.compile(regex);

// If the string is empty, return false
if (theValue == null || theValue.trim().equals("")) return false;
theProperty.addMessage("Please enter valid Aadhar Number");

// Pattern class contains matches() method to match the given string and regular expression
java.util.regex.Matcher m = p.matcher(theValue);
return m.matches();
```
## Edit Input rules
* For Auto Spacing
    * Input (Ex: `234112341234`)
    * Output (Ex: `2341 1234 1234`)

```bash
if (theValue.length() == 12)
{
String temp=theValue.toString();
theValue= temp.substring(0,4)+" "+temp.substring(4,8)+" "+temp.substring(8,12);
};
```
## Reference 
[Click Here](https://docs-previous.pega.com/reference/87/about-edit-validate-rules?){:target="_blank"} - **More details from pega academy for Edit Validate rules** 

[Click Here](https://docs-previous.pega.com/reference/87/about-edit-input-rules){:target="_blank"} - **More details from pega academy for Edit Input rules** 