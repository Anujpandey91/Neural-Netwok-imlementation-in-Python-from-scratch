<div align="center">

# mydl

### A Deep Learning Library Built from Scratch with NumPy

Build and understand neural networks by implementing their core mathematics from first principles.

[![Python](https://img.shields.io/badge/Python-3.11%2B-blue)](https://www.python.org/)
[![NumPy](https://img.shields.io/badge/NumPy-2.x-green)](https://numpy.org/)
[![Tests](https://img.shields.io/badge/Tests-89%20Passing-success)](#testing)

</div>

---

## Overview

**mydl** is an educational deep learning library implemented from scratch using **Python and NumPy**.

The project focuses on making the mathematics and internal mechanics of neural networks explicit rather than hiding them behind high-level deep learning frameworks.

Instead of treating neural networks as black boxes, `mydl` aims to connect the mathematical concepts behind deep learning with their actual implementation in code.

The library currently includes:

- Logistic Regression
- Two-Layer Neural Networks
- L-Layer Neural Networks
- Forward and backward propagation
- Mini-batch training
- Multiple optimization algorithms
- L1, L2, and combined L1/L2 regularization
- Dropout
- Training and validation history
- Binary classification metrics
- Training-history visualization

The project was developed alongside the **Deep Learning Specialization by Andrew Ng**, with an emphasis on translating mathematical concepts into working implementations.

---

## Features

### Models

- Logistic Regression
- Two-Layer Neural Network
- L-Layer Neural Network

### Neural Network Components

- ReLU activation
- Sigmoid activation
- Binary Cross-Entropy loss
- Linear layers
- He initialization
- Vectorized NumPy computation
- Dropout

### Optimizers

- Gradient Descent
- Momentum
- RMSProp
- Adam

### Regularization

- L1 Regularization
- L2 Regularization
- Combined L1 + L2 Regularization

### Training & Validation

- Mini-batch training
- Training loss history
- Training accuracy history
- Validation loss
- Validation accuracy
- Configurable classification threshold

### Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1 Score
- Binary confusion matrix

### Visualization

- Training loss vs. epoch
- Validation loss vs. epoch
- Training accuracy vs. epoch
- Validation accuracy vs. epoch

---

## Quick Start

The main deep learning model is `LLayerNN`.

```python
from mydl import LLayerNN, Adam

model = LLayerNN(
    hidden_layer=[32, 16, 8],
    optimizer=Adam(learning_rate=0.001),
    epochs=1000,
)

model.fit(X_train, Y_train)

predictions = model.predict(X_test)

score = model.score(X_test, Y_test)

print(f"Accuracy: {score:.4f}")
