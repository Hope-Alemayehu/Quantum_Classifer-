# Quantum Classifier Demo

This repository contains a proof-of-concept project comparing a classical logistic regression classifier with a quantum variational classifier (VQC) using PennyLane. Both models are trained on the `make_moons` dataset to demonstrate how AI models can operate in classical and quantum environments.

## Features

- Classical logistic regression classification with scikit-learn.
- Quantum variational classifier implemented with PennyLane on a simulated quantum device.
- Visualization of decision boundaries for both classifiers.
- Modular Jupyter notebook for easy experimentation and extension.
- Documentation guiding users through setup, training, and evaluation.

## Requirements

- Python 3.7+
- PennyLane
- scikit-learn
- matplotlib
- numpy
- qiskit (optional, for running on IBM Quantum hardware)

## Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/Hope-Alemayehu/Quantum_Classifer-.git
   cd Quantum_Classifer-
   ```
Notes
- The quantum classifier runs by default on a PennyLane simulated device.

- The code can be adapted to run on real IBM Quantum hardware with proper credentials.

- This project is designed for educational and exploratory purposes.
