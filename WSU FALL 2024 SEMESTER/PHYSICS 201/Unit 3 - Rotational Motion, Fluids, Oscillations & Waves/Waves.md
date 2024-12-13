---
tags: PHYSICS_201
created: 2024-11-4
---

### Types of Waves

1. **Mechanical wave**: oscillations of some medium
	- Examples: sound waves, water waves, waves on strings
2. **Electromagnetic wave**: oscillations of electromagnetic fields
	- Examples : light, x-rays, radio waves
3. **Matter waves**: particles that exhibit wave-like behavior
	- Examples: electrons, neutrons, protons
4. **Gravitational waves**: oscillations of space time

### Types of Wave Motion

1. **Transverse**: the motion of particles or fields are perpendicular to the direction of motion of the wave

![[11.4.24 Transverse Wave Drawing]]

2. **Longitudinal**: the motion of the particles are parallel to the direction of the motion of the wave.

![[11.4.24 Longitudinal Wave Drawing]]

You can have a combination of transverse and longitudinal (water).

### Snapshot Graph

![[11.4.24 Snapshot Graph Drawing]]

### History Graph

![[11.4.24 History Graph Drawing]]

### Displacement

$D(x, t)$: the displacement at some time, $t$, of a particle at position $x$

For a wave that does not change shape:
$D(x, t) = D(x - vt)$ when the wave is traveling $+x$
$D(x, t) = D(x + vt)$ when the wave is traveling $-x$

### Sinusoidal Waves

##### History Graph

![[11.4.24 Sinusoidal History Graph]]

$$\lambda = vT$$
$$v = \frac{\lambda}{T} = \lambda f$$

##### Snapshot Graph

![[11.4.24 Sinusoidal Snapshot Graph]]

Imagine a sine graph with a peak at A above x and x + $\lambda$(?) and a valley in between those two.

$D(x, t = 0) = A\sin({2\pi \frac{x}{\lambda} + \varphi_o})$
$\rightarrow D(x + 2, t = 0) = A\sin({2\pi \frac{x + 2}{\lambda} + \varphi_o})$
$\rightarrow A\sin({2\pi \frac{x}{\lambda} + \varphi_o + 2\pi})$
$= A\sin\left({2\pi \frac{x}{\lambda} + \varphi_o}\right)= D(x, t = 0)$

Also, $D(x, t) = A\sin\left({2\pi \frac{x - vt}{\lambda} + \varphi_o}\right)= A\sin\left({2\pi \left(\frac{x}{\lambda} - \frac{t}{T}\right)+ \varphi_o}\right)$

Define angular frequency: $\omega = \frac{2\pi}{T}$
Wave number: $k = \frac{2\pi}{\lambda}$

$\rightarrow D(x, t) = A\sin({kx - \omega t + \varphi_o})$

Also,
$$v = 2f = (\frac{2\pi}{k})\left(\frac{\omega}{2\pi}\right)= \frac{\omega}{k}$$

### Strings

$$v = \sqrt{\frac{T}{\mu}}$$

$T$: tension
$\mu$: linear mass density

> [!example]
> Known values:
> $T =$ 50 N
> $\mu =$ 5 g/m = 0.005 kg/m
> $A =$ 3.0 cm = 0.03 m
> $\lambda =$ 2.0 m
> 
> a) What is the speed of the wave on the string?
> $v = \sqrt{\frac{T}{\mu}}$
> $\hspace{3.5mm} = \sqrt{\frac{50}{0.005}} =$ 100 m/s
> 
> b) What is the maximum speed of the particle of the string?
> $v_{max} = \omega A = (vk)(A)$
> $\hspace{10mm} = \frac{2\pi v}{\lambda}A$
> $\hspace{10mm} = \frac{2\pi (100)}{2.0}(0.03)$
> $\hspace{10mm} =$ 9.92 m/s

> [!example]
> Known values:
> $T =$ 20 N
> $t =$ 50 ms = 0.050 s
> $L =$ 2.0 m
> 
> What is the mass of the string?
> 
> $v = \sqrt{\frac{T}{\mu}}$
> $\frac{L}{t} = \sqrt{\frac{T}{\frac{m}{L}}}$
> $m = \frac{Tt^2}{L}$ (from rearranging terms around)
> $\hspace{5mm} = \frac{(20)(0.050)}{2.0} =$ 25 g