# 6.036 Week10

## Bandit problems

exploit vs explore

## Sequential problems

Reinforcement learning is going to mix together three problems. It's going to mix together normal machine learning kind of problems, like how do I find a hypothesis that fits my data. It's going to mix in Markov decision process value iteration type solution of things. And it's going to mix in this exploration versus exploitation problem.

measure the quality of an RL algorithm:

* Ignoring the rt values that it gets while learning, but consider how many interactions with the environment are required for it to learn a policy π : S → A that is nearly optimal.
* Maximizing the expected discounted sum of total rewards while it is learning

Approaches to reinforcement-learning：

* Model-based
* Policy search
* Value function learning
