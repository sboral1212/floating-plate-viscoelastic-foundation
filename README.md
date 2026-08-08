### Physics-Informed Neural Networks (PINN) for Floating Elastic Plates on Viscoelastic Foundations

This repository contains the official PyTorch implementation and neural network weights for reproducing the **Physics-Informed Neural Network (PINN)** and **Deep Learning surrogate models** described in the 2026 paper published in *Applied Mathematics and Computation*. 

[](https://colab.research.google.com/)
[](https://opensource.org/licenses/MIT)
[](https://doi.org/10.1016/j.amc.2025.129872) 

### 📄 Associated Publication

If you find this computational framework useful, please cite the primary research paper: 

**Boral, S. (2026).**
*Dynamic response of a floating elastic plate supported on a viscoelastic foundation under moving periodic load: Analytical and neural modelling.*
**Applied Mathematics and Computation**, Volume 516, Article 129872.
**Digital Object Identifier (DOI):** [https://doi.org/10.1016/j.amc.2025.129872](https://doi.org/10.1016/j.amc.2025.129872) 

bibtex

@article{boral2026dynamic,
  title={Dynamic response of a floating elastic plate supported on a viscoelastic foundation under moving periodic load: Analytical and neural modelling},
  author={Boral, Susam},
  journal={Applied Mathematics and Computation},
  volume={516},
  pages={129872},
  year={2026},
  publisher={Elsevier},
  doi={10.1016/j.amc.2025.129872},
  url={https://doi.org/10.1016/j.amc.2025.129872}
}

Use code with caution.

### 📌 Executive Summary & Key AI Keywords

This project fuses **Scientific Machine Learning (SciML)** with traditional ocean engineering and **fluid-structure interactions (FSI)**. It replaces slow numerical differential equation solvers with rapid, high-accuracy neural network surrogates. 

* **Core Methodologies:** Physics-Informed Neural Networks (PINNs), Multilayer Perceptrons (MLP), Dispersion Model Mapping, Sine Activation Networks.
* **Physical Domain:** Hydroelasticity, wave propagation, flexural-gravity waves, moving periodic loads, Kelvin-Voigt/Maxwell viscoelastic foundations.
* **Target Applications:** Arctic ice sheet-structure interaction, runway designs on floating platforms, offshore engineering, floating airports, and wave energy converter arrays.

### 📂 Repository Architecture & File Manifest

* 📁 best_sine_pinn_model.pth — Pre-trained network weights for the PINN solver using sine activation functions.
* 📁 trained_dispersion_model.pth — Trained surrogate network mapping the hydroelastic dispersion relationship.
* 📁 X_norm.npy, Y_norm.npy — Standardized validation and testing tensors for benchmark evaluation.
* 📁 pinn_X_norm.npy, pinn_y_norm.npy — Pre-processed spatial-temporal data constraints for physics-based loss functions.

### 🚀 Execution & Quick Start Guide

### Prerequisites & Dependencies

Install the required computational mathematics and machine learning libraries: 

bash

pip install torch numpy matplotlib scipy

Use code with caution.

### Loading Pre-trained Models

You can load the neural network models into your PyTorch pipeline directly using the snippet below: 

python

import torch

# Load the dispersion relationship neural surrogate
dispersion_model = torch.load('trained_dispersion_model.pth')
dispersion_model.eval()

# Load the PINN model for floating elastic plate dynamics
pinn_model = torch.load('best_sine_pinn_model.pth')
pinn_model.eval()

print("Neural network weights successfully initialized.")

Use code with caution.

### 📊 Core Scientific Contributions

1. **Elimination of Computational Bottlenecks:** Shows how neural network surrogates cut down CPU compute times for moving-load wave equations from hours to fractions of a second.
2. **Viscoelastic Foundation Mapping:** Accurately tracks damping and subgrade drag variations without numerical stability failures.
3. **Resonance Boundary Capture:** Predicts quasi-resonance structural limits under critical velocities with low mean squared error (MSE).

### 🤝 Contact and Global Collaboration

**Dr. Susam Boral**
*Research Fellow, Trinity College Dublin*
*📧 Academic Inquiries:* susamboral@gmail.com / borals@tcd.ie
*🌐 Research Profile:* [Google Scholar Profile](https://scholar.google.com/citations?user=lxZzGV8AAAAJ)
