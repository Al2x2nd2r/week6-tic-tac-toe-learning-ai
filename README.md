# Tic-Tac-Toe Q-Learning AI
## Project Overview
This project demonstrates reinforcement learning by training an AI to play Tic-Tac-Toe through trial and error, without being explicitly programmed with strategies.

## How to Run
1. **Train the AI**
```bash
python train_agent.py
```
Choose training intensity (1000-10000 games)

2. **Play Against AI**
```bash
python play_game.py
```

## How Q-Learning Works
### The Q-Table
The AI maintains a table of Q-values for each state-action pair:
- **State**: Current board configuration
- **Action**: Where to place the mark
- **Q-Value**: How good that action is in that state

### Learning Process
1. **Exploration**: Try random moves to discover strategies
2. **Exploitation**: Use learned knowledge to make good moves
3. **Reward**: Win = +10, Lose = -10, Tie = +5
4. **Update**: Adjust Q-values based on outcomes

### My Training Results
- Games trained: The AI was trained with 10,000 Games
- Final win rate: 90%
- States learned: The AI learned thousands of unique Tic-Tac-Toe board configurations, each represented as a state in the Q-Table

## What I Observed
During training, the AI started out making completely random moves, but after a few thousand games it was able to avoid losing positions. It eventually started to setup its own winning paths and stopped falling for simple traps. This show that it has indeed learned patterns from repeated experience.

## Reinforcement Learning in Real Life
1. **Game AI**: Games use reinforcement learning to teach AI's to make smart decisions, like predicting player behavior or movement.
2. **Robotics**: Robots can use reinforcement learning to learn how to walk, balance, and other taks through trial and error.
3. **Recommendation Systems**: Many platforms learn which reccomendations keep users engaged and adjust suggestions based on that information.

## Challenges and Solutions
At first I didnt understand what the "states" and "Q-values" actually meant, so it was hard to understand how or what the AI was learning. But I quickly realized that a state is just the layout of the board and that a Q-value is basically the AI's rating of how good a move is. Another problem I had was that the AI didnt feel like it wasnt getting smarter, lowering the exploration rate later in training seemed to help with this issue and allowed it to use the knowledge it had accumulated.

## What I Learned

I learned how reinforcement learning teaches an AI through rewards rather than explicit instructions. Next, I learned how the Q-table works, storing knowledge about which possible moves are better or worse in different states. Lastly, I learned how exploration and exploitation balance each other out during training. Overall, this project taught me that even simple rules can lead to smart behavior after enough practice.
