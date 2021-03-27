[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"

# Project 2: Continuous Control

## Reinforcement Learning Environment
For this task we will be using the Reacher environment which has a double-jointed robotic arm that should move to target locations shown by the green spheres. The goal of the agent is to maintain the position of the end-effector at the target location for as long as possible.
The agent is trained using the DDPG algorithm. 

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

Section `1. Starting the Environment`, installs all the dependencies and loads the necessary software libraries and modules. 
For setting this up on a local machine, please follow the instructions at [click here](https://github.com/udacity/deep-reinforcement-learning)

## Instructions

Please follow the instructions in `Report.ipynb` to train the agent. 
- Once the environment is setup, the continuous state and action space can be examined in Section 2 and 3.
- The hyper-parameters for the DDPG algorithm is provided in Section 4.1.
- The Actor-Critic Network Architecture is defined in Section 4.2 and the Replay Memory in Section 4.3.
- The DDPG agent is defined in Section 4.4 and trained in Section 4.5.

## Results
- Using this implementation the task was solved in just 1347 episodes. The plot of rewards vs number of episodes is provided in Section 5.
- The actor and critic model weights are provided as `DDPG_actor_single.pth` and `DDPG_critic_single.pth`. 
