# Tic_Tac_Toe_RL

# 🧠 Reinforcement Learning Based Tic-Tac-Toe Player

This project implements an **RL-based Tic-Tac-Toe agent** using the **Q-Learning algorithm**.
It was developed as part of a **Pattern Recognition & Computational Vision (PBL) project**, focusing on how an AI agent can learn optimal strategies through interaction and reward feedback — *without prior knowledge of the game rules*.



## 🎯 Overview

The goal of this project is to develop an intelligent Tic-Tac-Toe player that can **learn from experience**.
Using **Q-Learning**, the agent repeatedly plays games against itself or a random opponent, gradually improving its gameplay by updating a Q-table — a memory of the best moves for each board configuration.

Over time, the model learns to **win or force draws** consistently, demonstrating the effectiveness of reinforcement learning in simple game environments.


## ⚙️ Features

* 🧩 **TicTacToeEnvironment** – Implements the 3×3 game logic, move validation, and winner checking.
* 🤖 **QLearningAgent** – Uses Q-Learning with ε-greedy policy for balancing exploration and exploitation.
* 🎮 **Training Module** – Agent trains over multiple episodes and stores learned Q-values.
* 📈 **Evaluation & Visualization** – Plots of rewards, win rates, and performance progression.
* 👤 **Interactive Mode** – Option to play against the trained agent in the notebook.


## 🧩 Project Structure

| File                      | Description                                                                    |
| ------------------------- | ------------------------------------------------------------------------------ |
| `Tic_Tac_Toe.ipynb`       | Jupyter Notebook containing the full implementation, training, and evaluation. |
| `tictactoe_flowchart.png` | Flowchart showing the architecture and control flow of the RL process.         |
| `README.md`               | Project documentation (this file).                                             |


## 🧠 Algorithm Used – Q-Learning

Q-Learning is a **model-free reinforcement learning** algorithm that learns the value of taking a specific action in a given state.
The update rule is defined as:

[
Q(s, a) = Q(s, a) + \alpha [r + \gamma \max_{a'} Q(s', a') - Q(s, a)]
]

Where:

* ( s ): current state
* ( a ): action taken
* ( r ): reward received
* ( \alpha ): learning rate
* ( \gamma ): discount factor
* ( s' ): next state

Through repeated gameplay, the agent learns an optimal **policy** — mapping states to actions that maximize long-term rewards.


## 🚀 How to Run

1. Clone this repository

   ```bash
   git clone https://github.com/<your-username>/TicTacToe-RL.git
   cd TicTacToe-RL
   ```

2. Open the notebook

   ```bash
   jupyter notebook Tic_Tac_Toe.ipynb
   ```

3. Run the training cells to allow the agent to learn from simulated games.

4. Optionally, run the **play** cell to challenge the trained agent.


## 📊 Results

* The agent starts with random moves but gradually learns optimal strategies.
* After sufficient training episodes, it rarely loses and often forces draws.
* The Q-values converge, indicating stable learning.
* Graphs show a steady improvement in cumulative reward and win rate.



