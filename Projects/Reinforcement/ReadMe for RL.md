# Introduction
Hello there!  My first assignment

Starting off with a lot of motivation  SO will try to cover all lectures first before touching the Research paper to get a better idea

# Flow
1. Lectures @UCL + Barto Sutton


THe book seemed very strange in the start. but the lectures were a great "preface " i would say to the book. Learned a lot of things such as the finite-MLPs and others. PRetty much in the starting few days were just spent on the basic concepts themselves, such as understanding what MDPs areand how they work around. Dynamic programming then methods like Monte Carlo sampling me a lot of struggles but the book came through here providing a strit theory with the intuition being derived from the lectures. Also learn about bootstrapping also not so useful nowadays. Temporal difference(lamda) was probably a game changeer for me . Yet not feeling confident in them i started the paper and learnt the relevant methods on the way.
# Assignment

## A small review of the Paper
The paper addresses the challenge of exploration in reinforcement learning, where agents must explore their environment to discover new and informative states/actions. Traditional exploration strategies, such as ε-greedy or softmax exploration, may not be efficient in complex environments.  
The authors propose an intrinsic curiosity model (ICM) that incentivizes agents to explore by rewarding them for visiting states/actions that lead to novel or unexpected outcomes. The key idea is to use self-supervised learning to predict the consequences of actions taken by the agent. The agent is rewarded based on the prediction error of the self-supervised model, encouraging it to seek out states/actions where the model's predictions are uncertain.

## The code and the Idea:
### actor_critic
Building from the asynch A3C paper first coding out our DQN:  
Network update is : 5 actions but 20 actions work better  
Input shape in original paper 4x84x84
I am doing 4 x42x42 and its consistent with the ICM paper  
Adding layer to network  
4 Conv layers  
Rec.Layer: Gated Rec. Layer 256 units  -> 2 outputs  
pi -> n_actions (softmax activation)   
V -> no activation  
Forward prop return actions, values , log prob, hidden state  
Disc. factor: 0.99  
Beta:0.01  

### icm module
4 Conv layers same as a3c  
Inverse: concat two features and pass through linear layer with 256 units followed with n_actions  
Forward: concat feature vector and action and pass through 2 liner layers with 256 and 288 units  
hyp-params:  
lambda=0.1  beta =0.2  lr.=0.0001  
Loss same as in the paper  
modify worker , parallel_env, main to accept global icm optimizer  

### Main idea:
Running parallel agents on different threads and stacking all the states, actions and then running them through the model.  


## Implementation
Was facing a lot of issues with the environment compatibilty and hence not completed due to time crunch.

## Summary
Pretty much to learn and RL seems pretty interesting will continue it.


