---
tags: PHYSICS_202
created: 2025-1-27
---

### Electric Potential Energy

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

### Electric Potential

> [!tip] Electric Potential Formula
> $$V = \frac{u}{q}$$
> 
> SI unit: volt (V) = J/C
> The potential difference $\Delta V$ is the voltage.

> [!example]
> What potential difference is needed to accelerate a $He^+$ ion from rest to a speed of 2.0 x 10^6 m/s?
> 
> Conservation of Energy:
> $E_f = E_i$
> $K_f + u_f = K_i + u_i$ <---- $K_i$ = 0 since the particle starts at rest (so initial velocity is 0)
> $u_f - u_i = -K_f$
> $\Delta u = -K_f$
> $q\Delta V = -K_f$
> $\Delta V = \frac{1}{2q} mv^2$
> $\hspace{9mm} = \frac{1}{2(1.6 \times 10^{-19})} (4)(1.661 \times 10^{-27})(2.0 \times 10^6)^2$
> $\hspace{9mm} =$ -83,000 V = -83 kV

> [!example]
> There are two parallel plate capacitors (one negative and one positive). The negative one has 0 V electric potential and the positive one has 500 V electric potential. The electric field goes from the positive to the negative plate. There is a proton at the midpoint (where the initial electric potential would be 250 V) between the two going 200,000 m/s towards the positive plate, but it will end up curving back to the negative plate (final electric potential is 0 V).
> 
> What is the proton's speed as it collides with the negative plate?
> 
> Conservation of Energy:
> $E_f = E_i$
> $K_f + u_f = K_i + u_i$
> $K_f = K_i - \Delta u$
> $\frac{1}{2}mv_f^2 = \frac{1}{2}mv_i^2 - q\Delta V$
> $v_f = \sqrt{v_i^2 - \frac{2q}{m}\Delta V}$
> 
> The voltage between the plates is:
> $\Delta V = \frac{\Delta u}{q} = \frac{qEs}{q} = Es$ <--- The voltage increases linearly with the distance.
> 
> $v_f = \sqrt{(200,000)^2 - \frac{2(1.6 \times 10^{-19})}{1.67 \times 10^{-27}} (0 - 250)} =$ 2.96 x 10^5 m/s

> [!example]
> There is a bead with a positive charge with a radius of 3 mm. The potential difference ($\Delta V$) 5mm from the center of the bead is 500 V.
> 
> What is the charge on the bead?
> 
> The potential for a point charge is:
> $V = \frac{u}{q} = \frac{\frac{q_1q_2}{4\pi\epsilon_0 r}}{q_2} = \frac{1}{4\pi\epsilon_0} \frac{q}{r}$
> 
> Thus,
> $\Delta V = \frac{q}{4\pi\epsilon_0}(\frac{1}{r_f} - \frac{1}{r_i})$
> $q = \frac{4\pi\epsilon_0 \Delta V}{(\frac{1}{r_f} - \frac{1}{r_i})}$
> $\hspace{3.5mm} = \frac{4\pi(8.85 \times 10^{-12}) (500)}{(\frac{1}{0.003} - \frac{1}{0.005})}$
> $\hspace{3.5mm} =$ 4.2 x 10^-10 C

> [!example]
> ![[1.29.25 Electric Potential Example 1]]
> 
> Find an expression for the electric potential at point P.
> 
> $V = \sum\limits_i \frac{1}{4\pi\epsilon_0} \frac{q_i}{r_i} \rightarrow \int \frac{1}{4\pi\epsilon_0} \frac{\text{d}q}{r}$ <--- where $\frac{\text{d}q}{Q} = \frac{\text{d}x}{L}$ and $r = d - x$
> $\hspace{4mm} = \frac{1}{4\pi\epsilon_0} \int_{\frac{-L}{2}}^{\frac{L}{2}} \frac{\frac{Q}{L} \text{d}x}{d - x}$
> $\hspace{4mm} = \frac{\frac{Q}{L}}{4\pi\epsilon_0} [-\ln(d - x)]_{\frac{-L}{2}}^{\frac{L}{2}}$
> $\hspace{4mm} = \frac{Q}{4\pi\epsilon_0 L} \ln(\frac{d + \frac{L}{2}}{d - \frac{L}{2}})$

> [!example]
> ![[1.29.25 Electric Potential Example 2]]
> 
> Find an expression for the electric potential at point P.
> 
> $V = \frac{1}{4\pi\epsilon_0} \int \frac{\text{d}q}{r}$ <---- where $\frac{\text{d}q}{Q} = \frac{\text{d}y}{L}$ and $$r = \sqrt{y^2 + d^2}$$
> $\hspace{4mm} = \frac{1}{4\pi\epsilon_0} \int_{\frac{-L}{2}}^{\frac{L}{2}} \frac{\frac{Q}{L} \text{d}y}{\sqrt{y^2 + d^2}}$
> $\hspace{4mm} = \frac{Q}{4\pi\epsilon_0 L} [\ln(\sqrt{y^2 + d^2} + y)]_{\frac{-L}{2}}^{\frac{L}{2}}$ <--- evaluate this to get the answer