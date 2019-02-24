# Paper

- **Title**: Evolution Strategies as a Scalable Alternative to Reinforcement Learning
- **Authors**: Tim Salimans, Jonathan Ho, Xi Chen, Szymon Sidor, Ilya Sutskever
- **Link**: https://arxiv.org/abs/1703.03864
- **Tags**: Reinforcement Learning, Evolution Strategies
- **Year**: 2017

## What
- Suggested the use of Evolution Strategies as an alternative to MDP-based RL method.
- The use of virtual batch normalization and other reparameterizations of the NN policy improve the reliability of evolution strategies.
- parallelizability of ES
- Better Data Efficiency
- Better Exploration than policy gradient methods such as TRPO
- More robust

**Black-box optimization such as Neural Evolution Strategies is indifferent to the distribution of rewards(sparse or dense), no need for backpropagating gradients. However, it's still less effective at solving hard RL tasks comparing to Q-learning and some policy gradient methods.**

## How

This work uses ES which belongs to the class of Neural Evolution Strategies. 

- Stochastically perturbing the parameters of the policy and evaluating the resulting parameters by running an episode in the environment
- Combining the results of multiple episodes, calculating a stochastic gradient estimate, updating the parameters.


Exploration in ES depends on parameters $\theta$, but sampling actions like Q-learning and policy gradient methods. Thus, we  need to ensure that perturbing the parameters by Gaussian noise sometimes lead to new individuals $\theta + \sigma\epsilon$ with better return. Since ES does not properly explore in some environments, they introduced virtual batch normalization which is essentially equivalent to batch normalization to make the policy more sensitive to very small changes in the input image at the early stages of training when the weights of the policy are random, leading that the policy takes a wide-enough variety of actions to gather occasional rewards.

## Result


## Conclusion
