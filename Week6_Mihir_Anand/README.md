# 🖼️ Denoising Autoencoder using MNIST

## 📌 Project Overview

This project implements a **Convolutional Denoising Autoencoder** using the **MNIST handwritten digit dataset**. The objective is to train a neural network that can reconstruct clean handwritten digit images from artificially corrupted (noisy) images.

Gaussian noise is added to the original images, and the autoencoder learns to remove the noise while preserving the important features of the digits.

---

## 🎯 Objectives

- Load and preprocess the MNIST dataset.
- Add Gaussian noise to the images.
- Build a Convolutional Denoising Autoencoder.
- Train the model using noisy images as input and clean images as output.
- Generate denoised images on the test dataset.
- Compare Original, Noisy, and Reconstructed images.
- Visualize training and validation loss.

---

## 🛠️ Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Pillow (PIL)

---

## 📂 Dataset

- Dataset: **MNIST Handwritten Digits**
- Training Images: **60,000**
- Testing Images: **10,000**
- Image Size: **28 × 28**
- Color Format: **Grayscale**

---

## 🏗️ Model Architecture

### Encoder

- Conv2D (32 Filters)
- MaxPooling2D
- Conv2D (64 Filters)
- MaxPooling2D

### Decoder

- Conv2D (64 Filters)
- UpSampling2D
- Conv2D (32 Filters)
- UpSampling2D
- Conv2D (1 Filter, Sigmoid Activation)

---

## ⚙️ Training Configuration

| Parameter | Value |
|-----------|-------|
| Optimizer | Adam |
| Loss Function | Binary Crossentropy |
| Epochs | 10 |
| Batch Size | 128 |
| Noise Type | Gaussian Noise |
| Noise Factor | 0.5 |

---

# 📸 Results

## Original Images

![Original Images](images/original.png)

---

## Noisy Images

![Noisy Images](images/noisy.png)

---

## Denoised Images

![Denoised Images](images/denoised.png)

---

## Training Loss

![Training Loss](images/loss.png)

---

# 📈 Observations

- The autoencoder successfully removed most of the Gaussian noise from the input images.
- The reconstructed images preserved the overall digit structure while reducing noise.
- Training and validation loss decreased consistently during training, indicating effective learning.
- Simpler digits such as **0** and **1** were reconstructed more accurately than more complex digits.
- A higher noise factor would require a deeper model or additional training epochs for better reconstruction.

---

# ⚠️ Challenges

- Selecting an appropriate noise factor without making reconstruction too difficult.
- Preserving fine image details while removing noise.
- Avoiding overfitting with limited training epochs.
- Balancing model complexity and reconstruction quality.

---

# 🚀 Future Improvements

- Train for more epochs.
- Compare different noise levels.
- Add Batch Normalization.
- Experiment with deeper encoder-decoder architectures.
- Evaluate performance using PSNR and SSIM metrics.



---

# 📌 Conclusion

This project demonstrates the effectiveness of Convolutional Denoising Autoencoders in image restoration tasks. The model successfully reconstructs clean handwritten digits from noisy inputs while preserving their essential features. The results highlight the capability of deep learning techniques for image denoising and provide a foundation for more advanced applications in computer vision and image enhancement.

---

## 👨‍💻 Author

**Mihir Anand**

Celebal Technologies – Data Science Internship
