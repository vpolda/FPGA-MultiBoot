# Partial Reconfiguration on Kria SOM implementing a YOLO algorithm. 
A project focused on implementing partial reconfiguration of the Programmable logic (PL) of a Xilinx SOC with various pretrained YOLO algorithm models. With the end goal of improvying dynamic high performance systems.
Done on a Kria KV260 which features a ZYNQ UltraScale+ MPSoC. OR ALVERO.

# IDK topics?
## YOLO
The YOLO algorithm....

## Vitis AI
To implement YOLO, we will be using Xilinx's Vitis along with Vitis AI. This allows us to rapidly deploy models for the following frameworks shown in the image below onto a Xilinx device.
Models can be uploaded untrained or pretrained onto the FPGA.

![Vitis-AI-arch](https://github.com/user-attachments/assets/a2b96df2-b5a4-4ac3-97e6-338a22c512af)

This is achieved through transforming a model into high level synthesis in C++, which is then compiled into premade HDL. Using this does have the down side of losing control of the details of the design, and increased overhead (therefore, increased power and resource consumption). 
However, in most general cases and ours, these are acceptable drawbacks for rapid deployment.

Vitis AI includes the following key components:

    AI Model Zoo: a comprehensive set of pre-optimized models that are ready to deploy on Xilinx devices.
    AI Optimizer: an optional model optimizer that can prune a model by up to 90%. It is separately available with commercial licenses.
    AI Quantizer: a powerful quantizer that supports model quantization, calibration, and fine-tuning.
    AI Compiler: compiles the quantized model to a high-efficient instruction set and data flow.
    AI Profiler: performs an in-depth analysis of the efficiency and utilization of AI inference implementation.
    AI Library: offers high-level yet optimized C++ APIs for AI applications from edge to cloud.
    DPU: efficient and scalable IP cores that can be customized to meet the needs of many different applications.

### Some Notes on install Vitis AI
Vitis AI is part of Vitis that must be installed separately from other xilinx tools. It must be git cloned and then have its dependencies installed through docker. And it must be installed via a Linux distro or WSL on windows.
We used the WSL Ubuntu on Windows 10 to get it running and had docker installed on the windows 10 side only. The git repo was also cloned to the windows 10 side. The only thing WSL is used for it to run the docker_run.sh.
It is extremely important to make sure Docker on windows recongnizes WSL.

**To launch **
 - Launch powershell
 - Enter: wsl -d ubuntu
 - Check that docker is running on windows AND vitis AI container is installed
 - switch to relevant user
 - cd to Vitis-AI git repo
 - Run: ./docker_run.sh xilinx/vitis-ai-cpu:latest

## Hardware
A Kria KV260 connected to remotely over ethernet. (IDK if this is going to work)

## Model
Which model are we going with? etc
TinyYOLO? etc
Constrained by needing to use pytorch, ONNX, and tensorflow

# Development
## Crawl
Implement YOLO on FPGA
 - 
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
