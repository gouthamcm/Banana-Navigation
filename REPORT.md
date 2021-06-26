# 1. Introduction

**How Deep Reinforcement Learning works?**

A simple introduction of the concept can be understood in this image:
![IMAGE OF RL AGENT](https://github.com/gouthamcm/Banana-Navigation/blob/main/RL.jpg)

# 2. Environment
The simulation contains a single agent that navigates a large environment.

State space

The state space has `37` dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.

Reward

A reward of `+1` is provided for collecting a yellow banana, and a reward of `-1` is provided for collecting a blue banana.

Actions

At each time step, it has four actions at its disposal:

`0` - walk forward
`1` - walk backward
`2` - turn left
`3` - turn right

# 3. Agent

The agent created on this project consists of an agent, a Deep Q-Learning and a memory unit.

Agent `dqn_agent.py`

The agent has the methods that interacts with the environment: `step()`, `act()`, `learn()` and some others.

Deep Q-Learning `model.py`

The architecture of the model is too simple, it's has an **input layer**, two **hidden layers** and then, an **output layer**.

# 4. Training Results

![Training Results](https://github.com/gouthamcm/Banana-Navigation/blob/main/Training%20results.png)

Agent has been trained for over 500 episodes to obtain an average reward of 13.0

# 5. Testing the Agent

See the video below to understand how the trained agent works

![Banana Navigator](https://github.com/gouthamcm/Banana-Navigation/blob/main/banana-navigator.gif)

# 6. Future Work

For further improvements, we can use a dueling network and implement prioritised memory.
