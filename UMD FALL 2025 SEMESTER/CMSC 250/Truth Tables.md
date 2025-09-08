---
tags: CMSC_250
created: 2025-9-7
description: 9/5 notes
---

**Interpretation** or **Truth valuation**: Assignment of T/F to every variable in a statement

> [!example]
> $p \land q$
> 
> | $p$ | $q$ | $p \land q$
> | - | - | - |
> | 1 | 1 | 1 |
> | 1 | 0 | 0 |
> | 0 | 1 | 0 |
> | 0 | 0 | 0 |

> [!example]
> $p \lor q$
> 
> | $p$ | $q$ | $p \lor q$ |
> | - | - | - |
> | 1 | 1 | 1 |
> | 1 | 0 | 1 |
> | 0 | 1 | 1 |
> | 0 | 0 | 0 |

> [!example]
> $p \hspace{2mm} \land \sim q$
> 
> | $p$ | $q$ | $\sim q$ | $p \hspace{2mm} \land \sim q$ |
> | - | - | - | - |
> | 1 | 1 | 0 | 0 |
> | 1 | 0 | 1 | 1 |
> | 0 | 1 | 0 | 0 |
> | 0 | 0 | 1 | 0 |

> [!example]
> $(p \hspace{2mm} \land \sim r) \lor (p \land r)$
> 
> | $p$ | $r$ | $\sim r$ | $p \hspace{2mm} \land \sim r$ | $p \land r$ | $(p \hspace{2mm} \land \sim r) \lor (p \land r)$ |
> | - | - | - | - | - | - |
> | 1 | 1 | 0 | 0 | 1 | 1 |
> | 1 | 0 | 1 | 1 | 0 | 1 |
> | 0 | 1 | 0 | 0 | 0 | 0 |
> | 0 | 0 | 1 | 0 | 0 | 0 |
> 
> Note: $p$ and $(p \hspace{2mm} \land \sim r) \lor (p \land r)$ are logically equivalent (see below)

> [!example]
> $(p \hspace{2mm} \land \sim r) \lor (q \hspace{2mm} \lor \sim r)$
> 
> | $p$ | $q$ | $r$ | $\sim r$ | $p \hspace{2mm} \land \sim r$ | $q \hspace{2mm} \lor \sim r$ | $(p \hspace{2mm} \land \sim r) \lor (q \hspace{2mm} \lor \sim r)$ |
> | - | - | - | - | - | - | - |
> | 1 | 1 | 1 | 0 | 0 | 1 | 1 |
> | 1 | 1 | 0 | 1 | 1 | 1 | 1 |
> | 1 | 0 | 1 | 0 | 0 | 0 | 0 |
> | 1 | 0 | 0 | 1 | 1 | 1 | 1 |
> | 0 | 1 | 1 | 0 | 0 | 1 | 1 |
> | 0 | 1 | 0 | 1 | 0 | 1 | 1 |
> | 0 | 0 | 1 | 0 | 0 | 0 | 0 |
> | 0 | 0 | 0 | 1 | 0 | 1 | 1 |
> 
> Note: $q \hspace{2mm} \lor \sim r$ and $(p \hspace{2mm} \land \sim r) \lor (q \hspace{2mm} \lor \sim r)$ are logically equivalent (see below)

Note: Truth table columns should be in alphabetical order, and should follow the pattern of 1 true, 1 false alternating in the inner-most column to 2 true, 2 false alternating, to 4 true, 4 false alternating, and so on

> [!info] Logical Equivalence
> Two statements are **logically equivalent** if they have the same truth values for every possible interpretation
> $$p \equiv \hspace{2mm} \sim \sim p$$

> [!info] Tautology and Contradiction
> **Tautology**: Statement that is true under every possible interpretation
> $$p \hspace{2mm} \lor \sim p$$
> 
> **Contradiction**: Statement that is false under every possible interpretation
> $$p \hspace{2mm} \land \sim p$$

![[9.7.25 Laws of Equivalence.png]]

> [!example]
> Prove that $\sim (\sim p \land q) \land (p \hspace{2mm} \lor \sim q) \equiv p \hspace{2mm} \lor \sim q$.
> 
> $\sim (\sim p \land q) \land (p \hspace{2mm} \lor \sim q) \equiv (\sim \sim p \hspace{2mm} \land \sim q) \land (p \hspace{2mm} \lor \sim q)$ <--- *DeMorgan's Law*
> $\hspace{50.3mm} \equiv p \hspace{2mm} \lor \sim q \land p \hspace{2mm} \lor \sim q$ <--- *Double Negative Law*
> $\hspace{50.3mm} \equiv p \hspace{2mm} \lor \sim q$ <--- *Idempotent Law*

> [!example]
> Prove that $\sim (p \hspace{2mm} \lor \sim q) \lor (\sim q \hspace{2mm} \land \sim p) \equiv \hspace{2mm} \sim p$.
> 
> $\sim (p \hspace{2mm} \lor \sim q) \lor (\sim q \hspace{2mm} \land \sim p) \equiv (\sim p \hspace{2mm} \land \sim \sim q) \lor (\sim q \hspace{2mm} \land \sim p)$ <--- *DeMorgan's Law*
> $\hspace{56.8mm} \equiv (\sim p \land q) \lor (\sim q \hspace{2mm} \land \sim p)$ <--- *Double Negative Law*
> $\hspace{56.8mm} \equiv (\sim p \land q) \lor (\sim p \hspace{2mm} \land \sim q)$ <--- *Commutative Law*
> $\hspace{56.8mm} \equiv \sim p \land (q \hspace{2mm} \lor \sim q)$ <--- *Distributive Law*
> $\hspace{56.8mm} \equiv \sim p \land \text{Tautology}$ <--- *Negation Law*
> $\hspace{56.8mm} \equiv \sim p$ <--- *Identity Law*