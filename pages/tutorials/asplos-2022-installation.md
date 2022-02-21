---
layout: single
title:  "Getting Started for ASPLOS 2022 Tutorial"
permalink: /tutorials/asplos-2022/installation
---

## 1. Getting Started from Source
### Install Prerequisites
```
sudo apt -y install\
    vim gcc g++ make cmake\
    libboost-dev libboost-program-options-dev\
    python3 git
```

### Clone ASTRA-sim
```
git clone --recursive https://github.com/astra-sim/astra-sim.git
```

### Compile ASTRA-sim
```
cd astra-sim/build/astra_analytical/
./build.sh -c
```

### Verify Installation
Work in progress; will be added soon!

## 2. Getting Started with Prebuilt Docker Image
### Pull Docker Image
```
docker pull astrasim/astra-sim-tutorial
```
### Run Container and Build ASTRA-sim
```
docker run -it astrasim/astra-sim-tutorial
cd astra-sim/
./build/astra_analytical/build.sh -c
```

<nav class="pagination">
    <a href="/tutorials/asplos-2022" class="pagination--pager">Back to Tutorial Page</a>
</nav>
