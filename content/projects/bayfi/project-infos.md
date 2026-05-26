---
title: Project's Infos & Updates
description: This page provides detailed information about the Bay-Fi project, including its objectives, methodology, and ongoing research activities.
date: 2025-10-27
weight: 2

toc: true
build:
  list: local
  render: always
---

## Abstract

Structural Health Monitoring (SHM) and operational modal analysis rely on accurate identification of modal frequencies from vibration signals. However, in many practical scenarios, acquiring high-frequency signals is constrained by hardware limitations, energy consumption, or data transmission bandwidth — making **Sub-Nyquist sampling** a key challenge.

**Bay-Fi** (Bayesian Frequency Identification) addresses this challenge by introducing a novel general method that enables **direct identification of the main modal frequency** without requiring:
- Signal reconstruction
- Any prior tuning of hyperparameters

The proposed approach employs a **Bayesian framework** to optimize a curve-fitting algorithm applied to highly under-sampled and randomly acquired vibration signals. This allows robust frequency estimates even when conventional methods would fail due to aliasing or insufficient data.

## Methodology

The core idea of Bay-Fi is to reformulate frequency identification as a **Bayesian optimization problem**. Rather than attempting to reconstruct the full signal from sparse measurements, the method directly estimates the dominant frequency by fitting a parametric model to the available samples in a probabilistic framework.

Key features of the method:
- **Parameter-free**: no prior knowledge or manual tuning required
- **Robust to under-sampling**: works with signals sampled well below the Nyquist rate
- **Random sampling compatible**: handles non-uniform and randomly acquired samples
- **Scalable**: applicable to single-channel and multi-channel measurements

## AI-generated Podcast

Ever wondered what Bay-Fi would sound like if two enthusiastic hosts explained it over coffee? Wonder no more. [Jari Vepsäläinen](https://research.aalto.fi/en/persons/jari-veps%C3%A4l%C3%A4inen/) (Aalto University, Finland) fed the paper to an AI and out came this surprisingly engaging podcast episode — Bayesian inference, Sub-Nyquist sampling, and all. Give it a listen!

<iframe src="https://drive.google.com/file/d/1lN-NvHyULYmEGEZbyHjiGe6cebQHBFlp/preview" width="100%" height="80" allow="autoplay" style="border:none; border-radius:8px;"></iframe>

## Updates

| Date | Update |
| :--- | :----- |
| Oct 2025 | Project launched, initial development of the Bayesian framework |
