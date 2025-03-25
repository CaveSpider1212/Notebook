---
tags: PHYSICS_202
created: 2025-3-23
---

**Inductor**: stores energy in the magnetic field

> Consider an ideal solenoid with a constant magnetic field $\vec{B}$.
> 
> The magnetic flux for each coil is $\Phi_{\text{per\hspace{0.5mm} coil}} = \int \vec{B} \cdot d\vec{A} = \vec{B} \cdot \vec{A} = \frac{\mu_0 NI}{l} \cdot A$.
> 
> Total flux is $\Phi_{\text{net}} = N \Phi_{\text{per\hspace{0.5mm}coil}} = \frac{\mu_0 N^2 A}{l} I$.
> 
> Flux through solenoid depends on current --> $\Phi_{\text{net}} \alpha I$.

> [!info] Self-Inductance
> **Self-inductance**: If current in loop is changed, magnetic field is guaranteed
> 
> Inductance formula:
> $$L = \frac{\Phi_m}{I}$$
> (dependent upon the geometry)
> 
> Ideal solenoid: $L = \frac{\mu_0 N^2 A}{l}$
> 
> SI unit: Henry (1 Henry (H) = ! Tm^2/A)

By Faraday's Law, the voltage across an inductor is $dV = \epsilon = \frac{-d\Phi_m}{dt} = \frac{-dL}{dt}$ if $L$ is constant.

> [!tip] Power used by Inductor
> $$P = I \Delta V = -LI \frac{dI}{dt}$$

> [!tip] Energy used by Inductor
> $$u = \int LI dI = \frac{1}{2} LI^2$$
> 
> Energy density: $u_B = \frac{u}{\text{volume}} = \frac{\frac{1}{2}LI^2}{Al} = \frac{1}{2\mu_0} B^2$, where $B = \frac{\mu_0 NI}{l}$

> [!tip] Potential Difference across an Inductor
> $$\Delta V_L = -L \frac{dI}{dt}$$
> 
> Kirchhoff's Loop Law can be used with $\Delta V_L$ the same way it can with $\Delta V_R$ and $\Delta V_C$.

> [!tip] Current through Inductance $L$
> $$I = I_0 e^{\frac{-t}{\tau}}$$

### LC Circuits

Contains a capacitor and an inductor
![[3.24.25 LC Circuit.png]]

> [!info]
> After the switch is closed for a long time, the capacitor is fully charged and acts as an open circuit, so the current through the circuit is 0.

> [!tip] Current through Inductor in an LC Circuit
> $$I = -\frac{dQ}{dt} = \omega Q_0 \sin\omega t = I_{max} \sin\omega t$$
> 
> where $I_{max} = \omega Q_0$

> [!info] Current and Charge in an LC Circuit over Time
> The current is zero when the capacitor is fully charged, and the charge is zero when the current is maximum.
> 
> ![[3.24.25 LC Circuit Charge Current Graph.png]]

### LR Circuits

Contains a resistor and an inductor
![[3.24.25 LR Circuit.png]]

> [!info]
> Even if there is no power source, the inductor will keep the circuit running until the inductor's magnetic field drops to zero.

> [!info]
> After the switch is closed for a long time, the inductor acts as a short circuit, so to find the current through the circuit at that point calculate the current as if the inductor was not there.

> [!tip] Current through Inductor in an LR Circuit
> $$I = I_0 e^{\frac{-t}{\tau}}$$
> 
> where $\tau = \frac{L}{R}$

> [!info] Current and Charge in an LR Circuit over Time
> The current $I$ in an LR circuit decays over time.
> 
> ![[3.24.25 LR Circuit Current Graph.png]]
> 
> $\frac{dI}{dt}$ is also decreasing over time, meaning $\Delta V_L$ decreases over time as well.