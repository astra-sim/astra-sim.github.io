---
layout: single
title:  "ASTRA-sim and Chakra: <br/>Enabling Software-Hardware Co-Design Exploration for Distributed Machine Learning Platforms"
permalink: /tutorials/micro-2024
---

## Organizer
### Synergy Lab, Georgia Institute of Technology
<img src="/assets/images/tutorials/micro-2024/GT-logo.png" alt="" width="40%"/><br/>

*Acknowledgments: Chakra and ASTRA-sim are a community effort with technical insights and code contributions from Meta, Intel, AMD, NVIDIA, HPE, Keysight, as well as several academic institutions.*

## Overview
<img src="/assets/images/astrasim_overview_codesign.png" alt="" width="100%"/>

In this tutorial, we will educate the research community about the challenges in the emerging domain of distributed machine learning, demonstrate the capabilities of Chakra Execution Trace and ASTRA-sim with examples and discuss ongoing development efforts.<br>

<span style="color:red;font-weight:bold">
NEW -- In this tutorial, we will (i) introduce details about the Chakra Execution Traces, (ii) running custom collective communications via MSCCL-IR in ASTRA-sim, (iii) and modeling LLM training/inference using ASTRA-sim.
</span>

### Date/Location
- Nov 3, 2024, 1--5 pm CST
- AT&T Hotel and Conference Center [Info](https://microarch.org/micro57/attend){: .btn .btn--info .btn--small}

## Description

As Artificial Intelligence (AI) models are scaling at an unprecedented rate, Machine Learning (ML) execution heavily relies on Distributed ML over customized neural accelerator (e.g., GPU or TPU)-based High-Performance Computing (HPC) platforms connected via high-speed interconnects (e.g., NVLinks). Examples today include NVIDIA's HGX, Google's Cloud TPU, and Meta's Research Supercluster. Distributed Deep Neural Network (DNN) execution involves a complex interplay between the DNN model architecture, parallelization strategy, scheduling strategy, collective communication algorithm, network topology, remote memory accesses, and the accelerator endpoint. As innovation in AI/ML models continues to grow at an accelerated rate, there is a need for a comprehensive methodology to understand and navigate this complex intertwined co-design space to (i) architect future platforms, (ii) develop novel parallelism schemes to support efficient training of future DNN models, and (iii) develop novel fabrics for AI systems. As an ongoing collaboration between Georgia Tech and several companies, we have been jointly developing (1) a comprehensive methodology to capture arbitrary distributed ML workloads, named Chakra Execution Trace and (ii) a detailed cycle-accurate distributed AI simulator called ASTRA-sim.

Chakra Execution Trace (Chakra ET) is a community-driven effort in MLCommons to standardize the representation of distributed ML workloads. The standardization effort via Chakra ET would harmonize the utilization of multiple upstream applications (e.g., trace profiler or trace generator) and distinct downstream tasks (e.g., simulators or replay). Chakra ET captures arbitrary distributed ML workloads by leveraging a directed acyclic graph representation of compute, communication, and remote memory nodes.

ASTRA-sim models the co-design space of distributed ML described above and schedules the compute-communication interactions over plug-and-play computation, network, and remote memory simulators. It enables a systematic study of bottleneck detection and futuristic system evaluation at the software and hardware levels for scaling distributed ML. ASTRA-sim leverages the Chakra format to describe arbitrary distributed ML workloads. It uses a Google TPU-like simulator as its computation model and provides a suite of network models (analytical network, Garnet, and ns-3) for the choice of simulation speed and fidelity.<br>

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
		Joongun Park is a Postdoctoral Researcher at Georgia Tech, focusing on hardware and system security, high-performance computing, and optimizing distributed machine learning systems. He is currently conducting applied research to develop secure and efficient design strategies for large-scale systems, with practical experience in both real-world and simulated environments. Joongun has collaborated with Intel on developing next-generation supercomputer architectures for an IARPA project. He holds a Ph.D. (2023), M.S. (2018), and B.S. (2016) in Computer Science from KAIST.
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
    <td><img src="/assets/images/tutorials/micro-2024/vinay_ramakrishnaiah.jpg" alt="Vinay Ramakrishnaiah"/></td>
    <td>
        <b>Vinay Ramakrishnaiah </b> (AMD) <br><a href="mailto:Vinay.Ramakrishnaiah@amd.com" class="btn btn--info"><i class="fa fa-envelope"></i> Email</a> <a href="https://www.linkedin.com/in/vinay-ramakrishnaiah-7425323b/" class="btn btn--info"><i class="fab fa-linkedin"></i> LinkedIn</a><br>
        Vinay Ramakrishnaiah is a Senior Member of Technical Staff at AMD working in the area of hardware-software codesign. His research interests include Artificial Intelligence (AI) at scale, scale-out networks, GPU schedulers, and developing and evaluating applications for emerging hardware architectures. Prior to joining AMD, Vinay was a staff scientist and principal investigator at the Los Alamos National Laboratory where he worked on multiple exascale computing projects, signal processing optimizations for satellites, and led the co-design summer school. Vinay obtained his Ph.D. in Electrical and Computer Engineering from the University of Wyoming with a research focus in applications of high-performance computing to antenna signal processing.
        <br>
    </td>
</tr>
</table>

## Schedule

| Time (CST) | Agenda | Presenter | Resources |
|:---:|:---|---|:---:|
| | **[ Introduction ]** | | |
| **1:00 pm** | Introduction to Distributed ML | Tushar (GT) | [Slide](/assets/tutorials/micro-2024/1_intro_to_distributed_ml.pdf){: .btn .btn--success .btn--small} [Video](https://youtu.be/Fd5vm-ImyuI?si=kMOO_mYNaCKll1IW){: .btn .btn--danger} |
| **1:30 pm** | Overview: ASTRA-sim and Chakra | Tushar (GT) | [Slide](/assets/tutorials/micro-2024/2_chakra_astrasim_overview.pdf){: .btn .btn--success .btn--small} [Video](https://youtu.be/wN8b-nq-5T0?si=lcTc4nIaWFbUtkYI){: .btn .btn--danger} |
| | | | |
| | **[ Chakra ]** | | | 
| **1:40 pm** | **Chakra Execution Trace** | Taekyung (NVIDIA) | [Slide](/assets/tutorials/micro-2024/3_chakra.pdf){: .btn .btn--success .btn--small} [Video](https://youtu.be/wDdRi4rUtqU?si=Y2dcO7ejFiHL3Wqi){: .btn .btn--danger} |
| | | | |
| | **[ ASTRA-sim ]** | | | 
| **2:00 pm** | Workload Layer | Taekyung (NVIDIA) | [Slide](/assets/tutorials/micro-2024/4_workload_layer.pdf){: .btn .btn--success .btn--small} [Video](https://youtu.be/XFNW8myIW_s?si=6aHUSkadBgf10wNe){: .btn .btn--danger} |
| **2:20 pm** | System Layer | Will (GT/AMD) | [Slide](/assets/tutorials/micro-2024/5_system_layer.pdf){: .btn .btn--success .btn--small} [Video](https://youtu.be/rASNeRewu4M?si=Ug140AwGdBwAjt5M){: .btn .btn--danger} |
| **2:40 pm** | Network Layer | Will (GT/AMD) | [Slide](/assets/tutorials/micro-2024/6_network_layer.pdf){: .btn .btn--success .btn--small} [Video](https://youtu.be/5l9o7ax0_c4?si=TUfOaHF0iquX13GW){: .btn .btn--danger} |
| | | | |
| **3:00 pm** | **[ Coffee Break ]** | | |
| | | | |
| | **[ Demo ]** | | |
| **3:30 pm** | Chakra + ASTRA-sim Demo | Joongun (GT) | [Slide](/assets/tutorials/micro-2024/7_demo.pdf){: .btn .btn--success .btn--small} [Video](https://youtu.be/F-xEPeN4Zgw?si=hWJEU3oRHOMW06yn){: .btn .btn--danger} |
| **3:50 pm** | (Supplementary) NS-3 Demo | Jinsun (GT) | [Slide](/assets/tutorials/micro-2024/7_demo_suppl_ns3.pdf){: .btn .btn--success .btn--small} [Video](https://youtu.be/YhYKMHJo7ns?si=U16jOLBOTym0jhCj){: .btn .btn--danger} |
| | | | |
| | **[ ASTRA-sim Updates ]** | | |
| **4:10 pm** | ASTRA-sim New Features | Vinay (AMD), Will (GT/AMD) | [Slide](/assets/tutorials/micro-2024/8_astrasim_new_features.pdf){: .btn .btn--success .btn--small} [Video](https://youtu.be/Db-1Aho4AlY?si=rc_A2j2a9kbNHsYt){: .btn .btn--danger} |
| **4:40 pm** | ASTRA-sim Wiki and Validation | Will (GT/AMD) | [Slide](/assets/tutorials/micro-2024/9_wiki_and_validation.pdf){: .btn .btn--success .btn--small} [Video](https://youtu.be/AIBCyMfnv_0?si=5ajWF3zIHfziSMdc){: .btn .btn--danger} |
| | | | |
| | **[ Closing ]** | | |
| **4:50 pm** | Closing Remarks | Tushar (GT) | [Slide](/assets/tutorials/micro-2024/10_conclusion.pdf){: .btn .btn--success .btn--small} [Video](https://youtu.be/xLAfxf9pTW4?si=gy44mdfqR8SZHsEY){: .btn .btn--danger} |

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

### CollectiveAPI Paper
Jinsun Yoo, William Won, Meghan Cowan, Nan Jiang, Benjamin Klenk, Srinivas Sridharan†, and Tushar Krishna,
"**Towards a Standardized Representation for Deep Learning Collective Algorithms,**"
In *Proc. of the 2024 IEEE Symposium on High-Performance Interconnects (HOTI '24)*, 2024.
{: .notice--info}
[paper](https://ieeexplore.ieee.org/document/10664245){: .btn .btn--success}

### Repositories
[ASTRA-sim](https://github.com/astra-sim/astra-sim){: .btn .btn--info}
[Chakra](https://github.com/mlcommons/chakra){: .btn .btn--info}
[Analytical Network](https://github.com/astra-sim/analytical){: .btn .btn--info}

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=http%3A%2F%2Fastra-sim.github.io%2Ftutorials%2Fmicro-2024&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
