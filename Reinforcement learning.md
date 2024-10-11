**Reinforcement Learning (RL)** is a type of machine learning where an agent learns to make decisions by interacting with an environment. The agent takes actions to achieve specific goals, receiving feedback in the form of rewards or penalties. The primary objective of the agent is to learn a policy that maximizes the cumulative reward over time. Unlike supervised learning, where the model learns from labeled input-output pairs, RL focuses on learning from the consequences of actions taken in an environment.
[[Return in RL]] [[Markov's Decision Process]] [[Bellman Equation]]   [[Deep Reinforcement Learning]]
[[Exploration vs Exploitation]]
![[Pasted image 20241011153623.png]]
### Key Concepts in Reinforcement Learning

1. **Agent**: The learner or decision maker that interacts with the environment to perform actions.
2. **Environment**: The external system or context with which the agent interacts. The environment provides feedback in response to the agent's actions.
3. **State**: A representation of the current situation of the agent within the environment. It contains all the necessary information for the agent to make a decision.
4. **Action**: The set of all possible moves the agent can make in a given state. The agent selects actions based on its current policy.
5. **Reward**: A scalar feedback signal received after taking an action in a particular state. Rewards can be positive (encouragement) or negative (punishment) and are used to evaluate the desirability of the actions taken.
6. [[Policy in RL]]: A strategy or mapping from states to actions that defines the agent's behavior. It can be deterministic (a specific action for each state) or stochastic (a probability distribution over actions).
7. [[Value Function]]: A function that estimates the expected return (cumulative reward) from a given state or state-action pair. The value function helps the agent evaluate how good it is to be in a particular state.
    - **State Value Function V(s)V(s)V(s)**: The expected return starting from state sss and following the policy thereafter.
    - **Action Value Function Q(s,a)Q(s, a)Q(s,a)**: The expected return starting from state sss, taking action aaa, and following the policy thereafter.
8. **Episode**: A sequence of states, actions, and rewards that ends when a terminal state is reached. An episode represents one complete interaction cycle between the agent and the environment.

# RL in autonomous helicopter
![[Pasted image 20241011163437.png]]
![[Pasted image 20241011163639.png]]

