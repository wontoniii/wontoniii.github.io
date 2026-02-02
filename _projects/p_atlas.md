---
layout: page
title: Robotic Swarm Cooperation
description: ""
img: 
importance: 1001
category: Projects
tags: [ATLAS]
---

Industry 4.0 environments are characterized by the coexistence of a diverse set
of devices, including sensors, mixed-reality displays, robots, drones, and smart
objects. These systems must be capable of autonomously taking critical in-time
decisions necessary to perform complex tasks without human input. One essential
application for Industry 4.0 is multi-robot exploration and mapping of unknown
environments, especially in critical missions such as hazard detection and
search and rescue. These missions share the need to reach full coverage of the
explorable space in the shortest time possible. To minimize completion time,
robots in the fleet must be able to exchange information about the environment
reliably with one another. However, existing exploration and mapping algorithms
suffer from inaccuracies and inefficiencies due to their lack of contextual
awareness of their surroundings, especially in terms of communications, lacking
flexibility and adaptability to the environment, and hence, adding unnecessary
delay to the mission at hand. Our work investigates the impact of communication
awareness on the performance of multi-robot exploration and mapping expeditions,
in terms of time to completion. 

## CARA: Connectivity-Aware Relay Algorithm for Multi-Robot Expeditions

*Abstract.* The exploration of unknown environments is an essential application of multi-robot
systems, particularly in critical missions, such as hazard detection and search and rescue. These
missions share the need to reach full coverage of the explorable space in the shortest time possible.
To minimize the completion time, robots in the fleet must be able to reliably exchange information
about the environment with one another. One of the main methods to expand coverage is by
placing relays. Existing relay-placement algorithms tend to either require prior knowledge of the
environment, or they rely on maintaining specific distances between the relays and the rest of the
robots. These approaches lack flexibility and adaptability to the environment. This paper introduces
the “Connectivity-Aware Relay Algorithm” (CARA), a dynamic context-aware relay-placement
algorithm that does not require any prior knowledge of the environment. We compare CARA against
a state-of-the-art distance-based relay-placement algorithm. Our results demonstrate that CARA
outperformed the state-of-the-art algorithm in terms of the time to completion by a factor of 10 as it
placed, on average, half the number of relays.

## Resources
You can download the source and datasets [here](https://github.com/openwsn-berkeley/Atlas)

For a broader view on this work, checkout Razanne's [PhD thesis](https://hal.science/tel-04017864/file/ABU_AISHEH_Razane_these_2023.pdf).

### Citation bibtex
```
@article{abu2022cara,
  title={CARA: Connectivity-Aware Relay Algorithm for Multi-Robot Expeditions},
  author={Abu-Aisheh, Razanne and Bronzino, Francesco and Sala{\"u}n, Lou and Watteyne, Thomas},
  journal={MDPI Sensors},
  year={2022}
  }
```