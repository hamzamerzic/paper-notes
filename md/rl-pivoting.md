## Reinforcement Learning for Pivoting Task

### Reminders
- Found in the "Domain Randomization for Transferring Deep Neural Networks from Simulation to the Real World" paper
    - "The authors train a policy to pivot a tool held in the reobot's gripper in a simulator with randomized friction and action delays, and find that it works in the real world and is robust to errors in estimation of the system parameters"

### Overview
- Goal is to transfer knowledge from training in simulator to the real world
- Pivoting the tool belongs to the group of extrinsic dexterity problems
- Mention three problems with RL in robotics:
    - data, hyperparameters, and forgetting (e.g. in case of changing different target angles)

### Key ingredients
- Using TRPO as RL algorithm
- Modelling the friction properly
- Adding 10% friction and delay noise
- [rllab](https://github.com/openai/rllab) as the starting point

### Comments
- Interesting benefit of simulation
    - If done right, it can add more variability, and hence more robustness to the solution, that what the real life learning could do
    - The reason for this is that IRL training could potentially overfit to the task in hand
- Overall interesting subject
- The paper could be better written - missing some details, e.g. how forgetting was tackled, while some parts are overly detailed
- All in all a very good contribution
