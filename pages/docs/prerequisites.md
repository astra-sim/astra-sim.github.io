---
layout: single
title:  "Prerequisites"
permalink: /docs/prerequisites
---

## Prerequisites
- C++ Compiler (clang++ / g++)
- CMake build system [CMake](https://cmake.org){: .btn .btn--info .btn--small}
- Boost C++ Libraries [Boost](https://www.boost.org){: .btn .btn--info .btn--small}

## Installaling Dependencies
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

<nav class="pagination">
    <a href="#" class="pagination--pager disabled">Previous</a>
    <a href="/docs/installation" class="pagination--pager">Next</a>
</nav>
