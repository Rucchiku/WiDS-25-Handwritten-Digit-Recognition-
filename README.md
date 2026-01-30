Handwritten Digit Recognition using Convolutional Neural Networks
Project Overview

This project implements a Handwritten Digit Recognition system using Convolutional Neural Networks (CNNs) with TensorFlow and Keras. The model is trained on the MNIST dataset, which contains grayscale images of handwritten digits (0–9).

The objective of this project is to demonstrate the complete deep learning workflow including data preprocessing, model design, training, evaluation, and testing, while understanding how CNNs extract spatial features from images.

Dataset

Dataset Used: MNIST Handwritten Digits

Number of Classes: 10 (digits 0–9)

Image Size: 28 × 28 pixels

Color Format: Grayscale

The dataset is loaded directly using TensorFlow’s built-in dataset loader.

Technologies and Libraries Used

Python

TensorFlow / Keras

NumPy

Matplotlib

Project Workflow
1. Data Loading

The MNIST dataset is loaded and split into:

Training data

Testing data

Each image represents a handwritten digit.

2. Data Preprocessing

The following preprocessing steps are applied:

Pixel values are normalized (scaled from 0–255 to 0–1)

Images are reshaped to match CNN input format
(28, 28, 1)

Labels remain as digit classes (0–9)

This improves training stability and convergence speed.

3. Model Architecture

The CNN model consists of the following layers:

Convolutional Layer

Extracts spatial features using filters

Max Pooling Layer

Reduces spatial dimensions and computation

Flatten Layer

Converts feature maps into a 1D vector

Fully Connected (Dense) Layers

Performs classification

Output Layer

Uses Softmax activation to predict digit probabilities

This layered structure allows the model to learn low-level features (edges) and high-level features (digit shapes).

4. Model Compilation

The model is compiled using:

Loss Function: Sparse Categorical Crossentropy

Optimizer: Adam

Evaluation Metric: Accuracy

This setup is suitable for multi-class classification problems.

5. Model Training

The model is trained using training data

Validation is performed on test data

Training occurs over multiple epochs to minimize loss

During training, the model learns optimal weights through backpropagation.

6. Model Evaluation

After training:

The model is evaluated on unseen test data

Accuracy and loss values are analyzed

Predictions can be visualized for sample images

This step verifies the generalization ability of the CNN.

Results

The trained CNN achieves high classification accuracy on handwritten digit images.

The model successfully identifies digits from 0 to 9 with minimal error.

CNN outperforms traditional neural networks due to its ability to capture spatial patterns.
