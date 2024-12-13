---
tags: PHYSICS_201
created: 2024-10-16
---

> ![[10.16.24 Rotational Dynamics Drawing]]
> 
> Free-body diagram:
> ![[10.16.24 Rotational Dynamics FBD]]
> 
> Newton's Second Law:
> <u>r-comp</u>
> $T - F_r = ma_r$
> $T - F\cos\varphi = m\frac{v^2}{r}$
> 
> <u>t-comp</u>
> $F_t = ma_t$
> $F_t = mr\alpha$
> $rF_t = mr^2\alpha$ ($\tau = rF_t$)
> $\tau = mr^2\alpha$
> 
> Torque causes angular acceleration.

> ![[10.16.24 Rotational Dynamics Complex]]
> 
> Newton's Second Law (t-component):
> $\tau_{net} = \sum\limits_i (m_ir_i^2\alpha) = \sum\limits_i (m_ir_i^2)\alpha$
> $\hspace{8.5mm} = I\alpha$ ($I$: moment of inertia)

### Pulleys with Mass

> ![[10.16.24 Pulley with Mass Drawing]]
> 
> $$v_{rim} = v_{obj} \rightarrow v_{obj} = \left|\omega\right|R$$
> $$a_{rim} = a_{obj} \rightarrow a_{obj} = \left|\alpha\right|R$$

> [!example]
> ![[10.16.24 Pulley Two Blocks Drawing]]
> 
> Known values:
> $m_1 =$ 1.0 kg
> $m_2 =$ 2.0 kg
> $m_p =$ 0.5 kg (dish-shaped)
> $R =$ 0.10 m
> 
> Unknown values:
> $a_{1y} =$ ?
> $T_1 =$ ?
> $T_2 =$ ?
> 
> Acceleration constraint:
> $-a_{1y} = a_{2x} = -\alpha R$
> 
> Free-body diagrams:
> ![[10.16.24 Pulley Two Blocks FBD]]
> 
> Newton's Second Law:
> **Block 1** -
> $T_1 - w_1 = m_1a_{1y}$
> 
> **Block 2** -
> <u>x-component</u>
> $T_2 = m_2a_{2x}$
> 
> <u>y-component</u>
> $n_2 - w_2 = m_2a_{2y}$ ($a_{2y}$ = 0 since there is no motion in the y-direction)
> 
> **Pulley** -
> <u>Torques</u>
> $\sum\limits \tau = I\alpha$
> $RT_2 - RT_1 = I\alpha$
> $R(T_2 - T_1) = I\alpha$
> $R(m_2a_{2x} - (m_1a_{1y} + m_1g)) =$ ($\frac{1}{2}m_pR^2)\alpha$ ($I = \frac{1}{2} m_p R^2$ is the moment of inertia of a disk)
> $R(m_2(-a_{1y}) - m_1a_{1y} - m_1g) = (\frac{1}{2} m_p R^2)(\frac{a_{1y}}{R})$ (using acceleration constraints)
> $a_{1y} = \frac{-m_1g}{\frac{1}{2}m_p + m_1 + m_2}$
> $\hspace{8mm} = \frac{-(1.0)(9.8)}{\frac{1}{2}(0.5) + 1.0 + 2.0}$
> $\hspace{8mm} =$ -3.02 m/s$^2$
> 
> $T_1 = m_1(a_{1y} + g) = (1.0)(-3.02 + 9.8) =$ 6.78 N
> $T_2 = m_2a_{2x} = (2.0)(3.02) =$ 6.04 N

> [!example]
> ![[10.16.24 Ladder Drawing]]
> 
> Known values:
> $\mu_{s, w} =$ 0
> $\mu_{s, g} =$ 0.40
> $L =$ 3.0 m
> 
> What is the minimum angle the ladder can make with the floor without slipping?
> 
> Newton's Second Law:
> <u>x-component</u>
> $n_1 - f_s = ma_x$ ($a_x$ = 0 because we don't want the ladder to move)
> $n_1 = \mu_s n_2$
> 
> <u>y-component</u>
> $n_2 - w = ma_y$ ($a_y$ = 0 because we don't want the ladder to move)
> $n_2 = mg$
> 
> <u>Torques</u>
> $\sum\limits\tau = I\alpha$ ($\alpha$ = 0 because we don't want the ladder to move)
> $-n_1L\sin\theta + w\frac{L}{2}\sin({90\degree - \theta}) = 0$ (comes from $T = rF\sin\theta$)
> $-n_1L\sin\theta + w\frac{L}{2}\cos\theta = 0$
> $\mu_s mgL\sin\theta + mg\frac{L}{2}\cos\theta = 0$
> $\mu_s \sin\theta + \frac{1}{2}\cos\theta = 0$ ($\tan\theta = \frac{1}{2\mu_s}$, got this by moving the terms around and dividing)
> $\theta = \tan^{-1}\left(\frac{1}{2(0.40)}\right) =$ 51.3$\degree$