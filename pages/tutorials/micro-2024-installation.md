---
layout: single
title:  "Getting Started for MICRO 2024 Tutorial"
permalink: /tutorials/micro-2024/installation
---

We provide Docker image set up for MICRO 2024 tutorial for clean ASTRA-sim execution environment. We strongly recommend you to use this Docker environment for this tutorial.

## Pulling Docker Image
First, you should pull `astrasim/astra-sim` Docker Image from the Docker Hub.
```bash
$ docker pull astrasim/tutorial-micro2024
```

## Cloning ASTRA-sim
We provide sandboxed Chakra and ASTRA-sim repository for tutorial purposes. You can clone them:
```bash
$ git clone git@github.com:astra-sim/tutorials.git
$ cd tutorials/micro2024
$ ./clone_repos.sh
```

## Starting Docker Container
You can start a Docker Container for the compliation/execution, while the cloned ASTRA-sim and Chakra linked to it.
```bash
$ docker run -it \
    -v $(pwd):/app/micro2024 \
    astrasim/tutorial-micro2024
[docker]$ cd ../micro2024
```

## Installing Chakra
Inside the Docker Container, first install Chakra (which is an ASTRA-sim dependency).
```bash
[docker]$ ./install_chakra.sh
```

## Compile ASTRA-sim
Once Chakra has been installed, compile ASTRA-sim with the analytical network backend.
```bash
[docker]$ ./compile_astra_sim.sh
```

## Running Examples
After successful installation and compilation of ASTRA-sim, please follow the examples in the actual tutorials, summarized in the [demo.pdf](https://astra-sim.github.io/assets/tutorials/micro-2024/7_demo.pdf).

<nav class="pagination">
    <a href="/tutorials/micro-2024" class="pagination--pager">Back to Tutorial Page</a>
</nav>

![Badge](https://hitscounter.dev/api/hit?url=https%3A%2F%2Fastra-sim.github.io%2Ftutorials%2Fmicro-2024%2Finstallation&label=&icon=window&color=%23198754&message=&style=flat&tz=US%2FEastern)
