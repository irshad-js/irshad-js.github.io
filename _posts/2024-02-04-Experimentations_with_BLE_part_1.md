---
layout: post
title: "Experimentations_with_BLE_part_1"
date: 2024-02-04 02:00:00 +0100
categories: [Bluetooth Low Energy]
tags: [BLE,DTM,stack,Book review]
---

# Recommended reading

This isn't a blog post introducing the readers to the technical details behind the Bluetooth Low Energy protocol as there exists already a wealth of such information authored by individuals and organizations working with BLE. Some of the most helpful introductory work to understand Bluetooth Low Energy can be seen in Robin Heydon's book titled "Bluetooth Low Energy: The Developer's Handbook".

![]({{site.data.navigation.Images[1][1]}})

In his book, Mr. Robin Heydon starts by introducing the readers to the power consumption requirements for the legacy Bluetooth classic protocol and the need for a much more power-optimized protocol in this current generation where everything has to connect to the World Wide Web. Also, he dedicates a chapter to each of the layers in the Bluetooth Low Energy stack and explains carefully how they all come together to create a power-efficient wireless protocol. Going through this work, I felt everything about the BLE protocol has been talked about and covered.

![]({{site.data.navigation.Images[1][2]}}) 

Another helpful reference book is from Mr. Mohammad Afaneh titled "Intro to Bluetooth Low Energy: The easiest way to learn BLE".

Though the protocols share a common name, Bluetooth Classic, and Bluetooth Low Energy enjoy vastly different use-case categories in the consumer market, with Bluetooth Classic taking the dominant position in wireless audio and Bluetooth Low Energy taking the dominant position in the low-powered wearables and the Internet of Things category. Though that was the case until some time ago, Bluetooth Low Energy has had consecutive protocol version updates recently that are set to de-throne Bluetooth Classic in its domain of wireless audio.

I've condensed my observation/experimentation on the inner workings of the protocol, especially, the Direct Test Mode layer of the BLE stack in a two-part blog post. At the end of this blog post, I have made a video presentation to introduce the hardware and software environments I used as well as the basic know-how that is necessary to follow along. I believe in learning by doing.

# Introduction to the experimentation

Please click on the image below to start the YouTube video.

[![Part - 1]({{site.data.navigation.Images[1][0]}})]({{site.data.navigation.Links[1][0]}})
