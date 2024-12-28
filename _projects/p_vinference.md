---
layout: page
title: Application Quality Inference
description: ""
img: 
importance: 999
category: Projects
tags: [Inference, dataset, Sigmetrics]
---


We develop systems and models to accurately infer application quality metrics in real time from encrypted traffic by using just a handful of features extracted from passive traffic measurement. 

## Inferring Streaming Video Quality from Encrypted Traffic: Practical Models and Deployment Experience

*Abstract.* Inferring the quality of streaming video applications is important
for Internet service providers, but the fact that most video streams are
encrypted makes it difficult to do so. We develop models that infer quality
metrics (i.e., startup delay and resolution) for encrypted streaming video
services. Our paper builds on previous work, but extends it in several ways.
First, the models work in deployment settings where the video sessions and
segments must be identified from a mix of traffic and the time precision of the
collected traffic statistics is more coarse (e.g., due to aggregation). Second,
we develop a single composite model that works for a range of different services
(i.e., Netflix, YouTube, Amazon, and Twitch), as opposed to just a single
service. Third, unlike many previous models, our models perform predictions at
finer granularity (e.g., the precise startup delay instead of just detecting
short versus long delays) allowing to draw better conclusions on the ongoing
streaming quality. Fourth, we demonstrate the models are practical through a
16-month deployment in 66 homes and provide new insights about the relationships
between Internet “speed” and the quality of the corresponding video streams, for
a variety of services; we find that higher speeds provide only minimal
improvements to startup delay and resolution.

### Resources
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