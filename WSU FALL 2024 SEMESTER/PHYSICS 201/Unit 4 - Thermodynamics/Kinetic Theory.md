---
tags: PHYSICS_201
created: 2024-12-2
---

> Change in Momentum: $\Delta p = mv_f - mv_i$
> For elastic collisions: $v_f = -v_i$
> 
> $\rightarrow \Delta p = 2mv$
> 
> By the impulse-momentum theorem:
> $J = \Delta p$
> $F_{avg}\Delta t_{coll} = 2mv$
> $F_{avg} = \frac{2mv}{\Delta t_{coll}}$
> 
> The net force is:
> $F_{net} = N_{coll} F_{avg} = 2mv_x \frac{N_{coll}}{\Delta t_{coll}}$

> The number of collisions is:
> $N_{coll} = \frac{1}{2} \frac{N}{V} A\Delta x$ ($\frac{1}{2}$ because it's only half moving)
> $\hspace{10mm} = \frac{1}{2} \frac{N}{V} A v_x \Delta t_{coll}$
> 
> Thus, $F_{net} = \frac{N}{V} m(v_x)^2 A$
> 

> 
> Take the average velocity, so
> $(v^2)_{avg} = (v_x^2)_{avg} + (v_y^2)_{avg} + (v_z^2)_{avg} = 3(v_x^2)_{avg}$
> 
> Define the root-mean-square (rms) speed:
> $v_{rms} = \sqrt{(v^2)_{avg}}$
> 
> Therefore, the pressure is:
> $p = \frac{F_{net}}{A} = \frac{1}{3} \frac{N}{V} m v_{rms}^2$
> 
> The average kinetic energy per molecule
> $\epsilon_{avg} = \frac{1}{2}m v^2_{avg} = \frac{1}{2} m v^2_{rms}$
> $\rightarrow p = \frac{2}{3} \frac{N}{V} \epsilon_{avg}$
> 
> From the ideal gas law ([[Macroscopic Description of Matter#^291e1d]]):
> $N k_B T = pV = \frac{2}{3} N \epsilon_{avg}$
> $\rightarrow \epsilon_{avg} = \frac{3}{2} k_B T$
> $v_{rms} = \sqrt{\frac{3 k_B T}{m}}$

> [!tip] Force
> $$F_{net} = 2mv_x \frac{N_{coll}}{\Delta t_{coll}} = \frac{N}{V} m(v_x)^2 A$$

> [!tip] Number of Collisions
> $$N_{coll} = \frac{1}{2} \frac{N}{V} A (v_x) \Delta t_{coll}$$
> 
> Move the $\Delta t_{coll}$ term to the other side to find the rate of collisions.

> [!tip] Pressure
> $$p = \frac{F_{net}}{A} = \frac{1}{3} \frac{N}{V} m v_{rms}^2 = \frac{2}{3} \frac{N}{V} \epsilon_{avg}$$

> [!tip] Root-Mean-Square (rms) Speed
> $$v_{rms} = \sqrt{\frac{3 k_B T}{m}}$$

> [!example]
> Imagine a cylinder container of height of 20 cm and diameter of 10 cm containing 2.0 x 10$^{22}$ atoms of argon gas at temperature 50$\degree$C.
> 
> a) What is the rms speed?
> 
> The mass of an argon atom is:
> $m =$ (40 u)(1.66 x 10$^{-27}$ kg/u) = 6.64 x 10$^{-26}$ kg
> 
> The rms speed is:
> $v_{rms} = \sqrt{\frac{3 k_B T}{m}}$
> $\hspace{10mm} = \sqrt{\frac{3(1.38 \times 10^{-23})(323)}{6.64 \times 10^{-26}}}$
> $\hspace{10mm} =$ 449 m/s
> 
> b) What is the rate at which atoms collide with one end of the cylinder?
> 
> $\frac{N_{coll}}{\Delta t_{coll}} = \frac{1}{2} \frac{N}{V} A (v_x)_{avg}$
> $\hspace{11.2mm} = \frac{1}{2} \frac{N}{\pi r^2 L} (\pi r^2) \sqrt{\frac{1}{3} v^2_{rms}}$
> $\hspace{11.2mm} = \frac{1}{2\sqrt{3}} \frac{2.0 \times 10^{22}}{0.20} (449)$
> $\hspace{11.2mm} =$ 1.30 x 10$^{25}$ atoms per second

### Thermal Energy and Specific Heat

##### Monatomic Gases

$$E_{th} = K_{micro} = N \epsilon_{avg}$$
$$\rightarrow E_{th} = \frac{3}{2} N k_B T = \frac{3}{2} nRT$$

For any ideal gas process:
$\Delta E_{th} = n C_v \Delta T$ ($C_v$: molar specific heat at constant volume)
$\rightarrow C_v = \frac{3}{2}R =$ 12.5 J/(mol x kg)

> [!info] Equipartition Theorem
> The thermal energy of a system of particles is equally divided among all the possible energy modes. For a system of $N$ particles at temperature $T$, the energy stored in each mode (degree of freedom) is $\frac{1}{2} N k_B T$ or $\frac{1}{2} nRT$.

> [!info] Degrees of Freedom
> **Monatomic**: 3 degrees of freedom ($E_{th} = \frac{3}{2} nRT$)
> 
> **Diatomic**: 3 translational modes, 2 rotational modes, 1 vibrational mode (counts as 2 modes for the two different types of energies, $K + u$), 7 degrees of freedom total ($E_{th} = \frac{5}{2} nRT$ at room temperature because the vibrational modes aren't active in these temperatures)
> 
> **Solid**: 3 vibrational modes (counts as 2 modes), 6 degrees of freedom total ($E_{th} = 3nRT$)