# NN — Simple Neural Network Library

> Lightweight, educational, and extensible neural network building blocks in pure Python.

---

## Quick Overview

**NN** is a minimal, easy-to-read neural network library implemented with NumPy. It provides core components — layers, activations, losses, optimizers, and a simple `DNN` model — so you can quickly prototype and learn how deep learning models work under the hood.

Key features:

- Small, modular codebase for learning and experimentation
- Forward / backward passes implemented for all layers
- Basic optimizers and loss functions included
- Easy to extend with new layers, activations or optimizers

---

## Project Structure

```
NN/
│
├── main.py                # Entry point for running experiments or training models
├── requirements.txt       # Python dependencies
├── setup.py               # Setup script for packaging
├── LICENSE
├── README.md
│
├── activations/           # Activation functions
│   ├── __init__.py
│   ├── activations.py     # Implementations of activation functions (ReLU, Sigmoid, Tanh, Softmax)
│   └── base.py            # Base class/interface for activations
│
├── layer/                 # Neural network layers
│   ├── __init__.py
│   ├── base.py            # Base class/interface for layers
│   └── layers.py          # Implementations of layers (Dense, etc.)
│
├── loss/                  # Loss functions
│   ├── __init__.py
│   ├── base.py            # Base class/interface for loss functions
│   └── loss.py            # Implementations of loss functions (MSE, CrossEntropy, etc.)
│
├── model/                 # Model definitions
│   ├── __init__.py
│   └── dnn.py             # Deep Neural Network class (model architecture, forward/backward pass)
│
└── optimizer/             # Optimizers
    ├── __init__.py
    ├── base.py            # Base class/interface for optimizers
    └── optimizer.py       # Implementations of optimizers (SGD)
```

---

## Installation

Recommended: create and activate a virtual environment first.

```bash
python -m venv .venv
source .venv/bin/activate  # Linux / macOS
pip install -r requirements.txt
# or for development (editable install)
pip install -e .
```

---

## API Reference (short)

- `model.dnn.DNN` — main class: `add(layer)`, `compile(loss, optimizer)`, `train(x, y, epochs, batch_size)`, `predict(x)`, `summary()`, `plot_history(history)`
- `layer.layers.Dense(input_size, output_size, activation)` — fully connected layer
- `activations.activations` — `Sigmoid`, `Relu`, `Tanh`, `Softmax`
- `loss.loss` — `MeanSquaredError`, `CategoricalCrossEntropy`
- `optimizer.optimizer` — `GD(learning_rate)`

---

## Contributing

Contributions are welcome!

- Open an issue to discuss larger changes
- Fork the repo and make small, focused pull requests
- Follow existing code style and include tests when applicable

---

## License

This project is licensed under the terms in the `LICENSE` file.

---

## Questions / Contact

If you have questions or suggestions, open an issue or submit a PR. Contributions and feedback are appreciated!
