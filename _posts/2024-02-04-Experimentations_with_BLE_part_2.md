---
layout: post
title: "Experimentations with BLE - part 2"
date: 2024-02-04 02:00:00 +0100
categories: [Bluetooth Low Energy]
tags: [BLE,DTM,stack]
---

## Direct Test Mode

![]({{site.data.navigation.Images[2][1]}}) 

To facilitate RF testing and validation on the production line, The Bluetooth SIG dictates a set of LE commands to be implemented that deal with the RF testing and validation. 

![]({{site.data.navigation.Images[2][2]}}) 

Direct Test Mode exists in the lower layers of the BLE stack. It enables direct communication between the BLE DUT (Device Under Test) and Bluetooth testers to control the DUT. In this experimentation, this is achieved by running the DTM application on DA14691. On a host computer, a Python script manages to talk with the BLE DUT through a UART port to send and receive commands and data. The RF terminal of the BLE DUT is connected to a Software Defined Radio called HackRF one through an SMA connector to analyze the BLE signal packets.

## Notes on the experimentation

[Github repo]({{site.data.navigation.Links[2][1]}})

Throughout the video that follows this section, I have noted my observations on experimenting with creating, capturing, and analyzing custom BLE packets using the DTM stack layer using a HackRF one SDR. 

![]({{site.data.navigation.Images[2][3]}})

The original BLE DTM packets recorded using the HackRF one, found in the GitHub repo, have the complex signals in IQ format. This is then used by the various blocks in the GNU Radio Companion flow model shown above to reconstruct, decode, and demodulate the original BLE signal sent by the DUT, resulting in a hex file containing the data sent from the DUT in a HEX file format.

In the video presentation mentioned above, several blocks are disabled momentarily, and raw output graphs are seen. Step by step, the disabled blocks are re-enabled, and the behavior change are also noted. Finally, the decoded and demodulated file in hex format can be found in the file path noted in the model.

## Experimentation with BLE DTM and HackRF one SDR

Please click on the image below to start the YouTube video presentation.

[![Part - 2]({{site.data.navigation.Images[2][0]}})]({{site.data.navigation.Links[2][0]}})
