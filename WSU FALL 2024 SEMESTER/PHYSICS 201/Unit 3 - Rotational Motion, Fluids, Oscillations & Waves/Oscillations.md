---
tags: PHYSICS_201
created: 2024-10-30
---

```desmos-graph
left = -1; right = 10;
top = 1.5; bottom = -1.5;
---
y = \cos(x)
```

- **Period** (T): length of the oscillation (from one valley to the next valley)
- **Amplitude** (A): height of the oscillation from the equilibrium point to the peak
- **Frequency** (f): amount of oscillations per unit of time
	- $f = \frac{1}{T}$
	- SI unit: 1 Hz = 1/1s

### Simple Harmonic Motion (SHM)

##### Position

$x(t) = A\cos(\frac{2\pi t}{T})$
$\hspace{9.5mm} = A\cos({2 \pi f t})$
$\hspace{9.5mm} = A\cos({\omega t})$

where $\omega = 2 \pi f = \frac{2\pi}{T}$ (angular frequency)

> [!tip] Position Formula
> $$x(t) = A\cos({\omega t})$$

> [!tip] Angular Frequency
> $$w = 2 \pi f = \frac{2 \pi}{T}$$

##### Velocity

$v(t) = \frac{dx(t)}{dt}$
$\hspace{9.5mm} = \frac{-2\pi A}{T}\sin({\frac{2\pi t}{T}})$
$\hspace{9.5mm} = -2\pi f A \sin({2\pi ft})$
$\hspace{9.5mm} = -\omega A \sin({\omega t})$

$v_{max} = \frac{2\pi A}{T} = 2\pi f A = \omega A$

> [!tip] Velocity Formulas
> 
> $$v(t) = -\omega A \sin({\omega t})$$
> $$v_{max} = \frac{2\pi A}{T} = 2\pi f A = \omega A$$

> [!info] Important
> When $x_f = 0$, $v = v_{max}$ (maximum velocity when $x_f$ is 0).
> When $x_f = A$, $v = 0$ (no velocity when $x_f$ is the amplitude).

### Circular Motion

![[10.30.24 Circular Motion Drawing]]

$x = A\cos{\varphi}$
where $\varphi(t) = \varphi_{0} + \omega t$

$x(t) = A\cos({\omega t + \varphi_0})$
$v(t) = -\omega A \sin({\omega t + \varphi_0})$

### Initial Angle

> [!tip] Initial Angle Formulas
> $x(t = 0) = A \cos{\varphi_0} \rightarrow \varphi_0 = \cos^{-1}({\frac{x(t = 0)}{A}})$
> $v(t = 0) = -\omega A \sin{\varphi_0} \rightarrow \varphi_0 = \sin^{-1}({\frac{-v(t = 0)}{\omega A}})$

### Energy

```desmos-graph
top = 10; bottom = -5;
---
y = 0.5x^2
y = 8
(-4, 8) | label: Turning point (-A)
(4, 8) | label: Turning point (A)
```

Blue line is potential energy ($u = \frac{1}{2}kx^2$), and green line is total energy ($E = \frac{1}{2}mv^2 + \frac{1}{2}kx^2$).

Thus,
At $x = \pm A \rightarrow E = u = \frac{1}{2}kA^2$
At $x = 0 \rightarrow E = k = \frac{1}{2}mv_{max}^2$

Since energy is conserved
$\frac{1}{2}kA^2 = \frac{1}{2}mv_{max}^2$
$\rightarrow v_{max} = A\sqrt{\frac{k}{m}}$

> [!tip] Maximum Velocity (from kinematics)
> $$v_{max} = \frac{2\pi A}{T} = 2\pi f A = \omega A$$

Therefore,
> [!tip] Oscillation Variables with Energy
> $$\omega = \sqrt{\frac{k}{m}}$$
> $$f = \frac{1}{2\pi}\sqrt{\frac{k}{m}}$$
> $$T = 2\pi \sqrt{\frac{m}{k}}$$

> [!example]
> Imagine a spring with some sort of object attached to it.
> 
> Known values:
> $k =$ 2.5 N/m
> $m =$ 100 g = 0.100 kg
> $x_i =$ -5.0 cm
> $v_i =$ 20 cm/s
> 
> a) What is the amplitude of the oscillation?
> 
> Conservation of Energy:
> $E_f = E_i$
> $\frac{1}{2}mv_f^2 + \frac{1}{2}kx_f^2 = \frac{1}{2}mv_i^2 + \frac{1}{2}kx_i^2$ ($v_f$ = 0 because the velocity is 0 at maximum displacement)
> $\frac{1}{2}kA^2 = \frac{1}{2}mv_i^2 + \frac{1}{2}kx_i^2$
> $A = \sqrt{\frac{m}{k}v_i^2 + x_i^2}$
> $\hspace{4.5mm} = \sqrt{\frac{0.100}{2.5}(20)^2 + (-5.0)^2}$
> $\hspace{4.5mm} =$ 6.4 cm
> 
> b) What is the speed of the mass when x = 3.0 cm?
> 
> Conservation of Energy:
> $E_f = E_i$
> $\frac{1}{2}mv_f^2 + \frac{1}{2}kx_f^2 = \frac{1}{2}mv_i^2 + \frac{1}{2}kx_i^2$
> $v_f = \sqrt{v_i^2 + \frac{k}{m}(x_i^2 - x_f^2)}$
> $\hspace{6mm} = \sqrt{(20)^2 + \frac{2.5}{0.100}((-5.00)^2 - (3.00)^2)}$
> $\hspace{6mm} =$ 28.3 cm/s

> [!example]
> (#6)
> Imagine a spring with an object attached to it that can "stretch" and oscillate with the known values below.
> 
> Known values:
> $m =$ 300 g = 0.300 kg
> $x_i$ = 3.0 cm
> $x_f =$ 6.0 cm
> $v_i =$ 95.4 cm/s
> $v_f =$ 71.4 cm/s
> 
> What is the oscillator's maximum speed?
> First, find $k$.
> 
> Conservation of Energy:
> $E_f = E_i$
> $\frac{1}{2}mv_f^2 + \frac{1}{2}kx_f^2 = \frac{1}{2}mv_i^2 + \frac{1}{2}kx_i^2$
> $k = \frac{m(v_i^2 - v_f^2)}{x_f^2 - x_i^2}$
> $\hspace{3.75 mm} = \frac{(0.300)((95.4)^2 - (71.4)^2)}{(6.00)^2 - (3.00)^2}$
> $\hspace{3.75mm} =$ 44.5 N/m
> 
> Next, find $v_{max}$.
> 
> Conservation of Energy:
> $E_f = E_i$
> $\frac{1}{2}mv_f^2 + \frac{1}{2}kx_f^2 = \frac{1}{2}mv_i^2 + \frac{1}{2}kx_i^2$ ($x_f$ = 0 since that gets us the maximum velocity)
> $\frac{1}{2}mv_{max}^2 = \frac{1}{2}mv_i^2 + \frac{1}{2}kx_i^2$
> $v_{max} = \sqrt{v_i^2 + \frac{k}{m}x_i^2}$
> $\hspace{11mm} = \sqrt{(95.4)^2 + \frac{44.5}{0.300}(3.00)^2}$
> $\hspace{11mm} =$ 102.2 cm/s

### Dynamics of SHM

> [!info] Dynamics of Simple Harmonic Motion
> Position: $x(t) = A\cos({\omega t + \varphi_0})$
> Velocity: $v(t) = \frac{dx}{dt} = -\omega A\sin({\omega t + \varphi_0})$
> Acceleration: $a(t) = \frac{dv}{dt} = -\omega^2 A\cos({\omega t + \varphi_0}) = -\omega^2 x(t)$

### Newton's Second Law for Springs

$F = ma$
$-kx = m\frac{d^2x}{dt^2}$
$\frac{d^2x}{dt^2} = \frac{-k}{m}x$ <--- equation of motion

$\rightarrow x(t) = A\cos({\omega t + \varphi_0})$
where $\omega = \sqrt{\frac{k}{m}}$

### Note on Conservation of Energy

> [!info] Important
> When doing Conservation of Energy for oscillations:
> - $v$ should equal $v_{max}$ when $s$ is 0, so set one side of the terms (either $v_i$ and $\Delta s_i$ or $v_f$ and $\Delta s_f$) to $v = v_{max}$ and $s = 0$
> - $v$ should equal 0 when $s$ is the amplitude, or maximum displacement, so set the other side of the terms to $v = 0$ and $s = A$