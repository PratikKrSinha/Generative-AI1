# 🧠 Lab 6 – Pix2Pix GAN (Image-to-Image Translation)

> 📌 Course: Introduction to Generative AI  
> 👨‍💻 Student: Pratik Sinha  
> 🧪 Experiment: Pix2Pix using U-Net + PatchGAN  

---

## 🚀 Overview

This lab implements **Pix2Pix**, a Conditional GAN (cGAN) for paired image-to-image translation.

The model learns to convert **edge images → realistic shoe images** and compares its performance with a simple **Baseline CNN encoder–decoder** model.

---

## 🎯 Objectives

✔ Implement U-Net Generator  
✔ Implement PatchGAN Discriminator  
✔ Train using Adversarial + L1 Loss  
✔ Compare Pix2Pix with Baseline CNN  

---

## 📂 Dataset

A simulated paired dataset was created using:

- 👟 FashionMNIST (shoe-related classes)
- 🖊 OpenCV Canny Edge Detection

Input: Edge image  
Target: Original grayscale shoe image  

---

## 🏗 Architecture

### 🔹 Generator – U-Net
- Encoder–decoder structure
- Skip connections preserve spatial information
- Final activation: Tanh

### 🔹 Discriminator – PatchGAN
- Fully convolutional
- No fully connected layers
- Produces patch-level authenticity map

### 🔹 Baseline Model
- Simple CNN encoder–decoder
- Trained only with L1 loss
- No adversarial training

---

## 📉 Loss Functions

### Generator Loss

Generator Loss = GAN Loss + (100 × L1 Loss)

- Adversarial Loss: BCEWithLogitsLoss
- L1 Reconstruction Loss

### Discriminator Loss

Binary classification between:
- Real pairs (edge + real)
- Fake pairs (edge + generated)

---

## ⚙ Training Details

| Parameter | Value |
|-----------|--------|
| Image Size | 64×64 |
| Batch Size | 64 |
| Epochs | 20 |
| Learning Rate | 0.0002 |
| Optimizer | Adam (β1=0.5, β2=0.999) |
| Device | CUDA (GPU) |

---

## 📊 Training Results

Final Loss Values After 20 Epochs:

- 🔵 Discriminator Loss ≈ 0.13  
- 🟢 Generator Loss ≈ 8.20  
- 🟡 Baseline L1 Loss ≈ 0.137  

Observations:
- Generator loss decreased steadily during training.
- Discriminator remained stable without collapse.
- Baseline minimized pixel loss but produced blurrier outputs.

---

## 🔍 Observations

- Pix2Pix produces sharper and smoother outputs.
- Baseline model generates blurry and blocky images.
- Adversarial training improves perceptual realism.
- PatchGAN enhances texture-level detail.

---

## 🧠 Key Learnings

✅ Understanding Conditional GANs  
✅ Importance of adversarial learning  
✅ Role of PatchGAN discriminator  
✅ Difference between L1-only vs GAN training  
✅ Why baseline CNN outputs are blurry  

---

## 🏁 Conclusion

Pix2Pix successfully learns the mapping from edge images to realistic shoe images.

Compared to the baseline CNN, Pix2Pix produces more visually convincing results due to:

- Adversarial optimization
- Patch-level discrimination
- Skip connections in U-Net

This experiment demonstrates the effectiveness of GAN-based image-to-image translation.

---

## 📎 Files Included

- Lab6.ipynb – Colab Implementation  
- Lab6.pdf – Lab Report  
- README.md – Documentation  
