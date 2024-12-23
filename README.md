# DermAI - Skin Lesion Classification

## Overview
DermAI is a deep learning project aimed at classifying skin lesions into three categories: **Nevus**, **Bruise**, and **Melanoma**. This system uses a pre-trained VGG16 model to assist in dermatological image analysis, providing accurate and reliable classifications.

---

## Methodology

### 1. Data Preprocessing
- **Dataset Sources**: Images were collected from the following sources on Roboflow:
  - [Nevus Dataset](https://universe.roboflow.com/aomsin-pvpaz/-vi0h8)
  - [Melanoma Dataset](https://universe.roboflow.com/dd-xovzc/cancer-sjstw)
  - [Bruises Dataset](https://universe.roboflow.com/new-workspace-khpun/bruises)
- **Steps**:
  - Applied data augmentation (resizing, cropping, flipping, and rotation).
  - Normalized pixel values for compatibility with the VGG16 input format.

### 2. Data Loading
- Used PyTorch’s `ImageFolder` to load and organize images and labels.
- Split data into **training** and **testing** sets.
- Configurations:
  - **Batch Size**: 16
  - **Shuffle**: Enabled

### 3. Model Implementation
- **Base Model**: VGG16 (pre-trained on ImageNet).
- Modified the final layer to classify the three skin lesion types.

### 4. Evaluation
- Performance was evaluated using metrics such as:
  - **Accuracy**: Achieved 97.63%.
  - **Classification Report**:
    - F1-Score
    - Precision
    - Recall

### 5. Deployment
- The trained model was deployed with an interactive interface for real-time classification.

---

## Features
- Classifies images into **Nevus**, **Bruise**, or **Melanoma**.
- Provides an accuracy of **97.63%**.
- Easy-to-use interactive interface.

---


