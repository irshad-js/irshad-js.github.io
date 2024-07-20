---
layout: post
title: "My Journey within the Embedded Domain part 5"
date: 2024-07-17 01:00:00 +0100
categories: [Archive]
tags: [Experience]
---

### 2021

### Work, as usual

Some major life events this year had put a wrench on my usual learning. Most of this year focussed just on work and getting by. In my current position, I was tasked with bringing up HTOL software for a couple of new microcontrollers taped out from Dialog. On the side, there were major updates to DCTmon as well. Apart from all these activities, I got a bit a little bit by a legacy beast that was being sold during the DECT times. This was a text-to-speech engine developed in the 90s by Gerard. One of the companies that licensed this technology wanted an update and this task subsequently fell on my desk. Chasing the combination of source code and its suitable toolchain used for compilation took a considerable amount of time.

### Embedded Online Conference

To my surprise, our Greek colleagues sent us an email during the middle of the year stating that Dialog is a sponsor for the current year's Online Embedded Conference. To the people not yet introduced to the concept, EOC (Embedded Online Conference) is an online-only congregation of like-minded embedded specialists. During the conference, special speakers from various industries volunteer their time and energy to share their learnings and experiences with a wider audience. There are theater talks, pre-recorded presentations, live workshops, and keynotes from industry-recognized juggernauts. This conference is recorded and archived. Catching a lucky coupon code from one of the organizers (Stephane and Jacob) makes the whole ordeal much more affordable if your company doesn't want to sponsor a seat on it.

![Attendance certificate]({{site.data.navigation.Images[10][0]}}) 

### Software Defined Radios and BLE deep dive

During one of my regular visits to the front page of Hackaday.com, I stumbled upon the concept of a Software Defined Radio (SDR). To the people who are not introduced to the concept, SDRs are software-customized radio transmitter/receiver working in a varied band of radio frequency, the HackRF is capable of tx/rx in the 1 MHz to 6 GHz band.  The versatility of these SDR prompted me to get my hands on one of the open-source SDR from GreatScott gadgets called HackRF. 

![Image of HackRF's internals from the internet]({{site.data.navigation.Images[10][1]}}) 

The creator of HackRF, Mr.Michael Ossmann also has a comprehensive training program with a good set of accompanying training videos to help newbies like me get into the world of experimenting with the radio spectrum. Find the link here : [HackRF training]({{site.data.navigation.Links[10][0]}}).

Halfway through the training and experimentation with HackRF, I thought to myself, what if we try to receive and decode BLE packets from scratch? Normally, BLE data is transmitted through 37 of the 40 available channels that are 2MHz wide. The advertisements are transmitted on the other 3 channels. I estimated that sniffing a BLE connection/transaction happening between two BLE devices is going to be much harder with the frequency hopping algorithm and the bandwidth limitation of HackRF. This is where the DTM work that I have been assisting Wik with, came in handy. I understood that most manufacturers of BLE microcontrollers nowadays ship out an application that can take custom commands from the user to perform various customized BLE packet transmission sequences. I used one of these DTM applications and recorded the TX on the microcontroller during a known custom packet transmission. Then using GFSK decoding and other filters and misc, helping tools from GNU Radio, I was able to decode the exact data that I sent using the DTM application. Find my experimentations on the topic here: [BLE DTM decoding - part 1]({{site.data.navigation.Links[10][1]}}) and here: [BLE DTM decoding - part 2]({{site.data.navigation.Links[10][2]}}).

![BLE experimentation with HackRF]({{site.data.navigation.Images[10][2]}}) 



