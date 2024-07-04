# Image-Fusion
Image Fusion for Enhanced Shape Classification using LeNet-5

## Overview

This project implements an image fusion strategy to enhance shape classification using a modified LeNet-5 architecture. The synthetic dataset used contains 1000 instances, each having three 32x32 images representing one of the four geometric shapes (pentagon, circle, square, or triangle) with different background types (gradient, noise, and spotlight).

## Project Structure
Image-Fusion-Shape-Classification/
│
├── data/ # Directory for dataset files
│
├── models/ # Directory for storing trained models
│
├── results/ # Directory for storing results like confusion matrices
│
├── notebooks/ # Directory for Jupyter notebooks
│ └── image_fusion.ipynb # Your Google Colab notebook
│
├── report/ # Directory for report files
│ └── final_report.pdf # Your task report
│
├── README.md # Project overview and instructions
│
└── .gitignore # Files and directories to ignore


## How to Run

1. Open the `image_fusion.ipynb` notebook in Google Colab.
2. Follow the instructions in the notebook to train and evaluate the models.
3. Results, including confusion matrices and accuracy, will be stored in the `results/` directory.

## Dependencies

- Python 3.x
- TensorFlow
- NumPy
- Matplotlib

You can install the dependencies using pip:

```bash
pip install tensorflow numpy matplotlib
```
Methodology

Change LeNet5 Architecture:

Modified the original LeNet-5 architecture to handle larger, grayscale images and distinguish between four classes (geometric shapes).
Train and Evaluate LeNet without Fusion:

Trained three separate LeNet-5 models on images with different background types (gradient, noise, spotlight).
Evaluated each model's accuracy using confusion matrices.
Implementing Fusion Strategy:

Low-Level Fusion: Combined the pixel values of the three images using pixel-based average fusion.
High-Level Fusion: Merged the results of models trained on different image backgrounds using majority voting.
Train and Evaluate LeNet with Fusion:

Trained a new LeNet-5 model on the fused dataset.
Evaluated the combined model's accuracy and compared it with individual models.
Results

The fusion strategy significantly improved the classification accuracy. The following table summarizes the accuracy of different models:

Models and Accuracies
Model 1 - Gradient Background	70.0%
Model 2 - Noise Background	61.5%
Model 3 - Spotlight Background	71.5%
Low-Level Fusion (Average Selection)	77.5%
Low and High-Level Fusion (Majority Voting)	82.5%

