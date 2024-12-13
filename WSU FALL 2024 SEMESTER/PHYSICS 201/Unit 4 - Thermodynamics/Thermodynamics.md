---
tags: PHYSICS_201
created: 2024-11-18
---

> [!tip] Work-Energy Theorem
> 
> $$\Delta K = W_{net} = W_c + W_{diss} + W_{ext}$$
> where $W_c = -\Delta u$ and $W_{diss} = -\Delta E_{th}$
> 
> $W_c$: work done by conservative forces
> $W_{diss}$: work done by dissipated forces
> $W_{ext}$: work done by external forces
> $E_{th}$: thermal energy
> 
> $$\rightarrow \Delta E_{sys} = \Delta K + \Delta u + \Delta E_{th} = W_{ext} \hspace{1mm} (+ Q)$$
> 
> $Q$: heat

### Work for Ideal Gases

> [!tip] Work done by External Forces
> 
> $$W_{ext} = \int_{s_i}^{s_f} F_{ext} ds$$
> $$\hspace{14mm} = \int_{s_i}^{s_f} -F_{gas}ds$$
> $$\hspace{14mm} = \int_{s_i}^{s_f} -(pA)ds$$
> $$\hspace{14mm} = -\int_{V_i}^{V_f} pdV$$
> 
> This is the negative of the area under the $pV$ curve

> [!info] Isochoric Process ($\Delta V$ = 0)
> 
> $W = 0$ since volume doesn't change

> [!info] Isobaric Process ($\Delta p$ = 0)
> 
> $W = -p\Delta V$ since it is just the area of the rectangle created by the pressure and the difference in volume

> [!info] Isothermal Process ($\Delta T$ = 0)
> 
> $W = -\int_{V_i}^{V_f} pdV$ since it is the area under the pressure curve
> $\hspace{6mm} = -\int_{V_i}^{V_f} \frac{nRT}{V}dV$
> $\hspace{6mm} = -nRT \int_{V_i}^{V_f} \frac{1}{V} dV$
> $\hspace{6mm} = -nRT \ln({\frac{V_f}{V_i}})$

### Heat (Q)

- **Heat**: energy transferred due to a temperature difference
	- $Q > 0$: $T_{env} > T_{sys}$
	- $Q = 0$: $T_{env} = T_{sys}$
	- $Q > 0$: $T_{env} < T_{sys}$

> [!info] First Law of Thermodynamics
> 
> $$\Delta E_{sys} = \Delta E_{mech} + \Delta E_{th} = W_{ext} + Q$$
> 
> **First Law of Thermodynamics**: If $\Delta E_{mech} = 0$, then $\Delta E_{th} = W_{ext} + Q$.

^8020b9

> [!example]
> Imagine a piston pushing down on some gas.
> 
> Known values:
> $d_{piston} =$ 16 cm = 0.16 m
> $p_{gas} =$ 3.0 atm = 303900 Pa
> 
> a) How much force does the gas exert on the piston?
> $F_{gas} = pA = (303900)\pi(0.08)^2 =$ 6110 N
> 
> b) The gas expands at constant pressure and pushes the piston out 10.0 cm. How much work is done by the environment?
> $W_{ext} = -\int_{V_i}^{V_f}pdV$
> $\hspace{11mm} = -p(V_f - V_i)$
> $\hspace{11mm} = -(303900)(\pi(0.08)^2(0.10))$
> $\hspace{11mm} =$ -611 J
> 
> c) The thermal energy of the gas increases by 196 J. How much heat was transferred?
> $\Delta E_{th} = W_{ext} + Q$
> $Q = \Delta E_{th} - W_{ext}$
> $\hspace{5mm} = 196 - (-611)$
> $\hspace{5mm} =$ 807 J

### Thermal Properties of Matter

> [!tip] Thermal Properties of Matter
> <u>As the temperature changes:</u>
> $$Q = mc\Delta T$$
> 
> $c$: specific heat (constant)
> 
> $$Q = nC \Delta T$$
> 
> $n$: number of moles
> $C$: molar specific heat
> 
> <u>During phase transformations:</u>
> $$Q = \pm mL$$
> 
> $L_f$: latent heat of fusion (positive for solid to liquid, negative for liquid to solid)
> $L_v$: latent heat of vaporization (positive for liquid to gas, negative for gas to liquid)

> [!example]
> Imagine a container of steam.
> 
> Known values:
> $V =$ 1530 cm$^3$ = 0.00153 m$^3$
> $T =$ 100$\degree$C
> $p =$ 2.0 atm = 202,600 Pa
> 
> How much heat is needed to change the steam into water at 20$\degree$C?
> 
> The number of moles of steam is:
> $n = \frac{pV}{RT} = \frac{(202600)(0.00153)} =$ 0.10 mol
> 
> The mass of the steam is:
> $m = nM_{mol} = (0.10)(18) =$ 1.8 g
> 
> The heat needed is:
> $Q = -mL_v + mc_w \Delta T$
> $\hspace{5mm} = (0.0018)[-(22.6 \times 10^5) + (4190)(20\degree - 100\degree)]$
> $\hspace{5mm} =$ -4700 J