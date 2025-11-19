---
tags: CHEM_134
created: 2025-11-11
description: 11/11 notes
---

### Redox Reactions

**Electrochemistry** involves the transfer of electrons and involves oxidation-reduction (**redox**) reactions. These are reactions in which one substance loses electrons while one substance gains electrons.

In reduction reactions, electrons are gained.
$$Ag^+ + e^- \rightarrow Ag(s)$$

In oxidation reactions, electrons are lost.
$$Cu(s) \rightarrow Cu^{2+} + 2e^-$$

To make a redox reaction, the number of electrons gained or lost have to be equal, so the $Ag$ reaction above needs to be written as $2Ag^+ + 2e^- \rightarrow 2Ag(s)$.

The overall redox reaction is $2NO_3^- + 2Ag^+ + Cu(s) + 2e^- \rightarrow 2Ag(s) + Cu^{2+} (aq) + 2NO_3^- + 2e^-$. Nitrate $NO_3^-$ is the **spectator ion** in this reaction since it does not undergo reduction or oxidation.

The reducing agent is the substance getting oxidized (copper in the above example), while the oxidizing agent is the substance getting reduced (silver in the above example).

### Galvanic Cells

**Galvanic cells** use a spontaneous redox reaction to generate electricity, requiring a separation of the two half reactions. It consists of an anode and a cathode, as well as a salt bridge.

Oxidation takes place at the anode, while reduction takes place in the cathode. The electrons flow in the direction of reduction (from the reducing agent to the oxidizing agent, or to the cathode).

The salt bridge has electrolytes preventing charge buildup, and neutralizes the solutions.

The correct notation for a galvanic cell is: "Anode | electrolyte of anode || electrolyte of cathode | cathode".

Since electrons flow from the anode to the cathode, that means the anode should be the reactant and the cathode should be the product if we were to make a balanced chemical equation out of a galvanic cell.

### Cell Potential

Electrons flow from a position of higher to lower potential energy. The greater the difference, the greater the tendency for electrons to flow. This difference is the **cell potential**, which depends on relative tendencies for the reactants to become oxidized or reduced.

The cell potential tells us if a redox reaction is spontaneous (positive) or nonspontaneous (negative).

> [!info] Cell Potential
> $$E^{\degree}_{cell} = E^{\degree}_{red} - E^{\degree}_{ox}$$

### Standard Reduction Potentials

> [!info] Reduction Potential
> $$V = \frac{\text{energy}}{\text{charge}}$$

Higher potential means more likely to gain electrons

### Solving for a cell potential for a galvanic cell

1. Figure out the two half-reactions
2. We do not need to balance the electrons or know the number of electrons
3. Find the potentials for the half cells. The larger one is the reduction potential for the cathode, $E^{\degree}_{red}$, while the smaller one is the reduction potential for the anode, $E^{\degree}_{ox}$
4. Calculate $E^{\degree}_{cell}$

### Gibbs Free Energy

Gibbs free energy also tells us how much electrical energy can be supplied by the redox reaction (or how much it requires).

> [!info] Gibbs Free Energy
> $$\Delta G^{\degree} = -RT\ln{K} = -n F E^{\degree}_{cell}$$
> 
> Gibbs free energy ($\Delta G^{\degree}$), cell potential ($E^{\degree}_{cell}$) and the equilibrium constant ($K$) are all related to each other.

A spontaneous reaction or process will perform work, while a nonspontaneous process requires an input of energy to proceed.

The change in Gibbs free energy allows us to predict spontaneity, with a negative value indicating a spontaneous process and a positive value indicating a nonspontaneous process.

The two equations for Gibbs free energy can be set equal to each other to obtain this equation:

$$E^{\degree}_{cell} = \frac{0.0592 V}{n} \log{K}$$

For a spontaneous reaction: $\Delta G^{\degree} < 0$, $E^{\degree} > 0$, and $K > 1$.

### Nernst Equation

Changing the concentrations of the reactants and products so that they are not 1 M will affect the free energy change, $\Delta G$. Similarly, $E_{cell}$, the voltage for the cell, will be different when the ion concentrations are not 1 M. In that case, the system would no longer be in its standard state.

We can use $Q$, the [[Equilibrium#^ac9ee7|reaction quotient]], to predict spontaneity at nonstandard conditions.

To adjust for nonstandard conditions, we add an additional term using $Q$:

$$\Delta G = \Delta G^{\degree} + RT \ln{Q}$$
$$-nFE_{cell} = -nFE^{\degree}_{cell} + RT \ln{Q}$$

> [!info] Nernst Equation
> $$E_{cell} = E^{\degree}_{cell} - \frac{0.0592 V}{n} \log{Q}$$

### Concentration Cells

It is possible to get a spontaneous reaction when the oxidation and reduction reactions are the same, if the electrolyte concentrations are different. Electrons will flow from the electrode in the less concentrated solution to the electrode in the more concentrated solution.

Oxidation of the electrode in the less concentrated solution will increase the ion concentration in the solution, and reduction of the solution ions at the electrode in the more concentrated solution reduces the ion concentration. Eventually the cell will become nonspontaneous when the concentrations become equal in both cells.

The only way to drive electron flow is if the cell potential is positive, and log must be negative for that, so $Q$ must be less than one. Therefore, the lower concentration of ions are treated as the products, and this concentration will increase as the reaction proceeds.

### Electrolysis

In electrolysis, we use electrical energy to overcome the energy barrier of a nonspontaneous reaction, allowing it to occur. The reaction that takes place is the opposite of the spontaneous process.

Electrolysis can be used for fuel cells, metal extraction, etc.

For the reaction to proceed, the compound must be in molten (liquid) state. Cations are reduced at the cathode to the metal elemental form, and anions are oxidized at the anode to nonmetal elemental form. Electrodes are normally graphite.

### Electroplating

Electroplating is when a layer of metal is deposited on a surface.

The amount (mass, in grams) of metal that can be deposited onto a surface can be found if we know the amount of current (in C/s) applied and the time (in seconds) it's applied for, and is given by the following equation:

$$\text{time} \times \text{current} \times \frac{1 \text{mol} \hspace{2mm} e^-}{96485 \text{C}} \times \frac{1 \text{mol metal}}{\text{mol} \hspace{2mm} e^-} \times \text{molar mass} = \text{mass metal}$$

### Batteries: Alkaline Dry Cell

Batteries are a type of voltaic cell. The alkaline dry cell is a common, nonrechargable battery.

**Anode**: Batteries are composed of an inner shell made of $Zn$ or $Mg$, which becomes oxidized.

$$Zn(s) + 2 OH^- (aq) \rightarrow Zn(OH)_2 (s) + 2 e^-$$

**Cathode**: A graphite or brass rod is immersed in $MnO_2$ in a $KOH$ electrolyte paste. $MnO_2$ is reduced.

$$2 MnO_2 (s) + 2 H_2 O (l) + 2 e^- \rightarrow Mn O(OH) (s) + 2 OH^- (aq)$$

### Lithium Ion Batteries

Lithium ion batteries are used in portable electronic devices and electric vehicles, and are rechargeable and have a long life, light weight, and large energy density. However, it could overheat, and there are environmental and human rights issues associated with lithium extraction.

The anode is lithium atom-intercalated graphite. The cathode is a $Li$-transition metal oxide such as cobalt oxide associated with lithium, and the transition metal gets reduced.

Unlike most batteries, $Li$ ion itself migrates from anode to cathode (through an electrolyte) accompanied by a corresponding migration of electrons from anode to cathode.

### Fuel Cells

Instead of a closed compartment like a battery, in a fuel cell, the reactants, $H_2$ and $O_2$, must be constantly added.

The anode and cathode are both $Pt$-coated metal. The electrolyte is an $OH^-$ solution.

Anode reaction: $2 H_2 (g) + 4 OH^- (aq) \rightarrow 4 H_2O (l) + 4 e^-$

Cathode reaction: $O_2 (g) + 2 H_2 O (l) + 4 e^- \rightarrow 4 OH^- (aq)$

Overall reaction: $2 H_2 (g) + O_2 (g) \rightarrow 2 H_2 O (l)$