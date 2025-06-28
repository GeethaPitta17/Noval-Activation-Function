
## 📌 Introduction

The primary objective of this novel activation function is to provide an alternative to popular activation functions like ReLU, sigmoid, and tanh. We focused on reducing issues like dying neurons, vanishing gradients, and exploding gradients while ensuring good computational efficiency and non-linearity.

## ❓ Problem Statement

We aimed to develop an activation function that satisfies the following requirements:

- **Non-linearity**: Effectively introduces non-linearity to enable the network to capture complex patterns.  
- **Gradient Issues**: Addresses the challenges of vanishing or exploding gradients during backpropagation.  
- **Smoothness**: Guarantees smoothness and differentiability throughout its domain to support gradient-based optimization.  
- **Bounded Output**: Optionally restricts the output within a specific range to avoid excessively large activations.  
- **Efficiency**: Ensures computational simplicity for practical implementation.  

## ⚙️ Methodology

We proposed two custom activation functions and evaluated them based on their properties. One of them, which we refer to as **Function2 (RTHIN)**, was found to perform best.  

- Unlike ReLU, it avoids the issue of dying neurons by ensuring a gradient exists for all inputs, including negative values.  
- Compared to tanh, it does not compress large positive inputs, allowing better information flow.  
- Its smooth transitions make it easier for optimization algorithms to learn effectively.  
- It ensures computational efficiency and stability, making it a better choice for addressing gradient-related problems while retaining flexibility for complex patterns.

## ✅ Advantages of Proposed Function (RTHIN)

1. **No Exploding Gradients**: The bounded negative region (tanh + atan) avoids the risk of large negative gradients during training.  
2. **Smooth Negative Handling**: The combination of tanh and atan ensures smoother gradient flow for negative inputs compared to ReLU's zero or ELU's exponential behavior.  
3. **Linear Behavior in Positive Region**: Like ReLU, it retains linear behavior for positive values but adds more flexibility in the negative region.  
4. **Better Convergence for Complex Models**: Adding non-linear yet bounded terms in the negative region helps the model explore a richer set of representations while maintaining stability.
