# Banana-Navigation
This project trains an agent to navigate (and collect bananas!) in a large, square world.

The goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The project environment is similar to, but not identical to the Banana Collector environment on the [Unity ML-Agents GitHub page!](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#banana-collector).

![Banana Navigator](https://github.com/gouthamcm/Banana-Navigation/blob/main/banana-navigator.gif)

# Installation
Step 1. Clone the DRLND Repository
Please follow the [instructions in the DRLND GitHub repository!](https://github.com/udacity/deep-reinforcement-learning#dependencies) to set up your Python environment. These instructions can be found in README.md at the root of the repository. By following these instructions, you will install PyTorch, the ML-Agents toolkit, and a few more Python packages required to complete the project.

Step 2. Download the Unity Environment
* Linux: [click here!](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
* Mac OSX: [click here!](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
* Windows (32-bit): [click here!](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
* Windows (64-bit): [click here!](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

Then, place the file in the p1_navigation/ folder in the DRLND GitHub repository, and unzip (or decompress) the file.

# Working

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:
* 0-move forward
* 1-move backward
* 2-turn left
* 3-turn right

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

# Instructions to run the code

**Module Description**

`model.py` - defines the Q architecture
`dqn_agent.py` - defines the DQN Agent

Open the jupyter notebook `Navigation.ipynb` and run the cells for the successful training of the agent. The code is well documented.
Make sure `model.py` and `dqn_agent.py` are also in the same directory.
