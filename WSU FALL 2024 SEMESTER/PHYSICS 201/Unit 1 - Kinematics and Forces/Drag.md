---
tags: PHYSICS_201
created: 2024-09-13
---

### Drag

- **Drag**: a resistive force through a gas or liquid
	1. Points in the opposite direction of the velocity
	2. Depends upon the cross-section area and velocity

> [!tip] Drag Formula
> $D = \displaystyle\frac{1}{2}C\rho Av^2$ for objects moving in air near the earth's surface
>	- $C$: coefficient of drag
>	- $\rho$: density of air
>	- $A$: cross-section area
>	- $v$: velocity

![[9.13.24 Cross Section Areas]]

> [!example]
> Minimum velocity to keep the paper from falling
> 
> Free-body diagram:
> ![[9.13.24 Paper FBD]]
> 
> Newton's Second Law:
> <u>x-component</u>
> $n - D = ma_x$ ($a_x$ = 0 because the speed of the paper is steady)
> $n - \frac{1}{2}C\rho A v^2= 0$
> $\frac{mg}{\mu _s} - \frac{1}{2}C\rho A v^2 = 0$
> $v = \sqrt{\frac{2mg}{C\rho A \mu _s}}$
> 
> <u>y-component</u>
> $f_s - w = ma_y$ ($a_y$ = 0 because the speed of the paper is steady)
> $\mu _s n - mg = 0$
> $n = \frac{mg}{\mu _s}$ (use in x-component part)
> 
> Minimum velocity found using $v = \displaystyle\sqrt{\frac{2mg}{C\rho A \mu _s}}$.

### Terminal Velocity

- **Terminal velocity**: maximum velocity an object gains because of drag forces
	- Essentially where the force due to drag is equal to the force due to weight (as shown below)

> Consider a falling object.
> 
> Free-body diagram:
> ![[9.13.24 Falling FBD]]
> 
> Newton's Second Law:
> $D - w = ma_y$ ($a_y$ = 0 because we would be at terminal velocity, so no acceleration)
> $\frac{1}{2}C\rho A v^2 - mg = 0$
> $v_{term} = \sqrt{\frac{2mg}{C\rho A}}$

> [!tip] Terminal Velocity Formula
> $v_{term} = \displaystyle\sqrt{\frac{2mg}{C\rho A}}$

> [!example]
> What is the terminal velocity of a skydiver?
> 
> ![[9.13.24 Skydive Diagram]]
> 
> Face down: $A$ = (0.40 m)(1.80 m) = 0.72 m$^2$
> $v_{term} = \sqrt{\frac{2mg}{C\rho A}} = \sqrt{\frac{2(75)(9.80)}{(0.8)(1.2)(0.72)}}$ = 100 m/s or about 100 mph
> 
> Feet down: $A$ = (0.40 m)(0.20 m) = 0.080 m$^2$
> $v_{term} = \sqrt{\frac{2mg}{C\rho A}} = \sqrt{\frac{2(75)(9.80)}{(0.8)(1.2)(0.080)}}$ = 138 m/s or about 310 mph

> [!example]
> What is the terminal velocity of an 80 kg skier going down a 40$\degree$ snow-covered slope on wooden skis? Assume that the skier is 1.8 m tall and 0.40 m wide and the drag coefficient is 1.1.
> 
> ![[9.13.24 Ski Drawing]]
> 
> Free-body diagram:
> ![[9.13.24 Ski FBD]]
> 
> Newton's Second Law:
> <u>x-component</u>
> $w_x - D - f_k = ma_x$ ($a_x$ = 0 because we're at terminal velocity)
> $mg\sin\theta - \frac{1}{2}C\rho Av^2 - \mu _k n = 0$
> $mg(\sin\theta - \mu _k \cos\theta) = \frac{1}{2}C\rho Av^2$
> $v = \sqrt{\frac{2mg(\sin\theta - \mu _k \cos\theta)}{C\rho A}}$
> $\hspace{4mm} = \sqrt{\frac{2(80)(9.8)(\sin{40\degree}-(0.12)\cos{40\degree})}{(1.1)(1.2)(1.80)(0.40)}}$ = 30 m/s
> 
> <u>y-component</u>
> $n - w_y = ma_y$ ($a_y$ = 0 because we're at terminal velocity)
> $n = mg\cos\theta$ (use that in x-component)

> [!example]
> ![[9.13.24 Puck Drawing]]
> 
> What is the puck's final speed at the bottom?
> 
> Free-body diagram:
> ![[9.13.24 Puck FBD]]
> 
> Newton's Second Law:
> <u>x-component</u>
> $w_x - f_k = ma_x$
> $mg\sin\theta - \mu _k n = ma_x$
> $mg\sin\theta - \mu _k \cos\theta = ma_x$ (the m's on both sides cancel each other out)
> $a_x = (\sin{40\degree} - (0.30)\cos{40\degree})(9.80)$ = 4.05 m/s$^2$
> 
> <u>y-component</u>
> $n - w_y = ma_y$ ($a_y$ = 0 because the puck isn't accelerating vertically, only horizontally)
> $n = mg\cos\theta$ (use in x-component part)
> 
> Kinematic Equation:
> $v_{fx}^2 = v_{ix}^2 + 2a_x\Delta x$ (initial velocity is 0)
> $v_{fx} = \sqrt{2a_x\Delta x}$
> $\hspace{8mm} = \sqrt{2(4.05)(1.8)}$ = 3.8 m/s