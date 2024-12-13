---
tags: PHYSICS_201
created: 2024-09-25
---

> [!example]
> ![[9.25.24 Rocket Cliff Drawing]]
> 
> Known values:
> $F_{thrust} =$ 2.0 N
> $m =$ 1.0 kg
> 
> How far does the rocket land from the base of the cliff?
> 
> First, find the horizontal velocity at the cliff's edge.
> $a_x = \frac{F_{thrust}}{m} = \frac{2.0}{1.0} =$ 2.0 m/s$^2$
> $v_{fx}^2 = v_{ix}^2 + 2a_x\Delta x$ ($v_{ix}$ = 0 since it starts from rest)
> $v_{fx} = \sqrt{2a_x\Delta x} = \sqrt{2(2.0)(4.0)} =$ 4.0 m/s
> 
> Then, find the time it takes the rocket to land.
> $y_f = y_i + v_{iy}\Delta t + \frac{1}{2}a_y(\Delta t)^2$ ($v_{iy}$ = 0 since it starts from rest)
> $\Delta t = \sqrt{\frac{-2y_i}{a_y}} = \sqrt{\frac{-2(2.0)}{-9.8}} =$ 0.64 s
> 
> Finally, find the distance away from the cliff it lands.
> $x_f = x_i + v_{ix}\Delta t + \frac{1}{2}a_x(\Delta t)^2$
> $\hspace{6mm} = (4.0)(0.64) + \frac{1}{2}(2.0)(0.64)^2 =$ 3.0 m

> [!example]
> ![[9.25.24 Rocket Drawing]]
> 
> Known values:
> $F_{thrust} =$ 140,700 N
> $m =$ 5000 kg
> 
> At what elevation does the rocket reach the speed of sound, 330 m/s?
> 
> Free-body diagram:
> ![[9.25.24 Rocket FBD]]
> 
> Newton's Second Law:
> <u>x-component</u>
> $F_{thrust, x} = ma_x$
> $F_{thrust}\cos\theta = ma_x$
> $a_x = \frac{F_{thrust}\cos\theta}{m} = \frac{(140700)\cos{44.7\degree}}{5000} =$ 20.0 m/s$^2$
> 
> <u>y-component</u>
> $F_{thrust, y} - w = ma_y$
> $F_{thrust}\sin\theta - mg = ma_y$
> $a_y = \frac{F_{thrust}\sin\theta - mg}{m} = \frac{(140700)\sin{44.7\degree} - (5000)(9.8)}{5000} =$ 10.0 m/s$^2$
> 
> The speed of the rocket is...
> $v = \sqrt{v_x^2 + v_y^2}$ where $v_{fx} = v_{ix} + a_x\Delta t$ and $v_{fy} = v_{iy} + a_y \Delta t$
> (the rocket starts from rest, so initial velocity is 0)
> $v = \Delta t \sqrt{a_x^2 + a_y^2}$
> 
> The time to reach the speed of sound is...
> $\Delta t = \frac{V}{\sqrt{a_x^2 + a_y^2}} = \frac{330}{\sqrt{(20.0)^2 + (10.0)^2}} =$ 14.8 s
> 
> The elevation is...
> $y_f = y_i + v_{iy} \Delta t + \frac{1}{2} a_y (\Delta t)^2$ (assume initial velocity is 0 and it started from the ground)
> $y_f = \frac{1}{2}(10.0)(14.8)^2 =$ 1095 m

### Dynamics of Circular Motion

##### rtz-coordinates

![[9.25.24 Circular Motion Drawing]]

> [!example]
> A concrete highway with a curve of radius 70 m is banked at a 15 degree angle. What is the maximum speed with which a 1500 kg rubber-tired car can take the corner without sliding?
> 
> ![[9.25.24 Car Drawing]]
> 
> Free-body diagram:
> ![[9.25.24 Car FBD]]
> 
> Newton's Second Law:
> <u>r-component</u>
> $f_{s,r} - n_r = ma_r$
> $\mu _s n \cos\theta - n\sin\theta = m\frac{v^2}{r}$
> $\frac{mg(\mu _s \cos\theta - \sin\theta)}{\cos\theta - \mu _s \sin\theta} = m\frac{v^2}{r}$
> $v = \sqrt{\frac{rg(\mu _s \cos\theta - \sin\theta)}{\cos\theta - \mu _s \sin\theta}} =$ 34.5 m/s
> 
> <u>z-component</u>
> $n_z = f_{s, z} - w = ma_z$
> $n\cos\theta \mu _s n \sin\theta - mg = 0$
> $n = \frac{mg}{\cos\theta - \mu _s \sin\theta}$ (use in r-component part))

### Circular Orbits

![[9.25.24 Projectile Drawing]]

> Orbiting object
> 
> Free-body diagram:
> ![[9.25.24 Orbiting Object FBD]]
> 
> Newton's Second Law:
> $w = ma_r$
> $mg = m\frac{v^2}{r}$
> $v = \sqrt{rg}$ (velocity needed to maintain orbit)
> $\hspace{3mm} =$ 7,900 m/s = 18,000 mph at the earth's surface

> [!tip] Velocity to Maintain Orbit Formula
> $v = \sqrt{rg}$

> [!example]
> ![[9.25.24 Space Station Drawing]]
> 
> Known values:
> $T =$ 90 min
> $h =$ 290 km above the Earth's surface
> 
> What is the acceleration due to gravity at the space station's orbit?
> 
> $v = \sqrt{rg} = \frac{2\pi r}{T}$
> $g = \frac{4(\pi)^2 r}{T^2} = \frac{4 \pi ^2 (6.37*10^6 + 2.90 * 10^3)}{((90)(60))^2} =$ 9.02 m/s$^2$ (radius includes both radius of the earth and the height off the earth's surface)