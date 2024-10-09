**TensorFlow** is an open-source machine learning framework developed by Google, designed to build, train, and deploy machine learning models, including neural networks. It is highly flexible and scalable, making it suitable for both simple tasks and complex deep learning applications.

## Sample Code

```
import tensorflow as tf
from tensorflow.keras import layers, models
from tensorflow.keras.datasets import mnist
import numpy as np

# 1. Load the MNIST dataset
(X_train, y_train), (X_test, y_test) = mnist.load_data()

# 2. Normalize the dataset (scaling pixel values from 0-255 to 0-1)
X_train = X_train.astype(np.float32) / 255.0
X_test = X_test.astype(np.float32) / 255.0

# 3. Reshape the data (since MNIST images are 28x28, we flatten them into vectors of size 28*28)
X_train = X_train.reshape(-1, 28 * 28)
X_test = X_test.reshape(-1, 28 * 28)

# 4. Build a simple neural network
model = models.Sequential([
    layers.InputLayer(input_shape=(28 * 28,)), # Input layer for 28x28 images
    layers.Dense(128, activation='relu'),      # Hidden layer with 128 neurons
    layers.Dense(10, activation='softmax')     # Output layer (10 classes for digits 0-9)
])

# 5. Compile the model (using categorical crossentropy for multi-class classification)
model.compile(optimizer='adam',
              loss='sparse_categorical_crossentropy',
              metrics=['accuracy'])

# 6. Train the model
model.fit(X_train, y_train, epochs=5, batch_size=32, validation_split=0.2)

# 7. Evaluate the model on test data
test_loss, test_acc = model.evaluate(X_test, y_test)

print(f"Test accuracy: {test_acc}")

```