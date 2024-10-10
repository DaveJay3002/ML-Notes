An **activation function** is a mathematical function used in artificial [[Neural Network]] to determine the output of a [[Neuron]]. It introduces non-linearity into the model, allowing the network to learn complex patterns and relationships in the data. Common activation functions include Sigmoid, ReLU (Rectified Linear Unit), and Tanh. The choice of activation function can significantly impact the performance and convergence of the neural network.

# Why do we need Activation Functions
- **Non-Linearity**: They introduce non-linearity into the model, allowing the network to learn complex patterns and relationships in the data. Without activation functions, the network would only be able to learn linear mappings.
    
- **Output Range**: Different activation functions help in scaling the output to a specific range, which is particularly important for ensuring the outputs are interpretable (e.g., probabilities in classification tasks).
    
- **Gradient Propagation**: Activation functions like ReLU and Sigmoid facilitate effective gradient propagation during backpropagation, enabling efficient training of deep networks.
    
- **Representation Power**: By using various activation functions, neural networks can represent a wider variety of functions, improving their performance on complex tasks.
# Types of Activation Functions
- [[Sigmoid Function]]
- [[ReLU]]

# Choosing an activation function
For binary classification problems, Sigmoid is the most suitable
For Regression data, use Linear activation function if the data can take both positive and negative values
For regression data with no negative values, ReLU is the most suitable 
ReLU is the most common choice for neural networks