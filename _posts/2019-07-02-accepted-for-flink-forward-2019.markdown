---
layout: post
title:  "Accepted for Flink Forward 2019"
date:   2019-07-02 18:19:19 +0200
categories: talks
---
I am very pleased to say that my talk submission for [Flink Forward 2019](https://berlin-2019.flink-forward.org/) has been accepted and that I will be presenting at the conference on 8/9th October 2019.

This talk is directly related to research I have been performing as part of my Master's Thesis.

I will update this page with more details about the talk and a recording as they become available. For now, see below for the talk abstract.

\- Matthew

### Moving on from RocksDB to something FASTER
For many years streaming applications requiring larger-than-memory fault-tolerant state have settled for RocksDB as the de facto state backend. This is despite it being optimised for read and range queries rather than the update intensive workloads typically exhibited in stream processing. Several features of RocksDB’s design, such as its key-order page format and Read-Copy-Update approach, become limiting factors in the throughput of state updates. Given these limitations, we have evaluated the use of FASTER, an embedded Key-Value store from Microsoft Research, as an alternative backend that is more suitable for streaming workloads. It uses in-place updates on a changeable “hot” set in-memory and a cache-optimised hash index to ensure a high throughput of point operations on its HybridLog that spans memory and disk. In this talk we present benchmarking results for different streaming workloads highlighting the performance differences between FASTER and RocksDB. We use these results to motivate an integration between FASTER and Timely Dataflow, with promising results demonstrating FASTER’s suitability as the state backend of choice for large stateful computations. Finally, we will show the early results from the integration of FASTER with Flink.