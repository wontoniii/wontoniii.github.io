---
layout: page
title: Network Performance Characterization
description: ""
# img: assets/img/tr.png
importance: 995
category: Projects
# redirect: https://traffic-refinery.github.io
tags: [Data interpolation, MPR architectures, open source, Sigmetrics, PAM]
---

A reliable Internet connection is no longer a luxury but a fundamental
requirement for modern life, enabling remote work, online learning, and
entertainment. However, Internet performance is far from uniform, varying widely
depending on geographic location and the type of connection used. These
disparities can create significant inequities in access to online resources and
opportunities. To address this, it is crucial to understand Internet performance
at a granular, local level, uncovering patterns and identifying areas where
connectivity falls short. Our research focuses on characterizing network
performance across both spatial and temporal dimensions, providing the insights
needed to build a more resilient and equitable Internet infrastructure.


## Beyond Data Points: Regionalizing Crowdsourced Latency Measurements

*Abstract.* Despite significant investments in access network infrastructure,
universal access to high-quality Internet connectivity remains a challenge.
Policymakers often rely on large-scale, crowdsourced measurement datasets to
assess the distribution of access network performance across geographic areas.
These decisions typically rest on the assumption that Internet performance is
uniformly distributed within predefined social boundaries, such as zip codes,
census tracts, or neighborhood units. However, this assumption may not be valid
for two reasons: (1) crowdsourced measurements often exhibit non-uniform
sampling densities within geographic areas; and (2) predefined social boundaries
may not align with the actual boundaries of Internet infrastructure. In this
paper, we present a spatial analysis on crowdsourced datasets for constructing
stable boundaries for sampling Internet performance. We hypothesize that greater
stability in sampling boundaries will reflect the true nature of Internet
performance disparities than misleading patterns observed as a result of data
sampling variations. We apply and evaluate a series of statistical techniques
to: (1) aggregate Internet performance over geographic regions; (2) overlay
interpolated maps with various sampling unit choices; and (3) spatially cluster
boundary units to identify contiguous areas with similar performance
characteristics. We assess the effectiveness of the techniques we apply by
comparing the similarity of the resulting boundaries for monthly samples drawn
from the dataset. Our evaluation shows that the combination of techniques we
apply achieves higher similarity compared to directly calculating central
measures of network metrics over census tracts or neighborhood boundaries. These
findings underscore the important role of spatial modeling in accurately
assessing and optimizing the distribution of Internet performance, which can
better inform policy, network operations, and long-term planning decisions.

### Resources
The research paper behind this paper  was accepted to ACM SIGMETRICS 2025,
and published in ACM POMACS in December 2024.

### Citation bibtex
```
@article{sharma2024beyond,
  title={Beyond Data Points: Regionalizing Crowdsourced Latency Measurements},
  author={Sharma, Taveesh and Schmitt, Paul and Bronzino, Francesco and Feamster, Nick and Marwell, Nicole P},
  journal={Proceedings of the ACM on Measurement and Analysis of Computing Systems},
  volume={8},
  number={3},
  pages={1--24},
  year={2024},
  publisher={ACM New York, NY, USA}
}
```

## Measuring the Performance of iCloud Private Relay

*Abstract.* Recent developments in Internet protocols and services aim
to provide enhanced security and privacy for users’ traffic. Apple’s iCloud
Private Relay is a premier example of this trend, introducing a well-
provisioned, multi-hop architecture to protect the privacy of users’ traf-
fic while minimizing the traditional drawbacks of additional network
hops (e.g., latency). Announced in 2021, the service is currently in the
beta stage, offering an easy and cheap privacy-enhancing alternative di-
rectly integrated into Apple’s operating systems. This seamless integra-
tion makes a future massive adoption of the technology very likely, calling
for studies on its impact on the Internet. Indeed, the iCloud Private Relay
architecture inherently introduces computational and routing overheads,
possibly hampering performance. In this work, we study the service from
a performance perspective, across a variety of scenarios and locations.
We show that iCloud Private Relay not only reduces speed test perfor-
mance (up to 10x decrease) but also negatively affects page load time and
download/upload throughput in different scenarios. Interestingly, we find
that the overlay routing introduced by the service may increase perfor-
mance in some cases. Our results call for further investigations into the
effects of a large-scale deployment of similar multi-hop privacy-enhancing
architectures. For increasing the impact of our work we contribute our
software and measurements to the community.

### Resources
The research paper behind this paper was accepted to PAM 2023.

You can access the source code of the project as well as the collected datasets at [https://github.com/marty90/icloud-private-relay-experiments](https://github.com/marty90/icloud-private-relay-experiments)

### Citation bibtex
```
@inproceedings{trevisan2023measuring,
  title={Measuring the performance of icloud private relay},
  author={Trevisan, Martino and Drago, Idilio and Schmitt, Paul and Bronzino, Francesco},
  booktitle={International Conference on Passive and Active Network Measurement},
  pages={3--17},
  year={2023},
  organization={Springer}
}
```

## Characterizing Service Provider Response to the COVID-19 Pandemic in the United States

*Abstract.* The COVID-19 pandemic has resulted in dramatic changes to the
daily habits of billions of people. Users increasingly have to rely
on home broadband Internet access for work, education, and other
activities. These changes have resulted in corresponding changes to
Internet traffic patterns. This paper aims to characterize the effects of
these changes with respect to Internet service providers in the United
States. We study three questions: (1) How did traffic demands change
in the United States as a result of the COVID-19 pandemic?; (2) What
effects have these changes had on Internet performance?; (3) How
did service providers respond to these changes? We study these ques-
tions using data from a diverse collection of sources. Our analysis of
interconnection data for two large ISPs in the United States shows a
30–60% increase in peak traffic rates in the first quarter of 2020. In
particular, we observe traffic downstream peak volumes for a major
ISP increase of 13–20% while upstream peaks increased by more
than 30%. Further, we observe significant variation in performance
across ISPs in conjunction with the traffic volume shifts, with evident
latency increases after stay-at-home orders were issued, followed
by a stabilization of traffic after April. Finally, we observe that in
response to changes in usage, ISPs have aggressively augmented
capacity at interconnects, at more than twice the rate of normal
capacity augmentation. Similarly, video conferencing applications
have increased their network footprint, more than doubling their
advertised IP address space.

### Resources
The research paper behind this paper was accepted to PAM 2021.

### Citation bibtex
```
@inproceedings{liu2021characterizing,
  title={Characterizing service provider response to the covid-19 pandemic in the united states},
  author={Liu, Shinan and Schmitt, Paul and Bronzino, Francesco and Feamster, Nick},
  booktitle={Passive and Active Measurement: 22nd International Conference, PAM 2021, Virtual Event, March 29--April 1, 2021, Proceedings 22},
  pages={20--38},
  year={2021},
  organization={Springer}
}
```