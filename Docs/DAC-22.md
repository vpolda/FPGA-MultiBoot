# Intro
Published at: https://mehmet.belviranli.com/papers/dac22.pdf
This doc is focused on relating DAC'22 to my current project with using an FPGA instead and implementing DFX (Dynamic Function eXchange). 
This is not a summary of the paper itself. ChatGPT was used to develop this doc.

# Paper Summary
## Data Flow and Scheduling
The user can set an Energy Consumption Target (ECT) which then determines which schedule the incoming data takes.
Either a performance focused one, ie through GPUs. Or an energy saving one, ie through DLAs. The scheduling allows the data to go through some of the NN layers on the GPU first and then the remaining on the DLAs.
This provides a hybrid of performance and energy saving, based on user constraints.



## Algorithms 
TensorRT as the engine. (I don't think TRT will work with non-FPGA things tbh)
They only used NN algorithms that were capable of running on either GPUs or DLAs: VGG-16/19, Resnet18/50, Alexnet, and GoogleNet. 

## Hardware constraints
Shared Memory
DLAs have their own private memory. This results in a lag of whenever the model transitions given that the DLA's must write their data back to the shared memory.


## Results

# Applicability to FPGAs
The paper proposes a dynamic schedule that prioritizes either performance or energy. Based on user settings.

The thing I noticed I believe an FPGA could improve is the DLA transistion period


# Other Questions
#### Should you make sure your energy consumption is larger than it actually is?
To give room for error, and in case energy saving is needed in a critical environment.

#### Switch power supplies?
Using say your laptop vs a wall plug.