---
title: "Razorpay Integration"
date: 2024-01-20 12:30:00 +/-0800   
categories: [Pega,Payment Integration]
math: true
mermaid: true
tags: [Pega,Payment]
image: "/assets/img/post/thumbnail/razorpay.jpg"
image:
  path:  /assets/img/post/thumbnail/razorpay.jpg
  width: 1000   # in pixels
  height: 400   # in pixels
  alt: Razorpay Integration
---
<!-- ## Video Tutorial

<div style="text-align: center;">
    <iframe width="700" height="400" src="https://www.youtube.com/embed/Q-SyOLMjWG8 " frameborder="0" allowfullscreen></iframe>
</div> -->
## Steps

* Create account in Razorpay website
    * [Click Here](https://razorpay.com/){:target="_blank"} - **To Continue Razorpay website**
    * Click Signup and create account
    <div style="text-align: center;">
    <img src="/assets/img/post/razorpay/razorpay-1.png" alt="razorpay-1" width="700" height="400">
    </div>

* Go to payment pages
<div style="text-align: center;">
    <img src="/assets/img/post/razorpay/razorpay-2.png" alt="razorpay-2" width="700" height="400">
</div>

* Create new payment page
<div style="text-align: center;">
    <img src="/assets/img/post/razorpay/razorpay-3.png" alt="razorpay-3" width="700" height="400">
</div>

* Select payment Page
<div style="text-align: center;">
    <img src="/assets/img/post/razorpay/razorpay-4.png" alt="razorpay-4" width="700" height="400">
</div>

* Click price field
<div style="text-align: center;">
    <img src="/assets/img/post/razorpay/razorpay-5.png" alt="razorpay-5" width="700" height="400">
</div>

* Select customer decide amount
<div style="text-align: center;">
    <img src="/assets/img/post/razorpay/razorpay-6.png" alt="razorpay-6" width="700" height="400">
</div>

* Add logo, page title, contact information
<div style="text-align: center;">
    <img src="/assets/img/post/razorpay/razorpay-7.png" alt="razorpay-7" width="700" height="400">
</div>

* Click Create and publish page
<div style="text-align: center;">
    <img src="/assets/img/post/razorpay/razorpay-8.png" alt="razorpay-8" width="700" height="400">
</div>

* Copy link and open in new tab
<div style="text-align: center;">
    <img src="/assets/img/post/razorpay/razorpay-9.png" alt="razorpay-9" width="700" height="400">
</div>

* Now Copy the URL
<div style="text-align: center;">
    <img src="/assets/img/post/razorpay/razorpay-10.png" alt="razorpay-10" width="700" height="400">
</div>

* Now Go to Dev Studio
* Create One Property For Payment Link (Ex:Razorpay Payment link)
* Create Declare Expression and open expression Expression builder
* Write expression (Ex:"https://pages.razorpay.com/pl_NSHJcyg287F0BK/view/?&amount="+.Amount+"&email="+.Details.EmailID+"&phone="+.Details.MobileNumber)
```bash 
"Your Payment Link/?&amount="+ .Amount property +"&email="+ .EmailID property +"&phone="+ .MobileNumber property
```
<div style="text-align: center;">
    <img src="/assets/img/post/razorpay/razorpay-11.png" alt="razorpay-11" width="700" height="400">
</div>

* Open Section and add button and add action set
    * Add event as click and action as Open URL in Window 
<div style="text-align: center;">
    <img src="/assets/img/post/razorpay/razorpay-12.png" alt="razorpay-12" width="700" height="400">
</div>

* Select the Check boxes and call the property
<div style="text-align: center;">
    <img src="/assets/img/post/razorpay/razorpay-13.png" alt="razorpay-13" width="700" height="400">
</div>
