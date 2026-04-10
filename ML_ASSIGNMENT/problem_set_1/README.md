# CNN-Based Pneumonia Detection from Chest X-rays

This project implements a **Convolutional Neural Network (CNN)** using TensorFlow/Keras to classify chest X-ray images into:

-  Normal (Healthy lungs)
-  Pneumonia (Infected lungs)

The goal is to demonstrate how deep learning can assist in **medical image diagnosis**.

---

#  Project Overview

Pneumonia is a serious lung infection that can be detected through chest X-rays. Manual diagnosis can be slow and subjective.

This project builds an AI model that automatically learns patterns from X-ray images and performs binary classification.

---

# Dataset Structure

The dataset is organized as follows:

Archive/
│
├── train/
│   ├── Normal
│   └── Pneumonia
│
├── val/
│   ├── Normal
│   └── Pneumonia
│
└── test/
    ├── Normal
    └── Pneumonia

Each folder represents a class label.

---

# Data Preprocessing

To improve model performance and reduce overfitting:

### Training Data:
- Rescaling (1./255)
- Rotation (±10°)
- Zoom augmentation
- Horizontal flipping

### Validation & Test Data:
- Only rescaling applied

---

# CNN Model Architecture

The model is built using multiple convolutional layers:

- Conv2D (32 filters)
- Conv2D (64 filters)
- Conv2D (128 filters)
- Conv2D (256 filters)
- Batch Normalization
- MaxPooling layers
- Global Average Pooling
- Dense layer (256 neurons)
- Dropout (0.5)
- Output layer (Sigmoid)

---

# Model Compilation

- Optimizer: Adam (learning rate = 0.0001)
- Loss Function: Binary Crossentropy
- Metric: Accuracy

---

# Training Strategy

To improve performance and avoid overfitting:

- EarlyStopping (patience = 3)
- ModelCheckpoint (best_model.h5)
- Training epochs: 20
- Batch size: 32

---

# Evaluation Metrics

The model is evaluated using:

- Accuracy
- Loss curves
- Confusion Matrix
- Classification Report
- ROC Curve (AUC)
- Precision-Recall Curve

---

# Visualizations

### Training Curves
- Accuracy vs Epochs
- Loss vs Epochs

### Confusion Matrix
Shows correct vs incorrect predictions

### ROC Curve
Measures classification performance

### Precision-Recall Curve
Evaluates model performance under class imbalance

---

# Error Analysis

Misclassified X-ray images are visualized to:

- Understand model weaknesses
- Identify difficult samples
- Improve future performance

---

# Model Saving

The best trained model is saved as:

best_model.h5

---

# Conclusion

This project demonstrates the use of **Deep Learning (CNN)** for medical image classification. It shows how AI can assist in detecting pneumonia from chest X-rays with high accuracy and strong generalization ability.

---

# Tools Used

- TensorFlow / Keras
- NumPy
- Matplotlib
- Scikit-learn
- Seaborn
- Google Colab