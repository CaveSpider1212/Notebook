---
tags: PHYSICS_202
created: 2025-1-10
---

> [!tip] Electric Fields (for point charges)
> $$\vec{E} = \frac{\vec{F}}{q} = \frac{1}{4\pi \epsilon_o} \frac{q}{r^2} \hat{r}$$
> 
> $\hat{r}$: unit vector pointing away from the charge $q$
> 
> Note: the electric field points towards negative charges, but away from positive charges

### Dipole

> [!example]
> ![[1.10.25 Dipole Drawing]]
> 
> What are the electric fields at the two points?
> 
> On dipole axis:
> ![[1.10.25 Dipole Axis Drawing]]
> 
> $\vec{E} = \vec{E}_+ + \vec{E}_-$
> $\hspace{4.5mm} = \frac{1}{4\pi \epsilon_o} \frac{q}{(y - \frac{s}{2})^2}\hat{j} + \frac{1}{4\pi \epsilon} \frac{q}{(y + \frac{s}{2})^2} (-\hat{j})$
> $\hspace{4.5mm} = \frac{q}{4\pi\epsilon_o} \frac{(y + \frac{s}{2})^2 - (y - \frac{s}{2})^2}{(y - \frac{s}{2})^2 (y + \frac{s}{2})^2} \hat{j}$
> $\hspace{4.5mm} = \frac{q}{4\pi\epsilon_o} \frac{2ys}{(y - \frac{s}{2})^2 (y + \frac{s}{2})^2} \hat{j}$
> 
> For $y >> s$, $y \pm \frac{s}{2} \approx y$
> 
> $\vec{E} = \frac{q}{4\pi\epsilon} \frac{2ys}{y^4} \hat{j} = \frac{1}{4\pi\epsilon} \frac{2qs}{y^3} \hat{j}$
> 
> Define the dipole moment:
> $\vec{p} = qs$ from the negative to positive charge (this would be $\hat{j}$ in this case).
> 
> Therefore,
> $\vec{E} = \frac{1}{4\pi\epsilon} \frac{2\vec{p}}{r^3}$

### Perpendicular to Dipole

> [!example]
> ![[1.10.25 Perpendicular Drawing]]
> 
> $\hat{E} = \hat{E}_+ + \hat{E}_-$
> $\hspace{4.5mm} = \frac{1}{4\pi\epsilon} \frac{q}{(x^2 + (\frac{s}{2})^2)} (\cos\theta \hat{i} - \sin\theta \hat{j}) + \frac{1}{4\pi\epsilon} \frac{q}{(x^2 + (\frac{s}{2})^2)} (-\cos\theta \hat{i} - \sin\theta \hat{j})$
> $\hspace{4.5mm} = \frac{-q}{4\pi\epsilon} \left(\frac{2}{x^2 + (\frac{s}{2})^2}\right)\sin\theta \hat{j}$
> $\hspace{4.5mm} = \frac{-q}{4\pi\epsilon} \left(\frac{2}{x^2 + (\frac{s}{2})^2}\right)\frac{\frac{s}{2}}{\sqrt{x^2 + (\frac{s}{2})^2}} \hat{j}$
> 
> For $x >> s$, $x^2 + (\frac{s}{2})^2 \approx x^2$
> 
> $\hat{E} = -\frac{1}{4\pi\epsilon} \frac{qs}{x^3} \hat{j} = -\frac{1}{4\pi\epsilon_o} \frac{\vec{p}}{r^3}$

### Infinite Line of Charge

> [!example]
> ![[1.10.25 Infinite Charge Drawing]]
> 
> What is the electric field for a line bisecting the charged line?
> 
> $\hat{E} = \frac{1}{4\pi\epsilon} \sum\limits_{i} \frac{q_i}{r_i^2} \hat{r}_i$
> $\displaystyle \rightarrow \frac{1}{4\pi\epsilon} \int \frac{dq}{r^2}\hat{r}$ <----- where $\frac{dq}{Q} = \frac{dy}{L}$
> $r = \sqrt{y^2 + d^2}$
> $\hat{r} = \cos\theta\hat{i} + \sin\theta\hat{j}$ <---- $\sin\theta\hat{j}$ is 0 by symmetry
> $\cos\theta = \frac{d}{r} = \frac{d}{\sqrt{y^2 + d^2}}$
> 
> $\hat{E} = \displaystyle \frac{1}{4\pi\epsilon} \int \frac{(\frac{Q}{L})dy}{y^2 + d^2} \frac{d}{\sqrt{y^2 + d^2}} \hat{i}$
> $\hspace{4.5mm} = \frac{\left(\frac{Q}{L}\right)d}{4\pi\epsilon} \int_{\frac{-L}{2}}^{\frac{L}{2}} \frac{1}{(y^2 + d^2)^{\frac{3}{2}}} dy \hat{i}$
> $\hspace{4.5mm} = \frac{1}{4\pi\epsilon_o} \frac{Q}{d \sqrt{(\frac{L}{2})^2 + d^2}} \hat{i}$ <---- for a finite line
> 
> For an infinite line $L \rightarrow \infty$,
> $\hat{E} = \frac{1}{4\pi\epsilon_o} \frac{Q}{d(\frac{L}{2})} \hat{i}$
> 
> Define linear charge density, $\lambda = \frac{Q}{L}$
> $\hat{E} = \frac{1}{4\pi\epsilon_o} \frac{2\lambda}{d} \hat{i}$

### Electric Field Lines

![[1.15.25 Electric Field Drawing]]

> [!tip] Properties of Electric Field Lines
> 1. Electric field lines are continuous curves drawn tangent to the electric field vectors.
> 2. Closely spaced field lines represent larger field strength.
> 3. Electric field lines never cross.
> 4. Electric field lines start from positive charges and end on negative charges.

> Single charge:
> ![[1.15.25 Single Charge Electric Field]]

> Two equal charges:
> ![[1.15.25 Two Equal Charges Electric Field]]