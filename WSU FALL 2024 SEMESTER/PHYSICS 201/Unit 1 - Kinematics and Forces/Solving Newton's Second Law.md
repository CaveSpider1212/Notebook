---
tags: PHYSICS_201
created: 2024-09-09
---


> [!example]
> **A 50 kg box hangs from a rope. What is the tension in the rope if...**
> 
> *a) the box is at rest?*
> 
> Free-body diagram:
> ![[9.9.24 Box FBD]]
> 
> Apply Newton's Second Law:
> $\sum F_y = ma_y$
> $T - w = ma_y$ ($a_y$ = 0 because it is at rest)
> $T = w = mg =$ (50 kg)(9.80 m/s$^2$) = 490 N
> 
> b) *the box moves up at a steady 5.0 m/s$^2$?*
> 
> $T - w = ma_y$ ($a_y$ = 0 because it is not accelerating, the velocity is constant)
> $T = w =$ 490 N
> 
> c) *the box has $v_y$ = 5.0 m/s and is speeding up at 5.0 m/s$^2$?*
> 
> $T - w = ma_y$
> $T = w + ma_y =$ (490 N) + (50 kg)(5.0 m/s$^2$) = 740 N
> 
> d) *the box has $v_y$ = 5.0 m/s and is slowing down at 5.0 m/s$^2$?*
> 
> $T - w = ma_y$
> $T = w + ma_y$ = (490 N) + (50 kg)(-5.0 m/s$^2$) = 240 N

> [!example]
> **A football coach sits on a sled while two players drag him with ropes. The friction force is 1000 N and the angle between the ropes is 20$\degree$. How hard must the players pull the coach at a steady 2.0 m/s?**
> 
> Free-body diagram (top view):
> ![[9.9.24 Sled FBD]]
> 
> Newton's Second Law:
> x-component:
> $\sum F_x = ma_x$
> $T_{1x} + T_{2x} - f_k = ma_x$ ($a_x$ = 0 because the velocity is steady)
> $T_1\cos\theta + T_2\cos\theta - f_k = 0$
> $2T_1\cos\theta = f_k$
> 
> y-component:
> $\sum F_y = ma_y$
> $T_{1y} - T_{2y} = ma_y$ ($a_y$ = 0 because the velocity is steady)
> $T_1\sin\theta - T_2\sin\theta = 0$
> $T_1 = T_2$
> 
> Combined:
> $T_1 = \frac{f_k}{2\cos\theta}$
> $\hspace{6mm} = \frac{1000 N}{2\cos{10\degree}}$
> $\hspace{6mm} = 508$ N

> [!example]
> **A 1.0 g plastic ball is suspended on a 60-cm-long string and given an electric charge. A charge rod brought near the ball exerts a horizontal force, $F_{elect}$, on it, causing the ball to swing out to a 20$\degree$ angle and remain there.**
> 
> Pictorial Diagram:
> ![[9.9.24 Ball Drawing]]
> 
> Free-body Diagram:
> ![[9.9.24 Ball FBD]]
> 
> *a) What is the magnitude of $F_{elect}$?*
> 
> *b) What is the tension in the string?*
> 
> x-component:
> $T_x - F_{elect} = ma_x$ ($a_x$ = 0 because the ball is just "sitting there")
> $T\sin\theta - F_{elect} = 0$
> $T\sin\theta = F_{elect}$
> $F_{elect} = (0.010)\sin{20\degree}$
> $\hspace{12mm} = 0.0034$ N
> 
> y-component:
> $T_y - w = ma_y$ ($a_y$ = 0 because the ball is just "sitting there")
> $T\cos\theta - mg = 0$
> $T = \frac{mg}{\cos\theta}$
> $\hspace{5mm} = \frac{(0.001)(9.8)}{\cos{20\degree}}$
> $\hspace{5mm} = 0.010$ N (use this number in the x-component part)

> [!example]
> A 1000 kg steel beam is supported by two ropes. Each rope has a maximum sustained tension of 6000 N. Does either rope break?
> 
> Picture:
> ![[9.9.24 Beam Drawing]]
> 
> Free-body Diagram:
> ![[9.9.24 Beam FBD]]
> 
> Newton's Second Law:
> x-component:
> $T_{2x} - T_{1x} = ma_x$ ($a_x$ = 0 because there is no acceleration on the ropes)
> $T_2\sin\theta _2 - T_1\sin\theta _1 = 0$
> $T_1 = T_2\frac{\sin\theta _2}{\sin\theta _1}$ (use in y-component part)
> $\hspace{6mm} = 6400$ N
> 
> y-component:
> $T_{1y} + T_{2y} - w = ma_y$ ($a_y$ = 0 because there is no acceleration on the rope)
> $T_1\cos\theta _1 + T_2\cos\theta _2 - mg = 0$
> $(T_2\frac{\sin\theta _2}{\sin\theta _1})\cos\theta _1 + T_2\cos\theta _2 - mg = 0$
> $T_2 = \frac{mg}{\frac{\sin\theta _2}{\sin\theta _1}\cos\theta _1 + \cos\theta _2}$
> $\hspace{6mm} = \frac{(1000)(9.8)}{\frac{\sin{30\degree}}{\sin{20\degree}}\cos{20\degree} + \cos{30\degree}}$
> $\hspace{6mm} = 4400$ N (use in x-component part)
> 
> Since $T_1$ is 6400 N, and is greater than 6000 N, rope 1 will break.