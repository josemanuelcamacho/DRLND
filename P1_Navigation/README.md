[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

# Project 1: Navigation

### Introduction

For this project, you will train an agent to navigate (and collect bananas!) in a large, square world.  

![Trained Agent][image1]

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

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
``````

This repository already contains the environment ready for Mac OSX. Download the environment that matches your operating system using the following links:
- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/VisualBanana_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/VisualBanana.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/VisualBanana_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/VisualBanana_Windows_x86_64.zip)

Then, place the file in the `DRLND/P1_Navigation/` folder in the working folder, and unzip (or decompress) the file.

Start a Jupyter session and check that you can see the `Navigation.ipynb` file:

``````sh
jupyter notebook
``````


### Instructions

Follow the instructions in `Navigation.ipynb` to get started with training your own agent!  

Make sure you update the path to 'Banana' environment according to the instructions given in the notebook before second cell.

Run cells until you reach the section 'FINAL AGENT' which is reserved to see the best trained agent in action. Before you run cells in this 'FINAL AGENT' section, make sure you are pointing to the right 'pth' file, i.e., 'checkpoint_<best.score>.pth'.
