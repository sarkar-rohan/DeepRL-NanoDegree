[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"

# Project 2: Continuous Control

## Reinforcement Learning Environment
For this task we will be using the Reacher environment which has a double-jointed obotic arm that should move to target locations shown by the green spheres. The goal of the agent is to maintain the position of the end-effector at the target location for as long as possible.
The agent was trained using the DDPG algorithm. 

The environment is a precompiled unity task which can be downloaded from :
Version 1: One agent

- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)
    
Version 2: Twenty agents

- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

![Trained Agent][image1]

### Rewards
A reward of +0.1 is provided for each time-step that the agent is able to hold the end-effector in the target ocation. Thus, the goal of the agent is to hold the hand at the target location for the maximum possible duration.  

### Continuous State Space
The state space has 33 dimensions and contains information related to the position, rotation, velocity and angular velocities of all the joints of the arm.

### Continuous Action Space
The action space is represented by a four dimensional vector with information related to the torque to be applied to the two joints of the arm for holding the end-effector at the target location. 

### Criterion for solving the task
The task is episodic, and in order to solve the environment, the agent must get an average score of +30 over 100 consecutive episodes.
## Setup 
My code is run in the Udacity workspace. All the necessary requirements are installed by running the first cell in the jupyter notebook:
!pip -q install ./python

This installs the dependencies mentioned in requirements.txt file. For setting this up on a local machine, please follow the instructions at 
[click here](https://github.com/udacity/deep-reinforcement-learning)

## Instructions

Follow the instructions in `Navigation_RS.ipynb` to train the agent.
The training algorithm (DQN or Double DQN) can be specified by passing the argument "DQN" or "DDQN" while instantiating the Agent, as mentioned below: 
- agent = Agent(state_size, action_size, seed, "DQN")
- agent = Agent(state_size, action_size, seed, "DDQN") 

## Results
- Using this implementation the task was solved in just 398 episodes using DQN and 392 episodes using Double DQN.
For comparison, the benchmark implementation provided by Udacity solves it in 1800 episodes. 
- Please check the `Report_RS.pdf` for more information. 
- The model weights are provided in checkpoint.pth
