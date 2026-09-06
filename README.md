# 🌾 Rice Leaf Disease Classification Using Deep Learning

A deep learning project for classifying rice leaf images into six disease/health categories using multiple deep learning architectures.

## 📌 Overview

Rice plants are affected by several diseases that can reduce crop productivity. This project explores deep learning based image classification for automatic identification of rice leaf diseases.

Five different deep learning architectures were implemented and compared:

- Baseline CNN
- DenseNet121
- EfficientNetV2-S
- ResNet50
- DeiT-B

The experiments were developed and executed using Kaggle notebooks.

---

## 📊 Dataset

The project uses the Rice Leaf Disease dataset.

### Dataset Statistics

- Number of classes: 6
- Training images: 2,100
- Validation images: 528
- Total images: 2,628
- Image size: 224 × 224
- Training images per class: 350
- Validation images per class: 88

The dataset is approximately balanced across all six classes.

### Classes

1. Bacterial Leaf Blight
2. Brown Spot
3. Healthy
4. Leaf Blast
5. Leaf Scald
6. Narrow Brown Spot

The dataset is not included in this repository. It is loaded from Kaggle during notebook execution.

---

## 🧠 Models Implemented

| Model | Description |
|---|---|
| Baseline CNN | Custom convolutional neural network used as a baseline |
| DenseNet121 | Transfer learning based DenseNet architecture |
| EfficientNetV2-S | EfficientNetV2 based image classification model |
| ResNet50 | Transfer learning using ResNet50 |
| DeiT-B | Data-efficient Vision Transformer |

---

## 🔬 Methodology

The general workflow followed in the project is:

1. Dataset loading
2. Dataset verification
3. Image resizing
4. Data augmentation
5. Model construction
6. Model training
7. Validation
8. Model checkpointing
9. Performance evaluation
10. Confusion matrix and classification analysis
11. Single-image prediction

Different experiments use model-specific training strategies.

### Data Augmentation

The experiments include augmentation techniques such as:

- Horizontal flipping
- Rotation
- Zoom
- Translation
- Contrast variation
- Brightness variation

---

## 📈 Evaluation

Model performance is evaluated using:

- Accuracy
- Loss
- Confusion Matrix
- Classification Report
- Precision
- Recall
- F1-score

The best-performing model can be compared with the baseline CNN and other architectures.

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

## 🏆 Results

The models were evaluated on the 528-image validation set.

| Model | Validation Accuracy | F1-Score |
|---|---:|---:|
| Baseline CNN | 85.98% | — |
| DenseNet121 | 93.75% | 94.00% |
| EfficientNetV2-S | 95.64% | 95.59% |
| ResNet50 | 96.59% | 97.00% |
| DeiT-B | 98.86% | 98.86% |

### Best Result

**DeiT-B achieved the best standard validation accuracy of 98.86%.**

With Test-Time Augmentation (TTA), the DeiT-B model achieved:

**99.05% validation accuracy.**

> Note: The 99.05% result is obtained using inference-time Test-Time Augmentation and is reported separately from the standard validation result.

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- PyTorch
- Torchvision
- timm
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- OpenCV
- LIME
- Scikit-image

---

## 📁 Project Structure

```text
rice-leaf-disease-detection/
│
├── notebook/
│   ├── 01_baseline_cnn.ipynb
│   ├── 02_densenet121.ipynb
│   ├── 03_efficientnetv2s.ipynb
│   ├── 04_resnet50.ipynb
│   └── 05_deit_b.ipynb
│
├── .gitignore
├── requirements.txt
└── README.md
