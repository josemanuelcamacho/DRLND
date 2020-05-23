# REPORT: P1 Navigation


## Learning Algorithm

The report clearly describes the learning algorithm, along with the chosen hyperparameters. It also describes the model architectures for any neural networks.
The chosen algorithm to solve the environment is MLP (multi-layer perceptron) with 3 layers of input/output sizes:

- Input Layer: (state_size, 8 * state_size)
- Hidden Layer 1: (8 * state_size, 4 * state_size)
- Hiden Layer 2: (4 * state_size, action_size)
- Output Layer: (action_size, action_size)

Activation function is ReLU for input and hidden layers.

Following hyperparameters are used along with an Adam Optimizer for weight updates during backprop.

- BUFFER_SIZE = int(1e5)  # replay buffer size
- BATCH_SIZE = 64         # minibatch size
- GAMMA = 0.99            # discount factor
- TAU = 1e-3              # for soft update of target parameters
- LR = 5e-4               # learning rate 
- UPDATE_EVERY = 4        # how often to update the network


## Plot of Rewards
	
Following plot shows rewards per episode. It is included to illustrate that the agent is able to receive an average reward (over 100 episodes) of at least +13 before 1800th episode is reached.

![Score per episode](./score.png?raw=true)

## Ideas for Future Work

- Increase the number of hidden layers and neurons per layer.
- Try an CNN which keeps up with several consecutive states.
- Try hyperopt or optuna packages for further hyperparameter optimization.

