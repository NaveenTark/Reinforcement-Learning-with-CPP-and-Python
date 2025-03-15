This repository implements a Gridworld Markov Decision Process (MDP) environment in Python using NumPy. It can be used for reinforcement learning algorithms like value iteration, policy iteration, and Q-learning.

Features

A customizable grid-based environment with configurable:

Start and Goal positions

Traps (negative reward states)

Obstacles (impassable states)

Stochastic transitions (with probability p_success)

Supports value iteration for solving MDPs.

Provides transition dynamics for reinforcement learning algorithms.

Allows environment rendering in a simple text-based format.

Environment Details

The agent moves in a 4x4 grid.

Actions:

0: Move UP

1: Move DOWN

2: Move LEFT

3: Move RIGHT

The movement is stochastic:

With probability p_success, the agent moves in the intended direction.

Otherwise, it moves randomly in any of the four directions.

Rewards:

+1 for reaching the goal.

-1 for stepping into a trap.

0 for normal moves.

Value Iteration Algorithm

Overview

Value iteration is a dynamic programming approach to solving Markov Decision Processes (MDPs). It computes the optimal value function by iteratively updating the value of each state based on the Bellman equation.

Bellman Update Rule

The update rule for value iteration is:



where:

 is the value of state .

 is an action.

 is the next state.

 is the transition probability.

 is the reward received for transitioning from  to .

 is the discount factor (how much future rewards are valued).

Extracting Policy from Value Function

Once the optimal value function is computed, the optimal policy can be derived by choosing the action that maximizes expected value at each state:



This means that for each state, we:

Evaluate all possible actions.

Compute the expected value for each action.

Select the action with the highest expected value.