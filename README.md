# Image-Processing-FPGA

## Table of contents

- [Aim](#aim)
- [About the Project](#about-the-project)
- [Theory](#theory)
- [Flowchart](#flowchart)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Results](#results)

## Aim

To compress and decompress an image using the JPEG algorithm on an FPGA (tested with the Tang Primer development board).

## About the Project

This repository implements a JPEG encoder/decoder pipeline in Verilog. Phase 1 focuses on the core JPEG compression/decompression modules. Phase 2 aims to add camera (e.g. OV2640/OV7670) and TFT display interfacing.

## Theory

FPGA stands for Field Programmable Gate Array.

## Flowchart

<img src="https://miro.medium.com/max/1400/1*JQ3JejBDau8TnNUPuzYSLw.png" width="900" height="540">

## Tech Stack

- [Verilog](https://www.chipverify.com/verilog/verilog-tutorial)
- [Tang Dynasty (TD IDE)](https://tang.sipeed.com/en/getting-started/installing-td-ide/)
- [Tang Primer Dev Board documentation](https://tang.sipeed.com/en/hardware-overview/lichee-tang/)
- ModelSim (Altera)
- [FPGA resources (Intel)](https://www.intel.com/content/www/us/en/products/details/fpga/resources/overview.html)

## Project Structure

- `Codes/` : Verilog sources for compression/decompression (DCT, IDCT, quantization, encoding, decoding, top module, etc.)
- `Testbench/` : Testbench files (e.g. `tb_jpeg_compression.v`)
- `RTL_simulation/` : Simulation wave and run files
- `Results/` : Sample input/output images and comparison results
- `Documentation/` : Project documentation and notes

## Getting Started

1. Install Tang Dynasty (TD IDE) and the Tang Primer USB drivers (see TD IDE and board links above).
2. Install ModelSim (or another simulator) for RTL simulation.
3. Clone this repository and open/create a project in TD IDE.
4. Add the Verilog files from `Codes/` to your project and run synthesis/simulation as needed.

Notes:

- The repository contains RTL-level modules; adapt constraints and pin assignments for your target board.

## Results

Example shown for a 32x32 input image and ~70% compression.

- [Input image](https://github.com/harshbhosale01/image-processing-fpga/blob/master/Results/Original-img.jpeg)
- [Output image with 70 percent compression](https://github.com/harshbhosale01/image-processing-fpga/blob/master/Results/70-compressed-img.png)
- [Comparison image](https://media.discordapp.net/attachments/1006252829687689408/1030724592135835648/Compression-comparison.png?width=1120&height=538)
