---
layout: single
title:  "Getting Started for ISCA 2022 Tutorial"
permalink: /tutorials/isca-2022/installation
---

# From Source Code
## Install Prerequisites
Please install dependencies shown below, according to your operating system.

### Debian/Ubuntu
Using `apt`.
```bash
sudo apt -y install \
    vim gcc g++ make cmake \
    libboost-dev libboost-program-options-dev \
    python3 git
```

### macOS
Using `homebrew`.
```bash
brew install boost cmake coreutils
```

### Windows
Please use Windows Subsystem for Linux. [WSL](https://docs.microsoft.com/en-us/windows/wsl/install){: .btn .btn--info}


## Clone ASTRA-sim Tutorial
```bash
git clone https://github.com/astra-sim/tutorials.git
```

## Clone ASTRA-sim
```bash
cd tutorials/isca2022
./clone_astra_sim.sh
```

## Build ASTRA-sim for Exercise 1
```bash
./exercise_1/build.sh
```
When build fails, please check if dependencies listed above are properly installed.
{: .notice--warning}

## Run Exercise 1
```bash
./exercise_1/exercise_1.sh
```
When execution fails, please check if ASTRA-sim is successfully compiled.
{: .notice--warning}

<br><br><br>

# From Prebuilt Docker Image
## Pull Docker Image
```bash
docker pull astrasim/astra-sim-tutorial
```

## Run Container and Build ASTRA-sim
```bash
docker run -it astrasim/astra-sim-tutorial
cd tutorials/isca2022/astra-sim/
./build/astra_analytical/build.sh -c
```

## Build ASTRA-sim for Exercise 1
```bash
./exercise_1/build.sh
```

## Run Exercise 1
```bash
./exercise_1/exercise_1.sh
```

<nav class="pagination">
    <a href="/tutorials/isca-2022" class="pagination--pager">Back to Tutorial Page</a>
</nav>

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=http%3A%2F%2Fastra-sim.github.io%2Ftutorials%2Fisca-2022%2Finstallation&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Visitor&edge_flat=false)](https://hits.seeyoufarm.com)
