# Cattle Detection: Aerial Monitoring Using YOLOv5


# Cattle Detection: Aerial Monitoring Using YOLOv5

An end-to-end computer vision pipeline developed to detect and monitor herds of cattle in aerial drone imagery and continuous video feeds using YOLOv5.

---

## 📌 Project Overview
Monitoring livestock across wide-range agricultural land using unmanned aerial vehicles (UAVs) requires robust object detection that can handle varying altitudes, scale variations, and complex terrain backgrounds. 

This repository details the training, validation, and inference workflows for a custom YOLOv5s model fine-tuned specifically on high-resolution aerial datasets.

- **Architecture:** YOLOv5s (Transfer Learning)
- **Class:** Single-class (`cow`)
- **Input Resolution:** 608 × 608
- **Training Epochs:** 30
- **Dataset:** Aerial drone images partitioned into Train, Validation, and Test sets

---

## 📊 Performance & Evaluation

The model converged effectively over 30 epochs, reaching a peak **mAP@0.5 of 95.1%** and high precision across validation folds:

| Metric | Score |
| :--- | :--- |
| **mAP@0.50** | **95.1%** |
| **Precision (P)** | **94.9%** |
| **Recall (R)** | **89.4%** |
| **mAP@0.50:0.95** | **57.7%** |

### Training Metrics & Loss Curves
Training metrics, loss functions, precision-recall dynamics, and mAP progression across epochs:

![Training Results](results/results.png)

### Model Predictions vs. Ground Truth
Sample predictions from the validation split evaluating detection confidence and spatial localization:

![Validation Predictions](results/val_batch0_pred.jpg)

---

## 📁 Repository Structure

```text
├── Cattle_Detection.ipynb   # Main workflow notebook (setup, training, detection)
├── results/                 # Visual evaluation artifacts, curves, and sample outputs
│   ├── results.png
│   ├── val_batch0_pred.jpg
│   └── val_batch1_labels.jpg
└── README.md                # Project documentation and summary
