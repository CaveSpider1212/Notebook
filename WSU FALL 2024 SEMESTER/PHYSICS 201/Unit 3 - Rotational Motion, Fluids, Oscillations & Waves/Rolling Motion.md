---
tags: PHYSICS_201
created: 2024-10-21
---

> ![[10.21.24 Rolling Motion Drawing]]
> 
> $\Delta x_{cm} = v_{cm}\Delta t = 2\pi R$
> 
> Rolling constraint:
> $\rightarrow v_{cm} = \frac{2\pi R}{T} = \omega R$ ($\omega = \frac{2\pi}{T}$)

![[10.21.24 Rolling Objects Drawing]]

> [!info]
> The point on the bottom of a rolling object is instantaneously at rest.

Kinetic energy about a point on the bottom is:

$K = \frac{1}{2}I\omega^2$
$\hspace{5.5mm} = \frac{1}{2}(I_{cm} + mR^2)\omega^2$
$\hspace{5.5mm} = \frac{1}{2}I_{cm}\omega^2 + \frac{1}{2}mR^2\omega^2$
$\hspace{5.5mm} = \frac{1}{2}I_{cm}\omega^2 + \frac{1}{2}mv_{cm}^2$ (first term is due to rotation, second term is due to translation)

> [!tip] Kinetic Energy About a Point On the Bottom
> $$K = \frac{1}{2}I_{cm}\omega^2 + \frac{1}{2}mv_{cm}^2$$

> [!example]
> ![[10.21.24 Sphere Drawing]]
> 
> Known values:
> $v =$ 5.0 m/s
> 
> How high does the sphere travel up the incline?
> 
> Conservation of Energy:
> $E_f = E_i$
> $\frac{1}{2}mv_f^2 + \frac{1}{2}I\omega_f^2 + mgy_f = \frac{1}{2}mv_i^2 + \frac{1}{2}I\omega_i^2 + mgy_i$ ($y_i$ = 0 since it starts from the bottom, and $v_f$ and $\omega_f$ are both 0 since it should be at rest when it's at the top)
> $mgy_f = \frac{1}{2}mv_i^2 + \frac{1}{2}(\frac{2}{3}mr^2)(\frac{v}{R})^2$
> $gy_f = \frac{1}{2}v_i^2 + \frac{1}{3}v_i^2$
> $y_f = \frac{5v_i^2}{6g}$
> $\hspace{5.5mm} = \frac{5(5.0)}{6(9.8)}$

### Cross Product

- Dot product (scalar product): $\overrightarrow{A} \cdot \overrightarrow{B} = AB\cos\alpha$
	- see [[Work#^78d923]]

- Cross (vector) product: $\overrightarrow{A} \times \overrightarrow{B} = AB\sin\alpha$
	- Direction given by the right hand rule (use right hand to determine if cross product goes in or out of page)

##### Properties

1. If $\overrightarrow{A}$ and $\overrightarrow{B}$ are parallel, then $\overrightarrow{A} \times \overrightarrow{B} = 0$
2. $\overrightarrow{A} \times \overrightarrow{B} = -\overrightarrow{B} \times \overrightarrow{A}$
3. $\hat{i} \times \hat{j} = \hat{k}, \hat{j} \times \hat{k} = \hat{i}, \hat{k} \times \hat{i} = \hat{j}$
4. $\frac{d}{dt}(\overrightarrow{A} \times \overrightarrow{B}) = \left(\frac{d\overrightarrow{A}}{dt} \times \overrightarrow{B}\right)+ (\overrightarrow{A} \times \frac{d\overrightarrow{B}}{dt})$

### Torque

> [!tip] Torque Formula with Cross Product
> $$\overrightarrow{\tau} = \overrightarrow{r} \times \overrightarrow{F} = \tau = rF\sin\varphi$$
> 
> The torque cross product is directed out of the page.

### Angular Momentum

> [!tip] Angular Momentum Formula with Cross Product
> $$\overrightarrow{L} = \overrightarrow{r} \times \overrightarrow{p} = rp\sin\varphi$$
> 
> The angular momentum cross product is directed out of the page.

Time derivative of $\overrightarrow{L}$:
$\frac{d\overrightarrow{L}}{dt} = \frac{d\overrightarrow{r}}{dt} \times \overrightarrow{p} + \overrightarrow{r} \times \frac{d\overrightarrow{p}}{dt}$
$\hspace{7.5mm} = \overrightarrow{v} \times \overrightarrow{p} + \overrightarrow{r} \times \overrightarrow{F}$
$\hspace{7.5mm} = \overrightarrow{\tau}$

> [!info] Angular Momentum
> - A net torque causes a change in angular momentum
> - Angular momentum is conserved if the net torque is zero.

For a symmetrical object,
$\overrightarrow{L} = I\overrightarrow{\omega}$

> [!example]
> ![[10.21.24 Turntable Drawing]]
> 
> Known values:
> $m_1 =$ 2.0 kg
> $m_2 =$ 500 g each
> $\omega_i =$ 100 rpm
> $d =$ 20 cm
> 
> What is the turntable's angular velocity after the blocks land?
> 
> Conservation of Angular Momentum:
> $L_f = L_i$
> $I_f\omega_{1f} + I_2\omega_{2f} = I_1\omega_{1i} + I_2\omega_{2i}$ ($\omega_{2i}$ = 0 since the blocks don't initially have angular velocity)
> $(I_1 + I_2)\omega_f = I_1\omega_{1i}$
> $\omega_{f} = \frac{I_1}{I_1 + I_2}\omega_{1i}$
> $\hspace{6.5mm} = \frac{\frac{1}{2}m_1R^2}{\frac{1}{2}m_1R^2 + 2m_2R^2} \omega_{1i}$
> $\hspace{6.5mm} = \frac{\frac{1}{2}(2.0)}{\frac{1}{2}(2.0) + 2(0.5)} (100)$
> $\hspace{6.5mm} =$ 50 rpm