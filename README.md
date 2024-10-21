# Reality2 LoRa Mesh

This repository is set up to share what we are doing and have found out in terms of LoRa mesh networking that could support a Reality2 distributed system.

Please feel free to comment, help, give suggestions etc as you see fit.  This is intended to be a helpful resource and perhaps a learning tool.

Some links:

 - [Learn more about Reality2.](https://github.com/reality-two/reality2-documentation)
 - [What is LoRa Mesh?](https://hackaday.com/2020/02/26/lora-mesh-network-with-off-the-shelf-hardware/)
 - [Meshtastic - An open source, off-grid, decentralized, mesh network built to run on affordable, low-power devices](https://meshtastic.org/) <-- This one looks really good - uses different components that described in this document - could be well worth investigating further.

## Context

The rationale for this work sprung from a problem based in the district of Wairoa in Aotearoa / New Zealand that has been adversley affected by storms as a result of increased climate variability.

The problem to solve is "How do we notify people when all power and communications are down, that there is danger?"

We got to thinking that, perhaps, some form of battery powered device in each person's home, connected by mesh network, could be a viable possibility, and then we wondered what could be made from easily available components.  These pages are a condensation of that journey.

## On Resilience

In addition to being an emergency device, we wondered whether it could be used as a communication device at other times, and ultimately bring other information about the environment, fed from IoT devices, and processed by a Digital Twin.

## Questions

There are many questions, including (but not exclusively):

1. What processor is required (currently looking at ESP32 Firebeetle 2)?
2. What LoRa frequency do we use? Each country is different.  NZ seems to be 915-928 MhZ.  See the regulatory documents [here](https://iotalliance.org.nz/wp-content/uploads/sites/4/2019/05/IoT-Spectrum-in-NZ-Briefing-Paper.pdf).
3. How do we build mesh networks?
4. How many nodes can we have in a mesh network?
5. How far can the network stretch?  What is the distance between nodes?  How far between the farthest nodes?
6. What limits the network?  Eg buildings, hills, valleys.  Do we need repeaters at high points?
7. How much power does it require?  Can this be supplied by a small battery?  Can these batteries be charged by solar power?  How long will the batteries last?  Are there ways to optimise power?
8. How do we route messages from a source to a destination?  Or, do we assume all devices show the same information?  How do we ensure each is current and up-to-date?
9. What is the speed of communication? (we know that between nodes is typically 9600 Baud, but a mesh will use some bandwidth in itself).  What can we, realistically, transmit in terms of information?

## Structure

The proposed structure that we are exploring in these documents is, approximately, as below.  Here, we are going to be concentrating on the lowest levels, upto and including the LoRa Mesh Network.

<img src="./images/technology stack.jpeg" style="display: block; margin-left: auto; margin-right: auto;">

## Plan

1. Get some kit, do some soldering, add some programs, and try to answer the questions above.
2. Do this together.  This is all opensource technology, there are amazing maker communities on the Internet.  Let's all learn together.

## Contents

In this repository, I will assemble what I know, and have found out so far, and hopefully you will be able to add and improve.

- [Where to get components](./WhereToGetComponents.md)
- [Why LoRa Mesh?](./WhyLoRaMesh.md)
- [The first (simplest) Proof of Concept](./SimplestPoC.md)