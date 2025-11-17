# Handwritten Digit Recognizer

This repository contains a complete end-to-end handwritten digit recognition project.

It includes:

- A web-based digit drawing tool (`index.html`)
- A Jupyter Notebook (`Neural Network.ipynb`) for training and evaluating a deep learning model using the MNIST dataset

---

##  Features

### Interactive Drawing Tool
A simple HTML and JavaScript interface for drawing digits (0–9).

### Data Preprocessing
The web app converts drawings into a 28×28 grayscale format suitable for MNIST models.

### Neural Network Training
The notebook includes:
- Loading the MNIST dataset  
- Normalizing the data  
- Building a TensorFlow/Keras neural network  
- Training and validating the model  

### Evaluation
Includes:
- Accuracy and loss metrics  
- Confusion Matrix  
- Predictions on sample digits  

### Custom Prediction
Predicts a custom handwritten digit (`digit (3).png`).

---

Open `index.html` in any browser.

Draw a digit and click **Get 28×28 Pixel Data** to see the normalized data in the browser console.

---

### 2. Training the Model

Required Python packages:  
tensorflow  
keras  
numpy  
pandas  
matplotlib  
seaborn  
pillow  
jupyter  

Run Jupyter Notebook.

Open **Neural Network.ipynb** and run all cells to:

- Load and preprocess MNIST  
- Build and train the model  
- Evaluate accuracy (around 97–98%)  
- Test a custom image (`digit (3).png`)  

---

## 🧠 Model Architecture

| Layer | Type    | Output | Activation | Description                      |
|-------|---------|--------|------------|----------------------------------|
| 0     | Flatten | 784    | —          | Converts 28×28 image to vector   |
| 1     | Dense   | 100    | Sigmoid    | Hidden layer                     |
| 2     | Dense   | 100    | Sigmoid    | Hidden layer                     |
| 3     | Dense   | 10     | Softmax    | Output layer                     |

Optimizer: **adam**  
Loss: **sparse_categorical_crossentropy**  
Accuracy: **~97–98%**

---

