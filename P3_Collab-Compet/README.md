[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135623-e770e354-7d12-11e8-998d-29fc74429ca2.gif "Trained Agent"
[image2]: https://user-images.githubusercontent.com/10624937/42135622-e55fb586-7d12-11e8-8a54-3c31da15a90a.gif "Soccer"


# Project 3: Collaboration and Competition

### Introduction

For this project, you will work with the [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) environment.

![Trained Agent][image1]

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1.  If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01.  Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation.  Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping. 

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
- This yields a single **score** for each episode.

The environment is considered solved, when the average (over 100 episodes) of those **scores** is at least +0.5.

    
### Getting Started
Create or cd into the working folder of your choice and clone the repository  

``````sh
mkdir workdirname && cd workdirname
git clone https://github.com/josemanuelcamacho/DRLND.git
``````

Enter into the cloned folder and create a conda environment with the packages indicated in `environment.yml`:

``````sh
cd DRLND/P1_Navigation
conda create -f environment.yml
conda activate drlnd
cd ../P3_Collab-Compet
``````

This repository already contains the environment ready for Mac OSX. You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)
        
Then, place the file in the `DRLND/P3_Collab-Compet/` folder in the working folder, and unzip (or decompress) the file.

Start a Jupyter session and check that you can see the `Tennis.ipynb` file:

``````sh
jupyter notebook
``````


### Instructions

Follow the instructions in `Tennis.ipynb` to get started with training your own agent!  

Make sure you update the path to 'Tennis' environment according to the instructions given in the notebook before second cell.

Run cells down until Section 3. If you are already familiar with the Unity environment, skip Section 3 and jump directly into Section 4 to train the agent. You can run my version using the weights in this repository and the code in section 5. 

Before you run cells in '5. Play Best Agent' section, make sure you are pointing to the right 'pth' file, i.e., 'checkpoint_<best.score>.pth'. Provided best model corresponds to 'checkpoint_<agenttype>.1.99.pth' file.
