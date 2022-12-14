---
template: blog-post
title: Modular Robotic Applique Kits
slug: /robotic-teleoperation
date: 2021-08-03 12:37
description: dfdfdfsf
featuredImage: /assets/mrzr-smoke-sized.png
titleImage: /assets/ara-robots.jpg
---

## Getting Into Robotics

While I love my mobile apps and developing robust UIs, when you're offered the opportunity to develop robotics, _you take it!_ While I've updated a WPF OCU or Xamarin mobile application from time to time, my current focus is working with the code base responsible for the control of electronics and actuators on a range of unmanned vehicles from MRZRs, CATs to USG classified vehicles.

## Autonomous Bucket Loaders

One of my most recent projects at **[<ins>Applied Research Associates, Inc.</ins>](https://www.ara.com)** has been tailoring our robotics code base to control a CAT 299D3 Bucket Loader. 
- I modified the vehicle kit to receive both proprietary CAN messages from a private controller and IOP (Inter-Operability Standard) messages from a fully autonomous B-Kit.
- It then relays those commands to the tool, starter, and ignition relays, and pulse width modulators responsible for controlling the steering, throttle, drive, power, bucket tilt and bucket lift of the machine.

![<span style="color:#777777;"> CAT 299D3 at work </span>](/assets/cat299D3.jpeg)

## ADAS and Teleoperation Enabled _"Platform"_

Unfortunately, this project is **Controlled Unclassified Information (CUI)** so it is export controlled and thus I cannot divulge too much information or show any cool gifs. That being said, my involvement in the project included:

- Developing the UI of the ADAS (Advanced Driver Assist) teleoperation control interface. 
- As the only software engineer willing to drive the _vehicle_ I was also responsible for much of the debugging process, leading to an expansive mile-wide-inch-deep knowledge of the overall system; from ML algorithms detecting pedestrians to adaptive cruise feedback loops to CAN hardware interfaces.
- I was selected to travel onsite to get the vehicle ready for a demo with the USG's Ground Vehicle's Systems Center (GVSC).

## Safety Processor Unit Tests

![<span style="color:#777777;"> Safety Processor Test Fixture </span>](/assets/ara-test-fixture.jpg)

One of my first responsibilities at ARA was to devise a bench-top setup for unit testing the safety processor on our vehicle interface controller. 
- Critical commands commands sent from our vehicle kit's main CPU are sent through a TI dual lock-step safety processor to ensure the command can be executed in the platforms current state.
- I created a mock set-up to send valid and invalid serial commands to the safety processor and read it's CAN outputs, ensuring edge cases and unsafe commands were being taking care of properly.
