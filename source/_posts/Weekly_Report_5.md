---
title: WR#5 - Racing Towards Launch Canada
tags:
  - Reflections
categories:
  - Weekly Reports
index_img: /img/banner/DSCF2918.jpg
banner_img: /img/banner/DSCF2918.jpg
math: false
excerpt: This article reflects on my life from the week of 07-29-2024 to 08-04-2024
date: 2023-08-05 12:00:00
---

> This article reflects on my life from the week of `07-29-2024` to `08-04-2024`.

Busy rocket week as we approach the Launch Canada competition. With less than two weeks until the event and our trailer departing in just one week, we're in a race against time to finalize preparations.

## UBC Rocket
> [UBC Rocket](https://www.ubcrocket.com) is an engineering student design team at the University of British Columbia dedicated to the design, manufacture, and launch of suborbital rockets. I’m currently contributing to the [Thrust Vector Rocket](https://github.com/UBC-Rocket/Thrust-Vectoring), our self-landing rocket project.

### ESC Replacement 
Following the [failure of our original Electronic Speed Controller (ESC)](https://shengw3n.github.io/2024/07/15/Weekly_Report_2/#UBC-Rockets), we finally received a replacement. However, local electronic stores does not have the connectors compatible with our existing setup. To resolve this, I cut the wires from the original ESC, soldered them to the new one, and applied heat shrink to maintain the original connectors. The staff at [Lee's Electronics](https://leeselectronic.com/)provided some great assistance and suggestions.

![ESC Soldered and Heat-Shrinked](/img/in-post/IMG_1538.HEIC)

### LiPo Battery Charging
I also gained practical experience in LiPo battery charging this week. I learned about selecting appropriate settings, voltage and current considerations, proper connection of balance pins, and the importance of using fireproof bags during charging.

![Charging LiPos](/img/in-post/IMG_1569.HEIC)

### Motor Testing Challenges
Our motor's expected thrust is 8 kg, but we've consistently achieved a maximum of only 4.6 kg, even with the new ESC. After validating our code and power supply specifications, we're still uncertain about the cause of this discrepancy:
- **Code**: Our PWM periods (900 to 2400 microseconds) match the manufacturer's data sheet
- **Power supply**: two 7s (25.9V) 3250 mAh 150c LiPo batteries in series
    - Voltage: 25.9 + 25.9 = 51.8 volts (check!)
    - Current: 3250 mAh × 150 = 487.5 A (more than enough!)
We've ruled out issues with PWM signals and power requirements. Despite balancing the LiPo cells, we haven't seen improvement. This remains an ongoing investigation, and I'll provide updates in future reports.

### Avionics Dock Design
I designed a simple avionics dock using Fusion360 this week. This dock will house our electronics during the Launch Canada tethered demonstrations. Once 3D-printed, we can proceed with PID tuning.

<iframe src="https://a360.co/46JoYuv" width="100%" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe

### Launch Canada Safety Meeting
We successfully completed a safety meeting for the thrust vector rocket, clearing us for competition participation.

### UBC Geering Up Presentation
We also presented for a classroom full of elementary school students for [UBC Geering Up](https://geeringup.apsc.ubc.ca) on university rocketry. The most common question I got from the kids was, "What's the minimum age to join UBC Rockets?" They are so cute.

![Me Carrying Rockets to The Classrooms](/img/in-post/IMG_1540.HEIC)

## Golf
I'm concluding a 5-week beginner golf course this week. It's been an enjoyable experience, and I'm looking forward to applying what I've learned.

<div style="position: relative; width: 100%; height: 0; padding-bottom: 75%;"><iframe 
src="/vid/3206.mov" alt="Gimbal PID Testing" scrolling="no" border="0" 
frameborder="no" framespacing="0" allowfullscreen="true" style="position: absolute; width: 100%; 
height: 100%; left: 0; top: 0;"> </iframe></div>

## Monitor Control
I am currently on monitor and have to fiddle though the buttons on the back of monitor just to change its brightness. Discovered this app called [Monitor Control](https://github.com/MonitorControl/MonitorControl) from Pseudoyu's [latest blog](https://www.pseudoyu.com/zh/2024/07/30/weekly_review_20240730/) that does that from the mac interface, pretty nice.


