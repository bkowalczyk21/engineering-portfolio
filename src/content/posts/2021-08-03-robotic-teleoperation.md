---
template: blog-post
title: Robotic Teleoperation; CATs, MRZRs and Beyond
slug: /robotic-teleoperation
date: 2021-08-03 12:37
description: dfdfdfsf
featuredImage: /assets/mrzr-smoke-sized.png
titleImage: /assets/ara-robots.jpg
---

![Test Fixture](/assets/test-fixture.jpg "Test Fixture")

![Bucket Loader](/assets/ara-bucket-loader.jpg "Bucket Loader")

![Robot Lineup](/assets/ara-robots.jpg "Robot Lineup")

While I love my mobile apps, when you're offered the opportunity to develop robotics you take it. As I was introduced to 
**[<ins>ARA's</ins>](https://www.ara.com)** system it my responsiblity to devise unit tests and a bench-top system to ensure serial commands being sent from
the vehicle controller's main CPU to were eventually sending safe CAN commands to critial actuators of the vehicle ater being passed through
the controller's dual lock-step safety processor. Soon, after developing the ADAS UI for the C++ Qt appliaction for tele-opartion of an unnamed 
platform, and the headin the debuggin of th eoveralll system I became one of the only engineers with knowledge across all facets of the system from sensor input, 
JAUS and IOP interfaces, adaptive cruise algorithms, to CAN and GPIO output. Hence, I was slected to go out and prepapre the vehicle for a  
demo for the Ground Vehicle Systems Center (GVSC). 

In my most recent project I programmed the vehicle interface controller for a CAT299D3 Bucket Loader which receives JAUS commmands from 
a seperate autonomous B-Kit or proprietary CAN messages froma hand-held controller.