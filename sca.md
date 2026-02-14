---
layout: default
title: Side-Channel Analysis
nav_order: 3
---

# Side-Channel Analysis

## Objective

Train a CNN on DES power traces to recover key-dependent leakage.

---

## Leakage Model

We assume **Hamming Weight leakage** of intermediate DES values.

---

## CNN Pipeline

```text
Power Trace → Convolution → Dense → Key Probability
