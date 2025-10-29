---
tags: CHEM_134
created: 2025-10-28
description: 10/28 notes
---

**Acids**:
- Dissolve in water to produce $H^+$ (or $H_3 O^+$)
- More generally, proton donor

**Bases**:
- Dissolve in water to produce $OH^-$. For example:

$$NaOH (aq) \rightarrow Na^+ (aq) + OH^- (aq)$$

- Note that we say "produce" $OH^-$ or accept protons. Bases do not always contain $OH^-$. For example:

$$NH_3 (aq) + H_2 O (l) \leftrightharpoons NH_4^+ (aq) + OH^-$$

- More generally, proton acceptor

### Strong Acids/Bases

Strong acids and bases dissociate completely.

$$HCl (g) + H_2 O (l) \rightarrow H_3 O^+ (aq) + Cl^- (aq)$$
$$NaOH (aq) \rightarrow Na (aq) + OH (aq)$$

We often denote complete dissociation with a forward arrow when writing the equation.

Example: Hydrochloric acid ($HCl$)

### Weak Acids/Bases

Weak acids and bases exhibit partial dissociation, shown with a double arrow.

Example: acetic acid (found in vinegar)

$$CH_3COOH (aq) + H_2O (l) \leftrightharpoons H_3O^+ (aq) + CH_3COO^- (aq)$$

Another important weak acid is hydrofluoric acid ($HF$).

$$HF (aq) + H_2O (l) \leftrightharpoons H_3O^+ (aq) + F- (aq)$$

Weak bases accept protons, but not completely. There is an equilibrium between the base and the protonated base (conjugate acid).

Example: Ammonia ($NH_3$)

$$NH_3 (aq) + H_2 O (l) \leftrightharpoons NH_4^+ (aq) + OH^- (aq)$$

### Neutralization

A solution can't be both acidic and basic. The combination of hydronium and hydroxide will result in neutralization. The following shows the reaction between hydrochloric acid and sodium hydroxide:

$$H^+ (aq) + Cl^- (aq) + Na^+ (aq) + OH^- (aq) \leftrightharpoons Na^+ (aq) + Cl^- (aq) + H_2O (l)$$

The sodium and chloride ions remain unchanged, so we cancel them out:

$$H_2O^+ (aq) + OH^- (aq) \leftrightharpoons 2H_2O (l)$$

Neutralization reactions are highly exothermic.

### Water

Water can act as *both* an acid and a base, depending on what other reactants are present.

In the following reaction, water acts as an acid:
$$NH_3 (aq) + H_2O (l) \leftrightharpoons NH_4^+ (aq) + OH^- (aq)$$

$NH_3$ is the base and $H_2O$ is the acid, while $NH_4^+$ is the conjugate acid and $OH^-$ is the conjugate base.

In the following reaction, water acts as a base:
$$H_2 SO_4 (aq) + H_2 O (l) \rightarrow HSO_4^- (aq) + H_3O^+ (aq)$$

$H_2 SO_4$ is the acid and $H_2O$ is the base, while $HSO_4^-$ is the conjugate base and $H_3O^+$ is the conjugate acid.

Note that every base and acid have a conjugate acid and conjugate base respectively. The conjugate base of an acid is the acid with one proton removed, while the conjugate acid of a base is the base with an extra proton.

### Water Equilibrium

Even in pure water, without an acid or base present, water dissociates slightly into hydronium and hydroxide ions. It acts as both acid and base with itself, which is called **autoionization**.

$$2H_2O (l) \leftrightharpoons H_3O^+ (aq) + OH^- (aq)$$

The equilibrium is described with the equilibrium constant $K_w$, also called the *ion dissociation product constant*.

$$K_w = 1 \times 10^{-14} = [H_3O^+] [OH^-]$$

For pure neutral water, the hydronium and hydroxide concentrations must be equal:

$$[H_3O^+] = [OH^-] = \sqrt{1 \times 10^{-14}} = 1 \times 10^{-7} M$$

When we have an acidic or basic solution *in the presence of water*, we will always have *both* hydronium and hydroxide ions present. It is just the relative amounts that will change depending on the acidity or basicity of the solution. For *aqueous solutions*, we can use $K_w$ to calculate the concentration of hydronium from hydroxide ion concentrations, or vice versa.

$$\frac{K_w}{[H_3 O^+]} = [OH^-]$$
$$\frac{K_w}{[OH^-]} = [H_3O^+]$$

- As $[H_3O^+]$ goes up, $[OH^-]$ goes down
- For pure water or neutral solutions, $[H_3O^+] = [OH^-]$
- For acidic solutions, $[H_3O^+] > [OH^-]$
- For basic solutions, $[OH^-] > [H_3O^+]$

### Calculating Equilibrium Concentrations

If you're given a balanced chemical equation, values for $K$ and *initial* concentrations, but *no* equilibrium concentrations:
1. Make an [[Equilibrium#^63aca6| ICE table]] with the given initial concentrations.
2. We don't know the change, but we know how much $A$ and $B$ change relative to each other, which we write as multiples of $x$ (Compare $Q$ to $K$ to figure out if reactants and products are increasing or decreasing)
3. Add up the initial and the change to get equilibrium values in terms of $x$.

> $$A(g) \leftrightharpoons 2B (g)$$
> $$K_c = 0.33$$
> 
> | |$[A]$|$[B]$
> |-|-|-
> |Initial|1.00|0.00
> |Change|$-x$|$+2(x)$
> |Equilibrium|$1.0 - x$|$2x$

$$K_c = \frac{[B]^2}{[A]} = \frac{(2x)^2}{1.0 - x} = 0.33$$
$$4x^2 + 0.33x - 0.33 = 0$$

We often need to use the quadratic formula to get $x$.

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

### Equilibrium of Weak Acids and Bases

$K_a$ and $K_b$ are the equilibrium constants used for acids and bases, respectively.

A common way of characterizing an acid or a base is with $pK_a$ and $pK_b$:

$$pK_a = -\log{K_a}$$
$$pK_b = -\log{K_b}$$

The lower the $pK_a$ (or $pK_b$) is, the more acid (or basic) the acid (or base) is.

### pH and pOH

$K_a$ and $K_b$, as well as $pK_a$ and $pK_b$ describe an acid or base's strength. $pH$ is used to describe the acidity or basicity of a *solution*

$$pH = -\log{[H_3O^+]}$$

If $pH < 7$, then the solution is acidic.
If $pH > 7$, then the solution is basic.
If $pH = 7$, then the solution is neutral.

$$pOH = -\log{[OH^-]}$$
$$pH + pOH = 14.00$$

The above makes sense because $[H_3O^+] [OH^-] = 1 \times 10^{-14}$.