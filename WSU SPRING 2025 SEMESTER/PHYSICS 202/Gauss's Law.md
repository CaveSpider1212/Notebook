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