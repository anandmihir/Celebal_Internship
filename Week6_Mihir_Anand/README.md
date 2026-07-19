# 🖼️ Denoising Autoencoder using MNIST

A **Denoising Autoencoder** is a type of neural network that learns to reconstruct clean images from noisy inputs. In this project, a Convolutional Denoising Autoencoder is trained on the MNIST handwritten digit dataset to remove artificially added Gaussian noise while preserving the original digit structure.

---

# 📌 Project Overview

The objective of this project is to implement a **Convolutional Denoising Autoencoder** using TensorFlow/Keras.

The workflow includes:

- Loading and preprocessing the MNIST dataset
- Adding Gaussian noise to clean images
- Building an Encoder-Decoder architecture
- Training the model using noisy images as inputs and clean images as targets
- Reconstructing clean images from noisy test images
- Comparing Original, Noisy, and Denoised images
- Visualizing training performance using loss curves

---

# 🎯 Objectives

- Load and preprocess the MNIST dataset.
- Normalize the images.
- Add artificial Gaussian noise.
- Build a Convolutional Denoising Autoencoder.
- Train the model using noisy images as inputs.
- Generate denoised outputs.
- Compare reconstruction results visually.
- Analyze the model performance.

---

# 🛠 Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Pillow (PIL)

---

# 📂 Dataset Information

Dataset Used: **MNIST Handwritten Digits**

- Training Images: **60,000**
- Testing Images: **10,000**
- Image Size: **28 × 28**
- Color Format: **Grayscale**

---

# 🏗 Model Architecture

## Encoder

- Conv2D (32 Filters, ReLU)
- MaxPooling2D
- Conv2D (64 Filters, ReLU)
- MaxPooling2D

## Decoder

- Conv2D (64 Filters, ReLU)
- UpSampling2D
- Conv2D (32 Filters, ReLU)
- UpSampling2D
- Conv2D (1 Filter, Sigmoid)

---

# ⚙ Training Configuration

| Parameter | Value |
|-----------|-------|
| Optimizer | Adam |
| Loss Function | Binary Crossentropy |
| Epochs | 10 |
| Batch Size | 128 |
| Noise Type | Gaussian Noise |
| Noise Factor | 0.5 |

---

# 📷 Original MNIST Images

The following images are randomly selected handwritten digits from the MNIST dataset before any preprocessing or noise is added.

<p align="center">
    <img src="images/original.png" width="750">
</p>

---

# 📷 Original vs Noisy Images

Artificial Gaussian noise is added to the original images to create the noisy inputs that will be used to train the denoising autoencoder.

<p align="center">
    <img src="images/original_noisy.png" width="850">
</p>

---

# 📷 Original vs Noisy vs Denoised Images

After training, the denoising autoencoder reconstructs clean images from the noisy inputs. The comparison below demonstrates the effectiveness of the model in removing noise while preserving the digit structure.

<p align="center">
    <img src="images/denoised.png" width="900">
</p>

---

# 📉 Training and Validation Loss

The graph below shows the decrease in training and validation loss during model training.

<p align="center">
    <img src="images/loss.png" width="700">
</p>

---

# 📊 Observations

- The autoencoder successfully learned to remove Gaussian noise from handwritten digit images.

- The reconstructed images retained the important structural features of the digits while eliminating most of the added noise.

- Training and validation loss decreased steadily, indicating that the model learned meaningful image representations.

- Digits with simpler shapes were reconstructed more accurately than more complex digits.

- Increasing the amount of noise would require a deeper architecture or additional training epochs for improved reconstruction.

---

# ⚠ Challenges

- Choosing an appropriate noise factor without making reconstruction too difficult.

- Preserving fine image details while removing noise.

- Balancing reconstruction quality and model complexity.

- Avoiding overfitting during training.

---

# 🚀 Future Improvements

- Train the model for more epochs.

- Experiment with different noise levels.

- Add Batch Normalization layers.

- Use Skip Connections (U-Net style architecture).

- Evaluate reconstruction quality using PSNR and SSIM metrics.

- Experiment with Variational Autoencoders (VAE).

---

# ▶️ How to Run the Project

### Install Dependencies

```bash
pip install tensorflow numpy matplotlib pillow
```

### Run the Notebook

Open

```
Week6_Mihir_Anand_DPGU.ipynb
```

using

- Jupyter Notebook
- Google Colab
- VS Code

Run all cells sequentially.

---

# 📌 Results

The trained Convolutional Denoising Autoencoder successfully reconstructs clean handwritten digit images from noisy inputs. Visual comparisons between the original, noisy, and reconstructed images demonstrate that the model effectively removes Gaussian noise while preserving the essential digit structures. The decreasing training and validation loss further confirms successful learning.

---

# 👨‍💻 Author

**Mihir Anand**

**Celebal Technologies – Data Science Internship**

**Week 6 Assignment**
