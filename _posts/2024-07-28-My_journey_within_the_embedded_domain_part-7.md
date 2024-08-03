---
layout: post
title: "My Journey within the Embedded Domain part 7"
date: 2024-07-28 01:00:00 +0100
categories: [Archive]
tags: [Experience]
---


# 2023

## Refinement of Python skills

I was tasked with developing the Python-based programmer tool for this startup that I have been working with. The idea was straightforward, The host PC has to speak with the FTDI IC on board that is connected to the single SPI flash on board. This SPI flash was also electrically connected to the microcontroller. At one time, either the FTDI could talk to it or the microcontroller. The microcontroller does not have any inbuilt flash region and hence has to rely on the external SPI flash for application image storage.

FTDI has library implementations of their MPSSE (Multi-Protocol Synchronous Serial Engine) called LibMPSSE that can on-the-fly change the target serial protocol. I used Python to interface with this libMPSSE library to make the interface USB to SPI serial device. I then constructed the necessary SPI flash handling routines. Finally, a cli was built that could take the COM port number and the application binary image to flash the image onto the single SPI flash using single SPI operations. During my time over there, Nathan, an incredibly experienced embedded systems expert from The US who is also my firmware team lead made himself accessible for code reviews and to help me get new perspectives in problem solving using software development. Nathan was kind enough to take the time to review my Python cli programmer during various milestone features to give me a good idea of how better software could be crafted. It is from him that I understood the need for a continuous integration pipeline. The bitbucket plan our firm used had some free compute minutes which Nathan used up to perform builds and other smoke tests.

## Upskill

### Beningo's book

Curious from multiple sources pointing to the book titled "Embedded Software Design: A Practical Approach to Architecture, Processes, and Coding Techniques" by Jacob Beningo to be incredible, I picked up a copy to go through.

[Embedded Software Design : Jacob Beningo]({{site.data.navigation.Images[12][0]}}) 

Color me impressed; this book was one of the best books that I have read within the domain of Embedded Systems. Some of the most interesting things to me were:

- Overview of available Embedded Software Architectures
- Traditional vs Modern Embedded Software development
- Overview of security and good practices
- Need for code instrumentation and performance analytics
- Different software metrics
- Embedded Devops and TDD
- Modeling, Simulation, and Code Generation
- Practical advice on reusable abstractions and APIs

A key takeaway for me when I completed reading through the book was that modeling and code generation in combination with UML could be super useful if you let it help you. Somehow, I slowly started believing that meaningful firmware development could be carried on even without the hardware. This was easily a game changer ideology for me as I had developed over the years a very nasty premonition that kept me hoarding hardware even when it was unnecessary.

### James Grenning's book and a related Udemy course

From time to time, I like to revisit the book titled "Test Driven Development for Embedded C" by Jacob Beningo. This time around, I was more mature than during my previous read-through. I decided to work out or walk through all the code examples and exercises found in the various chapters of the book. During this experiment, I have recorded my screen for future reference. If you would like to take a quick look at my walkthrough, the link is here: [TDD code-walkthrough]({{site.data.navigation.Links[12][0]}})

[Test Driven Development for Embedded C : James Grenning]({{site.data.navigation.Images[12][1]}})

This time around, the chapters at the end of the book focussing on SOLID principles were more understandable for me. The various ways to handle CppUTest to test units during development were fun. Working through the example code and the exercise codes has given me enough confidence necessary on the topics of mocks, stubs, unit tests, harnesses, CppUTest, fakes, and other TDD-related jargon.

Fresh off from James Grenning's TDD book, I wanted to test out my newly gained skillset. Udemy has a test-driven development-related course program titled "Interaction Tests, Mocks & Refactoring in Embedded Software". This course, interestingly the most expensive course purchase I have made to date, is structured so that a hardware kit is completely optional. The coursework has a self-contained docker image that has all the tools/software and source code necessary to complete the study. This course uses the testing framework called Unity which was invented by the same course instructors. The framework which is completely written in C has companion tools and modules created in the Ruby scripting language. Truly test-driven development could be observed here. The instructors also introduce various useful design patterns during the course. At the end of the coursework, if the course structure was followed, an application image could be developed without the aid of the respective hardware.

[Interaction Tests, Mocks & Refactoring in Embedded Software]({{site.data.navigation.Images[12][2]}})

### David Harel and Dr. Miro Samek

I have quickly read through Dr. Miro Samek's book titled "Practical UML Statecharts in C/C++, 2nd Ed" once already, albeit being a quick read that time. This year I decided to sit down and go through the book once more thoroughly. My thoughts on the book are noted here in my other [blog post]({{site.data.navigation.Links[12][1]}})

[Practical UML Statecharts in C/C++, 2nd Ed: Dr. Miro Samek]({{site.data.navigation.Images[12][3]}})

After this thorough read-through, I tested out my understanding of various event-driven software development concepts on my custom NRF52 PCB which I have composed into a [blog post]({{site.data.navigation.Links[12][2]}}). I have more thoughts to record on this topic, which I'll do in the next post for 2024. As a side effect of going through the book, my curiosity was piqued when Dr. Miro demonstrated his Qwin toolset which is a quick graphical toolkit that accompanies his real-time embedded framework. I whipped up a quick demo of my liking using his Qwin toolset

[Demo simulation]({{site.data.navigation.Images[12][4]}})

Dr. Miro Samek references the concept of hierarchical state machines as created by Professor David Harel from Israel. Since I liked the idea and convenience of the hierarchical state machines over normal state machines, I decided to learn more directly from the inventor. Lucky for us, Professor David Harel co-handles an impressive Edx-based course titled "Programming for Everyone – An Introduction to Visual Programming Languages".

[Programming for Everyone – An Introduction to Visual Programming Languages]({{site.data.navigation.Images[12][5]}})

Choosing to go through this program is a profitable investment. Prof David Harel and his co-instructor make good explanations about the theory behind state charts, live sequence charts, and related misc. The way these concepts give way to effective modeling of systems and algorithms makes them look like a match made in heaven. Don't forget to read through prof David Harel's initial scientific paper on statecharts and their effectiveness which includes a statechart representation of a common Casio digital watch.

I was also surprised to know that there are dedicated tools in the market now, that focus on statecharts and advanced state machines & code generation (for example Yakindu).

## Gas detection

Halfway through the year, I had an opportunity to explore the field of gas detection. I took the said opportunity. 

### Hojat

Here is where I met Hojat. Hojat is my firmware development team leader who arrived from Iran a year earlier. He initially started as a test engineer who eventually had a major impact on a problematic single-gas detection product that had been in the works for over a year or two. (It is said only because of his timely intervention has the product has been released in a timely fashion). The firm realized how important, impactful, and knowledgeable he is in the general field of electronics and engineering which made him promoted to firmware lead. To my surprise, Hojat mentioned that before arriving in the Netherlands, he and his wife Mahboub founded and successfully maintained a custom embedded hardware/software solutions company which made a variety of ATEX_certified products for the gas-detection industry, Radar-based Silo content estimation, Greenhouse controllers etc.,

Hojat was and is still sad that he had to leave his firm due to personal and political reasons from Iran. I am not able to share the exact reasons so that I don't infringe on confidentiality and his privacy. Over the time I have been working together with Hojat, it is nothing short of amazing. Hojat is a very highly skilled engineer able to tackle problems from any engineering segment without breaking a sweat. I was able to learn various problem-solving mindsets and approaches from him which I still think are just awesome. His interpersonal skills are nothing short of awesome as well. It is here, with him, that I felt the closeness of team-mates that I felt back in Dialog with Dennis! It was an expensive lesson for me to understand that moving jobs for any reason isn't completely awesome if the people do not want you there.

### Processor port

During the chip shortage era, it became difficult to procure some of the main microcontroller parts that one of our single gas detector units was running on. Hence, it naturally became obvious that we had to port the device to run on a different microcontroller. The team had chosen GD32 and one of its line of microcontrollers to replace the existing one. On the same topic, the first task that I got was to port the standard GD32 software development IDE and toolchain from being based on an Eclipse platform to a VSCode platform. To do this, I had to learn CMake thoroughly.

Fortunately, Udemy had a fantastic course titled "CMake, Tests, and Tooling for C/C++ Projects [2024 Edition]" which explained the Makefile for Makefile more thoroughly. The instructor was patient enough to start from scratch and explore all the features the Cmake offers.

[CMake, Tests and Tooling for C/C++ Projects]({{site.data.navigation.Images[12][6]}})

I would love to recommend this course to anyone willing to learn more about complex build systems.

Armed with critical Cmake know-how, I started to create a build environment for the GD32 microcontrollers mainly focussed on VSCode. The CMake scripts integrated well with the VSCode environment. I was able to bring up debug and release builds separately. I recommended the developers to take advantage of Jlink's pre-existing debugging software to start debugging the application images. Interestingly, a side effect of this whole situation was that a docker file mimicking the build setup now could be easily leveraged by CI/CD pipelines to build application binaries on the cloud. I used CircleCI to take care of the CI/CD pipelines. Docker images could be further leveraged by adding static analysis tools (CPPCheck and Clang-tidy) that are used during the analysis stages of the CI/CD pipelines. Being introduced to clang-tools, I quickly saw an opportunity to use the clang-tidy for static analysis and clang-format for unified code formatting. The Cmake script was further extended to incorporate Clang build tools to compile and link the source code in addition to GCC.


