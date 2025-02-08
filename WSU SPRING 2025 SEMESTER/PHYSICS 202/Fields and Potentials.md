---
tags: PHYSICS_202
created: 2025-2-3
---

$$\Delta V = \frac{\Delta u}{q} = \frac{-W}{q} = -\frac{1}{q} \int_{s_i}^{s_f} \vec{F} \cdot d\vec{s} = -\int_{s_i}^{s_f} \vec{E} \cdot d\vec{s}$$

> [!example]
> The electric field in a region of space is $E_x =$ -10,000x V/m^2. What is the potential difference between $x_i =$ -20 cm and $x_f =$ 30 cm?
> 
> $\Delta V = -\int_{s_i}^{s_f} \vec{E} \cdot d\vec{s}$
> $\hspace{9mm} = -\int_{x_i}^{x_f} (-10,000x)dx$
> $\hspace{9mm} = -(-5000x^2) |_{x_i}^{x_f}$
> $\hspace{9mm} = 5000(x_f^2 - x_i^2)$
> $\hspace{9mm} = 5000((0.30)^2 - (-0.20)^2)$
> $\hspace{9mm} =$ 250 V

> [!example]
> An infinitely long cylinder of radius $R$ has linear charge density $\lambda$. Find the potential relative to the surface at a point that is a distance $r$ from the axis, assuming $r > R$.
> 
> By Gauss's Law:
> $\oint \vec{E} \cdot d\vec{a} = \frac{Q_{in}}{\epsilon_0}$
> $EA = \frac{Q_{in}}{\epsilon_0}$
> $E(2\pi rL) = \frac{Q}{\epsilon_0}$
> $E = \frac{Q}{2\pi\epsilon_0 rL} = \frac{\lambda}{2\pi\epsilon_0 r}$ <---- where $\lambda = \frac{Q}{L}$
> 
> The potential is:
> $\Delta V = -\int_{s_i}^{s_f} \vec{E} \cdot d\vec{s}$
> $\hspace{9mm} = -\int_{R}^{r} \frac{\lambda}{2\pi\epsilon_0 r} dr$
> $\hspace{9mm} = -\frac{\lambda}{2\pi\epsilon_0} \ln{r} |_{R}^{r}$
> $\hspace{9mm} = -\frac{\lambda}{2\pi\epsilon_0}(\ln{r} - \ln{R})$
> $\hspace{9mm} = -\frac{\lambda}{2\pi\epsilon_0} \ln{(\frac{r}{R})}$

### Sources of Electric Potential

Van de Graaff generator
Battery

For an ideal battery: $\Delta V = \frac{W_{chem}}{q} = \epsilon$ <--- $\epsilon$: emf (electromotive force)

> [!example] 
> What is the emf of a battery that does 0.60 J of work to transfer 0.050 C of charge from the negative to positive terminal?
> 
> $\epsilon = \frac{W_{chem}}{q} = \frac{0.60}{0.050} =$ 12 V

> [!example]
> Light from the sun allows a solar cell to move electrons from the positive to negative terminal doing 2.4 x 10^-19 J of work per electron. What is the emf of the solar cell?
>
> $\epsilon = \frac{W}{q} = \frac{2.4 \times 10^{-19}}{1.6 \times 10^{-19}} =$ 1.5 V

### Finding the Electric Field from Potential

For a small distance in one dimension
$\Delta V = -E \Delta s$
$\rightarrow E = \frac{-\Delta v}{\Delta s}$

In the limit $\Delta s \rightarrow 0$, then
$E = -\frac{dV}{ds}$

In general,
$\vec{E} = E_x\hat{i} + E_y\hat{j} + E_z\hat{k}$
$\hspace{5mm} = (\frac{\partial V}{\partial x}\hat{i} + \frac{\partial V}{\partial y}\hat{j} + \frac{\partial V}{\partial z}\hat{k})$

### Kirchhoff's Loop Law

> [!tip] Kirchhoff's Loop Law
> $\Delta V_{loop} = -\oint \vec{E} \cdot d\vec{s} = -\frac{1}{q} \oint \vec{F} \cdot d\vec{s} = -\frac{1}{q}W_{elect}$
> 
> Since $W_{elect}$ is from a conservative force, i.e. the work is independent of path.

### Conductors

Recall that the electric field is zero at any point inside of a conductor.
$\rightarrow \Delta V = \int \vec{E} \cdot d\vec{s} = 0$ <---- $\vec{E} = 0$
--> any two points inside a conductor in electrostatic equilibrium are at the same potential

Also, recall that the exterior electric field $\vec{E}$ of a charged conductor is perpendicular to the surface.
--> equipotential surface close to the conductor must roughly match the shape of the conductor

Electric field is always perpendicular to equipotential surfaces.