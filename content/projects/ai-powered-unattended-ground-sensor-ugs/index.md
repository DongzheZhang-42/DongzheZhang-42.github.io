---
title: "Acoustic-Vibration Unattended Ground Sensor (UGS)"
date: 2021-05-01
summary: "A low-power wireless perimeter monitoring project that combines acoustic-vibration sensing, edge AI inference, and embedded system integration for long-duration unattended operation."
tags:
  - Edge UGS
  - Edge AI
  - Embedded Systems
  - Acoustic-Vibration Fusion
  - Low Power
tech_stack:
  - Embedded C
  - STM32
  - PyTorch
  - LoRa
  - DSP / STFT
featured: true
share: false
weight: 4
status: "Completed"
role: "Core Algorithm Designer & Embedded Systems Engineer"
duration: "May 2021 - Oct 2024"
team_size: 5
highlights:
  - "Designed and deployed an end-to-end acoustic-vibration detection pipeline on STM32 edge devices"
  - "Implemented low-power state-machine execution with robust wireless reporting for unattended deployment"
image:
  filename: 0ecd9b67-44ad-48c4-9a5e-46aabd775368.png
  preview_only: true
---

## Context and Objective

This project targeted unattended perimeter monitoring under strict constraints on power, computation, and wireless reliability.  
I deployed an AI detection model on STM32 chips and achieved efficient target detection performance.  
The objective was to build a deployable edge-intelligence pipeline that remains stable during long-duration field operation.

## My Contributions

- Designed frequency-domain features and a lightweight model architecture for resource-constrained MCUs  
- Implemented embedded firmware for acquisition, inference triggering, communication, and power-state transitions  
- Designed a multi-node communication protocol to support inter-node collaboration and reliable platform-side reporting  
- Built an integrated validation workflow from node-level performance to multi-node field operation

## Technical Approach

### 1) Edge Feature and Model Design

At the feature level, I built a time-frequency representation based on short-time spectral energy distribution to improve sensitivity to target behavior, and used normalization and windowing strategies to increase robustness in complex environments.  
At the model level, I adopted a compact `Conv -> ReLU -> MaxPool -> FC` structure to balance detection accuracy and computational efficiency on STM32, meeting real-time edge execution requirements.

### 2) Low-Power Embedded Execution

On the embedded side, I implemented continuous ADC sampling, DMA-based data transfer, and interrupt-driven wake-up control.  
The state-machine firmware design reduced idle overhead and enabled long-term unattended operation while preserving event responsiveness.

## Deployment and Validation

| Metric | Result | Engineering Implication |
| --- | --- | --- |
| Edge Inference | 128-point STFT + lightweight CNN | Feasible real-time inference on constrained MCU resources |
| Detection Quality | Walk recall > 90% at 12-24 m | Reliable perception in outdoor conditions |
| Power Behavior | Long unattended runtime | State-machine control lowers average consumption |
| System-Level Operation | Real-time node-to-platform reporting | Supports scalable multi-node deployment |

### Interface and Runtime Monitoring

<a href="ugs-dashboard.png" target="_blank" rel="noopener">
  <img src="ugs-dashboard.png" alt="UGS System Interface" />
</a>

*Figure 1. End-to-end workflow from on-device inference to event reporting and status monitoring.*

### Embedded Hardware Platform

<a href="dd3d9b98-8449-42d4-a748-a93840fa2cc6.png" target="_blank" rel="noopener">
  <img src="dd3d9b98-8449-42d4-a748-a93840fa2cc6.png" alt="UGS Mainboard" />
</a>

*Figure 2. Hardware integration of MCU, wireless module, and sensing interfaces for low-power operation.*

### Field Deployment

<a href="331768ef-60c7-440b-8a27-fc486140203f.png" target="_blank" rel="noopener">
  <img src="331768ef-60c7-440b-8a27-fc486140203f.png" alt="UGS Field Deployment" />
</a>

*Figure 3. Multi-node outdoor deployment used for long-duration validation and robustness testing.*

## Related Patent

- [Wireless low-power consumption ground defense monitoring devices (CN218511891U)](https://patents.google.com/patent/CN218511891U/en?oq=CN218511891U)
