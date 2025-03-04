---
layout: page
title: Synthetic Traffic Generation
description: ""
# img: assets/img/tr.png
importance: 996
category: Projects
# redirect: https://traffic-refinery.github.io
tags: [NetDiffusion, open source, Sigmetrics]
---

Synthetic traces, primarily emphasizing certain flow statistics or packet
attributes, are frequently used to support ML tasks in networking. However,
their limited alignment with real traces and challenges in converting to raw
network traffic hinder both their ML performance and broader applicability in
conventional network analyses. In our research, we tap into the promising
capabilities of generative models to enhance synthetic network traffic
production. 

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