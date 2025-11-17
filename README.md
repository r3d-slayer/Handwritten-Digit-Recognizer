✍️ Handwritten Digit Recognizer (MNIST)

This repository contains a full end-to-end project for recognizing handwritten digits. It includes a user-friendly web-based drawing application (index.html) to capture custom digits and a Jupyter Notebook (Neural Network.ipynb) demonstrating the training and evaluation of a deep learning model using the classic MNIST dataset.

🚀 Features

Interactive Drawing Canvas: A simple HTML/CSS/JavaScript canvas where users can draw a digit (0-9) using their mouse or touch.

Data Preprocessing: The web app can convert the drawing into a 28x28 pixel array, mirroring the input format required by the MNIST-trained model.

Neural Network Training: A clear, step-by-step notebook for loading the MNIST dataset, normalizing the data, defining a simple dense neural network using TensorFlow/Keras, and training the model.

Evaluation: Includes code for evaluating model performance (accuracy and loss) and visualizing results using a Confusion Matrix.

Custom Prediction: Code is included to preprocess and predict on a custom drawn image (digit (3).png).

🛠️ Project Structure

The repository is structured as follows:

.
├── index.html                  # The interactive digit drawing canvas (HTML/CSS/JS)
├── Neural Network.ipynb        # Jupyter Notebook for model training (TensorFlow/Keras)
├── digit (3).png               # Sample image of a drawn digit (used in the notebook)
└── README.md                   # This file



💻 Getting Started

1. Web Application (index.html)

To test the digit capture tool:

Clone this repository:

git clone [Your Repository URL]



Open the index.html file in any modern web browser.

Draw a digit on the canvas and use the "Get 28×28 Pixel Data" button to see the normalized data array in the browser console (developer tools).

2. Model Training (Neural Network.ipynb)

To run the training and evaluation notebook, you will need Python and a few common data science libraries.

Prerequisites:

Ensure you have these libraries installed:

pip install tensorflow keras numpy pandas matplotlib seaborn pillow jupyter



Steps:

Start a Jupyter environment:

jupyter notebook



Open the Neural Network.ipynb file.

Run the cells sequentially to:

Load and preprocess the MNIST dataset.

Define and train the Sequential Neural Network model.

Evaluate the model's accuracy (you should see results in the ~97-98% range).

Test a custom image (the included digit (3).png, which the notebook successfully predicts as '3').

🧠 Model Architecture

The neural network used for classification is a simple, effective Dense model:

Layer

Type

Output Shape

Activation

Purpose

0

Flatten

(784,)

N/A

Flattens the 28x28 input image

1

Dense

(100)

Sigmoid

First hidden layer

2

Dense

(100)

Sigmoid

Second hidden layer

3

Dense

(10)

Softmax

Output layer for 10 classes (0-9)

Optimizer: adam

Loss Function: sparse_categorical_crossentropy (suitable for multi-class classification)

🖼️ Example Prediction

The notebook includes an example showing the prediction on the sample image:

Input Image

Predicted Digit



3

🤝 Contribution

Feel free to open issues or submit pull requests for bug fixes or improvements, such as converting the trained Keras model to TensorFlow.js to run the prediction directly in the web app!
