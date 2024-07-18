---
title: 周报#2 - 忙碌的一周
tags: [Reflections]
categories: [Weekly Reports]
index_img: /img/in-post/DSCF3204.jpeg
banner_img: /img/in-post/DSCF3204.jpeg
math: false
excerpt: 本篇是对 `2024-07-08` 到 `2024-07-14` 这周生活的记录与思考。
date: 2024-07-15 12:00:00
---
>本篇是对 `2024-07-08` 到 `2024-07-14` 这周生活的记录与思考。

### 忙碌的一周
刚爬完[22公里的山](https://shengw3n.github.io/2024/07/08/Weekly_Report_1/#Garibaldi-Lake)就去乘船[挖生蚝](https://shengw3n.github.io/2024/07/15/Weekly_Report_2/#挖生蚝之Nanaimo一日游)，身体累。同一周还为了赶上Launch Canada的比赛，在一天内写完了37页的技术报告，心也累。更糟糕的是，还把比赛要用的[电调烧了](https://shengw3n.github.io/2024/07/15/Weekly_Report_2/#UBC-Rockets)，心更累了。上一周的周报写得很丧，这周心态还行。果然还是忙碌干活让我感觉充实。大三马上就要开始了，下周要开始学习学业上的东西了。顺便实习也得开始准备起来了。

### UBC Rockets

> [UBC Rocket](https://www.ubcrocket.com/) 是一个UBC工程学生设计团队，致力于亚轨道火箭的设计、制造和发射。目前我们有三个火箭项目并行研发：液态火箭、二级固态火箭和自着陆火箭。我正在负责其中的自着陆火箭项目，[Thrust Vector Rocket](https://github.com/UBC-Rocket/Thrust-Vectoring)。

这周我干了一件很蠢的事，把火箭的电调烧了。事情的起因是火箭的发动机推力一直没有达到预期的9kg，只在4kg左右徘徊。我和我们组的另一位lead一直在找原因，最后得出结论应该不是代码的问题，而是供电的问题。于是我们开始重新布置供电电路。然而我们两人同时脑子短路，把电路的电压干到了发动机接受范围的两倍，直接烧毁了电调。

这件事对我来说是一个深刻的教训。当时我们太急躁了，想着这么多天还没解决问题，没有停下来好好思考一下。以后还是得慢慢来，对这种高电压的电路，测试之前还是应该让别人检查一遍以确保稳妥。

**软件进展**
关于软件方面，这周我把陀螺仪和加速度计的传感信息用卡尔曼滤波处理了一下，然后将得到的角度数据输入到PID控制器中。至此，8月份在Launch Canada比赛中要展示的悬浮功能差不多已经成型了。跟液态火箭组的一个Lead视频咨询了一下，决定不做Matlab模型直接用Ziegler-Nichols 调参方法现场调试PID。做模型太复杂了直接现场调大力出奇迹。

下周等新的电调来了，机械组把调试台做好，就可以开始调试PID了。顺便也该开始测试无线网功能了。

**Gimbal PID Testing**
<div style="position: relative; width: 100%; height: 0; padding-bottom: 75%;"><iframe 
src="/vid/IMG_6815.MOV" alt="Gimbal PID Testing" scrolling="no" border="0" 
frameborder="no" framespacing="0" allowfullscreen="true" style="position: absolute; width: 100%; 
height: 100%; left: 0; top: 0;"> </iframe></div>

### 挖生蚝之Nanaimo一日游
周二买了张一日捕鱼证，乘渡船去了趟Nanaimo挖生蚝。第一次挖，整个沙滩遍地都是生蚝，赞👍。挖生蚝时手全是泥就没拿相机拍照了。 顺路去了Todd Creek Trestle，非常平庸的的一个桥梁景点，看了一次不会看第二次

{% gi 5 3-2 %}
  ![](/img/in-post/DSCF3429.jpeg)
  ![](/img/in-post/DSCF3204.jpeg)
  ![](/img/in-post/DSCF3304.jpeg)
  ![](/img/in-post/DSCF3425.jpeg)
  ![](/img/in-post/DSCF3115.jpeg)
{% endgi %}

