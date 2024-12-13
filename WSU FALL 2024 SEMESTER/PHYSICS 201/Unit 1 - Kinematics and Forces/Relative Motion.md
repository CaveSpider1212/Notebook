---
tags: PHYSICS_201
created: 2024-08-30
---

### Reference Frames

- **Reference frames**: coordinate system used to make measurements

![[8.30.24 Reference Frame Drawing]]

- **Galilean transformation**: switch between reference frames
  - Conditions
    1. The frames have the same orientation
    2. The origins coincide at t=0
    3. No motion in the z-direction
    4. The relative velocity, $\overrightarrow{V}$, is constant (inertial reference frame)

![[8.30.24 Relative Motion Graph]]

##### Note on subscripts

- This page of notes includes $r$, $v$, and $a$ either by itself, with a \' symbol, or capitalized, but it's also common to use subscripts starting from the different points
- When we are doing vector addition, the inner subscripts cancel each other out, and only the outermost subscripts on the very left and right sides of the equation should remain
  - $\overrightarrow{a}_{AC} = \overrightarrow{a}_{AB} + \overrightarrow{a}_{BC}$ (the B's on the inside cancel each other out, leaving only AC)
- $\overrightarrow{a}_{AC}$ means the acceleration of A from the reference frame of C
- $\overrightarrow{a}_{AC} = -\overrightarrow{a}_{CA}$
- $_{E}$ may stand for "Earth"

### Position

$\overrightarrow{r} = \overrightarrow{r'} + \overrightarrow{R} = \overrightarrow{r'} + \overrightarrow{V}t$

### Velocity

$\displaystyle\overrightarrow{v} = \frac{d\overrightarrow{r}}{dt} = \frac{d\overrightarrow{r'}}{dt} + \frac{d\overrightarrow{R}}{dt} = \overrightarrow{v'} + \overrightarrow{V}$

- Alternate equation: $\overrightarrow{v}_{BA} = \overrightarrow{v}_{BE} + \overrightarrow{v}_{EA} = \overrightarrow{v}_{BE} - \overrightarrow{v}_{AE}$
	- One-dimensional relative motion (i.e. there is only an x-component or a y-component, not both)
	- Equation applies to both position and acceleration as well if it is one-dimensional

- Two-dimensional relative motion (both x- and y-components): Pythagorean theorem is useful here
	- Same goes for position and acceleration (distance formula, which is basically Pythagorean theorem, using coordinates also useful for position)

### Acceleration

$\displaystyle\overrightarrow{a} = \frac{d\overrightarrow{v}}{dt}=\frac{d\overrightarrow{v'}}{dt}+\frac{d\overrightarrow{V}}{dt} = \overrightarrow{a'} + \overrightarrow{A}$

- Newton's laws of motion are valid

> A plane has an airspeed of 200 mph. The pilot wishes to make a destination due east, but the wind is blowing at 50 mph in the direction 30$\degree$ north of east. In what direction must the pilot head to reach her destination?
> 
> ![[8.30.24 Plane Vector Drawing]]
> 
> $\overrightarrow{V} = (50\cos{30\degree})\hat{x} + (50\sin{30\degree}\hat{y})$
> $\overrightarrow{v'} = (200\cos\theta)\hat{x} + (-200\sin\theta)\hat{y}$
> $\overrightarrow{v} = \overrightarrow{v'} + \overrightarrow{V} = [(200\cos\theta)+(50\cos{30\degree})]\hat{x} + [(-200\sin\theta) + (50\sin\theta)]\hat{y}$
> $200\sin\theta = 50\sin{30\degree}$ ($\hat{y} \to 0$ because we are going straight east, so we want a 0 y-component velocity)
> $\theta = \sin^{-1}{\frac{1}{4}\sin{30\degree}} = 7.2\degree$ south of east