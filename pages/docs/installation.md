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
Make sure to use `--recursive` option to clone necessary network submodules.
{: .notice--warning}

Then, move inside the downloaded directory.

## Compile the Code
ASTRA-sim can be compiled with different network simulators.

### Analytical backend
Run the compilation script with `-c` flag to compile and integrate astra-sim with the analytical model as a backend.
```bash
./build/astra_analytical/build.sh -c
```

Running the script with `-l` flag will clean and remove build files.
{: .notice--primary}

### Garnet 2.0
Run the compilation script with `-c` flag to compile and integrate astra-sim with gem5.
```bash
./build/astra_garnet/build.sh -c
```

Running the script with `-l` flag will clean and remove build files.
{: .notice--primary}

### NS3
Coming soon!

<nav class="pagination">
    <a href="/docs/prerequisites" class="pagination--pager">Previous</a>
    <a href="/docs/running-astra-sim" class="pagination--pager">Next</a>
</nav>
