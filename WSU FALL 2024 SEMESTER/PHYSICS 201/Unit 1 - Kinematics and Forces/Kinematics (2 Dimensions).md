---
tags: PHYSICS_201
created: 2024-08-28
---

### Important Quantities

##### Position

$\overrightarrow{r} = x\hat{i} + y\hat{j}$

##### Velocity

$\displaystyle\overrightarrow{v}_{avg} = \frac{\Delta\overrightarrow{v}}{\Delta t} = \frac{\Delta x}{\Delta t}\hat{i} + \frac{\Delta y}{\Delta t}\hat{j}$

$\displaystyle\overrightarrow{v} = \lim_{\Delta t \to 0} \frac{\Delta\overrightarrow{v}}{\Delta t} = \frac{d\overrightarrow{v}}{dt} = \frac{dx}{dt}\hat{i} + \frac{dy}{dt}\hat{j} = v_x\hat{i} + v_y\hat{j}$

$v = \sqrt{v_x^2 + v_y^2}$

![[8.28.24 Velocity Graph]]
$v_x = v\cos\theta$
$v_y = v\sin\theta$
$\theta = tan^{-1}({\frac{v_y}{v_x}})$

##### Acceleration

$\displaystyle\overrightarrow{a}_{avg} = \frac{\Delta\overrightarrow{v}}{\Delta t} = \frac{\Delta v_x}{\Delta t}\hat{i} + \frac{\Delta v_y}{\Delta t}\hat{j}$

$\displaystyle\overrightarrow{a} = \lim_{\Delta t \to 0} \frac{\Delta\overrightarrow{v}}{\Delta t} = \frac{d\overrightarrow{v}}{dt} = \frac{dv_x}{dt}\hat{i} + \frac{dv_y}{dt}\hat{j} = a_x\hat{i} + a_y\hat{j}$

### Kinematic Equations (for constant acceleration)

> [!tip] Horizontal Motion
> 
> $x_f = x_i + v_{ix}\Delta t + \frac{1}{2}a_x(\Delta t)^2$
> $v_{fx} = v_{ix} + a_x\Delta t$
> $v_{fx}^2 = v_{ix}^2 + 2a_x\Delta x$

> [!tip] Vertical Motion
> 
> $y_f = y_i + v_{iy}\Delta t + \frac{1}{2}a_y(\Delta t)^2$
> $v_{fy} = v_{iy} + a_y\Delta t$
> $v_{fy}^2 = v_{iy}^2 + 2a_y\Delta y$


>[!info] 
> Vertical motion and horizontal motion are independent of each other.

### Projectile Motion

- Motion of an object in 2D with only gravitational forces acting on it

>[!info] 
> Almost all of the time, $a_x = 0$ and $a_y = -g$

- Projectiles follow a parabolic trajectory

$x_f = x_i + v_{ix}\Delta t + \frac{1}{2}a_x(\Delta t)^2$
$\Delta t = \frac{x_f - x_i}{v_{ix}} = \frac{\Delta x}{v_{ix}}$
$y_f = y_i + v_{iy}\Delta t + \frac{1}{2}a_y(\Delta t)^2$
$y_f - y_i = v_{iy}\left(\frac{\Delta x}{v_{ix}}\right) + \frac{1}{2}(-g)\left(\frac{\Delta x}{v_{ix}}\right)$
$\Delta y=b \Delta x + c(\Delta x)^2$ (equation of a parabola)

> A scientist is trying to tranquilize a monkey sitting on a tree. The monkey drops at the same time as the trigger is pulled. Does the dart hit the monkey?
> 
> ![[8.28.24 Monkey Tree Drawing]]
> 
> Yes, because both the monkey and the dart drop with the same acceleration (-g).

> How far does a projectile travel to the same elevation?
> 
> ![[8.28.24 Projectile Drawing]]
> 
> $y_f = y_i + v_{iy}\Delta t + \frac{1}{2}a_y(\Delta t)^2$ ($y_f$ = $y_i$)
> $0 = (v_i\sin\theta)\Delta t + \frac{1}{2}(-g)(\Delta t)^2$
> $\Delta t = \frac{2v_i\sin\theta}{g}$
> 
> $x_f = x_i + v_{ix}\Delta t + \frac{1}{2}a_y(\Delta t)$ ($x_i$ = 0 and $a_x$ = 0)
> $x_f = (v_i\cos\theta)(\frac{2v_i\sin\theta}{g})$
> $\hspace{6 mm} = \frac{v_i^2}{g}(2\cos\theta\sin\theta)$
> $\hspace{6 mm} = \frac{v_i^2}{g}(\sin{2\theta})$
> 
> Max distance at $\theta = 45\degree$

> The plane flies 100m above the ground at $\theta = 30\degree$ and at a speed of 150 m/s. How far short of the target should the plane drop the package?
> 
> ![[8.28.24 Plane Drawing]]
> 
> The time it takes for the package to drop is given by:
> $y_f = y_i + v_{iy}\Delta t + \frac{1}{2}a_y(\Delta t)^2$ ($y_f$ = 0)
> $0 = (100) + (150\sin\theta)\Delta t + \frac{1}{2}(-9.80)(\Delta t)^2$
> Quadratic Formula: $\Delta t = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$
> $\Delta t$ = -1.23s or <u>16.5s</u>
> 
> The horizontal distance traveled is:
> $x_f = x_i + v_{ix}\Delta t + \frac{1}{2}a_x(\Delta t)^2$ ($a_x$ = 0 and $x_i$ = 0)
> $\hspace{6 mm} = (150\cos{30\degree})(16.5) = 2140$ m