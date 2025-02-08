---
tags: PHYSICS_202
created: 2025-1-15
---

> [!info] Electric Field for an Infinite Plate
> $\vec{E} = \frac{\eta}{2\epsilon_0} \vec{K}$ for above the plate
> 
> where $\eta = \frac{Q}{A}$ (surface charge density)

> Ideal Capacitor:
> ![[1.15.25 Ideal Capacitor Drawing]]
> 
> $\vec{E} = \vec{E}_+ + \vec{E}_-$
> $\hspace{4.5mm} = \frac{\eta}{2\epsilon_0} \hat{k} + \frac{\eta}{2\epsilon_0} \hat{k}$
> $\hspace{4.5mm} = \frac{\eta}{\epsilon_0} \hat{k}$ in between the plates
> 
> $\vec{E} = 0$ outside the plates

> [!example]
> ![[1.15.25 Electric Field Example]]
> 
> What is the electric field at points 1, 2, and 3?
> 
> Point 1:
> $\vec{E} = \vec{E}_1 + \vec{E}_2 = \frac{\eta_0}{2\epsilon_0}\hat{k} + \frac{3\eta_0}{2\epsilon_0} (-\hat{k}) = \frac{-\eta_0}{\epsilon_0}\hat{k}$
> 
> Point 2:
> $\vec{E} = \vec{E}_1 + \vec{E}_2 = \frac{\eta_0}{2\epsilon_0} (-\hat{k}) + \frac{3\eta_0}{2\epsilon_0} (-\hat{k}) = \frac{-2\eta_0}{\epsilon} \hat{k}$
> 
> Point 3:
> $\vec{E} = \vec{E}_1 + \vec{E}_2 = \frac{\eta_0}{2\epsilon_0} (-\hat{k}) + \frac{3\eta_0}{2\epsilon_0} \hat{k} = \frac{\eta_0}{\epsilon} \hat{k}$

### Motion of Charged Particles in Electric Fields

> [!example]
> ![[1.15.25 Motion Drawing]]
> 
> How far has the proton been deflected sideways when it reaches the end of the capacitor?
> 
> The time of flight is:
> $x_f = x_i + v_{ix}\Delta t + \frac{1}{2}a_x(\Delta t)^2$ <---- $x_i$ = 0 and $a_x$ = 0
> $\Delta t = \frac{x_f}{v_{ix}} = \frac{0.02}{1 \times 10^6} =$ 2.0 x 10$^{-8}$ s
> 
> The acceleration is:
> $F = ma_y$
> $qE = ma_y$
> $\frac{q\eta}{\epsilon} = ma_y$
> $a_y = \frac{q\eta}{m\epsilon} = \frac{(1.6 \times 10^{-19}) (1.0 \times 10^{-6})}{(1.67 \times 10^{-27}) (8.85 \times 10^{-12})} =$ 1.08 x 10$^{13}$ m/s$^2$ <---- $q$ and $m$ values are the values for a proton
> 
> The amount deflected is:
> $y_f = y_i + v_{iy}\Delta t + \frac{1}{2}a_y(\Delta t)^2$ <--- $y_i$ = 0 and $v_{iy}$ = 0
> $\hspace{6mm} = \frac{1}{2}(1.08 \times 10^{13}) (2.0 \times 10^{-8})^2$
> $\hspace{6mm} =$ 0.0022 m = 2.2 mm

### Motion of Dipole in Electric Fields

For uniform fields:
![[1.15.25 Uniform Fields Drawing]]

$\vec{F}_{net} = \vec{E}_+ + \vec{E}_- = q\vec{E} + (-q\vec{E}) = 0$
- No net force
- No translation of dipole

![[1.15.25 Net Force Drawing]]

$\tau_{net} = lF = (s\sin\theta)(qE) = pE\sin\theta$
where $p = qs$ (dipole moment)

> [!info]
> - There is a net torque if $\theta \neq 90\degree \text{or} 0\degree$
> - The dipole rotates