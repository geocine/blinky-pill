# Blinky Pill

Blinky test on Blue Pill STM32F103

![Blinky Blue Pill](https://i.imgur.com/9vPmKH5.gif)
## Setup

1. Execute the following to install dependencies needed for compilation. ***ARM Cross-Compiler and Linker***.

    **Mac**
    ```
    brew install gcc-arm-embedded
    ```
    **Linux (Ubuntu)**
    ```
    sudo apt install binutils-arm-none-eabi gcc-arm-none-eabi
    ```
2. Install rustup (the Rust toolchain installer) from https://rustup.rs/
3. Install the rust-std component `thumbv7m-none-eabi` to cross-compile for ARM Cortex-M3 (the processor used in the Blue Pill)
    ```
    rustup target add thumbv7m-none-eabi
    ```
4. Install `cargo-flash`
    ```
    cargo install cargo-flash
    ```

## Compiling
1. Build

    ```
    cargo build --release
    ```
2. Make sure your Blue Pill is connected to your ST Link programmer. Execute this command

    ```
    cargo flash --chip stm32f103C8 --release
    ```