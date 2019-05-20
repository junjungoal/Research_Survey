# Paper

- **Title**: Multi-Agent Actor-Critic for Mixed Cooperative-Competitive Environments
- **Authors**: Ryan Lowe, Yi Wu, Aviv Tamar, Jean Harb, Pieter Abbeel, Igor Mordatch
- **Link**: https://arxiv.org/abs/1706.02275
- **Tags**:
- **Year**: 2017

## What
They proposed an adaptation of actor-critic methods that considers action policies of other agents and is able to successfully learn policies that require complex multi-agent coordination.
Also, they introduced a training regimen utilizing an ensemble of policies for each agent that leads to more robust multi-agent policies. 

Traditional algorithms in multi-agent reinforcement learning such as Q-learning suffer from the non-stationarity of the environment caused by change in polices in agents. 


## How
In this method, an agent does not obtain other agents' actions, but approximate those. The method is a simple extension of actor-critic policy gradient methods where the critic is augmented with extra information about the policies of other agents. 

## Result

## Conclusion
