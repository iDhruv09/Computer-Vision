# 🧠 CNN Padding & Stride Experiments (MNIST)

This project explores how **padding and stride configurations affect the performance of Convolutional Neural Networks (CNNs)** when classifying handwritten digits from the **MNIST dataset**.

The notebook runs multiple CNN experiments using different **padding strategies and stride values** and compares their impact on:

- Model accuracy
- Training time
- Feature map behavior
- Parameter count

---

# 📌 Project Overview

Convolutional Neural Networks use **filters** to extract spatial features from images. Two key hyperparameters in convolution layers are:

## 1️⃣ Padding
Padding determines how the borders of the image are handled during convolution.

Types used in this experiment:

- **Same Padding**
  - Keeps the output size equal to the input size
  - Preserves edge information

- **Valid Padding**
  - No padding applied
  - Output feature maps shrink after convolution

---

## 2️⃣ Stride
Stride determines how far the convolution filter moves at each step.

Stride values tested:

- **Stride = 1** → detailed feature extraction  
- **Stride = 2** → faster downsampling  
- **Stride = 3** → aggressive spatial reduction  

---

# 🧪 Experiments Conducted

The following configurations were tested:

| Experiment | Padding | Stride |
|--------|--------|--------|
| Baseline | same | 1 |
| No Padding | valid | 1 |
| Downsample | same | 2 |
| Downsample | valid | 2 |
| Aggressive Downsample | same | 3 |

Each experiment trains a CNN on MNIST and records:

- Test accuracy
- Validation accuracy
- Training time
- Model parameters

---

# 🏗 CNN Architecture

The model architecture used for experiments:
