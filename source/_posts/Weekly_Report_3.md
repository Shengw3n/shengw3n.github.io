---
title: WR3 - Rediscovering Joy in Engineering
tags:
  - Reflections
categories:
  - Weekly Reports
index_img: /img/banner/DSCF2247.JPG
banner_img: /img/banner/DSCF2247.JPG
math: false
excerpt: This article reflects on my life from the week of `07-15-2024` to `07-21-2024`.
date: 2024-07-22 12:00:00
---

> This article reflects on my life from the week of `07-15-2024` to `07-21-2024`.

I've been slowly improving my study habits this week. I also started [CS50](https://cs50.harvard.edu/x/2024/) to refresh my knowledge of C, which I realized I had forgotten after taking my last C course, CPSC 259, a year ago. Once I finish the course, I should grind some LeetCode to better prepare for interviews.

### Finding Joy in Engineering Again
Second year of engineering was a challenging period. Despite cool projects such as the [FPGA RISC Machine](https://github.com/Shengw3n/FPGA-Reduced-Instruction-Set-Computer), [Reflow Oven Controller](https://github.com/Shengw3n/Reflow-Oven-Controller), and [Remote-Controlled Robot](https://github.com/Shengw3n/Remote-Controlled-Metal-Detector-Robot), the experience felt rushed and lacked the joy I once associated with engineering. Long lab hours and unending assignments made it a tough year overall.

![Me and my ELEC 291 group getting A&W at 6 am after an all-nighter](/img/in-post/IMG_0689.jpeg)

The turning point came this week with my [involvements](https://shengw3n.github.io/2024/07/22/Weekly_Report_3/#UBC-Rocket) in UBC Rocket. Successfully setting up Wi-Fi communication for the Thrust Vector Rocket brought back the excitement I had been missing. The sense of accomplishment when establishing a working connection was exhilarating, especially after analyzing the network protocol like a spy beforehand. Moving forward, I aim to seek out and cherish more of these fulfilling moments.

### UBC Rocket
> [UBC Rocket](https://www.ubcrocket.com) is an engineering student design team at the University of British Columbia dedicated to the design, manufacture, and launch of suborbital rockets. I’m currently contributing to the [Thrust Vector Rocket](https://github.com/UBC-Rocket/Thrust-Vectoring), our self-landing rocket project.

We are still waiting for the new ESC installation to start tuning the PID. In the meantime, I implemented a Wi-Fi communication using a custom-made ESP-12F I had at home.

#### Wi-Fi Station Communication 
It turns out the custom-made ESP-12F is designed for children aged 3-12 in China and is highly specialized, connecting only to a dedicated Android app and WeChat, with limited customization. It is also impossible to code the ESP-12F since it is soldered onto a custom PCB board. I managed to establish communication with the Android app using a MacBook android simulator, but the app itself is again very basic and lacks customization.

I considered giving up and buying a cheap Bluetooth Low Energy module instead (which we might do next year), but I decided to reverse engineer the communication protocol between the ESP-12F and the Android app first using a network analyzer tool like [Wireshark](https://www.wireshark.org/).

![Analyzing network protocol using Wireshark](/img/in-post/IMG_1234.png)

Of course I had to first spend a day learning network concepts ([this website](https://tttapa.github.io/ESP8266/Chap01%20-%20ESP8266.html) was particularly helpful), but in the end I managed to reverse-engineer the communication protocol and incorporated it into the code. 

#### Python Code Snippet
``` Python
def send_command(command): # Function to send command to ESP-12F
    host = '192.168.1.1'
    port = 2001

    try:
        with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
            s.connect((host, port))
            s.sendall((command + '\n').encode())
```

I also created a neat GUI with `tkinter`, allowing us to remotely control the rocket with style 😎:
![Simple Rocket Control GUI](/img/in-post/gui.png)
However, it is still impossible to send sensor data back from the rocket through the ESP-12F since I cannot code it. I am essentially mimicking the Android app. This functionality is sufficient for the Launch Canada Competition in a month, where we are showcasing the hover ability of our Thrust Vector Rocket instead of flying it. We will likely switch to a Bluetooth/radio module or an actual ESP-12F next year.

#### Baidu Netdisk Rant
I tried to download a data sheet for the custom ESP-12F, which was stored on Baidu Netdisk, the Chinese equivalent of Google Drive. The experience was terrible.

Instead of downloading from browser, a desktop app is required, which opens with unavoidable 5-second ads, is bloated with random functions, and has an incredibly slow download speed despite having great Wi-Fi connection. Consistently getting sub 150 KB/s in 2024 is absurd. It took a day to download 4 GB. (I later found out you need to buy VIP to unlock high speed download.)

![Baidu Netdisk Downloading Speed](/img/in-post/baidu.png)

The "datasheet" turned out to be 4 GB of an Android app APK and a 720p video explaining the product, with no actual data sheet. This experience, along with the terrible documentation for the JP Hobby ESC, emphasized the importance of providing detailed documentation to consumers. I vow to provide such for my future products to avoid such frustrations.

### First Time going to the Casino 
My friends recently all started going to the casino to play poker for some reason. I decided to tag along one night to see what's up. I ended up losing $50 while a friend lost $150. The only person who made a profit (+$72) had lost $100 the previous day, so it doesn't even count. What was alarming was that my first thought after losing $50 (despite having no job) was to watch poker videos and to watch Poker videos and comeback to play again. Thankfully, once I got home and my adrenaline lowered, I realized how dangerous this mentality was and decided to avoid the casino in the future. (My friends went back the next day; they desperately need help 🙏)

![Heading to the casino](/img/in-post/IMG_1498.jpeg)

### Hitting Silver in League

Besides the degen casino trip, I also managed to climb to Silver this week in League of Legends! (I uninstalled the same day, too much brain rot activities, I am pretty happy with silver)

![I hit silver!](/img/in-post/leagueoflegend.png)

