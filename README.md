[![Version](https://img.shields.io/github/v/release/Open-CMSIS-Pack/ST_NUCLEO-F030R8_BSP)](https://github.com/Open-CMSIS-Pack/ST_NUCLEO-F030R8_BSP/releases/latest)
[![License: Apache-2.0](https://img.shields.io/badge/License-Apache--2.0-green?label)](https://github.com/Open-CMSIS-Pack/ST_NUCLEO-F030R8_BSP/blob/main/LICENSE-Apache-2.0)
[![License: BSD-3-Clause](https://img.shields.io/badge/License-BSD--3--Clause-green?label)](https://github.com/Open-CMSIS-Pack/ST_NUCLEO-F030R8_BSP/blob/main/LICENSE-BSD-3-Clause)
[![Examples Build Test](https://img.shields.io/github/actions/workflow/status/Open-CMSIS-Pack/ST_NUCLEO-F030R8_BSP/Test-Examples.yml?logo=arm&logoColor=0091bd&label=Examples%20Build%20Test)](./.ci)

# ST_NUCLEO-F030R8_BSP

This is the development repository for the **STMicroelectronics NUCLEO-F030R8 Board Support Pack (BSP)** - a CMSIS software pack that is designed to work with all compiler toolchains (Arm Compiler, GCC, IAR, LLVM). It is released as [CMSIS software pack](https://www.keil.arm.com/packs/nucleo-f030r8_bsp-keil) and therefore accessible by CMSIS-Pack enabled software development tools.

This BSP uses the generator integration of the [CMSIS-Toolbox to Configure STM32 Devices with CubeMX](https://open-cmsis-pack.github.io/cmsis-toolbox/CubeMX/) that is also supported in µVision 5.40 and higher.

## Repository top-level structure

Directory                   | Description
:---------------------------|:--------------
[.ci](./.ci)                | Files that are related to the Continuous Integration (CI) tests of this BSP.
[.github/workflows](https://github.com/Open-CMSIS-Pack/ST_NUCLEO-F030R8_BSP/tree/main/.github/workflows) | [GitHub Actions](#github-actions) scripts described below.
[CMSIS/Driver](https://github.com/Open-CMSIS-Pack/ST_NUCLEO-F030R8_BSP/tree/main/CMSIS/Driver)           | Contains a [CMSIS-Driver VIO](https://arm-software.github.io/CMSIS_6/latest/Driver/group__vio__interface__gr.html) that is configured for the board peripherals.
[Documents](https://github.com/Open-CMSIS-Pack/ST_NUCLEO-F030R8_BSP/tree/main/Documents)                 | [Usage overview](https://github.com/Open-CMSIS-Pack/ST_NUCLEO-F030R8_BSP/tree/main/Documents/OVERVIEW.md) for examples and board documentation provided by STMicroelectronics.
[Examples/Blinky](https://github.com/Open-CMSIS-Pack/ST_NUCLEO-F030R8_BSP/tree/main/Examples/Blinky)     | Blinky example in *csolution project format* using [CMSIS-Driver VIO](https://arm-software.github.io/CMSIS_6/latest/Driver/group__vio__interface__gr.html) and [CMSIS-Compiler](https://arm-software.github.io/CMSIS-Compiler/main/index.html) for printf I/O retargeting.
[Images](https://github.com/Open-CMSIS-Pack/ST_NUCLEO-F030R8_BSP/tree/main/Images)                       | [Pictures](https://github.com/Open-CMSIS-Pack/ST_NUCLEO-F030R8_BSP/blob/main/Images/nucleo-f030r8_large.png) of the board.

## Using the development repository

This development repository can be used in a local directory and [mapped as software pack](https://open-cmsis-pack.github.io/cmsis-toolbox/build-tools#install-a-repository) using for example `cpackget` with:

    cpackget add <path>/Keil.NUCLEO-F030R8_BSP.pdsc

## Generate software pack

The software pack is generated using bash shell scripts.

- `./gen_pack.sh` based on [Open-CMSIS-Pack/gen-pack](https://github.com/Open-CMSIS-Pack/gen-pack) generates the software pack.
Run this script locally with:

      ST_NUCLEO-F030R8_BSP $ ./gen_pack.sh

### GitHub Actions

The repository uses GitHub Actions to generate the pack and build examples:

- `.github/workflows/pack.yml` based on [Open-CMSIS-Pack/gen-pack-action](https://github.com/Open-CMSIS-Pack/gen-pack-action) generates pack using the [Generate software pack](#generate-software-pack) scripts.
- `.github/workflows/Test-Examples.yml` test build of examples.

## Issues

Please feel free to raise an [issue on GitHub](https://github.com/Open-CMSIS-Pack/ST_NUCLEO-F030R8_BSP/issues)
to report misbehavior (i.e. bugs) or start discussions about enhancements. This
is your best way to interact directly with the maintenance team and the community.
We encourage you to append implementation suggestions as this helps to decrease the
workload of the maintenance team.
