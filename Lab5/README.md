
# 🧪 Lab 5 – Baseline CNN for Image-to-Image Translation

## 📌 Introduction

This project implements a **baseline Encoder–Decoder Convolutional Neural Network (CNN)** for paired image-to-image translation using the CIFAR-10 dataset.

The task performed is:

> Convert **Grayscale Images → RGB Color Images**

This model does **not** use GAN. It is a simple reconstruction-based architecture trained using L1/MSE loss.

---

## 🎯 Objective

* Load paired images
* Normalize images to [-1, 1]
* Train an Encoder–Decoder CNN
* Compute reconstruction loss (L1 / MSE)
* Visualize translated images

---

## 🗂️ Dataset

Dataset used: **CIFAR-10**

* Image size: 32 × 32
* 10 object classes
* Used for supervised image-to-image translation

---

## 🧠 Model Architecture

### 🔹 Encoder

* Conv2D layers
* Downsampling: 32×32 → 16×16 → 8×8
* Extracts feature representation

### 🔹 Decoder

* ConvTranspose2D layers
* Upsampling: 8×8 → 16×16 → 32×32
* Final activation: `Tanh()`

Output range: **[-1, 1]**

---

## 📉 Loss Function

* **L1 Loss** (Pixel-wise difference)
* Can also use **MSE Loss**

Reconstruction loss encourages the model to predict pixel values close to the ground truth image.

---

## ⚙️ Training Details

* Optimizer: Adam
* Learning rate: 0.0002
* Epochs: 5
* Batch size: 128
* Device: GPU (if available)

Loss decreases gradually during training, indicating proper learning.

---

## 🖼️ Results

We visualize:

* Input (Grayscale)
* Target (Original RGB)
* Output (Predicted RGB)

### ⚠️ Observation:

The output images are **blurry**.

---

## ❓ Why Are Outputs Blurry?

Because:

* Only reconstruction loss (L1/MSE) is used
* No adversarial loss (GAN)
* Model predicts average color distribution
* CIFAR-10 images are low resolution (32×32)

To generate sharper images, GAN-based methods are required.

---

## 🚀 How to Run

```bash
pip install torch torchvision matplotlib
```

Run the Colab notebook or Python script.

---

## 📚 Key Learning Outcomes

* Understanding Encoder–Decoder architecture
* Image normalization to [-1, 1]
* Pixel-wise reconstruction loss
* Basic image-to-image translation
* Limitations of non-GAN models

---

## 📌 Conclusion

This lab demonstrates how a baseline CNN can perform image-to-image translation using only reconstruction loss. While the model successfully learns the mapping from grayscale to RGB, the generated images lack sharp details due to the absence of adversarial training.

---


Tell me what level you want 😄

