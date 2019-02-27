# Paper

- **Title**: A Study of AI Population Dynamics with Million-agent Reinforcement Learning
- **Authors**: Yaodong Yang, Lantao Yu, Yiwei Bai, Jun Wang, Weinan Zhang, Ying Wen, Yong Yu
- **Link**: https://arxiv.org/pdf/1709.04511.pdf
- **Tags**: RL, Multu-Agent, Self-organization, Lotka-Volterra model
- **Year**: 2018

## What

Simulated the ordered collective system by using Deep Reinforcement Learning. It turned out to be similar to the Lotka-Volterra model.

In previous works, only a few multi agent is applied to tasks, which can be seen as micro-level simulation. However, in this work, they scaled it up to macro-level simulation by using million agents.

## How

Two-players: prey and Predator
Action Space of predator: forward, backward, left, right, rotate left, rotate right, stand still, join a group, and leave a group
Environment: infinite horizon

Predator can make a group to capture the prey effectively. 
Prey and Predator face the hazards of either being hunted as preys, or dying of starvation. To encourage this idea, they used the health status of the predator which decreases with time.

#### Model
- DQN
- Reply buffer is different from the one for the traditional DQN which maintains a first-in-first-out queue across different time step.
- calculate Q-value for each agent


## Result

Their model reveals an ordered pattern when measuring the transition of the population, and it also shows consistency to Lotka-Volterra model.
The emergent collective adaptations when the environmental resources changed over time.

## Conclusion

## Comment

what about food chain?
Is this realistic? => including individual size or speed would be more realistic? 
For example, a new individual is basically small and slow to mode. Therefore, it is easily captured by the predator. However, probably bigger prey would try to protect those small individuals?????



