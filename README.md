# MNIST Digit Classification: Architecture & Compilation

## Project Overview
This project focuses on the foundational setup of a deep learning model to classify handwritten digits (0-9) using the **MNIST dataset**. The scope of this phase was to complete the initial workflow, including data preprocessing, model architecture design, and the final compilation of the network.

**Note:** This repository currently covers the model configuration and compilation steps. Training and evaluation phases are documented as the next steps in development.

<img width="1171" height="500" alt="image" src="https://github.com/user-attachments/assets/c69c28c5-cbee-4bfc-9933-6f0acc18cf01" />

## The Dataset
The **MNIST** (Modified National Institute of Standards and Technology) dataset is a "hello world" dataset for computer vision. 
* **Training Data:** 60,000 images of handwritten digits.
* **Testing Data:** 10,000 images used to evaluate model accuracy.
* **Format:** Each image is a 28x28 pixel grayscale image, where each pixel value ranges from 0 (black) to 255 (white).

<img width="1167" height="129" alt="image" src="https://github.com/user-attachments/assets/6193567d-cd16-446e-9a74-342089afb2d7" />

## Model Architecture
I utilized a **Sequential** model from the Keras API, which allows for a linear stack of layers.

### 1. Layers
* **Dense Layer (Hidden):** A fully connected layer that processes the input data.
* **Softmax Layer (Output):** The final layer uses a softmax activation function to output a probability distribution across the 10 possible digit classes (0-9).

### 2. Compilation Step
To prepare the model for future training, I configured the three vital components that dictate how the network learns:

* **Optimizer:** Defined the algorithm that updates the weights of the neural network to reduce the loss.
  <img width="1166" height="32" alt="image" src="https://github.com/user-attachments/assets/ac16421a-2655-48d1-bb01-c981e52a6955" />

* **Loss Function:** Implemented `sparse_categorical_crossentropy` to measure the "distance" between the model's prediction and the actual label. 
  <img width="1173" height="38" alt="image" src="https://github.com/user-attachments/assets/ffbe15fd-6952-4c8e-8976-e6e0edcdec9b" />

* **Metrics:** Configured the model to track `accuracy` to evaluate the percentage of correctly classified images once training begins.
  <img width="1172" height="187" alt="image" src="https://github.com/user-attachments/assets/ee8910d5-2ae9-4608-a0b6-cf76038cd9e2" />

## Key Concepts Learned
* **Data Reshaping:** Understanding that the model requires a specific input shape (flattening 28x28 images into a 1D array).
* **Normalization:** Scaling pixel values from [0, 255] to [0, 1] to help the model converge faster.
* **Neural Configuration:** Learning the difference between defining a model (architecture) and compiling it (setting the training rules).

## Technical Environment
* **Platform:** Jupyter Notebook (Anaconda)
* **Infrastructure:** Hosted on a Proxmox Virtual Environment (VM)
* **Libraries:** TensorFlow, Keras, Matplotlib, NumPy
