---
tags: PHYSICS_201
created: 2024-11-8
---

### Superposition

**Superposition**: net displacement

$$D_{net} = D_1 + D_2 + ... + D_n = \sum\limits_{i}^{n} D_i$$

### Standing Wave

> Consider two traveling waves going toward each other, where
> $D_R = a\sin({kx - \omega t})$ <--- wave moving toward the right
> $D_L = a\sin({kx + \omega t})$ <--- wave moving toward the left
> 
> $a$: amplitude
> $D_R$: displacement of wave going to the right
> $D_L$: displacement of wave going to the left
> 
> Superposition of the waves:
> $D(x, t) = D_R + D_L$
> $\hspace{15.5mm} = a\sin({kx - \omega t}) + a\sin({kx + \omega t})$
> $\hspace{15.5mm} = a[\sin({kx})\cos({\omega t}) - \cos({kx})\sin({\omega t}) + \sin({kx})\cos({\omega t}) + \cos({kx})\sin({\omega t})]$
> $\hspace{15.5mm} = 2a\sin({kx})\cos({\omega t})$
> $\hspace{15.5mm} = A(x)\cos({\omega t})$ <--- where $A(x) = 2a\sin({kx})$

> [!info] Standing Waves
> - A standing wave is a superposition of two traveling waves.
> - Standing waves change in amplitude but not in wavelength.
> 
> - The **node** is where the amplitude is at a minimum and where there appears to be no displacement.
> - The **antinode** is where the amplitude is at a maximum and where there appears to be the most displacement.

### Strings

> Imagine a string going from one wall (x = 0) to another wall (x = L).
> 
> $A(x) = 2a\sin({kx})$
> 
> Boundary condition: $A(0) = 0$ and $A(L) = 0$
> $\rightarrow 2a\sin({kL}) = 0$
> $kL = m\pi \hspace{20mm} m = 1, 2, 3, ...$
> $\frac{2\pi}{\lambda}L = m\pi$

> [!tip] Wavelength and Frequency of Strings
> Wavelength:
> $$\lambda_m = \frac{2L}{m}$$
> 
> Frequency:
> $$f_m = \frac{v}{\lambda_m} = m\frac{v}{2L} \hspace{10mm} m = 1, 2, 3, ...$$
> 
> Fundamental frequency (m = 1):
> $$f_1 = \frac{v}{2L}$$
> 
> Harmonics:
> $$f_m = mf_1 \hspace{10mm} m = 2, 3, 4, ...$$

Normal modes - possible standing waves (plug $m$ into wavelength and frequency formulas above):
![[11.8.24 Mode Drawing]]

> [!example]
> An 80 cm (0.80 m) long guitar string with linear density of 1.0 g/m (0.001 kg/m) is under 200 N tension. What is the wavelength of the sound wave produced?
> 
> $v_{string} = \sqrt{\frac{T}{\mu}}$
> $\hspace{13mm} = \sqrt{\frac{200}{0.001}}$
> $\hspace{13mm} =$ 447.2 m/s
> 
> $f = \frac{v_{string}}{\lambda_{string}}$
> $\hspace{4mm} = \frac{447.2}{2(0.80)}$
> $\hspace{4mm} =$ 279.5 Hz
> 
> $\lambda_{sound} = \frac{v_{sound}}{f}$
> $\hspace{13mm} = \frac{343}{279.5}$
> $\hspace{13mm} =$ 1.23 m

### Tubes

Types of tubes:
- **Closed-closed**: both ends of the tube are closed
	- Both ends of the tube have nodes
- **Open-open**: both ends of the tube are open
	- Both ends of the tube have antinodes
- **Open-closed**: one end of the tube is closed while the other end is open
	- The closed end has a node and the open end has an antinode

> [!tip] Wavelength and Frequency of Closed-Closed or Open-Open Tubes
> 
> $$\lambda_m = \frac{2L}{m} \hspace{10mm} m = 1, 2, 3, 4, ...$$
> $$f_m = m\frac{v}{2L}$$

> [!tip] Wavelength and Frequency of Open-Closed Tubes
> 
> $$\lambda_m = \frac{4L}{m} \hspace{10mm} m = 1, 3, 5, 7, ...$$
> $$f_m = m\frac{v}{4L}$$

> [!example]
> Imagine an open-open pipe of length 78 cm and an open-closed pipe of an unknown length.
> 
> $$f_{1, open-closed} = f_{3, open-open}$$
> 
> How long is the open-closed pipe?
> 
> $f_{1, OC} = f_{3, OO}$
> $m_{OC}\frac{v}{4L_{OC}} = m_{OO}\frac{v}{2L_{OO}}$
> $L_{OC} = \frac{1}{2}\frac{m_{OC}}{m_{OO}}L_{OO}$
> $\hspace{10mm} = \frac{1}{2}(\frac{1}{3})(78)$
> $\hspace{10mm} =$ 13 cm