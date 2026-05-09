🖼️ CNN Image Classifier — CIFAR-10

A Convolutional Neural Network (CNN) built from scratch using **PyTorch** to classify images into 10 categories, achieving **86.34% accuracy** on the CIFAR-10 dataset. Deployed as an interactive **Gradio** web app.

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)](https://python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)](https://pytorch.org)
[![Gradio](https://img.shields.io/badge/Gradio-FF7C00?style=flat&logo=gradio&logoColor=white)](https://gradio.app)
[![CIFAR-10](https://img.shields.io/badge/Dataset-CIFAR--10-blue?style=flat)](https://www.cs.toronto.edu/~kriz/cifar.html)
[![Accuracy](https://img.shields.io/badge/Accuracy-86.34%25-success?style=flat)]()

---

## 🎯 Overview

This project builds a multi-block CNN architecture that classifies images into **10 categories**:

✈️ Airplane · 🚗 Car · 🐦 Bird · 🐱 Cat · 🦌 Deer
🐶 Dog · 🐸 Frog · 🐴 Horse · 🚢 Ship · 🚛 Truck

---

## 📊 Results

| Metric | Score |
|---|---|
| Best Test Accuracy | **86.34%** |
| Final Training Loss | 0.4696 |
| Dataset | CIFAR-10 (60,000 images) |
| Epochs | 20 |
| Training Device | Google Colab T4 GPU |

### Training Progress
| Epoch | Loss | Accuracy |
|---|---|---|
| 1 | 1.4599 | 57.74% |
| 5 | 0.7525 | 76.73% |
| 10 | 0.5916 | 83.23% |
| 15 | 0.5150 | 84.44% |
| 20 | 0.4696 | **86.34%** |

---

## 🏗️ Model Architecture
Input (3×32×32)
↓
Block 1: Conv(3→32) → BN → ReLU → Conv(32→32) → BN → ReLU → MaxPool → Dropout(0.25)
↓
Block 2: Conv(32→64) → BN → ReLU → Conv(64→64) → BN → ReLU → MaxPool → Dropout(0.25)
↓
Block 3: Conv(64→128) → BN → ReLU → Conv(128→128) → BN → ReLU → MaxPool → Dropout(0.25)
↓
Flatten → FC(512) → BN → ReLU → Dropout(0.5) → FC(10)
↓
Output (10 classes)

**Key techniques used:**
- Batch Normalization — stabilizes training
- Dropout — prevents overfitting
- Data Augmentation — random flip + crop
- Adam optimizer + ReduceLROnPlateau scheduler

---

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Framework | PyTorch |
| Dataset | CIFAR-10 (torchvision) |
| Evaluation | scikit-learn (F1, Confusion Matrix) |
| Deployment | Gradio Web App |
| Training | Google Colab T4 GPU |

---

## 🚀 How to Run

**1. Clone the repo**
```bash
git clone https://github.com/Mohitha1406/cnn-image-classifier
cd cnn-image-classifier
```

**2. Install dependencies**
```bash
pip install torch torchvision gradio scikit-learn matplotlib
```

**3. Open notebook**
```bash
jupyter notebook cnn_image_classifier.ipynb
```

**4. Run all cells** — dataset downloads automatically, trains in ~8 mins on GPU

---

## 🧠 What I Learned

- Building CNN architecture from scratch with multiple conv blocks
- Batch Normalization and Dropout for regularization
- Data augmentation to improve generalization
- Learning rate scheduling with ReduceLROnPlateau
- End-to-end model deployment with Gradio
- 
---

## 👩‍💻 Author

**Cheredla Jasvina**
🔗 [LinkedIn](https://www.linkedin.com/in/jasvina-cheredla) · [GitHub](https://github.com/jasvina3018) · 📧 jasvinachowdarycheredla@gmail.com
