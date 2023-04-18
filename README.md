# Nim
In the game of Nim, players take turns removing any non-negative number of objects from any one non-empty pile, until the last object is removed, and the player who removes the last object loses. In this project, we build an AI to learn the strategy for this game through reinforcement learning. By playing against itself repeatedly and learning from experience, eventually our AI will learn which actions to take and which actions to avoid.

## Requirements
You will need Python 3.10 to run this project. If you have an older version of Python, you will need to update it.

## Usage
To train the AI and start playing the game, run the following command:

`python play.py`

The AI will play against itself and learn from experience until it has completed 10,000 training games. After training, the AI will make its first move and prompt the human player to make a move.

## Example
Here is an example of what you might see when playing against the AI:


```
Playing training game 1
Playing training game 2
Playing training game 3
...
Playing training game 9999
Playing training game 10000
Done training

Piles:
Pile 0: 1
Pile 1: 3
Pile 2: 5
Pile 3: 7

AI's Turn
AI chose to take 1 from pile 2.

Piles:
Pile 0: 1
Pile 1: 3
Pile 2: 4
Pile 3: 7

Your Turn
Choose Pile:
...
```

## How it Works

In the game of Nim, players take turns removing objects from piles. The player who removes the last object loses. The AI learns to play the game using Q-learning, a technique for reinforcement learning.

The AI represents each state of the game as a list of integers, where each integer represents the number of objects in a pile. The AI chooses actions based on the Q-values, which represent the expected reward for each action in each state. The AI updates the Q-values after each action using the Q-learning formula:

`Q(s, a) <- Q(s, a) + alpha * (new value estimate - old value estimate)`

Where s is the current state, a is the chosen action, alpha is the learning rate, and new value estimate is the sum of the immediate reward and the estimated future reward. The AI uses an epsilon-greedy policy to balance exploration and exploitation.

## Project Structure
The project contains the following files:

- play.py: the main script that runs the game
- nim.py: contains the Nim and NimAI classes

## Credits
This program's relevant functions were written by me, and is based on a problem set for the course CS50AI from Harvard University. The course material and problem set were created by the staff at Harvard University, and are available at https://cs50.harvard.edu/ai/.
