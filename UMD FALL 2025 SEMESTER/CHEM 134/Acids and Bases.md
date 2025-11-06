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

> [!info] Finding $K_a$
> $$HA(aq) \rightarrow H_3O^+(aq) + A^-(aq)$$
> $$K_a = \frac{[H_3O^+] [A^-]}{[HA]}$$

> [!info] Finding $K_b$
> $$B(aq) + H_2O(l) \rightarrow BH^+(aq) + OH^-(aq)$$
> $$K_b = \frac{[BH^+] [OH^-]}{[B]}$$

A common way of characterizing an acid or a base is with $pK_a$ and $pK_b$:

$$pK_a = -\log{K_a}$$
$$pK_b = -\log{K_b}$$

The lower the $pK_a$ (or $pK_b$) is, the more acidic (or basic) the acid (or base) is.

### pH and pOH

$K_a$ and $K_b$, as well as $pK_a$ and $pK_b$ describe an acid or base's strength. $pH$ is used to describe the acidity or basicity of a *solution*

$$pH = -\log{[H_3O^+]}$$

If $pH < 7$, then the solution is acidic.
If $pH > 7$, then the solution is basic.
If $pH = 7$, then the solution is neutral.

$$pOH = -\log{[OH^-]}$$
$$pH + pOH = 14.00$$

The above makes sense because $[H_3O^+] [OH^-] = 1 \times 10^{-14}$.

### Solutions of Strong Acid

For strong acids and bases, we can assume complete dissociation, so this simplifies our calculations. We can simply assume that whatever concentration of strong acid (or base) we have in solution, we have the *same* concentration of hydronium ions (or hydroxide ions).

$$[HA] = [H_3 O^+]$$
$$[HB] = [OH^-]$$

### Salts with Acid-Base Properties: Anions

Salts are composed of ions, and sometimes those ions can act as acids or bases.

Anions can be considered conjugate bases of acids (which is just the acid with the proton removed, not necessarily basic).

One way to tell if an anion acts as a base is to add a proton to the structure, then ask yourself if you have a strong or weak acid (the weaker the acid, the stronger the conjugate base).

If you want to know the $K_b$ of your anion:
1. Add a proton to identify the corresponding acid.
2. Look up the $K_a$ of the corresponding acid, and solve for $K_b$.

$$K_b = \frac{K_w}{K_a} = \frac{1 \times 10^{-14}}{K_a}$$

$$pK_a = -\log K_a$$
$$pK_b = -\log K_b$$
$$pK_a + pK_b = 14$$

Thus, you have two types of anions:
1. Conjugate base of strong acids (like $Cl^-$), which have a neutral contribution to a salt solution. They are not proton acceptors.
2. Conjugate base of weak acids (like $F^-$), which have a basic contribution to a salt solution. They are weak proton acceptors (weakly basic).

Note: For a salt to form a basic solution in water, its anion has to be a conjugate base where it can be used in a basic reaction (making that conjugate base a conjugate acid) that forms $OH^-$.

### Salt with Acid-Base Properties: Cations

Cations can be considered conjugate acids of bases, and can be put into three categories:
1. Counterions of strong bases
2. Conjugate acids of weak bases
3. Small, highly charged metals

##### Counterions of strong bases

The cations (counterions) associated with these strong bases will not ionize water to form hydronium ions, so they have a neutral effect.

##### Conjugate acids of weak bases

If you can take away a proton from the cation and form a weak base, it is generally a weak acid.

##### Small highly charged metals

The smaller and more charged, the more acidic.

The highly charged cations interact strongly with the partial negative charge on water forming a shell of water. The cations draw electron density away from the partial positive charge on the $H$ end of the water. This weakens the $OH$ bond and other water molecules can accept a proton from shell of water.

If the anion is neutral and the cation is acidic, the solution will be acidic. If the cation is neutral and the anion is basic, the solution will be basic. If both ions are acidic or basic, it depends on the relative strength of each. That way, we can determine the $pH$ of the salt solution.

### Predicting Acid Strength

We need to examine both electronegativity and bond strength to predict acid strength.

##### Electronegativity

Electronegativity increases from left to right on the periodic table. The most electronegative conjugate base is the most stable, so the more stable product is favored and the acid will dissociate to form more product, giving us a stronger acid.

Therefore, more electronegative means stronger acid.

##### Bond strength

Bond strength decreases as you go down the periodic table. If bond strength decreases, the proton can be removed more easily, and acid strength increases.

Therefore, the lower you go on the periodic table, the weaker the bond strength, and therefore the stronger the acid.

### Lewis Acids and Bases

The Lewis acid and base definition focuses on the electron pair instead of the proton:
- A Lewis acid accepts an electron pair
- A Lewis base donates an electron pair