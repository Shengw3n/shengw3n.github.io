---
title: WR#2 - Busy Week
tags: [Reflections]
categories: [Weekly Reports]
index_img: /img/in-post/DSCF3204.jpeg
banner_img: /img/in-post/DSCF3204.jpeg
math: false
excerpt: This article reflects on my life from the week of `07-08-2024` to `07-14-2024`.
date: 2024-07-15 12:00:00
---
>This article reflects on my life from the week of `07-08-2024` to `07-14-2024`.

Busy and tiring week. Following my first weekly report, I’ve been working on building discipline by committing to daily planned tasks. Although I’ve made some progress, I still find myself spending a fair amount of time watching Bilibili and reading manga. It’s a gradual process, but I’m happy with the improvements I’m seeing.

### UBC Rockets

> [UBC Rocket](https://www.ubcrocket.com) is an engineering student design team at the University of British Columbia dedicated to the design, manufacture, and launch of suborbital rockets. I’m currently contributing to the [Thrust Vector Rocket](https://github.com/UBC-Rocket/Thrust-Vectoring), our self-landing rocket project.

This week, my teammate and I made a super stupid mistake by frying the ESC (Electric Speed Controller) for our rocket. The issue arose because our rocket's thrust was consistently below the expected 9kg, hovering around 4kg. After much troubleshooting, we concluded the problem was likely with the power supply rather than the code. In our haste to resolve the issue, we rewired the circuit, but ended up doubling the voltage beyond the engine's acceptable range, which destroyed the ESC.

This experience was a tough lesson in patience and thoroughness. Our haste prevented us from properly reviewing the circuit before testing. Moving forward, we need to ensure high-voltage circuits are reviewed carefully to avoid such mistakes.

#### Launch Canada Final Report
We (3 people) completed a 37-page technical report in one day for the Launch Canada competition. Horrendous experience that I do not want to go through again. I aspire to write it better next year.

#### Software Progress
This week I processed the gyroscope and accelerometer data using a Kalman filter and fed the resulting angle data into the PID controller. This marks significant progress towards the hover functionality we plan to showcase at the Launch Canada competition in August. You can see the gimbal reacting to the sensor's data below.

In terms of simulation, after consulting with fellow rocket member [Timothy](https://timothycai.com), we decided to forgo creating a Matlab model and instead use the Ziegler-Nichols method for in the loop PID tuning. This seems like a more practical approach.

#### Gimbal PID Testing
<div style="position: relative; width: 100%; height: 0; padding-bottom: 75%;"><iframe 
src="/vid/IMG_6815.MOV" alt="Gimbal PID Testing" scrolling="no" border="0" 
frameborder="no" framespacing="0" allowfullscreen="true" style="position: absolute; width: 100%; 
height: 100%; left: 0; top: 0;"> </iframe></div>


#### Next Steps
- Design and manufacture test rig for PID tuning
- Implement wireless functionalities


### Nanaimo Oysters Harvesting Trip
On Tuesday, I purchased a one-day fishing license and took a boat trip to Nanaimo for oyster harvesting. It was my first time and the beach was covered in oysters — a rewarding experience! No photos during harvesting cuz my hand was dirty.

{% gi 5 3-2 %}
  ![](/img/in-post/DSCF3429.jpeg)
  ![](/img/in-post/DSCF3204.jpeg)
  ![](/img/in-post/DSCF3304.jpeg)
  ![](/img/in-post/DSCF3425.jpeg)
  ![](/img/in-post/DSCF3115.jpeg)
{% endgi %}

