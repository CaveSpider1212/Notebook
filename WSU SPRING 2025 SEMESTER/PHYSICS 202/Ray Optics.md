---
tags: PHYSICS_202
created: 2025-4-11
---

> [!info] Ray Model of Light
> 1. Light rays travel in straight lines.
> 2. Light rays can cross.
> 3. A light ray travels forever unless it interacts with matter (refraction, reflection, scattering, or absorption will happen)
> 4. An object is a source of light rays.
> 5. The eye sees by focusing a diverging bundle of rays.

### Camera Obscura

![[4.11.25 Camera Obscura.png]]

By similar triangles,
$\frac{h_i}{h_o} = \frac{d_i}{d_o}$

### Reflection

![[4.11.25 Reflection.png]]

> [!info] Law of Reflection
> 1. The incident ray and reflected ray are in the same plane normal to the surface.
> 2. $\theta_i = \theta_r$

Spectral reflection:
![[4.11.25 Spectral Reflection.png]]

Diffuse reflection:
![[4.11.25 Diffuse Reflection.png]]

##### Plane Mirror

![[4.11.25 Plane Mirror.png]]

$d_o = d_i$ and $h_o = h_i$ <--- the object and image distances are equal, as well as their height (distances are $s$ in the image, and height is not shown)

### Refraction

- **Refraction**: occurs when the materials have two different index of refractions ($n = \frac{c}{v}$)

![[4.11.25 Refraction.png]]

> [!tip] Snell's Law (Law of Refraction)
> $$n_1 \sin\theta_1 = n_2 \sin\theta_2$$

![[4.11.25 Refraction Graph.png]]

![[4.11.25 Refraction Graph Reversed.png]]

##### Total Internal Reflection

- **Total Internal Reflection**: the light rays bend backwards during refraction

![[4.11.25 Total Internal Reflection.png]]

> [!info] Critical Angle
> $$\theta_c = \sin^{-1} \left(\frac{n_2}{n_1}\right)$$

> [!example]
> There is a layer of air ($n$ = 1.00) above a layer of water ($n$ = 1.33), which is above a layer of glass ($n$ = 1.50). The water later is 1.0 cm thick. A light is shined from behind the glass, which goes through the water layer. What is the minimum angle of incidence that the light can emerge into the air?
> 
> Max. angle from water
> $\theta_2 = \theta_c = \sin^{-1} \left(\frac{n_2}{n_1}\right) = \sin^{-1} \left(\frac{1.00}{1.33}\right) =$ 48.8$\degree$
> 
> Max angle from glass
> $\theta_1 = \theta_c = \sin^{-1} \left(\frac{n_2}{n_1} \sin \theta_2\right) = \sin^{-1} \left(\frac{1.33}{1.50} \sin(48.8 \degree)\right) =$ 41.0$\degree$

##### Image from Refraction

![[4.11.25 Image from Refraction.png]]

![[4.11.25 Finding Virtual Image.png]]

$l = s_o \tan \theta_1 = s_i \tan \theta_2$ <--- $s_o = s$ and $s_i = s'$ in the image above

For small angles $\tan\theta \approx \sin\theta$:
$s_o \sin\theta_1 = s_i \sin\theta_2$
$s_i = \frac{\sin\theta_1}{\sin\theta_2}s_o$