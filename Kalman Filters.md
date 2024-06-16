https://github.com/rlabbe/Kalman-and-Bayesian-Filters-in-Python

Data is noisy, sensors may be inaccurate
Combine knowledge of the past and that of the system to reliably make data estimates
Never throw away inaccurate data

Real sensors are more likely to provide measurements that are closer to the true value 

Blend of prediction and measurement

Measurement - Prediction = Residual

### g-h filter or $\alpha-\beta$ filter
g - scaling for the measurement 
* Smaller g -- closer to predictions
* Larger g -- closer to measurements 
* g greater than 1 -- overshoot from measurement

h - scaling for the rate 
_h is the factor that decides the reactivity of the filter to changes in the data. If h is small, the filter will react more slowly to changes in data, while a high h would imply faster responses. High h may also cause a increase in frequency of the ringing before reaching the steady state_

* Make prediction based on what we know
`prediction = previous_estimate + rate * time_step`
* Update estimate and rate
`updated_estimate = prediction + g * (measurement - prediction)`
`updated_rate = rate + h * (measurement - prediction)/time_step`
* Repeat

Terminology
* *System* - What we want to estimate
* _State_ - The actual configuration of the system or the actual value 
* _Estimate_ - The filter's estimate of the state
* _Measurement_ - A measured value of the state
* _Process model_ - How we think the state will change
* _System propagation_ - The prediction step
* _Measurement update_ - The update step

Kalman filters dynamically vary g and h
**Problem of g-h filter** - Systemic error (only as good as mathematical model. For example, if we introduction an acceleration factor while creating the data, the prediction falls behind the measurements and h is not enough to compensate for it here - a fundamental shortcoming of g-h filters)
