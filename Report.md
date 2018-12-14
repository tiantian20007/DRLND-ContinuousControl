# Method

## Algorithm
We use typical **Deep Deterministic Policy Gradients (DDPG)** to train our agent.
The algorithm is implemented in ddpg_agent.py and the ddpg function in Continuous_Control.ipynb.

### Deep Deterministic Policy Gradients (DDPG)
![alt text](https://github.com/tiantian20007/DRLND-ContinuousControl/blob/master/res/ddpg.png "DDPG")

### DNN
We use a deep neural networks as the proximation for the Q functions instead of the tradition Q table.
