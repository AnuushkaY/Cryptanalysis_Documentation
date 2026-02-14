---
title: Methodology
nav_order: 2
layout: default
---

# Methodology

## Cipher Classification

Model trained on ciphertext from AES, DES, Vigenère, and Speck32.

Pipeline:

```mermaid
flowchart LR
  A[Ciphertext] --> B[Neural Network]
  B --> C[Cipher Prediction]
```

<script src="https://cdnjs.cloudflare.com/ajax/libs/mermaid/10.4.0/mermaid.min.js"></script>
<script>mermaid.initialize({startOnLoad:true});</script>

Metric: Classification accuracy.
