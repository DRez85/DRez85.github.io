---
title: Block Diagram
---

# Overview

This document explains the block diagram and related design decisions for the Motor Driver Subsystem used in a daisy-chained UART-based embedded control system. The motor subsystem receives UART messages, decodes them using a PIC18F47Q10 microcontroller, and issues control commands via SPI to the IFX9201SGAUMA1 motor driver. All components and signal lines are clearly labeled with voltage, signal type, and pin counts to support manufacturing and debugging. The design addresses feedback and includes all required system-level elements such as power regulation, bidirectional ICSP, and future scalability.

## Changes Made From Feedback

In Regards to feedback from the first verion of the block diagram there were a few things that I changed. I added the correspoding pin that each component was connected to. IN addition, Labels were added for digital, digital parallel and voltage. 

![Motor_Block_Diagram_V2](https://github.com/user-attachments/assets/3ab39ad4-fbec-4805-aaf1-7ccc7b0ebc53)
