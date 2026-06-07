# 🩺 Chest X-Ray Disease Classification Using CNN
Deep learning-based chest X-ray classification system for detecting COVID-19, Viral Pneumonia, and Normal cases using Convolutional Neural Networks (CNNs)


## Overview

This project implements a **Convolutional Neural Network (CNN)** for the automatic classification of chest X-ray images into three categories:

* COVID-19
* Viral Pneumonia
* Normal

The objective is to develop a deep learning-based system that can assist healthcare professionals in the rapid screening and diagnosis of respiratory diseases using chest X-ray images.

---

## Dataset

The dataset contains chest X-ray images belonging to three classes:

* COVID-19
* Viral Pneumonia
* Normal

Dataset Source:

https://www.kaggle.com/datasets/pranavraikokte/covid19-image-dataset

### Data Distribution

| Class           | Training Images | Testing Images |
| --------------- | --------------- | -------------- |
| COVID-19        | 111             | 26             |
| Viral Pneumonia | 70              | 20             |
| Normal          | 70              | 20             |

---

## Methodology

The project follows the following workflow:

1. Data Collection
2. Image Preprocessing
3. Data Augmentation
4. CNN Model Development
5. Model Training
6. Early Stopping & Model Checkpointing
7. Performance Evaluation
8. Prediction on Test Images

---

## Image Preprocessing

* Image resizing to 224 × 224 pixels
* Pixel normalization (0–255 → 0–1)
* Data organization into training and testing directories

---

## Data Augmentation

To reduce overfitting and improve model generalization, the following augmentation techniques were applied:

* Random Rotation
* Width Shift
* Height Shift
* Random Zoom
* Rescaling
* Nearest Fill Mode

---

## CNN Architecture

The proposed CNN architecture consists of:

* Conv2D (32 Filters, 3×3, ReLU)
* MaxPooling2D
* Conv2D (64 Filters, 3×3, ReLU)
* MaxPooling2D
* Flatten Layer
* Dense Layer (128 Neurons, ReLU)
* Dense Layer (128 Neurons, ReLU)
* Output Layer (3 Neurons, Softmax)

Input Image Size:

224 × 224 × 3

---

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* Scikit-learn
* Google Colab / Jupyter Notebook

---

## Training Improvements

The following techniques were used to improve performance:

### Early Stopping

Stops training when validation accuracy stops improving.

### Model Checkpointing

Automatically saves the best-performing model.

### Data Augmentation

Generates variations of training images to improve robustness.

---

## Results

### Initial CNN Model

* Training Accuracy: 100%
* Validation Accuracy: 95.45%
* Mild overfitting observed

### Augmented CNN Model

* Training Accuracy: 95.22%
* Validation Accuracy: 96.97%
* Better generalization and reduced overfitting

The results demonstrate that CNNs can effectively classify chest X-ray images and distinguish between COVID-19, Viral Pneumonia, and Normal cases.

---

## Project Structure

```text
├── dataset/
│   ├── train/
│   ├── test/
│
├── models/
│   ├── cnn_model.h5
│
├── notebooks/
│   ├── training.ipynb
│
├── results/
│   ├── predictions/
│   ├── plots/
│
├── README.md
```

## Future Work

* Train on larger and more diverse datasets
* Apply Transfer Learning (DenseNet121, ResNet50, EfficientNet)
* Deploy as a web application
* Integrate explainable AI techniques (Grad-CAM)
* Improve multi-class classification performance

---

## Conclusion

This project successfully developed a CNN-based system for classifying chest X-ray images into COVID-19, Viral Pneumonia, and Normal categories. Through preprocessing, data augmentation, and deep learning techniques, the model achieved high classification accuracy and demonstrated the potential of artificial intelligence in medical image analysis and disease detection.

---

## Author

**Tanudip Ghosh**

University Project – Detection and Classification of COVID-19 and Pneumonia from Chest X-Ray Images Using Convolutional Neural Networks.
