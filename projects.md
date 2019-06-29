---
layout: page
title: Projects
permalink: /projects/
---

## Master's Thesis - FASTER State Management for Strymon
As part of my exchange program at ETH Zürich I am writing my thesis in the [Strymon](http://strymon.systems.ethz.ch/) research group. The group's focus is on simulating and performing online analysis of large datacenters. For my thesis I am designing and implementing an integration between Strymon and [FASTER](https://www.microsoft.com/en-us/research/project/FASTER/), an embedded Key-Value store, that will allow dataflow computations running on Strymon to support larger-than-memory state.

As part of this project I am working on an open-source Rust wrapper around the FASTER C++ library called [faster-rs](https://github.com/faster-rs/faster-rs/). This `crate` allows any Rust application to use FASTER as a Key-Value store for any serialisable `struct`.

## Third Year Group Project - Reconstruction of non-rigid objects from RGBD data
In the third year of my MEng Computing degree I worked as part of a group to produce an open-source implementation of [DynamicFusion](http://grail.cs.washington.edu/projects/dynamicfusion/papers/DynamicFusion.pdf), a SLAM system capable of reconstructing deforming scenes. Our project won the Palantir Forward Group Project Prize for software engineering excellence applied to solve an important real-world problem. Our project was also featured on the Department of Computing's website.

For more information download our [report](../assets/dynamic-fusion-report.pdf).

## SafeSpace
As part of IC Hack 2018 we created a Chrome browser extension that leveraged Microsoft's Cognitive Services to block images which matched a user-specified blacklist of keywords. The extension allowed users to either blur, block or replace the offending image.

I worked predominantly on the backend, focusing on interacting with Microsoft's API and caching results in Redis to prevent over-use of the API key.

All of the code is available in our [GitHub organisation](https://github.com/ICHack18).

## Huyendo
At the HackUPC Fall 2016 edition we created a web-based application to construct price estimates for a multi-legged trip. Our application allowed users to specify the amount of time they wanted to spend at each stop in ther trip. We used the Skyscanner API to fetch price estimates and the Amadeus API to enrich information about airports and locations.

For this project I worked mostly on the frontend design, learning how to use React JS to build a Single Page Application.

All of the code is available in our [GitHub organisation](https://github.com/HuyendoUPC).

## Alpaca
At my first hackathon, IC Hack 2016, we built an Android application for "crowd-sourced playlisting". The application allowed DJs to create a playlist and have users up/down-vote indivdual songs such that popular songs would be played first. The application also tracked accelerometer usage as an indicator for the DJ of how much people were moving to the music. We won several prizes for this project.

Most of my time was spent developing the Android application, in particular the backend of the application that dealt with interacting with the API we were also creating.

All of the code is available in our [GitHub organisation](https://github.com/AlpacaICHack).