## Deterministic Policy Gradient Algorithms

### Reminders
- Stochastic policy, usually denoted as $\pi(s,a)$ or $\mu(a|s)$, gives us the joint distribution of actions and policies, while the deterministic policy $\mu(s)$ gives us the actual action
- Stochastic policy natural for explorations

### Overview
- Deterministic policy gradient is the expected gradient of the action-value function
- Shows the existence of the deterministic policy gradient
- Stochastic policy gradient integrates over both actions and states $\implies$ needs more samples to estimate
-- Necessary to explare full state and action space (unless environment super noisy)
- *compatible* function approximation ensures unbiasedness of the gradient


### Key ingredients

### Comments

#### Off topic
Can we make any process MDP? Use the whole previous history to represent the state?