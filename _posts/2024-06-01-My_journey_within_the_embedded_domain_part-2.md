---
layout: post
title: "My Journey within the Embedded Domain part 2"
date: 2024-06-01 01:00:00 +0100
categories: [Archive]
tags: [Experience]
---

### 2018

### Flagship BLE beast

This year, my then-company was already in the process of taping out their flagship BLE-based microcontroller (with an ARM cortex M33 and a cortex M0 co-processor) with an integrated PMU(power management unit). They also focussed on bringing out a low-power alternative based on a cortex M0 processor as well. When people around were talking highly about the flagship microcontroller, I picked up the reason for the co-processor unit on the chip. It was supposed to be a configurable MAC (also known as CMAC). This essentially allows the BLE stack implementation to be upgradeable during its lifetime via software updates without worrying about the PHY layer dependency.

![Overview of DA1469x]({{site.data.navigation.Images[7][0]}}) 

### What is a BOOTROM, and what do I have to do with it?

Soon enough, I was tasked with helping Dennis, the main bootrom developer for both these projects. Dennis, if I haven't said this before is one of the most skillful and intelligent engineers that I have come across at that point. He worked within the same company for almost 12 years in 2018. The bootrom development was nearing completion and had to be rigorously tested before deployment. If there was a chance of bootrom getting into serious trouble during boot up, that product is essentially bricked as the application firmware has to be recognized and loaded successfully by the bootrom to get to the next stages of execution. Mistakes in this development will cause huge $$$ losses to the company.

![Flowchart of bootrom from one of the older Dialog microcontrollers]({{site.data.navigation.Images[7][1]}}) 

### Hi Dennis!

Dennis had devised elaborate test plans to cover all known corner cases, possible failure paths, and the normal testing paths. The happy path of testing where everything is supposed to work was the simplest. The test cases would often be like "So the UART loading has to work. Try building an application and load the binary via the UART". The device depended on XIP (execute in place) with an externally connected QSPI flash. The device could also run from the application loaded into the RAM region as well. For testing the problematic cases, Dennis would often implement cases where the bugs and issues were automatically injected artificially during the bootup process. This helped to take care of correcting the possible corner cases within the flow of control.

Apart from performing all the tests on a physical FPGA with a software core of the soon-to-be taped-out microcontroller, we had the capability of performing gate-level simulations as well. The compiled bootrom would be loaded into this simulation and the gate-level behavior of the core would be observed to detect any undesirable/inconsistent behavior as well.

Apart from the technical aspects of the job, we had a good ping-pong table on the site. By the end of the work days, some of us managed to find bits and pieces of time to challenge each other in ping pong matches. Dennis is a really strong ping pong player with lots of casual play-time under his belt. The consistent play matches we had between us with ping-pong, really did strengthen the friendly bond that we started to develop.

### HTOL

In parallel, I was assigned the task of bringing up the HTOL(High-Temperature Operating Life) software for the new microcontrollers. This software essentially stresses all the different peripherals in the microcontroller to determine the wear-level handling. It should also be noted that this test, HTOL is usually run on 100s of units at a time in a climate-controlled test chamber with temperatures up to 100 degrees Celsius. After some days (1000 Hours) in the oven, running HTOL tests, these units under the test are then sent back to testing teams to evaluate their performance during the tests. 

### ARM Training

In the middle of the year, Simon sent me to ARM basic training at Doulos, in the UK, to pick up the basics of ARM architecture. At Doulous, excellent trainers used a well-crafted curriculum to demonstrate and display the basic concepts of how ARM cortex - M range of microcontrollers worked under the hood, right from instruction fetching, decoding, and pipelines. Various hard fault mechanisms and debugger options were also shown clearly.

![Certificate of completion from Doulos]({{site.data.navigation.Images[7][2]}}) 

Apart from on-site training, I focussed on online and on-demand courses from Udemy to enhance my skillset as well. Specifically, 

![Udemy certificate of completion for the program "Custom bootloader development"]({{site.data.navigation.Images[7][3]}}) 


