---
title: Vigenère Cipher
nav_order: 3
layout: default
---
# Classical Cryptanalysis: Vigenère Cipher

## Background

The Vigenère cipher is a polyalphabetic substitution cipher defined as:

Ci = (Pi + Ki) mod 26

Its security depends on the secrecy of the key length and key characters.

---

## Key Length Detection

Two statistical techniques are used:

### Index of Coincidence (IC)

The IC measures the probability that two randomly selected letters are identical. English text has a higher IC than random text. By computing IC for different assumed key lengths, the correct key length can be estimated.

### Kasiski Examination

Repeated ciphertext patterns reveal periodic spacing. The greatest common divisor of these spacings provides candidate key lengths.

---

## Frequency Analysis

After determining the key length, the ciphertext is divided into columns. Each column behaves like a Caesar cipher. By comparing letter frequency distributions with English frequencies, the shift for each column is determined and the key is reconstructed.

---

## Outcome

- Successful recovery of the key
- Demonstration of classical statistical cryptanalysis
- Baseline comparison for modern machine learning based attacks
