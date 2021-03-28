[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135623-e770e354-7d12-11e8-998d-29fc74429ca2.gif "Trained Agent"
[image2]: https://user-images.githubusercontent.com/10624937/42135622-e55fb586-7d12-11e8-8a54-3c31da15a90a.gif "Soccer"


# Project 3: Collaboration and Competition

## Reinforcement Learning Environment
For this task we will be using the [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) environment which has two agents control rackets to bounce a ball over a net. The goal of the agent is to keep the ball in play for as long as possible.
The agent is trained using the DDPG algorithm. 

![Trained Agent][image1]

The environment is a precompiled unity task which can be downloaded from :

- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

### Rewards
If an agent hits the ball over the net, it receives a reward of +0.1.  If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01.  Thus, the goal of each agent is to keep the ball in play.

### Continuous State Space
The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation.  Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping. 

### Continuous Action Space
Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping. 

### Criterion for solving the task
The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
- This yields a single **score** for each episode.

The environment is considered solved, when the average (over 100 episodes) of those **scores** is at least +0.5.

## Setup 
My code is run in the Udacity workspace. All the necessary requirements are installed by running the first cell in the jupyter notebook:
!pip -q install ./python

Section `1. Starting the Environment`, installs all the dependencies and loads the necessary software libraries and modules. 
For setting this up on a local machine, please follow the instructions at [click here](https://github.com/udacity/deep-reinforcement-learning)

## Instructions

Please follow the instructions in `ReportTennis.ipynb` to train the agent. 
- Once the environment is setup, the continuous state and action space can be examined in Section 2 and 3.
- The hyper-parameters for the DDPG algorithm is provided in Section 4.1.
- The Actor-Critic Network Architecture is defined in Section 4.2 and the Replay Memory in Section 4.3.
- The DDPG agent is defined in Section 4.4 and trained in Section 4.5.

## Results
- Using this implementation, the task was solved in just 961 episodes. The plot of rewards vs number of episodes is provided in Section 5.
- The actor and critic model weights are provided as `DDPG_Actor.pth` and `DDPG_Critic.pth`. 
