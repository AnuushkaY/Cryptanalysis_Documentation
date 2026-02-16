---
title: Introduction
nav_order: 1
layout: default
---

# Energy-Based and Neurosymbolic methods for advanced Cryptanalysis

![alt text](image-1.png)
## Introduction

### Overview

Cryptanalysis is the study of analysing cryptographic systems in order to recover secret information without prior knowledge of the key. While modern cryptographic algorithms are mathematically secure against classical attacks, practical implementations often leak information through physical side channels such as power consumption, timing behaviour, and electromagnetic radiation.

This project investigates cryptanalysis using a multi-layered approach that combines:

- Classical statistical cryptanalysis
- Side-channel leakage modelling
- Deep learning based profiling attacks
- Energy-based neurosymbolic key ranking

The objective is to demonstrate how machine learning techniques can exploit statistical dependencies between leakage traces and intermediate cryptographic computations to recover secret keys.

---

Modern block ciphers are designed to resist structural cryptanalysis. However, physical implementations of these algorithms exhibit data-dependent power consumption. This leakage can be modelled and analysed to recover secret keys.

The key challenges addressed in this project are:

- modelling realistic side-channel leakage
- learning leakage patterns using neural networks
- ranking key hypotheses using energy-based scoring

---

### Objectives

- Implement classical Vigenère cryptanalysis using statistical methods
- Generate synthetic side-channel traces using the Hamming Weight model
- Train CNN-based profiling attacks for key recovery
- Recover DES subkeys using intermediate value classification
- Develop an energy-based model for key candidate ranking

---

### Tools and Technologies

- Python
- PyTorch
- NumPy
- HDF5 dataset format
- Convolutional Neural Networks (CNNs)
