# Current Mirror and Its Topologies

## Overview
This repository provides a detailed exploration of **current mirror topologies**, essential components in analog circuit design. Current mirrors are pivotal for applications such as biasing, signal amplification, and current regulation. This project covers their design, analysis, and implementation, offering comprehensive insights into their functionality and performance.

# Table of Content
- [Topologies Covered](#Topologies-Covered)
  - [Simple Current Mirror](#1-Simple-Current-Mirror)
  - [Cascode Current Mirror](#2-Cascode-Current-Mirror)
  - [Wide Swing Cascode Current Mirror](#3-Wide-Swing-Cascode-Current-Mirror)
  - [Self Biased Wide Swing Cascode Current Mirror](#4-Self-Biased-Wide-Swing-Cascode-Current-Mirror)
- [Comparative Summary](#Comparative-Summary)
- [Requirements](#Requirements)
- [Project Report](#Projject-Report)
- [Acknowledgement](#Acknowledgement)

## Topologies Covered

## 1. Simple Current Mirror

The simple current mirror is a basic analog circuit used to replicate a reference current to another branch.

### Circuit Description
- Consists of two matched MOSFETs (M1 and M2).
- M1 is diode-connected to force its drain current to match the reference current (I_ref).
- M2’s gate is connected to M1’s gate, ensuring the same V_GS for both transistors.
- Assumes matched transistors operating in saturation.

### Advantages
- Simple and easy to design.
- Minimal transistor count.

### Disadvantages
- Poor output impedance.
- Limited accuracy due to channel-length modulation.

---

## 2. Cascode Current Mirror

The cascode current mirror enhances the simple current mirror by increasing its output impedance and improving accuracy.

### Circuit Description
- Adds cascode devices (M3 and M4) to shield M1 and M2 from output voltage variations.
- M3 and M4 are biased to ensure M1 and M2 remain in saturation.

### Advantages Over Simple Current Mirror
- Higher output impedance.
- Improved current mirroring accuracy.

### Disadvantages
- Requires additional biasing circuitry.
- Increased complexity and transistor count.

---

## 3. Wide-Swing Cascode Current Mirror

The wide-swing cascode current mirror addresses the limited output swing of the traditional cascode configuration.

### Circuit Description
- Dynamically biases the cascode transistors’ gates to reduce the minimum voltage required for saturation.
- Allows for a larger output voltage swing.

### Advantages Over Cascode Current Mirror
- Larger output voltage swing.
- Retains high output impedance and accuracy.

### Disadvantages
- More complex biasing circuitry.
- Increased design complexity.

---

## 4. Self-Biased Wide-Swing Cascode Current Mirror

This configuration incorporates self-biasing mechanisms to simplify external biasing.

### Circuit Description
- Introduces a self-biasing network to generate required bias voltages internally.
- Ensures all transistors operate in their desired regions without external adjustments.

### Advantages Over Wide-Swing Cascode Current Mirror
- No need for external bias circuitry.
- Enhanced robustness against process and supply variations.
- Retains high output impedance and large output swing.

### Disadvantages
- Increased transistor count and silicon area.
- More complex to analyze and optimize.

---

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

## Acknowledgments
Special thanks to the contributors and the analog design community for inspiring this project. If you find this repository helpful, please consider giving it a ⭐!

