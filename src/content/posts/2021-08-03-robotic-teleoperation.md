---
template: blog-post
title: Robotic Teleoperation; CATs, MRZRs and Beyond
slug: /robotic-teleoperation
date: 2021-08-03 12:37
description: dfdfdfsf
featuredImage: /assets/mrzr-smoke-sized.png
titleImage: /assets/ara-robots.jpg
---

## Getting Into Robotics

While I love my mobile apps and developing clean UIs, when you're offered the opportunity to develop robotics, _you take it._ I am currently updating our code for tele-operatiom of Polaris MRZR-Ds from Ubuntu into the Nixos world while making some updates along the way.

```grid|2|
![Right](https://raw.githubusercontent.com/bkowalczyk21/engineering-portfolio/updated-images/static/assets/mrzr-autonomous.gif "<span style="color:#777777;"> Backseat of tele-operation! </span>")
![Left](https://github.com/bkowalczyk21/engineering-portfolio/blob/improve-pages/static/assets/mrzr-backseat.gif?raw=true "<span style="color:#777777;"> Autononous MRZR </span>")
```

## Autonmous Bucket Loaders

One of my most recent pojects at **[<ins>Applied Research Assicaites, Inc.</ins>](https://www.ara.com)** has been tailoring our robotics code base to conotrol a CAT 299D3 Bucket Loader. I created the Vehicle side controller which can receive both prorietary CAN messages from a private controller or IOP (Inter-Operability Standard) messages from a fully autonomous B-Kit and relay those commands to the tool, starter, and ingition relays, and pulse width modulators to properly control the steering, throttle, drive, power, tilt and lift of the machine.

![<span style="color:#777777;"> CAT 299D3 at work </span>](/assets/cat299D3.jpeg)

## ADAS and Tele-operation Enabled HMMWVs

Unfortunately this project is Controlled Unclassified Information so it is export controlled and thus I cannot divulgde too much information or show any cool GIFS. That being said, my involement in the project included developing the UI of the ADAS (Advanced Driver Assist) tele-operation control interface for the platform. As the only sfotware engineer willing to drive the HMMWV I was also responsible for much of the debugging process, leading to a comprehensive knowledge of the overal system; from ML algorithms detecting pedestrians to adaptive cruise algorthms to CAN hardware interfaces. Hence, I was selected travel onsite and get the vehicle ready for a demo with the USG's Ground Vehicle's Systems Center (GVSC).

## Safety Processor Unit Tests

![<span style="color:#777777;"> Safety Processor Test Fixture </span>](/assets/test-fixture.jpg)

One of my first responsibilities at ARA was to devise a bench-top setup for unit testing thr safety processor on our vehicle interface controller. Critical commands commands sent from the vheicles main CPU are sent through a TI dual lock-step safety processor to ensure the comand can be executed in the current state. I created a mock set-up and sent valid and invalid serial commands ti the safety processor to ensure it was taking care of our edge cases cases correctly.
