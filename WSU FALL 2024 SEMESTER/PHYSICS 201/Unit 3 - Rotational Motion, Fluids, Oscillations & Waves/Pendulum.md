---
tags: PHYSICS_201
created: 2024-11-1
---

>![[11.1.24 Pendulum Drawing]]
> 
> Free-body diagram:
> ![[11.1.24 Pendulum FBD]]
> 
> Newton's Second Law (t-component only):
> $-w_t = ma_t$
> $-mg\sin\theta = m \frac{d^2s}{dt^2}$
> 
> ![[11.1.24 Pendulum Triangle Drawing]]
> 
> For small angles
> $r\sin\theta \approx r\theta$
> $\sin\theta \approx \theta$ ($\theta$ in radians)
> 
> Therefore,
> $-mg\sin\theta = -mg$$\theta = m \frac{d^2(L\theta)}{dt^2}$
> $\frac{d^2\theta}{dt^2} = \frac{-g}{L}\theta$
> $\rightarrow \theta(t) = \theta_{max} \cos({\omega t + \varphi_o})$ or $s(t) = A\cos({\omega t + \varphi_o})$ where $\omega = \sqrt{\frac{g}{L}}$

> [!info] Important
> The frequency or the period of a pendulum is independent of the mass and amplitude for small angles.

> [!example]
> ![[11.1.24 Circle Pendulum Drawing]]
> 
> What is the frequency for small oscillations?
> 
> Conservation of Energy:
> $E_f = E_i$
> $\frac{1}{2}mv_f^2 + mgy_f = \frac{1}{2}mv_i^2 + mgy_i$ ($y_f$ = 0 since the final position is 0, and we assume the pendulum started at rest so $v_i$ = 0)
> $\frac{1}{2}v_f^2 = g(2L)$ ($y_i$ = 2L based on the drawing)
> $L = \frac{1}{4}\frac{v_f^2}{g}$
> $\hspace{4mm} = \frac{(5.00)^2}{4 * 9.8}$
> $\hspace{4mm} =$ 0.64 m
> 
> The frequency is
> $\omega = 2 \pi f = \sqrt{\frac{g}{L}}$
> $f = \frac{1}{2\pi} \sqrt{\frac{g}{L}}$
> $\hspace{4mm} = \frac{1}{2\pi} \sqrt{\frac{9.8}{0.64}}$
> $\hspace{4mm} =$ 0.62 Hz

### Damped Oscillations

> ![[11.1.24 Damped Oscillation Graph]]
> 
> ![[11.1.24 Damped Oscillation Diagram]]
> 
> Let $\overrightarrow{D} = -b \overrightarrow{v}$
> - $b$: damping constant
> 
> Newton's Second Law:
> $-F_{sp} - D = ma$
> $-kx - bv = ma$
> $-kx - b \frac{dx}{dt} = m \frac{d^2x}{dt^2}$
> $\frac{d^2x}{dt^2} + \frac{b}{m} \frac{dx}{dt} + \frac{k}{m} x = 0$
> $\rightarrow x(t) = Ae^{\frac{-bt}{2m}} \cos({\omega t + \varphi_o})$
> where $\omega = \sqrt{\frac{k}{m} - \frac{b^2}{4m^2}} = \sqrt{w_o^2 - \frac{b^2}{4m^2}}$
> - Undamped frequency: $\omega_o = \sqrt{\frac{k}{m}}$
> 
> Amplitude (envelope):
> $x_{max}(t) = Ae^{\frac{-bt}{2m}}$
> 
> ![[11.1.24 Amplitude with b Graph]]

##### Energy

Define the time constant $\tau = \frac{m}{b}$

Thus,
$E(t) = \frac{1}{2}kx_{max}^2 = \frac{1}{2}k(Ae^{\frac{-t}{2\tau}})^2$
$\hspace{8mm} = (\frac{1}{2}kA^2)e^{\frac{-T}{\tau}} = E_o e^{\frac{-T}{\tau}}$
where $E_o = \frac{1}{2}kA^2$ is the initial energy

![[11.1.24 Time Graph]]

> [!example]
> Imagine a "ball" on a spring rocking back and forth (like a bobblehead).
> 
> Known values:
> $m =$ 15 g = 0.015 kg
> $f =$ 4.0 Hz
> At $t =$ 0: $A =$ 2.0 cm
> At $t =$ 4.0 s: $A =$ 0.5 cm
> 
> a) What is the spring constant?
> $\omega = \sqrt{\frac{k}{m}}$
> $k = m\omega^2$
> $\hspace{4mm} = m(2\pi f)^2$
> $\hspace{4mm} = (0.015)(2\pi (4.0))^2$
> $\hspace{4mm} =$ 9.47 N/m
> 
> b) At t = 0, what is the ball's maximum speed?
> $v_{max} = \omega A = 2\pi f A$
> $\hspace{11mm} = 2\pi(4.0)(2.0)$
> $\hspace{11mm} =$ 50.3 cm/s
> 
> c) What is the damping constant?
> $x_{max} = Ae^{\frac{-bt}{2m}}$
> $\frac{x_{max}}{A} = e^{\frac{-bt}{2m}}$
> $\ln\left({\frac{x_{max}}{A}}\right) = \frac{-bt}{2m}$
> $b = \frac{-2m}{t} \ln({\frac{x_{max}}{A}})$
> $\hspace{4mm} = \frac{-2(0.015)}{4.0} \ln({\frac{0.5}{2.0}})$
> $\hspace{4mm} =$ 0.0104 kg/s

### Driven Oscillator

- Applying a periodic external force

**Driving frequency**: frequency at which the force is applied ($f_{ext}$)
**Natural frequency**: frequency of the oscillator ($f_o$)

Response curve:
![[11.1.24 Response Curve Graph]]