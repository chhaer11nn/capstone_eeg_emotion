# EEG-based Emotion Recognition with Cross-Modal Learning

## Overview

This project explores emotion recognition using EEG signals under visual and olfactory stimuli.
The main goal is to infer emotional responses to olfactory stimuli by leveraging EEG data collected during visual stimulus experiments.

---

## Key Idea

* Train emotion classification models using **visual stimulus EEG**
* Apply the trained models to **olfactory stimulus EEG**
* Perform **automated feature-model optimization** to find the best configurations

---

## Experimental Setup

* Subjects: 5 participants
* EEG Device: 19-channel system
* Visual Stimuli: Positive / Negative images
* Olfactory Stimuli: Multiple scents (e.g., lavender, etc.)
* Protocol: Rest (10s) / Task (10s)

---

## Pipeline

```
EEG Signal
 → Preprocessing
 → Feature Extraction
 → Model Training (Visual EEG)
 → Evaluation (Olfactory EEG)
 → Automated Optimization
```

---

## Preprocessing

* Band-pass filtering (0.5–55 Hz)
* Downsampling (250 Hz)
* CAR (Common Average Referencing)
* Task segment extraction (1–9 seconds)
* Sliding window (2s window, 1s overlap)

---

## Feature Extraction

* Power Spectral Density (PSD, Welch method)
* Differential Entropy (DE)
* DASM (Differential Asymmetry)
* RASM (Rational Asymmetry)

---

## Models

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Support Vector Machine (SVM)
* Random Forest
* XGBoost

---

## Automated Experiments

* Channel / Feature combinations: 86
* Frequency bands: 6
* Normalization methods: 3
* Models: 6
* Total combinations: **9,288**

---

## Results

* Performance improved with extended experimental conditions
* Stable accuracy achieved across multiple subjects
* Certain feature-model combinations showed consistently strong performance

---

## Repository Structure

```
automation/   # Experiment and automation code
results/      # Graphs and CSV results
docs/         # Paper, poster, presentation materials
```

---

## Contribution

* Designed EEG preprocessing pipeline
* Implemented feature extraction (PSD, DE, DASM, RASM)
* Conducted automated experiment search
* Analyzed and visualized experimental results

---

## Notes

* Raw EEG data is not included due to privacy and institutional restrictions
