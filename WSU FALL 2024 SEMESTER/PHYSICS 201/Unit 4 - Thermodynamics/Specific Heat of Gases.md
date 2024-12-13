---
tags: PHYSICS_201
created: 2024-11-22
---

> [!tip] For Constant Volume
> $$Q_v = n C_v \Delta T$$
> 
> $n$: number of moles
> $C$: molar specific heat

> [!tip] For Constant Pressure
> $$Q_p = n C_p \Delta T$$

![[11.22.24 Isotherms Graph]]

By the first law of thermodynamics ([[Thermodynamics#^8020b9]]):

$$(\Delta E_{th})_A = W_A + Q_A = n C_v \Delta T$$
$$(\Delta E_{th})_B = W_B + Q_B = -p \Delta V + n C_p \Delta T$$

Since $(\Delta T)_A = (\Delta T)_B$, then:

$(\Delta E_{th})_A = (\Delta E_{th})_B$
$nC_v \Delta T = -p \Delta V + n C_p \Delta T$
$n C_v \Delta T = -(n R \Delta T) + n C_p \Delta T$
$C_p = C_v + R$

Also, for any ideal-gas process:

$$\Delta E_{th} = n C_v \Delta T$$

![[11.22.24 Ideal Gas Graph]]

$(\Delta E_{th})_A = (\Delta E_{th})_B$
$W_A + Q_A = W_B + Q_A$ <--- $W_A \neq W_B$ and $Q_A \neq Q_B$

### Adiabatic Process (Q = 0)

- **Adiabatic process**: no heat flow into the system, but that doesn't necessarily mean the temperature doesn't change ($Q = 0$)

![[11.22.24 Adiabat Graph]]

By the first law of thermodynamics:

$$\Delta E_{th} = W + Q$$
$$\rightarrow W = \Delta E_{th} = nC_v \Delta T$$

Isotherms: $pV$ = constant
Adiabat: $pV^{\gamma}$ = constant, where $\gamma = \frac{C_p}{C_v}$ (1.67 when monotomic and 1.40 when diatomic)

> [!example]
> Imagine a nitrogen gas ($N_2$) isotherm at a constant 21$\degree$C temperature from 1.0 L to 4.0 L. There are 3 moles of the gas.
> 
> a) What is the work done on the gas?
> 
> $W = -nRT\ln({\frac{V_f}{V_i}})$
> $\hspace{6mm} = -(3)(8.31)[(21 + 273)]\ln({\frac{4.0}{1.0}})$
> $\hspace{6mm} =$ -10,000 J
> 
> b) What is the heat flow into the gas?
> 
> $\Delta E_{th} = W + Q = nC_v\Delta T$ <------ $\Delta T$ goes to 0
> $\rightarrow Q = -W =$ 10,000 J

> [!example]
> Imagine a nitrogen gas ($N_2$) adiabat starting at 21$\degree$C at 1.0 L to an unknown temperature at 4.0 L. There are 3 moles of the gas.
> 
> a) What is the work done on the gas?
> 
> The final temperature is:
> $p_1V_1^{\gamma} = p_2V_2^{\gamma}$
> $\left(\frac{nRT_1}{V_1}\right)V_1^{\gamma} = \left(\frac{nRT_2}{V_2}\right)V_2^{\gamma}$
> $T_1 V_1^{\gamma - 1} = T_2 V_2^{\gamma - 1}$
> $T_2 = \left(\frac{V_1}{V_2}\right)^{\gamma - 1} T_1$
> $\hspace{6mm} = \left(\frac{1.0}{4.0}\right)^{1.40 - 1}(294)$ <----- $\gamma =$ 1.40 since $N_2$ is a diatomic gas
> $\hspace{6mm} =$ 168 K
> 
> The work done is:
> $W = nC_v \Delta T = (3)(20.8)(168 - 294) =$ -7860 J
> 
> b) What is the heat flow into the gas?
> $Q = 0$ since it's an adiabatic process.

### Calorimetry

- **Calorimetry**: two objects of different temperatures will transfer heat to each other until the temperatures are at equilibrium

By conservation of energy:

$$Q_1 + Q_2 = 0$$
$$\rightarrow Q_1 = -Q_2$$

> [!example]
> Imagine water with a mass of 325 g in an aluminum container with mass 100 g, where both substances are heated to 98$\degree$C. Imagine another object (an unknown metal) with a mass of 512 g and a temperature of 15$\degree$C being placed into the water. When the ball is in the water, the total temperature of the system drops to 78$\degree$C.
> 
> What is the metal?
> $Q_m + Q_w + Q_{Al} = 0$
> $m_mC_m\Delta T_m + m_wC_w\Delta T_w + m_{Al}C_{Al}\Delta T_{Al} = 0$
> $C_m = \frac{-(m_w C_w \Delta T_w + m_{Al} C_{Al} \Delta T_{Al}}{m_m \Delta T_m}$
> $\hspace{8mm} = \frac{-[(325)(4190)(78 - 98) + (100)(900)(78 - 98)]}{(512)(83)}$
> $\hspace{8mm} =$ 900 J/kg \* K ------> This is aluminum.