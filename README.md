# Deep Learning Backpropagation Regression Demo

This repository contains a starter-phase deep learning model demonstrating backpropagation for a regression task. It is designed to help beginners understand how neural networks update their weights to make numerical predictions. 

## Overview
The project uses a small custom dataset to predict a candidate's `lpa` (Lakhs Per Annum) based on two features: `cgpa` and `profile_score`[cite: 1, 2]. The dataset consists of 4 sample rows[cite: 1, 2]. 

To demonstrate the underlying mechanics of deep learning, this repository tackles the same problem using two different approaches:
1.  **TensorFlow/Keras Implementation**
2.  **From-Scratch NumPy Implementation**

## Model Architecture
Both implementations build the same simple network:
*   **Input Layer:** Takes 2 input features (`cgpa` and `profile_score`)[cite: 1, 2].
*   **Hidden Layer:** A dense layer with 2 neurons and a linear activation function[cite: 1].
*   **Output Layer:** A dense layer with 1 neuron predicting the final continuous value (`lpa`)[cite: 1, 2].

## Implementations

### 1. Using TensorFlow and Keras
*   Uses a `Sequential` model to stack the dense layers[cite: 1].
*   Initializes the model with custom starting weights (0.1) and biases (0.0)[cite: 1].
*   Compiles the model using Mean Squared Error loss and the Adam optimizer with a learning rate of 0.001[cite: 1].
*   Trains the model over 75 epochs with a batch size of 1[cite: 1].

### 2. From Scratch using NumPy
*   Implements the neural network mathematics purely using Python and NumPy, without relying on deep learning frameworks[cite: 2].
*   Includes custom functions for parameter initialization (`initialize_parameters`)[cite: 2].
*   Calculates predictions manually via a linear forward propagation function (`L_layer_forward`)[cite: 2].
*   Updates the network's weights and biases manually using a custom backpropagation function (`update_parameters`)[cite: 2].
*   Loops through 5 training epochs, printing the progressively decreasing Mean Squared Error loss[cite: 2].

## Dependencies
To run the notebooks in this repository, you will need the following libraries:
*   `numpy`[cite: 1, 2]
*   `pandas`[cite: 1, 2]
*   `tensorflow` (and `keras`)[cite: 1]
