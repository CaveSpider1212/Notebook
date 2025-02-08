---
tags: PHYSICS_202
created: 2025-2-5
---

Recall the electric field between the plates of a parallel-plate capacitor is: $\vec{E} = \frac{Q}{\epsilon_0 A} \hat{k}$

The voltage difference between the plates: $\Delta V = Ed$ <--- $d$: distance between the plates

Thus, $Q = \frac{\epsilon_0 A}{d} \Delta V$, so charge ($Q$) is proportional to the voltage difference $\Delta V$.

> [!tip] Capacitance
> Constant of proportionality
> 
> $$C = \frac{Q}{\Delta V}$$
> 
> Note: only depends on geometry
> SI unit: farad

> [!info] Capacitance for a Parallel-Plate Capacitor
> $$C = \epsilon_0 \frac{A}{d}$$

> [!example] Spherical Capacitor Example
> ![[2.5.25 Spherical Capacitor Drawing]]
> 
> Find the capacitance.
> 
> The potential difference is:
> $\Delta V = -\int_{s_i}^{s_f} \vec{E} \cdot d\vec{s}$
> $\hspace{9mm} = -\int_{R_1}^{R_2} \frac{-Q}{4\pi\epsilon_0 r^2} dr$
> $\hspace{9mm} = \frac{Q}{4\pi\epsilon_0}\left(\frac{-1}{r}\right) |_{R_1}^{R_2}$
> $\hspace{9mm} = \frac{Q}{4\pi\epsilon_0} (-\frac{1}{R_2} + \frac{1}{R_1})$
> 
> The capacitance is:
> $C = \frac{Q}{\Delta V}$
> $\hspace{5mm} = \frac{4\pi\epsilon_0}{(\frac{-1}{R_2} + \frac{1}{R_1})}$
> $\hspace{5mm} = 4\pi\epsilon_0 (\frac{R_2 R_1}{R_2 - R_1})$

### Circuits with Capacitors (Equivalent Capacitance)

##### Parallel

![[2.5.25 Parallel Circuit Drawing]]

The total charge is: $Q = Q_1 + Q_2$

The potential difference is the same for each capacitor: $Q_1 = \epsilon C_1$ and $Q_2 = \epsilon C_2$

Hence, $Q = \epsilon C_1 + \epsilon C_2 = \epsilon(C_1 + C_2) = \epsilon C_{eq}$, where $C_{eq} = C_1 + C_2$ is the equivalent capacitance.

> [!tip] Equivalent Capacitance (Parallel Circuit)
> $$\displaystyle C_{eq} = \sum_i C_i$$

##### Series

![[2.5.25 Series Circuit Drawing]]

The charges are the same: $Q = C_1\Delta V_1$ and $Q = C_2\Delta V_2$

Hence, $\epsilon = \Delta V_1 + \Delta V_2 = \frac{Q}{C_1} + \frac{Q}{C_2} = Q\left(\frac{1}{C_1} + \frac{1}{C_2}\right) = \frac{Q}{C_{eq}}$, where $\frac{1}{C_{eq}} = \frac{1}{C_1} + \frac{1}{C_2}$

> [!tip] Equivalent Capacitance (Series Circuit)
> $$\displaystyle \frac{1}{C_{eq}} = \sum_i \frac{1}{C_i}$$

### Energy Stores in a Capacitor

$du = dq\Delta V = \frac{q}{C}dq$
$\rightarrow u = \int_{0}^{Q} \frac{q dq}{C} = \frac{1}{2} \frac{Q^2}{C} = \frac{1}{2} \frac{C\Delta V)^2}{C} = \frac{1}{2} C (\Delta V)^2$

> [!info] Energy Stored and Density
> $$u = \frac{1}{2} C (\Delta V)^2$$
> 
> The energy density is: $u_E = \frac{\text{energy}}{\text{volume}}$

> [!tip] Energy Density (Parallel-Plate Capacitor)
> $$u_E = \frac{\frac{1}{2} C (\Delta V)^2}{Ad} = \frac{1}{2}\epsilon_0 E^2$$ <--- $C = \frac{\epsilon_0 A}{d}$ and $\Delta V = Ed$

> [!example]
> ![[2.5.25 Series Circuit Example]]
> 
> Known values:
> $Q_1 =$ 450 $\micro$C
> $C_1 =$ 12 $\micro$F
> $\epsilon =$ 60 V
> 
> What is $C_2$ (capacitance of capacitor 2)?
> 
> $\epsilon = \frac{Q}{C_{eq}} = Q(\frac{1}{C_1} + \frac{1}{C_2})$
> $\rightarrow C_2 = Q(\epsilon - \frac{Q}{C_1})^{-1}$
> $\hspace{13mm} = \frac{(450 \times 10^{-6})}{60 - \frac{450 \times 10^{-6}}{12 \times 10^{-6}}}$
> $\hspace{13mm} =$ 2.0 x 10^-5 F = 20 $\micro$F