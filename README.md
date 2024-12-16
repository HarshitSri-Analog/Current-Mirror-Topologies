# Current Mirror and Its Topologies

## Overview
This repository focuses on the design, analysis, and implementation of various **current mirror topologies**, which are critical components in analog circuit design. Current mirrors are widely used for biasing, signal amplification, and current regulation in analog systems. This project provides theoretical insights, circuit diagrams, and simulation files for different current mirror configurations.

## Topologies Covered
1. **Simple Current Mirror**
   - The fundamental configuration for current mirroring with minimal complexity.
2. **Cascode Current Mirror**
   - Improved output resistance and reduced current variation.
3. **Wide-Swing Cascode Current Mirror**
   - Optimized for maximizing output voltage swing while maintaining high output resistance.
4. **Self-Bias Wide-Swing Cascode Current Mirror**
   - Advanced topology with self-biasing for better stability and enhanced performance.

## Features
- **Circuit Diagrams**: Clear schematic representations of all topologies.
- **Simulation Files**: SPICE or equivalent EDA tool files for circuit analysis.
- **Performance Analysis**: Detailed comparison of output resistance, compliance voltage, power consumption, and more.
- **Theoretical Insights**: Explanations of the working principles and advantages of each topology.
- **Applications**: Examples of how these topologies are used in analog systems like operational amplifiers, voltage references, and signal processing circuits.

## Repository Structure
```
├── diagrams/                # Circuit diagrams of the current mirror topologies
├── simulations/             # SPICE or EDA simulation files
├── docs/                    # Theoretical explanations and documentation
├── results/                 # Simulation results and performance analysis
├── README.md                # Project overview and instructions
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
- Circuit simulation software (e.g., LTspice, Cadence Virtuoso, Multisim)
- Basic understanding of analog circuit design

## Acknowledgments
Special thanks to the contributors and the analog design community for inspiring this project. If you find this repository helpful, please consider giving it a ⭐!
