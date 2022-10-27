---
template: blog-post
title: CocoaNEC For Radiation Models
slug: /cocoanec-radiation-model
date: 2018-09-13 12:46
description: sdasd
featuredImage: /assets/3d-output-sized.png
titleImage: /assets/horn-antenna-setup.png
---

### Breakthroughs in Concealed Object Detection

While there are several metal detection systems available (think TSA), many are still expensive and infrastructurally demanding. There is yet to be a lightweight technology which can discreminate betwen dangerous and benign conductive materials (specfically for private use). 

With specfific methods, the utilizization of pulsed ultra-wideband microwaves has shown positive results in shape detection of conductive materials.

 Please reference **[<ins>Dr. Kowalcyk's Dissertation</ins>](https://scholarworks.uvm.edu/cgi/viewcontent.cgi?article=2172&context=graddis)**


### My Involement

```grid|2|
![<span style="color:#777777;"> CocoaNEC Wire-Grid Model of Two Interacting Horn Antennas </span>](/assets/horn-grid.png)
![<span style="color:#777777;"> Corresponding 3D Antenna Pattern Output </span>](/assets/horn-3d-sized.png)
```
<center><span style="color:#777777;"> Wire-Grid Model of Two Interacting Horn Antennas and Corresponding 3D Antenna Pattern Output </span></center>

In order for Dr. Kowalczyk to further corroborate the breakthrough in his findings he needed to ensure that they RF field he was testing in was behaving according to his predictions. 

 - I wrote a CocoaNEC model for the output of two interacting double ridged waveguide horn antennas positioned one meter part and pointed at eachother radiating at 1000 MHz. 

 - By comparing theoretical output with field meausrements, Dr. Kowalczyk was able to further deonstrate that other effects beyond the complex permittivity of the obstructuve materials between the antennas must be influencing the transmitted microwave field. 
 
 If the field signal amplitude were solely due to the frequency of the radiated field and the dimensions of the obstructive sample, it would be expected that the observed reduction in field signal loss would increase continuously with frequency due to lensing effects. Instead, **signal gain was recorded!**

```grid|2|
![<span style="color:#777777;"> Azimuth Antenna Output of the Model </span>](/assets/horn-azimuth.png)
![<span style="color:#777777;"> Elevation Antenna Output of the Model </span>](/assets/horn-elevation.png)
```
<center><span style="color:#777777;"> Azimuth and Elevation Antenna Model Output </span></center>