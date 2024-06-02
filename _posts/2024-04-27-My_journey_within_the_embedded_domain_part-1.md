---
layout: post
title: "My Journey within the Embedded Domain part 1"
date: 2024-04-27 01:00:00 +0100
categories: [Archive]
tags: [Experience,Dialog,Simon,Dennis,Wik]
---

### 2017

![]({{site.data.navigation.Images[6][3]}}) 

In 2017, I reached the final leg of my master’s degree in Embedded systems at TU Chemnitz, Germany. While working on my final research project and getting my master's thesis ready for submission, I started applying for entry-level embedded software engineer positions within Germany.

![]({{site.data.navigation.Images[6][4]}}) 

It won't be a surprise to many reading this, in case you are unaware, the German Labor market for non-German speakers is incredibly unforgiving. After about 150+ applications to entry-level embedded software engineer roles and receiving not even one interview invitation, I focussed on the neighbouring countries as well.

I applied for a graduate-level embedded software engineer role in The Dialog Semiconductors, located in Den Bosch, The Netherlands. I was pleasantly surprised when I was invited for a telephone interview. I spoke with my then-boss, Simon. We had a good chat together on both technical and non-technical items. Looking back, I regret my answer when he asked me where I saw myself in the next 5 years. I told him, "I would like to be where you are now, as a manager". Sometimes, thinking back on this doesn't even make me chuckle, rather embarrassed.

Simon invited me on-site for a technical interview. I met him and then teammates, Wik and Dennis. All three of them probed me with various basic embedded software and hardware-related questions. After the interview was complete, I went back to my student hostel in Chemnitz, Germany. In a month, I received word from the hiring team at Dialog Semiconductors that I was offered a role there. I happily accepted the role and moved on to formally complete my master's degree as well.

![]({{site.data.navigation.Images[6][2]}}) 


In the last quarter of 2017, I moved to Den Bosch, The Netherlands to start my role as a graduate embedded software engineer. Simon, Dennis, and Wik welcomed me into their team. Simon, my direct boss is also responsible for at least 20+ engineers offshore. Our team directly reported to him. 

![]({{site.data.navigation.Images[6][1]}}) 

Wik, the most senior talent on the team, originally started his career/profession as a mechanical engineer. Later down the line, by switching roles strategically he landed a role that mixed software and hardware. Dennis, almost 10 years senior than me focussed on electronics at the end of his academic journey, thus leading him to this team. Regarding our daily activities, Dennis focussed on developing bootloaders for a new range of microcontrollers that Dialog Semiconductors released to the market. Wik, on the other hand, took care of Direct Test Mode (Lower-level Bluetooth Low Energy stack) related tasks. Until quite recently before I joined, the company was famous for its wireless DECT-related solutions. They gradually saw potential with the low-powered BLE and switched to it.

![]({{site.data.navigation.Images[6][0]}}) 

During the start of my career and job, I was asked to start learning the local build and development ecosystem by familiarising myself with the DA14195 and DA14495 range of microcontrollers that had DECT radio capabilities and an Xtensa DSP processor inside along with an ARM cortex M0 for the CPU. Interestingly the units ran off a QSPI flash memory unit. This surprised me at the time as I hadn't heard much about this specific QSPI controller yet. My teammates demonstrated the awesomeness of the peripheral when they probed a memory range associated with that peripheral and the unit responded with data in the memory range (from within the external QSPI flash) without any user intervention to handle the SPI flash commands. This type of boot-up mechanism and external peripheral handling impressed and amazed me. Meanwhile, along with a standard company-issued laptop, I was also provided with state-of-the-art debugging tools such as a logic analyzer, and Jlink debugger and access to a fully equipped scientific lab with even more serious/expensive test equipment.

Our sister team had an engineer [], who has been in the industry for so long that he even used tapes to feed in and feed out computational tasks. Quite some years ago, maybe in the 90s, he was tasked with creating/developing a microcontroller evaluation suite that the engineers in the other departments could start and talk with their microcontrollers, probing their memory ranges, reading, and writing to specific memory ranges. The application was called DCTmon, and it was also capable of many things, notably the ability to take the in-house generated data sheet of the microcontrollers and display a visual tree of peripherals that the user can read and write to. I was tasked with learning, maintaining, and developing the in-house development tool as they didn't have any active maintainers working on it.

As a maintainer of the internal characterization tool, I was also tasked with debugging/developing flash loaders for various old and new devices. I used the opportunity to develop a generic flash driver based on the JEDEC standard. Every FLASH memory device that was JEDEC compliant was able to operate with the generic flash loader.

The environment was conducive enough to encourage me to start a journey of learning embedded system (software and hardware) concepts and become experienced within them.

