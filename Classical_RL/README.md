# Gridworld MDP

This project implements a **Gridworld Markov Decision Process (MDP)** environment in Python using NumPy. It is then used in implementation of classical RL algorithms like  **Value iteration**, **Policy iteration**, **Q-value iteration** and **Max-Ent value iteration**.

## Features

- A customizable **grid-based environment** with configurable:
  - **Start and Goal positions**
  - **Traps** (negative reward states)
  - **Obstacles** (impassable states)
  - **Stochastic transitions** (with probability `p_success`)
- Supports **value iteration** for solving MDPs.
- Provides **transition dynamics** for reinforcement learning algorithms.
- Allows environment rendering in a simple text-based format.

## Environment Details

- The agent moves in a **4x4 grid**.
- Actions:
  - `0`: Move **UP**
  - `1`: Move **DOWN**
  - `2`: Move **LEFT**
  - `3`: Move **RIGHT**
- The movement is **stochastic**:
  - With probability `p_success`, the agent moves in the intended direction.
  - Otherwise, it moves randomly in any of the four directions.
- Rewards:
  - `+1` for reaching the goal.
  - `-1` for stepping into a trap.
  - `0` for normal moves.

---

* **Value Iteration:** An algorithm that learns the optimal state-value function through iterative updates.
* **Policy Iteration:** An algorithm that alternates between policy evaluation and policy improvement to find the optimal policy.
* **Q-Value Iteration:** An algorithm that learns the optimal Q-values (action-value function) through iterative updates.
* **Max-Ent Value Iteration:** A variation of value iteration that promotes exploration and stochastic policies by incorporating maximum entropy principles.

## Algorithms Explained

### Value Iteration

Value Iteration is a dynamic programming algorithm that aims to find the optimal state-value function, which represents the expected cumulative reward from a given state. By iteratively updating the value function based on the Bellman optimality equation, the algorithm converges to the optimal values. The optimal policy can then be derived by selecting the action that leads to the highest expected value in the next state.

### Policy Iteration

Policy Iteration consists of two main steps: policy evaluation and policy improvement. In policy evaluation, the value function of the current policy is calculated. In policy improvement, the policy is updated by selecting the action that maximizes the expected reward based on the evaluated value function. These two steps are repeated until the policy converges to the optimal policy.

### Q-Value Iteration

Q-Value Iteration is a dynamic programming algorithm that aims to find the optimal Q-values, which represent the expected cumulative reward for taking a specific action in a given state. By iteratively updating the Q-values based on the Bellman optimality equation, the algorithm converges to the optimal Q-values. The optimal policy can then be derived by selecting the action with the highest Q-value for each state.

### Max-Ent Value Iteration

Max-Ent Value Iteration is a modification of value iteration that incorporates the principle of maximum entropy. Instead of simply maximizing the expected reward, it aims to find a policy that maximizes both the expected reward and the entropy of the policy. This leads to policies that are more stochastic and robust, promoting exploration and handling uncertainty in the environment. This is accomplished by replacing the standard max operation in the value function update with a "soft max" operation.



