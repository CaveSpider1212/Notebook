---
tags: CMSC_250
created: 2025-9-8
description: 9/8 notes
---

> [!info] Argument
> If you make certain assumptions ("premises"), then a particular statement ("conclusion") must logically follow.
> 
> Valid when every interpretation that makes all of the premises true also makes the conclusion true.

Process:
1. Find the "critical rows", which are the rows/interpretations where all of the premises are true
2. For each critical row, see if the conclusion is also true for that same row/interpretation
3. If the conclusion is true, then the argument is valid (for that interpretation)

> [!example]
> Premises: $p \lor q$ and $q \rightarrow r$
> Conclusion: $p \lor r$
> Is the argument valid?
> 
> |$p$|$q$|$r$|$p \lor q$|$q \rightarrow r$|$p \lor r$
> |-|-|-|-|-|-
> |1|1|1|1|1|1
> |1|1|0|1|0|1
> |1|0|1|1|1|1
> |1|0|1|1|1|1
> |0|1|1|1|1|1
> |0|1|0|1|0|0
> |0|0|1|0|1|1
> |0|0|0|0|1|0
> 
> Rows 1, 3, 4, and 5 are the critical rows, and the conclusion is true for all of them, so the argument is valid for all of those 4 rows/interpretations.

### Proving Arguments

> [!tip] Rules of Inference
> Simple arguments that are known to be valid and used to prove the validity of more complex arguments.
> 
> ![[9.8.25 Rules of Inference.png]]

**Proof**: Sequence of statements, beginning with the premises, where each subsequent statement must follow the previous one, using the [[Truth Tables#^bdfe26|Laws of Equivalence]] and [[9.8.25 Rules of Inference.png|Rules of Inference]].

> [!example]
> Premises:
> $p \lor q$
> $q \rightarrow r$
> $\sim p$
> 
> Conclusion:
> $r$
> 
> Prove this argument.
> 
> |Line|Statement|Rule|Lines Used
> |-|-|-|-
> |P1|$p \lor q$|Given|
> |P2|$q \rightarrow r$|Given|
> |P3|$\sim p$|Given|
> |1|$q$|Elimination|P1, P3
> |2|$r$|Modus Ponens|P2, 1