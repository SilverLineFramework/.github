# SilverLine

**Stable documentation of the SilverLine Framework can be found in the [Wiki](https://github.com/SilverLineFramework/silverline/wiki).**

## Overview 

A paradigm shift in how we design distributed computing systems is almost inevitable. With advanced compute, networking, sensing, and actuation, Edge devices are increasingly capable. At the same time, there is a desire to expand some of the cloud infrastructure to the edge.

Figure 1 depicts the framework's scope: it spans off-perm cloud to an on-perm edge that includes server-class devices as well as devices with more reduced compute capabilities (edge and micro-edge devices). Silverline leverages a common execution runtime that supports isolation and resource monitoring across compute classes - from small embedded devices to edge servers - to manage workloads spanning the cloud and edge. It is distinct from several previous frameworks for managing distributed computing by focusing on adaptation to changing resources and support for highly heterogeneous distributed systems found at the edge. 

![Overview](https://github.com/SilverLineFramework/silverline/blob/main/images/overview.png)
**Figure 1. Silverline Framework Scope**

## Silverline Code Repositories

Silverline is composed of an [orchestrator](https://github.com/SilverLineFramework/orchestrator) and runtimes for different platforms ([linux runtime](https://github.com/SilverLineFramework/runtime-linux), [the zephyr micro runtime](https://github.com/SilverLineFramework/runtime-micro) and a [browser runtime](https://github.com/SilverLineFramework/runtime-browser)). We also maintain/develop other components such as a [fork of a message broker](https://github.com/SilverLineFramework/mosquitto-broker), [messaging libraries](https://github.com/SilverLineFramework/paho.mqtt.c), [benchmarks](https://github.com/SilverLineFramework/benchmarks), among others.

### Services

- [orchestrator](https://github.com/SilverLineFramework/orchestrator): SilverLine orchestrator
- [mosquitto-broker](https://github.com/SilverLineFramework/mosquitto-broker): fork of the [Eclipse Mosquitto Broker](https://github.com/eclipse/mosquitto) with added monitoring capabilities.
- [file-store](https://github.com/SilverLineFramework/file-store): SilverLine file store for serving and compiling WebAssembly programs
- [prediction](https://github.com/SilverLineFramework/prediction): Resource prediction algorithm

### Runtimes

- [runtime-linux](https://github.com/SilverLineFramework/runtime-linux): linux-based WASM runtime.
    - [wasm-micro-runtime](https://github.com/SilverLineFramework/wasm-micro-runtime): fork of [WAMR](https://github.com/bytecodealliance/wasm-micro-runtime) adding per-module opcode tracking during interpreted execution
    - [paho.mqtt.c](https://github.com/SilverLineFramework/paho.mqtt.c): fork of the [Eclipse Paho C Client](https://github.com/eclipse/paho.mqtt.c) adding support for loopback
- [runtime-micro](https://github.com/SilverLineFramework/runtime-micro): [Zephyr RTOS](https://www.zephyrproject.org/)-based WASM runtime for embedded devices.

### Programs

- [benchmarks](https://github.com/SilverLineFramework/benchmarks): benchmarks and test cases for SilverLine
    - [rustpython](https://github.com/SilverLineFramework/rustpython): [RustPython](https://github.com/RustPython/RustPython) modified to use the SilverLine channels interface
    - [libsilverline](https://github.com/SilverLineFramework/libsilverline): python library for interacting with SilverLine, i.e. spawning benchmarks
