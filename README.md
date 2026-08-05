# MNIST Digit Recognition

A from-scratch walkthrough of building and training a neural network to recognise handwritten digits (0-9) using the [MNIST](http://yann.lecun.com/exdb/mnist/) dataset, in PyTorch.

## What's in here

`mnist_walkthrough.ipynb` covers:
1. Loading and visualising the MNIST dataset
2. A simple fully-connected neural network, trained from scratch (manual training loop, not a black-box `.fit()`)
3. Evaluation: test accuracy, a confusion matrix, and inspection of misclassified digits
4. A convolutional neural network (CNN), compared against the fully-connected baseline

## Results

| Model | Test accuracy (5 epochs) |
|---|---|
| Fully-connected network | 97.6% |
| CNN | 98.8% |

## Setup

Requires Python 3.12 (PyTorch's pre-built wheels reliably support 3.12; newer Python versions may not yet be supported).

```bash
python -m venv .venv
.venv\Scripts\activate        # on Windows
pip install -r requirements.txt
```

Register the environment as a Jupyter kernel:

```bash
python -m ipykernel install --user --name mnist_nn --display-name "Python 3 (mnist_nn)"
```

## Running

Launch Jupyter and open `mnist_walkthrough.ipynb`, selecting the `mnist_nn` kernel:

```bash
jupyter notebook
```

The MNIST dataset (~11MB) downloads automatically into a local `data/` folder the first time the notebook runs.
