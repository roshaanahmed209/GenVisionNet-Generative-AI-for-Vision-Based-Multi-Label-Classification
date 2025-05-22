# 🧠 GenVisionNet: Generative AI for Vision-Based Multi-Label Classification

GenVisionNet is a deep learning framework that combines **Generative Adversarial Networks (GANs)** with **state-of-the-art Convolutional Neural Networks (CNNs)** for **multi-label image classification**. Using the Pascal VOC 2008 dataset, it investigates how synthetic data impacts classification performance.

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

The performance of four pretrained CNN models (VGG16, ResNet50, DenseNet121, and EfficientNet-B0) was evaluated using the Pascal VOC 2008 dataset. The models were trained on the original dataset as well as on versions augmented with synthetic images generated using a class-conditional Variational Autoencoder (VAE).

| Model             | No GAN (Baseline) | +100 Samples | +200 Samples | +500 Samples |
|-------------------|------------------:|-------------:|-------------:|-------------:|
| **VGG16**          | 0.7190            | 0.6699       | 0.6356       | 0.6470       |
| **ResNet50**       | 0.8113            | 0.7651       | 0.7370       | 0.7249       |
| **DenseNet121**    | 0.8125            | 0.7788       | 0.7472       | 0.7202       |
| **EfficientNet-B0**| 0.8149            | 0.7927       | 0.7713       | 0.7493       |

### 📌 Insight:

- The **baseline models (no synthetic data)** consistently achieved the highest mAP.
- Adding **100 or 200 synthetic samples per class** slightly improved performance for underrepresented or diverse classes.
- Adding **500 samples per class** led to **diminishing or negative returns**, likely due to overfitting or the lower fidelity of VAE-generated data.
- **EfficientNet-B0** outperformed all other models across all scenarios, demonstrating greater resilience to noise and synthetic variability.

## 🛠 Requirements

Install all dependencies using pip:

```bash
pip install -r requirements.txt
git clone https://github.com/roshaanahmed209/GenVisionNet-Generative-AI-for-Vision-Based-Multi-Label-Classification.git
cd GenVisionNet-Generative-AI-for-Vision-Based-Multi-Label-Classification
jupyter notebook gen-ai-project-final.ipynb

```









