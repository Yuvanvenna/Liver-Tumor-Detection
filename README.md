# Liver Tumor Detection using Quantum-Inspired Encoding and CNN

This project implements a liver tumor classification framework that integrates **quantum-inspired angle encoding** with a **Convolutional Neural Network (CNN)** to classify liver CT slices into **normal**, **benign tumor**, or **malignant tumor** classes.

---

## 🧠 Motivation

Early and accurate detection of liver cancer is critical for effective treatment. However, limited labeled datasets, overlapping tumor features, and class imbalance make traditional deep learning approaches less effective. This project addresses these challenges using quantum-inspired feature transformations to enrich medical image representations, thereby improving classification accuracy with limited data.

---

## 📂 Dataset

**LiTS17 (Liver Tumor Segmentation Challenge 2017)**  
- 201 contrast-enhanced 3D CT scans  
- 131 training, 70 test cases  
- Covers diverse liver tumor types (HCC, metastases, etc.)  
- Source: [LiTS Challenge](https://competitions.codalab.org/competitions/17094)

> All slices are preprocessed (normalization, resizing, ROI extraction) before quantum encoding.

---

## 🔬 Methodology

### 🔹 1. Quantum-Inspired Feature Encoding
- Pixel intensities normalized to [0, π]
- Encoded into two channels: `sin(θ)` and `cos(θ)`
- Tensor shape: `(2, H, W)` per slice
- Simulates quantum state representation:  
  `|ψ⟩ = cos(θ)|0⟩ + sin(θ)|1⟩`

### 🔹 2. CNN Classifier
- Input: 2-channel encoded images
- Architecture: Convolution → ReLU → MaxPooling → Dense → Softmax
- Output: Class probabilities for  
  **Normal**, **Benign**, or **Malignant** tumors

---

## 📊 Results

- Accuracy achieved: ~**90%**
- High sensitivity for **malignant tumor detection**
- Evaluation metrics: **Precision**, **Recall**, **F1-Score**, **Confusion Matrix**
- Grad-CAM used for explainability

> Detailed plots of accuracy/loss curves, probability distributions, and confusion matrix are available in the `/results` folder.

---

## 🛠️ Tools and Technologies

`Python`, `PyTorch`, `NumPy`, `Matplotlib`, `Skimage`, `scikit-learn`, `Qiskit (inspired method)`

---

## 🔮 Future Work

- Integrate with **federated learning** for privacy-preserving training across hospitals  
- Extend to **3D CNNs** for volumetric classification  
- Enable real-time inference in clinical settings

---

## 📜 License

This project is licensed under the MIT License.
