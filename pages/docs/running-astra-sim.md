---
layout: single
title:  "Installation"
permalink: /docs/running-astra-sim
---

## Running ASTRA-sim

### Analytical backend
Run an example inside the `examples/` directory with the analytical model as a backend.
```bash
./examples/run_allreduce.sh -n analytical
```

This command will run a single all-reduce collective on a Torus topology.
{: .notice--success}

### Garnet 2.0
Run an example inside the `examples/` directory with garnet as a backend.
```bash
./examples/run_allreduce.sh -n garnet
```

This command will run a single all-reduce collective on a Torus topology.
{: .notice--success}


### NS3
Coming soon!

<nav class="pagination">
    <a href="/docs/installation" class="pagination--pager">Previous</a>
    <a href="#" class="pagination--pager disabled">Next</a>
</nav>

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fastra-sim.github.io%2Fdocs%2Frunning-astra-sim&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=Visitor&edge_flat=false)](https://hits.seeyoufarm.com)
