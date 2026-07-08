# Adaptive Noise Cancellation: Classical vs. Deep Learning Approaches

This repository contains two linked projects exploring the evolution of Adaptive Noise Cancellation (ANC) techniques for digital signal processing. The goal of both projects is to successfully isolate a target audio signal from environmental interference by modeling the physical acoustic channel.

## Homework 1 (HW1): Classical Adaptive Filtering
The first project establishes a baseline using classical statistical signal processing. 
* **Approach:** Implements linear regression and adaptive filtering.
* **Mechanism:** Engineers temporal context by manually constructing Toeplitz matrices of delayed reference samples to act as a linear Finite Impulse Response (FIR) filter.
* **Key Takeaway:** Demonstrates strong performance on stationary noise but highlights the computational limitations of matrix inversion and manual feature engineering.

## Homework 2 (HW2): Deep Representation Learning
The second project modernizes the pipeline by replacing classical filters with end-to-end deep neural networks using PyTorch.
* **Approach:** Implements 1D Convolutional Neural Networks (CNNs).
* **Mechanism:** Replaces manually delayed samples with a sliding-window sequence strategy. The CNN automatically learns to act as an adaptive, non-linear FIR filter.
* **Key Takeaway:** Proves that deep models can automatically learn the underlying physics of an acoustic room channel. Includes controlled experiments on noise variance, window length, and network capacity, culminating in the successful noise reduction of real human speech audio files.

## Technologies & Libraries
* Python
* PyTorch (Deep Learning)
* SciPy & Librosa (Digital Signal Processing)
* NumPy & Matplotlib (Data Manipulation and Visualization)
