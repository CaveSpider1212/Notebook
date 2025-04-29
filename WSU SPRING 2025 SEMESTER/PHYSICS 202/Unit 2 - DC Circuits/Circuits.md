---
tags: PHYSICS_202
created: 2025-2-14
---

### Kirchhoff's Laws

> [!info] Kirchhoff's Laws
> 1. Junction: $\sum I_{in} = \sum I_{out}$
> 2. Loop: $\Delta V_{loop} = 0$

> For ideal batteries or capacitors -
> 
> If the travel of the loop is from the negative to positive end of the battery/capacitor:
> $\Delta V = \epsilon$ (batteries) or $\Delta V = \frac{Q}{C}$ (capacitors)
> 
> If the travel of the loop is from the positive to negative end of the battery/capacitor:
> $\Delta V = -\epsilon$ (batteries) or $\Delta V = \frac{-Q}{C}$ (capacitors)

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

### Examples

> [!example]
> ![[2.19.25 Example Circuit]]
> 
> Known values:
> $V_1$: 1.5 V
> $V_2$: 1.5 V
> $R_1$: 48 $\ohm$
> $R_2$: 220 $\ohm$
> $R_3$: 90 $\ohm$
> $R_4$: 100 $\ohm$
> $R_5$: 160 $\ohm$
> 
> Junction Law:
> $I_1 = I_2 + I_3$
> 
> Loop Law:
> 1) $1.5 - I_1(48) - I_3(90) - I_1(100) = 0$
> 2) $1.5 - I_2(160) + I_3(90) - I_2(220) = 0$
> 3) $1.5 - I_1(48) - I_2(220) + 1.5 - I_2(160) - I_1(100) = 0$
> 
> After using algebra to solve for the currents:
> $I_1 =$ 0.0080 A
> $I_2 =$ 0.0048 A
> $I_3 = I_1 - I_2 =$ 0.0032 A

### Meters

##### Ammeter

- Measures current
- Always go in series (because in series the current is always the same)
- They have very low resistance.
	- Low-resistance shunt connected in parallel with the galvanometer and the galvanometer resistor

##### Voltmeter

- Measures voltage drop
- Always go in parallel (because in parallel the voltage is always the same)
- They have a very high resistance.
	- High-resistance shunt connected in series with the galvanometer and the galvanometer resistor

##### Ohmmeter

- Measures resistance
- Circuit should be disconnected first
	- Circuit includes the battery this time (unlike with voltmeter and ammeter)

### Real Batteries

While ideal batteries have no resistance (so their change in potential, $\Delta V$, is equal to the voltage), real batteries have internal resistance (so $\Delta V = \epsilon - \text{IR}$)

> [!example]
> There is a real battery with voltage 9.0 V and internal resistance 1.0 $\ohm$ connected in series to an external resistor of resistance $R$. For what value of the resistance will the power dissipated by the load resistor will be maximum?
> 
> The current on the circuit is:
> $I = \frac{\epsilon}{r + R}$
> 
> The power dissipated by the resistor is:
> $P = I^2R = \frac{\epsilon^2 R}{(r + R)^2}$
> 
> The maximum power dissipated occurs with:
> $\frac{dP}{dR} = \frac{\epsilon^2}{(r + R)^2} - \frac{2 \epsilon^2 R}{(r + R)^3} = 0$
> $\frac{\epsilon^2 (r + R) - 2 \epsilon^2 R}{(r + R)^3} = 0$
> $r + R - 2R = 0$
> $R = r =$ 1.0 $\ohm$

### Grounded Circuits

![[2.19.25 Grounded Circuit]]

Grounding does not affect the circuit for one ground.

> [!example]
> ![[2.19.25 Grounded Circuit Example]]
> 
> Top resistor: 2 $\ohm$
> Bottom resistor: 4 $\ohm$
> Left battery: 9 V
> Right battery: 3 V
> 
> What is the current?
> 
> Junction Law:
> $I_2 + I_3 = I_1$
> 
> Loop Law:
> 1) $9 - I_1(2) - 3 - I_2(4) = 0$
> 2) $9 - I_1(2) - 3 = 0$
> 3) $I_2(4) = 0 \rightarrow I_2 = 0$
> 
> $I_1 =$ 3 A
> $I_3 =$ 3 A

### Discharge a Capacitor

> ![[2.21.25 Discharge Capacitor.png]]
> 
> Loop Law:
> $\Delta V_R + \Delta V_C = 0$
> $\rightarrow IR + \frac{Q}{C} = 0$
> $\rightarrow (-\frac{dQ}{dt})R + \frac{Q}{C} = 0$
> $\rightarrow{dQ}{dt} = \frac{-Q}{RC}$
> $\int_{Q_0}^{Q} \frac{dQ}{Q} = \int_0^t -\frac{dt}{RC}$
> $\ln Q ]_{Q_0}^{Q} = \frac{-t}{RC} ]_{0}^{t}$
> $\ln\left(\frac{Q}{Q_0}\right)= \frac{-t}{RC}$
> $Q = Q_0 e^{\frac{-t}{RC}}$
> 
> Time constant $\tau = RC$:
> $Q = Q_0 e^{\frac{-t}{\tau}}$
> 
> The current is:
> $I = \frac{-dQ}{dt} = \frac{Q_0}{RC} e^{\frac{-t}{RC}}$

### Charge a Capacitor

> ![[2.21.25 Charge Capacitor.png]]
> 
> Loop Law:
> $\Delta V_C + \epsilon + \Delta V_R = 0$
> $\frac{-Q}{C} + \epsilon - IR = 0$
> $\frac{-Q}{C} + \epsilon - (+\frac{dQ}{dt})R = 0$
> $\frac{dQ}{dt} = \frac{-Q}{RC} + \frac{\epsilon}{R}$
> $Q = C \epsilon (1 - e^{\frac{-t}{RC}})$
> $\hspace{5mm} = Q_{max} (1 - e^{\frac{-t}{\tau}})$
> 
> The current is given by:
> $I = \frac{dQ}{dt} = \frac{C\epsilon}{RC} e^{\frac{-t}{RC}}$

> [!example]
> ![[2.21.25 Capacitor Example.png]]
> 
> a) The switch is closed for a very long time. What is the charge of the capacitor?
> 
> Junction Law:
> $I_1 = I_2 + I_3$ <---- current by a long time??....also $I_3$ is 0 since the capacitor is considered as an open circuit if it is fully charged
> 
> Loop Law:
> 1. $100 - I_1(60) - I_2(40) = 0$
> 2. $100 - I_1(60) - I_3(10) - \frac{Q}{C} = 0$
> 3. $-I_3(10) - \frac{Q}{C} + I_2(40) = 0$
> 
> Loop 1 - $100 - I_1(60) - I_1(40) = 0$
>    $\rightarrow I_1(100) = 100$
>    $I_1 =$ 1.0 A
>    
> Loop 2 -$\frac{-Q}{C} + I_1(40) = 0$
>    $\rightarrow Q = I_1(40)C$
>    $\hspace{11mm} = (1.0)(40)(2.0 \times 10^{-6})$
>    $\hspace{11mm} =$ 80 x 10^-6 C = 80 $\micro$C
> 
> b) The switch is opened at t = 0 s. At what time has the charge decreased to 10% of its initial value
> 
> Charge on capacitor:
> $Q = Q_0 e^{\frac{-t}{RC}}$
> $t = RC \ln(\frac{Q}{Q_0})$
> $\hspace{3mm} = -(50)(2.0 \times 10^{-6})\ln(0.1 \frac{Q}{Q_0})$ <--- 10 $\ohm$ + 40 $\ohm$ = 50 $\ohm$
> $\hspace{3mm} =$ 2.3 x 10^-4 s = 0.23 ms
> 
> c) What is the current at this time?
> 
> $I = I_0 e^{\frac{-t}{Rc}}$
> $\hspace{4mm} = \frac{\Delta V}{R} e^{\frac{-t}{RC}}$ <---- $\Delta V = \frac{Q}{C} =$ 40 V
> $\hspace{4mm} = \frac{40}{50} e^{\frac{-2.3 \times 10^{-4}}{(80)(2.0 \times 10^{-6})}}$
> $\hspace{4mm} =$ 0.08 A = 80 mA
> 
> d) At this time how much power is dissipated by the resistors?
> 
> $P = I^2 R = (0.08)^2 (50) =$ 0.32 W
> 
> e) At this time how much power is being supplied by the capacitor?
> 
> $P = \frac{du}{dt}$
> $\hspace{4mm} = \frac{d}{dt}(\frac{Q^2}{2C})$
> $\hspace{4mm} = \frac{1}{2C} \frac{d}{dt} Q^2$
> $\hspace{4mm} = \frac{1}{2C} (2Q \frac{dQ}{dt})$
> $\hspace{4mm} = \frac{Q}{C}I$
> $\hspace{4mm} = \frac{8.0 \times 10^{-6}}{2.0 \times 10^{-6}} (0.08)$
> $\hspace{4mm} =$ 0.32 W

> [!info] Capacitors in a Steady-State Circuit (Relating to Open/Closed Switches)
> After the switch has been open or closed for a long time, the capacitors serve as open circuits once they are fully charged, so no current flows through them.
> 
> Note: The voltage drops across the capacitor may be different when the switch has been open or closed for a long time.
> 
> Note: The voltage drop is also 0 as soon as the switch is closed since the capacitor would initially have no charge (it charges over time).