---
layout: single
title:  "ASTRA-sim and Chakra Tutorial @ MICRO 2024"
permalink: /tutorials/micro-2024
---

## Organizers
<img src="/assets/images/tutorials/micro-2024/GT-logo.png" alt="" width="30%"/><br/>
<img src="/assets/images/tutorials/micro-2024/AMD-logo.png" alt="" width="30%"/><br/>
<img src="/assets/images/tutorials/micro-2024/NVIDIA-logo.png" alt="" width="30%"/>

## Overview
<img src="/assets/images/astrasim_overview_codesign.png" alt="" width="100%"/>

In this tutorial, we will educate the research community about the challenges in the emerging domain of distributed machine learning, demonstrate the capabilities of Chakra Execution Trace and ASTRA-sim with examples and discuss ongoing development efforts.<br>


### Date/Location
- Nov 3, 2024, 1--5 pm CST
- AT&T Hotel and Conference Center [Info](https://microarch.org/micro57/attend){: .btn .btn--info .btn--small}

## Description
As Artificial Intelligence (AI) models are scaling at an unprecedented rate, Machine Learning (ML) execution heavily relies on Distributed ML over customized neural accelerator (e.g., GPU or TPU)-based High-Performance Computing (HPC) platforms connected via high-speed interconnects (e.g., NVLinks). Examples today include NVIDIA's HGX, Google's Cloud TPU, and Meta's Research Supercluster. Distributed Deep Neural Network (DNN) execution involves a complex interplay between the DNN model architecture, parallelization strategy, scheduling strategy, collective communication algorithm, network topology, remote memory accesses, and the accelerator endpoint.

Collective communications (e.g., All-Reduce, Reduce-Scatter, All-Gather, All-to-All) are initiated at different phases for different parallelism approaches and play a crucial role in overall runtime if not hidden efficiently behind computation. This problem becomes paramount as recent Large Language Models (LLMs), such as GPT-3, and Recommendation models, such as DLRM, have billions to trillions of parameters and need to be scaled across tens of thousands of accelerator nodes. As innovation in AI/ML models continues to grow at an accelerated rate, there is a need for a comprehensive methodology to understand and navigate this complex intertwined co-design space to (i) architect future platforms, (ii) develop novel parallelism schemes to support efficient training of future DNN models, and (iii) develop novel fabrics for AI systems.

As an ongoing collaboration between Georgia Tech and several companies (Intel, Meta, AMD, NVIDIA, and HPE), we have been jointly developing a detailed cycle-accurate distributed AI simulator called ASTRA-sim. ASTRA-sim models the co- design space of distributed ML described above and schedules the compute-communication interactions over plug-and-play computation, network, and remote memory simulators. It enables a systematic study of bottleneck detection and futuristic system evaluation at the software and hardware levels for scaling distributed ML. ASTRA-sim leverages the MLCommons Chakra format to describe arbitrary distributed ML workloads. It uses a Google TPU-like simulator as its computation model and provides a suite of network models (analytical network, Garnet, and ns-3) for the choice of simulation speed and fidelity.<br>

<span style="color:red;font-weight:bold">
NEW -- In this tutorial, we will (i) introduce details about the Chakra Execution Traces, (ii) running custom collective communications via MSCCL-IR in ASTRA-sim, (iii) and modeling LLM training/inference using ASTRA-sim.
</span>

*Acknowledgments: Chakra and ASTRA-sim are a community effort with technical insights and code contributions from Meta, Intel, AMD, NVIDIA, HPE, Keysight, as well as several academic institutions.*

### Target Audience
Any researcher with the interest in full-stack, large-scale AI/ML simulation.

## Organizers
<table style="width:100%">
<colgroup>
    <col span="1" style="width:20%">
    <col span="1" style="width:80%">
</colgroup>
<tr>
    <td><img src="/assets/images/tutorials/micro-2024/tushar_krishna.jpg" alt="Tushar Krishna"/></td>
    <td>
        <b>Tushar Krishna</b> (Georgia Tech) <br><a href="mailto:tushar@ece.gatech.edu" class="btn btn--info"><i class="fa fa-envelope"></i> Email</a> <a href="https://tusharkrishna.ece.gatech.edu" class="btn btn--info"><i class="fas fa-address-card"></i> Website</a> <a href="https://www.linkedin.com/in/tushar-krishna-a60b0970/" class="btn btn--info"><i class="fab fa-linkedin"></i> LinkedIn</a><br>
        Tushar Krishna is an Associate Professor in the School of Electrical and Computer Engineering at Georgia Tech. He is currently also a Visiting Associate Professor at the Department of Electrical Engineering and Computer Science at MIT. He has a Ph.D. in Electrical Engineering and Computer Science from MIT (2014), a M.S.E in Electrical Engineering from Princeton University (2009), and a B.Tech in Electrical Engineering from the Indian Institute of Technology (IIT) Delhi (2007). Before joining Georgia Tech in 2015, Dr. Krishna spent a year as a researcher at the VSSAD group at Intel, Massachusetts. Dr. Krishna's research spans computer architecture, interconnection networks, networks-on- chip (NoC), and AI/ML accelerator systems, with a focus on optimizing data movement in modern computing platforms. His research is funded via multiple awards from NSF, DARPA, IARPA, SRC (including JUMP2.0), Department of Energy, Intel, Google, Meta/Facebook, Qualcomm and TSMC.
        <br>
    </td>
</tr>
<tr>
    <td><img src="/assets/images/tutorials/micro-2024/will_won.jpg" alt="Will Won"/></td>
    <td>
        <b>William Won (Will) </b> (Georgia Tech) <br><a href="mailto:william.won@gatech.edu" class="btn btn--info"><i class="fa fa-envelope"></i> Email</a> <a href="https://www.willjwon.com" class="btn btn--info"><i class="fas fa-address-card"></i> Website</a> <a href="https://www.linkedin.com/in/willjwon" class="btn btn--info"><i class="fab fa-linkedin"></i> LinkedIn</a><br>
        William Won is a Ph.D. student in the College of Computing at Georgia Tech. He received M.S. in Computer Science at Georgia Tech in 2022, and B.S. in Computer Science and Enginnering at Seoul National University in 2019. His research interests include training and inference of distributed machine learning, simulation of distributed machine learning workloads, collective communication optimizations, and machine learning algorithms.
        <br>
    </td>
</tr>
<tr>
    <td><img src="/assets/images/tutorials/micro-2024/joongun_park.jpg" alt="Joongun Park"/></td>
    <td>
        <b>Joongun Park </b> (Georgia Tech) <br> <br><a href="mailto:jpark3234@gatech.edu" class="btn btn--info"><i class="fa fa-envelope"></i> Email</a> <a href="https://sites.google.com/casys.kaist.ac.kr/jupark/" class="btn btn--info"><i class="fas fa-address-card"></i> Website</a> <a href="https://www.linkedin.com/in/joongun-park-8a7364b3/" class="btn btn--info"><i class="fab fa-linkedin"></i> LinkedIn</a><br>
        Joongun Park is a postdoctoral researcher at Georgia Tech. He earned his Ph.D. in Computer Science from KAIST in 2023, focusing on hardware security and Trusted Execution Environments. He collaborated with Intel on next-generation supercomputer architecture for IARPA project. His research interests include securing and optimizing HW/SW for distributed machine learning.
        <br>
    </td>
</tr>
<tr>
    <td><img src="/assets/images/tutorials/micro-2024/taekyung_heo.jpg" alt="Taekyung Heo"/></td>
    <td>
        <b>Taekyung Heo </b> (NVIDIA) <br> <a href="https://sites.google.com/view/taekyungheo/" class="btn btn--info"><i class="fas fa-address-card"></i> Website</a> <a href="https://www.linkedin.com/in/taekyungheo/" class="btn btn--info"><i class="fab fa-linkedin"></i> LinkedIn</a><br>
        Taekyung Heo is a Senior HPC Middleware Developer at NVIDIA, where he specializes in distributed machine learning systems, performance modeling, and memory systems. His work emphasizes bridging the gap between theory and practical implementation through hardware-software co-design, focusing on scaling AI workloads across thousands of GPUs. He is one of the main developers of Chakra. Taekyung holds a Ph.D. in Computer Science from KAIST (2022), an M.Sc. in Computer Science from KAIST (2016), and a B.Sc. in Computer Engineering from Sungkyunkwan University (2014).
        <br>
    </td>
</tr>
<tr>
    <td></td>
    <td>
        <b>Vinay Ramakrishnaiah </b> (AMD) <br><a href="mailto:Vinay.Ramakrishnaiah@amd.com" class="btn btn--info"><i class="fa fa-envelope"></i> Email</a> <a href="https://www.linkedin.com/in/vinay-ramakrishnaiah-7425323b/" class="btn btn--info"><i class="fab fa-linkedin"></i> LinkedIn</a><br>
        <br>
    </td>
</tr>
</table>

## Schedule

| Time (CST) | Agenda | Presenter | Resources |
|:---:|:---|---|:---:|
| **1:00 pm** | **Introduction to Distributed ML** | Tushar (GT) | |
| **1:30 pm** | **Overview: ASTRA-sim and Chakra** | Tushar (GT) | |
| **1:40 pm** | **Chakra Execution Trace** | Taekyung (NVIDIA) | |
| | **[ASTRA-sim Deeper Dive]** | | |
| **2:00 pm** | Workload Layer | Taekyung (NVIDIA) | |
| **2:20 pm** | System Layer | Will (GT/AMD) | |
| **2:40 pm** | Network Layer | Will (GT/AMD) | |
| **3:00 pm** | **Coffee Break** | | |
| **3:30 pm** | **ASTRA-sim Wiki and Validation** | Will (GT/AMD) | |
| **3:40 pm** | **ASTRA-sim New Features** | AMD | |
| | **[Demo]** | | |
| **4:20 pm** | Chakra Demo | Joongun (GT) | |
| **4:35 pm** | ASTRA-sim Demo | Joongun (GT) | |
| **4:50 pm** | **Closing Remarks** | Tushar (GT) | |

## Additional Resources

### MLCommons Chakra Working Group
[Website](https://mlcommons.org/working-groups/research/chakra/){: .btn .btn--info}

### ASTRA-sim2.0 Paper
William Won, Taekyung Heo, Saeed Rashidi, Srinivas Sridharan, Sudarshan Srinivasan, and Tushar Krishna,
"**ASTRA-sim2.0: Modeling Hierarchical Networks and Disaggregated Systems for Large-model Training at Scale,**"
In *Proc. of the IEEE International Symposium on Performance Analysis of Systems and Software (ISPASS '23)*, 2023.
{: .notice--info}
[paper](https://arxiv.org/abs/2303.14006){: .btn .btn--success}

### Chakra Paper
Srinivas Sridharan, Taekyung Heo, Louis Feng, Zhaodong Wang, Matt Bergeron, Wenyin Fu, Shengbao Zheng, Brian Coutinho, Saeed Rashidi, Changhai Man, and Tushar Krishna, 
"**Chakra: Advancing Performance Benchmarking and Co-design using Standardized Execution Traces,**"
In *arXiv:2305.14516 [cs.LG]*, 2023.
{: .notice--info}
[paper](https://arxiv.org/abs/2305.14516){: .btn .btn--success}

### MSCCL-IR Paper
Meghan Cowan, Saeed Maleki, Madanlal Musuvathi, Olli Saarikivi, and Yifan Xiong, 
"**MSCCLang: Microsoft Collective Communication Language,**"
In *Proc. of the 28th ACM International Conference on Architectural Support for Programming Languages and Operating Systems (ASPLOS '23)*, 2023.
{: .notice--info}
[paper](https://dl.acm.org/doi/10.1145/3575693.3575724){: .btn .btn--success}

### Repositories
[ASTRA-sim](https://github.com/astra-sim/astra-sim){: .btn .btn--info}
[Chakra](https://github.com/mlcommons/chakra){: .btn .btn--info}
[Analytical Network](https://github.com/astra-sim/analytical){: .btn .btn--info}

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=http%3A%2F%2Fastra-sim.github.io%2Ftutorials%2Fmicro-2024&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
