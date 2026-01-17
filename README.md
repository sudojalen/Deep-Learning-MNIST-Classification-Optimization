# MNIST Digit Classification with TensorFlow & Keras

## Project Overview
This project involves building a deep learning model to classify handwritten digits (0-9) using the **MNIST dataset**. The goal was to understand the fundamental workflow of a neural network, including data preprocessing, model architecture design, and the compilation process.

## The Dataset
The **MNIST** (Modified National Institute of Standards and Technology) dataset is a "hello world" dataset for computer vision. 
* **Training Data:** 60,000 images of handwritten digits.
* **Testing Data:** 10,000 images used to evaluate model accuracy.
* **Format:** Each image is a 28x28 pixel grayscale image, where each pixel value ranges from 0 (black) to 255 (white).



## Model Architecture
I utilized a **Sequential** model from the Keras API, which allows for a linear stack of layers.

### 1. Layers
* **Dense Layer (Hidden):** A fully connected layer that processes the input data.
* **Softmax Layer (Output):** The final layer uses a softmax activation function to output a probability distribution across the 10 possible digit classes (0-9).



### 2. Compilation Step
To prepare the model for training, I configured three vital components:
* **Optimizer:** This is the algorithm (like `rmsprop` or `adam`) that updates the weights of the neural network to reduce the loss. It determines *how* the model learns.
* **Loss Function:** I used `sparse_categorical_crossentropy`. This measures the "distance" between the model's prediction and the actual label. The goal of training is to minimize this value.
* **Metrics:** I monitored `accuracy` to see the percentage of correctly classified images during training and testing.

## Key Concepts Learned
* **Data Reshaping:** Understanding that the model requires a specific input shape (flattening 28x28 images into a 1D array).
* **Normalization:** Scaling pixel values from [0, 255] to [0, 1] to help the model converge faster.
* **Training vs. Testing:** The importance of keeping a separate test set to ensure the model can generalize to data it hasn't seen before.

## Technical Environment
* **Platform:** Jupyter Notebook (Anaconda)
* **Infrastructure:** Hosted on a Proxmox Virtual Environment (VM)
* **Libraries:** TensorFlow, Keras, Matplotlib, NumPy
