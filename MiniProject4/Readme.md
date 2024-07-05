# Wumpus World Reinforcement Learning
This repository contains the implementation of Q-learning and Deep Q-learning (DQN) algorithms to solve the Wumpus World problem. The objective is to create an agent that can navigate a 4x4 grid, avoid hazards, collect gold, and possibly eliminate the Wumpus.

## Overview
The Wumpus World is a grid-based environment where the agent must learn to navigate efficiently, avoid potholes and the Wumpus, collect gold, and potentially eliminate the Wumpus. The grid is a 4x4 grid with different cells that can be empty, contain a pit, Wumpus, or gold.

## Algorithms
### Q-learning
Q-learning is a model-free reinforcement learning algorithm that aims to find the optimal policy by learning the Q-values for state-action pairs. The Q-values are updated iteratively based on the rewards received from the environment.

### DQN
Deep Q-learning (DQN) is an advanced version of Q-learning that uses a neural network to approximate the Q-values. This approach enables handling larger state spaces and complex environments more effectively.

### Comparison of Results
The average reward per episode for both agents after 1000 episodes shows the performance comparison:

Q-learning: -1024.639
DQN: 42.087
DQN outperforms Q-learning significantly, demonstrating better learning and adaptation to the environment.

### Epsilon Decay Impact
Epsilon decay controls the exploration-exploitation trade-off:

High epsilon: The agent explores more, leading to initial negative rewards as it discovers the environment.
Low epsilon: The agent exploits learned policies, resulting in higher rewards over time.
### Consistency in Q-learning
The Q-learning agent struggled to achieve consistent performance, failing to find gold without dying in the given episodes.

### Optimal Policy Learning Speed
DQN learned the optimal policy faster, achieving consistent performance in 29 episodes, whereas Q-learning did not achieve consistency within 1000 episodes.

## Neural Network Architecture
### Architecture
* Input Layer: 16 neurons (4x4 grid state)
* Hidden Layers:
* First Hidden Layer: 24 neurons, ReLU activation
* Second Hidden Layer: 24 neurons, ReLU activation
* Output Layer: 4 neurons (actions), linear activation
### Rationale
* Simplicity and Efficiency: Two hidden layers with 24 neurons each strike a balance between complexity and performance.
* ReLU Activation: Ensures faster training and avoids vanishing gradient problems.
* Linear Output Layer: Produces continuous Q-values for action selection.
## Conclusion
The DQN algorithm, leveraging neural networks, demonstrated superior performance compared to Q-learning in the Wumpus World problem. The architecture chosen for DQN enabled efficient learning and adaptation, leading to faster achievement of optimal policies.

Feel free to explore the code, tweak the parameters, and experiment with different architectures to further enhance the agent's performance. Contributions and suggestions are welcome!
