Temporal Convolutional Network (TCN) for Multihorizon Instability Prediction

This repository contains a Temporal Convolutional Network (TCN)–based pipeline for modeling multimodal time-series data and predicting future instability events using a multi-horizon formulation. The workflow is designed for physiological and biomechanical signals collected during locomotion and balance tasks and emphasizes temporal structure preservation rather than heavy feature aggregation.

The pipeline supports data preprocessing, dataset construction, model training, inference, and evaluation, and is suitable for both offline analysis and future real-time deployment.

Project Overview

The core objective of this project is to predict future instability/misstep events from continuous time-series signals by:

Preserving temporal dynamics at a fixed sampling rate (e.g., 50 Hz)

Using multi-horizon binary labels instead of a single future point

Handling missing data and temporal gaps robustly

Supporting reproducible training and evaluation workflows

This approach is particularly relevant for:

Human balance and gait studies

Neuroergonomics and sensorimotor research

Assistive device and exoskeleton control systems
