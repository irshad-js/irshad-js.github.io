---
layout: post
title: "Experimentations_with_QPC_part_1"
date: 2024-03-16 02:00:00 +0100
categories: [Hierarchical state machines]
tags: [HSM,QPC,STATECHARTS]
---

# Recommended reading and prerequisite know-how

Harel Statecharts are advanced concepts within the domain of state machines. They introduce the concept of Hierarchical State Machines (HSM) where states can be designed as super-states and sub-states when necessary (thereby preventing state implosion when the complexity of the system scales up). Working on top of the primitive state machine mechanisms, the HSMs introduce a multitude of powerful additions such as:  

- Entry action
- Exit action
- Internal transition
- Local transition
- External transition
- Initial transition
- History states
- Orthogonal regions
- Sub-states
- Super-states

Prof. David Harel has an online-based free-to-audit course in the EDX learning platform named "IsraelX: Programming for Everyone – An Introduction to Visual Programming Languages". In this course, he explains how humans are beings capable of working effectively with visual paradigms and convinces students that visual formalism helps construct resilient and robust systems.

There exist UML notations to assist us in representing states and transitions as prescribed by Harel in his statechart technique. Dr. Miro Samek, a veteran in the domain of embedded systems programming has taken the statechart concept and constructed a set of real-time embedded software frameworks around it and named them QPC/C++. In combination with the QPC and QPC++, Dr. Miro also has an instrumentation tool named QSPY built into the framework to help understand the system's internal working with minimal overhead.

![]({{site.data.navigation.Images[3][0]}}) 

Dr. Miro has a meticulously crafted book named "Practical UML Statecharts in C/C++: Event-Driven Programming for Embedded Systems" where he introduces the concept of HSM for newcomers along with providing them the techniques to use UML notations to visualize the systems in an event-driven formalism. Throughout the book (which is 700+ pages!), Dr. Miro painstakingly walks through his dual-licensed real-time embedded software framework "QPC", taking the time to explain why conventional real-time operating systems that use the blocking principle are inferior in effectiveness when compared with the Run-To-Completion principle adopted by the real-time embedded software framework "QPC".

Dr. Miro also has an incredibly awesome YouTube playlist which covers: 

- Embedded software programming from the basics
- ARM microcontroller architecture basics
- Design of conventional real-time operating systems
- State machine principles
- Event-driven architecture
- Object-oriented software principles
- Active objects
- Software Instrumentation with QSPY

Mr. Kiran Nayak has a Udemy course titled "Embedded System Design using UML State Machines" that is based on the concepts found in the book "Practical UML Statecharts in C/C++: Event-Driven Programming for Embedded Systems" written by Dr. Miro. In this recommended course, Mr. Kiran explores the concepts of UML and the different ways to create firmware using state machine concepts. Near the end of the course, Mr. Kiran explored the now-retired version of QPC called QP nano focussed on microcontrollers with low memory footprint. Also, he helps us understand the QM modeling tool effectively as well.

# Hardware and Software pre-requisites

In the following parts of this topic, I will experiment with the real-time embedded software framework "QPC" and the software tooling that exists around it uses a 32-bit ARM Cortex-M4 based microcontroller "NRF52832".

Here is the list of hardware and software requirements if you would like to join me in the experimentation:

- Embedded software studio from Segger (SES)
- Any NRF52 based dev-kit
- Jlink or any compatible debugger capable of working with SES
- Nordic NRF5 based SDK

Join me in the next section to see HSMs in action.
