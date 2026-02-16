---
title: Future Scope
nav_order: 5
layout: default
---
# Future Scope

## Current Limitations

Although the project demonstrates successful cryptanalysis using simulated data and deep learning models, several limitations remain:

### 1. Synthetic Side-Channel Traces

The SPECK32 dataset is generated using a simulated Hamming Weight leakage model.  
Real hardware traces contain:

- measurement noise
- clock jitter
- voltage fluctuations
- device-specific leakage behaviour

These factors make real-world attacks significantly more challenging.

---

### 2. Fixed-Key Profiling Assumption

The current profiling setup assumes access to a device with a fixed and known key during training.  
In practical attack scenarios, the attacker may not have access to such a profiling device, leading to a mismatch between training and attack conditions.

---

### 3. Limited Cipher Coverage

The project focuses on:

- Vigenère (classical)
- DES (Feistel network)
- SPECK32 (ARX lightweight cipher)

Modern cryptographic deployments primarily use AES and other standardized block ciphers, which involve more complex leakage behaviour and larger key spaces.

---

### 4. CNN Architectural Constraints

Convolutional Neural Networks are effective at capturing local temporal features but have limitations:

- difficulty modelling long-range dependencies
- sensitivity to large desynchronization
- fixed receptive field

This restricts performance on highly misaligned traces.

---

### 5. Partial Key Recovery

The DES implementation targets S-box subkey recovery rather than full key reconstruction.  
Extending the attack to full key recovery requires combining multiple subkey predictions and performing key schedule inversion.

---

### 6. Energy Model Scalability

The energy-based classifier is currently applied to cipher classification and key hypothesis scoring.  
Scaling this approach to full key spaces of modern ciphers requires:

- efficient candidate pruning
- hierarchical search strategies
- improved energy function generalization

---

## Proposed Future Work

### 1. Real Hardware Side-Channel Acquisition

Collect power traces from:

- microcontrollers
- FPGA implementations

This will enable evaluation of the models under realistic noise and leakage conditions.

---

### 2. AES Side-Channel Analysis

Extend the framework to AES, which introduces:

- SubBytes nonlinear leakage
- MixColumns diffusion
- larger key size

This will test the scalability of CNN and energy-based models.

---

### 3. Transformer-Based Leakage Modelling

Replace CNNs with Transformer architectures to:

- capture long-range temporal dependencies
- handle large desynchronization
- improve feature learning across entire traces

---

### 4. Countermeasure Evaluation

Implement and analyse common hardware countermeasures:

- masking
- hiding
- shuffling

Study how deep learning models can adapt to protected implementations.

---

### 5. Full Key Recovery Pipeline

Combine:

- multiple subkey predictions
- key schedule inversion
- probabilistic key search

to achieve complete key reconstruction for DES and AES.

---

### 6. Energy-Guided Key Search

Use the energy model for:

- hierarchical key candidate pruning
- beam search over key space
- reinforcement learning guided cryptanalysis

This will enable efficient exploration of large key spaces.

---

### 7. Transfer Learning for Side-Channel Attacks

Train models on one device and adapt them to another using:

- domain adaptation
- fine-tuning
- few-shot learning

This addresses the profiling mismatch problem.

---

## Research Impact

Future work will move the project from simulated cryptanalysis to practical, real-world attack scenarios and improve the scalability of machine learning based side-channel analysis.
