# Synthroids
A [game](https://www.react.uni-saarland.de/publications/GHKF19.pdf) synthesized for FPGAs from [Temporal Stream Logic](https://www.react.uni-saarland.de/publications/FKPS19a.pdf)

## Requirements

### TSL-tools
You need the TSL-toolchain to convert TSL-specifications into the TLSF-format and to convert the control flow model to code of a [FRP-framework](https://www.react.uni-saarland.de/publications/FKPS19b.pdf).
- https://github.com/reactive-systems/tsltools

### Synthesis tool
You need a TLSF-compatible LTL-synthesis tool. We used the following ones
- [Strix](https://strix.model.in.tum.de/)
- [Bosy](https://github.com/reactive-systems/bosy)

Note that different sysnthesis tools might vary in how much recources they use and in the size of their outputed controll-flow-model.

### Clash
You need the Clash HDL used as the FRP-Framework, generating verlog code:
- https://github.com/clash-lang/clash-compiler

Due to different version we recommend to do
`` git checkout fff460634d80db6f4add2b887cea22c2d937fc35``
before building the compiler.

### Hardware
You may not need the following tools depending if you want work on generated verilog code or if you want to rebuild the whole physical system.

#### Yosys
You need the Yosys Open SYnthesis Suite to synthesize the generated verilog code.
- https://github.com/YosysHQ/yosys

#### Nextpnr
You need nextpnr a vendor neutral, timing driven, FOSS FPGA place and route tool.
- https://github.com/YosysHQ/nextpnr

#### Icestorm
You need the IceStorm tools.
- https://github.com/cliffordwolf/icestorm

#### Icotools
You need the icoprog programming tool for IcoBoards.
- https://github.com/cliffordwolf/icotools
