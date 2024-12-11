# Diabetic Retinopathy Classification Project

## Overview

This repository contains various machine learning and deep learning models aimed at diagnosing diabetic retinopathy using retinal images. The models include Convolutional Neural Networks (CNN), EfficientNet, Inception V3, and a stacking method for EfficientNet models. These models are designed to classify retinal images into one of five categories:

- **Mild DR**
- **Moderate DR**
- **No DR**
- **Proliferate DR**
- **Severe DR**

The project includes the following files, each implementing different methods or strategies for image classification:

## File Descriptions

### 1. `CNN Project.ipynb`
This Jupyter notebook implements a basic Convolutional Neural Network (CNN) model to classify diabetic retinopathy images. The CNN architecture includes convolution layers for feature extraction, pooling layers for dimensionality reduction, and fully connected layers for classification. 

**Main features**:
- Simple CNN model for image classification.
- Trains and evaluates the model using the diabetic retinopathy dataset.
  
### 2. `DenseNet+XGboost.ipynb`
This notebook combines the DenseNet architecture with XGBoost for classification. DenseNet is used for feature extraction, followed by an XGBoost classifier to enhance the model’s prediction capabilities. This method integrates convolutional neural networks with a powerful gradient boosting algorithm for improved accuracy.

**Main features**:
- Combines DenseNet (a deep CNN) with XGBoost for a hybrid approach.
- Works for classification of retinal images into different diabetic retinopathy categories.

### 3. `K-Fold EfficientNet Updated.ipynb`
This notebook applies K-fold cross-validation to an EfficientNet model. The dataset is divided into K equally sized subsets, and the model is trained and evaluated K times, ensuring more robust and generalized performance.

**Main features**:
- Implements K-fold cross-validation for EfficientNet.
- Ensures better model generalization and reduces overfitting.
  
### 4. `Stacking EfficientNet.ipynb`
This notebook demonstrates the stacking technique for multiple EfficientNet models. It trains multiple EfficientNet models on different subsets of the data, then uses a meta-model to combine predictions from each of the individual models. This ensemble method enhances performance by leveraging diverse predictions.

**Main features**:
- Stacks multiple EfficientNet models for improved prediction accuracy.
- Uses a meta-model to combine predictions and produce a final result.

### 5. `efficientnet.ipynb`
This notebook builds and trains an EfficientNet model for classifying diabetic retinopathy images. EfficientNet is a highly efficient convolutional neural network architecture that balances model accuracy and computational efficiency.

**Main features**:
- Implements EfficientNet for image classification.
- Aims for high accuracy with computational efficiency using the compound scaling technique.

### 6. `inception v3.ipynb`
This Jupyter notebook implements the Inception V3 model for diabetic retinopathy classification. Inception V3 uses multiple convolution layers of different sizes (1x1, 3x3, 5x5) to capture information at different scales, making it highly effective for image classification tasks.

**Main features**:
- Implements the Inception V3 architecture for classification.
- Efficiently captures hierarchical features through multiple convolution sizes.

### 7. `README.md`
This file. It describes the overall project, explains the functionality of the various Jupyter notebooks, and provides guidance on running and using the models in the repository.

## Dataset

The dataset used in this project contains retinal images categorized into five classes representing different stages of diabetic retinopathy:

- **Mild DR**
- **Moderate DR**
- **No DR**
- **Proliferate DR**
- **Severe DR**

The images are resized to 224x224 pixels to be compatible with the deep learning models. Each image is labeled according to the severity of diabetic retinopathy.

## Requirements

To run the notebooks, you need the following Python libraries:

- **TensorFlow** or **Keras**
- **NumPy**
- **Pandas**
- **OpenCV**
- **Matplotlib**
- **XGBoost**
- **Scikit-learn**

You can install the required packages using pip:

```bash
pip install tensorflow keras numpy pandas opencv-python matplotlib xgboost scikit-learn
```

## Running the Notebooks
1. Training a Model
To train a model, simply open the corresponding Jupyter notebook and run the cells. Each notebook contains the necessary code to load the dataset, preprocess the images, train the model, and evaluate its performance.

2. Inference
Once a model is trained, you can use it to predict diabetic retinopathy in new retinal images:


## Results
- CNN Model: Accuracy: 85%
- DenseNet + XGBoost: Accuracy: 92%
- EfficientNet: Accuracy: 91%
- Inception V3: Accuracy: 90%
- Stacked EfficientNet: Accuracy: 95%
- The stacked EfficientNet model provided the best performance, demonstrating the power of ensemble learning for image classification tasks.




