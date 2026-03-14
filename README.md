# mlp_vs_cnn_cats_dogs_classification
This repository explores binary image classification using two different deep learning approaches: a Multi-Layer Perceptron (MLP) enhanced by an unsupervised Autoencoder and a Convolutional Neural Network (CNN).
# Overview
The goal was to evaluate how different architectures handle spatial structure in images. While MLPs struggle with pixel-level variations, I addressed this using an unsupervised pre-training stage (Autoencoder) to learn meaningful latent features before classification.
# Key Methodologies
* Unsupervised Pre-training: Used an MLP Autoencoder to compress 64x64 images into a 256-dimensional latent space, reducing noise and capturing essential features.
* Data Augmentation: Implemented RandomRotation, HorizontalFlip, and ColorJitter to improve generalization and simulate real-world variations.
* CNN Implementation: Leveraged 3x3 kernels, BatchNormalization, and MaxPool2d to automatically learn hierarchical spatial patterns.
* Optimization: Both models were trained using the Adam optimizer with a learning rate of $1e-3$ and a batch size of 32.
# Performance Comparison

| Model Architecture | Test Accuracy | Key Observations |
| :--- | :---: | :--- |
| **MLP + Autoencoder** | 61.5% | Performance boost of 2% compared to random initialization; slight bias towards "Cats". |
| **CNN** | **76.4%** | Significant improvement; efficiently learns hierarchical textures and edges. |
