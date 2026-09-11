# 🐢 Sea Turtle Video Detection with YOLO11

A computer vision demo exploring lightweight object detection for identifying sea turtles in image and video data.

## 📌 Overview

This project uses a pretrained YOLO11 model and transfer learning to detect sea turtles from annotated imagery.

## 📂 Dataset

The project uses the **GTST-2023 Green Sea Turtle dataset**, a public image and video dataset containing annotated footage of nesting green sea turtles.

The dataset includes:

- 🖼️ Video and image data
- 📦 Bounding-box annotations for sea-turtle detection
- 🌊 Natural background and lighting variation

Dataset source:  
https://www.kaggle.com/datasets/william2020/gtst-2023

Reference:  
_GTST-2023: An image and video dataset of nesting green sea turtles with annotated data_

> The dataset is not included directly in this repository. Please obtain it from the original source and follow the dataset licence and attribution requirements.

## 🤖 Model

The current baseline uses:

- **YOLO11n**
- Pretrained weights
- Image size: `640 × 640`
- Batch size: `8`
- Training epochs: `20`
- CUDA acceleration
- Single-class sea-turtle detection

YOLO11n was selected as the initial model because it is lightweight and suitable for fast object detection.

## 📊 Evaluation

The trained model achieved the following validation results:

| Metric            |            Result |
| ----------------- | ----------------: |
| 🎯 Precision      |         **0.990** |
| 🔍 Recall         |         **0.966** |
| 📈 mAP@50         |         **0.984** |
| 📉 mAP@50–95      |         **0.922** |
| ⚡ Inference time | **~1.1 ms/image** |

Validation data:

- **1,407 images**
- **1,054 annotated instances**

The baseline results show high precision and recall, providing a strong starting point for further analysis and model refinement.
