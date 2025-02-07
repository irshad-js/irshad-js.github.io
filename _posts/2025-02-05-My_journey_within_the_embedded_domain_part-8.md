---
layout: post
title: "My Journey within the Embedded Domain part 8"
date: 2025-02-05 01:00:00 +0100
categories: [Archive]
tags: [Experience]
---


# 2024

## Overview

The year 2024 allowed me to learn and experiment a great deal of concepts such as Hierarchical State Machines, Software modelling / Simulations, CI/CD, CMake, Static Analyzer, Python prototyping, PCB design, and finally revisiting basics/foundational level electronics class.

## Hierarchical State Machines

I was able to spend some time setting up and pipe cleaning an environment with my custom NRF52 PCB (link to the PCB) to experiment with active objects and model-driven development using QM (QP framework). 

After the successful setup, I started some hands-on experimentation with the basic feature set of QPC such as 

- Direct event posting to AO
- Timeout events
- Publish subscribe event delivery 
- Mutable event posting to AO

Finally, I refreshed my understanding of the history state usage through the QPC nano experimentation video tutorials from an Udemy course on UML (by Kiran Naik of fastbit embedded).

The hands-on experimentation of the various important concepts of the QP framework helped to cement the understanding of the theory and the various difficulties in real-world implementation.

[QPC -1]({{site.data.navigation.Links[13][0]}}) and [QPC-2]({{site.data.navigation.Links[13][1]}})

## Software Modelling and Simulations

After a while in the gas detection industry, I was now exposed (pun intended) to the operational theory of portable gas detection instruments, their alarm behavior, calibration, battery handling and data handling routines. In short, I’ve levelled up a bit with my gas detection expertise and knowledge.

I was able to leverage my QPC knowledge in this case when I decided to create a simulation model of a gas detection device to improve upon my software modelling skills. In short, I learnt to use the wxWidgets platform to create a front end visualization of a portable gas detection device. The back end processing/logic of the instrument was modelled using the QM tool and the resulting firmware was modified to run on an X86 Host machine (in this case Windows 10). When both these software were connected to each other and compiled together using C++ (and sometimes combined with C), they worked flawlessly on the host machine.

Following the success of this host machine combination, I ported the state machine firmware to the hardware platform on the portable gas detection device and was successful in that case too.

{% include embed/youtube.html id='423iz-gy4ro' %}


## CI/CD - CMAKE

The firmware development process of the equipment under development in my position was entirely manual with vendor-lockin tools and processes. This meant that team work and validation was error prone and difficult while collaborating.

This was where my CMake skills came in handy. I was able to port the compilation process of the firmware from the vendor IDE using their custom on-demand Eclipse makefile generation to a Visual Studio Code environment with CMake environment. Two different build profiles (Debug and Release) were created for more convenience.

An added advantage to this CMake environment was the dead simple integration with dockerfile and the CircleCI pipelines. Finally, I built a firmware pipeline where, when a developer makes a commit, the CircleCI activates and builds the firmware binary in the cloud. The firmware binary is then zipped into release and debug zips that any developer could download and use.

The firmware binary itself wasn’t enough in this case for testing/development as the onboard bootloader will not allow firmware binaries with different CRC results than that of the CRC result stored within the bootloader boundary. Here, python was used to sandwich a bootloader binary with the firmware binary on the cloud to generate an executable combination.

Finally, just for the sake of completion, some final touches were added in the CircleCI pipeline such as the ability to embed the git message as changelog in the firmware binary, compiling the binary using Clang tools, and running the static analyzer CppCheck on the firmware to generate firmware stability reports.


## Back to the basics

For some time now, I’ve always had this voice in the back of my head that said I was long overdue for a full-blown refresher course in the fundamentals of electronics. This year, I decided to listen to the voice and did just that.

I selected a couple of Udemy courses and decided to give them a go. The first course that intrigued me was (link). Crash Course Electronics and PCB Design by the author Andre Lamothe that had 161 hours of theory and explanation. For the first time, I listened through the entire course and completed it. But then, I wanted to at least follow along with the course by doing calculations on paper and simulation on the computer. So, for a second time, I went through the course as well, but this time, performing all the calculations/derivations and simulations of the theoretical concepts as I went along with the course.

The other course titled The Complete Electronics Course: Analog Hardware Design in Udemy was a nice complement to Andre’s one. This one had at least 24 hours of content and I was able to follow along with the content by simulating the concepts on the falstad webpage.

[Revisiting Electronics]({{site.data.navigation.Links[13][2]}})

A huge advantage I gained because of these courses was the my hesitation and fear of using/coming across BJT transistors, MOSFET transistors and OPAMPS were gone as I now deeply understood the theory and practical usage of these discrete components.
