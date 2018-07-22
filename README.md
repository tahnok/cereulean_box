```
                        __                    __              
  ________  _______  __/ /__  ____ _____     / /_  ____  _  __
 / ___/ _ \/ ___/ / / / / _ \/ __ `/ __ \   / __ \/ __ \| |/_/
/ /__/  __/ /  / /_/ / /  __/ /_/ / / / /  / /_/ / /_/ />  <  
\___/\___/_/   \__,_/_/\___/\__,_/_/ /_/  /_.___/\____/_/|_|  
                                                              
```

> Learning some hardware, some history and some rust

The goal of this project is to make a bluebox using an stm32 f3 discovery in rust.


# Setup


??? need to try this on a fresh machine. To steal from [cortex_m_quickstart](https://docs.rs/cortex-m-quickstart/0.3.1/cortex_m_quickstart/)

 - Nightly Rust toolchain newer than nightly-2018-04-08: rustup default nightly
 - Rust target: rustup target add thumbv7em-none-eabihf
 - ARM toolchain: sudo apt-get install gcc-arm-none-eabi (on Ubuntu)
 - GDB: sudo apt-get install gdb-arm-none-eabi (on Ubuntu)
 - OpenOCD: sudo apt-get install OpenOCD (on Ubuntu)


# Running

In one terminal run `openocd -f interface/stlink-v2-1.cfg -f target/stm32f3x.cfg`

In another, `cargo run`. This drops you into a gdb session for now. Type `continue`
