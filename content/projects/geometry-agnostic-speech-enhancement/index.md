---
title: "Geometry-Agnostic Multichannel Speech Enhancement"
date: 2024-01-01
summary: "A geometry-agnostic multichannel speech enhancement framework that avoids array-specific retraining while reducing computational complexity by 25%-33.7%."
tags:
  - Speech Enhancement
  - Microphone Array
  - Deep Learning
  - Edge AI Efficiency
  - ICASSP 2026
tech_stack:
  - PyTorch
  - Python
  - Eigenbeam Transform
  - Multichannel Audio
featured: true
share: false
weight: 1
image:
  filename: cover.jpg
  preview_only: true
status: "Ongoing"
role: "PhD Researcher"
duration: "Jan 2024 - Present"
team_size: 4
highlights:
  - "Matched or outperformed strong baselines on PESQ and STOI under randomized array settings"
  - "Reduced GFLOPS by 25%-33.7% for edge-friendly deployment"
---

## Context and Objective

Most multichannel speech enhancement models are strongly coupled to microphone geometries seen during training.  
This project addresses that bottleneck by developing a geometry-agnostic framework that generalizes across array layouts while remaining computationally efficient.

In one sentence: I designed a deployable enhancement pipeline that improves cross-array robustness without sacrificing efficiency.

## My Contributions

- Built a beampattern-driven Spatial Filter Bank (SFB) design workflow for principled channel selection  
- Developed an Eigenbeam-domain representation for geometry-agnostic feature extraction  
- Proposed an efficient architecture that replaces heavy attention modules with lightweight recurrent modeling

## Technical Approach

### 1) Spatial Filter Bank Design

I designed SFB configurations using spatial coverage analysis to preserve directional information while minimizing redundant channels.

### 2) Geometry-Agnostic Representation

Raw multichannel audio is projected into an orthogonal Eigenbeam-domain feature space, enabling consistent model behavior across unseen planar array geometries.

### 3) Efficient Enhancement Architecture

To reduce computational burden, I replaced heavy MHSA components with lightweight LSTM blocks and introduced a Multi-order Spatial Encoder Network (MSEN) for parallel spatial feature modeling.

## Results and Validation

Under fully randomized planar array settings, the method matched or exceeded strong baselines on **PESQ** and **STOI**, while reducing **GFLOPS by 25%-33.7%**.  
These results indicate improved portability to heterogeneous edge devices with limited compute budgets.

## System Architecture

<a href="framework.jpg" target="_blank" rel="noopener">
  <img src="framework.jpg" alt="End-to-End Geometry-Agnostic Pipeline" />
</a>

*Figure 1. SFB-LSTM pipeline: arbitrary array inputs are transformed into geometry-invariant features and enhanced with a lightweight recurrent model.*

## Spatial Coverage Analysis

<div style="display:flex; gap:1rem; flex-wrap:wrap;">
  <a href="beam_I3.png" target="_blank" rel="noopener">
    <img src="beam_I3.png" alt="3-channel beampattern coverage" style="max-width:48%; min-width:260px;" />
  </a>
  <a href="beam_I5.png" target="_blank" rel="noopener">
    <img src="beam_I5.png" alt="5-channel beampattern oversampling" style="max-width:48%; min-width:260px;" />
  </a>
</div>

*Figure 2. The 3-channel configuration (left) provides efficient spatial coverage, while the 5-channel setting (right) introduces oversampling and feature redundancy.*

## Research-Oriented Value

This work highlights my strengths in bridging acoustic theory, deep learning design, and practical deployment constraints.  
It emphasizes reproducible methodology and hardware-transferable modeling rather than device-specific optimization.
