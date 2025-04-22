---
tags: PHYSICS_202
created: 2025-4-21
---

### Galilean Transformation

![[4.21.25 Reference Frames.png]]

Since $x = x' + vt$, then the position transform as
$x' = x - vt$
$v' = y$
$z' = z$

Let $u_x = \frac{dx}{dt}$, then the velocities transform as
$u_x' = u_x - v$
$u_y' = y$
$u_z' = z$

The accelerations are independent of the reference frame.

### Postulates of Special Relativity

> [!tip] Postulates of Special Relativity
> 1. The laws of physics are invariant under inertial transformations.
> 2. The speed of light is independent of the motion of the source.

### Simultaneity

> [!info] Simultaneity
> Two events that are simultaneous in one inertial system are not in general simultaneous in another.

For example, in a moving car with a light
- The light hits both ends at the same time in the rest frame
- The light hits both ends at different times in the moving frame

### Time Dilation

> [!info] Time Dilation
> Moving clocks run slower.

For example, in a moving car with a ball??
- The time to hit the floor is $\Delta t' = \frac{h}{c}$ in the rest frame
- The time to hit the floor is $\Delta t = \frac{h}{c} \frac{1}{\sqrt{1 - \frac{v^2}{c^2}}}$ in the moving frame

> [!tip] Time Dilation
> $\Delta t = \frac{\Delta t'}{\sqrt{1 - \frac{v^2}{c^2}}} = \frac{\Delta \tau}{\sqrt{1 - \beta^2}}$
> 
> where $\Delta \tau$ is the proper time (time interval between two events that occur at the same position) and $\beta = \frac{v}{c}$

### Length Contraction

> [!info] Length Contraction
> Moving objects are shortened

For example, in a train car if something were to move from the back to the front
- The time for a round trip is $\Delta t' = 2 \frac{\Delta x'}{c}$ in the rest frame
- In the moving frame
	- The time to hit front is $\Delta t_1 = \frac{\Delta x + v \Delta t_1}{c}$
	- The time to hit back is $\Delta t_2 = \frac{\Delta x - v \Delta t_2}{c} \rightarrow \Delta t_1 = \frac{\Delta x}{c - v}, \Delta t_2 = \frac{\Delta x}{c + v}$
	- The round trip time is $\Delta t = \Delta t_1 + \Delta t_2 = 2 \frac{\Delta x}{c} \frac{1}{1 - \frac{v^2}{c^2}}$

Thus, $\Delta x' = \frac{c}{2} \Delta t' = \frac{c}{2} \sqrt{1 - \frac{v^2}{c^2}} \Delta t = \frac{\Delta x}{\sqrt{1 - \frac{v^2}{c^2}}}$

> [!tip] Length Contraction
> $$L = l \sqrt{1 - \beta^2}$$
> 
> where $l$ is the proper length (measured in the rest frame)

### Lorentz Transformation

> [!tip] Lorentz Transformation Formulas
> $$x' = \gamma (x - vt) \hspace{30mm} x = \gamma(x' + vt')$$
> $$y = y \hspace{30mm} y = y'$$
> $$z' = z \hspace{30mm} z = z'$$
> $$t' = \gamma \left(t - \frac{vx}{c^2}\right) \hspace{30mm} t = \gamma \left(t' + \frac{vx'}{c^2}\right)$$
> $$u' = \frac{u - v}{1 - \frac{uv}{c^2}} \hspace{30mm} u = \frac{u' + v}{1 + \frac{u' v}{c^2}}$$
> 
> where $\gamma = \frac{1}{\sqrt{1 - \frac{v^2}{c^2}}}$

> [!tip] Spacetime Interval
> $$S^2 = c^2 (\Delta t)^2 - (\Delta x)^2$$
> 
> --> invariant in all inertial frames

> [!info] Binomial Approximation
> If $x \ll 1$, then $(1 + x)^n = 1 + nx$.

> [!example]
> There is a spaceship moving at 0.8 times the speed of light relative to the Earth and a projectile moving 0.9 times the speed of light relative to the spaceship. What is the projectile's speed relative of the Earth?
> 
> $u' = \frac{u - v}{1 - \frac{uv}{c^2}}$ <--- where $v$ = 0.8$c$ and $u'$ = 0.9$c$
> $u = \frac{u' + v}{1 + \frac{u' v}{c^2}}$
> $\hspace{4mm} = \frac{0.9 + 0.8}{1 + \frac{(0.9)(0.8)}{c^2}}$
> $\hspace{4mm} =$ 0.988$c$