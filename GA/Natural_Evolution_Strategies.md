# Paper

- **Title**: Natural Evolution Strategies
- **Authors**: Tom Schaul, Tobias Glasmachers, Yi Sun, Jan Peters, Jurgen Schmidhuber
- **Link**: http://www.jmlr.org/papers/volume15/wierstra14a/wierstra14a.pdf
- **Tags**:
- **Year**: natural gradient, stochastic search, evolution strategies, black-box optimization, sampling

## What

Presented Natural Evolution Strategies(NES), a family of black-box optimization algorithms that use the natural gradient to update a parameterized search distribution in the direction of higher expected fitness. 

Evolution Strategies is essentially designed to cope with high-dimensional continuous-valued domains.

- evaluating the fitness
- keep the best genotypes and discard others
- survivors procreate(slightly mutating all of their genes)


Natural Evolution Strategies iteratively update a search distribution by using an estimated gradient on its distribution parameters.

- The parameterized search distribution is used to produce a batch of search points
- evaluating fitness function at each search point, allowing the algorithm to adaptively capture the local structure of the fitness function.
- performing a gradient ascent step on the parameters towards the higher expected fitness value along the natural gradient
- repeat this until a stopping criterion is met


Define the search gradient as the sampled gradient of expected fitness.




## How



## Result

## Conclusion
