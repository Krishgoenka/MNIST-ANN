# 🖥️ MNIST Handwritten Digit Classification

![MNIST Sample](https://upload.wikimedia.org/wikipedia/commons/2/27/MnistExamples.png)

## 📌 Overview  
This project builds a **Neural Network** to classify **handwritten digits (0-9)** from the **MNIST dataset** using **TensorFlow/Keras**. The model learns to recognize digits with high accuracy by training on **60,000 images** and testing on **10,000 images**.

- **Dataset:** MNIST (Modified National Institute of Standards and Technology)  
- **Model Type:** Multi-layer Perceptron (MLP) / Artificial Neural Network (ANN)  
- **Accuracy:** ~98.09%  
- **Framework:** TensorFlow, Keras  

---

## 🛠️ Installation & Setup  
### 🔹 Prerequisites  
Make sure you have Python and the required libraries installed.  

```bash
pip install tensorflow numpy matplotlib

git clone https://github.com/your-username/mnist-digit-classifier.git
cd mnist-digit-classifier
🧠 Understanding the Model
1️⃣ Loss Function: Categorical Crossentropy
Used for multi-class classification to measure the difference between predicted and actual labels.

2️⃣ Optimizer: Adam
The Adam optimizer adjusts weights efficiently using gradients, combining Momentum & RMSprop methods.

3️⃣ Accuracy & Why It Dropped with More Layers
Adding too many layers led to overfitting (model memorized data but didn’t generalize well).
Vanishing gradients might have slowed training.
Hyperparameter tuning (learning rate, dropout, etc.) can improve results.
📸 Sample Predictions
Here are some correctly and incorrectly classified images:

import matplotlib.pyplot as plt
import numpy as np

predictions = model.predict(x_test)

plt.imshow(x_test[0], cmap='gray')
plt.title(f"Predicted: {np.argmax(predictions[0])}")
plt.show()
