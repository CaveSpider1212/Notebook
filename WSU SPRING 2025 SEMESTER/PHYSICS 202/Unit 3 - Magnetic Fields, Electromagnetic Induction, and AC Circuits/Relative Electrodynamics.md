---
tags: PHYSICS_202
created: 2025-3-31
---

Moving frame (a) and rest frame (b):
![[3.31.25 Reference Frames.png]]

For inertial frames, the forces in a moving frame and a rest frame are equivalent, so
$$\vec{F} = \vec{F}'$$
$$q(\vec{E} + \vec{v} \times \vec{B}) = q\vec{E}'$$
$$\vec{E}' = \vec{E} + \vec{v} \times \vec{B}$$

In the rest frame, the electric field of the charge is:
$$\vec{E} = \frac{1}{4\pi \epsilon_0} \frac{q}{r^2} \hat{r}$$

In the moving frame, by the Biot-Savart Law:
$$\vec{B}' = \frac{-\mu_0}{4 \pi} \frac{q}{r^2} \vec{v} \times hat{r} = -\epsilon_0 \mu_0 \vec{v} \times \left(\frac{1}{4\pi \epsilon_0} \frac{q}{r^2} \hat{r}\right) = -\epsilon_0 \mu_0 \vec{v} \times \vec{E}$$

> Consider
> 
> $\frac{1}{\sqrt{\epsilon_0 \mu_0}} = \frac{1}{\sqrt{(4\pi \times 10^{-9}) (8.85 \times 10^{12})}} =$ 3.00 x 10^8 m/s = c <--- speed of light

In general,
$$\vec{B}' = \vec{B} - \frac{1}{c^2} \vec{v} \times \vec{E}$$

> [!example]
> There is an electron moving through a 0.010 T magnetic field to the right at 2.00 x 10^7 m/s. What is the strength and direction of the electric field that will allow the electron to not be deflected?
> 
> $\vec{F} = 0 = q(\vec{E} + \vec{v} \times \vec{B})$
> $\rightarrow \vec{E} = - \vec{v} \times \vec{B}$
> $\hspace{11mm} = (2.0 \times 10^{7}) (0.010) \sin{90 \degree}$
> $\hspace{11mm} =$ 2.0 x 10^5 N/C, downward

### Displacement Current

Ampere's Law: $\oint \vec{B} \cdot d\vec{s} = \mu_0 I$ <--- $I$ is the current passing through any closed surface bounded by the closed curve C

![[3.31.25 Ampere's Law Surface.png]]

> [!tip] Displacement Current
> $$I_d = \epsilon_0 \frac{d \Phi_E}{dt}$$
> 
> where $\Phi_E$ is the electric flux crossing the surface.

> [!info] Generalized Form of Ampere's Law
> $\oint_c \vec{B} \cdot d\vec{s} = \mu_0(I + I_d) = \mu_0 I + \mu_0 \epsilon_0 \frac{d \Phi_E}{dt}$ <--- $(I + I_d)$ is the generalized current
> 
> - The generalized current is identical for all surfaces bounded by the curve C.
> - If the displacement current is zero, then there is no charge build up.

### Maxwell's Equations

> [!info] Maxwell's Equations
> $\oint \vec{E} \cdot d\vec{A} = \frac{Q_{in}}{\epsilon_0}$ <--- Gauss's Law
> $\oint \vec{B} \cdot d\vec{A} = 0$ <--- Gauss's Law for magnetism
> $\oint \vec{E} \cdot d\vec{s} = \frac{-d \Phi_m}{dt}$ <--- Faraday's Law
> $\oint \vec{B} \cdot d\vec{s} = \mu_0 I + \mu_0 \epsilon_0 \frac{d \Phi_E}{dt}$ <--- Ampere-Maxwell Law

> [!example]
> There are 2 parallel-plate capacitors with wires attached to them separated by 1.0 mm with radii of 2.3 cm. There is a 5.0 A current flowing through the capacitor wires.
> 
> a) What is the rate of change of the electric field between the plates?
> 
> For parallel plates:
> $E = \frac{Q}{\epsilon_0 A}$
> 
> Thus,
> $\frac{dE}{dt} = \frac{1}{\epsilon_A} \frac{dQ}{dt} = \frac{I}{\epsilon_0 A} = \frac{5.0}{(8.85 \times 10^{-12}) (\pi (0.023)^2)} =$ 3.4 x 10^14 V/m\*s
> 
> b) What is the displacement current between the plates?
> $I_d = \epsilon_0 \frac{d \Phi_E}{dt} = \epsilon_0 \frac{d}{dt} (\int \vec{E} \cdot d\vec{A})$
> $\hspace{5.5mm} = \epsilon_0 \frac{d}{dt} (EA)$
> $\hspace{5.5mm} = \epsilon_0 A \frac{dE}{dt}$
> $\hspace{5.5mm} = (8.85 \times 10^{-12})(\pi (0.023)^2) (3.40 \times 10^{14})$
> $\hspace{5.5mm} =$ 5.0 A

> [!example]
> There is a series circuit with a battery, resistor, capacitor, and a switch. The resistor has a value of 150 $\ohm$, the capacitor has a value of 2.5 pF and the plates are separated by 5.0 mm, and the battery has a voltage of 25 V. The switch is open.
> 
> What is the maximum electric flux and maximum displacement current through the capacitor?
> 
> The maximum electric flux is:
> $\Phi_E = \int \vec{E} \cdot d\vec{A}$
> $\hspace{7mm} = EA$
> $\hspace{7mm} = \left(\frac{\epsilon}{d}\right)(\frac{Cd}{\epsilon_0})$ <--- where $C = \frac{\epsilon_0 A}{d}$
> $\hspace{7mm} = \left(\frac{25}{5.0 \times 10^{-3}}\right) (\frac{(2.5 \times 10^{-12}) (5.0 \times 10^{-3})}{8.85 \times 10^{-12}})$
> $\hspace{7mm} =$ 7.1 Vm
> 
> The maximum displacement current is:
> $I_d = \epsilon_0 \frac{d \Phi_E}{dt}$
> $\hspace{5.5mm} = \epsilon_0 \frac{d}{dt} (\frac{V_C C}{\epsilon_0})$
> $\hspace{5.5mm} = C \frac{d V_C}{dt}$
> $\hspace{5.5mm} = C \frac{d}{dt} (\epsilon e^{\frac{-t}{RC}})$
> $\hspace{5.5mm} = \frac{-\epsilon}{R} e^{\frac{-t}{RC}}$
> $I_{d, max} = \frac{\epsilon}{R} = \frac{25}{150} =$ 0.17 A