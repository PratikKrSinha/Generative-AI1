# 🎨 DCGAN Image Generator (TensorFlow)

A complete implementation of a **Deep Convolutional Generative Adversarial Network (DCGAN)** built using **TensorFlow & Keras**, capable of generating realistic images from random noise.

---

## 📌 Project Summary

This project demonstrates how **Generative Adversarial Networks (GANs)** can learn complex data distributions and generate new, realistic samples.

The model is trained on the **CIFAR-10 dataset** and learns to create synthetic images through an adversarial process between two neural networks.

---

## ⚙️ How It Works

A GAN consists of two competing models:

### 🧩 Generator

* Takes a random noise vector as input
* Learns to generate realistic images
* Uses:

  * Dense + Reshape layers
  * Transposed Convolutions
  * Batch Normalization
  * ReLU activation
* Final output uses **tanh** activation

---

### 🔍 Discriminator

* Takes an image (real or generated) as input
* Classifies whether the image is real or fake
* Uses:

  * Convolutional layers
  * LeakyReLU activation
  * Dropout for regularization

---

### ⚔️ Adversarial Training

* Generator tries to **fool the discriminator**
* Discriminator tries to **detect fake images**
* Both models improve simultaneously

---

## 📂 Dataset Details

* **Dataset:** CIFAR-10
* **Total Images:** 60,000
* **Image Size:** 32 × 32 × 3
* **Classes:** Airplane, Car, Bird, Cat, Deer, Dog, Frog, Horse, Ship, Truck

Images are normalized to the range **[-1, 1]** for stable GAN training.

---

## ✨ Key Features

* 🚀 End-to-end DCGAN implementation
* 📊 Real-time training progress visualization
* 🎨 Image generation after each epoch
* 🔄 Latent space interpolation (smooth transitions)
* 💾 Model saving & reloading
* ☁️ Fully compatible with Google Colab (single-cell execution)

---

## 🛠️ Tech Stack

* **Python 3**
* **TensorFlow / Keras**
* **NumPy**
* **Matplotlib**

---

## ▶️ Getting Started

### 🔹 Run on Google Colab (Recommended)

1. Open Google Colab
2. Paste the full code into a single cell
3. Run the cell

---

### 🔹 Run Locally

Install dependencies:

```bash
pip install tensorflow matplotlib numpy
```

Run the script:

```bash
python your_script.py
```

---

## 📸 Results & Output

* The model generates images at regular intervals during training
* Image quality improves as training progresses
* Final outputs resemble CIFAR-10-like objects

---

## 🔄 Latent Space Interpolation

This project includes interpolation between two random noise vectors:

* Produces a smooth transformation between generated images
* Demonstrates how the model learns meaningful feature representations

---

## 💾 Model Persistence

The trained generator is saved as:

```bash
dcgan_generator.keras
```

Reload the model:

```python
import tensorflow as tf
model = tf.keras.models.load_model("dcgan_generator.keras")
```

---

## 📈 Training Configuration

| Parameter     | Value               |
| ------------- | ------------------- |
| Epochs        | 30                  |
| Batch Size    | 128                 |
| Latent Dim    | 100                 |
| Optimizer     | Adam                |
| Learning Rate | 0.0001              |
| Loss Function | Binary Crossentropy |

---

## 🚧 Future Enhancements

* 🔼 Train on higher-resolution datasets
* 🎭 Implement Conditional GAN (cGAN)
* 🎨 Upgrade to StyleGAN / CycleGAN
* 🌐 Deploy as a web app (Streamlit/Flask)
* ⚡ Improve training stability and image quality

---

## 👨‍💻 Author

**Pratik Sinha**

