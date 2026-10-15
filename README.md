# ectool

A lightweight, modern C++ user-space utility for interacting with ChromeOS Embedded Controllers (EC) on Linux systems.

## Overview

`ectool` is a low-level system utility designed to communicate directly with Embedded Controllers (EC) via hardware interfaces such as LPC, I2C, and dev interfaces. It enables real-time system monitoring, thermal management, battery diagnostics, and EC status queries directly from a native Linux environment.

## Features

- **Direct EC Communication:** Interface with LPC, I2C, and dev-interface host commands.
- **Hardware Telemetry:** Read real-time thermal sensor data, fan speeds, and power states.
- **Lightweight & Fast:** Written in native C++ with minimal external dependencies.
- **ChromeOS Hardware Support:** Optimized for MediaTek, Intel, AMD, and ARM-based Chromebook hardware running custom Linux environments.

## Building from Source

### Prerequisites

Ensure you have `cmake` and a C++ compiler installed on your system:

```bash
sudo apt update
sudo apt install build-essential cmake
```

### Compilation Steps

```bash
# Clone the repository
git clone git@github.com:bmkrb436-web/ectool-for-linux.git
cd my-first-project

# Create a build directory and compile
mkdir -p build && cd build
cmake ..
make
```

## Usage

Run `ectool` with elevated privileges (`sudo`) to allow raw access to hardware interfaces:

```bash
# Print Embedded Controller version
sudo ./src/ectool version

# Query battery status and statistics
sudo ./src/ectool battery

# Read thermal sensor values
sudo ./src/ectool temps all

# Read fan speed
sudo ./src/ectool pwmgetfanrpm
```

## License
