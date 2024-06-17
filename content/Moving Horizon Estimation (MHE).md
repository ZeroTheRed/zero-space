>[!Definition]
>The *optimization* approach that uses a series of measurements that span over time to estimate unknown variables of a *dynamical system*[^1]

MHE is *non-deterministic* -> Requires *iteration* that relies on *linear* or *nonlinear programming* solvers. You can't obtain a definite solution by following a definite and algorithmic path

# Advantages
1. **MHE outperforms most traditional state-estimation methods (such as EKF)** - This is gold in nonlinear dynamical systems because they are rigorously treated with MHE but EKF works reliably only on systems that are almost *linear*[^2]
2. **Additional constraints can be added** - This allows us to place *bounds* on estimated variables

# Limitations
1. **Increased computational complexity** - Systems that have good compute power can benefit immensely from MHE but otherwise, not so much but there are MHE packages that attempt to mitigate this issue

>[!Note]
>Under certain conditions, MHE reduces to the [[Kalman Filters|Kalman filter]]

![[Pasted image 20240523155237.png]]
*J* - Optimization function
$w_y$ - Weight representing the relative importance of measured variable $y_i$
$w_\hat{x}$ - Weight representing the relative importance of predicted variable $\hat{x}_i$
$w_{p_i}$ - Weight penalizing big changes in parameter $p_i$


[^1]: https://en.wikipedia.org/wiki/Moving_horizon_estimation
[^2]: https://www.do-mpc.com/en/latest/theory_mhe.html