---
tags: PHYSICS_201
created: 2024-10-23
---

- **Fluid**: a substance that flows
	- Takes the shape of the container
	- Liquids and gases both considered fluids
		- Liquids are incompressible (volume does not change)
		- Gases are compressible

- **Mass density**: mass to volume ratio

$$\rho = \frac{m}{V}$$

- **Pressure**: force to area ratio
	- SI unit: Pascals (Pa)
		- 1 Pa = 1 N/m$^2$

$$P = \frac{F}{A}$$

### Causes of Pressure

1. Gravitational contribution

![[10.23.24 Gravitational Liquid Drawing]]

2. Thermal contribution

![[10.23.24 Temperature Gas Drawing]]

- **Vacuum**: pressure goes to zero
	- There are no particles in the region

##### Atmospheric pressure
![[10.23.24 Atmospheric Pressure Drawing]]

At sea level,
$P_{atmos} =$ 1 standard atmosphere = 1 atm = 101,300 Pa

##### Pressures in Liquid (Hydrostatic Pressure)

> ![[10.23.24 Hydrostatic Pressure Drawing]]
> 
> Free-body diagram:
> ![[10.23.24 Hydrostatic Pressure FBD]]
> 
> Newton's Second Law:
> $PA - P_{o}A - w = ma_y$ ($a_y$ = 0 since there is no acceleration)
> $P = P_o + \frac{mg}{A}(\frac{d}{d})$
> $\hspace{5mm} = P_o + \rho g d$

> [!info]
> A connected liquid in hydrostatic equilibrium rises to the same height in all open regions of the container.

> [!info]
> The pressure is the same at all points on a horizontal line through a connected liquid in hydrostatic equilibrium.

> [!info] Pascal's Principle
> A change in the pressure at one point in an incompressible fluid appears undiminished at all points in the fluid.

### Hydraulics

![[10.23.24 Hydraulic Drawing]]

$P_1 = P_2$

> [!tip] Hydraulics Equation
> $$\frac{F_1}{A_1} = \frac{F_2}{A_2} + \rho g h$$

> [!example]
> How far must a 2.0-cm diameter piston be pushed down into one cylinder of a hydraulic lift to raise an 8.0-cm diameter piston by 20 cm?
> 
> ![[10.23.24 Hydraulic Lift Drawing]]
> 
> Known values:
> $d_1 =$ 2.0 cm
> $d_2 =$ 8.0 cm
> 
> $V_1 = V_2$
> $A_1h_1 = A_2h_2$
> $h_1 = \frac{A_2}{A_1}h_2$
> $\hspace{6mm} = \frac{\pi r_2^2}{\pi r_1^2}h_2$
> $\hspace{6mm} = \frac{(4.0)^2}{(1.0)^2}(20)$
> $\hspace{6mm} =$ 320 cm = 3.2 m

> [!example]
> a) A 70 kg student balances a 1200 kg elephant on a hydraulic lift. What is the diameter of the piston the student is standing on?
> 
> ![[10.23.24 Student Elephant Drawing]]
> 
> Known values:
> $m_1 =$ 70 kg
> $m_2 =$ 1200 kg
> $d_2 =$ 2.0 m
> 
> $P_1 = P_2$
> $\frac{F_1}{A_1} = \frac{F_2}{A_2}$
> $\frac{m_1g}{\pi r_1^2} = \frac{m_2g}{\pi r_2^2}$
> $r_1 = \sqrt{\frac{m_1}{m_2}}r_2$
> $\hspace{5.5mm} = \sqrt{\frac{70}{1200}}(1.0)$
> $\hspace{5.5mm} =$ 0.242 m
> 
> b) A second 70 kg student joins the first student. How high do they lift the elephant?
> 
> $P_1 = P_2$
> $\frac{F_1}{A_1} = \frac{F_2}{A_2} + \rho g (h_1 + h_2)$ (The students go down a height of $h_1$ and the elephant rises a height of $h_2$)
> $\frac{F_1}{A_1} = \frac{F_2}{A_2} + \rho g (h_2 \frac{A_2}{A_1} + h_2)$
> $\frac{m_1g}{\pi r_1^2} = \frac{m_2g}{\pi r_2^2} + \rho g (h_2 \frac{\pi r_2^2}{\pi r_1^2} + h_2)$
> $h_2 = \frac{\frac{m_1}{\pi r_1^2} - \frac{m_2}{\pi r_2^2}}{\rho (\frac{r_2^2}{r_1^2} + 1)}$
> $\hspace{6mm} =$ 0.0233 m = 2.33 cm (plugging in values, using 900 kg/m$^3$ for $\rho$, or density of the oil)