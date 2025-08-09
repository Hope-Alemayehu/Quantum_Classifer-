# 🧠 Quantum vs Classical Classifier – Proof of Concept

This repository demonstrates a **hybrid quantum-classical machine learning pipeline** using [PennyLane](https://pennylane.ai/) to compare classical and quantum classification models. The project includes two Jupyter notebooks:
1. **Simulator-based model** – Runs entirely on a local quantum simulator.
2. **Real quantum device model** – Connects to IBM Quantum hardware via `pennylane-qiskit`.

## 📂 Repository Structure

```
.
├── Quantum_Classifier_Simulator.ipynb    # Variational Quantum Classifier on simulator
├── Quantum_Classifier_Real_Device.ipynb  # Same classifier run on real IBM Quantum device
└── README.md
```

## 🚀 Project Overview

We train a **Variational Quantum Classifier (VQC)** on a sample dataset and compare its performance to a **classical logistic regression** baseline.

The steps are:
1. **Preprocess dataset** – normalize and split into train/test sets.
2. **Classical baseline** – Logistic Regression from `scikit-learn`.
3. **Quantum model** – Feature encoding, variational circuit, and training with gradient descent.
4. **Results comparison** – Accuracy and decision boundaries.

## 🧰 Tech Stack

- **Python 3.9+**
- [PennyLane](https://pennylane.ai/) – Quantum machine learning framework
- [pennylane-qiskit](https://docs.pennylane.ai/projects/qiskit/) – IBM Quantum integration
- [scikit-learn](https://scikit-learn.org/) – Classical ML baseline and preprocessing
- [Matplotlib](https://matplotlib.org/) – Visualization
- **NumPy / Pandas** – Data handling

## 📦 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Hope-Alemayehu/Quantum_Classifer.git
   cd Quantum_Classifer
   ```

2. Install dependencies:
   ```bash
   pip install pennylane matplotlib scikit-learn numpy pandas
   pip install pennylane-qiskit
   ```

## 🔧 Running the Notebooks

### 1️⃣ Simulator Version
Open `Quantum_Classifier_Simulator.ipynb`.

Runs locally with:
```python
qml.device("default.qubit", wires=2)
```

### 2️⃣ Real Quantum Device Version
Open `Quantum_Classifier_Real_Device.ipynb`.

**Requirements:**
- An IBM Quantum account ([sign up here](https://quantum.cloud.ibm.com/))
- API token from IBM Quantum dashboard
- Valid backend with at least 2 qubits

Set your token:
```python
from qiskit_ibm_runtime import QiskitRuntimeService
QiskitRuntimeService.save_account(channel="ibm_quantum", token="YOUR_IBM_QUANTUM_TOKEN")
```


## ⚠️ Notes

- Running on real devices can take several minutes due to queue times.
- This project is proof-of-concept, not optimized for large-scale datasets.
- For larger datasets, quantum circuit depth and number of qubits must be carefully managed to avoid excessive noise.

## 📜 License

MIT License – feel free to use and adapt for your own experiments.
