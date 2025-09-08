---
tags: CMSC_250
created: 2025-9-8
description: 9/8 notes
---

> [!info] Conditional Statement
> $p \rightarrow q$ represents "if $p$ then $q$" or "$p$ implies $q$"
> 
> |$p$|$q$|$p \rightarrow q$
> |-|-|-
> |1|1|1
> |1|0|0
> |0|1|1
> |0|0|1
> 
> $p \rightarrow q$ is only false when the left side ($p$) is true and the right side ($q$) is false.
> 
> Precedence is lower than conjunction/disjunction.
> 
> $$p \rightarrow q \equiv \sim p \lor q$$
> ("Definition of $\rightarrow$", see the [[Truth Tables#^bdfe26|Laws of Equivalence]] chart)

The **converse** of $p \rightarrow q$ is $q \rightarrow p$.

The **inverse** of $p \rightarrow q$ is $\sim p \rightarrow \sim q$.

The **contrapositive** of $p \rightarrow q$ is $\sim q \rightarrow \sim p$.

> [!info] Biconditional Statements
> $p \leftrightarrow q$ represents "$p$ if and only if $q$" or "$p$ implies $q$ and $q$ implies $p$"
> 
> $$p \leftrightarrow q \equiv (p \rightarrow q) \land (q \rightarrow p)$$
> ("Definition of $\leftrightarrow$", see the [[Truth Tables#^bdfe26 | Laws of Equivalence]] chart)
> 
> Note: $p \leftrightarrow q$ means "$p$ and $q$ always agree", i.e. "Both $p$ and $q$ are both true or both false", so:
> 
> $$p \leftrightarrow q \equiv (p \land q) \lor (\sim p \land \sim q)$$
> 
> |$p$|$q$|$p \leftrightarrow q$
> |-|-|-
> |1|1|1
> |1|0|0
> |0|1|0
> |0|0|1