# FPGA_MultiBoot
A project focused on implementing multi-hardware configuration functionality on a Xilinx SOC with the goal of improvying dynamic high performance systems.
Done on a Kria KV260 which features a UltraScale+ MPSoC ZU5EV.

## Goal 
Improving high performance heterogenous computer systems

# Questions
## Typical setup?
I think this answer would define some of my other questions, but what will a typical setup look like?

## Why Kria SOM?

## Part/core swap(DFX) or full image boot?
 - Dependant on if different i/o is needed per config, ie different external hardware
 - DFX is faster, less intense

## How much Processor intervention?
Looks like both DFX and full image require configuration on the processor side, maybe we could look into development of Programmable Logic only.
Either would require the processor to be the driver or an external microcontroller (if custom board is designed). It interfaces with the ICAP interface.

# Requirements
## Design
 - Switch between at least two configurations
 - Use anything beside jtag programming via external PC

## Analysis
 - Record boot and load time and power consumption?
 - Relation to bit stream size?
 - Memory requirements?

# Development

## PS Driven
### Crawl
Boot from memory

### Walk

### Run

## PL Driven (Hardware only)
### Crawl

### Walk

### Run

# Future Developments
Pull images/DFX cores from remote server.
