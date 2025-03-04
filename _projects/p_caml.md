---
layout: page
title: Cost-Aware ML on Networks
description: ""
# img: assets/img/tr.png
importance: 994
category: Projects
# redirect: https://traffic-refinery.github.io
tags: [CATO, Traffic Refinery, open source, Sigmetrics, NSDI]
---

Network management frequently utilizes machine learning to predict network
performance and security based on traffic analysis. In such tasks, the
representation of traffic data is as critical as the choice of the machine
learning model. The features used by the model and their representations
significantly impact the model’s accuracy and determine its feasibility and
deployment practicality. Consequently, designing and evaluating these models
necessitates considering not only their accuracy but also the system costs
involved in deploying them within an operational network. Our work focuses on
developing systems-driven approaches to design and train machine learning models
that balance the trade-off between feature extraction costs and model accuracy.


## CATO: End-to-end Optimization of ML Traffic Analysis Pipelines

*Abstract.* Machine learning has shown tremendous potential for improving the
capabilities of network traffic analysis applications, often outperforming
simpler rule-based heuristics. However, ML-based solutions remain difficult to
deploy in practice. Many existing approaches only optimize the predictive
performance of their models, overlooking the practical challenges of running
them against network traffic in real time. This is especially problematic in the
domain of traffic analysis, where the efficiency of the serving pipeline is a
critical factor in determining the usability of a model. In this work, we
introduce CATO, a framework that addresses this problem by jointly optimizing
the predictive performance and the associated systems costs of the serving
pipeline. CATO leverages recent advances in multi-objective Bayesian
optimization to efficiently identify Pareto-optimal configurations, and
automatically compiles end-to-end optimized serving pipelines that can be
deployed in real networks. Our evaluations show that compared to popular feature
optimization techniques, CATO can provide up to 3600× lower inference latency
and 3.7x higher zero-loss throughput while simultaneously achieving better model
performance.

### Resources
The research paper was accepted to USENIX NSDI 2025.

### Citation bibtex
```
@article{wan2025cato,
  title={CATO: End-to-end Optimization of ML Traffic Analysis Pipelines},
  author={Wan, Gerry and Liu, Shinan and Bronzino, Francesco and Feamster, Nick and Durumeric, Zakir},
  journal={USENIX Symposium on Networked Systems Design and Implementation},
  year={2025}
}
```

## Traffic Refinery: Cost-aware Network Traffic Analysis.

Relationships between systems costs and model performance would ideally inform
machine learning pipelines during design; yet, most existing network traffic
representation decisions are made *a priori*, without concern for future use by
models. To enable this exploration, we have created `Traffic Refinery`, a system
designed to offer **flexibly extensible network data representations**, the
ability to assess the **systems-related costs** of these representations, and
the **effects of different representations on model performance**. 

### System Overview
![Traffic Refinery System Overview Diagram](/assets/img/system.png){:align="center" height="65%" width="65%"}

The figure shows an overview of the system architecture. `Traffic Refinery` is
implemented in Go to exploit performance and flexibility, as well as its
built-in benchmarking tools. The system has three components: 

1. A traffic categorization module responsible for associating network traffic
   with applications 
2. A packet capture and processing module that collects network flow statistics
   and tracks their state; moreover, this block implements a cache used to store
   flow state information
3. An aggregation and storage module that queries the flow cache to obtain
   features and statistics about each traffic flow and stores higher-level
   features concerning the applications of interest for later processing

### tl;dr: What Can You Do with Traffic Refinery?
*  Traffic (i.e., flows) are classified as "services" using either DNS domains
   or IP prefixes that the user can provide. *Note: DNS is increasingly
   encrypted, making this method less reliable. An area of ongoing research is
   privacy-preserving flow categorization.*
*  For each service, users can select from a set of existing features or create
   additional ones to collect along with their frequency.
*  The system-related costs of each feature can be profiled, enabling users to
   explore tradeoffs between ML model performance and feature costs in their
   particular environment.

### Why is Traffic Refinery Necessary?
Network management increasingly relies on machine learning to make predictions
about performance and security from network traffic. Often, the representation
of the traffic is as important as the choice of the model. The features that the
model relies on, and the representation of those features, ultimately determine
model accuracy, as well as where and whether the model can be deployed in
practice. Thus, the design and evaluation of these models ultimately requires
understanding not only model accuracy but also the systems costs associated with
deploying the model in an operational network. 

To highlight the need for `Traffic Refinery`, we show results from our [prior
work](https://dl.acm.org/doi/10.1145/3366704) by training multiple ML models to
infer the resolution of encrypted video streaming applications over time using
different data representations: 1) using only L3 features, as would be available
using `netflow`; 2) adding transport layer features; and 3) adding application
layer features to L3; and combining all features. The figure below shows the
precision and recall achieved by each representation. 

![Resolution inference features](/assets/img/resolution_features.png){:align="center" height="40%" width="40%"}

As one might expect, a model trained solely with L3 features achieves the
poorest performance. Hence, relying solely on features offered by existing
network infrastructure would produce the worst performing models. On the other
hand, combining Network and Application features results in more than a 10%
increase in both precision and recall. This example showcases how limiting
available data representations to the ones typically available from existing
systems (e.g., NetFlow) can inhibit potential gains, highlighted by the
blue-shaded area. 

Of course, any representation is possible if packet traces are the starting
point, but raw packet capture can be prohibitive in operational networks,
especially at high speeds.  The figure below shows the amount of storage
required to collect a one-hour packet capture from a live 10 Gbps link. 

![Storage profile](/assets/img/storage_profile.png){:align="center" height="40%" width="40%"}


`Traffic Refinery` provides a new framework and system that enables a joint
evaluation of both the conventional notions of machine learning performance
(e.g., model accuracy) and the systems-level costs of different representations
of network traffic. 

### Resources
The research paper behind `Traffic Refinery` was accepted to ACM SIGMETRICS 2022,
and published in ACM POMACS in December 2021.

You can access the source code of the project as well as detailed documentation at [https://traffic-refinery.github.io](https://traffic-refinery.github.io)

### Citation bibtex
```
@article{bronzino2021traffic,
  title={Traffic refinery: Cost-aware data representation for machine learning on network traffic},
  author={Bronzino, Francesco and Schmitt, Paul and Ayoubi, Sara and Kim, Hyojoon and Teixeira, Renata and Feamster, Nick},
  journal={Proceedings of the ACM on Measurement and Analysis of Computing Systems},
  volume={5},
  number={3},
  pages={1--24},
  year={2021},
  publisher={ACM New York, NY, USA}
}
```