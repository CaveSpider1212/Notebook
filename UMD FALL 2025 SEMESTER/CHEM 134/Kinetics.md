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

$$K = \frac{[C]^c [D]^d}{[A]^a [B]^b}$$ ^cb4d11

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

Units of $k$ in a zero-order reaction: M/s
Units of $k$ in a first-order reaction: 1/s
Units of $k$ in a second-order reaction: 1/(Ms)

Plug 0, 1, or 2 into the above equation for $n$ to get these units (note: the rate has units of M/s)

Note: If there are multiple reactants that each have an order, then add up the individual orders to get the overall order of the reaction

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

To find the half-life equation of a zero- or second-order reaction, substitute in $\frac{1}{2} [A]_0$, or half of the initial calculation, for $[A]_t$ in the respective integrated rate law and solve for $t$.

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

The **frequency factor** is the number of approaches to the energy barrier per unit time.

> [!info] Frequency Factor
> $$A = pz$$
> 
> $p$: Steric/orientation factor (between 0 and 1)
> $z$: Collision frequency

### Arrhenius Plot

> [!info]
> $$\ln k = \ln A + \frac{-E_a}{R}(\frac{1}{T})$$
> 
> The equation is written in slope-intercept form, so we can graph $\frac{1}{T}$ (x-axis) against $\ln k$ (y-axis), and the slope would be $\frac{-E_a}{R}$ (since $R$ is a constant, we can calculate the activation energy this way).

> [!tip]
> $$\frac{-E_a}{R} = \frac{\ln(\frac{k_2}{k_1})}{(\frac{1}{T_2} - \frac{1}{T_1})}$$
> 
> We can use this equation to calculate activation energy if we have 2 values of the rate constant and temperature each (or calculate one of those if we have activation energy).

### Reaction Mechanism

The reaction mechanism isn't obvious from the overall reaction equation and requires a sequence of steps (elementary steps).

To get an overall reaction, we need to break it down into **elementary steps** which shows how the reactant molecules and intermediates actually interact, not just how the products end up.

The slow step of a reaction is the one that dictates the rate of reaction.

![[9.30.25 Elementary Steps Table.png]]

If you have the rate law of a reaction, then you can use it to find the first elementary step.

The **intermediate** is the substance/compound that is produced in one elementary step reaction and consumed in another, and doesn't appear in the overall reaction

### Catalysts

**Catalysts** increase the rate of a reaction and are not created or destroyed in the process.

> [!info] Homogeneous Catalysts
> Homogeneous catalysis is when the catalyst and the reactants are in the same phase.
> 
> - Gas phase catalyst combined with gas phase reactants
> - Solution based reaction with both reactants and catalyst in solution
> - Catalysis of ozone depletion is homogeneous

> [!info] Heterogeneous Catalysts
> Heterogeneous catalysis is when the catalysts and reactants are in different phases.
> 
> - Gas phase reaction with a solid surface acting as a catalyst
> - Solution phase reaction (reactants are dissolved solutes) with a solid surface acting as a catalyst

The most common heterogeneous systems are when gases or solutes (in solution) react on a solid surface. These catalyzed reactions proceed through four steps:
- Adsorption: The reactants associate with the surface
- Diffusion: The reactants migrate around the surface
- Reaction: The reactants collide and react
- Desorption: The product desorbs (opposite of adsorbs) and departs from the surface