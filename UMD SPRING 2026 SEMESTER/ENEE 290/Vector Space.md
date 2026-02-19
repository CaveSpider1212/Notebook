---
tags: ENEE_290
created: 2026-2-18
description: 2/18 notes (Lecture 7)
---

### Field

> [!info] Field
> A **field** $F$ is a set on which two operations (addition and multiplication) are defined so that for each pair of elements $x, y \in F$, there are unique elements $x + y$ and $x \cdot y$ in $F$, which satisfy the following conditions for all $a, b, c \in F$:
> 1. Commutativity
> 2. Associativity
> 3. Identity element
> 4. Inverse element
> 5. Distributing multiplication over addition

Elements of a field are called **scalars**.

### Vector Space

> [!info] Vector Space
> A **vector space** over a field $F$ is a set $V$ along with two operations (vector addition and scalar multiplication), which satisfy the following:
> 1. Closed under vector addition ($v + w \in V$ for all $v, w \in V$)
> 2. Vector addition is commutative
> 3. Vector addition is associative
> 4. There is a "zero vector" $0 \in V$ such that $v + 0 = v$
> 5. Each element $v \in V$ has additive inverse $w \in V$, i.e. $v + w = 0$
> 6. Closed under scalar multiplication ($r \cdot v \in V$)
> 7. Addition of scalars distributes over scalar multiplication
> 8. Scalar multiplication distributes over vector addition
> 9. Ordinary multiplication of scalars associates with scalar multiplication
> 10. Multiplication by the scalar 1 is the identity operation
> 
> \#1 and \#6 are the most important ones.

Additional properties of vector spaces $V$ over field $F$:
- The zero vector $0$ is unique
- $0u = 0$ for all $u \in V$
- $k0 = 0$ for all scalars $k \in F$
- The additive inverse of each element $u \in V$, denoted by $-u$, is unique
- For all $u \in V$, $-u = (-1)u$, where -1 is the additive inverse of the multiplicative identity in the field $F$
- If $k$ is a scalar in $F$ and $u \in V$ such that $ku = 0$, then either $k = 0$ or $u = 0$

