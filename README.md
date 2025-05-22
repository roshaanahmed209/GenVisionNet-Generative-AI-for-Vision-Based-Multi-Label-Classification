# 🧠 GenVisionNet: Generative AI for Vision-Based Multi-Label Classification

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)

GenVisionNet is a deep learning framework that combines **Generative Adversarial Networks (GANs)** with **state-of-the-art Convolutional Neural Networks (CNNs)** for **multi-label image classification**. Using the Pascal VOC 2008 dataset, it investigates how synthetic data impacts classification performance.

---

## 📚 Table of Contents

- [🚀 Project Overview](#-project-overview)
- [📂 Dataset](#-dataset)
- [🔧 Features](#-features)
- [📁 Project Structure](#-project-structure)
- [📈 Results](#-results)
- [🛠 Requirements](#-requirements)
- [▶️ How to Run](#️-how-to-run)
- [🧪 Future Work](#-future-work)
- [📜 License](#-license)
- [👤 Author](#-author)

---

## 🚀 Project Overview

This project explores how **GAN-generated synthetic data** can improve the performance of **pretrained CNN models** on a multi-label image classification task. It uses a **Conditional GAN (cGAN)** to generate additional training data and compares results across multiple architectures and synthetic data volumes.

---

## 📂 Dataset

- **Name**: Pascal VOC 2008
- **Type**: Multi-label image dataset with 20 object classes
- **Structure**:
VOCdevkit/VOC2008/

├── Annotations/

├── JPEGImages/

├── ImageSets/Main/


---

## 🔧 Features

- ✅ **Conditional GAN** for class-wise synthetic image generation
- ✅ **Transfer Learning** with VGG16, ResNet50, DenseNet121, EfficientNet-B0
- ✅ **Evaluation using mean Average Precision (mAP)**
- ✅ **Flexible synthetic data scaling** (100, 200, 500 samples per class)
- ✅ **Visualizations** of GAN output and classification performance

---

## 📁 Project Structure

├── gen-ai-project-final.ipynb # Main notebook with all experiments

├── /gan_synthetic_images # Folder containing generated images

├── /models # Trained CNN model weights

├── /data # Pascal VOC dataset and synthetic images

├── requirements.txt # Dependencies list

├── README.md # Project documentation


---

## 📈 Results

| Model          | No GAN (Baseline) | +100 Samples | +200 Samples | +500 Samples |
|----------------|------------------|--------------|--------------|--------------|
| VGG16          | XX.XX            | XX.XX        | XX.XX        | XX.XX        |
| ResNet50       | XX.XX            | XX.XX        | XX.XX        | XX.XX        |
| DenseNet121    | XX.XX            | XX.XX        | XX.XX        | XX.XX        |
| EfficientNet-B0| XX.XX            | XX.XX        | XX.XX        | XX.XX        |

> 📌 Replace `XX.XX` with your actual mAP values from experiments.

---

## 🛠 Requirements

Install all dependencies using pip:

```bash
pip install -r requirements.txt
git clone https://github.com/roshaanahmed209/GenVisionNet-Generative-AI-for-Vision-Based-Multi-Label-Classification.git
cd GenVisionNet-Generative-AI-for-Vision-Based-Multi-Label-Classification
jupyter notebook gen-ai-project-final.ipynb

```









