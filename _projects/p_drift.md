---
layout: page
title: Concept Drift in Networks
description: ""
# img: assets/img/tr.png
importance: 998
category: Projects
# redirect: https://traffic-refinery.github.io
tags: [LEAF, CoNEXT]
---

An important step in deploying machine learning models for networking tasks in
practice is dealing with concept drift. Although this phenomenon has been
explored in other contexts, it has received limited attention in the networking
domain. To address it, our work characterizes drift patterns across multiple
models and KPIs and develops solutions to detect, explain, and mitigate drift
for black-box models applied to cellular demand forecasting.

## LEAF: Navigating Concept Drift in Cellular Networks

*Abstract.* Operational networks commonly rely on machine learning models for
many tasks, including detecting anomalies, inferring application performance,
and forecasting demand. Yet, model accuracy can degrade due to concept drift,
where either the relationships between features and the target to be predicted,
or the features themselves change. Mitigating concept drift is an essential part
of operationalizing machine learning models in general, but is of particular
importance in networking’s highly dynamic deployment environments. In this
paper, we first characterize concept drift in a large cellular network for a
major metropolitan area in the United States. We find that concept drift occurs
across many important key performance indicators (KPIs), independently of the
model, training set size, and time interval—thus necessitating practical
approaches to detect, explain, and mitigate it. We then show that frequent model
retraining with newly available data is not sufficient to mitigate concept
drift, and can even degrade model accuracy further. Finally, we develop a new
methodology for concept drift mitigation, Local Error Approximation of Features
(LEAF). LEAF works by detecting drift; explaining the features and time
intervals that contribute the most to drift; and mitigating it using forgetting
and over-sampling. We evaluate LEAF against industry-standard mitigation
approaches (notably, periodic retraining) with more than four years of cellular
KPI data. Our tests with a major cellular provider in the US show that LEAF
consistently outperforms periodic and triggered re-training on complex,
real-world data while reducing costly retraining operations.

### Resources
Access the released dataset accompanying the paper at this page: [LEAF Dataset](https://docs.google.com/forms/d/e/1FAIpQLSe5wpn70MLkw5TsZYb7ONxDU4chj0Isksbr5GFpp-y77OJ50A/viewform)

### Citation bibtex
```
@article{liu2023leaf,
  title={LEAF: Navigating Concept Drift in Cellular Networks},
  author={Liu, Shinan and Bronzino, Francesco and Schmitt, Paul and Nitin Bhagoji, Arjun and Feamster, Nick and Crespo, Hector Garcia and Coyle, Timothy and Ward, Brian},
  journal={Proceedings of the ACM on Networking},
  year={2023}
}
```