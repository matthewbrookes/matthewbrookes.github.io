---
layout: post
title:  "Presented at Flink Forward 2019"
date:   2019-10-22 18:19:19 +0200
categories: talks
---
Just over two weeks ago I gave a talk at [Flink Forward 2019](https://berlin-2019.flink-forward.org/) on the topic of State Management for Streaming Applications and the
performance of different state backends. This talk was directly related to research I performed as part of my Master's Thesis.

A recording of my talk has now been uploaded to YouTube so I am linking it here.

<iframe width="560" height="315" src="https://www.youtube.com/embed/xWNbbkQMtfI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

\- Matthew

### Moving on from RocksDB to something FASTER
For many years streaming applications requiring larger-than-memory fault-tolerant state have settled for RocksDB as the de facto state backend. This is despite it being optimised for read and range queries rather than the update intensive workloads typically exhibited in stream processing. Several features of RocksDB’s design, such as its key-order page format and Read-Copy-Update approach, become limiting factors in the throughput of state updates. Given these limitations, we have evaluated the use of FASTER, an embedded Key-Value store from Microsoft Research, as an alternative backend that is more suitable for streaming workloads. It uses in-place updates on a changeable “hot” set in-memory and a cache-optimised hash index to ensure a high throughput of point operations on its HybridLog that spans memory and disk. In this talk we present benchmarking results for different streaming workloads highlighting the performance differences between FASTER and RocksDB. We use these results to motivate an integration between FASTER and Timely Dataflow, with promising results demonstrating FASTER’s suitability as the state backend of choice for large stateful computations. Finally, we will show the early results from the integration of FASTER with Flink.