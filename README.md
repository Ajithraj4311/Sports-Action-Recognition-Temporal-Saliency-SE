# Enhancing Sports Action Recognition With Temporal Saliency and Squeeze-Excitation Networks

## Overview

This repository contains the official implementation of the research paper:

**Enhancing Sports Action Recognition With Temporal Saliency and Squeeze-Excitation Networks**

The proposed framework integrates:

- Temporal Saliency Extraction
- Optical Flow-Based Motion Analysis
- Squeeze-and-Excitation (SE) Networks
- Inception-V3 Deep Learning Architecture

for accurate sports action recognition from video sequences.

The framework focuses on identifying the most informative temporal regions within sports videos and enhancing feature representations through channel attention mechanisms.

---

## Related Publication

**Title:**

Enhancing Sports Action Recognition With Temporal Saliency and Squeeze-Excitation Networks

**Journal:**

The Visual Computer

---

## Repository Structure

```text
Sports-Action-Recognition-Temporal-Saliency-SE
│
├── train_sports_action_recognition.py
├── requirements.txt
├── README.md
│
├── datasets
│   └── dataset_download_link.txt
│
├── outputs
│   ├── figures
│   ├── tables
│   └── models
│
├── sample_results
│   ├── confusion_matrix.png
│   ├── roc_curve.png
│   ├── precision_recall_curve.png
│   ├── model_accuracy.png
│   └── model_loss.png
│
└── LICENSE
```

---

## Dataset

### UCF101 Action Recognition Dataset

Official Dataset Website:

https://www.crcv.ucf.edu/data/UCF101.php

### Sports Classes Used

- Baseball Pitch
- Basketball Shooting
- Billiards Shot
- Cricket Shot
- Floor Gymnastics
- Long Jump

---

## Data Preprocessing

The following preprocessing steps are performed:

### 1. Frame Extraction

- Uniform frame sampling
- 16 frames extracted per video

### 2. Normalization

```python
frame = frame.astype(np.float32) / 255.0
```

### 3. Frame Resizing

```python
299 × 299
```

### 4. Median Filtering

```python
cv2.medianBlur(frame, 3)
```

### 5. Temporal Saliency Extraction

- Optical Flow Computation
- Motion Saliency Map Generation
- Saliency-Based Feature Enhancement

---

## Proposed Architecture

### Temporal Saliency Module

Input Video

↓

Frame Extraction

↓

Optical Flow

↓

Motion Saliency Detection

↓

Saliency Map Generation

↓

Salient Frame Representation

---

### Classification Module

Input Frame

↓

Inception-V3 Backbone

↓

Squeeze-and-Excitation Block

↓

Global Average Pooling

↓

Fully Connected Layers

↓

Softmax Classification

---

## Software Requirements

### Python Version

```text
Python 3.10+
```

### Libraries

```text
TensorFlow
Keras
OpenCV
NumPy
Pandas
Matplotlib
Scikit-learn
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Training

Run:

```bash
python train_sports_action_recognition.py
```

Training outputs:

- Accuracy Curve
- Loss Curve
- Confusion Matrix
- ROC Curve
- Precision-Recall Curve
- Performance Tables

are automatically saved inside:

```text
outputs/
```

---

## Testing

The best model is automatically saved as:

```text
outputs/models/SE_InceptionV3_Temporal_Saliency.h5
```

Prediction can be performed using:

```python
model.predict(test_data)
```

---

## Performance Results

| Metric | Value (%) |
|----------|----------|
| Accuracy | 98.83 |
| Precision | 98.48 |
| Recall | 98.37 |
| F1-Score | 98.37 |

---

## Generated Outputs

### Figures

- Performance Metrics
- Confusion Matrix
- FPR vs FNR
- ROC Curve
- Precision-Recall Curve
- Training Accuracy
- Training Loss

### Tables

- Dataset Distribution
- Train/Test Split
- Performance Metrics
- Classification Report
- ROC-AUC Results
- Precision-Recall AUC Results
- Software Configuration

---

## Hardware Configuration

Example Experimental Setup

```text
CPU      : Intel Core i7 / AMD Ryzen 7
RAM      : 16 GB
GPU      : NVIDIA RTX Series (Optional)
Storage  : SSD Recommended
OS       : Windows 10/11 or Linux
```

---

## Reproducibility

All experiments can be reproduced using:

1. UCF101 Dataset
2. Provided source code
3. requirements.txt
4. Same train/test split configuration

Random Seed:

```python
42
```

---

## Citation

If you use this repository, please cite:

```bibtex
@article{Marzouk2026,
title={Enhancing Sports Action Recognition With Temporal Saliency and Squeeze-Excitation Networks},
author={Radwa Marzouk and Essa Alyounis and Aisha Blfgeh and Turke Althobaiti and Aseel Smerat and Mohamed Loey},
journal={The Visual Computer},
year={2026}
}
```

---

## DOI

Zenodo DOI:

```text
To be added after repository publication.
```

Example:

```text
https://doi.org/10.5281/zenodo.xxxxxx
```

---

## Code Availability

The complete implementation, trained models, and experiment scripts are publicly available through GitHub and archived through Zenodo.

GitHub Repository:

```text
https://github.com/yourusername/Sports-Action-Recognition-Temporal-Saliency-SE
```

Zenodo DOI:

```text
https://doi.org/10.5281/zenodo.xxxxxx
```

---

## License

This project is released under the MIT License.

---

## Acknowledgement

The authors acknowledge the UCF101 dataset creators for providing a publicly available benchmark dataset for sports action recognition research.

Dataset:

https://www.crcv.ucf.edu/data/UCF101.php
