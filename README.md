[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

# Project Navigation

### Introduction

This project consists of training an agent to navigate (and collect bananas!) in a large, square world.  

This is how a well trained banana lover agent looks like:

![Trained Agent][image1]

### Unity Environment
After downloading the Unity Environment and saving it into the same folder where the main notebook `Navigation.ipynb` sits, one can load the env by running the following code:

> `env = UnityEnvironment(file_name="Banana.app")`
>
>  `brain_name = env.brain_names[0]`
>
>  `brain = env.brains[brain_name]`
>
>  `env_info = env.reset(train_mode=True)[brain_name]`


### Problem Definition and success criteria
In RL, any problem should be defined as MDP (Markov Decision Process) that consists of States, Actions, Reward function and Transition Fucntion

#### States

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  

One can check how the state vector looks like by running the following code:

> `state = env_info.vector_observations[0]`
> `print(state)`


#### Actions

Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

One can check the number of actions:

> `print(brain.vector_action_space_size)`


#### Rewards

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

#### When the task is considered solved

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.


### Getting Started

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.

2. Place the file in the `p1_navigation/` folder, and unzip (or decompress) the file. 

3. 
