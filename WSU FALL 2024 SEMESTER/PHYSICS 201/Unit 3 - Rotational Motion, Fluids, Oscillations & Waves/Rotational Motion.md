---
tags: PHYSICS_201
created: 2024-10-14
---

### Center of Mass

- **Center of mass/gravity**: mass-weighted center of an object
	- Unconstrained objects rotate about their center of mass.

> [!tip] Location of the Center of Mass of Individual Particles
> $$x_{cm} = \frac{1}{M}\sum_{i}m_ix_i = \frac{m_1x_1 + m_2x_2 + ...}{m_1 + m_2 + ...}$$
> 
> $$y_{cm} = \frac{1}{M}\sum_{i}m_iy_i = \frac{m_1y_1 + m_2y_2 + ...}{m_1 + m_2 + ...}$$
> 
> where $M = m_1 + m_2 + ...$ (total mass)

> [!example] Moon Example
> 
> ![[10.14.24 Earth Moon Drawing]]
> 
> Known values:
> $m_E =$ 5.98 \* 10$^{24}$ kg
> $m_M =$ 7.36 \* 10$^{22}$ kg
> $x_1 =$ 0
> $x_2 =$ 3.84 \* 10$^{8}$
> 
> $x_{cm} = \frac{(5.98 * 10^{24})(0) + (7.36 * 10^{22})(3.84 * 10^8)}{(5.98 * 10^{24}) + (7.36 * 10^{22})}$
> $\hspace{8.5mm} =$ 4.67 \* 10$^6$ m
> 
> The earth's radius is 6.37 \* 10$^6$ m.
> --> the Earth and moon orbit around a point inside the Earth.

> [!tip] Location of the Center of Mass for Extended Objects
> $$x_{cm} = \frac{1}{M}\sum x_i \Delta m \rightarrow x_{cm} = \frac{1}{M}\int x dm$$
> $$y_{cm} \frac{1}{M}\sum y_i \Delta m \rightarrow y_{cm} = \frac{1}{M} \int y dm$$

### Rotational Energy

> ![[10.14.24 Rotational Energy Drawing]]
> 
> The kinetic energy is
> $K = \frac{1}{2}m_1v_1^2 + \frac{1}{2}m_2v_2^2 + ...$
> $\hspace{5.5mm} = \frac{1}{2}m_1(r_1\omega)^2 + \frac{1}{2}m_2(r_2\omega)^2 + ...$
> $\hspace{5.5mm} = \frac{1}{2}(\sum\limits_i m_i r_i^2)\omega^2$
> 
> Define the moment of inertia
> $I = \sum\limits_i m_i r_i^2$
> 
> Therefore,
> $K = \frac{1}{2}I \omega^2$

### Moment of Inertia

> [!tip] For Particles
> $$I = \sum\limits_i m_i r_i^2$$

> [!tip] For Extended Objects
> $$I = \lim_{\Delta m \rightarrow 0} \sum\limits_i \Delta m r_i^2 = \int r^2 dm$$

> [!example] Thin Rod About Center Example
> ![[10.14.24 Thin Rod Center Drawing]]
> 
> $I = \int x^2 dm$ (where $\frac{M}{L} = \frac{dm}{dx}$)
> $\hspace{4mm} = \int_{\frac{-L}{2}}^{\frac{L}{2}} x^2 (\frac{M}{L} dx)$
> $\hspace{4mm} = \frac{M}{L}(\frac{x^3}{3}\Big|_{\frac{-L}{2}}^{\frac{L}{2}})$
> $\hspace{4mm} = \frac{M}{L}[\frac{L^3}{3 * 8} - \frac{-L^3}{3 * 8}]$
> $\hspace{4mm} = \frac{1}{12}mL^2$

### Parallel-Axis Theorem

> ![[10.14.24 Parallel Axis Theorem Drawing]]
> 
> $I = \int x^2 dm$
> $\hspace{4mm} = \int (x' + d)^2 dm$
> $\hspace{4mm} = \int (x')^2dm + 2d\int x dm + d^2\int dm$
> $\hspace{4mm} = I_{cm} + 2d(Mx_{cm}) + d^2M$ ($2d(Mx_{cm})$ = 0 since $x_{cm}$ = 0)
> 
> Therefore,
> $I = I_{cm} + Md^2$

> [!example] Thin Rod About End Example
> ![[10.14.24 Thin Rod End Drawing]]
> 
> $I = I_{cm} + Md^2$
> $\hspace{4mm} = \frac{1}{12}ML^2 + M(\frac{L}{2})^2$
> $\hspace{4mm} = \frac{1}{3}ML^2$

### Torque

- **Torque**: rotational equivalent of force, i.e. causes change to rotation
	- SI unit: newton-meter (N-m)

![[10.14.24 Torque Drawing]]

> [!tip] Torque
> $$\tau = rF\sin\varphi$$

> [!info] Important
> Forces directed at the pivot cause no torque (because the angle is 0).

##### Two interpretations of torque

1. ![[10.14.24 Torque Interpretation 1]]
2. ![[10.14.24 Torque Interpretation 2]]

##### Two or more torques

![[10.14.24 Two Torques Drawing]]

Total torque: $T = T_1 + T_2 = -r_1F_1 + r_2F_2$
