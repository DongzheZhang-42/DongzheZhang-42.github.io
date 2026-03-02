---
title: "Distributed Sound Event Localization and Detection (SELD) System"
date: 2020-10-01
summary: "A WASN-based distributed SELD project for robust outdoor localization and classification, integrating edge hardware design, multimodal learning, and real-world validation."
tags:
  - Distributed SELD
  - Acoustic Sensing
  - Sound Source Localization
  - Distributed Systems
  - Edge AI
tech_stack:
  - Microphone Arrays
  - Python
  - MATLAB
  - Deep Learning
  - Embedded C
  - STM32F4
featured: true
share: false
weight: 2
status: "Completed"
role: "Technical Co-founder & Acoustic Engineer"
duration: "Oct 2020 - Oct 2022"
team_size: 5
highlights:
  - "Designed a WASN-based SELD pipeline for outdoor localization and classification"
  - "Implemented synchronized edge sensing nodes with real-time feature extraction"
  - "Produced 3 peer-reviewed publications spanning IEEE, Springer, and Elsevier venues"
image:
  filename: IMG_3415.jpg
  preview_only: true
---

## Context and Objective

This project aimed to build a distributed acoustic perception system based on a Wireless Acoustic Sensor Network (WASN) for complex outdoor environments.  
The goal was to jointly localize and classify sound events with strong robustness to interference and deployment variability.

In one sentence: I developed and validated a full-stack SELD system from synchronized edge sensing hardware to multimodal deep learning inference.

## My Contributions

- Designed distributed sensing architecture, including edge acquisition, synchronization, and feature-extraction pathways  
- Built multimodal SELD learning models for joint sound event classification (SEC) and source localization (SSL)  
- Organized real-world field evaluations and failure-case analysis against conventional localization baselines

## Technical Approach

### 1) Edge Hardware and Time Synchronization

I developed array nodes around **STM32F4 + AD7606**, with **DMA double buffering** for continuous audio acquisition.  
To support distributed localization, I implemented timestamping with **GPS PPS** alignment across nodes.  
I also deployed edge-side feature extraction (SoundMap and GTGram) to reduce transmission load and central compute pressure.

<div style="display:flex; gap:1rem; flex-wrap:wrap;">
  <figure style="flex:1; min-width:260px; margin:0;">
    <a href="hw_1.png" target="_blank" rel="noopener">
      <img src="hw_1.png" alt="Edge node dataflow from microphones to network interface" />
    </a>
    <figcaption style="font-size:0.9rem; opacity:0.85;">Figure 1. Hardware dataflow: microphone array to edge processing and network output.</figcaption>
  </figure>
  <figure style="flex:1; min-width:260px; margin:0;">
    <a href="hw_2.png" target="_blank" rel="noopener">
      <img src="hw_2.png" alt="Distributed timestamp and PPS synchronization design" />
    </a>
    <figcaption style="font-size:0.9rem; opacity:0.85;">Figure 2. Distributed timestamping and PPS-based synchronization.</figcaption>
  </figure>
</div>

### 2) Multimodal SELD Learning Architecture

I designed a multimodal architecture that fuses frequency, temporal, and spatial cues.  
The model combines CNN-based representation learning with Transformer-style attention and a multitask objective for joint SEC/SSL optimization.

<figure style="margin:1rem 0 0 0;">
  <a href="network.png" target="_blank" rel="noopener">
    <img src="network.png" alt="Multimodal SELD network architecture" />
  </a>
  <figcaption style="font-size:0.9rem; opacity:0.85;">Figure 3. Multimodal SELD model with parallel encoders and joint SEC/SSL learning.</figcaption>
</figure>

<figure style="margin:1rem 0 0 0;">
  <a href="structure.png" target="_blank" rel="noopener">
    <img src="structure.png" alt="Distributed SELD system architecture overview" />
  </a>
  <figcaption style="font-size:0.9rem; opacity:0.85;">Figure 4. System-level architecture of distributed sensing nodes and central fusion.</figcaption>
</figure>

## Deployment and Validation

The system was evaluated under practical outdoor interference rather than only controlled benchmarks.

### Interference-Robust Localization Case

In a five-node setup, the target class was **Siren**, while **Dog Bark** near node A5 acted as strong interference.

- Classical methods showed large localization bias:  
  - PLSE: up to **22.1 m** error  
  - FUZZY: up to **13.3 m** error
- The proposed method maintained **3.7 m** localization error in the same condition

<figure style="margin:1rem 0 0 0;">
  <a href="failure.png" target="_blank" rel="noopener">
    <img src="failure.png" alt="Failure case comparison under strong interference" />
  </a>
  <figcaption style="font-size:0.9rem; opacity:0.85;">Figure 5. Comparative failure case showing robustness under strong nearby interference.</figcaption>
</figure>

<div style="display:flex; gap:1rem; flex-wrap:wrap; margin-top:1rem;">
  <figure style="flex:1; min-width:260px; margin:0;">
    <a href="T11.png" target="_blank" rel="noopener">
      <img src="T11.png" alt="Real-world test scene T11" />
    </a>
    <figcaption style="font-size:0.9rem; opacity:0.85;">Figure 6. Field test scene T11.</figcaption>
  </figure>
  <figure style="flex:1; min-width:260px; margin:0;">
    <a href="T21.png" target="_blank" rel="noopener">
      <img src="T21.png" alt="Real-world test scene T21" />
    </a>
    <figcaption style="font-size:0.9rem; opacity:0.85;">Figure 7. Field test scene T21.</figcaption>
  </figure>
</div>

## Field Deployment Gallery

<div style="display:flex; gap:1rem; flex-wrap:wrap;">
  <figure style="flex:1; min-width:260px; margin:0;">
    <a href="IMG_3348.JPG" target="_blank" rel="noopener">
      <img src="IMG_3348.JPG" alt="SELD field deployment snapshot 1" />
    </a>
    <figcaption style="font-size:0.9rem; opacity:0.85;">Figure 8. On-site setup and validation context.</figcaption>
  </figure>
  <figure style="flex:1; min-width:260px; margin:0;">
    <a href="IMG_3415.jpg" target="_blank" rel="noopener">
      <img src="IMG_3415.jpg" alt="SELD field deployment snapshot 2" />
    </a>
    <figcaption style="font-size:0.9rem; opacity:0.85;">Figure 9. Real-world sensing environment and node placement.</figcaption>
  </figure>
  <figure style="flex:1; min-width:260px; margin:0;">
    <a href="IMG_3425.jpg" target="_blank" rel="noopener">
      <img src="IMG_3425.jpg" alt="SELD field deployment snapshot 3" />
    </a>
    <figcaption style="font-size:0.9rem; opacity:0.85;">Figure 10. Field-test execution and system operation state.</figcaption>
  </figure>
</div>

## Research-Oriented Value

This project demonstrates end-to-end capability across distributed sensing hardware, synchronization, multimodal learning, and in-situ robustness evaluation.  
It also generated a coherent publication trail from system-level deployment to methodological advances and robustness training in peer-reviewed venues.

## Selected Publications and Patent

- [Sound Event Localization and Classification using Wireless Acoustic Sensor Networks in Outdoor Environments](https://ieeexplore.ieee.org/document/11192195)
- [Multiple sound sources localization using sub-band spatial features and attention mechanism](https://link.springer.com/article/10.1007/s00034-024-02925-6)
- [Synthesis-to-real robust training for enhanced sound event localization and detection using dynamic kernel convolution networks](https://www.sciencedirect.com/science/article/abs/pii/S0003682X24004183)
- [Air sonar array device for acousto-optic linkage monitoring and positioning (CN218003722U)](https://patents.google.com/patent/CN218003722U/en?oq=CN218003722U)
