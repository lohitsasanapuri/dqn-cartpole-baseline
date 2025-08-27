# DQN CartPole Baseline

A simple implementation of a Deep Q-Network (DQN) to solve the classic CartPole-v1 balancing problem using OpenAI Gym. This project serves as a baseline for understanding reinforcement learning (RL) concepts and the DQN algorithm.

🚀 Overview
- Implements a DQN agent to balance a pole on a moving cart.
- Uses experience replay and a target network for stable training.
- Trains with an epsilon-greedy exploration strategy and decaying epsilon.
- Provides plots for rewards and loss trends during training and evaluation.
- Saves the trained model (cartpole_dqn_model.h5) for reuse.

⚙️ Environment
- Environment: CartPole-v1
- Observation Space: 4 values (cart position, cart velocity, pole angle, pole angular velocity).
- Action Space: 2 discrete actions {0 = push left, 1 = push right}.
- Reward: +1 per time step pole remains balanced.
- Episode ends if:
  • Pole angle > ±12°
  • Cart position > ±2.4
  • Episode length > 500 steps

📚 Key Concepts
- Bellman Equation for Q-learning updates
- Experience Replay: Stores transitions for batch updates
- Target Network: Stabilizes Q-value estimation
- Epsilon Decay: Shifts from exploration → exploitation

🔧 Implementation
- Frameworks: TensorFlow / Keras, NumPy, Pandas, Matplotlib
- Neural Network:
  • Input: 4 state features
  • Hidden layers: 2 × Dense(128, ReLU)
  • Output: Q-values for each action

📊 Results
- Trained over 700 episodes with batch size 32.
- Average reward increased steadily after ~400 episodes.
- Loss decreased over time with some fluctuations.
- Test runs achieved stable rewards >100 per episode.

📂 Files
- Final DQN.ipynb → Main training notebook

▶️ Run
```bash
# Install dependencies
pip install gym tensorflow numpy pandas matplotlib

# Run training
python Final_DQN.ipynb
```
📌 References
- Barto, Sutton, Anderson (1983) Neuronlike Adaptive Elements That Can Solve Difficult Learning Control Problems
- Gym Docs: https://www.gymlibrary.dev/environments/classic_control/cart_pole/
