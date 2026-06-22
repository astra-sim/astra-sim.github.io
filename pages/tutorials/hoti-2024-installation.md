---
layout: single
title:  "Getting Started for HotI 2024 Tutorial"
permalink: /tutorials/hoti-2024/installation
---

We provide Docker image set up for HotI 2024 tutorial for clean ASTRA-sim execution environment. We strongly recommend you to use this Docker environment for this tutorial.

## Pulling Docker Image
First, you should pull `astrasim/astra-sim` Docker Image from the Docker Hub.
```bash
$ docker pull astrasim/tutorial-hoti2024
```

## Cloning ASTRA-sim
We provide sandboxed Chakra and ASTRA-sim repository for tutorial purposes. You can clone them:
```bash
$ git clone git@github.com:astra-sim/tutorials.git
$ cd tutorials/hoti2024
$ ./clone_astra_sim.sh
```

## Starting Docker Container
You can start a Docker Container for the compliation/execution, while the cloned ASTRA-sim and Chakra linked to it.
```bash
$ docker run –it \
    -v $(pwd):/app/hoti2024 \
    astrasim/tutorials-hoti2024
[docker]$ cd hoti2024
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

<nav class="pagination">
    <a href="/tutorials/hoti-2024" class="pagination--pager">Back to Tutorial Page</a>
</nav>

