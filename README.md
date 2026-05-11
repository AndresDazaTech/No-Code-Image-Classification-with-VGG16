# 🖼️ L01: Deep Learning Exploration 
### *No-Code Image Classification with VGG16*

[![TensorFlow](https://img.shields.io/badge/Framework-TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)
[![Keras](https://img.shields.io/badge/API-Keras-D00000?style=flat-square&logo=keras&logoColor=white)](https://keras.io/)
[![VGG16](https://img.shields.io/badge/Architecture-VGG16-blue?style=flat-square)](https://arxiv.org/abs/1409.1556)
[![Google Colab](https://img.shields.io/badge/Environment-Google--Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white)](https://colab.research.google.com/)

## 📌 Overview
This lab serves as a foundational introduction to **Deep Learning (DL)** by interacting with **VGG16**, a world-class pre-trained Convolutional Neural Network (CNN). Instead of training a model from scratch, this project focuses on **Model Inference**—the process of using a trained "brain" to recognize patterns in new data.

The project demonstrates the critical role of **Data Preprocessing** and how high-level APIs like Keras make sophisticated AI accessible for rapid prototyping and deployment.

---

## 🎯 Learning Objectives
*   **Workflow Intuition:** Experience the end-to-end lifecycle of a DL project (Input → Preprocess → Inference → Output).
*   **Architectural Awareness:** Understand the structure of VGG16 and its historical significance in the ImageNet challenge.
*   **Input Sensitivity:** Observe how subtle changes in image filters, resolution, and color channels affect AI confidence.
*   **Framework Proficiency:** Utilize Keras and TensorFlow to load weights and execute classification tasks.

---

## 🧠 The "Brain": VGG16 Architecture
VGG16 is a landmark model in the field of Computer Vision, known for its simplicity and depth.

*   **Trained On:** ImageNet (1.2 million images).
*   **Capability:** Can recognize **1,000 different object categories**.
*   **Depth:** 16 layers with weights (13 Convolutional, 3 Fully Connected).
*   **Parameters:** ~138 Million.
*   **Input Requirement:** 224 × 224 pixels, RGB.

---

## 🧪 Technical Workflow
The notebook automates the following pipeline:
1.  **Model Loading:** Instantiates VGG16 with weights pre-trained on ImageNet.
2.  **Preprocessing (Critical Step):**
    *   Resizing images to $224 \times 224$.
    *   Converting images to NumPy arrays.
    *   **Mean Subtraction:** Adjusting pixel values to match the distribution the model was trained on.
3.  **Inference:** Passing the processed tensor through the network.
4.  **Decoding:** Translating the raw output vector into human-readable labels (e.g., "Golden Retriever", "Space Shuttle").

---

## 📊 Key Insights & Observations

### 1. The Preprocessing "Gatekeeper"
The most significant takeaway is that **AI is only as good as its input**. Passing a raw image without proper resizing or color-space normalization resulted in "hallucinated" predictions. Preprocessing is not an option; it is a requirement.

### 2. Feature Hierarchy
By testing various images, the lab illustrates how the CNN looks for **features** (edges, textures, shapes) rather than just "pixels." When an image is blurry or heavily filtered, the model loses its ability to detect these features, causing confidence scores to drop.

### 3. Transfer Learning Foundation
This lab demonstrates the power of **Inference-only workflows**. It proves that developers can build powerful tools (like automated photo tagging) by "borrowing" the intelligence of existing models without needing massive GPU clusters for training.

---

## 🛠️ Tools & Libraries
*   **Engine:** TensorFlow / Keras
*   **Image Processing:** PIL (Pillow), NumPy
*   **Visualization:** Matplotlib
*   **UI/UX:** `ipywidgets` (for the interactive image uploader)

---

## 🚀 How to Use
1.  Open the notebook in **Google Colab**.
2.  Run the setup cells to load the VGG16 weights.
3.  Use the **Upload Button** to provide any image from your computer.
4.  Observe the Top-3 predictions and the percentage of confidence for each.

---

## 👤 Author
**Andres Daza**    
Houston Community College — ITAI 2376
