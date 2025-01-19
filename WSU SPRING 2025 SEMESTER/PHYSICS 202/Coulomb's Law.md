---
tags: PHYSICS_202
created: 2025-1-8
---

> [!tip] Coulomb's Law
> $$F_{1 \text{on} 2} = F_{2 \text{on} 1} = \frac{K(q_1)(q_2)}{r^2}$$
> 
> $K =$ 8.99 $\times$ 10$^9$ N m$^2$/C$^2$

### Properties

1. The force is repulsive for two like charges and attractive for two opposite charges.
2. Coulomb's law applies only to point charges.
3. Coulomb's law only applies to electrostatics.
4. Electric forces can be superimposed.

$$\vec{F}_{net} = \vec{F}_{1 \text{on} j} + \vec{F}_{2 \text{on} j} + \vec{F}_{3 \text{on} j}$$

> [!info] Permittivity Constant
> $\epsilon_o = \frac{1}{4\pi K} = 8.85 \times 10^{-12}$ C$^2$/Nm$^2$
> $\rightarrow F = \frac{1}{4\pi \epsilon} \frac{|q_1| |q_2|}{r^2}$

> [!example]
> ![[1.8.25 Coulomb Sphere Drawing]]
> 
> What is the initial acceleration?
> 
> Free-body diagram:
> ![[1.8.25 Coulomb Spheres FBD]]
> 
> Newton's Second Law (x-component):
> $F_{coulomb} = ma_x$
> $a_x = \frac{F_{coulomb}}{m} = \frac{K |q_1| |q_2|}{mr^2} = \frac{(8.99 \times 10^9) (10 \times 10^{-6}) (10 \times 10^{-6})}{(1.0)(1.0)^2} =$ 2.90 m/s$^2$

> [!info] Important
> If the vector is facing to the left, it is $-\hat{i}$, but if it is facing to the right, it is $+\hat{i}$.
> If the vector is facing down, it is $-\hat{j}$, but if it is facing up, it is $+\hat{j}$.

> [!example]
> ![[1.8.25 Equilateral Coulomb Drawing]]
> 
> What is the force on the 1.0 nC charge?
> 
> The force due to charge 2 is
> $F_{2 \text{on} 1} = K \frac{q_1 q_2}{r^2} = (8.99 \times 10^9) \frac{(1.0 \times 10^{-9}) (2.0 \times 10^{-9})}{(0.01)^2} =$ 1.80 $\times$ $10^{-4}$ N
> 
> The force due to charge 3 is
> $F_{3 \text{on} 1} = K \frac{q_1 q_3}{r^2} =$ 1.80 $\times$ $10^{-4}$ N <--- the numbers are the same
> 
> ![[1.8.25 Equilateral Coulomb Net Force]]
> 
> The net force is
> $\vec{F}_{net} = \vec{F}_{21} + \vec{F}_{31} = (1.80 \times 10^{-4})(\cos{60\degree} \hat{i} + \sin{60\degree} \hat{j}) + (1.80 \times 10^{-4})(-\cos{60\degree} \hat{i} + \sin{60\degree} \hat{j})$
> $\hspace{8mm} = 2(1.80 \times 10^{-4}) \sin{60\degree} \hat{j}$
> $\hspace{8mm} = 3.1 \times 10^{-4} \hat{j}$

> [!example]
> ![[1.8.25 Coulomb Example 2 Drawing]]
> 
> What is the force (magnitude and direction) on the -2.0 nC charge?
> 
> The net force is
> $\vec{F}_{net} = \vec{F}_{21} + \vec{F}_{31}$
> $\hspace{8mm} = K \frac{|q_1| |q_2|}{r_{12}^2}(-\cos\theta \hat{i} + \sin\theta \hat{j}) + K \frac{|q_1| |q_3|}{r_{13}^2} \hat{i}$ <----- $\vec{F}_{21}$ is going to the left and up, so $\hat{i}$ (cosine) is negative and $\hat{j}$ (sine) is positive; $\vec{F}_{31}$ is only going to the right in the x direction, so there is only $\hat{i}$ which is positive
> 
> $\hspace{8mm} = \left(-K \frac{|q_1| |q_2|}{r_{12}^2} \cos\theta + K \frac{|q_1| |q_3|}{r_{13}^2}\right) \hat{i} + K \frac{|q_1| |q_2|}{r_{12}^2} \sin\theta \hat{j}$
> $\cos\theta = \frac{0.04}{\sqrt{(0.04)^2 + (0.03)^2}} = \frac{4}{5}$
> $\sin\theta = \frac{0.03}{\sqrt{(0.04)^2 + (0.03)^2}} = \frac{3}{5}$
> 
> $\vec{F} = (8.99 \times 10^9) \left[- \frac{(2.0 \times 10^{-9}) (5.0 \times 10^{-9})}{0.05}^2 \left(\frac{4}{5}\right)+ \frac{(2.0 \times 10^{-9}) (3.0 \times 10^{-9})}{(0.03)^2}\right]\hat{i} + (8.99 \times 10^9) \frac{(2.0 \times 10^{-9}) (5.0 \times 10^{-9})}{(0.05)^2} \left(\frac{3}{5}\right)\hat{j}$
> $\hspace{4.5mm} = (-2.67 \times 10^{-5} \hat{i} + 2.1576 \times 10^{-5} \hat{j})$
> 
> ![[1.9.25 Coulomb Example 2 Net Force]]
> 
> $F = \sqrt{F_x^2 + F_y^2} = \sqrt{(-2.67 \times 10^{-5})^2 + (2.16 \times 10^{-5})}$
> $\varphi = \tan^{-1}\left(\left| \frac{F_y}{F_x} \right|\right) = \tan^{-1}\left(\frac{2.16 \times 10^{-5}}{2.67 \times 10^{-5}}\right)$