# flappy-dqn

A Deep Q-Network (DQN) reinforcement learning agent that learns to play Flappy Bird from scratch.

## What It Does

The agent observes the game state — bird position, velocity, and pipe locations — and learns to flap or do nothing through pure trial and error. No hardcoded rules. No human demonstrations. Just reward signals and a neural network that gets better over time.

## How It Works

DQN combines Q-learning with a deep neural network to approximate the optimal action-value function. The agent:

- Observes the current game state
- Selects an action (flap or wait) using an epsilon-greedy policy
- Receives a reward based on survival and pipe clearance
- Stores the experience in a replay buffer
- Trains the network by sampling random batches from that buffer

The replay buffer breaks the correlation between consecutive experiences, stabilizing training. A separate target network is updated periodically to prevent the Q-value estimates from chasing a moving target.

## Stack

- Python
- PyTorch
- `flappy-bird-gymnasium`
- Stable Baselines3

## Project Structure

```
flappy-dqn/
├── train.py          # Training loop
├── agent.py          # DQN agent and replay buffer
├── model.py          # Neural network architecture
└── README.md
```

## Getting Started

```bash
pip install flappy-bird-gymnasium stable-baselines3 torch
python train.py
```

## Results

Training in progress. Results and reward curves coming soon.

## Related Projects

Built this after [pokegym](https://github.com/Hrishirt/pokegym) — a hierarchical RL + LLM agent that plays Pokémon FireRed.
