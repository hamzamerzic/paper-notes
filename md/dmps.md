## Dynamic Movement Primitives

- are a method for trajectory planning
- define a way to adjust complex inputs *without* **manual parameter tuning** and **instability issues**.
- each DMP is a nonlinear dynamical system

### Key ingredients

 - Take a stable, well defined dynamical system and add a term that makes it follow a specific trajectory. 

#### Discrete DMPs
The stable dynamical system in this case is the **point attractor** system:

$$\ddot{y}= \alpha_y(\beta_y (y_{des} - y) - \dot{y}).$$

We add to this the nonlinear **forcing function** $f$ to obtain:

$$\ddot{y}= \alpha_y(\beta_y (y_{des}  - y) - \dot{y}) + f,$$

where $f = \frac{\sum_{i=1}^N{w_i\psi_i}}{\sum_{i=1}^N{\psi_i}}x(y_{des} - y_0),$ for $\psi_i=\exp{(-h_i(x-c_i)^2)}$, which acts as a Gaussian -- $h_i$ defines the variance, $c_i$ the mean. 

- $x$ is the *canonical dynamical system* $\dot{x} = -\alpha_x x$, which acts as a diminishing term driving $f$ to zero, and leaving only the point attractor dynamics.

- Spatial and temporal scaling allows stretching or compressing of  the trajectory in spatial ($y$) and temporal ($t$) domain. 

### Comments
- How to choose means (centers) and the variances of basis functions $\psi_i$? 

There two common ways of choosing the centers of basis functions; by spreading them uniformly on the time axis, or by distributing them according to the complexity of the desired trajectory - more functions around more difficult areas. 

The variance parameter can be chosen according to $h_i = \frac{\#basis\_functions}{c_i}$.

- Examples of DMPs in action?

*Imitating desired paths*. We can choose $f$ such that our trajectory imitates $y_d$. By double differentiation of $y_d$, and some additional manipulation, we can get a supervised version of the problem of estimating the parameters. For that, a simple solution exists.

Other examples, could be found in reinforcement learning, e.g. *Path Integral Policy Improvement*, since we can use DMP to efficiently parametrize and learn policies.