---
tags: PHYSICS_201
created: 2024-10-28
---

### Ideal Fluid Model

1. Fluid is incompressible
2. Fluid is non-viscous (flows easily)
3. Flow is steady
4. Flow is irrotational

> Equation of Continuity:
> ![[10.28.24 Streamlines Drawing]]
> 
> ![[10.28.24 Flow Tube Drawing]]
> 
> Since the fluid is incompressible, the amount of fluid flowing through area $A_1$ equals the amount through area $A_2$.
> 
> $$V_1 = V_2$$
> ($V$: volume)
> 
> ![[10.28.24 Volume Drawing]]
> 
> $A_1 \Delta x_1 = A_2 \Delta x_2$
> $A_1 v_1 \Delta t = A_2 v_2 \Delta t$
> $A_1 v_1 = A_2 v_2$ (equation of continuity)
> 
> Volume flow rate: $Q = Av = \frac{V}{\Delta t}$ ($v$: velocity, $V$: volume)

> [!tip] Equation of Continuity
> $A_1 v_1 = A_2 v_2$ (equation of continuity)
> 
> Volume flow rate: $Q = Av = \frac{V}{\Delta t}$ ($v$: velocity, $V$: volume)

> Bernoulli's Equation
> ![[10.28.24 Bernoulli's Principle Drawing]]
> 
> Work-Energy Theorem:
> $\Delta K + \Delta u = w_{nc}$
> 
> The work done on the fluid is
> $w_1 = \overrightarrow{F}_1 \cdot \Delta \overrightarrow{r}_1 = (\rho_1 A_1) \Delta x_1 \cos{0 \degree} = P_1V_1$
> $w_2 = \overrightarrow{F}_2 \cdot \Delta \overrightarrow{r}_2 = (\rho_2 A_2) \Delta x_2 \cos{180 \degree} = -P_2V_2$
> 
> $w_{net} = w_1 + w_2 = p_1V - p_2V$ where $V_1 = V_2 = V$ (incompressible, so volumes must be equal)
> 
> The change in kinetic energy is
> $\Delta K = \frac{1}{2}mv_2^2 - \frac{1}{2}mv_1^2 = \frac{1}{2}\rho V v_2^2 - \frac{1}{2} \rho V v_1^2$
> 
> The change in potential energy is
> $\Delta u = mgy_2 - mgy_1 = \rho V g y_2 - \rho V g y_1$
> 
> Therefore,
> $\frac{1}{2}\rho V v_2^2 - \frac{1}{2}\rho V v_1^2 + \rho V g y_2 - \rho V g y_1 = P_1 V - P_2 V$
> 
> Bernoulli's:
> $P_1 + \frac{1}{2}\rho v_1^2 + \rho g y_i = P_2 + \frac{1}{2}\rho v_2^2 + \rho g y_2 =$ constant

> [!tip] Bernoulli's Equation
> $P_1 + \frac{1}{2}\rho v_1^2 + \rho g y_i = P_2 + \frac{1}{2}\rho v_2^2 + \rho g y_2 =$ constant

### Venturi Tube

> ![[10.28.24 Venturi Tube Drawing]]
> 
> What are the velocities of the gas?
> 
> Bernoulli's Equation:
> $P_1 + \frac{1}{2}\rho_{gas}v_1^2 + \rho_{gas}gy_1 = P_2 + \frac{1}{2}\rho_{gas}v_2^2 + \rho_{gas}gy_2$ ($\rho_{gas}gy_1$ and $\rho_{gas}gy_2$ are the same term)
> 
> Equation of continuity:
> $v_1A_1 = v_2A_2$
> 
> Hydrostatic Pressure:
> $P_1 = P_2 + \rho_{liq}gh$
> 
> Hence,
> $(P_2 + \rho_{liq}gh) + \frac{1}{2}\rho_{gas}v_1^2 = P_2 + \frac{1}{2}\rho_{gas}(v_1 \frac{A_1}{A_2})^2$
> $v_1 = A_2\sqrt{\frac{2\rho_{liq}gh}{\rho_{gas}(A_1^2 - A_2^2)}}$
> $v_2 = A_1\sqrt{\frac{2\rho_{liq}gh}{\rho_{gas}(A_1^2 - A_2^2)}}$