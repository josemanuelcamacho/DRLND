# REPORT: P2 Continuous Control


## Learning Algorithm

The report clearly describes the learning algorithm, along with the chosen hyperparameters. It also describes the model architectures for any neural networks.
The chosen algorithm to solve the environment is two MLP (multi-layer perceptron). Two consecutive states are buffered and used as input in order to estimate target velocity.

#### ACTOR with batch normalization and 3 layers of input/output sizes:

- Input Layer: (2 * state_size, 256)
- Hidden Layer 1: (256, 128)
- Hiden Layer 2: (128, action_size)
- Output Layer: (action_size, action_size)

Batch normalization takes place at input layer. Activation function is 'ReLU' for input and hidden layers. 'Tanh' for output layer to achieve continuous control output.

#### CRITIC with batch normalization and 3 layers of input/output sizes:

- Input Layer: (2 * state_size, 128)
- Hidden Layer 1: (128, 64)
- Hiden Layer 2: (64, 32)
- Output Layer: (32, 1)

Batch normalization takes place at input layer. Activation function is 'ReLU' for input and hidden layers.


#### Hyperparameters
Following hyperparameters are used along with an Adam Optimizer for weight updates during backprop.

- BUFFER_SIZE = int(1e6)  # replay buffer size
- BATCH_SIZE = 512         # minibatch size
- GAMMA = 0.95            # discount factor
- TAU = 1e-1              # for soft update of target parameters
- LR_ACTOR = 1e-4               # learning rate
- LR_CRITIC = 1e-3               # learning rate
- WEIGHT_DECAY = 0
- UPDATE_EVERY = 20        # how often to update the network


## Plot of Rewards
	
Following plot shows rewards per episode. It is included to illustrate that the agent is able to receive an average reward (over 100 episodes) of at least +30 and hold it.

<img src="https://raw.githubusercontent.com/josemanuelcamacho/DRLND/master/P2_ContinuousControl/score.png" width="50%" height="20%">

## Ideas for Future Work

- Increase the number of hidden layers and neurons per layer.
- Try an CNN which keeps up with several consecutive states.
- Try hyperopt or optuna packages for further hyperparameter optimization.

