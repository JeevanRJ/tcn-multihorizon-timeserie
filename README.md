# Temporal Convolutional Network (TCN) for Multihorizon Instability Prediction

This repository contains a **Temporal Convolutional Network (TCN)–based pipeline** for modeling multimodal time-series data and predicting **future instability events** using a **multi-horizon formulation**. The workflow is designed for physiological and biomechanical signals collected during locomotion and balance tasks and emphasizes **temporal structure preservation** rather than heavy feature aggregation.

The pipeline supports **data preprocessing, dataset construction, model training, inference, and evaluation**, and is suitable for both **offline analysis** and **future real-time deployment**

---

## Project Overview

The core objective of this project is to predict **future instability/misstep events** from continuous time-series signals by:

- Preserving temporal dynamics at a fixed sampling rate (e.g., 50 Hz)
- Using **multi-horizon binary labels** instead of a single future point
- Handling missing data and temporal gaps robustly
- Supporting reproducible training and evaluation workflows

This approach is particularly relevant for:
- Human balance and gait studies  
- Neuroergonomics and sensorimotor research  
- Assistive device and exoskeleton control systems  
- Real-time human–machine interfaces  

---

## Repository Structure

```
.
├── Preprocess_shared.ipynb
├── Build_tcn_data_future_multihorizon_missteps.ipynb
├── Train_and_Save_TCNModel.ipynb
└── README.md
```

---

## Notebook Descriptions

### 1. Preprocess_shared.ipynb
Shared preprocessing utilities used across the entire pipeline.

**Key functionality**
- Resampling multimodal streams to a common frequency (e.g., 50 Hz)
- Temporal alignment across signals
- Handling missing samples and gaps
- Standardized normalization and windowing logic

---

### 2. Build_tcn_data_future_multihorizon_missteps.ipynb
Constructs the **TCN-ready dataset** with **multi-horizon labels**.

**Key functionality**
- Sliding-window segmentation of continuous trials
- Generation of binary labels at multiple future horizons
- Trial-aware dataset construction
- Export to `.npz` format for efficient training

---

### 3. Train_and_Save_TCNModel.ipynb
Trains the **multi-output TCN model** and saves the best checkpoint.

**Key functionality**
- TCN architecture definition
- Class imbalance handling using `pos_weight`
- Early stopping based on validation loss
- Saving model weights, feature ordering, and split metadata

---


## Key Design Choices

- Temporal modeling over feature aggregation
- Multi-horizon early warning formulation
- Reproducible training and evaluation
- Real-time compatible preprocessing logic

---

## Requirements (Typical)

- Python ≥ 3.9  
- PyTorch  
- NumPy, SciPy, pandas  
- Matplotlib / Seaborn  

---

## Intended Use

This repository is intended for **research and prototyping** purposes.  
Additional validation and engineering are required for safety-critical or embedded deployment.

---

## License

This project is released under the **MIT License**.
