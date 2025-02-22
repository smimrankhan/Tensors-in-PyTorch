# PyTorch Tensors

This repository contains a Python script demonstrating the use of **tensors in PyTorch**. Tensors are the fundamental building blocks in PyTorch and are similar to NumPy arrays, but with additional capabilities for GPU acceleration.

## Features

- Creation of tensors using different methods
- Tensor operations (arithmetic, reshaping, slicing, etc.)
- Moving tensors between CPU and GPU
- Automatic differentiation using PyTorch's `autograd`

## Prerequisites

Ensure you have the following installed:

- Python (>=3.7)
- PyTorch (>=1.9)
- NumPy (optional, but useful for conversions)

You can install PyTorch using:

```sh
pip install torch
```

## Usage

Run the script using:

```sh
python tensors.py
```

## Code Overview

### 1. Importing Required Libraries

```python
import torch
```

### 2. Creating Tensors

```python
x = torch.tensor([1, 2, 3])
```

### 3. Performing Tensor Operations

```python
x = torch.ones(3, 3)
y = torch.zeros(3, 3)
z = x + y  # Element-wise addition
```

### 4. Moving Tensors to GPU (if available)

```python
device = torch.device("cuda" if torch.cuda.is_available() else "cpu")
x = x.to(device)
```

### 5. Using Autograd for Differentiation

```python
x = torch.tensor(2.0, requires_grad=True)
y = x ** 2

y.backward()
print(x.grad)  # Outputs: tensor(4.)
```



Author

S. M. Imran Khan
