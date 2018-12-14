# DRLND-ContinuousControl
Navigation project for Deep Reinforcement Learning Nanodegree Program

# Environment
For this project, we will work with the Reacher environment provided by Udacity.

![alt text][env]
[env]: https://github.com/tiantian20007/DRLND-ContinuousControl/blob/master/res/env "Reacher"

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

# Environment setup

## Step 1: Clone the DRLND Repository
If you haven't already, please follow the [instructions in the DRLND GitHub repository](https://github.com/udacity/deep-reinforcement-learning#dependencies) to set up your Python environment. These instructions can be found in README.md at the root of the repository. By following these instructions, you will install PyTorch, the ML-Agents toolkit, and a few more Python packages required to complete the project.

(For Windows users) The ML-Agents toolkit supports Windows 10. While it might be possible to run the ML-Agents toolkit using other versions of Windows, it has not been tested on other versions. Furthermore, the ML-Agents toolkit has not been tested on a Windows VM such as Bootcamp or Parallels.

## Step 2: Download the Unity Environment - Version 2: Twenty (20) Agents
For this project, you will not need to install Unity - this is because we have already built the environment for you, and you can download it from one of the links below. You need only select the environment that matches your operating system:

- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

**Then, place the file in the root folder in the this cloned repository, and unzip (or decompress) the file.**

(For Windows users) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

# Run the code

## Step 1: Start a IPython kernel
Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment. Execute following code in the "python" folder of your cloned [DRLND GitHub repository](https://github.com/udacity/deep-reinforcement-learning)
```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```
## Step 2: Start the jupyter notebook in this repository: Navigation.ipynb
Before running code in the notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. 

![alt][jupyternotebook]

[jupyternotebook]: https://user-images.githubusercontent.com/10624937/42386929-76f671f0-8106-11e8-9376-f17da2ae852e.png "Logo Title 3"

## Step 3: Run the code one cell by one
The model file will be saved as checkpoint.pth in the root folder

# Result
Our agent got an average score of +30 over 100 consecutive episodes after 637 episodes traning.

![alt text][result]

[result]: https://github.com/tiantian20007/DRLND-ContinuousControl/blob/master/res/result.png "Result"
