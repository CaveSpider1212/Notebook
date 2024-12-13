---
tags: PHYSICS_201
created: 2024-10-7
---

### Potential Energy

> Consider a falling object.
> 
> ![[10.7.24 Falling Object Drawing]]
> 
> Newton's Second Law:
> $F = ma = m\frac{dv}{dt}$
> $-mg = m\frac{dv}{dy}\frac{dy}{dt}$
> $-mg = mv\frac{dv}{dy}$
> $-mg dy = mv dv$
> $-\int_{y_i}^{y_f}mg dy = \int_{v_i}^{v_f} mvdv$
> $-mgy_f + mgy_i = \frac{1}{2}m v_f^2 - \frac{1}{2}m v_i^2$
> $\frac{1}{2}m v_f^2 + mg y_f = \frac{1}{2}m v_i^2 + mg y_i$
> 
> Conservation of Energy:
> 
> Kinetic energy - $K = \frac{1}{2}mv^2$
> Gravitational potential energy: $u = mgy$

> [!info] Energy
> 
> **Kinetic energy**: energy due to motion
> 
> $$K = \frac{1}{2}mv^2$$
> 
> **Potential energy**: energy due to position
> $$u = mgy$$
> 
> Energy (combine both, may need to split into initial and final parts):
> $$E = \frac{1}{2}mv^2 + mgy$$
> 
> Add kinetic energy if there is motion involved, and add potential energy if there is height involved.

^7ee0d5

### Zero of Potential Energy

> ![[10.7.24 Betty Bill Diagram]]
> 
> Betty:
> $\frac{1}{2}mv_f^2 + mgy_f = \frac{1}{2}mv_i^2 + mgy_i$ (plug in known values)
> $\frac{1}{2}mv_f^2 = mgy_f$
> $v_f = \sqrt{2gy_f}$
> $\hspace{5.5mm} = \sqrt{2(9.8)(1.0)}$
> $\hspace{5.5mm} =$ 4.43 m/s
> 
> Bill:
> $\frac{1}{2}mv_f^2 + mgy_f = \frac{1}{2}mv_i^2 + mgy_i$ (plug in known values)
> $\frac{1}{2}mv_f^2 = mgy_f = 0$
> $v_f = \sqrt{-2gy_i}$
> $\hspace{5.5mm} = \sqrt{-2(9.8)(-1.0)}$
> $\hspace{5.5mm} =$ 4.43 m/s
> 
> Absolute energies do not matter, only the change.
> $\frac{1}{2}mv_f^2 + mgy_f = \frac{1}{2}mv_i^2 + mgy_i$
> $\frac{1}{2}mv_f^2 - \frac{1}{2}mv_i^2 = -mgy_f + mgy_i$
> $\Delta K = -\Delta K$

> [!example]
> A ball is tossed straight up at 10 m/s from a height of 20 m.
> 
> ![[10.7.24 Ball Drop]]
> 
> What is the ball's impact speed?
> 
> Conservation of Energy:
> $E_f = E_i$
> $\frac{1}{s}mv_f^2 + mgy_f = \frac{1}{2}mv_i^2 + mgy_i$  ($y_f$ = 0 since it hits the ground)
> $v_f = \sqrt{v_i^2 + 2gy_i}$ (this is the same as one of the kinematic equations)
> $\hspace{5.5mm} = \sqrt{(10)^2 + 2(9.8)(20)}$
> $\hspace{5.5mm} =$ 22.2 m/s

> [!example]
> What speed does a 100 g hockey puck need to it to the top of a 3.0 m long, 20$\degree$ frictionless ramp?
> 
> ![[10.7.24 Puck]]
> 
> Conservation of Energy:
> $E_f = E_i$
> $\frac{1}{2}mv_f^2 + mgy_f = \frac{1}{2}mv_i^2 + mgy_i$ ($v_f$ = 0 since the puck is supposed to stop at the top before coming down again)
> $v_i = \sqrt{2gy_f}$ ($y_f = l\sin\theta$ using trig)
> $\hspace{5mm} = \sqrt{2(9.8)(3.0)\sin{20\degree}}$
> $\hspace{5mm} =$ 4.48 m/s

> [!example]
> A 20 kg child is on a swing that hangs on 3.0 m long chains. What is her maximum speed if she swings out to a 45$\degree$ angle?
> 
> ![[10.7.24 Swing]]
> 
> Conservation of Energy:
> $E_f = E_i$
> $\frac{1}{2}mv_f^2 + mgy_f = \frac{1}{2}mv_i^2 + mgy_i$ ($v_i$ = 0 since it starts from rest)
> $v_f = \sqrt{2gy_i}$
> 
> ![[10.7.24 Swing Length]]
> 
> $v_f = \sqrt{2(9.8)(3.0)(1 - \cos{45\degree})}$
> $\hspace{5.5mm} =$ 4.15 m/s