---
title: "ASTRA-sim"
layout: splash
permalink: /
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/banner.jpg
  actions:
    - label: "Get Started"
      url: "/astra-sim-docs/index.html"
    - label: "Tutorials"
      url: "/tutorials"
excerpt: "An Open-source Distributed Deep Learning Training Simulator Infrastructure"
intro:
mlsys_2022_tutorial:
  - image_path: /assets/images/tutorials/asplos-2023/banner-vancouver.jpg
    title: "ASTRA-sim Tutorial @ ASPLOS 2023"
    excerpt: "We successfully delivered the ASTRA-sim tutorial at ASPLOS 2023.<br>Mar 26, 2023<br>Vancouver, Canada."
    url: "/tutorials/asplos-2023"
    btn_label: "Read More"
    btn_class: "btn--primary"
toc: false
---
{% include feature_row id="mlsys_2022_tutorial" type="left" %}



# Tutorials
### 2023
- [ASPLOS 2023](/tutorials/asplos-2023){: .btn .btn--inverse}

### 2022
- [MLSys 2022](/tutorials/mlsys-2022){: .btn .btn--inverse}
- [ISCA 2022](/tutorials/isca-2022){: .btn .btn--inverse}
- [ASPLOS 2022](/tutorials/asplos-2022){: .btn .btn--inverse}

<br><br>

# Overview
This is the ASTRA-sim distributed Deep Learning Training simulator, developed in collaboration between Georgia Tech, Meta and Intel.

An overview is presented here:<br>
<img src="/assets/images/astrasim_overview_codesign.png" alt="" width="80%"/>

The full description of the tool and its strength can be found in these papers.


### ASTRA-sim2.0 (ISPASS 2023)
[paper](https://arxiv.org/abs/2303.14006){: .btn .btn--success}
[slides](/assets/papers/astra-sim2/ASTRA-sim2-ISPASS_2023.pdf){: .btn .btn--success}
[video](https://youtu.be/QGilXx_GEXs?si=3bASNTAtyTsk_Gi8){: .btn .btn--danger}

William Won\*, Taekyung Heo\*, Saeed Rashidi\*, Srinivas Sridharan, Sudarshan Srinivasan, and Tushar Krishna,
"ASTRA-sim2.0: Modeling Hierarchical Networks and Disaggregated Systems for Large-model Training at Scale,"
In *Proc. of the IEEE International Symposium on Performance Analysis of Systems and Software (ISPASS)*, 2023. \\
\* These authors contributed equally to this work.
{: .notice--info}
```latex
@inproceedings{astrasim2,
  author={William Won and 
          Taekyung Heo and 
          Saeed Rashidi and 
          Srinivas Sridharan and
          Sudarshan Srinivasan and
          Tushar Krishna},    
  {% raw %}title={{ASTRA-sim2.0}: Modeling Hierarchical Networks and Disaggregated Systems for Large-model Training at Scale},{% endraw %}
  booktitle={IEEE International Symposium on Performance Analysis of Systems and Software (ISPASS)},
  year={2023}
}
```

### ASTRA-sim (ISPASS 2020)
[paper](https://sites.gatech.edu/ece-synergy/files/2020/08/astrasim_ispass2020.pdf){: .btn .btn--success}
[slides](https://cpb-us-w2.wpmucdn.com/sites.gatech.edu/dist/c/332/files/2020/08/ISPASS2020-ASTRA-SIM_talk.pdf){: .btn .btn--success}
[video](https://www.youtube.com/watch?v=S-HE9yBv8_I&list=PLHJB2bhmgB7crXM7wBKIDi7OEa0UTZtrR&index=10){: .btn .btn--danger}

Saeed Rashidi, Srinivas Sridharan, Sudarshan Srinivasan, and Tushar Krishna,
"ASTRA-SIM: Enabling SW/HW Co-Design Exploration for Distributed DL Training Platforms,"
In *Proc. of the IEEE International Symposium on Performance Analysis of Systems and Software (ISPASS)*, 2020.
{: .notice--info}

```latex
@inproceedings{astrasim,
  author={Saeed Rashidi and
          Srinivas Sridharan and
          Sudarshan Srinivasan and
          Tushar Krishna},
  {% raw %}title={{ASTRA-SIM}: Enabling SW/HW Co-Design Exploration for Distributed DL Training Platforms},{% endraw %}
  booktitle={IEEE International Symposium on Performance Analysis of Systems and Software (ISPASS)},
  year={2020}
}
```

## Contact
For any questions about using ASTRA-sim, you can email the ASTRA-sim User Mailing List: <astrasim-users@googlegroups.com>

To join the mailing list, please fill out this [form](https://forms.gle/18KVS99SG3k9CGXm6).

## Core Developers
* Saeed Rashidi (Georgia Tech) <a href="mailto:saeed.rashidi@gatech.edu" class="btn btn--info"><i class="fa fa-envelope"></i> Email</a>
* Srinivas Sridharan (Meta) <a href="mailto:ssrinivas@fb.com" class="btn btn--info"><i class="fa fa-envelope"></i> Email</a>
* William Won (Georgia Tech) <a href="mailto:william.won@gatech.edu" class="btn btn--info"><i class="fa fa-envelope"></i> Email</a>
* Taekyung Heo (Georgia Tech) <a href="mailto:taekyung@gatech.edu" class="btn btn--info"><i class="fa fa-envelope"></i> Email</a>

## Additional Contributors
* Jiayi Huang (University of California, Santa Barbara)
* Apurve Chawde (Georgia Tech)
* Santosh Kumar Elangoven (Georgia Tech)
* Tushar Krishna (Georgia Tech)
* Greg Steinbrecher (Meta)
* Sudarshan Srinivasan (Intel)


{% include feature_row id="intro" %}

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fastra-sim%2Fastra-sim.github.io&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Visitor&edge_flat=false)](https://hits.seeyoufarm.com)
