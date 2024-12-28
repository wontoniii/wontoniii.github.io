---
layout: page
title: MobilityFirst
description: ""
img: 
importance: 1002
category: Projects
tags: [NOVN, MFTP, open source, ICN]
---

The MobilityFirst project is founded on the premise that the Internet is approaching an historic inflection point, with mobile platforms and applications poised to replace the fixed-host/server model that has dominated the Internet since its inception. This predictable, yet fundamental, shift presents a unique opportunity to design a next generation Internet in which mobile devices, and applications, and the consequent changes in service, trustworthiness, and management are primary drivers of a new architecture. The goal of MobilityFirst is to better accommodate mobile entities on the Internet in a scalable, trustworthy, and useable manner. Inherently a clean-slate project, MobilityFirst takes a radical approach to redesigning the Internet including rethinking end-point naming, such as through IP, and connection-oriented protocols, such as TCP. At a high level, MobilityFirst allows applications to securely interact with abstract, mobile entities in a connectionless fashion, providing connectivity and minimal user-disruption in the presence of mobility. 

## NOVN: A named-object based virtual network architecture to support advanced mobile edge computing services

*Abstract.* Achieving advanced Mobile Edge Computing (MEC) services such as
dynamic resource assignment and slicing, maintaining Quality of Service (QoS),
and enabling heterogeneous virtual functions are some of the technical
challenges associated with edge-cloud enhanced 5G architectures now under
consideration. This paper proposes a named-object based virtual network (NOVN)
architecture to support low-latency applications in the MEC. Software router
implementation running on the ORBIT testbed validates the named-object approach,
showing low VN processing and control overhead, and making it possible to
achieve low latency. A latency performance improvement of 30% is achieved as
compared to the baseline implementation without NOVN. The results also validate
feasibility of using the advanced MEC services for an example latency
constrained edge cloud scenario.

### Resources
The research paper was accepted to Elsevier Pervasive and Mobile Computing.

Tutorials and source code can be accessed from the orbit website: [https://www.orbit-lab.org](https://www.orbit-lab.org)

### Citation bibtex
```
@article{bronzino2020novn,
  title={NOVN: A named-object based virtual network architecture to support advanced mobile edge computing services},
  author={Bronzino, Francesco and Maheshwari, Sumit and Seskar, Ivan and Raychaudhuri, Dipankar},
  journal={Pervasive and Mobile Computing},
  volume={69},
  pages={101261},
  year={2020}
}
```

## MFTP: A Clean-Slate Transport Protocol for the Information Centric MobilityFirst Network

*Abstract.* This paper presents the design and evaluation of clean-slate
transport layer protocols for the MobilityFirst (MF) future Internet
architecture based on the concept of named objects. The MF architecture is a
specific realization of the emerging class of Information Centric Networks (ICN)
that are designed to support new modes of communication based on names of
information objects rather than their network addresses or locators. ICN
architectures including MF are characterized by the following distinctive
features: (a) use of names to identify sources and sinks of information; (b)
stor- age of information at routers within the network in order to support
content caching and disconnection; (c) multicasting and anycasting as integral
network services; and in the MF case (d) hop-by-hop reliability protocols
between routers in the network. These properties have significant implications
for transport layer protocol design since the current Internet transports (TCP
and UDP) were designed for the end-to-end Internet principle which uses address
based rout- ing with minimal functionality (i.e. no storage or reliability
mechanisms) within the network. Several use cases including web access, large
file transfer, Machine-to-machine and multicast services are considered, leading
to an identification of four basic functions needed to constitute a flexible
transport protocol for ICN: (i) fragmentation and end-to- end re-sequencing;
(ii) lightweight end-to-end error recovery with in-network transport proxies;
(iii) optional flow and congestion control mechanisms; and (iv) scalable
multicast delivery mechanisms. The design of the MobilityFirst trans- port
protocol (MFTP) framework realizing these features in a modular and flexible
manner is presented and discussed. The proposed MFTP protocol is then
experimentally evaluated and compared with TCP/IP for a few representative
scenarios including mobile data delivery, web content retrieval and
disconnected/late binding service. The results show that significant performance
gains can be achieved in each case.

### Resources
The research paper was accepted to ACM ICN 2015.

Tutorials and source code can be accessed from the orbit website: [https://www.orbit-lab.org](https://www.orbit-lab.org)

### Citation bibtex
```
@inproceedings{su2015mftp,
  title={Mftp: A clean-slate transport protocol for the information centric mobilityfirst network},
  author={Su, Kai and Bronzino, Francesco and Ramakrishnan, KK and Raychaudhuri, Dipankar},
  booktitle={Proceedings of the 2nd ACM Conference on Information-Centric Networking},
  pages={127--136},
  year={2015}
}
```

## Achieving Scalable Push Multicast Services Using Global Name Resolution

*Abstract.* This paper presents a novel approach to achieving scalable push
multicast services using the distributed global name resolution service
associated with emerging name-based network architectures. The proposed
named-object multicast (NOMA) scheme employs unique names to identify multicast
groups, while using the global name resolution service (GNRS) to store the tree
structure and maintain current mappings to mobile end-user addresses. The NOMA
scheme achieves improved scalability and performance over conventional multicast
protocols such as PIM-SM and MDSP by taking advantage of the GNRS to simplify
tree management and limit control overhead. Performance evaluation results
including comparisons with IP multicast are given using a combination of
analysis and NS-3 simulation. The results show good scalability properties along
with low control overhead for medium to large multicast groups. In addition,
NOMA seamlessly handles mobility for end-hosts subscribed to a group, avoiding
data losses upon mobility events. Results further demonstrate how separating
names from addresses enables NOMA to dynamically forward traffic to mobile
users. In conclusion, we describe a proof-of-concept prototype developed for
further experimental validation of the proposed NOMA multicast routing scheme.

### Resources
The research paper was accepted to IEEE Globecom 2016.

Tutorials and source code can be accessed from the orbit website: [https://www.orbit-lab.org](https://www.orbit-lab.org)

### Citation bibtex
```
@inproceedings{mukherjee2016achieving,
  title={Achieving scalable push multicast services using global name resolution},
  author={Mukherjee, Shreyasee and Bronzino, Francesco and Srinivasan, Suja and Chen, Jiachen and Raychaudhuri, Dipankar},
  booktitle={2016 IEEE Global Communications Conference (GLOBECOM)},
  pages={1--6},
  year={2016},
  organization={IEEE}
}
```
