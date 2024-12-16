# Current Mirror and Its Topologies

## Overview
This repository provides a detailed exploration of **current mirror topologies**, essential components in analog circuit design. Current mirrors are pivotal for applications such as biasing, signal amplification, and current regulation. This project covers their design, analysis, and implementation, offering comprehensive insights into their functionality and performance.

## Topologies Covered
1. **Simple Current Mirror**
   - The foundational configuration for current mirroring, characterized by minimal complexity and ease of implementation.
2. **Cascode Current Mirror**
   - Enhances output resistance and reduces current variation, making it ideal for high-performance analog circuits.
3. **Wide-Swing Cascode Current Mirror**
   - Designed to maximize output voltage swing while retaining high output resistance, addressing the limitations of conventional cascode designs.
4. **Self-Bias Wide-Swing Cascode Current Mirror**
   - An advanced topology that incorporates self-biasing for enhanced stability and optimized performance.

## Features
- **Circuit Diagrams**: High-quality schematic representations for each topology.
- **Simulation Files**: Ready-to-use SPICE or equivalent EDA tool files for performance analysis.
- **Performance Metrics**: Detailed evaluations, including output resistance, compliance voltage, power consumption, and voltage swing.
- **Theoretical Insights**: In-depth explanations of the operating principles and design considerations of each topology.
- **Applications**: Real-world use cases in analog systems such as operational amplifiers, voltage references, and signal processing circuits.

## Repository Structure
```
├── Schematics/                                    # SPICE or EDA simulation files
├── current mirror Doc_updated/                    # Project report and theoretical documentation
├── Simulations and Results/                       # Simulation results and performance analysis
├── README.md                                      # Project overview and instructions
```

## Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/current-mirror-topologies.git
   ```
2. Navigate to the repository:
   ```bash
   cd current-mirror-topologies
   ```
3. Open the simulation files in your preferred circuit simulation tool (e.g., LTspice, Cadence Virtuoso).

## Requirements
To explore and simulate the current mirror designs, ensure you have the following:
- Circuit simulation software (e.g., LTspice, Cadence Virtuoso, Multisim)
- A basic understanding of analog circuit design principles

## Project Report
The detailed project report, containing theoretical explanations and analysis, is available in the `docs/` folder:  
[Project_Report.pdf](https://github.com/HarshitSri-Analog/Current-Mirror-Topologies/blob/main/Current%20Mirror%20Doc_updated.pdf)

## Acknowledgments
Special thanks to the contributors and the analog design community for inspiring this project. If you find this repository helpful, please consider giving it a ⭐!

