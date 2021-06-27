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

# 4.Hyperparameters

```
Replay buffer size = 1e5
discount rate = 0.99
learning rate = 5e-4
Target model update frequency : 4 time steps
Maximum steps per episode: 1000
Maximum episodes = 1000
Starting epsilion = 1.0
Ending epsilion = 0.01
Epsilion decay rate = 0.995
TAU = 1e-3
Batch Size = 64
Optimizer = Adam
Loss = MSE
```

Network Architecture:

Since the input is not an image, fully connected layers are used instead of Convolutional layers. The details of the network architecture are:
* Fully connected layer - **input** size is 37(state size) and **output** is 64 **activation** used is RELU
* Fully connected layer - **input** size is 64 and **output** is also 64 **activation** used is RELU
* Fully connected layer - **input** size is 64 and **output** is 4(action size)

The above model is defined using Pytorch.

# 5. Training Results

![Training Results](https://github.com/gouthamcm/Banana-Navigation/blob/main/Training%20results.png)

Agent has been trained for over 500 episodes to obtain an average reward of 13.0
Output of the training is shown below and at **526th** episode, the training got completed.

```
Episode 100	Average Score: 1.08
Episode 200	Average Score: 4.96
Episode 300	Average Score: 7.12
Episode 400	Average Score: 10.42
Episode 500	Average Score: 11.98
Episode 526	Average Score: 13.03
Environment solved in 526 episodes!	Average Score: 13.03
```

# 6. Testing the Agent

See the video below to understand how the trained agent works

![Banana Navigator](https://github.com/gouthamcm/Banana-Navigation/blob/main/banana-navigator.gif)

# 7. Future Work

For further improvements, we can use a dueling network and implement prioritised memory.
