---
layout: page
title: Traceroute of Application Flows
description: ""
img: 
importance: 1001
category: Projects
tags: [Service traceroute, open source]
---

Service traceroute is a tool that allows the discovery of individual application
flows paths. Service traceroute leverages the ideas from paratrace, Sidecar, and
0trace, to passively listen to application traffic to then issue traceroute
probes that pretend to be part of the application flow. Service traceroute
extends this idea to work for modern Internet services and support tracing of
multiple concurrent TCP flows, as well as for UDP flows. Service traceroute is
available both as command-line tool and library versions. 

## Service traceroute: Tracing Paths of Application Flows

*Abstract.* Traceroute is often used to help diagnose when users experience
issues with Internet applications or services. Unfortunately, probes issued by
classic traceroute tools differ from application traffic and hence can be
treated differently by routers that perform load balancing and middleboxes
within the network. This paper proposes a new traceroute tool, called Service
traceroute. Service traceroute leverages the idea from paratrace, which
passively listens to application traffic to then issue traceroute probes that
pretend to be part of the application flow. We extend this idea to work for
modern Internet services with support for identifying the flows to probe
automatically, for tracing of multiple concurrent flows, and for UDP flows. We
implement command-line and library versions of Service traceroute, which we
release as open source. This paper also presents an evaluation of Service
traceroute when tracing paths traversed by Web downloads from the top-1000 Alexa
websites and by video sessions from Twitch and Youtube. Our evaluation shows
that Service traceroute has no negative effect on application flows. Our
comparison with Paris traceroute shows that a typical traceroute tool that
launches a new flow to the same destination discovers different paths than when
embedding probes in the application flow in a significant fraction of
experiments (from 40% to 50% of our experiments in PlanetLab Europe).

### Resources
The research paper was accepted to PAM 2019.

You can download the source and datasets [here](https://github.com/inria-muse/service-traceroute)

### Citation bibtex
```
@inproceedings{morandi2019service,
  title={Service traceroute: tracing paths of application flows},
  author={Morandi, Ivan and Bronzino, Francesco and Teixeira, Renata and Sundaresan, Srikanth},
  booktitle={Passive and Active Measurement: 20th International Conference, PAM 2019, Puerto Varas, Chile, March 27--29, 2019, Proceedings 20},
  pages={116--128},
  year={2019},
  organization={Springer}
}
```