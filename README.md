# 🧠 CNN Model Architecture
- This project uses a Sequential Convolutional Neural Network (CNN) with regularization, batch normalization, and dropout to improve generalization and prevent overfitting.

### 🔍 Layer-by-Layer Breakdown
- Conv2D Layer
- Filters: 32
- Kernel Size: (3, 3)
- Padding: same (output size preserved)
- Regularization: L2 (λ = 0.001) — discourages overly complex weights
- Purpose: Detects low-level features such as edges and simple patterns

### Batch Normalization
- Normalizes activations to speed up training and stabilize learning
### ReLU Activation
- Introduces non-linearity so the network can learn complex patterns
### Dropout (0.3)
- Randomly disables 30% of neurons to prevent overfitting
### MaxPooling2D
- Downsamples feature maps by taking the max value from each patch
- Reduces spatial dimensions and computational cost
### Second Conv2D Layer
- Filters: 64
- Kernel Size: (3, 3)
- Padding: same
- Regularization: L2 (λ = 0.001)
- Purpose: Learns more detailed, abstract features
#### Batch Normalization
#### ReLU Activation
#### Dropout (0.3)
#### MaxPooling2D

### Flatten Layer
- Converts 2D feature maps into a 1D vector for dense layers
### Dense Layer
- Units: 128
- Activation: ReLU
- Learns high-level feature relationships
### Dropout (0.5)
- Further regularization by disabling half the neurons during training
### Output Layer
- Units: 2 (binary classification)
- Activation: Softmax — outputs class probabilities

### ⚡ Summary
- Strengths: L2 regularization + Dropout + Batch Normalization make the model robust against overfitting
- Use case: Perfect for binary classification of RGB images
- Input shape: Must match the preprocessing pipeline (e.g., (height, width, 3))
Input shape: Must match the preprocessing pipeline (e.g., (height, width, 3))

