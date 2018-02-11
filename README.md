# CarND-Controls-PID
Self-Driving Car Engineer Nanodegree Program

---

### Overview
This project involves driving a simulated car on a track with the help of Propotional-Integral-Derivative (PID) controller. Steering values are primarily controlled in this project. Steps involved in this project:
* Calculate different errors and the total error.
* Tune Kp, Ki, and Kd values for the car to drive smoothly around the track.

### Reflection
The lessons about PID controller helped me with this project. Even though implementation was straight forward, tuning the parameters was a bit time consuming.

##### 'P' - Propotional parameter:
The propotional error means that the car will steer in propotion to the cross-track error. This would make the car steer towards the center line and overshoot to the other side of the road. The car would pretty much travel like a sinusoidal wave. If the 'P' coefficient is too high, then the oscillation will be more. If the 'P' coefficient is low, then the car will take a lot of time to steer to the center.

##### 'I' - Integral parameter:
A possible bias on the system is removed with the help of 'I' value. If there is no bias, which is the case with this simulator, it makes the car go in circles. The sum of all errors over time is defined as the Integral error. 

##### 'D' - Differential parameter:
The change in cross-track error is the Differential. This will help solve the problem of overshoot observed in Propotional parameter. The Differential parameter tries to act in the opposite way during overshoot and will help dampen the values much faster. This will also help in smoother drive.

#### Tuning the co-efficients
The initial values were set to 'p' - 1, 'i' - 0, 'd' - 0. With this car started oscillating as it drove down the track. An addition of 'd' parameter smoothened the oscilations. By decreasing 'p' and increasing 'd', the car had a smooth start and smooth turning. With addition of 'i', the car started to go in rounds at the start. The value of 'i' was decreased to observe the smooth drive of car around the track.

#### Video
Click [here](https://github.com/AbhishekGurudutt/CarND-PID-Control-Project/blob/master/pid_project.mov) 
