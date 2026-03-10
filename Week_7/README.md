# 🎨 Neural Style Transfer – Lab 7

## 📚 Course

**CSET419 – Introduction to Generative AI**

---

# 🧠 Objective

The objective of this lab is to implement **Neural Style Transfer (NST)** using a **pretrained Convolutional Neural Network (CNN)**.

Neural Style Transfer combines:

🖼 **Content** from one image
🎨 **Style** from another image

The final generated image preserves the **structure of the content image** while applying the **artistic style of the style image**.

---

# ⚙️ Methodology

The implementation uses a **pretrained VGG19 model** to extract important visual features from images.

### 🔍 Steps Performed

1️⃣ Load the **Content Image**
2️⃣ Load the **Style Image**
3️⃣ Load **Pretrained VGG19 Model**
4️⃣ Extract **Feature Maps** from different CNN layers
5️⃣ Compute **Content Loss**
6️⃣ Compute **Style Loss using Gram Matrix**
7️⃣ Combine losses into **Total Loss**
8️⃣ Optimize the generated image using **Gradient Descent**

---

# 🧩 Technologies Used

| Tool           | Purpose                 |
| -------------- | ----------------------- |
| 🐍 Python      | Programming Language    |
| 🔥 PyTorch     | Deep Learning Framework |
| 📦 Torchvision | Pretrained Models       |
| 📊 Matplotlib  | Image Visualization     |

---

# 🖼 Images Used

## 📌 Content Image

<img src="content.png" width="400">

---

## 🎨 Style Image

<img src="style.png" width="400">

---

# ✨ Stylized Output

The final generated image after applying **Neural Style Transfer**:

<img src="output.png" width="450">

---

# 📊 Results

✅ The **content structure** of the original image is preserved.

✅ The **texture, colors, and artistic patterns** from the style image are transferred.

✅ The generated image produces a visually **artistic and stylized output**.

---

# 📂 Repository Structure

```
Generative-AI1
│
├── Lab5
├── Lab6
│
└── Week_7
      ├── README.md
      ├── style_transfer.py
      ├── content.png
      ├── style.png
      └── output.png
```

---

# 🚀 How to Run

1️⃣ Install required libraries

```
pip install torch torchvision matplotlib
```

2️⃣ Run the style transfer script

```
python style_transfer.py
```

3️⃣ The generated stylized image will be displayed using **Matplotlib**.

---

# 👨‍💻 Author

**Pratik Sinha**
🎓 B.Tech – Computer Science
📍 Generative AI Lab – Week 7

---

# ⭐ Project Highlights

✨ Implemented **Neural Style Transfer using VGG19**
✨ Used **Gram Matrix for style representation**
✨ Applied **optimization-based image generation**

---

💡 *This project demonstrates how deep learning models can creatively combine visual styles and generate artistic images.*
