This is a fork of the [original repository](https://github.com/spov-research/purl.git) under the project [Smart_POV](https://github.com/hamidrezafahimi/Smart_POV.git) which funds basics for intelligence development on simulated voyager agents. The original code is editted such that it simply interacts - and may be evaluated - with our developed professional (D)RL-evaluation platform [MIIO2V](https://github.com/mohammadr-kaz/MIIO2V.git). A comparison of this project with [other similar works]() id documented [here]().

## Prerequisites

- Ubuntu 20.04
- ROS Noetic
- Anaconda

## How to Run
1. Clone the repository.
```sh
git clone https://github.com/spov-research/purl.git
cd purl
```

2. Create a conda environment with python 3.6 and tensorflow 1.13.1 then activate it.
```sh
conda create -n purl python=3.6 tensorflow=1.13.1
activate purl
```
3. Install the requirements.
```sh
pip install -r requirements.txt
```

### `train`

To train a model, run:

```sh
./purl train
```

For example, to train a model using the PPO algorithm on the `MiniGrid-LavaCrossingS9N1-v0` environment, use the following arguments:

```
./purl train --algorithm ppo --environment MiniGrid-LavaCrossingS9N1-v0
```

- Algorithms
MDP (using the `FullyObsWrapper`)
* Q-table
* Q-network
POMDP
* PPO
* DQN (with the Double DQN extension) - work in progress, not currently working as intended
* DRQN  - work in progress, not currently working as intended

### `visualize`

To visualize a model, run:

```sh
./purl vizualize
```
