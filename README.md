# Microwatt-Accelerated TinyML Core for Edge AI

## Project Overview
This project explores the integration of the open-source Microwatt POWER CPU core with a custom hardware accelerator for TinyML inference.  
The accelerator focuses on enabling efficient edge AI workloads, such as small-scale image or sensor data classification, within the ChipFoundry OpenFrame platform.

## Motivation
AI-enabled edge devices are becoming increasingly important in areas such as IoT, robotics, and intelligent driving systems.  
However, CPUs alone often struggle with compute-intensive ML tasks.  
By adding a hardware TinyML accelerator alongside Microwatt, we demonstrate a scalable and open-source solution for low-power AI at the edge.

## Technical Approach
- **Microwatt CPU**: Orchestrates computation, loads weights, manages memory, and controls the accelerator.  
- **TinyML Accelerator**: Implements a parameterized 3×3 MAC array with ReLU activation, optimized for small convolutional neural network layers.  
- **Integration**: The accelerator is attached as a coprocessor accessible through Microwatt’s bus interface.  
- **Verification**: RTL simulation with Verilator + custom testbenches, including SDF/STA constraints for reproducibility.  
- **Physical Design**: Hardened using the OpenLane flow on SKY130 technology, passing ChipFoundry precheck requirements.  

## Deliverables
- Verilog RTL for the TinyML accelerator and top-level integration with Microwatt.  
- Testbenches with reproducible results.  
- OpenLane configuration and run results for SKY130.  
- Documentation of design process, AI prompts used (if applicable), and reproducibility instructions.  
- Video demonstration and project walkthrough.  

## License
This project is released under the Apache 2.0 License.
