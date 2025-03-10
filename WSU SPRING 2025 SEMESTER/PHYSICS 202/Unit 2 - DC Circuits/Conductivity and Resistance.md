---
tags: PHYSICS_202
created: 2025-2-12
---

Recall:
$J = n_e e v_d = n_e e \left(\frac{e \tau E}{m}\right) = \frac{n_e e^2 \tau}{m} E$ <--- current density - [[Current#^964316]]

> [!info] Conductivity
> $$\sigma = \frac{n_e e^2 \tau}{m}$$
> 
> Only depends on the material

> [!tip] Current Density
> $$J = \sigma E$$

> [!info] Resistivity
> $$\rho = \frac{1}{\sigma} = \frac{m}{n_e e^2 \tau}$$

**Superconductors**: materials that have zero resistivity at low temperatures

> Consider a wire of length $L$ with a potential difference $\Delta V$ between both ends of the wire, and containing an electric field $E$ of current $I$, and opening is of area $A$.
> 
> Recall: $E = -\frac{dV}{ds}$
> 
> For constant electric fields
> $E = \frac{\Delta V}{\Delta s} = \frac{\Delta V}{L}$ (only considering magnitude)
> 
> Also,
> $I = JA = A \sigma E = \frac{A}{\rho} E$

> [!tip] Current
> $$I = \frac{A}{\rho} E = \frac{A}{\sigma L} \Delta V = A \sigma E$$

> [!info] Resistance
> $$R = \frac{\rho L}{A}$$
> 
> SI unit: ohm (1 $\ohm$ = 1 V/A)

> [!tip] Ohm's Law
> $$I = \frac{\Delta V}{R}$$

> [!example]
> Lightning strikes a lightning rod and delivers 50 kA of current in 50 $\micro$s. The lightning rod is 5.0 meters long and is made out of iron. You don't want the potential difference between the top and bottom of the rod to exceed 100 V. What is the minimum diameter that the rod can be?
> 
> By Ohm's Law:
> $I = \frac{\Delta V}{R} = \frac{\Delta V}{\frac{\rho L}{A}} = \frac{\Delta V}{\frac{\rho L}{\pi r^2}}$
> $\rightarrow r = \sqrt{\frac{I \rho L}{\pi \Delta v}}$
> $\hspace{9.5mm} = \sqrt{\frac{(50 \times 10^3) (5.8 \times 10^{-8}) (5.0 m)}{\pi (100)}}$
> $\hspace{9.5mm} =$ 8.8 x 10^-3 m = 0.88 cm
> 
> Diameter: 1.76 cm

> [!example]
> There are 2 parallel-plate capacitors separated by 1.0 cm. The capacitors are 10 cm long. The capacitor on the right is charged at 12.5 nC and the capacitor on the left is charged at -12.5 nC. To discharge the capacitors, there is a copper wire with diameter 0.224 mm connected to both of them.
> 
> a) What is the maximum current in the wire?
> The capacitance is:
> $C = \frac{\epsilon_0 A}{d} = \frac{(8.85 \times 10^{-12}) (\pi (0.05)^2)}{0.01}$
> $\hspace{5mm} =$ 7.0 x 10^-12 F
> 
> The potential difference between the plates is:
> $\Delta V = \frac{Q}{C} = \frac{12.5 \times 10^{-9}}{7.0 \times 10^{12}} =$ 1800 V
> 
> The resistance of the wire is:
> $R = \frac{\rho L}{A} = \frac{(1.7 \times 10^{-8}) (0.01)}{\pi (0.112 \times 10^{-3})^2} =$ 4.3 x 10^-3 $\ohm$
> 
> By Ohm's Law, the current is:
> $I = \frac{\Delta V}{R} = \frac{1800}{4.3 \times 10^{-3}} =$ 4.2 x 10^5 A
> 
> b) What is the largest electric field in the wire?
> $E = \frac{Q}{\epsilon_0 A} = \frac{12.5 \times 10^{-9}}{(8.85 \times 10^{-12}) (\pi (0.05)^2)} =$ 1.8 x 10^5 N/C
> 
> c) What is the total energy dissipated in the wire?
> $u = \frac{1}{2} \frac{Q^2}{C} = \frac{1}{2} \frac{(12.5 \times 10^{-9})^2}{7.0 \times 10^{-12}} =$ 1.1 x 10^-5 J