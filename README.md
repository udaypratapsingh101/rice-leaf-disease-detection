# 🌾 Rice Leaf Disease Classification Using Deep Learning

A deep learning project for automatic classification of rice leaf images into six disease/health categories using multiple deep learning architectures.

## 📌 Overview

Rice leaf diseases can negatively affect crop health and productivity. This project explores deep learning-based image classification for identifying different rice leaf disease categories from leaf images.

The project compares five deep learning approaches:

- Baseline CNN
- DenseNet121
- EfficientNetV2-S
- ResNet50
- DeiT-B

The experiments were developed and executed using Kaggle notebooks.

---

## 🎯 Objective

The main objective of this project is to develop and compare deep learning models for multi-class rice leaf disease classification and identify the architecture that provides the best validation performance.

---

## 📊 Dataset

The project uses the Rice Leaf Disease dataset.

### Dataset Statistics

| Property | Value |
|---|---:|
| Number of classes | 6 |
| Training images | 2,100 |
| Validation images | 528 |
| Total images | 2,628 |
| Image size | 224 × 224 |
| Training images per class | 350 |
| Validation images per class | 88 |

The training and validation sets contain the same six classes and the training dataset is balanced across the classes.

### Classes

1. Bacterial Leaf Blight
2. Brown Spot
3. Healthy
4. Leaf Blast
5. Leaf Scald
6. Narrow Brown Spot

The dataset is not included in this GitHub repository. The notebooks load it from the Kaggle environment.

---

## 🧠 Models Implemented

| Model | Approach |
|---|---|
| Baseline CNN | Custom convolutional neural network used as the baseline |
| DenseNet121 | Transfer learning with DenseNet121 followed by fine-tuning |
| EfficientNetV2-S | Transfer learning and fine-tuning using EfficientNetV2-S |
| ResNet50 | Transfer learning and fine-tuning using ResNet50 |
| DeiT-B | Vision Transformer based approach with advanced training techniques |

---

## 🔬 Methodology

The general workflow used in the experiments is:

1. Dataset loading
2. Dataset and class verification
3. Image resizing to 224 × 224
4. Data preprocessing
5. Data augmentation
6. Model initialization
7. Transfer learning where applicable
8. Model training
9. Fine-tuning
10. Validation
11. Best-model checkpointing
12. Performance evaluation
13. Confusion matrix and classification analysis
14. Single-image prediction

Different models use model-specific training strategies.

### Data Augmentation

The experiments use augmentation techniques such as:

- Horizontal flipping
- Rotation
- Zoom
- Translation
- Contrast variation
- Brightness variation

The DenseNet121 experiment also includes MixUp-based training.

---

## ⚙️ Training Techniques

Different experiments use different optimization and regularization strategies.

The project includes techniques such as:

- Transfer learning
- Fine-tuning
- Data augmentation
- MixUp
- MixUp/CutMix
- Learning-rate scheduling
- Model checkpointing
- Adaptive learning-rate reduction
- Mixed-precision training
- Gradient clipping

The DeiT-B experiment additionally uses a custom training and validation loop and inference-time Test-Time Augmentation (TTA).

---

## 📈 Evaluation Metrics

The models are evaluated using:

- Accuracy
- Loss
- Precision
- Recall
- F1-score
- Confusion Matrix
- Classification Report

---

## 🏆 Results

The verified validation performance currently reported by the notebooks is:

| Model | Best Validation Accuracy |
|---|---:|
| Baseline CNN | 85.98% |
| DenseNet121 | 93.75% |
| EfficientNetV2-S | To be added |
| ResNet50 | 96.59% |
| DeiT-B | 98.86% |

### Best Performing Model

**DeiT-B achieved the highest standard validation accuracy of 98.86%.**

The DeiT-B model was additionally evaluated using Test-Time Augmentation (TTA), where the validation accuracy increased to **99.05%**.

> Note: 99.05% is the TTA-enhanced inference result and is reported separately from the standard DeiT-B validation accuracy of 98.86%.

---

## 📓 Notebooks

### 1. Baseline CNN

[Open Baseline CNN Notebook](notebook/01_baseline_cnn.ipynb)

### 2. DenseNet121

[Open DenseNet121 Notebook](notebook/02_densenet121.ipynb)

### 3. EfficientNetV2-S

[Open EfficientNetV2-S Notebook](notebook/03_efficientnetv2s.ipynb)

### 4. ResNet50

[Open ResNet50 Notebook](notebook/04_resnet50.ipynb)

### 5. DeiT-B

[Open DeiT-B Notebook](notebook/05_deit_b.ipynb)

---

## 📊 Model Comparison

The experiments show progressive improvement from the baseline CNN to more advanced architectures.

```text
Baseline CNN      → 85.98%
DenseNet121       → 93.75%
EfficientNetV2-S  → To be added
ResNet50          → 96.59%
DeiT-B            → 98.86%
DeiT-B + TTA      → 99.05%
## 🚀 How to Run

### Using Kaggle

These notebooks are designed to run in the Kaggle environment because the dataset is accessed using Kaggle-specific input paths.

1. Open the required notebook from the `notebook/` directory.
2. Open or import the notebook in Kaggle.
3. Add the Rice Leaf Disease dataset to the Kaggle notebook.
4. Make sure the dataset is available at the expected Kaggle input path.
5. Enable the required computing environment/accelerator.
6. Run the notebook cells sequentially from top to bottom.
7. Review the training, validation, confusion matrix, classification report, and prediction results.

### Dataset Structure

The notebooks expect the following dataset structure:

```text
RiceLeafsDisease/
├── train/
└── validation/
