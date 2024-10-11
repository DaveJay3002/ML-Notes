**Deep Reinforcement Learning (DRL)** combines the principles of Reinforcement Learning (RL) with deep learning techniques to address complex decision-making tasks where traditional RL methods may struggle. By leveraging deep neural networks, DRL can process high-dimensional sensory inputs, such as images or video, to make informed decisions in environments with large state spaces.
[[Exploration vs Exploitation]] [[Mini-batch]]
![[Pasted image 20241011163726.png]]
### Key Concepts of Deep Reinforcement Learning

1. **Reinforcement Learning Basics**:
    
    - In RL, an agent learns to make decisions by interacting with an environment. The agent receives feedback in the form of rewards based on its actions and aims to maximize the cumulative reward over time.
    - The learning process involves exploring the environment, exploiting known information, and updating its strategy (policy) based on experiences.
2. **Deep Learning**:
    
    - Deep learning utilizes neural networks with multiple layers (deep networks) to learn complex patterns from large datasets. These networks can approximate complex functions and representations, making them well-suited for tasks such as image recognition and natural language processing.

### How Deep Reinforcement Learning Works

1. **Function Approximation**:
    
    - In traditional RL, value functions or policies are often represented using tables, which become impractical in environments with large state spaces. DRL employs deep neural networks as function approximators to estimate these values and policies.
    - The neural networks can learn to map states to actions (policy) or states to expected rewards (value function) based on the training data generated from the agent's experiences.
2. **Experience Replay**:
    
    - DRL often uses a technique called experience replay, where the agent stores its experiences (state, action, reward, next state) in a memory buffer. During training, the agent samples from this buffer to learn, allowing it to break correlations between consecutive experiences and improve learning stability.
3. **Exploration Strategies**:
    
    - To learn effectively, the agent must explore the environment to discover new states and actions. Various strategies, such as ε-greedy (where the agent chooses random actions with a certain probability), are used to balance exploration and exploitation.
4. **Training with Temporal Difference Learning**:
    
    - DRL frequently employs methods like Q-learning or policy gradients, where the neural network is updated based on the difference between the predicted and actual rewards. This approach helps the agent refine its policy over time.
5. **End-to-End Learning**:
    
    - One of the significant advantages of DRL is that it allows for end-to-end learning. The agent can directly learn from raw sensory input (like pixel values from images) to output actions, making it applicable to tasks like playing video games or robotic control.

![[Pasted image 20241011164046.png]]

# More efficient implementation of DRL
![[Pasted image 20241011164207.png]]

Instead of giving a single action with some magnitude, here each action produces some magnitude so that we get more control over the assumed lander.

