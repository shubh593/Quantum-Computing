# Quantum Computing & Deep Learning Workspace (`qc`)

A research and experimentation repository integrating **Quantum Circuit Simulation** (via Qiskit), **Reinforcement Learning** (Gym, Stable-Baselines3), and **Deep Learning** (PyTorch, TensorFlow/Keras).

---

## Overview

This workspace explores computational modeling across quantum and classical paradigms:
- **Quantum Computing**: Single-qubit state superposition, measurement, and Aer simulation using Qiskit.
- **Reinforcement Learning**: Tabular Q-learning on discrete environments (`FrozenLake-v1`) and Deep Q-Network (DQN) architectures on continuous control benchmarks (`CartPole-v1`).
- **Computer Vision & Deep Learning**: Convolutional Neural Networks implemented in both PyTorch (MNIST) and TensorFlow/Keras (CIFAR-10).

---

## Project Structure

```text
.
├── data/                  # Downloaded datasets (MNIST, CIFAR-10)
├── main.py                # Package entrypoint script
├── pyproject.toml         # Project specifications and core dependencies
├── uv.lock                # Pinned dependency lockfile
├── .gitignore             # Ignored runtime and build artifacts
│
├── Quantum_Circuit.ipynb  # Superposition and Aer quantum simulation
├── RL_Gym.ipynb           # Q-Learning (FrozenLake) & DQN setup (CartPole)
├── PyTorch_CNN.ipynb      # PyTorch CNN on MNIST classification (~98% acc)
└── Keras_CNN.ipynb        # Keras/TensorFlow CNN on CIFAR-10 classification

```

---

## Key Modules & Experiments

### 1. Quantum Simulation (`Qiskit`)

* Builds a 1-qubit quantum circuit with a Hadamard gate ($H$) to induce quantum superposition.
* Simulates 1,000 shots on `qiskit_aer.AerSimulator` and visualizes measurement state distributions.

### 2. Reinforcement Learning (`Gym` & `Stable-Baselines3`)

* **Q-Learning**: Tabular Bellman equation updates with $\epsilon$-greedy exploration decay on `FrozenLake-v1`.
* **Deep Q-Networks (DQN)**: Multi-layer perceptron neural policy network built in PyTorch for `CartPole-v1`.

### 3. Deep Learning (`PyTorch` & `TensorFlow/Keras`)

* **PyTorch (MNIST)**: 2D Convolutional neural network with max-pooling and cross-entropy loss, trained via Adam optimizer.
* **Keras (CIFAR-10)**: Sequential CNN classifier evaluated on multi-channel natural image categorization.

---

## Requirements & Environment Setup

This project requires **Python >= 3.12**.

### 1. Clone Repository

```bash
git clone <repository-url>
cd qc

```

### 2. Setup Virtual Environment

#### Using `uv` (Recommended)

```bash
# Sync dependencies directly from pyproject.toml and uv.lock
uv sync

```

#### Using standard `venv` & `pip`

```bash
python -m venv .venv

# On Linux/macOS:
source .venv/bin/activate
# On Windows:
.venv\Scripts\activate

pip install -e .

```

---

## Usage

### Run Entry Point Script

```bash
python main.py

```

### Launch Jupyter Notebooks

To interactively run the experiments:

```bash
jupyter lab
# or
jupyter notebook

```

Select the `.venv` kernel when executing the notebooks.

---

## Core Dependencies

| Package | Purpose |
| --- | --- |
| **`qiskit`** & **`qiskit-aer`** | Quantum circuits, gate operations, and simulator backend |
| **`torch`** & **`torchvision`** | PyTorch deep learning framework and datasets |
| **`tensorflow`** & **`keras`** | End-to-end deep learning and neural network APIs |
| **`gym`** & **`stable-baselines3`** | Reinforcement learning environments and baseline agents |
| **`numpy`** & **`matplotlib`** | Array computing and data/histogram visualization |

---

## License

This project is licensed under the MIT License - feel free to adapt and expand for research and experimentation.

```

```
