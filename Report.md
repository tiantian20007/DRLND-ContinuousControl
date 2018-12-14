# Method

## Algorithm
We use typical **Deep Deterministic Policy Gradients (DDPG)** to train our agent.
The algorithm is implemented in ddpg_agent.py and the ddpg function in Continuous_Control.ipynb.

### Deep Deterministic Policy Gradients (DDPG)
![alt text](https://github.com/tiantian20007/DRLND-ContinuousControl/blob/master/res/ddpg.png "DDPG")

### DNN
We use one deep neural network mapping states to a specific action (Actor), and another deep neural network as the proximation for the Q functions (Critic).

### Fixed Q-Targets
In Q-Learning, we update a guess with a guess, and this can potentially lead to harmful correlations. To avoid this, we can update the parameters w in the network q^ to better approximate the action value corresponding to state _S_ and action _A_ with the following update rule:
![alt text](https://github.com/tiantian20007/DRLND-Navigation/blob/master/res/fix-target.png "Fixed Q-Targets")

where w<sup>-</sup> are the weights of a separate target network that are not changed during the learning step, and (_S_, _A_, _R_, _S'_) is an experience tuple.
 
We use the same method for the Actor network updating.

## Model architectures
The actor DNN contains 2 hidden layers, the first has 200 neuron units and the second has 150. Actor DNN Ouputs the actions. 

The critic DNN contains also contains 2 hidden layers, the first has 200 neuron units and the second has 150. 

The actions calculated by the Actor DNN will be concatenated to the first critic hidden layer's output, and to be the input of the second critic hidden layer. 

We choose relu as the activate function.
The mode is implemented in model.py. 

## Hyperparameters

- BUFFER_SIZE = int(1e6)  # replay buffer size
- BATCH_SIZE = 128        # minibatch size
- GAMMA = 0.99            # discount factor
- TAU = 1e-3              # for soft update of target parameters
- LR_ACTOR = 1e-3         # learning rate of the actor 
- LR_CRITIC = 1e-3        # learning rate of the critic
- WEIGHT_DECAY = 0        # L2 weight decay

- eps_start=1.0
- eps_end=0.01
- eps_decay=1e-6

# Rewards

![alt text](https://github.com/tiantian20007/DRLND-ContinuousControl/blob/master/res/result.png "Result")

# Future Work

[Distributed Distributional Deep Deterministic Policy Gradient algorithm, D4PG](https://openreview.net/forum?id=SyZipzbCb)

This algorithm are implemented as a neural network layer mapping the output of the
critic torso (see Figure 1) to the parameters of a given distribution

![alt text](https://github.com/tiantian20007/DRLND-ContinuousControl/blob/master/res/d4pg.png "d4pg")

A modification to the DDPG update which utilizes N-step returns when estimating the TD error. This can be seen as replacing the Bellman operator with an N-step variant

![alt text](https://github.com/tiantian20007/DRLND-ContinuousControl/blob/master/res/N-stepTD.png "N-stepTD")



