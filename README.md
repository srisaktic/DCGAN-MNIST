<h1 align="center">🧠 DCGAN on MNIST</h1>

<p align="center">
  Handwritten Digit Generation using Deep Convolutional GANs 🚀
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Deep Learning-GAN-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Model-DCGAN-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Dataset-MNIST-orange?style=for-the-badge" />
</p>

---

## 🎯 Project Overview

<p align="center">
This project implements a <b>Deep Convolutional Generative Adversarial Network (DCGAN)</b> to generate realistic handwritten digits using the MNIST dataset.
</p>

<p align="center">
The focus is on understanding how architectural design choices, activation functions, and hyperparameter tuning influence the quality and stability of generated images.
</p>

---

## 🎓 Project Context

<p align="center">
Developed as part of a <b>Deep Learning course</b> during my Master’s in Data Science at NYIT, this project demonstrates practical implementation of GANs and experimental evaluation of model behavior.
</p>

---

## ⚙️ How It Works

<table align="center">
<tr>
<td>

🔹 Generator creates fake digit images from random noise  
🔹 Discriminator classifies real vs fake images  
🔹 Both models train in an adversarial setup  
🔹 Generator improves over time to produce realistic digits  

</td>
</tr>
</table>

---

## 🧪 Experimental Setup

### ✅ Baseline Model

- Noise Vector (z-dim): 100  
- Activation: LeakyReLU  
- Batch Size: 64  
- Learning Rate: 1e-4  
- Momentum: 0.9  

---

### 🧪 Experiment 1: Epoch Comparison

| Epoch | Observation |
|------|------------|
| 10   | Noisy, unclear digits |
| 50   | Improved structure and clarity |
| 100  | High-quality, stable digit generation |

---

### 🧪 Experiment 2: Activation Functions

| Activation | Observation |
|------------|------------|
| LeakyReLU  | Stable training, consistent results |
| ReLU       | Sharper digits, smoother convergence |

---

### 🧪 Experiment 3: Hyperparameter Tuning

| Parameter       | Baseline | Modified |
|----------------|----------|----------|
| Noise Vector   | 100      | 200      |
| Batch Size     | 64       | 256      |
| Learning Rate  | 1e-4     | 1e-3     |
| Momentum       | 0.9      | 0.7      |

🔎 **Result:** Modified configuration led to unstable outputs and noisy images due to aggressive learning rate and reduced momentum.

---

## 📊 Results Summary

<p align="center">

🏆 Best Model: <b>Baseline (LeakyReLU, Epoch 100)</b><br>
✨ Sharpest Output: <b>ReLU at Epoch 50</b><br>
⚠️ Worst Performance: <b>Modified Hyperparameters</b>

</p>

---

## 📌 Key Insights

<ul align="center">
<li>GAN training stability is highly sensitive to hyperparameters</li>
<li>LeakyReLU improves training stability</li>
<li>ReLU produces sharper outputs but may risk instability</li>
<li>Higher learning rates can degrade GAN performance</li>
</ul>

---

## 🧱 Model Architecture

<p align="center">
<b>Noise Vector → Generator → Fake Image → Discriminator → Real/Fake Prediction</b>
</p>

---

## 📂 Project Structure

```bash
dcgan-mnist/
│
├── generator.py
├── discriminator.py
├── training.ipynb
├── outputs/
├── models/
└── README.md
