# ForgeryDetectNet

## Table of Contents

1. Introduction
2. Data Preparation and Preprocessing
3. Data Loading and Transformation
4. Model Architecture and Training
5. Model Evaluation and Testing
6. Saving the Trained Model
7. Making Predictions on New Data

## 1. Introduction

The documented solution is aimed at detecting document forgery using a deep learning-based approach. The process involves data preparation, model creation, training, evaluation, and testing. The solution utilizes Python, PyTorch, and related libraries for image processing and deep learning tasks.

## 2. Data Preparation and Preprocessing

The initial step involves organizing the data into genuine and forged document categories. The data is split into training and testing sets using the 'train_test_split' function from the sklearn library. Files are then moved to their respective folders for further processing.

## 3. Data Loading and Transformation

Data loading and transformation are essential for preparing the data for the deep learning model. The 'ImageFolder' class from the torchvision library is used to load the images, and transformations are applied using the 'Compose' class. These transformations include resizing, cropping, and normalization to standardize the input data.

## 4. Model Architecture and Training

A Convolutional Neural Network (CNN) architecture based on the ResNet18 model is used for the forgery detection task. The model is defined as the 'ForgeryDetectionCNN' class, with necessary modifications to the fully connected layer for the desired number of classes. The model is trained using the training data, with the 'SGD' optimizer and the 'CrossEntropyLoss' criterion.

## 5. Model Evaluation and Testing

The trained model is evaluated on the test dataset to measure its performance. The accuracy of the model is calculated based on the number of correctly predicted labels over the total number of labels in the test dataset.

## 6. Saving the Trained Model

The trained model is saved in the '.pth' format using the 'torch.save' function. This allows for the model to be reused or deployed for future predictions or real-time forgery detection tasks.

## 7. Making Predictions on New Data

The solution includes a function to make predictions on new data. This function takes an image file path as input, preprocesses the image, and feeds it into the trained model for prediction. The predicted class is then displayed based on the trained classes ('genuine' and 'forged').

The provided solution showcases an end-to-end process for document forgery detection, including data preparation, model training, evaluation, and prediction. It serves as a comprehensive guide for understanding and implementing a deep learning-based approach for document forgery detection.
