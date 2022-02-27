---
layout: single
title:  "Getting Started for ASPLOS 2022 Tutorial"
permalink: /tutorials/asplos-2022/installation
---

## 1. Getting Started with Source Codes
### Install Prerequisites
```
sudo apt -y install\
    vim gcc g++ make cmake\
    libboost-dev libboost-program-options-dev\
    python3 git
```

### Clone ASTRA-Sim Tutorial
```
git clone --recursive https://github.com/astra-sim/tutorials.git
```

### Clone ASTRA-Sim
```
cd tutorials/asplos2022
./clone_astra_sim.sh
```

### Build ASTRA-sim
```
cd astra-sim/
./build/astra_analytical/build.sh -c
```

### Setup Exercise 0
```
cd ../
./exercise_0/setup.sh
```

## 2. Getting Started with Prebuilt Docker Image
### Pull Docker Image
```
docker pull astrasim/astra-sim-tutorial
```
### Run Container and Build ASTRA-sim
```
docker run -it astrasim/astra-sim-tutorial
cd tutorials/asplos2022/astra-sim/
./build/astra_analytical/build.sh -c
```

### Setup Exercise 0
```
cd ../
./exercise_0/setup.sh
```

<nav class="pagination">
    <a href="/tutorials/asplos-2022" class="pagination--pager">Back to Tutorial Page</a>
</nav>
