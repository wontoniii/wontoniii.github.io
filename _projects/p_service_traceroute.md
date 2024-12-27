---
layout: page
title: Service Traceroute
description: "Tracing Paths of Application Flows"
img: 
importance: 3
category: Projects
tags: [pam, open source]
---

Service Traceroute is a tool that allows the discovery of individual application flows paths. Service Traceroute leverages the ideas from paratrace, Sidecar, and 0trace, to passively listen to application traffic to then issue traceroute probes that pretend to be part of the application flow. Service Traceroute extends this idea to work for modern Internet services and support tracing of multiple concurrent TCP flows, as well as for UDP flows. Service Traceroute is available both as command-line tool and library versions. Check out our paper for more details on how Service Traceroute works.

## Resources
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