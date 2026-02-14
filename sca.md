---
title: Side-Channel Analysis
nav_order: 3
layout: default
---

# Side-Channel Analysis

## Objective

Train a CNN on DES power traces to recover key-dependent leakage.

## Leakage Model

Hamming Weight of intermediate DES values.

## CNN Pipeline

Power Trace → Convolution → Dense → Key Probability

## Metric

Key Rank vs Number of Traces.
