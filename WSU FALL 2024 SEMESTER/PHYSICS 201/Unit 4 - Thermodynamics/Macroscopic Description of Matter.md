---
tags: PHYSICS_201
created: 2024-11-15
---

**State variable**: describes the state of the system
- Examples: volume, pressure, mass, mass density, thermal energy, moles, number density, temperature

**Thermal equilibrium**: all state variables are constant and not changing

**Number density**: number of molecules divided by the volume

**Atomic mass number**: sum of the number of protons and neutrons

**Atomic mass**: usually the atomic mass number multiplied by the atomic mass units (u)
- The unit is "u" or "g/mol"

**Mole**: the amount of a substance that contains as many molecules as there are atoms in a given mass of an atom with an atomic mass number
- $n = \frac{N}{N_A}$ where $N_A =$ 6.022 $\times$ 10$^23$ molecules/mole (Avogadro's number)

**Molar mass**: mass in grams of 1 mole of a substance
- $m_{mol} = \frac{m}{n}$

> [!example]
> $H_2O \rightarrow m(H_2O) = 2m(^1H) + m(^{16}O) =$ 18 u
> 
> 100 g of $H_2O \rightarrow n = \frac{100}{18} =$ 5.36 mol

### Temperature Scales

|     |  Celsius ($\degree$C)   |  Fahrenheit ($\degree$F)   |  Kelvin (K)   |
| --- | --- | --- | --- |
| Boiling point of water    | 100    |  212   |  373   |
| Freezing point of water    |  0   |  32   |  273   |
| Absolute zero    |  -273   | -460    |  0   |


Conversions:
- Celsius --> Fahrenheit: $T_F = \frac{9}{5}T_C + 32$
- Fahrenheit --> Celsius: $T_C = \frac{5}{9}(T_F - 32)$
- Celsius --> Kelvin: $T_K = T_C + 273$

##### Absolute Zero

![[11.15.24 Absolute Zero Drawing]]

### Phase Diagrams

![[11.15.24 Phase Diagram Graph]]

On the fusion curve, both solid and liquid can coexist.

At the critical point, there is no distinction between a liquid and gas.

At the triple point, all three phases are in equilibrium.

> [!info] Water
> For water, $T =$ 273.16 K and $P =$ 611.2 Pa.

### Ideal Gas Law

> [!tip] Ideal Gas Law Formulas
> 
> $$pV = nRT$$
> 
> where $n$ is the number of moles $R =$ 8.31 J/(mol $\cdot$ k) <---- universal gas constant
> 
> $$pV = Nk_B T$$
> 
> where $N$ is the number of molecules or atoms and $k_B = \frac{R}{N_A} =$ 1.38 $\times$ 10$^{-23}$ J/k (Boltzmann's constant)

^291e1d

##### For constant temperature

> [!tip] Boyle's Law
> 
> $$p_f V_f = p_i V_i$$

When graphing the above law (pressure against volume) you will get hyperbolas called "isotherms" (with constant temperature), and the isotherms closer to the origin have lower temperature and the ones further away has higher temperature.

##### For constant pressure

> [!tip] Charles' Law
> 
> $$\frac{v_f}{T_f} = \frac{v_i}{T_i}$$

When graphing the above law (pressure against volume), you will get a straight horizontal line called an isobar with constant pressure.

##### For constant volume

> [!tip] Gay-Lussac Law
> 
> $$\frac{P_f}{T_f} = \frac{P_i}{T_i}$$

When graphing the above law (pressure against volume), you will get a straight vertical line called an isochoric process.

> [!example]
> ![[11.15.24 IGL Example Graph 1]]
> 
> Known values:
> $n =$ 0.10 mol
> 
> a) What are the temperatures at points 1 and 2?
> $p_1V_1 = nRT_1$
> $T_1 = \frac{p_1V_1}{nR} = \frac{(3)(\frac{101,300}{1})(1000)(\frac{1}{100})^3}{(0.10)(8.31)} =$ 366 K
> 
> $\frac{p_1V_1}{T_1} = nR = \frac{p_2V_2}{T_2}$
> $T_2 = \frac{p_2V_2}{p_1V_1}T_1 = \frac{(1)(3000)}{(3)(1000)}(366) =$ 366 K
> 
> 
> b) The gas undergoes isochoric heating from point 2 to p = 3 atm. What is the final temperature?
> 
> ![[11.15.24 IGL Example Graph 2]]
> 
> $\frac{p_2V_2}{T_2} = \frac{p_3V_3}{T_3}$
> $T_3 = \frac{p_3}{p_2}T_2 = \frac{3}{1}(366) =$ 1098 K