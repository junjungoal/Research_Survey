# Paper

- **Title**: Curriculum Adversarial Training
- **Authors**: Qi-Zhi Cai, Min Du, Chang Liu, Dawn Song
- **Link**: https://arxiv.org/abs/1805.04807
- **Tags**: Adversarial example, curriculum learning
- **Year**: 2018

## What

Proposed the defense mechanism against to adversarial examples by making use of curriculum learning. The state-of-the-art result shows that adversarial training can be applied to train a robust model on MNIST, but not for more complex dataset. In this work, they proposed a method which is also applicable to such complex dataset, and its performance on non-adversarial inputs is still comparable to the state-of-the-art model. 

## Background

Adversarial examples
$$
f_{\theta}(x^{*})  \neq y \wedge d(x, x^{*} \leq \epsilon)
$$

Optimization problem

$$
argmax_{x^{*}} \mathcal{L}(f_{\theta}(x^{*}, y))

s.t. d(x, x^{*}) \leq \epsilon
$$

Iterative Optimization attach and Projected Gradient Descent are the state-of-the-art approach for the $L_{\infty}$ norm distance.




## How

## Result

## Conclusion
