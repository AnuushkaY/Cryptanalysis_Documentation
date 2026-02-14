---
title: Methodology
nav_order: 2
layout: default
---

# Methodology

## Cipher Classification

We train a deep learning model on ciphertext samples generated from:

- AES  
- DES  
- Vigenère  
- Speck32  

The model learns statistical signatures present in ciphertext without using encryption keys.

## Model Pipeline

Ciphertext → Tokenization → Neural Network → Cipher Prediction

## Evaluation Metric

Classification accuracy across all cipher classes.
