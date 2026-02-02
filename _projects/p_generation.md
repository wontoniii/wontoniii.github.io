---
layout: page
title: Synthetic Traffic Generation
description: ""
# img: assets/img/tr.png
importance: 996
category: Projects
# redirect: https://traffic-refinery.github.io
tags: [NetSSM, NetDiffusion, CoNEXT, Sigmetrics]
---

Synthetic traces, primarily emphasizing certain flow statistics or packet
attributes, are frequently used to support ML tasks in networking. However,
their limited alignment with real traces and challenges in converting to raw
network traffic hinder both their ML performance and broader applicability in
conventional network analyses. In our research, we tap into the promising
capabilities of generative models to enhance synthetic network traffic
production. 

## NetSSM: Multi-Flow and State-Aware Network Trace Generation using State-Space Models

*Abstract.* Access to raw network traffic data is essential for many computer networking tasks, from traffic modeling
to performance evaluation. Unfortunately, this data is scarce due to high collection costs and governance
rules. Previous efforts explore this challenge by generating synthetic network data, but fail to reliably han-
dle multi-ow sessions, struggle to reason about stateful communication in moderate to long-duration net-
work sessions, and lack robust evaluations tied to real-world utility. We propose a new method based on
state-space models called NetSSM that generates raw network traffic at the packet-level granularity. Our
approach captures interactions between multiple, interleaved ows – an objective unexplored in prior work
– and effectively reasons about ow-state in sessions to capture traffic characteristics. NetSSM accomplishes
this by training with a context window more than 8× longer, and produces traces up to 78× longer than exist-
ing transformer-based raw packet generators. Evaluation results show that NetSSM generates high-fidelity
traces that outperform prior efforts in existing benchmarks. We also nd that NetSSM’s traces have high
semantic similarity to real network data regarding compliance with standard protocol requirements and ow
and session-level traffic characteristics.

### Resources
Source code and results: [https://github.com/noise-lab/netssm](https://github.com/noise-lab/netssm)

### Citation bibtex
```
@article{chu2026netssm,
  title={NetSSM: Multi-Flow and State-Aware Network Trace Generation using State-Space Models},
  author={Chu, Andrew and Jiang, Xi and Liu, Shinan and Nitin Bhagoji, Arjun  and Bronzino, Francesco and Schmitt, Paul and Feamster, Nick},
  journal={Proceedings of the ACM on Networking},
  volume={1},
  number={CoNEXT5},
  year={2026}
}
```

## NetDiffusion: Network Data Augmentation Through Protocol-Constrained Traffic Generation

*Abstract.* Datasets of labeled network traces are essential for a multitude of
machine learning (ML) tasks in networking, yet their availability is hindered by
privacy and maintenance concerns, such as data staleness. To overcome this
limitation, synthetic network traces can often augment existing datasets.
Unfortunately, current synthetic trace generation methods, which typically
produce only aggregated flow statistics or a few selected packet attributes, do
not always suffice, especially when model training relies on having features
that are only available from packet traces. This shortfall manifests in both
insufficient statistical resemblance to real traces and suboptimal performance
on ML tasks when employed for data augmentation. In this paper, we apply
diffusion models to generate high-resolution synthetic network traffic traces.
We present *NetDiffusion*, a tool that uses a finely-tuned, controlled variant
of a Stable Diffusion model to generate synthetic network traffic that is high
fidelity and conforms to protocol specifications. Our evaluation demonstrates
that packet captures generated from NetDiffusion can achieve higher statistical
similarity to real data and improved ML model performance than current
state-of-the-art approaches (e.g., GAN-based approaches). Furthermore, our
synthetic traces are compatible with common network analysis tools and support a
myriad of network tasks, suggesting that NetDiffusion can serve a broader
spectrum of network analysis and testing tasks, extending beyond ML-centric
applications.

### Resources
Source code and results: [https://github.com/noise-lab/NetDiffusion_Generator](https://github.com/noise-lab/NetDiffusion_Generator)

### Citation bibtex
```
@article{xi2024netdiffusion,
  title={NetDiffusion: Network Data Augmentation Through Protocol-Constrained Traffic Generation},
  author={Jiang, Xi and Liu, Shinan and Gember-Jacobson, Aaron and Nitin Bhagoji, Arjun  and Schmitt, Paul and Bronzino, Francesco and Feamster, Nick},
  journal={Proceedings of the ACM on Measurement and Analysis of Computing Systems},
  year={2024}
}
```