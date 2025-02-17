---
tags: PHYSICS_202
created: 2025-2-14
---

### Kirchhoff's Laws

1. Junction: $\sum I_{in} = \sum I_{out}$
2. Loop: $\Delta V_{loop} = 0$

> For ideal batteries or capacitors -
> 
> If the travel of the loop is from the negative to positive end of the battery:
> $\Delta V = \epsilon$
> 
> If the travel of the loop is from the positive to negative end of the battery:
> $\Delta V = -\epsilon$

> For resistors -
> 
> If the travel of the loop is in the same direction as the current flow:
> $\Delta V = -IR$
> 
> If the travel of the loop in the opposite direction as the current flow:
> $\Delta V = IR$

> [!example]
> A 150 $\ohm$ resistor is connected in series to a 24 V battery. The current flows from the positive end of the battery and the travel of the loop is in the same direction. What is the current in the circuit?
> 
> By Kirchhoff's Loop Law:
> $\Delta V_{loop} = 0$
> $\epsilon - IR = 0$
> $I = \frac{\epsilon}{R} = \frac{24}{150} =$ 0.16 A

### Energy and Power

> Assume there is a resistor with $\Delta V$ voltage drop and $\Delta Q$ charge going through.
> 
> Energy change: $\Delta u = Q \Delta V$

> [!info] Power
> $$P = \frac{\Delta u}{\Delta t} = \frac{Q}{\Delta t} \Delta V = I \Delta V$$
> 
> Using Ohm's Law ($\Delta V = IR$):
> 
> $$P = I^2 R = \frac{(\Delta V)^2}{R}$$
> 
> SI unit: Watt (W or J/s or A * V))

> [!example]
> A 2.0 A battery charge is connected to a 120 V supply. The charger is left on for an hour. Assume that electricity costs $0.08 kWh. What is the cost to run the charger?
> 
> The power used is:
> $P = I \Delta V = (2.0)(120) =$ 240 W
> 
> The cost is:
> cost = $P\Delta t (\frac{\text{cost}}{\text{kWh}}) = (240)(1)\left(\frac{0.08}{1000}\right)=$ $0.019 = 2 cents

### Equivalent Resistance

##### Series

> ![[2.14.25 Series Circuit Drawing]]
> 
> By Kirchhoff's Loop Law:
> $\epsilon - IR_1 - IR_2 = 0$
> $\epsilon = I(R_1 + R_2) = I R_{eq}$ <--- where $R_{eq} = R_1 + R_2$ is the equivalent resistance

> [!tip] Equivalent Resistance (Series)
> $$R_{eq} = \sum R_i$$

##### Parallel

> ![[2.14.25 Parallel Circuit Drawing]]
> 
> By Kirchhoff's Junction Law:
> $I = I_1 + I_2$
> 
> By Kirchhoff's Loop Law:
> Loop 1 - $\epsilon - I_1R_1 = 0 \rightarrow I_1 = \frac{\epsilon}{R_1}$ <--- battery to first resistor, then back to the battery
> Loop 2 - $\epsilon - I_2R_2 = 0 \rightarrow I_2 = \frac{\epsilon}{R_2}$ <--- battery to second resistor, then back to the battery
> Loop 3 - $-I_2R_2 + I_1R_1 = 0$ <--- from top junction through second resistor and then the first resistor, then back to the top junction; current travels against the first resistor
> 
> Thus,
> $I = \frac{\epsilon}{R_1} + \frac{\epsilon}{R_2} = \epsilon\left(\frac{1}{R_1} + \frac{1}{R_2}\right)= \frac{\epsilon}{R_{eq}}$ <--- where $\frac{1}{R_{eq}} = \frac{1}{R_1} + \frac{1}{R_2}$

> [!tip] Equivalent Resistance (Parallel)
> $$\frac{1}{R_{eq}} = \sum \frac{1}{R_i}$$

##### Combination

> ![[2.14.25 Combination Circuit Drawing]]
> 
> Work from the smallest unit of the circuit outward
> 1. Convert the 2 resistors in series into a single resistor (combined resistor is now 2R by using the equivalent resistance formula for series circuits)
> 2. Convert the 2R that we just got with the resistor (R) that is in parallel into a single resistor (combined resistor is now 2/3R by solving for equivalent resistance with the parallel circuits formula)