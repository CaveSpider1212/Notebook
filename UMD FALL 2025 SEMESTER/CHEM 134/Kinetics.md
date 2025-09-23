---
tags: CHEM_134
created: 2025-9-23
description: 9/23 notes
---

### Defining Kinetics and Thermodynamics

**Thermodynamics** gives us information about the energy of our initial and final states, as well as spontaneity of the reaction (Gibbs free energy, $\Delta G \degree = -RT \ln{K}$, negative means more spontaneous).

**Kinetics** tells us about the intermediate states and speed of the reaction.

### Dynamic Equilibrium

The reaction is in equilibrium when the concentrations of the products and reactants "level out" over time (i.e. neither is increasing or decreasing).

$$K = \frac{[C]^c [D]^d}{[A]^a [B]^b}$$

### Collision Model

For reactions to occur, reactants need to:
1. Collide
2. Collide with enough energy
3. Collide at the right orientation

To increase the rate of reaction:
- Increase concentration of reactants (more collisions)
- Increase the temperature (more thermal energy)
- Select appropriate reactants (control structure, orientation)
- Add a catalyst (reduce energetic barrier)

### Kinetics and Rates of Reaction

> [!tip] Rate of Reaction
> $$\text{Rate} = \frac{\pm \Delta [A]}{x \Delta t}$$
> 
> Note: + if the product is being formed, - if the reactant is being used
> $x$ is the number of moles of substance $A$

### Rate Laws and Reaction Order

Rates depend on concentration of reactants but how it is must be experimentally determined.

> [!info] Rate Law
> $$\text{Rate} = k[A]^n$$
> 
> $k$: rate constant
> $A$: reactant
> $n$: rate order (0, 1, 2, also possibly noninteger)

### Using Initial Rates to Determine Reaction Order

**1st order reactions**: When the concentration of a reactant is doubled, the initial rate also doubles (rate of change of initial rate is the same as the rate of change of concentration)

**2nd order reaction**: When the concentration of a reactant is doubled, the initial rate is multiplied by 4 (rate of change of initial rate is double the rate of change of concentration)

**Zero order reaction**: When the concentration of a reactant is doubled, the initial rate stays the same (rate of change of initial rate is 0)

Substitute initial rate for "$\text{Rate}$", reactant concentration for $[A]$, and reaction order for $n$ to solve for $k$ in the Rate Law.

### Integrated Rate Law

Found using calculus/integration

> [!info] Integrated Rate Laws
> Zero order: $[A]_t = -kt + [A]_0$
> 1st order: $\ln{[A]_t} = -kt + \ln{[A]_0}$
> 2nd order: $\frac{1}{[A]_t} = kt + \frac{1}{[A]_0}$

If you were to plot any of the concentration terms ($[A]$, $\ln{[A]}$, $\frac{1}{[A]_0}$), whichever graph is linear corresponds with the order of the reaction.

### Half-Life

**Half-life** is the time for a substance to reach half of its original concentration

> [!tip] Half-Life of 1st Order Reaction
> $$t_{\frac{1}{2}} = \frac{0.693}{k}$$

### Arrhenius Equation

> [!tip] Arrhenius Equation
> $$k = A e^{\frac{-E_a}{RT}}$$
> 
> $R$: gas constant (J/mol\*K)
> $T$: temperature (K)
> $A$: frequency factor
> $E_a$: activation energy (J)

**Activation energy** is the energetic barrier to reach the transition state (high energy, short-lived) of reactants. A higher activation energy means a slower reaction (and also decreases $e^{\frac{-E_a}{RT}}$)

Higher temperatures lead to a faster reaction (likely due to more energy), and $e^{\frac{-E_a}{RT}}$ increases.