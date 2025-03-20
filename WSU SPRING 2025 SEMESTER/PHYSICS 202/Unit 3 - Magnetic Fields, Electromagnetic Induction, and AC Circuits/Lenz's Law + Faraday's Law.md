---
tags: PHYSICS_202
created: 2025-3-19
---

> [!info] Lenz's Law
> There is an induced current in a closed conducting loop if and only if the magnetic flux through the loop is changing. The direction of the induced current is such that the induced magnetic field opposes the change in flux.
> 
> Process:
> 1. **Determine the direction of the applied magnetic field.** The field must pass through the loop
> 2. **Determine how the flux is changing.** Is it increasing, decreasing, or staying the same?
> 3. **Determine the direction of an induced magnetic field that will oppose the *change* in the flux.**
> 	- Increasing flux: the induced magnetic field points opposite the applied magnetic field
> 	- Decreasing flux: the induced magnetic field points in the same direction as the applied magnetic field.
> 	- Steady flux: there is no induced magnetic field.
> 4. **Determine the direction of the induced current.** Use the right-hand rule to determine the current direction in the loop that generates the induced magnetic field you found in step 3.

> ![[3.19.25 Example 1.png]]
> ![[3.19.25 Induced Current 1.png]]

> ![[3.19.25 Induced Current Example 2.png]]

### Faraday's Law

> [!info] Faraday's Law
> The magnitude of emf is
> 
> $$\epsilon = \left| \frac{d \Phi_m}{dt} \right|$$

> [!example]
> There is a current loop (induced going clockwise) inside a uniform and constant magnetic field.
> $r = r_0 e^{-\beta t}$ (shrinking radius)
> 
> What is the emf induced in the loop?
> 
> The magnetic flux is:
> $\Phi_m = \int \vec{B} \cdot d\vec{A} = B \cdot \vec{A} = B \pi r_0^2 e^{-2\beta t}$
> 
> By Faraday's Law, the emf in the loop is
> $\epsilon = \left| \frac{d \Phi_m}{dt} \right| = | B \pi r_0^2 (-2\beta) e^{-2\beta t} | = 2\beta B \pi r_0^2 e^{-2 \beta t}$

> [!example]
> There is a 10 cm x 10 cm square loop, where the magnetic field is $\vec{B} = (0.30 t) \hat{i} + (0.50 t^2) \hat{k}$. What is the emf induced in the loop at $t$ = 0.5 s?
> 
> The magnetic flux is:
> $\Phi_m = \int \vec{B} \cdot d\vec{A} = \vec{B} \cdot \vec{A}$
> $\hspace{8mm} = [(0.30 t) \hat{i} + (0.50 t^2) \hat{k}] \cdot (0.10)^2 \hat{k}$
> $\hspace{8mm} = (0.005 t^2)$ T m^2/s^2 
> 
> By Faraday's Law, the emf in the loop is:
> $\epsilon = \left| \frac{d\Phi_m}{dt} \right| = (0.010 t)$
> $\epsilon (0.5) = (0.010)(0.5) =$ 0.005 V

### Generators

> [!info] Magnetic Flux of a Generator
> $\Phi_m = \int \vec{B} \cdot d\vec{A} = BA \cos\theta = BA \cos\omega t$
> 
> $\omega$ is the angular frequency

> [!tip] emf of a Generator
> $$\epsilon = -N \frac{d\Phi_m}{dt} = N \omega AB sin\omega t$$
> 
> where $N$ is the number of turns (so there is more emf for every turn)
> 
> emf graph will look like an alternating current (AC) graph (sine waves)

### Transformer

> ![[3.19.25 Transformer.png]]
> 
> Kirchhoff's Loop Law for the primary coil:
> $\epsilon - N_1 \frac{d\Phi_m}{dt} = 0$
> 
> Kirchhoff's Loop Law for the secondary coil:
> $V_2 - N_2 \frac{d\Phi_m}{dt} = 0$
> 
> Assuming all flux lines follow the ferromagnetic coil:
> $\frac{V_2}{N_2} = \frac{\epsilon}{N_1} \rightarrow V_2 = \epsilon \frac{N_2}{N_1}$
> 
> If $N_2 > N_1 \rightarrow V_2 \rightarrow \epsilon$, it is a step-up transformer.
> If $N_1 > N_2 \rightarrow V_2 < \epsilon$, it is a step-down transformer.

> [!example]
> There are power lines from point A to B, and the wires have a resistance of 0.02 $\ohm$ per kilometer. A and B are 10 km apart. We want to transmit 200 kW of power through the wires.
> 
> a) How much is lost if the power is transmitted at 240 V?
> $P = IV$
> $\rightarrow I = \frac{P}{V} = \frac{200,000}{240} =$ 833 A
> 
> $P_{\text{loss}} = I^2 R = (833)^2(0.02)(10) =$ 139,000 W (~70% of power transmitted)
> 
> b) If transformers with a turn ratio of 20, how much power is lost?
> 
> $V_2 = V_1\left(\frac{N_2}{N_1}\right)= (240)(20) =$ 4800 V
> $I = \frac{P}{V} = \frac{200,000}{4800} =$ 41.7 A
> $P_{\text{loss}} = I^2 R = (41.7)^2 (0.02)(10) =$ 348 W (~0.2% of power transmitted)