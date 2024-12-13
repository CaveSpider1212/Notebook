---
tags: PHYSICS_201
created: 2024-09-11
---

### Mass and Weight

- Mass and weight are not the same
	- **Mass**: amount of matter an object contains
		1. Scalar
		2. SI unit: kilogram (kg)
	- **Weight**: gravitational force on an object (not the same as mass)
		1. Vector
		2. SI unit: Newton (N)
		3. $\overrightarrow{w} = m\overrightarrow{a}_{free fall}$ = (mg, downward)

- Measuring mass and weight
	- Mass: use a balance
	- Weight: use a scale (really measures $\overrightarrow{F}_{sp}$)

- **Apparent weight** ($w_{app}$): weight you feel under acceleration
	- $w_{app} = w(1 + \displaystyle\frac{a_y}{g})$

- **Weightlessness**: the feeling of no weight
	- $w_{app} = 0$
	- $a_y = -g$ (the object is in free fall)

> [!example]
> It takes an elevator 4.0s to reach its cruising speed of 10 m/s. A 60 kg passenger gets abroad on the ground floor. What is the passenger's apparent weight..
> 
> a) before the elevator starts moving?
> $w_{app} = w(1 + \displaystyle\frac{a_y}{g})$ ($a_y$ = 0 since the elevator isn't moving)
> $\hspace{10mm} = w = (60)(9.80)$ = 590 N
> 
> b) while the elevator is speeding up?
> $v_{fy} = v_{iy} + a_y \Delta t$ ($v_{iy}$ = 0 since it starts from rest)
> $a_y = \frac{v_{fy}}{\Delta t} = \frac{10}{4.0}$ = 2.5 m/s$^2$
> 
> $w_{app} = w\left(1+\frac{a_y}{g}\right)= (590)(1 + \frac{2.5}{9.8})$ = 740 N
> 
> c) after the elevator reaches the cruising speed?
> $w_{app} = w\left(1 + \frac{a_y}{g}\right)$ ($a_y$ = 0 because the elevator is no longer accelerating)
> $w_{app}$ = 590 N

### Friction

- **Static friction**: a force that keeps an object from moving
	1. Points in the opposite direction to prevent motion
	2. Maximum possible size, $f_{s,max}$ (objects begin to slip when $f_s = f_{s,max}$)
	3. $f_{s,max} = \mu _s n$
		- $\mu _s$: coefficient of static friction
		- $n$: magnitude of the normal force

- **Kinetic friction**: a resistive force of motion
	1. Points in the opposite direction of motion
	2. Nearly a constant
	3. $f_k = \mu _k n$
	4. $\mu_k < \mu_s$
		- $\mu _k$: coefficient of kinetic friction

![[9.11.24 Friction Graph]]

- **Rolling friction**: same properties as kinetic friction, except $f_r = \mu _r n$
	- $\mu _r$: coefficient of rolling friction

> [!example]
> A 4000 kg truck is parked on a 15$\degree$ slope. How big is the friction force on the truck?
> 
> ![[9.11.24 Truck Drawing]]
> 
> Free-body diagram:
> ![[9.11.24 Truck FBD]]
> 
> Newton's Second Law:
> <u>x-component</u>
> $w_x - f_s = ma_x$ ($a_x$ = 0 because the truck isn't accelerating)
> $mg\sin\theta - f_s = 0$
> $f_s = mg\sin\theta$
> $\hspace{5mm} = (4000)(9.80)\sin{15\degree}$
> $\hspace{5mm} = 10000$ N
> 
> <u>y-component</u>
> $n - w_y = ma_y$ ($a_y$ = 0 because the truck isn't accelerating)
> $n - mg\cos\theta = 0$
> $n = mg\cos\theta$

> [!example]
> A 50,000 kg locomotive is traveling at 10 m/s when both its engine and brakes fail. How far will the locomotive roll before it comes to a stop.
> 
> Free-body diagram:
> ![[9.11.24 Locomotive FBD]]
> 
> Newton's Second Law:
> <u>x-component</u>
> $-f_r = ma_x$
> $a_x = \frac{-f_r}{m}$
> $\hspace{6mm} = \frac{\mu _r n}{m}$
> $\hspace{6mm} = \frac{\mu _ r mg}{m}$
> $\hspace{6mm} = -(0.002)(9.8) =$ -0.02 m/s$^2$
> 
> <u>y-component</u>
> $n - w = ma_y$ ($a_y$ = 0 because the locomotive isn't accelerating in the y direction)
> $n = mg$ (use in x-component section)
> 
> Kinematic Equation:
> $v_{fx}^2 = v_{ix}^2 + 2a_x\Delta x$
> $\Delta x =$ 2500 m (plug in numbers)
> 
> The stopping distance is 2500 meters.