---
title: "Password Format"
date: 2024-01-5 12:30:00 +/-0800   
categories: [Pega]
math: true
mermaid: true
tags: [Pega,Password Format,Edit validate rule,Pattern Validation]
# image: "/assets/img/post/LV.png"
# image:
#   path:  /assets/img/post/LV.png
#   width: 1000   # in pixels
#   height: 400   # in pixels
#   alt: Login Validation
---
## Video Tutorial

<div style="text-align: center;">
    <img src="/assets/img/post/LV.png" alt="Your GIF" width="560" height="315">
</div>


## Format - 1 (Display custom message)
* The password must be atleast 8 - 15 character
* Include both lower and upper case characters
* Include at least one number are symbol

```bash
// regex to check password
String regex= ("^(?=.*[a-z])(?=.*[A-Z])(?=.*\\d)(?=.*[@#$%^&+=!])(?=\\S+$).{8,15}$");

// Compile the ReGex
  java.util.regex.Pattern p=java.util.regex.Pattern.compile(regex);

// If the string is empty, return false
if (theValue == null || theValue.trim().equals("")) return false;
// Custom message
theProperty.addMessage("Be atleast 8 - 15 characters long");
theProperty.addMessage("Include both lower and upper case characters");
theProperty.addMessage("Include at least one number are symbol");

// Pattern class contains matches() method to match the given string and regular expression
java.util.regex.Matcher m = p.matcher(theValue);
return m.matches();
```
## Format - 2 (Display property name as error)
* The password must be atleast 8 - 15 character
* Include both lower and upper case characters
* Include at least one number are symbol

```bash
// Regex to check valid Password  
String regex= ("^(?=.*[a-z])(?=.*[A-Z])(?=.*\\d)(?=.*[@#$%^&+=!])(?=\\S+$).{8,15}$");
// Compile the ReGex 
java.util.regex.Pattern p=java.util.regex.Pattern.compile(regex); 
// If the string is empty, return false 
if (theValue == null || theValue.trim().equals("")) return false;
 // Pattern class contains matcher() method to match the given string and the regular expression 
java.util.regex.Matcher m = p.matcher(theValue); 
// Return if the string matched the ReGex 
return m.matches();
```

## Reference 
[Click Here](https://docs-previous.pega.com/reference/87/about-edit-validate-rules?){:target="_blank"} - **More details from pega academy** 