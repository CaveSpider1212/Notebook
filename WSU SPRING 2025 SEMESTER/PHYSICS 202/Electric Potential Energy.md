---
tags: PHYSICS_202
created: 2025-1-27
---

Recall for mechanical potential energy
$\Delta u = -W_c$ <---- $W_c$ is the work due to conservative forces

Also,
$\displaystyle W = \int_{s_i}^{s_f} \vec{F} \cdot \text{d}\vec{s}$

> Consider a positive charge between a parallel plate capacitor.
> ![[1.27.25 Parallel Plate Capacitor Drawing]]
> 
> Electric field: $\vec{E} = \frac{\eta}{\epsilon_0}\hat{k}$ <---- where $\eta = \frac{Q}{A}$
> 
> $W = \int_{s_i}^{s_f} \vec{F} \cdot \text{d}\vec{s}$
> $\hspace{6mm} = \int_{s_i}^{s_f} q\vec{E} \cdot \text{d}\vec{s}$
> $\hspace{6mm} = qE(s_f - s_i)$ <---- uniform electric field
> 
> Thus, the electric potential energy is
> $\Delta u = -W = -qE(s_f - s_i)$
> 
> In general, $s$ is measured from the negative place, so:
> $u_{\text{elect}} = u_0 + qEs$ <--- where $u_0 = u(s = 0)$

> For point charges
> ![[1.27.25 Point Charge Drawing]]
> 
> $W = \int_{s_i}^{s_f} \vec{F} \cdot \text{d}\vec{s}$
> $\hspace{6mm} = \int_{s_i}^{s_f} \frac{1}{4\pi\epsilon_0} \frac{q_1q_2}{s^2} \text{d}s$
> $\hspace{6mm} = -\frac{1}{4\pi\epsilon_0} q_1q_2 (\frac{1}{s_f} - \frac{1}{s_i})$
> 
> $\Delta u = \frac{1}{4\pi\epsilon_0} q_1q_2 (\frac{1}{s_f} - \frac{1}{s_i})$
> 
> Let the zero of the electric potential be at $\infty$.
> Therefore, the electric potential energy for two point charges is
> $u_{\text{elect}} = \frac{1}{4\pi\epsilon_0} \frac{q_1q_2}{r}$

> [!tip] Electric Potential Energy for Two Point Charges
> $$u_{\text{elect}} = \frac{1}{4\pi\epsilon_0} \frac{q_1q_2}{r}$$
> 
> Add up all of the electric potential energies between two charges if there are more than 2 points.

> [!example]
> 3 particles, all 1 cm apart-
> 
> Particle 1: 1.0 g, 5.0 nC, positive charge
> Particle 2: 2.0 g, -1.0 nC, negative charge
> Particle 3: 1.0 g, 5.0 nC, positive charge
> 
> What is the speed of the positive beads, when they are very far apart?
> 
> Conservation of energy:
> $E_f = E_i$
> $K_f + u_f = K_i + u_i$ <--- $K_i$ = 0 since it starts from rest, $u_f$ = 0 because when the charges are very far apart there is no electric potential energy
> $\frac{1}{2}m_1v_1^2 + \frac{1}{2}m_1v_2^2 + \frac{1}{2}m_3v_3^2 = \frac{1}{4\pi\epsilon_0}(\frac{q_1q_2}{r_{12}} + \frac{q_1q_3}{r_{13}} + \frac{q_2q_3}{r_{23}})$ <---- $v_2$ = 0 since particle 2 never moves
> $mv^2 = \frac{1}{4\pi\epsilon_0} (\frac{q_1q_2}{r_{12}} + \frac{q_1q_3}{r_{13}} + \frac{q_2q_3}{r_{23}})$ <--- $m_1v_1^2$ and $m_2v_2^2$ are combined since they are the same term basically
> $v = \sqrt{\frac{1}{4\pi\epsilon_0 m} (\frac{q_1q_2}{r_{12}} + \frac{q_1q_3}{r_{13}} + \frac{q_2q_3}{r_{23}})}$
> $\hspace{4mm} =$ 0.047 m/s = 4.7 cm/s <---- after plugging all of the known values into the above equation

> [!example]
> Two positive point charges are 5.0 cm apart. If the electric potential energy is 72 $\micro$J, what is the magnitude of the force between the charges?
> 
> The force is
> $F = \frac{1}{4\pi\epsilon_0} \frac{q_1q_2}{r^2} = \frac{u}{r} = \frac{72 \times 10^{-6}}{0.05} =$ 1.4 x 10$^3$ N

> Now, consider a dipole in a uniform electric field
> ![[1.27.25 Dipole Drawing]]
> 
> $W = \int_{s_i}^{s_f} \vec{F} \cdot \text{d}\vec{s}$
> $\hspace{6mm} = \int_{s_i}^{s_f} F_t \text{d}s$ <---- $F_t$ is the tangential force
> $\hspace{6mm} = \int_{\varphi_i}^{\varphi_f} F_t r \text{d}\varphi$
> $\hspace{6mm} = \int_{\varphi_i}^{\varphi_f} \tau \text{d}\varphi$
> $\hspace{6mm} = \int_{\varphi_i}^{\varphi_f} (-pE\sin\varphi) \text{d}\varphi$
> $\hspace{6mm} = pE(\cos\varphi_f - \cos\varphi_i)$
> (see)
> 
> Therefore, the potential energy is
> $u = -W = -pE\cos\varphi = -\vec{p} \cdot \vec{E}$

> [!tip] Electric Potential Energy for a Dipole
> $$u_{\text{elect}} = -pE\cos\varphi = -\vec{p} \cdot \vec{E}$$

> [!example]
> Consider a dipole that oscillates between $\pm$ 60$\degree$ with the following potential energy curve:
> 
> ```desmos-graph
> left = -3.25; right = 3.25
> top = 3; bottom = -3
> ---
> y = -2\cos(x)
> ```
> Note: electric potential energy is 2 $\micro$J at -180 and 180 degrees
> 
> What is the dipole's kinetic energy when it is aligned with the electric field?
> 
> The total mechanical energy at 60$\degree$ is
> $E = K + u = -pE\cos\varphi = (2)\cos(60\degree) =$ -1 $\micro$J
> 
> The kinetic energy at 0$\degree$ is
> $K = E - u = -1 - (-2) =$ 1 $\micro$J