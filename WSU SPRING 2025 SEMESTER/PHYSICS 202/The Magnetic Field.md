---
tags: PHYSICS_202
created: 2025-2-26
description: Chapter 29 in textbook
---

### The Magnetic Field

> [!info]
> <u>Moving</u> charges are the source of the magnetic field

> [!info] Properties of the Magnetic Field $\vec{B}$
> 1. A magnetic field is created at *all* points in space surrounding a current-carrying wire
> 2. The magnetic field at each point is a vector. It has both a magnitude, which we call the *magnetic field strength* $B$, and a direction
> 3. The magnetic field exerts forces on magnetic poles. The force on a north pole is parallel to $\vec{B}$; the force on a south pole is opposite $\vec{B}$.

![[2.26.25 Magnetic Forces.png]]

Magnetic forces cause a compass needle to become aligned parallel to a magnetic field, with the north pole of the compass showing the direction of the magnetic field at that point.

![[2.26.25 Magnetic Field Around Current.png]]

> [!info] Magnetic Field Lines
> These are imaginary lines drawn through a region of space so that
> 
> - A tangent to a field line is in the direction of the magnetic field, and
> - The field lines are closer together where the magnetic field strength is larger

> [!tip] Right-hand Rule for Fields
> 1. Point your *right* thumb in the direction of the current.
> 2. Curl your fingers around the wire to indicate a circle.
> 3. Your fingers point in the direction of the magnetic field lines around the wire

### The Source of the Magnetic Field: Moving Charges

> [!tip] Biot-Savart Law
> ![[2.26.25 Magnetic Field Point Charge.png]]
> 
> $$\vec{B}_{\text{point charge}} = (\frac{\mu_0}{4\pi} \frac{qv \sin\theta}{r^2}, \text{direction given by the right-hand rule})$$
> 
> $\mu_0 = 1.26 \times 10^{-6} \text{T m/A}$
> 
> $\theta$: angle between the charge's velocity and the line to the point where the field is evaluated ($\vec{r}$ in the image)
> 
> The Biot-Savart Law gives us the magnetic field of a charged particle $q$ with moving velocity $\vec{v}$.

SI unit of magnetic field strength: 1 tesla = 1 T = 1 N/A m

> [!example]
> A proton moves with velocity $\vec{v} = 1.0 \times 10^7$ m/s. As it passes the origin (0, 0, 0), what is the magnetic field at the (x, y, z) positions (1 mm, 0 mm, 0 mm), (0 mm, 1 mm, 0 mm), and (1 mm, 1 mm, 0 mm)?
> 
> ![[2.26.25 Magnetic Field Example 1.png]]
> 
> Magnetic field at Position 1:
> $\theta_1 = 0$, so $\vec{B}_1 = 0$
> 
> Magnetic field at Position 2:
> $r_2 =$ 0.0010 m
> $\theta_2 = 90\degree$
> 
> $B = \frac{\mu_0}{4\pi} \frac{qv \sin\theta_2}{r_2^2}$
> $\hspace{5mm} = \frac{1.26 \times 10^{-6}}{4\pi} \frac{(1.60 \times 10^{-19}) (1.0 \times 10^7) \sin(90\degree)}{(0.0010)^2}$
> $\hspace{5mm} =$ 1.60 x 10^-13 T
> 
> The field points in the positive $z$ direction by the right-hand rule, so
> $\vec{B}_2 = 1.60 \times 10^{-13} \hat{k}$ T
> 
> Magnetic field at Position 3:
> $r_3 = \sqrt{2}$ mm = 0.00141 m <---- using geometry
> $\theta_3 =$ 45$\degree$ <---- using geometry
> 
> Using the Biot-Savart Law:
> $\vec{B}_3 = 0.57 \times 10^{-13} \hat{k}$ T

> [!info] Superposition
> $$\vec{B}_{\text{total}} = \vec{B}_1 + \vec{B}_2 + ... + \vec{B}_n$$

> [!tip] Biot-Savart Law with Cross Product
> $$\vec{B}_{\text{point charge}} = \frac{\mu_0}{4\pi} \frac{q\vec{v} \times \hat{r}}{r^2}$$
> 
> $\hat{r}$ points from charge $q$ to a point at which we want to evaluate the field

### The Magnetic Field of a Current

> [!info] Three Key Magnetic Fields
> ![[2.26.25 Magnetic Field Infinite Wire.png]]
> 
> $$B = \frac{\mu_0}{2\pi} \frac{I}{r}$$
> 
> ![[2.26.25 Magnetic Field Current Loop.png]]
> 
> $$B_{\text{center}} = \frac{\mu_0}{2} \frac{NI}{R}$$
> 
> ![[2.26.25 Magnetic Field Solenoid.png]]

> [!tip] Biot-Savart Law for Very Short Segment of Current
> $$\vec{B}_{\text{current segment}} = \frac{\mu_0}{4\pi} \frac{I \Delta \vec{s} \times \hat{r}}{r^2}$$

> [!tip] Biot-Savart Law for a Long, Straight Wire
> $$B_{wire} = \frac{\mu_0}{2\pi} \frac{I}{r}$$
> 
> $r$: distance from the wire

> [!tip] Biot-Savart Law for an $N$-turn Current Loop
> $$B_{\text{coil center}} = \frac{\mu_0}{2} \frac{NI}{R}$$

### Magnetic Dipoles

> [!tip] Electric Field of an Electric Dipole
> $$\vec{E}_{\text{dipole}} = \frac{1}{4\pi\epsilon_0} \frac{2\vec{p}}{z^3}$$
> 
> where the electric dipole moment $\vec{p} =$ qs, from negative to positive charge

> [!tip] Magnetic Field of a Current Loop
> $$B_{\text{loop}} = \frac{\mu_0}{2} \frac{IR^2}{(z^2 + R^2)^{\frac{3}{2}}}$$

> [!info] Magnetic Dipole Moment
> $$\vec{m} = AI$$
> 
> where $A$ is the area and $I$ is the current, from the south pole to the north pole
> 
> SI units: A m^2 

> [!tip] On-Axis Field of a Magnetic Dipole
> $$\vec{B}_{\text{dipole}} = \frac{\mu_0}{4\pi} \frac{2\vec{m}}{z^3}$$

### Ampere's Law and Solenoids

> [!info] Line Integral of $\vec{B} \cdot d\vec{s}$ from $i$ to $f$
> $$\int_i^f \vec{B} \cdot d\vec{s}$$
> 
> If $\vec{B}$ is everywhere perpendicular to a line, the line integral of $\vec{B} \cdot d\vec{s}$ is 0
> 
> If $\vec{B}$ is everywhere tangent to a line of length $l$ and has the same magnitude $B$ at every point, then the line integral is equal to $Bl$.

> [!tip] Ampere's Law
> $$\oint \vec{B} \cdot d\vec{s} = \mu_0 I_{\text{through}}$$

> [!info] Magnetic Field inside a Solenoid
> $$B_{\text{solenoid}} = \frac{\mu_0 NI}{l} = \mu_0 nI$$

### Magnetic Force on a Moving Charge

> [!tip] Magnetic Force on a Charge $q$
> If there is a charge $q$ moving through a magnetic field $\vec{B}$ with velocity $\vec{v}$, the force on $q$ can be written as:
> 
> $$\vec{F} = q\vec{v} \times \vec{B} = qvB\sin\alpha$$
> 
> where $\alpha$ is the angle between $\vec{v}$ and $\vec{B}$, and the direction is determined by the right-hand rule

> [!info] Magnetic Force Properties
> - Only a *moving* charge experiences a magnetic force. There is no magnetic force on a charge at rest ($\vec{v} = \vec{0}$) in a magnetic field.
> - There is no force on a charge moving parallel ($\alpha = 0\degree$) or antiparallel ($\alpha = 180\degree$) to a magnetic field.
> - When there is a force, the force is perpendicular to the plane containing $\vec{v}$ and $\vec{B}$.
> - The force is a maximum $\left| q \right| vB$ when $\vec{v}$ is perpendicular to $\vec{B}$.
> - The force on a negative charge is in the direction *opposite* to $\vec{v} \times \vec{B}$.

> [!info] Radius of Cyclotron Orbit
> $$r_{\text{cyc}} = \frac{mv}{qB}$$

> [!tip] Frequency of Cyclotron Orbit
> $$f_{\text{cyc}} = \frac{qB}{2\pi m}$$

The **Hall effect** is used to gain information about the charge carriers in a conductor, and is also the basis of a widely used technique for measuring magnetic field strengths

> [!info] Steady-State Condition where $F_B = F_E$
> $$F_B = e v_d B = F_E = eE = e \frac{\Delta V}{w}$$
> 
> $w$: width of the conductor
> $\Delta V$: potential difference between the two surfaces of the conductor

> [!info] Hall Voltage
> $$\Delta V_H = w v_d B = \frac{IB}{tne}$$

> [!info] Drift Speed
> $$v_d = \frac{J}{ne} = \frac{\frac{I}{A}}{ne} = \frac{I}{wtne}$$

### Magnetic Forces on Current-Carrying Wires

> [!info] Magnetic force on a current-carrying wire
> ![[3.11.25 Magnetic Current Carrying Wire.png]]

> [!tip] Magnetic Force
> $$F = I \Delta x B$$
> 
> where $\Delta x$ is the length of the segment of the wire

> [!tip] Force on length $l$ of a current-carrying wire
> $$\vec{F}_{\text{wire}} = I \vec{l} \times \vec{B} = (IlB\sin\alpha, \text{direction \hspace{0.25mm} of \hspace{0.25mm} right-hand \hspace{0.25mm} rule})$$

> [!info]
> The right-hand for forces applies to a current-carrying wire. Point your right thumb in the direction of the current (parallel to $\vec{l}$) and your index finger in the direction of $\vec{B}$. Your middle finger is then pointing in the direction of the force $\vec{F}$ on the wire.

> [!tip] Force exerted by the Lower Wire on the Upper Wire (2 parallel wires of length $l$)
> $$F_{\text{parallel}} = I_1 l B_2 = I_1 l \frac{\mu_0 I_2}{2\pi d} = \frac{\mu_0 l I_1 I_2}{2\pi d}$$
> 
> where $r = d$

> [!info]
> Parallel wires carrying currents in the same direction attract each other; parallel wires carrying currents in opposite directions repel each other.

### Forces and Torques on Current Loops

![[3.11.25 Torque Magnetic Field.png]]

> [!tip] Torque exerted by the Magnetic Field
> $$\tau = 2Fd = 2(IlB)\left(\frac{1}{2} l \sin\theta\right)= (Il^2) B \sin\theta = mB\sin\theta$$
> 
> $$\vec{\tau} = \vec{m} \times \vec{B}$$