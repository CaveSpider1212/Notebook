---
tags: PHYSICS_201
created: 2024-10-4
---

> ![[10.4.24 Force Diagram]]
> 
> Newton's Second Law:
> $F_s = ma_s$
> $F_s = m\frac{dv_s}{dt}$
> $F_s = m\frac{dv_s}{ds}\frac{ds}{dt}$
> $F_s = mv_s\frac{dv_s}{ds}$
> $F_s ds = mv_sdv_s$
> $\int_{s_i}^{s_f} F_s ds = \int_{v_i}^{v_f} mv_sdv_s = \frac{1}{2}mv_f^2 - \frac{1}{2}mv_i^2$
> 
> Define work:
> $W = \int_{s_i}^{s_f} F_sds$
> 
> Define Kinetic Energy:
> $K = \frac{1}{2}mv^2$

> [!tip] Work-Energy Theorem
> $W_{net} = \Delta K$
> 
> Work and energy are measured in joules (J).
> 
> Use this when relating motion to the amount of work, or to the magnitude of the force, distance, and even angle (see Work formula below).

>[!tip] Kinetic Energy Formula
> $$K = \frac{1}{2}mv^2$$

> Consider a constant force
> ![[10.4.24 Constant Force Diagram]]
> 
> $\displaystyle W = \int_{s_i}^{s_f} F_sds = \int_{s_i}^{s_f} F\cos\theta ds = F(\Delta s)\cos\theta$

> Consider a force perpendicular to the motion
> ![[10.4.24 Perpendicular Force Diagram]]
> 
> $W = F(\Delta s)\cos{90\degree} = 0$
> 
> Perpendicular forces to the motion do no work.

> [!tip] Work Formula
> $$W = F\Delta s \cos\theta$$
> 
> Angles (in relation to the direction of motion):
> - Positive when $0\degree < \theta < 90\degree$
> - Negative when $90\degree < \theta < 180\degree$
> - Zero when $\theta = 90\degree$

### Dot Product (Scalar Product)

^78d923

- A way of multiplying two vectors

> ![[10.4.24 Dot Product Diagram]]
> $\overrightarrow{A} \cdot \overrightarrow{B} = AB\cos\alpha$
> 
> Components:
> $\overrightarrow{A} \cdot \overrightarrow{B} = (A_x\hat{i} + A_y\hat{j}) \cdot (B_x\hat{i} + B_y\hat{j})$
> $\hspace{13mm} = A_xB_x(\hat{i} - \hat{i}) + A_xB_y(\hat{i} - \hat{j}) + A_yB_x(\hat{j} - \hat{i}) + A_yB_y(\hat{j} - \hat{j})$
> $\hspace{13mm} = A_xB_x + A_yB_y$
> 
> Therefore,
> $W = \overrightarrow{F} \cdot \Delta \overrightarrow{r}$ (for constant forces)

> [!tip] Work Formula with Dot Product
> $$W = \overrightarrow{F} \cdot \Delta \overrightarrow{r} = F\Delta r \cos\theta$$

> [!example]
> A 1000 kg elevator accelerates upward at 1.0 m/s$^2$ for 10 m, starting from rest.
> 
> Known values:
> $\uparrow \overrightarrow{a} = 1.0$ m/s$^2$
> 
> a) How much work does gravity do on the elevator?
> $W = \overrightarrow{F} \cdot \Delta \overrightarrow{v}$
> $\hspace{6mm} = F(\Delta r)\cos\theta$
> $\hspace{6mm} = mg\Delta r \cos\theta$
> $\hspace{6mm} = (1000)(9.8)(10)\cos{180\degree}$
> $\hspace{6mm} = -98000$ J
> 
> b) How much work does tension do on the elevator?
> 
> Free-body diagram:
> ![[10.4.24 Elevator FBD]]
> 
> Newton's Second Law:
> $T - w = ma_y$
> $T = ma_y + mg$
> $\hspace{4.5mm} = m(a_y + g)\Delta r\cos\theta$
> $\hspace{4.5mm} = (1000)(1.0 + 9.8)(10)\cos{0\degree}$
> $\hspace{4.5mm} = 108000$ J
> 
> c) What is the kinetic energy of the elevator when it reaches 10 m?
> 
> Work-Energy Theorem:
> $W_{net} = \Delta K$
> $W_{g} + W_{T} = K_f - K_i$ ($K_i$ = 0 because the elevator started from rest)
> $K_f = -98000 + 108000 = 10000$ J
> 
> d) What is the speed of the elevator at 10 m?
> $K_f = \frac{1}{2}mv_f^2$
> $v_f = \sqrt{\frac{2K_f}{m}}$
> $\hspace{6mm} = \sqrt{\frac{2(10000)}{1000}}$
> $\hspace{6mm} = 4.47$ m/s

> [!example]
> ![[10.4.24 Box Rope Diagram]]
> 
> How much work is done by each rope if the box is moved 3.0 m to the left?
> 
> $W_1 = \overrightarrow{F}_1 \cdot \Delta\overrightarrow{r}$
> $\hspace{8mm} = T_1\Delta r\cos\theta _1$
> $\hspace{8mm} = (326)(3.0)\cos{160\degree}$
> $\hspace{8mm} = 919$ J
> 
> $W_2 = \overrightarrow{F}_2 \cdot \Delta\overrightarrow{r}$
> $\hspace{8mm} = T_2\Delta r \cos\theta_2$
> $\hspace{8mm} = (225)(3.0)\cos{150\degree}$
> $\hspace{8mm} = -579$ J
> 
> $W_3 = \overrightarrow{F}_3 \cdot \Delta r$
> $\hspace{8mm} = T_3 \Delta r \cos\theta_3$
> $\hspace{8mm} = (500)(3.0)\cos{0\degree}$
> $\hspace{8mm} = 1500$ J