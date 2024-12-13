---
tags: PHYSICS_201
created: 2024-09-27
---

> [!example]
> ![[9.27.24 Bucket Drawing]]
> 
> Known values:
> $m =$ 4.5 kg
> $r =$ 1.1 m
> 
> What minimum speed must the bucket have if it is to complete the circle without spilling any water?
> 
> Free-body diagram (at the top of the circle):
> ![[9.27.24 Bucket FBD]]
> 
> Newton's Second Law:
> $n + w = ma_r$ ($n \rightarrow 0$ when the water loses contact with bucket)
> $mg = m\frac{v^2}{r}$
> $v = \sqrt{gr} = \sqrt{(9.8)(1.1)} =$ 3.3 m/s

> [!example]
> A student ties a 500 g rock to a 1.0 m string and swings it around her head in a horizontal circle. At what angular velocity in rpm does the string tilt down at a 10$\degree$ angle?
> 
> ![[9.27.24 String Drawing]]
> 
> Free-body diagram:
> ![[9.27.24 String FBD]]
> 
> Newton's Second Law:
> <u>r-component</u>
> $T_r = ma_r$
> $T\cos\theta = m\omega ^2 r$ ($\omega$: angular velocity...see [[Circular Motion]])
> $(\frac{mg}{\sin\theta})\cos\theta = m\omega^2r$
> $\omega = \sqrt{\frac{g\cos\theta}{r\sin\theta}}$ ($r = l\cos\theta$ using trigonometry, and $l$ is the length of the string))
> $\hspace{4mm} = \sqrt{\frac{g\cos\theta}{(l\cos\theta)\sin\theta}}$
> $\hspace{4mm} = \sqrt{\frac{9.8}{(1.0)\sin{10\degree}}} = 7.5$ rad/s
> 
> <u>z-component</u>
> $T_z - w = ma_z$ ($a_z$ = 0 since there is no acceleration in the z-direction, only in the r-direction, left to right)
> $T\sin\theta - mg = 0$
> $T = \frac{mg}{\sin\theta}$ (use in r-component part)
> 
> Answer in rad/s: 7.5
> Answer in rpm: $7.5 * (\frac{1 rev}{2\pi rad})\left(\frac{60 s}{1 min}\right) = 72$ rpm

> [!example]
> ![[9.27.24 Rocket Drawing]]
> 
> Known values:
> $m =$ 0.50 kg
> $F_{thrust} =$ 4.0 N
> 
> The maximum tension the tube can withstand without breaking is 50 N. If the rocket starts at rest, how many revolutions does it make before the tube breaks?
> 
> Free-body diagram:
> ![[9.27.24 Rocket FBD]]
> 
> Newton's Second Law:
> <u>r-component</u>
> $T = ma_r = m\omega^2r$
> $\omega = \sqrt{\frac{T}{mr}}$
> $\hspace{4mm} = \sqrt{\frac{50}{(0.50)(1.2)}} =$ 9.1 rad/s
> 
> <u>t-component</u>
> $F_{thrust} = ma_t$
> $a_t = \frac{F_{thrust}}{m}$
> $\hspace{5mm} = \frac{4.0}{0.50} =$ 8.0 m/s$^2$
> 
> Kinematic Equations:
> $\omega_f^2 = \omega_i^2 + 2\alpha\Delta\theta$ (see [[Circular Motion]] for meaning of the symbols)
> $\Delta\theta = \frac{\omega_f^2}{2\alpha_t / r}$
> $\hspace{7mm} = \frac{(9.1)^2}{2(8.0) /(1.2)}=$ 6.2 rad ~~ 1.0 revolution

> [!example]
> A 1500 kg car starts from rest and drives around a flat 50m-diameter circular track. The forward force is 1000 N.
> 
> a) What is the magnitude and direction of the car's acceleration at t = 10 s?
> 
> ![[9.27.24 Car Drawing]]
> 
> Free-body diagram (top-view):
> ![[9.27.24 Car FBD]]
> 
> Newton's Second Law:
> <u>r-component</u>
> $f_s = ma_r = m\omega^2r$
> 
> <u>t-component</u>
> $F = ma_t$
> $a_t = \frac{F}{m}$
> $\hspace{5mm} = \frac{1000}{1500} =$ 0.67 m/s$^2$
> 
> Kinematic Equations:
> The angular velocity after 10 s is
> $\omega_f = \omega_i + \alpha\Delta t = \frac{a_t}{r}\Delta t$ ($\omega_i$ = 0 since it starts from rest)
> $\hspace{7mm} = \frac{0.67}{25}(10)$
> $\hspace{7mm} =$ 0.27 rad/s
> 
> The radial acceleration is
> $a_r = \omega^2r = (0.27)^2(25) =$ 1.8 m/s$^2$
> 
> The magnitude of the car's acceleration is
> $a = \sqrt{a_r^2 + a_t^2} =$ 1.9 m/s$^2$
> 
> The direction of the acceleration is
> ![[9.27.24 Acceleration Graph]]
> $\theta = \tan^-1\left(\frac{a_r}{a_t}\right) = 20\degree$