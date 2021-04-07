# Project Overview

### Learning Algorithm

#### Learning algorithm

The chosen algorithm for solving the project is Deep Q-Learning with the single mention that it is not using error clipping.

Tha algorithm consists of two main steps:

1. Sample: At first, the agent interacts with the environment and stores the experience tuples in agent's "Memory". Agent is choosing the action at each step based on the e-greedy policy.

2. Learn: As soon as the agent has enough experiences, he then samples a batch from its "Memory" in order to learn. 

#### Hyperparameters

We have the following hyperparameters we need to work with:
* Replay buffer size, `BUFFER_SIZE` represent the "Memory" we want our agent to have. Ideally we would like as much memory as we can get.
* Learning mini batch size, `BATCH_SIZE` is the amount of samples we will extract from "Memory" in order to learn based on.
* The discount factor, `GAMMA` is mainly the discount that we apply on the next state and its best action pair value. We could play with this factor  in order to balance the long and short term agent objectives.
* The update rate, `TAU`, one should think about this as a learning rate for weights from local network to target network
* learning rate, `LR`
* UPDATE_EVERY

#### Model architectures for NN


### Plot of Rewards

![RewardsPlot][report_episode_score.png]

### Ideas for Future Work


