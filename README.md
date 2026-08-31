# 🧠 Brain Tumor Classification & Segmentation

## 📌 Project Overview

This project focuses on applying Deep Learning techniques to brain MRI images for two important tasks:

1. **Brain Tumor Classification** – Identifying the type of brain tumor from an MRI image.
2. **Brain Tumor Segmentation** – Detecting and segmenting the tumor region within the MRI image.

The project was developed using the **BRISC2025 dataset** and implemented using **TensorFlow and Keras**.

---

# 👩‍💻 Team Members

| Name            | Responsibility             |
| --------------- | -------------------------- |
| **Malak Ahmed** | Brain Tumor Classification |
| **Aya Emad**    | Brain Tumor Segmentation   |

---

# 📂 Dataset

The project uses the **BRISC2025 dataset**, which contains brain MRI images for both classification and segmentation tasks.

The dataset includes:

* MRI brain images
* Tumor classification labels
* Tumor segmentation masks
* Training and testing data

---

# 🔹 Part 1: Brain Tumor Classification

### 👩‍💻 Developed by: Malak Ahmed

The classification task aims to predict the type of brain tumor from an MRI image.

### Classes

The model classifies MRI images into four categories:

* Glioma
* Meningioma
* No Tumor
* Pituitary Tumor

---

## 🔄 Data Preprocessing

The following preprocessing and augmentation techniques were applied:

* Image resizing to **512 × 512**
* Image normalization using rescaling
* Rotation augmentation
* Horizontal flipping
* Vertical flipping
* Training and validation split

---

## 🧠 Classification Model

A Convolutional Neural Network (CNN) was built using TensorFlow/Keras.

The model includes:

* Convolutional Layers
* Batch Normalization
* Max Pooling
* Dropout Layers
* Dense Layers

The model was trained using:

* **Optimizer:** Adam
* **Loss Function:** Categorical Crossentropy
* **Metric:** Accuracy

Additional callbacks were used to improve training:

* Early Stopping
* Reduce Learning Rate on Plateau

---

## 🚀 Deployment

The trained classification model was integrated into a simple API using:

* FastAPI
* TensorFlow
* Uvicorn

The API allows users to upload an MRI image and receive a prediction of the tumor class.

---

# 🔹 Part 2: Brain Tumor Segmentation

### 👩‍💻 Developed by: Aya Emad

The segmentation task aims to identify the exact tumor region in a brain MRI image.

Instead of predicting only the tumor class, segmentation predicts a mask that highlights the location of the tumor.

---

## 🔄 Data Preprocessing

The segmentation pipeline includes:

* Loading MRI images and corresponding masks
* Image resizing to **224 × 224**
* Image normalization
* Binary mask conversion
* Training and validation split
* TensorFlow `tf.data` pipeline
* Batch processing and prefetching

A subset of images was also separated as unseen deployment data.

---

## 🧠 Segmentation Model

A **U-Net architecture** was implemented for tumor segmentation.

The architecture consists of:

### Encoder

The encoder extracts important features from MRI images using:

* Convolutional layers
* ReLU activation
* Max Pooling

### Decoder

The decoder reconstructs the segmentation mask using:

* Transposed Convolution
* Skip Connections
* Feature Concatenation

The final layer uses a **Sigmoid activation function** to produce a binary tumor mask.

---

## 📊 Loss Function

The segmentation model uses a combination of:

* Binary Cross Entropy
* Dice Loss

### Combined Loss

```text
Combined Loss = Binary Cross Entropy + Dice Loss
```

This combination helps the model learn the tumor region more effectively.

---

## 📈 Evaluation Metrics

The segmentation model was evaluated using:

* Dice Coefficient
* Binary Accuracy
* Intersection over Union (IoU)

For medical image segmentation, Dice Score and IoU are particularly important because they measure the overlap between the predicted tumor mask and the ground truth mask.

---

# 🛠️ Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib
* Seaborn
* FastAPI
* Kaggle / KaggleHub

---



for the Brain Tumor Segmentation task.

---

# 🎯 Project Goal

The goal of this project is to demonstrate how Deep Learning can be applied to medical imaging for:

* Classifying brain tumors
* Identifying tumor locations
* Processing MRI images
* Building Deep Learning models
* Evaluating model performance
* Preparing AI models for real-world deployment

---

# ⚠️ Disclaimer

This project is developed for educational and research purposes only.

The models are not intended to replace professional medical diagnosis or clinical decision-making.

---

# 👩‍💻 Contributors

**Malak Ahmed**
Brain Tumor Classification

**Aya Emad**
Brain Tumor Segmentation
