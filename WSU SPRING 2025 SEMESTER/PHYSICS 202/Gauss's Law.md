---
tags: PHYSICS_202
created: 2025-1-17
---

![[IMG_0063 2.heic]]

- Symmetry
	- Translational (#1 in drawing)
	- Rotational (#2 in drawing)
	- Reflection (#3 in drawing)

> [!info]
> The symmetry of the charge distribution matches the symmetry of the electric field.

- Fundamental electrostatic symmetries
	- Planar (#4 in drawing)
	- Cylindrical (#5 in drawing)
	- Spherical (#6 in drawing)

### Electric Flux

- **Electric flux**: total amount of electric field passing through a given surface
	- Proportional to the number of field lines passing through the surface

> [!tip] Electric Flux
> $$\Phi_E = \int \vec{E} \cdot d\vec{A}$$
> 
> ![[1.17.25 Area Vector Drawing]]
> 
> For uniform electric fields (such as parallel lines): $\Phi_E = \vec{E} \cdot \int d\vec{A} = \vec{E} \cdot \vec{A}$

> [!example]
> A 2.0 cm x 3.0 cm rectangle lies in the xy-plane. What is the electric flux through the rectangle if $\vec{E} = (50\hat{i} + 100\hat{k})$ N/C?
> 
> ![[1.17.25 Electric Flux Example 1]]
> 
> $\vec{A} = (0.02)(0.03)\hat{k} = (0.0006) \hat{k}$
> 
> The electric flux is
> $\Phi_E = \int \vec{E} \cdot d\vec{A} = \vec{E} \cdot \vec{A}$
> $\hspace{7mm} = [(50\hat{i} + 100\hat{k})] \cdot (0.0006 \hat{k})$
> $\hspace{7mm} = [(50)(0.0006)(\hat{i} \cdot \hat{k})] + (100)(0.0006)(\hat{k} \cdot \hat{i})$ <---- $\hat{i} \cdot \hat{k}$ and $\hat{k} \cdot \hat{i}$ both equal 0
> $\hspace{7mm} =$ 0.06 Nm\^2/C

> [!example]
> Same as above except $\vec{E} = (50\hat{i} + 100\hat{j})$ N/C.
> 
> The electric flux is
> $\Phi_E = \int \vec{E} \cdot d\vec{A} = \vec{E} \cdot \vec{A}$
> $\hspace{7mm} = [(50 \hat{i} + 100\hat{j})] \cdot (0.0006 \hat{k})$
> $\hspace{7mm} =$ 0

> [!info]
> Electric fields parallel to the surface produces no electric force.

> [!example]
> A cube with side lengths of 3.0 cm with an electric field magnitude of 500 N/C, and the field is traveling 30$\degree$ with respect to the right side (side 1) on the front face.
> 
> ![[1.17.25 Electric Flux Example 2]]
> 
> The electric fluxes are
> $\Phi_E = \int \vec{E} \cdot d\vec{A} = \vec{E} \cdot \vec{A}$
> 
> $\Phi_1 = (500)(0.03)^2\cos{30\degree} = 0.39$ Nm^2/C
> $\Phi_2 = (500)(0.03)^2\cos{60\degree} = 0.23$ Nm^2/C
> $\Phi_3 = (500)(0.03)^2\cos{150\degree} = -0.39$ Nm^2/C
> $\Phi_4 = (500)(0.03)^2\cos{120\degree} = -0.23$ Nm^2/C
> 
> The net flux is $\Phi_{net} = \Phi_1 + \Phi_2 + \Phi_3 + \Phi_4 = 0$.

> [!example]
> A spherically symmetric charge distribution produces the electric field $\vec{E} = (5000 r^2)\hat{r}$ N/m^2/C. What is the electric field through a 40-cm-diameter spherical surface that is concentric with the charge distribution?
> 
> The electric flux is
> $\Phi_E = \int \vec{E} \cdot d\vec{A} = \vec{E} \cdot \vec{A}$
> $\Phi_E = [(5000 r^2) \hat{r}] \cdot [(4\pi r^2) \hat{r}]$
> $\hspace{7mm} = 20,000\pi r^4$
> $\hspace{7mm} = 20,000\pi (0.20)^4$ <--- radius is 0.20 m
> $\hspace{7mm} = 100$ Nm^2/C

### Gauss's Law

##### For a point charge

> ![[1.17.25 Gauss's Law 1]]
> 
> $\Phi_E = \int \vec{E} \cdot d\vec{A} = EA = (\frac{1}{4\pi\epsilon_0} \frac{q}{r^2})(r\pi r^2) = \frac{q}{\epsilon_0}$
> 
> The flux through any closed surface is independent of the shape of the Gaussian surface.

> ![[1.17.25 Gauss's Law 2]]
> 
> $\Phi_E = \frac{q}{\epsilon_0}$

> ![[1.17.25 Gauss's Law 3]]
> 
> $\Phi_E = 0$

##### For multiple charges

> [!tip] Gauss's Law
> $$\Phi_E = \int \vec{E} \cdot d\vec{A} = \frac{Q_{in}}{\epsilon_0}$$
> 
> This formula gives us the total electric flux through the surface.
> 
> Note: the shape of the surface (the area) does not affect the total electric flux

> [!example]
> Find the electric field of an infinite wire with linear charge density, $\lambda$.
> 
> Note: the Gaussian surface is a cylinder of length L on the outside of the wire
> 
> By Gauss's Law
> $\int \vec{E} \cdot d\vec{A} = \frac{Q_{in}}{\epsilon_0}$
> $EA = \frac{Q_{in}}{\epsilon_0}$
> $E(2\pi rL) = \frac{Q}{\epsilon_0}$
> $E = \frac{Q}{2\pi\epsilon_0 rL} = \frac{\lambda}{2\pi\epsilon_0 r}$ <--- where $\lambda = \frac{Q}{L}$

> [!example]
> Find the electric field of an infinite plane with surface charge density, $\eta$.
> 
> Note: the Gaussian surface is a cylinder(?) through the plane
> 
> By Gauss's Law
> $\int \vec{E} \cdot d\vec{A} = \frac{Q_{in}}{\epsilon_0}$
> $EA = \frac{Q_{in}}{\epsilon_0}$
> $E(2\pi R^2) = \frac{Q}{\epsilon_0}$
> $E = \frac{Q}{2\pi R^2 \epsilon_0} = \frac{\eta}{2\epsilon_0}$ <--- where $\eta = \frac{Q}{A} = \frac{Q}{\pi R^2}$

> [!example]
> What is the electric field inside a uniformly charged sphere?
> 
> Note: the Gaussian surface is a sphere inside of the charged sphere
> 
> By Gauss's Law
> $\int \vec{E} \cdot d\vec{A} = \frac{Q_{in}}{\epsilon_0}$
> $EA = \frac{Q_{in}}{\epsilon_0}$
> $E(4\pi r^2) = \frac{Q_{in}}{\epsilon_0}$ <--- where $\frac{Q_{in}}{Q} = \frac{V_{gauss}}{V_{dist}} = \frac{\frac{4}{3}\pi r^3}{\frac{4}{3}\pi R^3}$
> $E(4\pi r^2) = \frac{Q \frac{r^3}{R^3}}{\epsilon_0}$
> $E = \frac{Qr}{4\pi\epsilon_0 R^3}$

### Conductors

> [!info] Important Things about Conductors
> - The electric field is zero within a conductor, since the charges are free to move.
> 
> By Gauss's Law
> (the Gaussian surface is of the same shape as the conductor but inside the conductor)
> 
> $\int \vec{E} \cdot d\vec{A} = \frac{Q_{in}}{\epsilon_0} = 0$ <--- the integral is 0 since there is no electric field
> 
> ---> all excess charges are on the surface
> 
> - Since the charges are at rest, the electric field is perpendicular to the surface of the conductor.
> 
> - The electric field is zero inside any hole within a conductor unless there is a charge in the hole.

> [!example]
> ![[1.22.25 Conductor Example Drawing]]
> 
> Lengths:
> 1 - 5 cm
> 2 - 10 cm
> 3 - 15 cm
> 4 - 8 cm
> 5 - 17 cm
> 
> Charges:
> $\vec{E}_1 =$ -10,000 N/C $\hat{r}$
> $\vec{E}_2 =$ 10,000 N/C $\hat{r}$
> 
> What is the total charge on (a) the exterior of the inner sphere, (b) the inside surface of the hollow sphere, and (c) the exterior surface of the hollow sphere?
> 
> a)
> Note: the Gaussian surface is on the outside of the inner sphere with a radius of 8 cm (the Gaussian sphere is likely where $\vec{E}_1$ is)
> 
> By Gauss's Law
> $\int \vec{E} d\vec{A} = \frac{Q_{in}}{\epsilon_0}$
> $EA = \frac{Q_1}{\epsilon_0}$
> $Q_1 = \epsilon_0 EA = (8.85 \times 10^{12}) \cdot (-10,000)(4\pi (0.08)^2)$
> $\hspace{6.5mm} =$ -7.1 nC
> 
> b)
> Note: the Gaussian surface is between the 2nd and 3rd spheres
> 
> By Gauss's Law
> $\int \vec{E} \cdot d\vec{A} = \frac{Q_{in}}{\epsilon_0}$
> $EA = \frac{Q_1 + Q_2}{\epsilon_0}$ <--- $E$ is 0 because either it is a conductor or it is in between the points which have opposite field strengths??
> $\rightarrow Q_2 = -Q_1 =$ 7.1 nC
> 
> c)
> Note: the Gaussian spheres is outside of all of the spheres and has a radius of 17 cm (this is likely where $\vec{E}_2$ is)
> 
> By Gauss's Law
> $\int \vec{E} \cdot d\vec{A} = \frac{Q_{in}}{\epsilon_0}$
> $EA = \frac{Q_1 + Q_2 + Q_3}{\epsilon_0}$ <--- $Q_1$ and $Q_2$ are opposites of each other, so they cancel each other out
> $Q_3 = \epsilon_0 EA = (8.85 \times 10^{-12}) \cdot (10,000)(4\pi (0.17)^2)$
> $\hspace{7mm} =$ 32 nC