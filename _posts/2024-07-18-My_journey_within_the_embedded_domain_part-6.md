---
layout: post
title: "My Journey within the Embedded Domain part 6"
date: 2024-07-18 01:00:00 +0100
categories: [Archive]
tags: [Experience]
---

# 2022

Oh boy, this year was a roller coaster ride. I am certain that this post could be much longer relatively.

## Upskill

I began to look within and evaluate myself to understand better if I had mastered some basic and expected skills from an embedded software engineer. This reflection took me to the various corners of the internet in search of answers. Along the way, I was exposed to sophisticated software jargon such as design patterns, implementing object-oriented concepts in C, and test-driven development in C. I also used the custom NRF52 PCB and module by practicing Zephyr.

Stumbling upon some of the fantastic embedded software content from Dr. Miro Samek on YouTube, [Dr. Miro's content]({{site.data.navigation.Links[11][0]}}), I felt encouraged to venture into event-driven embedded software architecture.

## Advanced C user?

### Design patterns

![Design patterns by the gang of four]({{site.data.navigation.Images[11][0]}}) 

Back in the 90s, people in the software engineering world noticed that several software developers encountered similar problems in their day-to-day tasks. Some people decided to extract common approaches to solving these issues. Thus, the gang of four (the authors of the famous book, "Design Patterns") categorized these common approaches into three different categories. Creational design patterns provided flexibility in creating objects rather than instantiating them directly. One of the most common design patterns under the creational category that I've seen until now is the Factory design pattern, which can in runtime, create different types of objects as needed, and the singleton design pattern which ensures a resource-critical/sensitive class is instantiated exactly once during the lifetime of the application.

In the Structural design patterns category, I liked the decorator design pattern which enhanced the behavior of class member functions during run time. I found the adapter pattern that acted as an adapter between different classes to be interesting too. Finally, the behavioural design pattern has the most interesting design patterns within it. I found the observer pattern to be the most interesting of the bunch. I first noticed this type of behavior during the FreeRTOs training program where the notify feature of the RTOS worked similarly. Having worked with C programming for a while now, I wanted to experiment with all these design patterns using C. [My GitHub repo for design patterns in C]({{site.data.navigation.Links[11][1]}})

### Object-oriented C

![Miro Samek's application note]({{site.data.navigation.Images[11][1]}}) 

Dr. Miro has multiple useful application notes on his website, this one focussed on object-oriented concepts using C: [Miro's app note] ({{site.data.navigation.Links[11][2]}}). This application note, in combination with the YouTube content from Dr. Miro, has established a good foundation in my mind about the possibility of experimenting the object-oriented concepts using C.

### SOLID 

The term SOLID has now crossed me multiple times in the different articles that I have been reading through. It caught my attention as many people talked about it. Turns out, SOLID, a term made famous by "Uncle" Bob, is a set of guidelines/ good practices for modern software development. Following "Uncle" Bob's videos in YouTube does help to grasp the core concepts that the SOLID design principles advocate. I still don't agree with some of its recommendations (especially the recommendations of keeping function size super short) but SOLID is now widely accepted in the software development community to be standard good practices.

Kindly find my un-edited notes on design patterns, object-oriented C, and SOLID at the end of this article as observed in 2022.

### Test-driven development

Over the years, I have heard about unit tests being recommended everywhere by software developers. Strangely, the embedded software domain is quite silent on this topic. You will have to make a conscious effort to find the people in the embedded software domain who practice and preach this type of software testing. I had a chance to quickly run through the famous book "Test Driven Development for Embedded C" by James Grenning. (P.S. Later in 2023, I will invest considerable time and effort to read the book more carefully the second time and practice the code snippet exercises as recorded here: [TDD practice]({{site.data.navigation.Links[11][3]}}) )

My initial impression was mixed. (This is mostly because I couldn't see the big picture of where this TDD fits, yet). I grasped that such a concept exists and didn't care much to get to know or try experimenting more on the topic at that moment.

### Hierarchical state machines

Going through Dr.Miro's content on his website, [Quantum leaps]({{site.data.navigation.Links[11][4]}}), and on his YouTube channel, [Dr.Miro's YouTube]({{site.data.navigation.Links[11][0]}}), I became interested in learning more about UML, state machines, and event-driven embedded software architecture. On the Udemy platform, I took a course from Kiran on the same topic. I have more detailed observations on Dr. Miro’s content over here: [QPC - 1]({{site.data.navigation.Links[11][5]}}) and here: [QPC - 2]({{site.data.navigation.Links[11][6]}})

![Udemy certificate of completion for the program "Embedded System Design using UML State Machines"]({{site.data.navigation.Images[11][2]}}) 

At the end of the Udemy class, I was quite knowledgeable about UML, state machines, and event-driven embedded software design. I was able to practice by creating a kitchen timer experiment using the PCB that I created for the NRF52.

P.S. I'll make more detailed observations about Dr. Miro’s content later in 2023.

### LEETCODE!!!??

What in the fresh hell did I just stumble upon this year? 

After quite a while of working with Dialog semiconductors, I decided to look around and find more challenging embedded software-oriented jobs that could help grow my career. I joined a company which specializes in secondment. I'm a contractor now. To assess my software development proficiency, my current team lead who assigns me contracts to work at different companies made me take a leetcode style test. Boy was I unaware of this concept. Leetcode, to the uninitiated, is designed to be an assessment of a developer's ability to solve worthless programming problems at a given time limit. The higher the score is, the more valuable you'll be perceived. 

I never really understood the appeal of these tests or on-the-spot programming tasks during interviews as well. Some people just don't operate mentally, this way. Someone looking over my shoulder will hinder my thinking process. This doesn't mean I don't understand problem-solving through software development. 

Later I learned that this pile of garbage has spanned a whole industry that coaches young developers and software engineers to crack these Leetcode-style tests for a substantial premium. After all is said and done, even during the end of 2024 when this article is being authored, I struggle to find the necessity of this abomination.

My team lead in 2022 in the company specializing in secondment also wanted me to secure a scrum master certification. I read through the text prescribed by people knowledgeable in the domain and gave it a go at the certification test.

![My Scrum master certification]({{site.data.navigation.Images[11][3]}}) 

## Bosch video surveillance systems

Reviewing my leet code results, I was deemed good enough to work as an embedded software engineer at Bosh in its video surveillance systems as a contractor. Here, with a team consisting of 5 other embedded software engineers, I worked on a big video camera product. Interestingly, the other team members, even though being awarded the titles of embedded software engineers were quite reluctant to get hands-on with the hardware. I was assigned to handle tasks that arose with the motor controller inside the camera that handles the focus and zoom motors. This was essentially an STM32 microcontroller that talked with UART to the main Embedded Linux platform handling the main C++ based application for the camera.

The entire ecosystem around the camera development was indeed fascinating and helped me learn a bunch of good practices that are respected at corporate levels. If I remember correctly, the main embedded Linux processor is a common image signal processor (ISP) based on ARM that is available on the market (hint: google the term "image signal processor on a GoPro"). This processor did the heavy lifting of speaking with the image sensor and doing all sorts of enhancement and color magic on raw image pixel data. The manufacturer incrementally released new Linux images that improved certain aspects of the SOC and its reliability in some intervals.

The configuration scripts that the team had available to create a working environment were quite magical. A vagrant script is executed on the developer's machine that fetches the latest Linux image from the ISP manufacturer and spawns headless virtual machines ready for development. At the end of the script, the developers have access to the latest source code for the main application with git metadata and everything set up with Visual Studio to start development immediately.

Here is where I learned the effectiveness of working in git branches and making pull requests when the work is complete. Every task assigned to the developer would first satisfy internal integration testing to see if it does not break any existing functionality. Later, it is also encouraged to be mocked (if necessary) to see if it plays well with the simulated camera application. Finally, some unit testing is also recommended. 

### William

Being new to anything other than bare-metal firmware development, the current setup in Bosch intimidated me with its complexity now and then. My team at that point had an incredibly knowledgeable youngster named William who had impressive expertise in C++. When I had to request my peer developers to review my pull requests, I would often go to William to help me with that. He was kind enough to help me navigate the gargantuan C++ code base and helped me identify the factory pattern and the usage of dependency inversion.

It was interesting to observe the product release planning and deployment cycles of disciplined engineering teams in Bosch where all sorts of engineering teams come together to make it possible.

## Fabless startup 

At the end of the year, 2022, I had an opportunity to work at a startup that tried to tape out GPS-based microcontrollers. There, I had the chance to improve my Python experience by building a Windows-only programmer based on cli. This programmer talked with the USB FTDI chip on board the dev board and used the libMPSSE engine provided by the FTDI to create a custom SPI library capable of handling single SPI flash operations. I had a chance to improve the bootrom of the microcontroller. I was able to pick up the theory behind the GNSS protocol as well.


```
Unedited notes from back in 2022 about object-oriented concepts and SOLID

SOLID design and Object-oriented concepts in C

Reference: https://www.baeldung.com/solid-principles

Single responsibility principle: a class should only have one responsibility.
Furthermore, it should only have one reason to change.

Open-closed principle: classes should be open for extension but closed for modification 
(A popular generic example is USB. USB ports in computers help extension of capabilities
but are closed for modification)

Liskov substitution principle: objects of a superclass shall be replaceable with 
objects of its subclasses without breaking the application

Interface segregation principle: larger interfaces should be split into smaller ones. 
By doing so, we can ensure that implementing classes only need to be concerned about 
the methods that are of interest to them.

The dependency inversion principle refers to the decoupling of software modules. 
This way, instead of high-level modules depending on low-level modules, both 
will depend on abstractions.

A real-world scenario I observed SOLID: Flash-loader project built within DCTMon – 
Microcontrollers need to be interfaced with new SPI flashes from time to time, 
and application support is necessary.

The software architecture design restricted the main class to be responsible only 
for handling the microcontroller interaction with the SPI Flash – thereby 
fulfilling the single responsibility principle. 

The design further restricted modification to the main class except to fix 
bugs and issues that are found. This meant that the main class was closed 
to any modifications but was allowed to be extended further by inheriting 
the base class in the future if any such need arose.

The new supported flashes that are often added to the support list would 
be Quad SPI flash chips that offer 4X the normal data transfer speed. 
This prompted the design to allow the SPI flashes to be operated in two 
distinct modes 1. Normal mode and 2. Quad mode. Both the modes are hence 
interchangeable class implementations of the Flash class interface which 
now satisfy the Liskov substitution principle.

New flash devices are free to implement any functionality from the base 
interface class it deems fit thereby satisfying the Interface segregation 
principle. The design isolates the high-level interface and low-level 
code using function pointers and hence satisfies the dependency inversion principle.

```

```
Observations on object-oriented concepts:

Polymorphism - Overloading and Overriding are different - (static or 
compile time polymorphism) Overloading is when the class has multiple functions 
with the same name but different inputs (Dynamic polymorphism) and overriding 
is during run time where the abstract definition of a method from the parent 
class is defined again with different functionalities in the child class.

There are compile time or link time polymorphism and run time polymorphism as well.

Run time polymorphism is the technique where passing different function pointers 
to different places (Dependency injection?) makes the application behavior 
different during run time due to varying external/internal factors.

Build time polymorphism is the technique where you can replace the Hardware 
abstraction layer of a different target platform to create a portable 
application that works on multiple platforms.

Abstraction - Implementation hiding from external actors (to prevent misuse/modification)

Encapsulation - Objects that self-contain methods and attributes/properties 
into a single unit would be an example of Encapsulation

Inheritance - Base Classes can have their properties inherited by Child classes. 
Methods and attributes/properties from Base classes are usable by child classes.

```

```
Objects in C:

Structs are the de-facto objects in C

Inheritance is possible as new structs with base structs included in them can 
be up-converted (Up casted) to base struct and sent to functions that require base struct

Polymorphism is possible using function pointers and tables - In effect, the 
main function is going to reference a function with the same name, but 
depending upon the struct object the reference is going to invoke a different
function with a different struct. Hence polymorphism is achieved. One name, many forms.

Encapsulation is possible by encapsulating functions and data to be acted on 
into the same struct

```

```

Observer design pattern - Extremely useful design pattern that creates (Publishers 
that are called Subjects and Subscribers that are called Observers). 
Observer objects subscribe to Subject objects to be notified when data changes
or new data is available.

Strategy design pattern - Design pattern where the algorithm of the main 
application is divided into different objects that are called correct 
during runtime

Decorator design pattern - (Pizza example - Base Pizza is decorated by 
toppings) Here Pizza Base is the object to be decorated and the toppings 
class is the decorator object

Factory design pattern - A pattern where Objects are chosen at run time 
differently encapsulating important information about said objects

Design pattern - Opaque pattern

This pattern is derived from the normal object pattern where the struct 
with relevant data is declared in the header file and initialized in the 
accompanying c source file. Any other source file/module with access to 
the header file is free to use the object as they wish (De reference the 
object from outside the header/source combo where it was declared).

The opaque pattern takes it a step further where the header file does not have 
the struct definition but the source file accompanying the header file has the 
definition. This means that any source module outside even if it gets its hands 
on the object, would not be able to dereference or use it as per their liking. 
This does involve static memory allocation and de-allocation.

A prime example of this pattern is the python libmpsse dll combination. The 
libmpsse dll gives out a memory handle that all the functions within the dll need. 
Even though the user has the memory object or handle from the dll, they are not 
able to dereference it or use it. thereby isolating the user from the internals 
of the implementation.

Design pattern - Singleton pattern

The singleton pattern closely follows the Opaque pattern. consider this: you 
are technically limited to one opaque pointer. This is now a singleton. No 
multiple instances are allowed or technically possible.

Just like with the opaque pattern, forward declaring structs in the header file 
and defining them in the source makes any translatable unit/ source file 
outside impossible to dereference or use the object.

```
