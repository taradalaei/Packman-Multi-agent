# Pacman Multi-Agent Search

## Overview

This project implements various AI agents to play the classic Pacman game. The agents use different search algorithms, including Reflex Agent, Minimax, Alpha-Beta Pruning, and Expectimax. Additionally, custom evaluation functions are designed to improve the performance of these agents.

The project is based on the Pacman AI projects developed at UC Berkeley. The core projects and autograders were primarily created by John DeNero and Dan Klein. Student side autograding was added by Brad Miller, Nick Hay, and Pieter Abbeel.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Agents](#agents)
  - [Reflex Agent](#reflex-agent)
  - [Minimax Agent](#minimax-agent)
  - [Alpha-Beta Agent](#alpha-beta-agent)
  - [Expectimax Agent](#expectimax-agent)
- [Evaluation Functions](#evaluation-functions)
- [Attribution](#attribution)
- [Licensing](#licensing)

## Installation

To run this project, you need to have Python installed. Follow these steps to get started:

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/pacman-multiagent.git
   cd pacman-multiagent
   ```

2. Ensure you have the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

To run the Pacman game with different agents, use the following commands:

- Run the Reflex Agent:
  ```bash
  python pacman.py -p ReflexAgent
  ```

- Run the Minimax Agent:
  ```bash
  python pacman.py -p MinimaxAgent -a depth=2
  ```

- Run the Alpha-Beta Agent:
  ```bash
  python pacman.py -p AlphaBetaAgent -a depth=2
  ```

- Run the Expectimax Agent:
  ```bash
  python pacman.py -p ExpectimaxAgent -a depth=2
  ```

## Agents

### Reflex Agent

The `ReflexAgent` chooses an action at each choice point by examining its alternatives via a state evaluation function.

### Minimax Agent

The `MinimaxAgent` uses the minimax algorithm to choose the best move by assuming that the ghosts are trying to minimize Pacman's score.

### Alpha-Beta Agent

The `AlphaBetaAgent` is an optimized version of the Minimax Agent that uses alpha-beta pruning to reduce the number of nodes evaluated in the search tree.

### Expectimax Agent

The `ExpectimaxAgent` models the ghosts as choosing their moves uniformly at random, rather than adversarially.

## Evaluation Functions

### Reflex Agent Evaluation Function

This function evaluates the desirability of a state based on several factors, including the distance to the nearest food and the distance to the ghosts.

### Minimax, Alpha-Beta, and Expectimax Evaluation Function

These functions evaluate states by considering the score of the game, distances to the food, and distances to the ghosts.

### Custom Evaluation Function

The `betterEvaluationFunction` provides an advanced evaluation strategy that considers ghost states (scared or not) and their distances, food distances, power pellet availability, and the current game score.

## Attribution

The Pacman AI projects were developed at UC Berkeley. The core projects and autograders were primarily created by John DeNero and Dan Klein. Student side autograding was added by Brad Miller, Nick Hay, and Pieter Abbeel.

## Licensing

You are free to use or extend these projects for educational purposes provided that:
1. You do not distribute or publish solutions.
2. You retain this notice.
3. You provide clear attribution to UC Berkeley, including a link to [UC Berkeley AI](http://ai.berkeley.edu).
