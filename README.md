# Plot-4-Game-Using-Reinforcement-Learing

This repository contains the implementation of a Connect-X (Plot-4) game using reinforcement learning techniques. The project includes a custom game engine, visual rendering for the game board, and a framework for integrating Deep Q-Learning (DQN) to train an AI agent.

## Features

### 1. Connect-X Game Engine
- Implements the core game logic for a Connect-X (similar to Connect-4) board game.
- Supports two players with customizable board dimensions.
- Detects win, draw, and lose conditions.
- Includes a reset functionality to restart the game.

### 2. Visual Rendering
- Utilizes `matplotlib` for visually displaying the game board.
- Uses red and blue circles to represent player tokens on a grid.
- Real-time rendering of game progress.

### 3. Experience Replay
- Implements a `replayMemory` class to store game transitions (state, action, reward, next state).
- Allows random sampling of batches for training a DQN model.
- Helps decorrelate transitions to stabilize training.

---

## Prerequisites

To run this project, ensure you have the following installed:
- Python 3.7 or later
- Required Libraries:
  - `numpy`
  - `matplotlib`
  - `torch`

---

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/Plot-4-Game-Using-Reinforcement-Learning.git
   cd Plot-4-Game-Using-Reinforcement-Learning

Install the required dependencies:

bash
Copy code
pip install -r requirements.txt
Open the Jupyter Notebook to explore or modify the game and learning logic:

bash
Copy code
jupyter notebook PLOT_4_GAME.ipynb


Usage
1. Visualizing the Game Board
To initialize and render the game board:
python
Copy code
from connect_x import connect_x

env = connect_x()  # Initialize the game
env.reset()         # Reset the board
env.render()        # Visualize the empty board


2. Simulating Moves
You can simulate moves for players using the make_move function:
python
Copy code
env.make_move(3, 'p1')  # Player 1 moves in column 3
env.make_move(4, 'p2')  # Player 2 moves in column 4
env.render()            # Visualize the board after moves


3. Experience Replay for DQN
Use the replayMemory class for storing and sampling game transitions:
python
Copy code
memory = replayMemory()
memory.dump((state, action, reward, next_state))
batch = memory.sample(batch_size=32)

4. Visualizations
   ![image](https://github.com/user-attachments/assets/1e30e225-0768-4b53-8727-2f8e1a4a90b6)

Future Enhancements:
-Implement Deep Q-Learning to train an AI agent to play Connect-X.

-Add advanced reinforcement learning techniques such as:

-Experience Replay: Randomized sampling for better training.

-Self-Play: Train the agent using AlphaGo-inspired evaluation phases.

-Policy Optimization: Fine-tune the policy for higher rewards.

