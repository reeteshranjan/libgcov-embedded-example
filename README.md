# libgcov-embedded-example
An example GNU ARM Eclipse project that exhibits how to use [libgcov-embedded](https://github.com/reeteshranjan/libgcov-embedded) - a port of gcov functions for embedded systems - to get code coverage.
## Overview
It's a Blinky project for stm32f4-discovery board. It also runs fine with an emulator as well, which is easy to setup (please see below).
## Cloning Instructions
This repository has a git submodule. You need to clone it as follows.
```
$ git clone --recursive git@github.com:reeteshranjan/libgcov-embedded-example.git
```
See [this post](http://stackoverflow.com/a/4438292/3348386) in case of issues.
## Setup
- [eclipse cdt neon.1](http://www.eclipse.org/downloads/packages/eclipse-ide-cc-developers/neon1a)
- [gnu arm eclipse](http://gnuarmeclipse.github.io/). **NOTE**: The gnu arm eclipse documentation mentions a much older eclipse mars as suggested platform; however, eclipse neon.1 works just fine.
- [gnu arm toolchain v5-2016-q3-update](https://launchpad.net/gcc-arm-embedded/5.0/5-2016-q3-update) or later. **NOTE**: gcov data structures are pretty stable so things should work with older versions as well; however, it's not verified yet.
- One of:
 - smt32f4-discovery board. If using one, you also need [OpenOCD](http://gnuarmeclipse.github.io/openocd/install/) setup.
 - [QEMU](http://gnuarmeclipse.github.io/qemu/install/) emulator for stm32f4-discovery.
- May need to setup the STM32F4xx_DFP gnu arm eclipse [pack](http://gnuarmeclipse.github.io/plugins/packs-manager/). Look for "STM32F4 series" under "STMicroelectronics" and install it.

## Run
Follow this [tutorial](https://technfoblog.wordpress.com/2016/11/05/code-coverage-using-eclipse-gnu-arm-toolchain-and-gcov-for-embedded-systems/) to run this project and see how to generate gcda files.
