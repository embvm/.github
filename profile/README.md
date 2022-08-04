## Embedded Virtual Machine Project


The Embedded Virtual Machine (Embedded VM or embvm for short) is an experimental development effort by [Embedded Artistry](https://github.com/orgs/embeddedartistry/). We are creating a software framework that demonstrates how developers can create software that is easy to change, easy to test, and easy to reuse. We hope that it can serve as a model of evolutionary embedded software design techniques.

The ultimate goals of the Embedded Virtual Machine project are:

- Increasing the ability to reuse embedded systems software across products
- Minimizing the cost of hardware changes in an embedded system by constraining existing code modifications to isolated modules
- Reduce time-to-market by enabling developers to build embedded systems software by leveraging modular, tested component
- Provide developers with tools and constructs that enable them to develop, test, and debug embedded software on their development machines

We carefully selected these goals because we were continually tired of repeatedly facing [the same challenges the past twelve years](https://embeddedartistry.com/blog/2018/08/06/musings-on-tight-coupling-between-firmware-and-hardware/). We're tired of being stuck in the software development dark ages. We want to do our part to improve the state of the art in embedded systems software development, enabling users like you to more quickly develop reliable embedded systems software.

## Core Project

[embvm-core](https://github.com/embvm/embvm-core) is the primary Embedded VM repository. This repo provides the core abstractions, boot-related code, utilities, and supporting libraries that are used to build Embedded VM applications. These abstractions are used to quickly create and port embedded systems software from one platform to another. It is the minimal dependency needed for a new Embedded VM project.

## Reference Projects

- [c-interfaces](https://github.com/embvm/c-interfaces) - a collection of abstract interfaces in C

## Demonstration Projects

We provide a number of demonstration projects.

### Applications

- [embvm/blinky](https://github.com/embvm/blinky) contains the application layer code for a simple `blinky` example. This project runs on a personal computer using an Aardvark adapter hooked up to an LED, an nRF52840 development kit, an nRF USB Dongle, and an STM32 NUCLEO-L4R5ZI development board.
- [embvm-demo](https://github.com/embvm/embvm-demo) contains a more complicated example application involving LEDs, a time-of-flight sensor, and an OLED display. This application runs on a personal computer using an Aardvark adapter, an nRF52840 development kit, and an STM32L4R5ZI-P Nucleo development kit.

### Hardware Platforms

- [embvm-demo-platforms](https://github.com/embvm/embvm-demo-platforms) contains example platforms and hardware platforms that are shared by our [blinky](https://github.com/embvm/blinky) and [embvm-demo](https://github.com/embvm/embvm-demo) projects
- [stm32l4](https://github.com/embvm/stm32l4) provides an example hardware platform, platform, and blinky application that will run on an STM32 NUCLEO-L4R5ZI development kit.

## Processor Support

We have modules that provide minimal support for the following processors:

- [arm-architecture](https://github.com/embvm/arm-architecture) provides common functionality that can be (re)used across ARM processors
- [nordic](https://github.com/embvm/nordic) (nRF52840)
- [stm32l4](https://github.com/embvm/stm32l4)

## OS Support

- POSIX support is provided as part of [embvm-core](https://github.com/embvm/embvm-core)
- [freertos-interface](https://github.com/embvm/freertos-interface)

## Related Efforts

- Drivers that are designed to support this ecosystem can be found in the [embvm-drivers](https://github.com/embvm-drivers) organization
- The Embedded VM project makes use of repositories that can be found in the [embeddedartistry](https://github.com/embeddedartistry) organization:
  - [libc](https://github.com/embeddedartistry/libc)
  - [libmemory](https://github.com/embeddedartistry/libmemory)
  - [libcpp](https://github.com/embeddedartistry/libcpp)
  - [meson-buildsystem](https://github.com/embeddedartistry/meson-buildsystem)
  - [compiler-rt](https://github.com/embeddedartistry/compiler-rt)
  - [openlibm](https://github.com/embeddedartistry/openlibm)
  - [embedded-unwind](https://github.com/embeddedartistry/embedded-unwind)

## Contributor Guidelines

We welcome contributions from the community for all of our projects. If you are interested in contributing, please review the following information:

- [Code of Conduct](https://embeddedartistry.com/fieldatlas/embedded-artistry-code-of-conduct/) 
- [Source Code Commit Guidelines](https://embeddedartistry.com/fieldatlas/source-control-commit-guidelines/)
- [Embedded Artistry's GitHub Process](https://embeddedartistry.com/fieldatlas/embedded-artistrys-github-process/)

If you are unfamiliar with open source development, you will want to start with our [Open Source Contribution Guide](https://embeddedartistry.com/fieldatlas/open-source-contribution-guide/).
