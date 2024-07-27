---
title: WR#1 - Reflections on Ambition and Motivation
tags: [Reflections]
categories: [Weekly Reports]
index_img: /img/in-post/DSCF2890.jpeg
banner_img: /img/in-post/DSCF2890.jpeg
math: false
excerpt: This article reflects on my life from the week of `07-01-2024` to `07-07-2024`.
date: 2024-07-08 12:00:00
---

>This article reflects on my life from the week of `07-01-2024` to `07-07-2024`.


Over the past two years at university, my busy schedule and various distractions have diminished my time for independent thinking, impacting my study efficiency and motivation. Watching my GPA decline each semester and feeling increasingly distanced from my ideal self, I realized I faced a crucial decision: continue on my current path or make a change.

The idea of writing weekly reports began about six months ago after discovering [pseudoyu](https://www.pseudoyu.com/zh/)’s blog. I aim to evaluate my life, work, and studies weekly, much like his approach. Writing these reports is my way of motivating myself to get closer to who I want to become.

### Dreams, Discipline, and the Pain of Failure
Fencing has been a bittersweet journey for me. Since I was 12, my dream was to join the Canadian fencing national team. I invested significant time and money, fenced almost daily, attended numerous competitions, and trained diligently. Despite these efforts, I did not achieve my goal.

Reconciling with myself has been difficult, especially when surrounded by talented individuals. A friend who began fencing just six months before me is heading to the Paris Olympics, while others a year older and younger have made the national team. Though the pandemic disrupted my schedule, I ultimately hold myself accountable.

I need to understand what I lack compared to my successful peers. I’ve identified two major deficiencies: discipline and a strong desire to win.

Firstly, I struggle with discipline. Although I showed dedication at the fencing strip, I lacked the consistency needed for additional training and overall fitness improvement. This lack of discipline also affects my academic work, where my efforts are sporadic and lack sustained focus.

Secondly, my desire to win isn’t as strong as it should be. This paradox is evident both in fencing and my studies. While I enjoy fencing and the idea of being on the national team, I don’t display the intense determination necessary for success. My reaction to wins or losses is subdued, and similarly, while I prefer high exam scores, I’m not deeply affected by low ones. This discrepancy between my aspirations and reality is a significant source of frustration.

### Adapting to Present Challenges
My dreams have deep roots in my childhood and remain consistent. Beyond fencing, I also aspired to become an engineer from a young age, inspired by the giant robots in animes like “Code Geass” and “Gundam 00.” I even shared my Gundam ambitions during my first-year Engineering Physics interview, a moment that now makes me smile with embarrassment.

After the setback of my fencing dream, I’ve approached my engineering aspirations with increased caution. As I’ve grown older, anxiety and fear have intensified. Rejections from job interviews, unsatisfactory exam results, and failed engineering projects have made me restless, undermining my focus on current goals. As my sense of security gradually fades, loneliness has taken its place. I am slowly learning to navigate this new, isolating reality.

### UBC Rockets
> [UBC Rocket](https://www.ubcrocket.com) is an engineering student design team at the University of British Columbia dedicated to the design, manufacture, and launch of suborbital rockets. I’m currently contributing to the [Thrust Vector Rocket](https://github.com/UBC-Rocket/Thrust-Vectoring), our self-landing rocket project.

This week, I focused on developing the basic PID control for the gimbal. The principle is straightforward: if the rocket tilts to one side, the gimbal tilts in the opposite direction to correct it.

**PID Code Snippet**
``` C++
  inputY = a.acceleration.y; // Using acceleration as input
  pidY.Compute();
  int servoPosY = constrain(90 + outputY, 0, 180); // outputY = PID output
  servoY.write(servoPosY);
```

**Debugging**
1. The gyroscope MPU-6050’s AD0 pin (I2C Address pin) was not connected to ground, causing occasional sensor freezes.
2. The Arduino PID Library <PID_v1.h> has a default output range of 0-255, which caused issues with negative PID outputs. `SetOutputLimits()` resolved this.

**Next Steps**
- Combine accelerometer and gyro readings using a complementary Kalman filter for more accurate rocket angle estimation
- Motor Test
- Matlab simulations (?)

### Canada Day
Monday was Canada Day, went to an all-you-can-eat hotpot with friends and later played some poker at the park while we wait for the fireworks. Photos taken using my newly bought FUJI XT5 😎. 

{% gi 5 2-3 %}
  ![](/img/in-post/DSCF2758.jpeg)
  ![](/img/in-post/DSCF2753.jpeg)
  ![](/img/in-post/DSCF2679.jpeg)
  ![](/img/in-post/DSCF2622.jpeg)
  ![](/img/in-post/DSCF2582.jpeg)
{% endgi %}

### Garibaldi Lake
On Sunday I went on a hike to Garibaldi Lake, carrying 3.5 liters of water and a camera for 22 kilometers. The hike was tedious, with mosquitoes constantly bothering me, but the view was ok.

{% gi 5 3-2 %}
  ![](/img/in-post/DSCF2889.jpeg)
  ![](/img/in-post/DSCF2890.jpeg)
  ![](/img/in-post/DSCF2898.jpeg)
  ![](/img/in-post/DSCF2969.jpeg)
  ![](/img/in-post/DSCF2789.jpeg)
{% endgi %}
