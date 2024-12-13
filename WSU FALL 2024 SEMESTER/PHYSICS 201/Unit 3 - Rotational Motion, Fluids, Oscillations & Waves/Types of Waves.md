---
tags: PHYSICS_201
created: 2024-11-6
---

### Sound

![[11.6.24 Sound Wave Drawing]]

Speed of sound depends upon the media
- Air (20$\degree$ C): 343 m/s
- Water: 1480 m/s
- Granite: 6000 m/s

> [!example]
> ![[11.6.24 Ear Sound Drawing]]
> 
> What is the difference in arrival times?
> 
> ![[11.6.24 Eye Sound Triangle Drawing]]
> 
> $d_L = \sqrt{x^2 + y^2}$
> $\hspace{6mm} = \sqrt{(5.0\cos{45\degree})^2 + (5.0\sin{45\degree})^2}$
> $\hspace{6mm} =$ 5.07 m
> 
> $d_R = \sqrt{(5.0\cos{45\degree} - 0.10)^2 + (5.0\sin{45\degree})^2}$
> $\hspace{6.5mm} =$ 4.93 m
> 
> $\Delta t = \frac{\Delta d}{v}$
> $\hspace{7mm} = \frac{5.07 - 4.93}{343}$
> $\hspace{7mm} =$ 0.000408 s = 408 $\mu$s (microseconds)

### Light

![[11.6.24 Light Wave Drawing]]

Speed of light in vacuum: $C =$ 299,792,458 m/s $\approx$ 3.00 $\times$ 10$^8$

> [!tip] Index of Refraction
> Ratio of speed of light in a vacuum to the speed of light in a material
> $$n = \frac{C}{v}$$
> 
> The frequency remains the same but the wavelength decreases when the wave is going through the material.

n-values:
- Vacuum: $n = 1$
- Air: $n = 1.0003$
- Water: $n = 1.33$
- Glass: $n = 1.50$

> [!example]
> a) What is the frequency of red light (650 nm or 650 $\times$ 10$^{-9}$ m)?
> 
> $v = \lambda f$
> $f = \frac{v}{\lambda}$
> $\hspace{4mm} = \frac{3.00 \times 10^8}{650 \times 10^{-9}}$
> $\hspace{4mm} =$ 4.62 $\times$ 10$^{14}$ Hz
> 
> b) What is the index of refraction of a material in which the red-light wavelength is 450 nm?
> $n = \frac{C}{v}$
> $\hspace{4mm} = \frac{\lambda_{vac} f_{vac}}{\lambda_{mat} f_{mat}}$ (frequency stays the same, so they cancel each other out)
> $\hspace{4mm} = \frac{650}{450}$
> $\hspace{4mm} =$ 1.44

### Intensity

- **Intensity**: ratio of power to area
	- $I = {P}{A}$
	- The energy gets spread out over larger surfaces

For a spherical source:
$$I = \frac{P_{source}}{4\pi r^2}$$

> [!example]
> Imagine a 2W lightbulb.
> 
> What is the light intensity on a wall 2.0 m from the light bulb?
> $I = \frac{P}{A} = \frac{2}{4\pi(2.0)^2} =$ 0.0398 W/m$^2$

> [!example]
> Imagine a 2W laser with a beam diameter of 2.0 mm.
> 
> What is the light intensity on a wall 2.0 m away from the laser?
> $I = \frac{P}{A} = \frac{2}{\pi(0.001)^2} =$ 637,000 W/m$^2$

### Doppler Effect

![[11.6.24 Doppler Effect Drawing]]

The wavelengths are:
- Source moving towards: $\lambda_+ = (V - v_s)T$
- Source moving away: $\lambda_- = (v + v_s)T$

$v$: velocity of sound
$v_s$: velocity of source
$T$: period

The frequencies are:
- $f_+ = \frac{v}{\lambda_+} = \frac{v}{(v - v_s)T} = \frac{1}{1 - \frac{v_s}{v}}f_o$
- $f_- = \frac{v}{\lambda_-} = \frac{v}{(v + v_s)T} = \frac{1}{1 + \frac{v_s}{v}}f_o$

For a stationary square
- Observer moving towards: $f_+ = (1 + \frac{v_o}{v})f_o$
- Observer moving away: $f_- = (1 - \frac{v_o}{v})f_o$

$v_o$: velocity of the observer

> [!example]
> Imagine a person swinging a buzzer over their head.
> 
> Known values:
> $f_o =$ 600 Hz
> $r =$ 1.0 m
> $\omega =$ 100 rpm
> 
> What are the highest and lowest frequencies, heard?
> $v = \omega r = (100)(\frac{2\pi}{1})(\frac{1}{60})(1.0) =$ 10.5 m/s
> $f_+ = \frac{1}{1 - \frac{v_s}{v}}f_o = \frac{1}{1 - \frac{10.5}{343}}(600) =$ 619 Hz
> $f_- = \frac{1}{1 + \frac{v_s}{v}}f_o = \frac{1}{1 + \frac{10.5}{343}}(600) =$ 582 Hz