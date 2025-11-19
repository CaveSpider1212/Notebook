---
tags: CHEM_134
created: 2025-10-7
description: 10/7 notes
---

> [!info] Dynamic Equilibrium
> **Dynamic equilibrium** is where the forward rate of reaction is equal to the reverse rate of reaction, and the concentrations of the reactants and products are constant.
> 
> We can calculate the equilibrium concentrations using the [[Kinetics#^cb4d11|equilibrium constant]], $K$.

### Equilibrium Constant

$K$ is always positive, but:
- If $K$ is close to 0 (for example, $10^{-30}$), then the reactants are favored in the reaction, and the forward reaction essentially doesn't proceed.
- If $K$ is very large (for example, $10^{30}$), then the products are favored in the reaction, and the reaction is essentially irreversible (reactant concentrations are negligible)

$K$ has no units, but is calculated with either Molarity (M) for chemical reactions in solutions or pressure (atm) with gases.

> [!info] Reverse Reactions
> $K_{\text{rev}}$ and $K_{\text{for}}$ are inverses. This means that if:
> 
> $$K_{\text{for}} = \frac{[C]^c}{[A]^a [B]^b}$$
> 
> then:
> 
> $$K_{\text{rev}} = \frac{[A]^a [B]^b}{[C]^c}$$

> [!info] Changing Coefficients in Reactions
> If the coefficients in the reaction were to be multiplied in the reaction by $n$, take the old equilibrium constant $K$ to the power of $n$
> 
> This means that if we have a reaction $A + 2B \rightleftharpoons 3C$ with equilibrium constant:
> 
> $$K = \frac{[C]^3}{[A] [B]^2}$$
> 
> then $nA + 2nB \rightleftharpoons 3nC$ would have an equilibrium constant of:
> 
> $$K' = \frac{[C]^{3n}}{[A]^n [B]^{2n}} = (\frac{[C]^3}{[A] [B]^2})^n = K^n$$

### Heterogeneous Equilibria

> [!info]
> Gases and aqueous substances are always included in the equation for $K$, while liquids and solids are omitted.

### Combining Chemical Equations

When chemical reactions are combined, like below:

$$A \rightleftharpoons 2B$$
$$2B \rightleftharpoons 3C$$
$$\rightarrow A \rightleftharpoons 3C$$

then the equilibrium constant equations (or values) of the individual reactions can be multiplied to get the $K$ equation/value for the combined equation.

> [!example]
> $A(g) + B(g) \rightleftharpoons AB(g)$ -- $K_{C1} =$ 0.24
> $AB(g) + A(g) \rightleftharpoons A_2B(g)$ -- $K_{C2} =$ 3.8
> $2A(g) + B(g) \rightleftharpoons A_2B(g)$ -- $K_{C3} =$ ?
> 
> The $AB(g)$ on the products side of Equation 1 and the reactants side of Equation 2 can be cancelled out, and the $A(g)$ in the reactants of both Equation 1 and 2 can be added together.
> 
> The 2 $A(g)$ and 1 $B(g)$ are still there in the reactants sides of the equations, and the $A_2B(g)$ is still there on the products side, and Equations 1 and 2 can be added together to get Equation 3, so the $K_C$ values can be multiplied.
> 
> $K_{C3} = K_{C1} \times K_{C2} = 0.24 \times 3.8 =$ 0.912

### $K_P$

> [!info] $K_P$
> $$K_P = \frac{P_C^c P_D^d}{P_A^a P_B^b}$$
> 
> where $A$ and $B$ are reactants, $C$ and $D$ are the products, and $a, b, c, d$ are the coefficients.
> 
> Note: $K_P$ is not necessarily equal to $K_C$
> 
> $$K_P = K_C (RT)^{c + d - (a + b)}$$

Note: $K_P = K_C$ when $(RT)^{c + d - (a + b)} = 0$, so either the temperature needs to be 0 or there needs to be no change in the moles of gas between the products and reactants in the equation.

### Unknown $K$

If we have initial concentrations and one equilibrium concentration, we can use ICE (initial, change, equilibrium) tables to determine the equilibrium constants and find $K$ from there. ^63aca6

Find the change between the equilibrium concentration and the initial, and then use the concentration of that and other reactants/products as well as whether they are being used or produced to find the other change values.

> [!example]
> $$A(g) \rightleftharpoons 2B(g)$$
> 
> If we have 1.00 M of $A$ and 0 M of $B$ to begin, and end with 0.50 M of $B$, what is the equilibrium constant?
> 
> | |$A$|$2B$
> |-|-|-
> |Initial|1.00 M|0.00 M
> |Change|-(0.25 M)|+2(0.25M)
> |Equilibrium|0.75 M | 0.50 M
> 
> $K = \frac{[B]^2}{[A]} = \frac{(0.50)^2}{0.75} =$ 0.333

### Reaction Quotient

> [!info] Reaction quotient
> The **reaction quotient** ($Q$) helps determine the direction of reaction.
> 
> $$Q = \frac{[C]^c [D]^d}{[A]^a [B]^b}$$
> 
> Although the equation is the same, $Q$ isn't necessarily at equilibrium.

^ac9ee7

If you know $K$, and
- $Q > K$: higher concentration of products, so reaction will go towards reactants (reverse)
- $Q < K$: higher concentration of reactants, so reaction will go towards products (forward)
- $Q = K$: the system is at equilibrium

### Le Chatelier's Principle

The direction a reaction will proceed depends on:
- Concentration: increasing the concentration on one side (reactants or products) pushes the reaction towards the other side, so the reaction rate in that direction is increased
- Temperature
- Pressure and volume (for gases): increased pressure shifts the reaction towards the products, decreased pressure shifts it towards the reactants