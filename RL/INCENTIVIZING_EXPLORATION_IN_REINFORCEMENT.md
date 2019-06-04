# Paper

- **Title**: INCENTIVIZING EXPLORATION IN REINFORCEMENT LEARNING WITH DEEP PREDICTIVE MODELS
- **Authors**:
- **Link**: https://arxiv.org/pdf/1507.00814.pdf
- **Tags**: Reinforcement Learning
- **Year**: 2016

## What
Suggested a new efficient and scalable exploration method based on assigning exploration bonuses from a concurrently learned model of the system dynamics, which is applicable to high dimensional state space.

## How

We want to encourage agent exploration by giving the agent exploration bonuses for visiting novel states, thus identifying the novel states are required. To achieve this, we need to supply some representation of the agent's state space, as well as a mechanism to use this representation to assess its novelty. => Unsupervised learning, representation learning 

In this work, they used the representation learning with NNs.

Let $\sigma(s)$ be the encoding of the state s, and let $M_{\phi}: \sigma(S) \times A \rightarrow \sigma $ be a dynamics predictor parameterized by. $\phi $.

The prediction error is represented by 

$$
e(s_{t}, a_{t}) = ||\sigma(s_{t+1}-M_{\phi}(\sigma(s_{t}, a_{t})))||
$$

Then, we assign the novelty function to a reward function

$$
R_{Bonus}(s, a)  = R(s, a) + \beta(\frac{e_{t}(s_{t}, a_{t})}{t*C})
$$

where C is a decay constant.

The input is the representation derived from the intermediate layer in Autoencoder.

## Result

## Conclusion
