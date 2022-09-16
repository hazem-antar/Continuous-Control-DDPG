
Continuous Control project using a DDPG algorithm in Reinforcement Learning

# Udacity Deep Reinforcement Learning Nanodegree
## Project 2 - Continuous-Control-DDPG

This is the second project for the Udacity Deep Reinforcement Learning Nanodegree. The goal is to implement model based on [Deep Deterministic Policy Gradient (DDPG)](https://arxiv.org/abs/1509.02971)to allow controlling a group of robotic arms in a Unity ML-Agents environment. 

![Trained DQN Agent](./img/1_8-NXPwKsxg5QYfzaRqKeYg.gif)
## Environment description

The simulation contains a single agent navigating in a large, square environment.

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has **37 dimensions** and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. **Four discrete actions** are available:

- `0` - walk forward 
- `1` - walk backward
- `2` - turn left
- `3` - turn right

The task is episodic, and in order to solve the environment, the agent must get an average score of **+13** over 100 consecutive episodes.

## Dependencies Installation and Usage Guide

1. Prepare new Conda environment (with python 3.6) following guidelines on [Udacity DRL repo](https://github.com/udacity/deep-reinforcement-learning#dependencies) 


2. Install the `unityagents` package with:

```sh
pip install unityagents==0.4.0
```

3. Download custom Banana environment (Unity ML-Agents env) prepared by Udacity

Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

The file needs to placed in the root directory of this repository and unzipped.

Path to the executable has to be provided to `UnityEnvironment` function in `Navigation.ipynb` 

For example on 64-bit Windows:
```python
env = UnityEnvironment(file_name="./Banana_Windows_x86_64/Banana.exe")
```

4. Run the `Navigation_Project.ipynb` notebook to either train the DQN agent from scratch or use the already trained model weights in the file `checkpoint.pth`.

5. You can see how trained agent move in environment by running the last cell in the notebook.
