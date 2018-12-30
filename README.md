## Continuous control for DRLND Udacity Nanodegree
--- 
This is the second project in the Udacity Deep Reinforcement Learning Nanodegree. The task is to train a double-jointed arm to target locations.

The environment implementation to train on is [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher)

![reacher gif](https://github.com/doctorcorral/DRLND-p2-continuous/raw/master/images/reacherg.gif)


## Project Details
In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location.
It is, the arm must follow the target as much as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

## Getting Started
Follow the Udacity DRL ND dependencies [instructions here](https://github.com/udacity/deep-reinforcement-learning#dependencies) 

Be sure of install [Unity ML-Agents](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Installation.md), [NumPy](http://www.numpy.org/) and [PyTorch](https://pytorch.org/) 

Download a prebuilt simulator

### Singe agent:
Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

### Twenty Agents:
Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

Place this file in the same directory as this repo content.



## Instructions
Run the [`DDPG_Continuous_Control.ipynb`](https://github.com/doctorcorral/DRLND-p2-continuous/blob/master/DDPG_Continuous_Control.ipynb) notebook using the drlnd kernel to train the DDPG agent.

Use `ddpg` function to perform the training. This function returns a dictionary containing relevant internal variables that can be fed again to this function to continue training where it was left. Play around with this, change hyper parameters in between training runs to train your own intuition.

This problem is said to be solved when you hit a `30` score (see an example [Reward Plot](https://github.com/doctorcorral/DRLND-p2-continuous/blob/master/output/result.png?raw=true)).

Once trained the model weights will be saved in the same directory in the files `checkpoint_actor.pth` and `checkpint_critic.pth`.

The model weights are used by the [`run_agent.ipynb` ](https://github.com/doctorcorral/DRLND-p2-continuous/blob/master/run_agent.ipynb) notebook against the simulator. 
