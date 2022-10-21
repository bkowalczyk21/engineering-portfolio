---
template: blog-post
title: Bluetooth Solutions For Remote Photography
slug: /pocket-wizard-app
date: 2019-05-21 12:55
description: Developing an iOS app for controlling settings via bluetooth on remote camera triggers for professional photography.
featuredImage: /assets/Pocket_Wizard_Plus3.png
titleImage: /assets/pw-logo.jpg

---

```grid|3|NR1 Screenhots!
![](/assets/pw-homepage.jpeg)
![](/assets/pw-control.jpeg)
![](/assets/pw-ota-update.png)
```

As a part time devleoper for **[<ins>PocketWizard</ins>](https://pocketwizard.com)** I created a full-stack iOS
application for controlling mode, frequency, and tamper settings on their latest radio trigger prototype over 
Bluetooth Low Energy. Each trigger would be placed on professional cameras placed around anywhere within 
miles given line of sight in order to capture some of the greatest sports, nature and masss event shots.
I became a master with XCode's Interface Builder and UIKit (although I look forward to the mass adoption of SwiftUI).
Of course I also had to delve deep into the CoreBLE library and learn quite a bit about the relationship between
mobile applicaions and their microcontroller peripherals. 

The absolute neatest feature implemeted though was the over-the-air (OTA) updates. When our embedded engineer created
firmware updates to improve reliability, range and performance of the remote triggeers I had an AWS S3 bucket set up for
him to drop new images into. The iOS applicaiton would occaisonally query for new firmware and when they were detected the user was 
alerted. If the user so chose, the image was pulled from the AWS bucket and delivered packet by packet from the phone onto the 
device via Bluetooth with broke image checks to avoid bricking any triggers.