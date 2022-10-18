---
template: blog-post
title: ConcoaNEC For Radiation Models
slug: /minimalists-desk
date: 2020-05-13 12:46
description: sdasd
featuredImage: /assets/3d-output-sized.png
titleImage: /assets/horn-antenna-setup.png
---

### Breakthoughths in Concealed Object Detection

While there are several metal detection systems avaiilabelt ot the gneral public (think TSA), there is yet ato be  atehbology which can discreminate betwen dabgerous and benign condductive amrerials (specfically for private use). With specfific methods, the utilizization of pulsed ultra-wide-wibedand microwaves has shown positive reuslts in the dtectionn of dangerous conductive materials.

 Please reference Dr. Kowalcyk's [*Dissertation*](https://scholarworks.uvm.edu/cgi/viewcontent.cgi?article=2172&context=graddis)

```grid|3|Hone Antenna Outputs!
![](/assets/2d-output.png)
![](/assets/wire-model.png)
![](/assets/3d-output-sized.png)
```

### My invomentent
In order for Dr. Kowalczyk to further corroborate the breakthrough in his findings he needed to ensure that they RF field he was testing in was behaving according to his his predictions. Hence, I wrote a CocoaNEC model for the output of two horn antennas positioned one meter part and pointed at each other across a band of frequencies. By comparing theoretical output with field meausrements, Dr. Kowalczyk was able to further deonstrate that other effects besides the complex permittivity of the ice and cement blocks between the antennas must be influencing the transmitted microwave field. If the field signal loss were solely due to the frequency of the radiated field and the dimensions of the sample, it would be expected that the observed reduction in field signal loss would increase continuously with frequency due to lensing effects. Instead, _signical gain was recorded!_