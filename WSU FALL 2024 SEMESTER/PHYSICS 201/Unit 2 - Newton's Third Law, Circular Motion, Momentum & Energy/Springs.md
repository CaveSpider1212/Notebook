---
tags: PHYSICS_201
created: 2024-10-9
---

- **Springs**:  possess a restoring force

![[10.9.24 Spring Force Drawing]]

> [!tip] Hooke's Law
> $$F_{sp} = -k\Delta s$$
> 
> $k$: spring constant
> $\Delta s$: displacement from equilibrium

^735f02

### Elastic Potential Energy

> ![[10.9.24 Elastic Potential Drawing]]
> 
> Newton's Second Law:
> $F_{sp} = ma$
> $-k\Delta s = m\frac{dv}{dt}$
> $-k\Delta s ds = mv dv$
> $\frac{-1}{2}k(\Delta s_f)^2 + \frac{1}{2}k(\Delta s_i)^2 = \frac{1}{2}mv_f^2 - \frac{1}{2}mv_f^2$
> 
> Define the elastic potential energy:
> $u = \frac{1}{2}k(\Delta s)^2$

> [!tip] Elastic Potential Energy Formula
> $$u = \frac{1}{2}k(\Delta s)^2$$
> 
> Add this to the Conservation of Energy equation if there are springs involved (see [[Potential Energy#^7ee0d5]] for other stuff in Conservation of Energy).

> [!example]
> A vertical spring with K = 490 N/m is standing on the ground. You are holding a 5.0 kg block just above the spring.
> 
> a) How far does the spring compress if we let go of the block suddenly?
> 
> ![[10.9.24 Block Spring Drawing]]
> 
> Conservation of Energy:
> $E_f = E_i$
> $\frac{1}{2}mv_f^2 + mgy_f + \frac{1}{2}k(\Delta s_f)^2 = \frac{1}{2}mv_i^2 + mgy_i + \frac{1}{2}k(\Delta s_i)^2$ ($v_i$ = 0 since it starts from rest, $s_i$ = 0 since there is no compression in the beginning, $v_f$ = 0 since the block would also have no velocity at the end, $y_f$ = 0 based on the picture)
> $\frac{1}{2}k(\Delta s_f)^2 = mgy_i$ ($\Delta s_f = y_i$ )
> $\frac{1}{2}k(y_i)^2 = mgy_i$
> $y_i = \frac{2mg}{k}$
> $\hspace{5mm} = \frac{2(5.0)(9.8)}{490}$
> $\hspace{5mm} =$ 0.20 m
> 
> b) How far does the spring compress if we slowly lower the block?
> 
> Energy is not conserved (because our hand is involved now).
> 
> Free-body diagram:
> ![[10.9.24 Block Spring FBD]]
> 
> Newton's Second Law:
> $F_{sp} - w = ma_y$ ($a_y$ = 0 since there is no acceleration)
> $k\Delta s - mg = 0$
> $\Delta s = \frac{mg}{k} =$ 0.10 m

### Conservation of Energy

- **Conservative force**: a force for which the work done on the particle is independent of the path

> ![[10.9.24 Conservative Forces Drawing]]
> 
> $w_1 = \overrightarrow{F} \cdot \Delta \overrightarrow{r}$
> $\hspace{7mm} = mgl\cos({\theta + 90\degree})$
> $\hspace{7mm} = -mgl\sin\theta$
> $\hspace{7mm} = -mgl(\frac{h}{l})$
> $\hspace{7mm} = -mgh$
> 
> $w_2 = \overrightarrow{F} \cdot \Delta \overrightarrow{r}$
> $\hspace{7mm} = -mgh$

> [!info]
> By the work-energy theorem, $\Delta K = w$ and by conservation of energy ($\Delta K = -\Delta u$), then $\Delta u = -w_c$ for a conservative force.

- **Nonconservative force**: a force for which the work done is dependent upon the path
	- Friction is a nonconservative force

> ![[10.9.24 Nonconservative Force Drawing]]
> 
> Path 1:
> $w_1 = \overrightarrow{F} \cdot \Delta \overrightarrow{r}$
> $\hspace{7mm} = \mu_k mg (L\sqrt{2})\cos{180\degree}$
> 
> Path 2:
> $w_2 = \overrightarrow{F} \cdot \Delta \overrightarrow{r}$
> $\hspace{7mm} = \mu_k mg(2L)\cos{180\degree}$

> [!tip] Work-Energy Theorem
> 
> $\Delta K = w_{net} = w_c + w_{nc}$
> $\Delta K = -\Delta u + w_{nc}$
> $\Delta K + \Delta u = w_{nc}$
> $\rightarrow \Delta E_{mech} = \Delta K + \Delta u = w_{nc}$ ($E_{mech}$: mechanical energy)
> 
> Therefore, if $w_{nc} = 0$, then $\Delta E_{mech} = 0$, i.e. the mechanical energy is conserved.

> [!example]
> ![[10.9.24 Block Slope Drawing]]
> 
> Known values:
> $m =$ 50 g
> $K =$ 25 N/m
> $\mu_k =$ 0.20
> 
> How far will the block travel up the slope?
> 
> $\Delta K + \Delta u = w_{nc}$ ($\Delta K$ = 0 because the block is at rest both in the beginning and in the end)
> $mgy_f + \frac{1}{2}k(\Delta s_f)^2 - mgy_i - \frac{1}{2}k(\Delta s_i)^2 = \overrightarrow{f}_k \cdot \Delta \overrightarrow{r}$ ($s_f$ = 0)
> $mgy_f - \frac{1}{2}k(\Delta s_i)^2 = (\mu_k mg \cos\theta)\Delta r \cos{180\degree}$ (it is 180 degrees because there is 180 degrees between the $\Delta \overrightarrow{r}$ and $\overrightarrow{f}_k$ vectors)
> $mg \Delta r \sin\theta - \frac{1}{2}k(\Delta s_i)^2 = -\mu_k mg \Delta r \cos\theta$
> $\Delta r = \frac{\frac{1}{2}k(\Delta s_i)^2}{mg(\sin\theta + \mu_k \cos\theta)}$
> $\hspace{7.5mm} = \frac{\frac{1}{2}(25)(0.10)^2}{(0.050)(9.8)(\sin{30\degree} + (0.20)\cos{30\degree})}$
> $\hspace{7.5mm} =$ 0.379 m