---
tags: PHYSICS_201
created: 2024-11-13
---

![[11.13.24 Speaker Distance Drawing]]

$D_1(x_1, t) = a\sin({kx_1 - \omega t + \varphi_{1o}})$
$D_2(x_2, t) = a\sin({kx_2 - \omega t + \varphi_{2o}})$

### Constructive Interference

![[11.13.24 Constructive Interference Wave]]

> [!tip] Constructive Interference
> $$D_1(x_1, t) = D_2(x_2, t)$$
> $$\rightarrow \varphi_1 = \varphi_2 + 2\pi m, \hspace{5mm} m = 0, 1, 2, ...$$

Phase difference:
$\Delta \varphi = \varphi_2 - \varphi_1$
$\hspace{8.5mm} = (kx_2 - \omega t + \varphi_{2o}) - (kx_1 - \omega t + \varphi_{1o})$
$\hspace{8.5mm} = k(x_2 - x_1) + (\varphi_{2o} - \varphi_{1o})$
$\hspace{8.5mm} = k \Delta x + \Delta \varphi_o$
$\hspace{8.5mm} = \frac{2\pi}{\lambda}\Delta x + \Delta \varphi_o$

> [!info] Maximum Constructive Interference
> Therefore, maximum constructive interference occurs when
> 
> $$\frac{2\pi}{\lambda}\Delta x + \Delta \varphi_o = 2\pi m$$

### Destructive Interference

![[11.13.24 Destructive Interference Wave]]

> [!tip] Destructive Interference
> $$D_1(x_1, t) = -D_2(x_2, t)$$
> $$\rightarrow \varphi_1 = \varphi_2 + \pi + 2\pi m, \hspace{5mm} m = 0, 1, 2, 3, ...$$

> [!info] Maximum Destructive Interference
> Therefore, perfect destructive interference occurs when
> 
> $$\frac{2\pi}{\lambda}\Delta x + \Delta \varphi_o = 2\left(m + \frac{1}{2}\right)\pi$$

### General Interference

> [!tip] General Interference
> 
> $$D = D_1 + D_2 = a\sin({kx_1 - \omega t + \varphi_{1o}}) + a\sin({kx_2 - \omega t + \varphi_{2o}})$$
> 
> Note: $\sin\alpha + \sin\beta = 2\cos\left[{\frac{1}{2}(\alpha - \beta)}\right] \sin \left[{\frac{1}{2}(\alpha + \beta)}\right]$
> 
> $D = 2a\cos \left[\frac{1}{2}((kx_1 - \omega t + \varphi_{1o}) - (kx_2 - \omega t + \varphi_{2o}))\right] \cdot \sin \left[\frac{1}{2}((kx_1 - \omega t + \varphi_{1o}) - (kx_2 - \omega t + \varphi_{2o}))\right]$
> $\hspace{5mm} = 2a\cos \left[\frac{1}{2}(kx_1 - kx_2 + \varphi_{1o} - \varphi_{2o}) \right] \sin \left[\frac{1}{2}(kx_1 + kx_2) - \omega t + \frac{1}{2}(\varphi_{1o} + \varphi_{2o}) \right]$
> $\hspace{5mm} = 2a \cos \left[\frac{1}{2} \Delta\varphi \right] \sin [kx_{avg} - \omega t + \varphi_{o, avg}]$
> 
> $$D = 2a \cos \left[\frac{1}{2} \Delta\varphi \right] \sin [kx_{avg} - \omega t + \varphi_{o, avg}]$$

> [!tip] Amplitude for General Interference
> The amplitude is:
> $$A = \left|2a\cos \left[\frac{1}{2} \varphi \right]\right|$$
> 
> Maximum amplitude occurs when
> $$\frac{1}{2}\Delta \varphi = m\pi$$
> $$\rightarrow \Delta\varphi = 2\pi m$$
> 
> Minimum amplitude occurs when
> $$\frac{1}{2}\Delta\varphi = \frac{2m + 1}{2}\pi$$
> $$\rightarrow \Delta\varphi = 2(m + \frac{1}{2})\pi$$

> [!example]
> Imagine two speakers that are playing and a person standing in the middle. There is constructive interference at the middle and destructive interference when the speaker moves d meters closer to the speaker on the right.
> 
> Known values:
> $f =$ 242 Hz (in phase)
> 
> How far must the observer walk to first experience destructive interference?
> 
> ![[11.13.24 Person Speakers Drawing]]
> 
> Destructive interference:
> $\frac{2\pi}{\lambda}\Delta x + \Delta \varphi_o = 2(m + \frac{1}{2})\pi$ <--- where $m = 0$ (first mode)
> $\frac{2\pi}{\lambda} \Delta x = \pi$
> $\Delta x = x_2 - x_1 = \frac{\lambda}{2}$
> $(l + d) - (l - d) = \frac{\lambda}{2}$
> $2d = \frac{\lambda}{2}$
> $d = \frac{\lambda}{4} = \frac{\frac{v}{f}}{4} = \frac{\frac{343}{242}}{4} =$ 0.354 m

### Beats

![[11.13.24 Beats Drawing]]

$D_1(x, t) = a_1\sin({k_1 x - \omega_1 t + \varphi_{1o}})$
$D_2(x, t) = a_2\sin({k_1 x - \omega_2 t + \varphi_{2o}})$

Assumptions:
1. Amplitudes are equal: $a_1 = a_2 = a$
2. Detector is located at the origin, $x = 0$
3. The sources are in phase, $\varphi_{1o} = \varphi_{2o}$
4. The source phase is $\varphi_{1o} = \varphi_{2o} = \pi$

Thus,
$D_1(x = 0, t) = a\sin({-\omega_1 t + \pi}) = a\sin({\omega_1 t})$
$D_2(x = 0, t) = a\sin({-\omega_2 t + \pi}) = a\sin({\omega_2 t})$

> [!tip] Beats
> 
> $$D = D_1 + D_2 = 2a\cos[\omega_{mod} t] \sin[\omega_{avg} t]$$
> where $\omega_{mod} = \frac{1}{2}(\omega_1 - \omega_2)$ (modulation frequency) and $\omega_{avg} = \frac{1}{2}(\omega_1 + \omega_2)$ (average frequency)

> [!tip] Beat Frequency
> $$f_{beat} = 2f_{mod} = \frac{2\omega_{mod}}{2\pi} = \left(\frac{\omega_1}{2\pi} - \frac{\omega_2}{2\pi}\right)= |f_1 - f_2|$$

> [!example]
> Imagine a piano and a tuner with tuning forks.
> 
> Known values:
> $f =$ 261 Hz
> 
> If the tuner hears 6 beats every 2.00 seconds, what are the possible frequencies of the piano key?
> 
> $f_{beat} = |f_1 - f_2|$
> $\pm f_{beat} = f_1 - f_2$
> $f_1 = f_2 \pm f_{beat}$
> $\hspace{5.5mm} = (261) \pm (6 / 2.00)$
> $\hspace{5.5mm} =$ 258 Hz or 264 Hz (depending on $\pm$ sign)