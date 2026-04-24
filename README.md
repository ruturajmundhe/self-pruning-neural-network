# Self-Pruning Neural Network

## Overview
This project implements a neural network that dynamically prunes its own weights during training using learnable gating mechanisms and sparsity regularization.

Unlike traditional post-training pruning methods, this approach integrates pruning directly into the learning process, allowing the model to automatically identify and remove redundant connections.

---

## Key Result
The model achieves over **80% sparsity** with only a minimal drop in accuracy on the CIFAR-10 dataset.

---

## Results

| Lambda (λ) | Test Accuracy (%) | Sparsity (%) |
|-----------|------------------|--------------|
| 0.001     | 54.15            | 33.59        |
| 0.1       | 54.24            | 50.25        |
| 1.0       | 53.28            | 81.03        |

---

## Observations

- Increasing λ leads to higher sparsity, indicating effective pruning of less important weights.  
- The model maintains relatively stable accuracy even as sparsity increases, suggesting many parameters are redundant.  
- At λ = 1.0, the model achieves over 80% sparsity with only a minor drop in accuracy.  
- This demonstrates a clear trade-off between model compactness and performance.

---
