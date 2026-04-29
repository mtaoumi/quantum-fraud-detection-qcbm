# Quantum Fraud Detection with QCBM

> Quantum Circuit Born Machine (QCBM) for unsupervised anomaly detection in financial transactions using hybrid quantum-classical learning.

---

## Academic Supervision

This project was completed under the supervision of Dr. Fouad Mohammed Abbou as part of academic research work.

---

## Overview

Financial fraud remains a major challenge for institutions because fraudulent transactions are extremely rare and continuously evolving. Traditional supervised models rely on labeled fraud examples, which are limited and may not generalize to new attack patterns.

This project explores the use of a **Quantum Circuit Born Machine (QCBM)** as a generative quantum model to learn the distribution of normal transactions and detect anomalies as low-probability events.

Two data representations were evaluated:

- **PCA + QCBM**
- **VAE + QCBM**

The objective was to compare how feature representation affects quantum anomaly detection performance.

---

## Research Goals

- Learn normal transaction behavior using a quantum generative model  
- Detect suspicious transactions without relying on fraud labels  
- Compare linear and non-linear feature compression methods  
- Evaluate hybrid quantum-classical workflows for fraud detection  

---

## Dataset

This work uses the **Credit Card Fraud Detection Dataset**, containing:

- **284,807 transactions**
- **492 fraud cases**
- Highly imbalanced real-world fraud scenario

Because fraud cases represent less than 0.2% of the data, anomaly detection is particularly challenging.

---

## Methodology

### 1. Data Preprocessing

- Log transformation on transaction amount  
- Feature normalization  
- Dimensionality reduction to 2D latent space  

### 2. Feature Representations

#### PCA + QCBM
Principal Component Analysis was used to project features into 2 dimensions.

#### VAE + QCBM
A Variational Autoencoder was trained on normal transactions to learn a compact latent representation.

### 3. Quantum Model

The QCBM architecture includes:

- **8 qubits**
- **8 variational layers**
- Trainable **Ry rotation gates**
- Circular **CNOT entanglement**
- **256 output states** matching a 16×16 probability grid

---

## Key Findings

### Strong Performance on Separable Data

When fraud and normal samples were clearly separated in latent space, QCBM performed well.

### Main Limitation: Overlap

On the full dataset, fraud transactions overlapped heavily with normal transactions, making anomaly detection difficult.

### Important Insight

The main bottleneck was **data representation**, not the quantum circuit itself.

---

## Repository Contents

```text
.
├── gate_efficient_qcbm.py
├── QCBM_Code.ipynb
├── QCBM_Hybrid_VAE.ipynb
├── QCBM_Refactored_PCA.ipynb
├── Quantum_financial.pdf
├── paper.docx
├── report.docx
└── README.md
