[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

# Project 1: Navigation

## Reinforcement Learning Environment

For this project, an agent was trained using the DQN and Double DQN algorithm to navigate (and collect bananas!) in a large, square world. 
The environment is a precompiled unity task which can be downloaded from :
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip) 
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip) 
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip) 
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip) 

![Trained Agent][image1]

### Rewards
A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

### Continuous State Space
The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  

### Discrete Action Space
Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

### Criterion for solving the task
The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

## Instructions

Follow the instructions in `Navigation_RS.ipynb` to train the agent.
The training algorithm (DQN or Double DQN) can be specified by passing the argument "DQN" or "DDQN" while instantiating the Agent.

## Results
Using this implementation the task was solved in just 398 episodes using DQN and 392 episodes using Double DQN.
For comparison, the benchmark implementation provided by Udacity solves it in 1800 episodes. 
Please check the `Report_RS.pdf` for more information. 

