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

### Thin Lenses: Ray Tracing

![[4.14.25 Converging Lens.png]]
Focal point, $f > 0$

![[4.14.25 Diverging Lens.png]]
Focal point, $f < 0$

For $s_o > f$, real and inverted.
For $s_o < f$, virtual and erect.

### Lateral Magnification

> [!info] Lateral Magnification
> $$m = \frac{h_i}{h_o} = -\frac{s_i}{s_o}$$
> 
> $m > 0$: erect image
> $m < 0$: inverted image

### Thin Lenses: Refraction Theory

![[4.14.25 Spherical Surface Refraction.png]]
$\theta_1 = \alpha + \phi$
$\theta_2 = \phi - \beta$

> Snell's Law (small angle approximation, $\sin \theta = \theta$)
> $n_1 \theta_1 = n_2 \theta_2$
> $n_1 (\alpha + \phi) = n_2 (\phi - \beta)$
> $\frac{n_1}{s_o}+ \frac{n_2}{s_i} = \frac{n_2 - n_1}{R}$

> [!tip] Refraction Theory Equation
> $$\frac{n_1}{s_o}+ \frac{n_2}{s_i} = \frac{n_2 - n_1}{R}$$

![[4.14.25 Lens.png]]

> [!tip] Thin-Lens Equation
> $$\frac{1}{s_o} + \frac{1}{s_i} = \frac{1}{f}$$
> 
> $s_o$ is the distance of the object to the left of the lens
> $s_i$ is the distance of the image to the right of the lens

> [!tip] Lens Maker's Equation
> $$\frac{1}{f} = (n - 1) (\frac{1}{R_1} - \frac{1}{R_2})$$

### Spherical Mirrors

Concave Mirror:
![[4.14.25 Concave Mirror.png]]

Convex Mirror:
![[4.14.25 Convex Mirror.png]]

> [!tip] Mirror Equation
> $$\frac{1}{s_0} + \frac{1}{s_i} = \frac{1}{f}$$
> 
> $$f = \frac{R}{2}$$

> [!example]
> A 2.0-cm-length object is 15 cm in front of a converging lens that has a 20 cm focal length. Where is the image?
> 
> $\frac{1}{s_o} + \frac{1}{s_i} = \frac{1}{f}$
> $\frac{1}{s_i} = \frac{1}{f} - \frac{1}{s_i}$
> $\frac{1}{s_i} = \frac{s_o - f}{f s_o}$
> $s_i = \frac{f s_o}{s_o - f} = \frac{(20)(15)}{15 - 20} =$ -60 cm

> [!example]
> An object is 30 cm in front of a convex mirror with a focal length of 20 cm. Where is the image?
> 
> $\frac{1}{s_o} + \frac{1}{s_i} = \frac{1}{f}$
> $s_i = \frac{f s_o}{s_o - f} = \frac{(-20)(30)}{30 + 20} =$ -12 cm