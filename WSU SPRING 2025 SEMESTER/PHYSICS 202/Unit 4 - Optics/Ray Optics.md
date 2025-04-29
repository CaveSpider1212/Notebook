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

Concave Mirror ($f > 0$):
![[4.14.25 Concave Mirror.png]]

Convex Mirror ($f < 0$):
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

> [!info] Real and Virtual Images
> Lenses: If the image distance is negative, that means it is on the **same side of the lens as the object** and is a **virtual and upright** image (however if $m$ is negative then it is inverted). If the image distance is positive, then it is a **real** image and on the opposite side of the object.
> 
> Mirrors: If the image distance is negative, then the image is located **behind the mirror** and is **virtual and upright**. If the image distance is positive, then it is a **real** image and on the same side as the object.

### Multiple Lenses

> [!example]
> There are 2 converging lenses separated by 10 cm. The first lens has a focal length of 40 cm, and the second lens has a focal length of 20 cm. The object is 15 cm to the left of the first lens. Where is the image?
> 
> The image from the first lens is located at:
> $\frac{1}{s_o} + \frac{1}{s_i} = \frac{1}{f}$
> $s_i = \frac{s_o f}{s_o - f} = \frac{(15)(40)}{15 - 40} =$ -24 cm
> 
> The image from the second lens is located at:
> $s_i = \frac{s_o f}{s_o - f} = \frac{(24 + 10) (20)}{(24 + 10) - 20} =$ 49 cm <--- the 24 comes from 24 cm, since the image is located 24 cm away from the first lens to the left, and the 10 comes from 10 cm, the distance separating the lenses; The image starts from 34 cm to the left of the second lens

> [!example]
> There is a converging lens and a diverging lens placed 160 cm apart. The converging lens has a focal length of 40 cm, and the diverging lens has a focal length of -40 cm. The image is 60 cm to the left of the converging lens. Where is the image?
> 
> The image from the first lens is located at:
> $s_i = \frac{s_o f_1}{s_o - f_1} = \frac{(60) (40)}{60 - 40} =$ 120 cm
> 
> The image from the second lens is located at:
> $s_i = \frac{s_o f_2}{s_o - f_2} = \frac{(160 - 120) (-40)}{(160 - 120) - (-40)} =$ -20 cm <--- the 160 comes from the lenses being 160 cm apart, and the 120 cm comes from the image being 120 cm to the right of the converging lens; the image starts from 40 cm to the left of the diverging lens