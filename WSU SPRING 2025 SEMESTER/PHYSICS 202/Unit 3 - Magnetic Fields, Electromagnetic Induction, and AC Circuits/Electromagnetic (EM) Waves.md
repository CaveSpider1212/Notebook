---
tags: PHYSICS_202
created: 2025-4-2
---

> Let $E_y = E_0 \cos(\frac{2\pi x}{\lambda} - 2\pi ft)$.
> 
> By Faraday's Law:
> $\oint \vec{E} \cdot d\vec{s} = \frac{-d \Phi_m}{dt} = \frac{-d}{dt} \int \vec{B} \cdot d\vec{A}$
> $\frac{\partial E_y}{\partial x} = -\frac{\partial B_z}{\partial t}$
> 
> Thus,
> $B_z = -\frac{\partial}{\partial x} \int E_y dt$
> $\hspace{6.5mm} = \frac{-\partial}{\partial x} \int E_0 \cos\left(\frac{2\pi x}{\lambda} - 2\pi ft\right)dt$
> $\hspace{6.5mm} = \frac{-\partial}{\partial x} \left(\frac{-1}{2\pi f}\right)E_0 \sin(\frac{2\pi x}{\lambda} - 2\pi ft)$
> $\hspace{6.5mm} = \left(\frac{1}{2\pi f}\right)\left(\frac{2\pi}{\lambda}\right)\cos(\frac{2\pi x}{\lambda} - 2\pi ft)$
> $\hspace{6.5mm} = \frac{E_0}{v} \cos(\frac{2\pi x}{\lambda}  - 2\pi ft)$ <--- where $v = \lambda f$

### Properties of EM Waves

> [!info]
> 1. $\vec{E}$ and $\vec{B}$ are perpendicular to each other.
> 2. $\vec{E}$ and $\vec{B}$ are perpendicular to the direction of propagation.
> 3. The wave travels in vacuum at $c = \frac{1}{\sqrt{\epsilon_0 \mu_0}}$, the speed of light.
> 4. $E = cB$ at any point in the wave.

> Define the Poynting vector (rate of energy transfer per unit area) as:
> $$\vec{S} = \frac{1}{\mu_0} \vec{E} \times \vec{B}$$
> 
> where $\vec{S}$ is in the direction of wave propagation.
> 
> The average intensity (power per area):
> $I = S_{avg} = \frac{1}{2\mu_0} E_0 B_0 = \frac{1}{2 c \mu_0} E_0^2$
> 
> The radiation pressure (force per unit area exerted normal to a surface by the EM wave) as
> $P = \frac{I}{c}$

> [!example]
> A laser beam shines straight up onto a flat black foil with a mass of 15 $\mu$g. What laser power is needed to levitate the foil?
> 
> $F_{laser} = mg$
> $pA = mg$
> $\frac{I}{c} A = mg$
> $\frac{\frac{P}{A}}{c} A = mg$
> $P = mgc$
> $\hspace{5mm} = (15 \times 10^{-9})(9.8)(3.0 \times 10^8)$
> $\hspace{5mm} =$ 44.1 W

### Polarization

The plane of polarization is in the plane of the electric field.

> If we have unpolarized natural light traveling through a vertical polarizer, it will come out as polarized with an intensity of $I_0$. That same light goes through a second polarizer (horizontal) and comes out with an unknown intensity $I$.
> 
> The transmitted electric field through the second polarizer is:
> $E_{trans} = E_0 \cos\theta$
> 
> The intensity is:
> $I_{trans} = I_0 \cos^2 \theta$ <--- Malus's Law
> 
> For unpolarized light:
> $I_{trans} = \frac{1}{2}I_0$

> [!tip] Malus's Law
> Intensity:
> $$I_{\text{trans}} = I_0 \cos^2 \theta$$
> 
> Unpolarized light intensity:
> $$I_{\text{trans}} = \frac{1}{2} I_0$$

> [!example]
> There is a natural light with intensity $I_0$ that goes through a vertical polarizer and comes out with an intensity of $I_1$. That polarized light then goes through a 45-degree tilted polarizer and comes out with an intensity of $I_2$. Then it goes through a horizontal polarizer and comes out with an intensity of $I_3$.
> 
> What light intensity emerges from the third polarizer?
> 
> 1st polarizer:
> $I_1 = \frac{1}{2}I_0$
> 
> 2nd polarizer:
> $I_2 = I_1 \cos^2 (45\degree) = \left(\frac{1}{2}I_0\right)\left(\frac{1}{\sqrt{2}}\right)^2 = \frac{1}{4}I_0$
> 
> 3rd polarizer:
> $I_3 = I_2 \cos^2 (45\degree) = \left(\frac{1}{4} I_0\right)(\frac{1}{\sqrt{2}})^2 = \frac{1}{8}I_0$