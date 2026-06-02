# 🌸 Flower Image Classification Using CNNs and Transfer Learning

## Overview

This project focuses on classifying flower images into five categories:

* Daisy
* Dandelion
* Rose
* Sunflower
* Tulip

The objective is to compare the performance of custom Convolutional Neural Networks (CNNs) with a transfer learning approach using MobileNetV2. The project evaluates model accuracy, computational efficiency, training time, and generalization capability on a real-world flower image dataset.

## Dataset

The dataset contains over 4,300 labeled flower images distributed across five classes.

### Data Preprocessing

* Image resizing to **224 × 224**
* Image normalization
* Data augmentation:

  * Rotation
  * Horizontal flipping
  * Zooming
* Removal of corrupted images
* Stratified 80/20 train-test split

## Models Implemented

### 1. Baseline CNN

A lightweight CNN architecture consisting of:

* 3 Convolutional Layers
* Max Pooling Layers
* Fully Connected Dense Layers
* Softmax Output Layer

Used as a benchmark for performance comparison.

### 2. Deep CNN

An enhanced architecture featuring:

* 8 Convolutional Layers
* Batch Normalization
* Dropout Regularization
* L2 Regularization
* Multiple Dense Layers

Designed to improve feature extraction and reduce overfitting.

### 3. Transfer Learning (MobileNetV2)

A pre-trained MobileNetV2 model trained on ImageNet:

* Frozen base layers
* Global Average Pooling
* Dense Classification Layers
* Dropout Regularization
* Fine-tuning of upper layers

This approach leverages learned visual features for improved accuracy and faster convergence.

## Results

| Model                         | Test Accuracy |
| ----------------------------- | ------------- |
| Baseline CNN (Adam)           | 69%           |
| Deep CNN (Adam)               | 76%           |
| MobileNetV2 Transfer Learning | 91%           |

### Key Findings

* Deep CNN significantly reduced overfitting compared to the baseline model.
* Adam optimizer consistently outperformed SGD.
* MobileNetV2 achieved the highest accuracy while requiring less training time.
* Transfer learning proved highly effective for limited computational resources.

## Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook

## Future Improvements

* Implement advanced augmentation techniques using GANs.
* Experiment with EfficientNet, DenseNet, and ResNet architectures.
* Perform extensive hyperparameter tuning.
* Deploy the best-performing model as a mobile application for real-time flower recognition.

## Conclusion

The project demonstrates that deeper CNN architectures improve classification performance, but transfer learning with MobileNetV2 delivers the best balance of accuracy, training speed, and computational efficiency. The final MobileNetV2 model achieved approximately **91% test accuracy**, making it the most effective solution among all evaluated approaches.
