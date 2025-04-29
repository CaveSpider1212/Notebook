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

> [!tip] Double-Slit Equation
> $$d \sin\theta_m = m \lambda$$
> 
> $d$: width between the centers of the two fringes
> $\theta_m$: angle to a bright fringe
> $m$: mode of a bright fringe
> $\lambda$: wavelength of the light
> 
> $y$: distance from the central maximum to a bright fringe

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

### Single Slit

![[4.7.25 Single Slit Diffraction.png]]

> [!info] Single Slit Formulas
> The path difference is
> $\Delta r = \frac{a}{2}\sin\theta$
> 
> Similarly, a wavefront could be paired with one $\frac{a}{2p}$ where $p = 1, 2, 3, ...$.
> 
> Maximum destructive interference occurs where $\Delta r = \frac{\lambda}{2}$
> $\rightarrow \frac{a}{2p}\sin\theta = \frac{\lambda}{2}$
> $\rightarrow a \sin\theta = p \lambda$
> 
> The position of the dark fringe is
> $y_p= L \tan\theta_p$

> [!tip] Single-Slit Equation
> $$a \sin\theta_p = p \lambda$$
> 
> $a$: width of the slit
> $\theta_p$: angle to dark fringe
> $p$: mode of dark fringe
> $\lambda$: wavelength of the light

> [!example]
> There is a pattern on a wall where there are 5 peaks in intensity and the peak at the center is the highest, and in between $y = 1$ cm and $y = 2$ cm. The wavelength is 600 nm and the length is 2.0 m. What is the width of the slit?
> 
> We want to look at where $p = 1$, at the minimum value closest to the peak intensity to the right.
> 
> $a = \frac{p \lambda}{\sin\theta}$
> $\hspace{4mm} = \frac{p \lambda}{\sin(\tan^{-1} (\frac{y}{L}))}$
> $\hspace{4mm} = \frac{(1) (600 \times 10^{-9})}{\sin(\tan^{-1} (\frac{0.005}{2.0}))}$
> $\hspace{4mm} =$ 2.4 x 10^-4 m

### Circular Aperture

What it looks like:
![[4.7.25 Circular Aperture.png]]

> [!info] Circular Aperture Formulas
> The diameter of bright central maximum is
> $w = \frac{2.44 \lambda L}{D}$ <--- where $D$ is the diameter of the circle and $L$ is the length of the light
> 
> The first dark fringe is located at
> $\theta_1 = \frac{1.22 \lambda}{D}$
> $y_1 = \frac{1.22 \lambda L}{D}$

> [!example]
> There are 5 peaks with the third peak being the maximum from $y = 1$ cm to $y = 2$ cm. The wavelength is 500 nm and the length is 1.0 m. What is the diameter of the circular aperture?
> 
> $w = \frac{2.44 \lambda L}{D}$
> $D = \frac{2.44 \lambda L}{w}$
> $\hspace{5mm} = \frac{2.44 (500 \times 10^{-9}) (1.0)}{0.01}$
> $\hspace{5mm} =$ 0.122 mm = 1.22 x 10^-4 m

### Michelson Interferometer

![[4.7.25 Michelson Interferometer.png]]

> [!info] Michelson Interferometer
> The path difference is
> $\Delta r = 2L_2 - 2L_1$
> 
> For constructive interference
> $\Delta r = m \lambda, m = 0, \pm 1, \pm 2, ...$
> $\rightarrow L_2 - L_1 = \frac{m \lambda}{2}$

> [!example]
> There is a Michelson interferometer, but there is a piece of glass inserted in the path of the waves traveling horizontally. The glass has a length of 0.10 mm. The wavelength of the waves is 500 nm. The glass causes the fringe position o shift by 200 fringes. What is the index of refraction of the glass?
> 
> When the waves travel through the piece of glass, the wavelength changes by $\frac{\lambda}{n}$, where $n$ is the index of refraction.
> 
> Number of wavelength without glass is:
> $m_1 = \frac{2d}{\lambda}$
> 
> Number of wavelengths with glass is:
> $m_2 = \frac{2d}{\frac{\lambda}{n}}$
> 
> The difference is:
> $\Delta m = m_2 - m_1 = n \frac{2d}{\lambda} - \frac{2d}{\lambda} = \frac{2d}{\lambda} (n - 1)$
> $\rightarrow n = \frac{\lambda}{2d} \Delta m + 1$
> $\hspace{10.5mm} = \frac{500 \times 10^{-9}}{2 (0.10 \times 10^{-3})} (200) + 1$
> $\hspace{10.5mm} =$ 1.5