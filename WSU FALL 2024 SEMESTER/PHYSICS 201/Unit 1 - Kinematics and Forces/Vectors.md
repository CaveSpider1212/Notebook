---
tags:
- PHYSICS_201
created: 2024-08-26
---


- **Scalar**: can be described by a single number

> Mass, Temperature, Energy

- **Vector**: have a size (magnitude) and direction

> Velocity, Acceleration, Force

- Two vectors are equal if they have the same magnitude and direction

> In Seattle traveling 60 mph east
> In Pullman traveling 60 mph east
> 
> (those 2 vectors are equal)

### Vector Addition

^d5fd45

$$\overrightarrow{C} = \overrightarrow{A} + \overrightarrow{B} = \overrightarrow{B} + \overrightarrow{A}$$

- Graphically, vectors add tip to tail or using the parallelogram rule

![[8.26.24 Tip to Tail Method Drawing]]

![[8.26.24 Parallelogram Rule Drawing]] ^60fd81

### Vector Multiplication

- Multiplication by a positive scalar only affects the magnitude of the vector

![[8.26.24 Multiplying Vectors Drawing]]

- Multiplication by zero results in a zero vector $\overrightarrow{0}$ which has no direction or magnitude
- Multiplication by -1 reverses the direction of the vector without changing its length

![[8.26.24 Negative Vectors]]

### Vector Subtraction

$$\overrightarrow{C} = \overrightarrow{A} - \overrightarrow{B} = \overrightarrow{A} + (-\overrightarrow{B})$$

![[8.26.24 Subtracting Vectors Drawing]]

### Component Vectors

- **Component Vector**: projection of a vector onto the coordinate system

![[8.26.24 Component Vectors Drawing]]

Triangle #1:
$A_y = A\sin{\theta}$
$A_x = A\cos{\theta}$
$\theta = \tan^{-1}{(\frac{A_y}{A_x})}$

Triangle #2:
$A_y = A\cos{\theta}$
$A_x = A\sin{\theta}$
$\theta = \tan^{-1}{(\frac{A_x}{A_y})}$

### Unit Vectors

- **Unit Vector**: a vector with magnitude equal to one
  - $\hat{i}$ = unit vector in the +x direction
  - $\hat{j}$ = unit vector in the +y direction
  - $\hat{k}$ = unit vector in the +z direction

- All vectors can be written in terms of unit vectors

$$\overrightarrow{A} = \overrightarrow{A_x} + \overrightarrow{A_y} = A_x\hat{i} + A_y\hat{j}$$

##### Adding vectors using unit vectors

$$\overrightarrow{C} = \overrightarrow{A} + \overrightarrow{B} = (A_x\hat{i} + A_y\hat{j}) + (B_x\hat{i} + B_y\hat{j}) = (A_x + B_x)\hat{i} + (A_y + B_y)\hat{j}$$

> Sparky runs 50 m northeast to a tree, then 70 m west to a second tree, and then finally 20 m south to a third tree.
> 
> a) Draw a picture and establish a coordinate system
> 
> ![[8.26.24 Sparky Graph]]
> 
> b) Calculate Sparky's displacement in component form
> 
> $\overrightarrow{D} = \overrightarrow{A} + \overrightarrow{B} + \overrightarrow{C}$
> $\hspace{5mm} = (A_x\hat{i} + A_y\hat{j}) + (B_x\hat{i} + B_y\hat{j}) + (C_x\hat{i} + C_y\hat{j})$
> 
> ($B_y$ and $C_x$ are both equal to 0 since they only run horizontally and vertically, respectively)
> 
> $\hspace{5mm} = (A\cos\theta + B_x)\hat{i} + (A\sin\theta + B_y)\hat{j}$
> $\hspace{5mm} = ((50)\cos{45} + (-70))\hat{i} + ((50)\sin{45} + (-20))\hat{j}$
> $\hspace{5mm} = -35\hat{i} + 15\hat{j}$
> 
> c) Calculate Sparky's net displacement in magnitude and an angle
> 
> $D = \sqrt{D_x^2 + D_y^2} = \sqrt{(-35)^2 + (15)^2} = 38$ m
> $\psi = \tan^{-1}(\left|\frac{D_y}{D_x}\right|) = \tan^{-1}(\left|\frac{15}{-35}\right|) = 23\degree$ north of west

> Three forces are exerted on an object placed on a tilted floor.
> 
> ![[8.26.24 Three Forces Drawing]]
> 
> What are the components of the net force $\overrightarrow{F_{net}} = \overrightarrow{F_1} + \overrightarrow{F_2} + \overrightarrow{F_3}$ parallel and perpendicular to the floor?
> 
> ![[8.26.24 Tilted Coordinate Drawing]]
> 
> $\overrightarrow{F_{net}} = (F_{1x}\hat{i} + F_{1y}\hat{j}) + (F_{2x}\hat{i} + F_{2y}\hat{j}) + (F_{3x}\hat{i} + F_{3y}\hat{j})$
> 
> (in the tilted coordinate system, $F_{1x}$ and $F_{2y}$ are both 0 because they both would only run vertically and horizontally, respectively)
> 
> $\hspace{8mm} = (F_{2x} + F_{3x})\hat{i} + (F_{1y} + F_{3y})\hat{j}$
> $\hspace{8mm} = (F_{2x} + F_3\sin\theta)\hat{i} + (F_{1y} + F_3\cos\theta)$
> 
> ![[8.26.24 Three Forces F3 Drawing]]
> 
> ($F_3$ is positive in the $\hat{i}$ term since the x-component of $F_3$ is probably positive, but negative in the $\hat{j}$ term since the y-component is negative, or facing down)
> $\hspace{8mm} = ((-3) + (5)\sin{30\degree})\hat{i} + ((6) - (5)\cos{30\degree})$
> $\hspace{8mm} = -0.5\hat{i} + 1.67\hat{j}$