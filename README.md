# Mobilisable Strength Design (MSD) for Laterally Loaded Piles in Sand

This repository contains the numerical implementation of the **Mobilisable Strength Design (MSD)** method for laterally loaded piles in sand, as described in Dobrisan et. al(2026).

## License

This project is released under an MIT-based license with additional research and liability disclaimers.

The license is based on the MIT License, with supplementary clauses clarifying that the software is provided strictly for research purposes and without responsibility for engineering or professional use.

See the [LICENSE](LICENSE) file for the full license text.

## Overview

This code provides a design method for the monotonic lateral loading of piles. It applies to a wide array of pile gemoetries, from slender piles used in offshore jacket structures to rigid, large-diameter monopiles for wind turbine foundations. Unlike empirical or semi-empirical _p-y_ methods, this approach is grounded in soil mechanics, using lower-bound plastic mechanisms (Prandtl flow and passive wedge failure) linked to mobilisable soil strength to predict pile response.

### Key Features
* **Unified Theory:** Valid for a wide range of aspect ratios ($L/D$).
* **Physics-Based:** Derived from soil mechanics rather than semi-empirical formulae
* **Complete Profiles:** Generates depth-profiles for displacement ($y$), rotation ($\theta$), bending moment ($M$), shear force ($S$), and net soil pressure ($p$).

## Requirements
* **Software:** MATLAB (R2025a or later recommended). The optional **Optimization Toolbox** needs to be installed for the code to run.

### Inputs
The function requires a set of pile and soil properties (see `input_structure_example.m` for a template).

**Required Parameters:**
* **Load:** Lateral force $H$ [N], Load application height $h$ [m].
* **Pile:** Diameter $D$ [m], Embedment length $L$ [m], Wall thickness $t$ [m], Young's Modulus $E$ [Pa].
* **Soil:** Relative density $D_r$ [%], Effective vertical stress $\sigma'_{v0}$ [Pa], Water table depth $z_{wt}$ [m], Void ratios ($e_{min}, e_{max}$) [-], Uniformity coefficient $C_u$ [-], Critical friction angle $\phi_{crit}$ [degrees].

**Optional/Advanced Parameters:**
* Small strain stiffness $G_0$, Earth pressure coefficient $K_0$, Peak friction angle $\phi_{peak}$, Peak dilation angle $\psi_{peak}$, Soil-pile interface friction angle $\delta$

## Installation

1.  Clone this repository:
    ```bash
    git clone [https://github.com/your-username/repo-name.git](https://github.com/your-username/repo-name.git)
    ```
2.  Add the repository folder to your MATLAB path.

## Usage

The main entry point is the function `msd_pile_design.m`.

### Example Code
To be added

### Citation

If you use this code or the MSD method in your work, please cite the following paper:

**Dobrisan, A., Faramarzi, A., Haigh, S. K., Osman, A., and Metje, N. (2026).** "Mobilisable strength design for laterally loaded piles in sand." Géotechnique. (Under Review).

```
@article{dobrisan2026mobilisable,
  title={Mobilisable strength design for laterally loaded piles in sand},
  author={Dobrisan, A. and Faramarzi, A. and Haigh, S.K. and Osman, A. and Metje, N.},
  journal={Geotechnique},
  year={2026},
  note={Under Review}
}
```
