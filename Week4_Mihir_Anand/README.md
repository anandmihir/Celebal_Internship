# Week 4 Assignment – CIFAR-10 Image Classification using ANN & CNN

## Overview

This repository contains my Week 4 assignment for the **Celebal Technologies Data Science Internship**. The objective of this project is to build and compare Artificial Neural Networks (ANN) and Convolutional Neural Networks (CNN) for image classification using the CIFAR-10 dataset. The assignment also includes an enhanced CNN model with data augmentation and Early Stopping to improve model performance.

---

## Dataset

- **Dataset:** CIFAR-10
- **Training Images:** 50,000
- **Testing Images:** 10,000
- **Image Size:** 32 × 32 RGB
- **Classes:** 10

Classes:
- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

---

## Project Workflow

### 1. Data Loading
- Loaded the CIFAR-10 dataset using TensorFlow/Keras.
- Displayed sample images with their corresponding class labels.

### 2. Data Preprocessing
- Normalized pixel values from **0–255** to **0–1**.
- Flattened images for the ANN model.

### 3. Artificial Neural Network (ANN)
- Built a baseline ANN using Dense and Dropout layers.
- Compiled using the Adam optimizer.
- Trained for 10 epochs.
- Evaluated test accuracy.

### 4. Convolutional Neural Network (CNN)
- Implemented a CNN using:
  - Conv2D
  - BatchNormalization
  - MaxPooling2D
  - Flatten
  - Dense
  - Dropout
- Trained for 10 epochs.
- Evaluated test accuracy.

### 5. Model Comparison
- Compared ANN and CNN validation accuracy.
- Visualized validation accuracy curves.
- Created a comparison table of test accuracies.

---

## Advanced Student Tasks

The following enhancements were implemented:

- Increased Dense layer configuration.
- Increased CNN filters from **32 → 64 → 128**.
- Extended training to **20 epochs**.
- Integrated **EarlyStopping** to prevent overfitting.
- Implemented data augmentation using:
  - RandomFlip
  - RandomRotation
  - RandomZoom
- Trained an advanced CNN model with data augmentation.
- Compared the performance of all model variants.

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Google Colab

---

## Results

The project demonstrates that:

- CNN significantly outperforms ANN for image classification.
- Data augmentation improves the model's ability to generalize.
- EarlyStopping helps reduce overfitting by stopping training when validation loss no longer improves.
- Increasing CNN depth and filter sizes improves classification performance.

---

## Repository Contents

```
Week4/
│── CIFAR10_ANN_CNN_Learning_Project.ipynb
│── README.md
```

---

## Learning Outcomes

Through this assignment, I gained practical experience in:

- Image preprocessing
- Artificial Neural Networks (ANN)
- Convolutional Neural Networks (CNN)
- Batch Normalization
- Dropout Regularization
- Data Augmentation
- EarlyStopping
- Model Evaluation
- Deep Learning using TensorFlow/Keras

---

## Author

**Mihir Anand**

Data Science Intern – Celebal Technologies
