# 🧠 Generative AI Lab – Sequential Data Generation

## 📌 Course

**CSET419 – Introduction to Generative AI**

## 🎯 Objective

This lab focuses on building generative models capable of learning patterns from sequential data and generating new sequences. The implementation explores deep learning techniques such as **LSTM (Recurrent Neural Networks)** and **Transformer architectures**.

---

## 📖 Overview

Sequential data generation refers to the process where a model learns patterns from ordered data and predicts the next element in a sequence.

### 🔹 Examples of Sequential Data

* Text generation (sentences, chatbots)
* Speech signals
* Time-series data
* Music composition
* DNA sequences

Generative models learn the **probability distribution** of sequences and use it to generate meaningful outputs.

---

## 🧪 Lab Components

### 🔹 Component I: LSTM-Based Sequence Generation

#### Steps:

1. Load and preprocess dataset
2. Perform word-level tokenization
3. Create input-output sequence pairs
4. Build LSTM-based model
5. Train model on dataset
6. Generate text using seed input

#### ✅ Key Features:

* Uses **Embedding + LSTM + Dense**
* Learns context from previous words
* Generates human-like sentence continuation

---

### 🔹 Component II: Transformer-Based Sequence Generation

#### Steps:

1. Use same dataset
2. Apply tokenization
3. Add positional encoding
4. Build Transformer encoder
5. Train model for prediction
6. Generate sequences

#### ✅ Key Features:

* Uses **Multi-Head Attention**
* Captures long-range dependencies
* More powerful than traditional RNNs

---

## 📂 Dataset

The dataset consists of multiple sentences related to AI and machine learning concepts, such as:

```
artificial intelligence systems learn patterns from data.
sequence models process information step by step.
recurrent neural networks are useful for sequence prediction.
...
```

---

## ⚙️ Technologies Used

* Python 🐍
* TensorFlow / Keras
* Google Colab
* Deep Learning (LSTM & Transformer)

---

## 🚀 How to Run

1. Open **Google Colab**
2. Copy the provided code into a single cell
3. Run the cell
4. Observe generated outputs from:

   * LSTM model
   * Transformer model

---

## 📊 Output

The models generate new text sequences based on a given seed input.

### 🔹 Example:

```
Input: "machine learning"
Output: "machine learning helps computers learn automatically ..."
```

---

## 📈 Learning Outcomes

After completing this lab, you will be able to:

* Understand sequential data generation
* Preprocess text data for deep learning
* Implement LSTM-based models
* Understand Transformer architecture basics
* Generate meaningful text sequences
* Evaluate generated outputs

---

## 🔍 Key Concepts

* Tokenization
* Sequence Padding
* LSTM (Long Short-Term Memory)
* Attention Mechanism
* Positional Encoding
* Text Generation

---

## ⚡ Conclusion

This lab demonstrates how generative models can learn from sequential data and generate new meaningful sequences. While LSTM models capture short-term dependencies effectively, Transformer models provide better performance for complex and long-range relationships.

---

## 📎 Future Improvements

* Use larger datasets
* Train for more epochs
* Implement GPT-style models
* Add evaluation metrics (BLEU, Perplexity)
* Deploy as a chatbot

---

## 👨‍💻 Author

**Pratik Kumar Sinha**

---

## ⭐ If you found this helpful

Give this repository a ⭐ on GitHub!
