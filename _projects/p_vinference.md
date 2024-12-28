---
layout: page
title: Video QoE Inference
description: ""
img: 
importance: 999
category: Projects
tags: [Inference, dataset, Sigmetrics]
---

We developed a system that accurately infers video streaming quality metrics in real time, such as startup delay or video resolution, by using just a handful of features extracted from passive traffic measurement. Network Microscope passively collects a corpus of network features about the traffic flows of interest in the network and directs those to a real-time analytics framework that can perform more complex inference tasks. Network Microscope enables network operators to determine degradations in application quality as they happen, even when the traffic is encrypted.

## Resources
The research paper was accepted to SIGMETRICS 2020,
and published in ACM POMACS in December 2019.

You can download the dataset described in the paper [here](https://nm-public-data.s3.us-east-2.amazonaws.com/dataset/all_traffic_time_10.pkl)

### Citation bibtex
```
@article{bronzino2019inferring,
  title={Inferring streaming video quality from encrypted traffic: Practical models and deployment experience},
  author={Bronzino, Francesco and Schmitt, Paul and Ayoubi, Sara and Martins, Guilherme and Teixeira, Renata and Feamster, Nick},
  journal={Proceedings of the ACM on Measurement and Analysis of Computing Systems},
  volume={3},
  number={3},
  pages={1--25},
  year={2019},
  publisher={ACM New York, NY, USA}
}
```