# 🚀 Deep Q-Learning for Lunar Landing

This project implements a **Deep Q-Learning (DQN)** agent to successfully land a spacecraft in the **LunarLander-v2** environment from OpenAI Gym.  
The agent learns to control the lander’s thrusters to achieve a soft landing between the flags with minimal fuel consumption.  

https://github.com/yourusername/Deep-Q-Learning-Lunar-Lander/assets/your_video_link_here

---

## 🧠 Project Overview

The goal of this project is to train an intelligent agent using **Reinforcement Learning (RL)**, specifically the **Deep Q-Learning** algorithm.  
The Lunar Lander environment provides continuous state observations (position, velocity, angle, etc.) and discrete action outputs for the thrusters.

The agent learns by interacting with the environment and maximizing cumulative rewards through experience replay and target network updates.

---

## 🎯 Environment Details

- **Environment:** `LunarLander-v2` (OpenAI Gym)
- **State Space:** 8 continuous values
  - X, Y position
  - X, Y velocity
  - Angle, angular velocity
  - Left and right leg contact flags
- **Action Space:** 4 discrete actions
  - `0` – Do nothing  
  - `1` – Fire left engine  
  - `2` – Fire main engine  
  - `3` – Fire right engine

---

## 🧩 Algorithm: Deep Q-Learning (DQN)

### Key Techniques:
- **Experience Replay:** Random sampling of past experiences to break correlation between consecutive updates.
- **Target Network:** A delayed copy of the Q-network to stabilize learning.
- **Epsilon-Greedy Policy:** Exploration-exploitation tradeoff for action selection.
- **Reward Optimization:** Encourages smooth, safe landings with minimal fuel usage.

---

## ⚙️ Implementation Steps

1. **Initialize environment** and neural network (Q-Network).
2. **Collect experiences**: `(state, action, reward, next_state, done)`.
3. **Store experiences** in a replay buffer.
4. **Sample mini-batches** from the buffer and compute target Q-values.
5. **Train Q-Network** using mean squared error between predicted and target Q-values.
6. **Update target network** at fixed intervals.
7. **Adjust epsilon** over time for balanced exploration.

---

## 📈 Results

The trained agent successfully lands the spacecraft consistently after sufficient training episodes.

### 🎥 Demo Video  
Check out the final performance in the demo video below:

> [Watch the result video](./lunar_lander_result.mp4)

---

## 🧾 Files Included

| File | Description |
|------|--------------|
| `Deep_Q_Learning_for_Lunar_Landing_Complete_Code.ipynb` | Main Jupyter notebook with full implementation |
| `lunar_lander_result.mp4` | Recorded video showing the trained agent landing |
| `README.md` | Project overview and documentation |

---

## 🧰 Requirements

Install the required dependencies using pip:

```bash
pip install gym==0.26.2
pip install pygame
pip install torch
pip install numpy
matplotlib
