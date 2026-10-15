
# ectool

A lightweight C++ implementation for interacting with ChromeOS Embedded Controllers (EC) from user-space on Linux systems.

## Overview
`ectool` is a low-level system utility designed to send commands to Embedded Controllers (EC) via direct hardware interfaces (e.g., LPC, I2C, Dev interface). It enables monitoring system telemetry, controlling thermal profiles, managing battery configurations, and querying EC status directly from a Linux environment.

## Features
- **Direct EC Communication:** Supports LPC and dev-interface host commands.
- **Hardware Telemetry:** Read thermal sensor data, fan speeds, and power states.
- **Lightweight Architecture:** Built with native C/C++ with minimal external dependencies.
- **Custom Hardware Support:** Optimized for ChromeOS devices running native Linux distributions.

## Building from Source

### Prerequisites
Make sure you have `cmake` and `g++` installed:
```bash
sudo apt update
sudo apt install build-essential cmake
