---
tags: PHYSICS_202
created: 2025-3-24
---

> Consider an AC source
> $\epsilon = \epsilon_0 \cos\omega t$
> ![[3.24.25 AC Sine Wave.png]]
> 
> This can be represented graphically by a phasor (a rotating vector):
> ![[3.24.25 AC Phasor.png]]

### Resistor Circuits

> Now, consider a resistor circuit.
> ![[3.24.25 AC Resistor Circuit.png]]
> 
> $v_R = V_R \cos\omega t$ <--- $v_R$ is the instantaneous voltage; $V_R$ is the peak voltage
> $i_R = \frac{v_R}{R} = \frac{V_R}{R} \cos\omega t = I_R \cos\omega t$
> 
> ![[3.24.25 AC Resistor Graph and Phasor.png]]

### Capacitor Circuits

> Now, consider a capacitor circuit.
> ![[3.24.25 AC Capacitor Circuit.png]]
> 
> $v_C = V_c \cos\omega t$
> $q = C v_C = C V_C \cos\omega t$
> $i_C = \frac{dq}{dt} = -\omega C V_C \sin\omega t = \omega C V_c \cos(\omega t + \frac{\pi}{2})$
> 
> ![[3.24.25 AC Capacitor Graph and Phasor.png]]

##### Capacitive Resistance

> [!tip] Capacitive Resistance
> $$X_C = \frac{1}{\omega C}$$
> 
> SI unit: ohm
> 
> Thus, $I_C = \frac{V_C}{X_C}$, but $i_c \neq \frac{v_C}{X_C}$.

> [!example]
> There is a capacitor circuit where the AC source has a peak voltage of 2.2 V and a frequency of 250 kHz. What is the capacitance if the peak current is 330 $\mu$A?
> 
> $I_C = \frac{V_C}{X_C} = \omega C V_C$
> $C = \frac{I_C}{\omega V_C}$
> $\hspace{5mm} = \frac{I_C}{2\pi f V_C}$
> $\hspace{5mm} = \frac{330 \times 10^{-6}}{2\pi(250 \times 10^3) (2.2)}$
> $\hspace{5mm} =$ 9.5 x 10^-4 F

### RC Circuits

> Now, consider an RC circuit.
> ![[3.24.25 AC RC Circuit.png]]
> 
> ![[3.24.25 AC RC Circuit Phasor.png]]
> 
> $\epsilon^2 = V_R^2 + V_C^2 = (IR)^2 + (IX_C)^2 = (R^2 + X_C) I^2 = \left(R^2 + \frac{1}{\omega^2 C^2}\right)I^2$
> 
> Thus, the peak current is
> $I = \frac{\epsilon_0}{\sqrt{R^2 + \frac{1}{\omega^2 C^2}}}$
> 
> The peak voltages are
> $V_R = IR = \frac{\epsilon_0 R}{\sqrt{R^2 + \frac{1}{\omega^2 C^2}}}$
> $V_C = IX_C = \frac{\frac{\epsilon_0}{\omega C}}{\sqrt{R^2 + \frac{1}{\omega^2 C^2}}}$
> 
> ![[3.24.25 AC RC Frequency Graph.png]]
> $\omega_C$ is the crossover frequency (where $V_R = V_C$)

##### Filters

![[3.24.25 Low-Pass Filter.png]]

![[3.24.25 High-Pass Filter.png]]

> [!example]
> The first circuit has only a resistor and a capacitor in series. The second circuit is a low-pass filter.
> 
> In the first circuit, the capacitor voltage decays to half its initial value in 2.5 ms. Using the same resistor and capacitor in the low-pass filter, what is the cross-over frequency?
> 
> For the first circuit:
> $v_C = v_o e^{\frac{-t}{RC}}$
> $RC = \frac{t}{-\ln(\frac{v_C}{v_o})}$
> $\hspace{9mm} = \frac{2.5 \times 10^{-3}}{-\ln(\frac{1}{2})}$
> $\hspace{9mm} =$ 3.6 x 10^-3 s
> 
> Therefore, the crossover frequency is
> $f_C = \frac{\omega_C}{2\pi}$
> $\hspace{7mm} = \frac{1}{2\pi RC}$
> $\hspace{7mm} = \frac{1}{2\pi(3.6 \times 10^{-3})}$
> $\hspace{7mm} =$ 44 Hz