---
layout: single
title:  "Installation"
permalink: /docs/installation
---

## Download ASTRA-sim
To install ASTRA-sim, clone it from the GitHub repo.
```bash
git clone --recursive https://github.com/astra-sim/astra-sim.git
```
Make sure to use `--recursive` option to clone necessary network simulation submodules.
{: .notice--warning}

Then, move inside the downloaded directory.


## Compile the Code
ASTRA-sim can be compiled with different network simulators.

### Analytical backend
To compile, run the compilation script with `-c` flag.
```bash
./build/astra_analytical/build.sh -c
```

Running the script with `-l` flag will clean and remove build files.
```bash
./build/astra_analytical/build.sh -l
```

### Garnet 2.0
To be added

## Package Dependencies
To be added
