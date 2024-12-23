# Current Mirror and Its Topologies

# Table of Content
- [Overview](#Overview)
- [Tools Used](#Tools-Used)
- [Topologies Covered](#Topologies-Covered)
  - [Simple Current Mirror](#1-Simple-Current-Mirror)
  - [Cascode Current Mirror](#2-Cascode-Current-Mirror)
  - [Wide Swing Cascode Current Mirror](#3-Wide-Swing-Cascode-Current-Mirror)
  - [Self Biased Wide Swing Cascode Current Mirror](#4-Self-Biased-Wide-Swing-Cascode-Current-Mirror)
- [Comparative Summary](#Comparative-Summary)
- [Requirements](#Requirements)
- [Project Report](#Projject-Report)
- [Acknowledgement](#Acknowledgement)

## Overview
This repository provides a detailed exploration of **current mirror topologies**, essential components in analog circuit design. Current mirrors are pivotal for applications such as biasing, signal amplification, and current regulation. This project covers their design, analysis, and implementation, offering comprehensive insights into their functionality and performance.

## Tools Used

- [Cadence Virtuoso Schematic Editor](https://www.cadence.com/en_US/home/tools/custom-ic-analog-rf-design/circuit-design/virtuoso-schematic-editor.html) : The Cadence Virtuoso Schematic Editor provides numerous capabilities to facilitate fast and easy design entry, including design assistants that speed common tasks by as much as 5X. Well-defined component libraries allow faster design at both the gate and transistor levels.
- [Cadence Virtuoso Circuit Simulator](https://www.cadence.com/en_US/home/tools/custom-ic-analog-rf-design/circuit-simulation/spectre-fmc-analysis.html?utm_campaign=Custom_Virtuoso_Studio_product_eu_google_search_june_2023&utm_source=google&utm_medium=search&utm_content=cdn_paid_media&utm_content=Circuit_Simulation&s_kwcid=AL!14272!3!662289232220!b!!g!!circuit%20simulation&gad=1&gclid=Cj0KCQjwpompBhDZARIsAFD_Fp8Z-SxLLihhZBFwTmCU69lX0z8FEUvoFW2uLaLdkUzkxbE_Gtb2_GUaAi4xEALw_wcB) : The Cadence Spectre FMC Analysis enables fast and comprehensive design space exploration using Monte Carlo simulations of complex analog, RF, I/O, mixed-signal blocks, memories, standard cells, and bit cells while maintaining necessary statistical accuracy. It works with the Spectre X and Spectre APS Simulators and allows you to distribute Monte Carlo simulation workloads to increase throughput.

## Topologies Covered

## 1. Simple Current Mirror

The simple current mirror is a basic analog circuit used to replicate a reference current to another branch.

### Circuit Description
- Consists of two matched MOSFETs (M1 and M2).
- M1 is diode-connected to force its drain current to match the reference current (I_ref).
- M2’s gate is connected to M1’s gate, ensuring the same V_GS for both transistors.
- Assumes matched transistors operating in saturation.

#### Advantages
- Simple and easy to design.
- Minimal transistor count.

#### Disadvantages
- Poor output impedance.
- Limited accuracy due to channel-length modulation.

***Explaination:** This simplest form of a current mirror consists of two transistors, where the current is replicated (or mirrored) by ensuring that the transistors are matched in their characteristics. Typically, one transistor is configured to set a reference current, and the other transistor mirrors this current, maintaining an equivalent current in its branch.*

## 2. Cascode Current Mirror

The cascode current mirror enhances the simple current mirror by increasing its output impedance and improving accuracy.

### Circuit Description
- Adds cascode devices (M3 and M4) to shield M1 and M2 from output voltage variations.
- M3 and M4 are biased to ensure M1 and M2 remain in saturation.

#### Advantages Over Simple Current Mirror
- Higher output impedance.
- Improved current mirroring accuracy.

#### Disadvantages
- Requires additional biasing circuitry.
- Increased complexity and transistor count.

***Explaination:** This configuration is employed to achieve a higher output impedance, as an ideal current source is characterized by infinite output resistance. To make the current mirror closer to an ideal current source, this arrangement is utilized. Furthermore, due to the effects of channel-length modulation, accurate current mirroring is achieved only when the drain-to-source voltages (Vds) of both transistors are equal.*

## 3. Wide-Swing Cascode Current Mirror

The wide-swing cascode current mirror addresses the limited output swing of the traditional cascode configuration.

### Circuit Description
- Dynamically biases the cascode transistors’ gates to reduce the minimum voltage required for saturation.
- Allows for a larger output voltage swing.

#### Advantages Over Cascode Current Mirror
- Larger output voltage swing.
- Retains high output impedance and accuracy.

#### Disadvantages
- More complex biasing circuitry.
- Increased design complexity.

***Explaination:** When utilizing the cascode configuration in current mirrors, a notable challenge arises: the minimum output voltage required for accurate current mirroring is relatively high. This limitation reduces the output voltage swing of any circuitry employing the cascode configuration. However, this drawback is effectively addressed by implementing the wide-swing cascode configuration for the current mirror. In this design, an additional transistor, with a channel length four times that of the other transistors in the circuit, is introduced. The connections are arranged strategically to significantly lower the minimum output voltage required for current mirroring, thereby mitigating the issue and enhancing the performance of the circuit.*

## 4. Self-Biased Wide-Swing Cascode Current Mirror

This configuration incorporates self-biasing mechanisms to simplify external biasing.

### Circuit Description
- Introduces a self-biasing network to generate required bias voltages internally.
- Ensures all transistors operate in their desired regions without external adjustments.

#### Advantages Over Wide-Swing Cascode Current Mirror
- No need for external bias circuitry.
- Enhanced robustness against process and supply variations.
- Retains high output impedance and large output swing.

#### Disadvantages
- Increased transistor count and silicon area.
- More complex to analyze and optimize.

***Explaination:** The drawback of increased power consumption in the wide-swing cascode configuration, caused by the use of two current sources, was effectively addressed by replacing one of the current sources with a resistor. This modification reduces the overall power consumption while maintaining the desired functionality.*

**NOTE:** The self-biased and simple wide-swing configurations of current mirrors are utilized interchangeably, depending on the specific application and the requirements of the circuitry in which they are employed.

## Comparative Summary

| **Parameter**                | **Simple Mirror** | **Cascode Mirror** | **Wide-Swing Cascode** | **Self-Biased Wide-Swing**  |
|------------------------------|-------------------|--------------------|------------------------|---------------------------- |
| Output Impedance             | Low               | High               | High                   | High                        |
| Voltage Swing                | High              | Low                | Higher                 | Highest                     | 
| Complexity                   | Low               | Moderate           | High                   | Highest                     |
| Accuracy                     | Low               | High               | High                   | High                        |
| Design Robustness            | Moderate          | Moderate           | Moderate               | High                        |


## Requirements
To explore and simulate the current mirror designs, ensure you have the following:
- Circuit simulation software (e.g., LTspice, Cadence Virtuoso, Multisim)
- A basic understanding of analog circuit design principles

## Project Report
The detailed project report, containing theoretical explanations and analysis, is available here:  
[Project_Report.pdf](https://github.com/HarshitSri-Analog/Current-Mirror-Topologies/blob/main/Current%20Mirror%20Doc_updated.pdf)

Special thanks to the contributors and the analog design community for inspiring this project. 

Feel free to explore the repository for insights into the design and implementation of Bandgap Reference circuits. Contributions and feedback are welcome!

***If you find this repository helpful, please consider giving it a ⭐!***

