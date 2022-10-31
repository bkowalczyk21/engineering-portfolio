---
template: blog-post
title: Bluetooth Solutions For Remote Photography
slug: /pocket-wizard-app
date: 2019-05-21 12:55
description: Developing an iOS app for controlling settings via bluetooth on remote camera triggers for professional photography.
featuredImage: /assets/Pocket_Wizard_Plus3.png
titleImage: /assets/pw-logo.jpg
---

## Quick PocketWizard Overview

**[<ins>PocketWizard</ins>](https://pocketwizard.com)** creates radios which allow for the wireless control and synchronization of cameras, flash lighting and light meters--perfect for sports, nature, event photography and much more. Their radio's connect to a wide variety of professional cameras allowing a photographer to trigger captures from several devices across long distances.

## Controlling Camera Trigger Settings Over Bluetooth

Working at PocketWizard I created a **full-stack iOS application** for controlling the mode (flash vs trigger), radio frequency, and tamper settings on their latest radio trigger prototype over Bluetooth Low Energy. 

- I learned Swift and became a master with XCode's Interface Builder and UIKit Core (although I look forward to the mass adoption of SwiftUI).
- Of course I also had to delve deep into the CoreBLE library and learn quite a bit about the relationship between mobile applications and microcontroller peripherals.
- I got to express my artistic side and develop a couple Adobe XD mock-ups and edit images in GIMP 

```grid|3|
![<span style="color:#777777;"> Device List Homepage </span>](/assets/pw-homepage.jpeg)
![<span style="color:#777777;"> Device BLE Control </span>](/assets/pw-control.jpeg)
![<span style="color:#777777;"> Over-the-Air Firmware Update </span>](/assets/pw-ota-update.png)
```
<center><span style="color:#777777;"> Homepage, Radio Control and OTA Update Pages </span></center>

### This doesn't sound fullstack? ###

The neatest feature implemented though was the over-the-air (OTA) firmware updates:

1. Firmware updates improving reliability, range and performance of the remote triggers could be uploaded into an AWS S3 bucket by our embedded systems engineer.
2. The mobile application would then make occasional queries to determine if there was a new firmware update. If so, the user would be alerted and, with agreement, the image was pulled from the AWS bucket.
3. The iOS application would send commands to the trigger microcontroller to switch into an app-loader mode.
4. Keeping the old firmware image in the upper half of the microcontroller's memory to avoid a brick, the iOS application would deliver the new image packet-by-packet in a closed-loop fashion with a responsive UI indicating the update's progress.
5. After the update was completed, a check would be run to ensure a clean image was received and then the old image was deleted.

**Disclaimer:** Unfortunately, during this time COVID-19 hit reducing company budget for new projects and I also found a new job thus this product never made it to production. 
