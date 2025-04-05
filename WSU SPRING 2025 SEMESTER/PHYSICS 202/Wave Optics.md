---
tags: PHYSICS_202
created: 2025-4-4
---

### Double Slit Experiment

![[4.4.25 Double Slit Experiment.png]]

![[4.4.25 Double Slit.png]]

The path lengths are
$r_1 = \sqrt{L^2 + (y - \frac{d}{2})^2}$
$r_2 = \sqrt{L^2 + (y + \frac{d}{2})^2}$

Thus,
$r_2^2 - r_1^2 = \left(L^2 + y^2 + yd + \frac{d^2}{4}\right) - \left(L^2 + y - yd + \frac{d^2}{4}\right)= 2yd$
$\rightarrow r_2 - r_1 = \frac{2yd}{r_2 + r_1} = \frac{2yd}{2L} = \frac{yd}{L}$ where $r_1 \approx r_2 \approx L$

Maximum constructive interference occurs when
$\Delta r = m \lambda, m = 0, \pm 1, \pm 2, \pm 3$

The possible positions of the bright fringe are
$y_m = \frac{m \lambda L}{d}$

> [!info] Double Slit Formulas
> $$\tan \theta_m = \frac{y_m}{L}$$
> 
> For small angles
> $$\theta_m = \frac{m \lambda}{d}$$
> $$\Delta y = y_{m + 1} - y_m = \frac{(m + 1) \lambda L}{d} - \frac{m \lambda L}{d} = \frac{L}{d} \lambda$$
> 
> The amplitude of two superimposed waves is
> $$A = \left| 2a \cos\left(\frac{\Delta \varphi}{2}\right) \right|$$
> 
> The phase difference is
> $$\Delta \varphi = 2\pi \frac{\Delta r}{\lambda} = 2\pi \frac{yd}{L \lambda}$$
> 
> The intensity is:
> $$I = cA^2 = 4c a^2 \cos^2\left(\frac{\pi d}{\lambda L} y\right) = 4 I_1 \cos^2(\frac{\pi d}{\lambda L} y)$$
> where $I_1 = ca^2$ (the intensity of one wave) and $c$ is a constant

Ideally, the intensity of the fringes would have equal intensity. In reality, the fringe intensity decreases as we go away from the slits because the light from a single slit is not uniform.

> [!example]
> Let $\Delta y$ = 4.0 mm. How far from the central maximum is the first position at which the intensity is equal to $I_1$?
> 
> The intensity is:
> $I = 4I_1 \cos^2 \left(\frac{\pi d}{\lambda L} y\right) = I_1$
> 
> The fringe spacing is:
> $\Delta y = \frac{L}{d}\lambda =$ 4.0 mm
> 
> Thus,
> $I_1 = 4I_1 \cos^2(\frac{\pi y}{\Delta y})$
> $\cos^2 \left(\frac{\pi y}{\Delta y}\right)= \frac{1}{4}$
> $\frac{\pi y}{\Delta y} = \cos^{-1} (\frac{1}{2})$ <--- after taking square root of both sides
> $y = \frac{\Delta y}{\pi} \cos^{-1}(\frac{1}{2})$
> $\hspace{4mm} = \frac{4.0}{\pi} (\frac{\pi}{3})$
> $\hspace{4mm} =$ 1.3 mm

### Diffraction Grating

![[4.4.25 Diffraction Grating.png]]
The paths are nearly parallel.

> [!info] Diffraction Grating
> The path difference is:
> $\Delta r = d \sin\theta$
> 
> Maximum constructive interference occurs when:
> $\Delta r = d \sin\theta_m = m \lambda, m = 0, \pm 1, \pm 2, ...$
> 
> The position of the bright fringes is:
> $y_m = L \tan\theta_m$ <--- same as before

> [!example]
> A diffraction grating with 600 lines per millimeter is illuminated with light of wavelength 500 nm. A very wide viewing screen is 2.0 m behind the grating.
> 
> a) What is the distance between the two m = 1 bright fringes (m = 1 and m = -1)?
> $y_1 = L \tan\theta_1$
> $\hspace{6mm} = L \tan(\sin^{-1} (\frac{m \lambda}{d}))$
> $\hspace{6mm} = (2.0) \tan(\sin^{-1} (\frac{(1)(500 \times 10^{-9})}{\frac{1}{600} \times 10^{-3}}))$
> $\hspace{6mm} =$ 0.63 m
> 
> $y_1 - y_{-1} = 2(0.63) =$ 1.26 m
> 
> b) How many bright fringes are seen on the screen?
> $d \sin\theta_m = m \lambda$
> $m = \frac{d}{\lambda} \sin\theta_m = \frac{\frac{1}{600} \times 10^{-3}}{500 \times 10^{-9}} \sin 90\degree =$ 3.3
> 
> There are seven bright fringes, $m = 0, \pm 1, \pm 2, \pm 3$.

> [!example]
> There is one peak in intensity at $y =$ 160.6 cm and another peak at $y =$ 161.1 cm. The wavelength of the second peak (the one at 161.1 cm) is 610 nm, and the wavelength of the first one is unknown.
> 
> Other known values:
> $L =$ 1.5 m
> $m =$ 2
> 
> What is the smaller wavelength?
> 
> The position of the bright fringe is
> $y_m = L \tan\theta_m = L \tan(\sin^{-1} (\frac{m \lambda}{d}))$
> 
> The spacing of the grating is:
> $d = \frac{m \lambda}{\sin(\tan^{-1} (\frac{y}{L}))}$
> $\hspace{4mm} = \frac{(2)(610 \times 10^{-9})}{\sin(\tan^{-1} (\frac{{1.611}{1.5}}))}$
> $\hspace{4mm} =$ 1.667 x 10^-6 m
> 
> The smaller wavelength is:
> $\lambda = \frac{d}{m} \sin(\tan^{-1} (\frac{y}{L}))$
> $\hspace{4mm} = \frac{1.667 \times 10^{-6}}{2} \sin(\tan^{-1} (\frac{1.606}{1.5}))$
> $\hspace{4mm} =$ 6.09 x 10^-7 m = 609 nm