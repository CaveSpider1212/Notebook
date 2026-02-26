---
tags: ENEE_244
created: 2026-2-23
description: 2/23, 2/25 notes (Slide set 7)
---

### Implies and Subsumes

**Implies**: Function `f1` implies `f2` if when `f1` is true, then `f2` is true.

In a sum-of-products expression, any term in it implies the whole function, because if it is true, then the whole function is true. Each term would be called an **implicant**.

K-maps help us determine minimum-size implicants for a function, and a minimum number of such implicants.

**Subsumes**: ("includes") A term `t1` subsumes `t2` if and only if all the literals of `t2` are also in `t1`

### Absorption Law

If one term subsumes another in an expression, then the subsuming (larger) term can be delete from the deleted from the expression without changing the value of the function described.

### Prime implicants

An implicant is called a **prime implicant** if it does not subsume any other implicant with fewer literals of the function.

Any "smallest" implicant is a prime implicant. Maximum-size rectangles in K-maps are prime implicants.

### Prime implicants and minimization

> [!tip] Theorem
> There is always a minimum form of any function `f` which is a sum of prime implicants.
> 
> To search for a minimum form, it is enough to look at prime implicant terms only for inclusion in the result.

**irredundant normal forms**: An irredundant (not redundant) normal form is one which only has prime implicants in it, and no term can be removed without changing the function.

Any K-map result must be an irredundant normal form.

### Why K-maps work

Observation 1: Each maximum-size rectangle is a prime implicant.
- It is an implicant because when it is true, the function is true
- It is a prime implicant because no larger rectangle (implicant with fewer literals) subsumes it

Observation 2: No term can be eliminated from our K-map result since no term subsumes another in the expression (this is because we only choose maximum size rectangles).

In this way, K-maps work, because they make it easy to find the prime implicants, and the minimum number of these prime implicants.

### Uniqueness of K-map results

In general, there can be multiple resulting minimum-size results possible from K-maps.

### Essential Prime Implicants

A prime implicant is **essential** if there exists some minterm in it that is contained in only that prime implicant.

Find all essential prime implicants by drawing all prime implicants and find the cells (on the K-map) covered by only one prime implicant.

### Finding all the minimum formulas

How to generate all possible minimum expressions:
- Essential prime implicants are contained in all minimum expressions (because they are essential)
- Combine a minimum number of non-essential prime implicants in all possible ways to include all the minterms