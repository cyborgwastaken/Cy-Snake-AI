# Cy-Snake-AI
A Machine Learnig Project 


# Snake Game AI

This project implements an AI agent that plays the classic Snake game using a machine learning model. The game is implemented in Python using the Pygame library.

## Files

### `game.py`

This file contains the main game logic and the `SnakeGameAI` class. Key functionalities include:

- **Initialization**: Sets up the game environment, including display settings and game clock.
- **Game State Management**: Tracks the state of the game, including the snake's position, direction, score, and food location.
- **Game Logic**: Handles player input, updates the game state based on player actions, checks for collisions, and manages the placement of food.
- **User Interface**: Renders the game graphics, including the snake, food, and score display.

The `SnakeGameAI` class provides methods for resetting the game, playing a single step of the game, and checking for collisions.

### `agent.py`

This module contains the implementation of the AI agent that plays the Snake game. The agent utilizes a machine learning model to make decisions and learn from its experiences.

Key functionalities of the `Agent` class include:

- **Initialization**: Sets up parameters such as exploration rate (`epsilon`), discount rate (`gamma`), memory buffer, and the neural network model.
- **State Representation**: Converts the game state into a format suitable for input to the neural network.
- **Memory Management**: Stores experiences (state, action, reward, next state, done) in a replay memory buffer.
- **Training**: Implements methods for both short-term and long-term memory training. Short-term memory training updates the neural network with individual experiences, while long-term memory training performs batch training using experiences stored in memory.
- **Action Selection**: Determines the agent's action based on the current state, using an exploration-exploitation strategy.

The `train()` function initializes the game environment and agent, and then iteratively plays and trains the agent on the Snake game. It also includes functionality for plotting scores and saving the model weights.

### `model.py`

This module contains the definition of the neural network model used by the Snake Game AI agent, as well as the training logic.

Key functionalities of the `Linear_QNet` and `QTrainer` classes include:

- **Linear_QNet**: Defines a simple feedforward neural network model with one input layer, one hidden layer, and one output layer. Provides methods for model initialization and saving.
- **QTrainer**: Responsible for training the neural network model. Defines the training step, which includes computing the loss between predicted and target Q-values, performing backpropagation, and updating the model parameters using the Adam optimizer.

### `helper.py`

This module contains helper functions for visualization during training of the Snake Game AI agent.

- **plot(scores, mean_scores)**: Plots the scores achieved by the agent during training, as well as the mean scores over time. Uses Matplotlib for plotting and IPython for displaying the plots dynamically.

## Usage

To use the Snake Game AI, follow these steps:

1. Ensure you have Python 3.x installed on your system.
2. Install the required dependencies (`pygame`, `torch`, `matplotlib`, `ipython`) using pip.
3. Run the the `agent.py` file to train the AI agent on the Snake game.
4. Monitor the training progress using the live plot displayed during training.

## Dependencies

- Python 3.11
- Pygame
- Torch
- Matplotlib
- IPython

---

**Step 1: Install PyGame**

```bash
pip install pygame
```

**Step 2: Install PyTorch**

```bash
pip3 install torch torchvision
```

**Step 3: Install MatPlotLib**

```bash
pip install matplotlib
```

**Step 4: Install IPython**

```bash
pip install ipython
```

## Credits

This project was created by Ayushman Das - Cyborg.
