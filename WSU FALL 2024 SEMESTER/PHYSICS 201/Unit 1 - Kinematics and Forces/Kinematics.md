---
tags:
- PHYSICS_201
created: 2024-08-21
---

- **Kinematics**: a mathematical description of motion

- Important qualities in kinematics are velocity, position, and acceleration, which are all vector quantities

- In one-dimensional kinematics, the direction of the vector is given by its sign
  - For example, up and right are positive, and down and left are negative

#### Position

- Displacement: change in position (delta s)

![[8.21.24 Displacement Graph]]

#### Velocity

- **Velocity**: rate of change of the position
- **Average velocity**: displacement divided by change in time (delta s/delta t)

![[8.21.24 Average Velocity Graph]]

- The slope of s vs. time is the velocity
- Uniform motion = constant velocity
  - **Average velocity**: $v = \displaystyle\frac{\Delta s}{\Delta t} = \displaystyle\frac{(s_f - s_i)}{\Delta t}$
  - $s_f = s_i + v\Delta t$
  - **Average speed**: $speed = \displaystyle\frac{d}{t}$

- **Instantaneous velocity**: velocity of a single instant of time
  - $v = \lim_{\Delta t\to 0} \displaystyle\frac{\Delta s}{\Delta t} = \frac{ds}{dt}$

> Let $s = (10 m/s^2)t^2 + (-1.0 m/s^3)t^3$
> 
> a) What is the position at t = 2.0 s?
> 
> $s = (10 m/s^2)(2.0s)^2 + (-1.0 m/s^3)(2.0s)^3$
> $s = 40m - 8m = 32m$
> 
> Answer: <u>32m</u>
> 
> 
> b) What is the instantaneous velocity at t = 2.0 s?
> 
> $v = ds/dt = (20 m/s^2)t + (-3.0 m/s^3)t^2$
> $v(2.0s) = (20 m/s^2)(2.0s) + (-3.0 m/s^3)(2.0s)^2$
> $v = 40 m/s - 12 m/s = 28 m/s$
> 
> Answer: <u>28 m/s</u>
> 
> 
> c) What is the average velocity from t = 0 s to t = 2.0 s?
> 
> $v_{avg} = \Delta s / \Delta t = (32 m - 0 m) / 2 s = 16 m/s$
> 
> Answer: <u>16 m/s</u>

#### Finding Position from Velocity

- The total displacement is:
  - $\Delta s \approx \Delta s_1 + \Delta s_2 + ... + \Delta s_n$
  - $\Delta s \approx v_1\Delta t + v_2\Delta t + ... + v_n\Delta t$
  - $\Delta s \approx \displaystyle\sum_{k=1}^{n} v_k\Delta t$
  - $s_f = s_i + \displaystyle\sum_{k=1}^{n} v_k\Delta t$
  - Let $\Delta t \rightarrow 0$, so
    - $s_f = s_i + \displaystyle\lim_{\Delta t \to 0} \displaystyle\sum_{k=1}^{n} v_k\Delta t$
    - $s_f = s_i + \displaystyle\int_{t_i}^{t_f} v \,dt$

#### Acceleration

- **Acceleration**: rate of change of velocity
- **Average acceleration**: $\displaystyle\frac{\Delta \overrightarrow{v}}{\Delta t}$

![[8.21.24 Average Acceleration Graph]]

- The slope of $\,\overrightarrow{v}$ vs. t is the acceleration
- Uniform accelerated motion = constant acceleration
  - $v_f = v_i + a\Delta t$
  - $s_f = s_i + \displaystyle\int_{t_i}^{t_f} v \,dt$
  - $s_f = s_i + v_i\Delta t + \displaystyle\frac{1}{2}a(\Delta t)^2$
  - $v_f^2 = v_i^2 + 2a\Delta s = v_i^2 + 2a(s_f - s_i)$
- Instantaneous acceleration
  - $a = \displaystyle\lim_{\Delta t\to 0} \displaystyle\frac{\Delta v}{\Delta t} = \displaystyle\frac{dv}{dt} = \displaystyle\frac{d^2s}{dt^2}$

#### Finding Velocity from Acceleration

$v_f = v_i + \displaystyle\lim_{\Delta t\to 0} \displaystyle\sum_{k=1}^{n} a_k\Delta t = v_i + \displaystyle\int_{t_i}^{t_f} a \,dt$