# Partial Reconfiguration on Kria SOM implementing a YOLO algorithm. 
A project focused on implementing partial reconfiguration of the Programmable logic (PL) of a Xilinx SOC with various pretrained YOLO algorithm models. With the end goal of improvying dynamic high performance systems.
Done on a Kria KV260 which features a ZYNQ UltraScale+ MPSoC. OR ALVERO.

# YOLO
The YOLO algorithm....

To implement this, we will be using Xilinx's Vitis along with it's accelerated libraries, Vitis AI.
Vitis AI is part of Vitis that must be installed separately through docker. (Docker is used to install all of the dependencies)
Vitis AI must be installed via a Linux distro or WSL on windows.

![Vitis-AI-arch](https://github.com/user-attachments/assets/a2b96df2-b5a4-4ac3-97e6-338a22c512af)


# Partial Reconfiguration
The Processor is in control of the partial reconfiguration (DFX for xilinx), and is responsible for initiating the switch. 

# Hardware requirements
A Kria KV260 connected to remotely over ethernet.

# Software requirements
Vitis

# Data requirements
PreTrained Model

# Development
## Crawl
Implement YOLO on FPGA

## Walk
Implement DFX for basic function

## Run
Combine the two

# Questions
## Processor
Which processor to run DFX stuf?

## General
How to initiate switching of models?

What data will we capture during reprogramming?
 - programming time
 - Bit stream file size
 - Power consumption
 - Could then find ratio of new to old bitstream file and relate it to programming time

# Resources
## Code references

## Relevant papers

## Basis for Research
DATE'24 and DAC'22 are reference papers. I discuss them in /docs "DATE-24.md" and "DAC-22.md"

# Future Developments
Pull images/DFX cores from remote server.
PL only reprogramming.
