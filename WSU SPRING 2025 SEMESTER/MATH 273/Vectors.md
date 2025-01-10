---
tags: MATH_273
created: 2025-1-7
---

Let $\overrightarrow{u} = (1, 2, 3) = \overrightarrow{i} + 2\overrightarrow{j} + 3\overrightarrow{k}$ and $\overrightarrow{v} = (2, -1, 4) = 2\overrightarrow{i} - \overrightarrow{j} + 4\overrightarrow{k}$

$\overrightarrow{i} = (1, 0, 0)$, $\overrightarrow{j} = (0, 1, 0)$, $\overrightarrow{k} = (0, 0, 1)$

![[1.7.25 Vector Graph.png]]

Then:

- The length of $\overrightarrow{u}$ is $\left| \overrightarrow{u} \right| = \sqrt{1^2 + 2^2 + 3^2} = \sqrt{14}$.
- A unit vector in the same direction as $\overrightarrow{u}$ is $\overrightarrow{u}$ is $\frac{\overrightarrow{u}}{\left| \overrightarrow{u} \right|} = \frac{<1, 2, 3>}{\sqrt{14}} = (\frac{1}{\sqrt{14}}, \frac{2}{\sqrt{14}}, \frac{3}{\sqrt{14}})$
- $\overrightarrow{u} + \overrightarrow{v} = (1, 2, 3) + (2, -1, 4) = (3, 1, 7)$
- $\vec{u} - \vec{v} = \vec{u} + -\vec{v} = (1, 2, 3) + (-2, 1, -4) = (-1, 3, -1)$

> [!info] Dot Product
> The dot product of $\vec{u} = (u_1, u_2, u_3)$ and $\vec{v} = (v_1, v_2, v_3)$ is $\vec{u} \cdot \vec{v} = u_1v_1 + u_2v_2 + u_3v_3$.

Recall:
$\vec{u} \cdot \vec{v} = |\vec{u}| |\vec{v}| \cos\theta$

So, $\vec{u} \cdot \vec{v}$ is
- 0 when $\theta = \frac{\pi}{2}$
- \>0 when $0 \leq \theta \lt \frac{\pi}{2}$
- <0 when $\frac{\pi}{2} \lt \theta \leq \pi$

By definition, $\vec{u}$ and $\vec{v}$ are perpendicular or orthogonal if and only if $\vec{u} \cdot \vec{v} = 0$.

The orthogonal projection of $\vec{u}$ onto $\vec{v}$:
![[1.7.25 Scalar Projection.png]]

Length is $|\vec{u}| \cos\theta = \frac{|\vec{u}| |\vec{v}| \cos\theta}{|\vec{v}|} = \frac{\vec{u} \cdot \vec{v}}{|\vec{v}} =$ scal$_{\vec{v}} \vec{u}$

The vector is $\large{\left(\dfrac{\vec{u} \cdot \vec{v}}{|\vec{v}|}\right)\dfrac{\vec{v}}{|\vec{v}|} = \left(\dfrac{\vec{u} \cdot \vec{v}}{|\vec{v}|^2} \right)\vec{v} = \left(\dfrac{\vec{u} \cdot \vec{v}}{\vec{v} \cdot \vec{v}}\right)\vec{v} = \text{proj}_\vec{v}\vec{u}}$

![[1.9.25 Vector Projection.png]]

> [!example]
> Compute $\vec{u} \cdot \vec{v}$ and find the angle between $\vec{u}$ and $\vec{v}$:
> 
> $$\vec{u} = \langle 3, -5, 2 \rangle \hspace{10mm} \vec{v} = \langle -9, 5, 1 \rangle$$
> 
> $\vec{u} \cdot \vec{v} = -27 + -25 + 2 = -50$
> 
> $\vec{u} \cdot \vec{v} = |\vec{u}| |\vec{v}| \cos\theta$
> $\rightarrow \frac{\vec{u} \cdot \vec{v}}{\left| \vec{u} \right| \left| \vec{v} \right|} = \cos\theta$
> 
> $\theta = \cos^{-1}(\frac{-50}{\sqrt{38} \sqrt{107}})$

> [!example]
> Calculate $\text{proj}_{\vec{v}} \vec{u}$ and $\text{scal}_{\vec{v}} \vec{u}$:
> 
> $$\vec{u} = \langle 1, 4, 7 \rangle \hspace{10mm} \vec{v} = \langle -2, -4, 2 \rangle$$
> 
> $\text{scal}_{\vec{v}} \vec{u} = \frac{\vec{u} \cdot \vec{v}}{|\vec{v}|} = \frac{-2 + -16 + 14}{\sqrt{2^2 + 4^2 + 2^2}} = \frac{-4}{\sqrt{24}} = \frac{-2}{\sqrt{6}}$
> 
> $\text{proj}_{\vec{v}} \vec{u} = \left(\frac{\vec{u} \cdot \vec{v}}{\vec{v} \cdot \vec{v}}\right)\vec{v} = \frac{-4}{24}\vec{v} = \frac{-1}{6} \langle -2, -4, 2 \rangle = \frac{1}{3} \langle 1, 2, -1 \rangle = \langle \frac{1}{3}, \frac{2}{3}, \frac{-1}{3} \rangle$

> [!info] Cross-Product
> The cross-product of $\vec{u}$ with $\vec{v}$ is a vector, denoted $\vec{u} \times \vec{v}$, with these properties:
> 
> 1. $\vec{u} \times \vec{v}$ is orthogonal to $\vec{u}$ and $\vec{v}$.
> 2. The direction of $\vec{u} \times \vec{v}$ is determined by the "right-hand rule"
> 
> ![[1.9.25 Right Hand Rule.png]]
> 
> 3. $\left| \vec{u} \times \vec{v} \right| = \left| \vec{u} \right| \left| \vec{v} \right| \sin\theta =$ area of parallelogram
> 
> ![[1.9.25 Parallelogram.png]]

> [!tip] Properties of Cross Products
> 1. $u \times v = -(v \times u)$
> 2. $(au) \times (bv) = ab(u \times v)$
> 3. $u \times (v + w) = (u \times v) + (u \times w)$
> 4. $(u + v) \times w = (u \times w) + (v \times w)$

> [!info] How to do Cross Product
> $$\vec{u} = \langle u_1, u_2, u_3 \rangle \hspace{7mm} \vec{v} = \langle v_1, v_2, v_3 \rangle$$
> 
> Distribute:
> $\vec{u} \times \vec{v} = (u_1 \vec{i} + u_2\vec{j} + u_3\vec{k}) \times (v_1\vec{i} + v_2\vec{j} + v_3\vec{k}) = ...$
> 
> Using matrix determinants (see [[Introduction to Determinants]]):
> $\vec{u} \times \vec{v} = \text{det}\begin{bmatrix} \vec{i}&\vec{j}&\vec{k}\\u_1&u_2&u_3\\v_1&v_2&v_3 \end{bmatrix}$
> Use first row

> [!example]
> Find $\vec{u} \times \vec{v}$ and $\vec{v} \times \vec{u}$
> 
> $$\vec{u} = \langle 3, -1, -2 \rangle \hspace{7mm} \vec{v} = \langle 1, 3, -2 \rangle$$
> 
> $\vec{u} \times \vec{v} = \text{det} \begin{bmatrix} \vec{i}&\vec{j}&\vec{k} \\ 3&-1&-2 \\ 1&3&-2 \end{bmatrix} = \langle 2-(-6), -(-6 - (-2)), 9-(-1) \rangle = \langle 8, 4, 10 \rangle$
> 
> $\vec{v} \times \vec{u} = -(\vec{u} \times \vec{v}) = \langle -8, -4, -10 \rangle$

> [!example]
> Find the area of triangle $T$, whose vertices are $A(5, 6, 2), B(7, 16, 4), C(6, 7, 3)$.
> 
> $AC = \langle 1, 1, 1 \rangle \hspace{7mm} AB = \langle 2, 10, 2 \rangle$
> 
> $\vec{AB} \times \vec{AC} = \langle 2, 10, 2 \rangle \times \langle 1, 1, 1 \rangle = \text{det} \begin{bmatrix} \vec{i}&\vec{j}&\vec{k} \\ 2&10&2 \\ 1&1&1 \end{bmatrix} = \langle 8, 0, -8 \rangle = 8 \langle 1, 0, -1 \rangle$
> 
> Area of $ABC$:
> $\frac{1}{2} \left| 8 \langle 1, 0, -2 \rangle \right| = \frac{1}{2}(8) \left| \langle 1, 0, -1 \rangle \right| = 4\sqrt{2}$