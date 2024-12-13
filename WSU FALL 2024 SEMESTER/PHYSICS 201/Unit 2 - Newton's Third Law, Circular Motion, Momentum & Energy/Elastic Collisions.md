---
tags: PHYSICS_201
created: 2024-10-11
---

- **Elastic collisions**: Conserve both [[Momentum]] and energy
	- **Inelastic collisions**: only conserve [[Momentum]]

> Consider two objects and let object 2 be at rest, then
> 
> Conservation of momentum:
> $m_1v_{1f} + m_2v_{2f} = m_1v_{1i} + m_2v_{2i}$ ($v_{2i}$ = 0 since the object starts at rest)
> 
> Conservation of energy:
> $\frac{1}{2}m_1v_{1f}^2 + \frac{1}{2}m_2v_{2f}^2 = \frac{1}{2}m_1v_{1i}^2 + \frac{1}{2}m_2v_{2i}^2$ ($v_{2i}$ = 0 here, same reason)
> 
> Therefore, 
> $v_{1f} = \frac{m_1 - m_2}{m_1 + m_2} v_{1i}$
> $v_{2f} = \frac{2m_1}{m_1 + m_2} v_{1i}$

> [!tip] Elastic Collisions
> These are the velocities right after the collision (could be considered the initial velocity of the conservation of energy/momentum part):
> $$v_{1f} = \frac{m_1 - m_2}{m_1 + m_2} v_{1i}$$
> $$v_{2f} = \frac{2m_1}{m_1 + m_2} v_{1i}$$
> 
> For $m_1 = m_2$:
> $$v_{1f} = 0$$
> $$v_{2f} = v_{1i}$$
> 
> For $m_1 \gg m_2$ (much larger):
> $$v_{1f} \approx v_{1i}$$
> $$v_{2f} \approx 2v_{1i}$$
> 
> For $m_1 \ll m_2$ (much smaller):
> $$v_{1f} \approx -v_{1i}$$
> $$v_{2f} \approx 0$$

> [!example] Example with Reference Frames (see [[Relative Motion]])
> ![[10.11.24 Reference Frame Elastic Collision Drawing]]
> 
> Known values:
> $m_1 =$ 200 g
> $m_2 =$ 100 g
> $v_{1i} =$ 2.0 m/s
> $v_{2i} =$ 3.0 m/s
> 
> Let $v_1' = v_1 - V$ and $v_2' = v_2 - V$
> 
> Choose $V = v_{2i} =$ -3.0 m/s
> $\rightarrow v_{1i}' = 2.0 - (-3.0) =$ 5.0 m/s
> $\rightarrow v_{2i}' = -3.0 - (-3.0) =$ 0
> 
> Thus,
> $v_{1f}' = \frac{m_1 - m_2}{m_1 + m_2} v_{1i}' = \frac{200 - 100}{200 + 100} (5.0) =$ 1.67 m/s
> $v_{2f}' = \frac{2m_1}{m_1 + m_2} v_{1i}' = \frac{2(200)}{200 + 100} (5.0) =$ 6.67 m/s
> 
> Therefore,
> $v_{1f} = v_{1f}' + V = 1.67 + (-3.0) =$ -1.33 m/s
> $v_{2f} = v_{2f}' + V = 6.67 + (-3.0) =$ 3.67 m/s

> [!example]
> ![[10.11.24 Pendulum Drawing]]
> 
> Known values:
> $m_1 =$ 100 g
> $m_2 =$ 20 g
> 
> a) If the collision is elastic, what is the speed of block 2?
> 
> Conservation of Energy:
> $E_f = E_i$
> $\frac{1}{2}m_1v_{1f}^2 + m_1gy_{1f} = \frac{1}{2}m_1v_{1i}^2 + m_1gy_{1i}$ ($y_{1i}$ = 0 as shown in the drawing, $v_{1i}$ = 0 since the pendulum initially starts from rest)
> $\frac{1}{2}m_1v_{1f}^2 = m_1gy_{1i}$
> $v_{1f} = \sqrt{2gy_{1i}}$
> $\hspace{7mm} = \sqrt{2(9.8)(1.0)(1 - \cos{50\degree})}$
> $\hspace{7mm} =$ 2.65 m/s
> 
> Elastic Collision:
> $v_{2f} = \frac{2m_1}{m_1 + m_2} v_{1i}$
> $\hspace{7.5mm} = \frac{2(100)}{100 + 20} (2.65)$ (we got 2.65 because the pendulum's calculated "final" velocity is now the initial velocity in the elastic collision)
> $\hspace{7.5mm} =$ 4.42 m/s
> 
> b) If the block and pendulum stick together, what is their combined speed just after the collision?
> 
> Conservation of momentum:
> $P_f = P_i$
> $m_1v_{1f} + m_2v_{2f} = m_1v_{1i} + m_2v_{2i}$ ($v_{2i}$ = 0 since it started at rest, $v_{1f} = v_{2f}$ because they stick together so they have a combined final velocity)
> $(m_1 + m_2)v_f = m_1v_{1i}$
> $v_f = \frac{m_1v_{1i}}{m_1 + m_2}$
> $\hspace{6mm} = \frac{(100)(2.65)}{100 + 20}$
> $\hspace{6mm} =$ 2.21 m/s