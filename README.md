EasyFlipView
============
[![Build Status](https://travis-ci.org/wajahatkarim3/EasyFlipView.svg?branch=master)](https://travis-ci.org/wajahatkarim3/EasyFlipView) [ ![Download](https://api.bintray.com/packages/wajahatkarim3/EasyFlipView/com.wajahatkarim3.EasyFlipView/images/download.svg) ](https://bintray.com/wajahatkarim3/EasyFlipView/com.wajahatkarim3.EasyFlipView/_latestVersion) [![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-EasyFlipView-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/5051) [![API](https://img.shields.io/badge/API-15%2B-blue.svg?style=flat)](https://android-arsenal.com/api?level=15) [![](https://img.shields.io/badge/MaterialUp-EasyFlipView-yellowgreen.png)](https://material.uplabs.com/posts/easyflipview)

A quick and easy flip view through which you can create views with two sides like credit cards, poker cards etc. 

![](https://github.com/wajahatkarim3/EasyFlipView/blob/master/Art/demo.gif)

Demo
====
Install [Demo](https://github.com/wajahatkarim3/EasyFlipView/releases/download/1.0.0/EasyFlipView-Demo_v1.0.0.apk) app or APK from [Releases](https://github.com/wajahatkarim3/EasyFlipView/releases) on your device and click on any card to flip it!

Changelog
=========
Changes exist in the [releases](https://github.com/wajahatkarim3/EasyFlipView/releases) tab.

Installation
============
Add this in your app's build.gradle file:
```groovy
dependencies {
  compile 'com.wajahatkarim3.EasyFlipView:EasyFlipView:1.0.2'
}
```

Or add EasyFlipView as a new dependency inside your pom.xml

```xml
<dependency> 
  <groupId>com.wajahatkarim3.EasyFlipView</groupId>
  <artifactId>EasyFlipView</artifactId> 
  <version>1.0.2</version> 
  <type>pom</type> 
</dependency>
```
Usage
=====

XML
---
EasyFlipView In XML layouts
```xml
<com.wajahatkarim3.easyflipview.EasyFlipView
	android:layout_width="match_parent"
	android:layout_height="wrap_content"
	app:flipOnTouch="true"
	app:flipEnabled="true"
	app:flipDuration="400">

	<!-- Back Layout Goes Here -->
	<include layout="@layout/flash_card_layout_back"/>
        
	<!-- Front Layout Goes Here -->
	<include layout="@layout/flash_card_layout_front"/>

</com.wajahatkarim3.easyflipview.EasyFlipView>
```
All customizable attributes for EasyFlipView
```xml
<declare-styleable name="easy_flip_view">
	<!-- Whether card should be flipped on touch or not (Default is true) -->
	<attr name="flipOnTouch" format="boolean"/>
	<!-- The duration of flip animation in milliseconds (Default is 400 ms) -->
	<attr name="flipDuration" format="integer"/>
	<!-- If this is set to false, then it won't flip ever (Default is true) -->
	<attr name="flipEnabled" format="boolean"/>
</declare-styleable>
```

In Code (Java)
----
```java
// Flips the view with or without animation
mYourFlipView.flipTheView();
mYourFlipView.flipTheView(false);

// Sets and Gets the Flip Animation Duration in milliseconds (Default is 400 ms)
mYourFlipView.setFlipDuration(1000);
int dur = mYourFlipView.getFlipDuration();

// Sets and gets the flip enable status (Default is true)
mYourFlipView.setFlipEnabled(false);
boolean flipStatus = mYourFlipView.isFlipEnabled();

// Sets and gets the flip on touch status (Default is true)
mYourFlipView.setFlipOntouch(false);
boolean flipTouchStatus = mYourFlipView.isFlipOnTouch();

// Get current flip state in enum (FlipState.FRONT_SIDE or FlipState.BACK_SIDE)
EasyFlipView.FlipState flipSide = mYourFlipView.getCurrentFlipState();

// Get whether front/back side of flip is visible or not.
boolean frontVal = mYourFlipView.isFrontSide();
boolean backVal = mYourFlipView.isBackSide();

```

Donations
=============

This project needs you! If you would like to support this project's further development, the creator of this project or the continuous maintenance of this project, feel free to donate. Your donation is highly appreciated (and I love food, coffee and beer). Thank you!

**PayPal**

* **[Donate $5](https://www.paypal.me/WajahatKarim/5)**: Thank's for creating this project, here's a tea (or some juice) for you!
* **[Donate $10](https://www.paypal.me/WajahatKarim/10)**: Wow, I am stunned. Let me take you to the movies!
* **[Donate $15](https://www.paypal.me/WajahatKarim/15)**: I really appreciate your work, let's grab some lunch!
* **[Donate $25](https://www.paypal.me/WajahatKarim/25)**: That's some awesome stuff you did right there, dinner is on me!
* **[Donate $50](https://www.paypal.me/WajahatKarim/50)**: I really really want to support this project, great job!
* **[Donate $100](https://www.paypal.me/WajahatKarim/100)**: You are the man! This project saved me hours (if not days) of struggle and hard work, simply awesome!
* **[Donate $2799](https://www.paypal.me/WajahatKarim/2799)**: Go buddy, buy Macbook Pro for yourself!
Of course, you can also choose what you want to donate, all donations are awesome!

Developed By
============
```
Wajahat Karim
```
- Website (http://wajahatkarim.com)
- Twitter (http://twitter.com/wajahatkarim)
- Medium (http://www.medium.com/@wajahatkarim3)
- LinkedIn (http://www.linkedin.com/in/wajahatkarim)

# How to Contribute
1. Fork it
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create new Pull Request

# License

    Copyright 2016 Wajahat Karim

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
