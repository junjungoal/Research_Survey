# Paper

- **Title**: Diagnosing Bottlenecks in Deep Q-learning Algorithms
- **Authors**: Justin Fu * 1 Aviral Kumar * 1 Matthew Soh 1 Sergey Levine 1
- **Link**: https://arxiv.org/pdf/1902.10250.pdf
- **Tags**:
- **Year**: 2019

## What

Investigated issues in Q-learning, especially questions related to function approximation, sampling error and nonstationarity. Found that large NN architectures have many advantages regarding learning stability; offer several practical compensations for overfitting; and develop a novel sampling method based on explicitly compensating for function approximation error that yields fair improvement on high-dimensional continuous control domains.


## How

### Function Approximation and Convergence

Quantities: Trend between function approximation and performance, and a measure for the bias in the learning procedure introduced by function approximation.

Exact-FQI with uniform weighting (to remove sampling error), they measured the returns of the learning policy, and $l^{\infty}$ error between $Q^{*}$ and the solution found by Exact-FQI or the projection of the optimal solution. The difference between FQI error and projection error represents the bias introduced by the bootstrapping procedure, while controlling for bias that is simply due to function approximation -- **inherent Bellman error** of the function class.

=> Smaller architecture of a function approximator produce lower returns, converge to more suboptimal solutions, and introduce significant bias in the learning process.
=> Large network is significantly easier to train using bootstrapping and suffer less from nonconvergence issues.

### Sampling Error and Overfitting

Sampling Error = Generalisation error

- More samples leads to lower validation loss, confirming that overfitting can in fact occur
- Sampling from the replay buffer results in the lowest on-policy validation loss, despite bias due to distribution minibatch from sampling off-policy data => Replay Buffer reduce the effect of overfitting and create relatively good converge over the state space.


### Nonstationarity

Nonstationarities in both distributions and target values, when isolated, do not cause significant stability issues. Instead other factors such as sampling error and function approximation appear to have more significant effects on performance.


### Sampling or weighting distribution

High state-entripy and spread mass uniformaly among state-action pairs, seem to be highly effective for training. 

=> Proposed a new weighting distribution which balances high-entropy and state aliasing, **AFM**, that yields fair improvement in both tabular and continuous domains.

## Result

## Conclusion
