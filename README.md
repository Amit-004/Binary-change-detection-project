# Binary Change Detection using Siamese ResNet34 U-Net

## Project Description

This project performs binary change detection on EO-SAR satellite image pairs using a Siamese ResNet34 U-Net architecture. The model learns temporal differences between pre-event and post-event satellite images and predicts pixel-level binary change masks.

The architecture combines Siamese feature extraction with a U-Net based encoder-decoder segmentation framework for improved spatial localization and feature representation.

---

# Methodology

- Siamese dual-branch architecture
- ResNet34 encoder backbone
- U-Net decoder with skip connections
- BCE + Dice combined loss
- Threshold tuning for optimal F1-score
- Data augmentation:
  - Horizontal flip
  - Vertical flip
  - Rotation augmentation

---

# Requirements

Python Version:

```bash
Python 3.10
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# Environment Setup

## Kaggle Environment

The project was developed and trained using Kaggle Notebook with GPU acceleration.

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# Dataset Structure

Dataset should follow this structure:

```text
dataset/
├── train/
│   ├── pre-event/
│   ├── post-event/
│   └── target/
│
├── val/
│   ├── pre-event/
│   ├── post-event/
│   └── target/
│
├── test/
│   ├── pre-event/
│   ├── post-event/
│   └── target/
```

Note:
Dataset is not included due to size limitations.

---

# Training

Open and run:

```text
Assignment.ipynb
```

Training and evaluation are implemented inside the notebook.

---

# Evaluation

Evaluation and prediction generation are included in:

```text
Assignment.ipynb
```

Generated prediction masks are stored in:

```text
test_predictions.zip
```

---

# Configuration

Hyperparameters are stored in:

```text
config.yaml
```

Main parameters:

- Image Size: 256
- Batch Size: 4
- Epochs: 50
- Learning Rate: 1e-4
- Optimizer: AdamW
- Loss Function: BCE + Dice Loss

---

# Model Weights

Download trained model checkpoint from:

```text
https://drive.google.com/file/d/1eSCKmP39JU35HokM6o9K1Canh2_V7bIw/view?usp=sharing 
```

---

# Results

| Metric | Value |
|---|---|
| Precision | 0.0347 |
| Recall | 0.0792 |
| F1 Score | 0.0483 |
| IoU | 0.0247 |

---

# Files Included

- Assignment.ipynb
- config.yaml
- requirements.txt
- Technical_Report.pdf
- test_predictions.zip

---

# References

1. Ronneberger, O., Fischer, P., & Brox, T. (2015). U-Net: Convolutional Networks for Biomedical Image Segmentation. MICCAI 2015.

2. Daudt, R. C., Le Saux, B., & Boulch, A. (2018). Fully Convolutional Siamese Networks for Change Detection. ICIP 2018.

3. Bandara, W. G. C., & Patel, V. M. (2022). A Transformer-Based Siamese Network for Change Detection. IGARSS 2022.

4. Cao, et al. (2024). A Siamese Swin-UNet for Image Change Detection. Scientific Reports.

---

# Author

Amit Nagora  
M.Tech in Signal Processing and Machine Learning  
Indian Institute of Technology Guwahati
