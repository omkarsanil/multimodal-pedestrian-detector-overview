# Multimodal Pedestrian Detection System

## Overview

A research-oriented two-stage multimodal pedestrian detection pipeline designed for robust low-visibility and nighttime detection scenarios using RGB-Thermal fusion.

The system combines:

* Thermal anomaly proposal generation using a masked convolutional autoencoder
* RGB-Thermal contrastive verification using a dual-stream MoCo encoder
* Centroid-based similarity scoring for pedestrian verification
* Non-Maximum Suppression (NMS) for final detection refinement

---

## Architecture

Thermal Image
      ↓
Masked Thermal Autoencoder
      ↓
Anomaly Proposal Generation
      ↓
RGB + Thermal Crop Extraction
      ↓
Dual-Stream MoCo Encoder
      ↓
Contrastive Embedding Similarity
      ↓
Centroid-Based Verification
      ↓
Non-Maximum Suppression (NMS)
      ↓
Final Pedestrian Detections

## Key Features

* Multimodal RGB-Thermal fusion
* Thermal anomaly-based proposal generation
* Contrastive representation learning
* Low-visibility pedestrian detection
* Two-stage detection pipeline
* Centroid similarity verification
* Research-focused modular architecture

---

## Methodology

### Stage 1 — Thermal Proposal Generation

A masked thermal convolutional autoencoder is trained exclusively on background thermal information. During inference, reconstruction error is used to localize anomalous pedestrian regions.

### Stage 2 — Multimodal Verification

Candidate regions are verified using a dual-stream RGB-Thermal MoCo encoder trained through contrastive learning.

Positive embeddings are aggregated into a centroid representation, and cosine similarity scoring is used for final pedestrian verification.

---

## Dataset

Primary dataset used:

* LLVIP Dataset
  
---

### Detection Performance





---

## Result Visualizations


<img width="1280" height="1024" alt="result_1774605810597" src="https://github.com/user-attachments/assets/9ff848f5-bad3-4513-b7b2-ff852980abf7" />


<img width="1280" height="1024" alt="result_1772632232" src="https://github.com/user-attachments/assets/fbc2431e-90fc-49b4-ae2d-86ff1a49081c" />


<img width="1280" height="1024" alt="result_1774606263311" src="https://github.com/user-attachments/assets/6e0fd2ae-c558-4199-b9f5-a136335b1d53" />


<img width="1280" height="1024" alt="result_1774628420722" src="https://github.com/user-attachments/assets/341ff33e-d181-48f7-9a75-758c56f3d99a" />


## Tech Stack

* Python
* PyTorch
* OpenCV
* NumPy
* Matplotlib

## Research Focus

This project explores robust multimodal pedestrian detection under challenging environmental conditions through anomaly localization and contrastive multimodal representation learning.
