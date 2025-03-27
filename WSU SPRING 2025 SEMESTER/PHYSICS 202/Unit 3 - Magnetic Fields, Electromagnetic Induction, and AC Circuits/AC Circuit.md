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

> [!tip] Capacitive Reactance
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

### Inductor Circuits

> Consider an inductor circuit
> ![[3.26.25 Inductor Circuit.png]]
> 
> $v_L = V_L \cos\omega t = L \frac{d i_L}{dt}$
> $d i_L = \frac{V_L}{L} \cos\omega t dt$
> $i_L = \frac{V_L}{\omega L} \sin\omega t = \frac{V_L}{\omega L} \cos(\omega t - \frac{\pi}{2})$
> 
> ![[3.26.25 Inductor Circuit Graph and Phasor.png]]

> [!info] Inductive Reactance
> $$X_L = \omega L$$
> 
> Thus, $I_L = \frac{V_L}{X_L}$.

> [!example]
> There is a series circuit with 10 V AC source operating at 100 kHz and an inductor with 20 mH inductance. What is the peak current?
> 
> $I_L = \frac{V_L}{X_L}$
> $\hspace{6mm} = \frac{V_L}{\omega L}$
> $\hspace{6mm} = \frac{V_L}{2 \pi f L}$
> $\hspace{6mm} = \frac{10}{2\pi (100 \times 10^3) (20 \times 10^{-3})}$
> $\hspace{6mm} =$ 8.0 x 10^-4 A = 0.80 mA

### Series RLC Circuit

> Consider a series RLC (resistor, inductor, capacitor) circuit
> ![[3.26.25 Series RLC Circuit.png]]
> 
> ![[3.26.25 Series RLC Circuit Phasor.png]]
> 
> The current is:
> $i = I \cos(\omega t - \varphi)$ <--- where $\tan\varphi = \frac{V_L - V_C}{V_R} = \frac{(X_L - X_C)I}{IR} = \frac{X_L - X_C}{R}$ and $\varphi$ is the phase angle
> 
> The peak voltage is:
> $\epsilon_0 = (V_R^2 + (V_L - V_C)^2)^{\frac{1}{2}}$
> $\hspace{5.5mm} = [R^2 + (X_L - X_C)^2]^{\frac{1}{2}} I$
> 
> The peak current is:
> $I = \frac{\epsilon_0}{Z}$ <--- where $Z = \sqrt{R^2 + (X_L - X_C)^2}$, $Z$ is the impedance, $R$ is the resistance, and $X_L - X_C$ is the total reactance
> 
> Resonance occurs when $I$ is maximum ($Z$ is minimum)
> $X_L = X_C$
> $\rightarrow \omega L = \frac{1}{\omega C}$
> $\rightarrow \omega = \frac{1}{\sqrt{LC}}$ (resonance frequency)

> [!example]
> There is a series RLC circuit with a 10 V power supply, 10 $\ohm$ resistance, 10 mH inductance, and 10 $\mu$F capacitance.
> 
> a) What is the resonance frequency?
> $\omega = \frac{1}{\sqrt{LC}} = \frac{1}{\sqrt{(10 \times 10^{-3}) (10 \times 10^{-6})}} =$ 3200 rad/s
> 
> b) Find $V_R$ and $V_C$ at resonance.
> 
> $V_R = IR = \frac{\epsilon_0}{Z} R$
> At resonance $Z = R$
> $V_R = \epsilon_0 =$ 10 V
> 
> $V_C = IX_C = \left(\frac{\epsilon_0}{Z}\right)\left(\frac{1}{\omega C}\right)= (\frac{10}{10})\left(\frac{1}{(3200)(10 \times 10^{-6})}\right) =$ 31 V

### Power

> [!tip] Power in Resistors
> Power dissipated by the resistor:
> $$p_R = i_R v_R = i_R^2 R = I_R^2 R \cos^2(\omega t)$$
> 
> Average power loss in a resistor:
> $$P_R = \frac{1}{2} I_R^2 R$$
> 
> Root-mean-square (rms) of current and voltage:
> $I_{\text{rms}} = \frac{I_R}{\sqrt{2}}$
> $V_{\text{rms}} = \frac{V_R}{\sqrt{2}}$
> 
> Average power loss in a resistor:
> $$P_R = (I_{\text{rms}})^2 R = \frac{(V_{\text{rms}})^2}{R} = I_{\text{rms}} V_{\text{rms}}$$

> [!tip] Power in Capacitors
> Power dissipated by the capacitor
> $$p_C = v_C i_C = (V_C \cos\omega t)(-\omega C V_C \sin\omega t) = -\frac{1}{2} \omega C V_C^2 \sin(2\omega t)$$
> 
> Average power loss in a capacitor:
> $$P_C = 0$$

> [!tip] Power in Inductors
> Power dissipated by the inductor:
> $$p_L = v_L i_L = (V_L \cos\omega t)\left(\frac{V_L}{\omega L} \sin\omega t\right)= \frac{1}{2} \frac{V_L^2}{\omega L} \sin(2\omega t)$$
> 
> Average power loss in an inductor:
> $$P_L = 0$$

> [!tip] Source Power
> Power supplied by the emf:
> $$p_{\text{source}} = i \epsilon $$
> 
> Average power supplied by the emf:
> $$P_{\text{source}} = I_{\text{rms}} \epsilon_{\text{rms}}$$
> 
> Instantaneous source power:
> $$p_{\text{source}} = i \epsilon = (I \cos(\omega t - \varphi)) (\epsilon_0 \cos\omega t) = I \epsilon_0 \cos\omega t \cos(\omega t - \varphi)$$
> 
> Average power:
> $$P_{\text{source}} = \frac{1}{2} I \epsilon_0 \cos\varphi = I_{\text{rms}} \epsilon_{\text{rms}} \cos\varphi$$
> - $\cos\varphi$ is the power factor