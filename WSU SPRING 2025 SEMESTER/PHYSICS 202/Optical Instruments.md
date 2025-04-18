---
tags: PHYSICS_202
created: 2025-4-16
---

### Multiple Lenses

> [!example]
> There are 2 converging lenses separated by 10 cm. The first lens has a focal length of 40 cm, and the second lens has a focal length of 20 cm. The object is 15 cm to the left of the first lens. Where is the image?
> 
> The image from the first lens is located at:
> $\frac{1}{s_o} + \frac{1}{s_i} = \frac{1}{f}$
> $s_i = \frac{s_o f}{s_o - f} = \frac{(15)(40)}{15 - 40} =$ -24 cm
> 
> The image from the second lens is located at:
> $s_i = \frac{s_o f}{s_o - f} = \frac{(24 + 10) (20)}{(24 + 10) - 20} =$ 49 cm <--- the 24 comes from 24 cm, since the image is located 24 cm away from the first lens to the left, and the 10 comes from 10 cm, the distance separating the lenses; The image starts from 34 cm to the left of the second lens

> [!example]
> There is a converging lens and a diverging lens placed 160 cm apart. The converging lens has a focal length of 40 cm, and the diverging lens has a focal length of -40 cm. The image is 60 cm to the left of the converging lens. Where is the image?
> 
> The image from the first lens is located at:
> $s_i = \frac{s_o f_1}{s_o - f_1} = \frac{(60) (40)}{60 - 40} =$ 120 cm
> 
> The image from the second lens is located at:
> $s_i = \frac{s_o f_2}{s_o - f_2} = \frac{(160 - 120) (-40)}{(160 - 120) - (-40)} =$ -20 cm <--- the 160 comes from the lenses being 160 cm apart, and the 120 cm comes from the image being 120 cm to the right of the converging lens; the image starts from 40 cm to the left of the diverging lens

### Camera

![[4.16.25 Camera.png]]

> [!info] Focal Ratio (f-number)
> $$\text{f-number} = \frac{f}{D}$$
> 
> $D$: diameter of aperture

> [!info] Light Intensity
> The light intensity is
> 
> $$I \propto \frac{D^2}{f^2} = \frac{1}{(\text{f-number})^2}$$

> [!example]
> What is the aperture diameter of a 12-mm-focal-length lens set to f/4.0?
> 
> $\text{f-number} = \frac{f}{D}$
> $D = \frac{f}{\text{f-number}} = \frac{12}{4.0} =$ 3.0 mm

> [!example]
> A camera takes a properly exposed photo at f/5.6 and 1/125 s. What shutter speed should be used if the lens if changed to f/4.0?
> 
> $t_1 I_1 = t_2 I_2$
> $t_2 = \frac{t_1 I_1}{I_2}$
> $\hspace{5mm} = t_1 \left( \frac{\frac{1}{\text{f-number}_1}}{\frac{1}{\text{f-number}_2}} \right)^2$
> $\hspace{5mm} = (\frac{1}{125})(\frac{4.0}{5.6})^2$
> $\hspace{5mm} =$ 0.00408 s = 1/250 s

### Eyeglasses

Near-sightedness (Myopia)
![[4.16.25 Myopia 1.png]]
![[4.16.25 Myopia 2.png]]
![[4.16.25 Myopia 3.png]]

Far-sightedness (Hyperopia):
![[4.16.25 Hyperopia 1.png]]
![[4.16.25 Hyperopia 2.png]]
![[4.16.25 Hyperopia 3.png]]

> [!info] Dioptric Power
> $$P = \frac{1}{f}$$
> 
> where 1 diopter (D) = 1 meter$^{-1}$

> [!example]
> Ramon has contact lenses with the prescription of +2.0 D.
> 
> a) What condition does he have?
> Far-sighted <--- because the dioptric power is positive, so it is a converging lens
> 
> b) What is the near point without the lenses?
> The normal near point is 25 cm.
> 
> The focal point is:
> $f = \frac{1}{P} = \frac{1}{2} =$ 0.5 m
> 
> The near point is:
> $\frac{1}{s_o} + \frac{1}{s_i} = \frac{1}{f}$
> $s_i = \frac{s_o f}{s_o - f} = \frac{(25) (50)}{25 - 50} =$ -50 cm

> [!example]
> Model the eye as a single lens 24 cm in front of the retina. Approximately, what is the f-number of a relaxed eye with
> 
> a) the pupil fully dilated to 8.0 mm?
> $\text{f-number} = \frac{f}{D} = \frac{24}{0.80} =$ 3
> 
> b) the pupil is fully contracted to 1.5 mm?
> $\text{f-number} = \frac{f}{D} = \frac{24}{0.15} =$ 16

### Magnifying Glasses

![[4.18.25 Magnifier.png]]

> [!info] Angular Magnification
> $$M = \frac{25 \hspace{0.5mm} \text{cm}}{s_o} \approx \frac{25 \hspace{0.5mm} \text{cm}}{f}$$

### Microscope

![[4.18.25 Microscope.png]]

If we have 2 lenses (one for the objective lens and one for the eyepiece lens), then the lens with the larger magnification is the objective lens in a microscope.

> [!info] Total Angular Magnification
> $$M = m_{\text{obj}} M_{\text{eye}} = -\frac{L}{f_{\text{obj}}} \frac{25 \hspace{0.5mm} \text{cm}}{f_{\text{eye}}}$$

> [!example]
> You are asked to build a 12x microscope from a 2.0x and 4.0x magnifying lens. What will be the length of the microscope?
> 
> The objective lens is the 4.0x lens.
> 
> The focal lengths are:
> $m = {25 \text{cm}}{f}$
> $\rightarrow f_{\text{obj}} = \frac{25 \text{cm}}{4} =$ 6.25 cm
> $\rightarrow f_{\text{eye}} = \frac{25 \text{cm}}{2} =$ 12.5 cm
> 
> The length of the tube is:
> $M = \frac{L}{f_{\text{obj}}} \frac{25 \text{cm}}{f_{\text{eye}}}$
> $\rightarrow L = M \frac{f_{\text{obj}} f_{\text{eye}}}{25 \text{cm}}$
> $\hspace{11mm} = (12) \frac{(6.25)(12.5)}{25 \text{cm}} =$ 3 cm

### Telescope

![[4.18.25 Telescope.png]]

If we have 2 lenses (one for the objective lens and one for the eyepiece lens), then the lens with the smaller magnification is the objective lens in a telescope.

> [!info] Magnification
> $$m = \frac{-f_{\text{obj}}}{f_{\text{eye}}}$$
> 
> A negative sign for magnification indicates that the image is inverted.

> [!example]
> You've been asked to build a telescope from a 2.0x and 5.0x magnifying lens. What is the length and magnification of the telescope?
> 
> The objective lens is the 2.0x lens.
> 
> The focal lengths are:
> $f_{\text{eye}} = \frac{25\text{cm}}{5.0} =$ 5.0 cm
> $f_{\text{obj}} = \frac{25\text{cm}}{2.0} =$ 12.5 cm
> 
> The length of the telescope is:
> $L = f_{\text{eye}} + f_{\text{obj}} = 5.0 + 12.5 =$ 17.5 cm <--- the focal points coincide in a telescope, so you can just add the focal lengths
> 
> The magnification is:
> $m = \frac{-f_{\text{obj}}}{f_{\text{eye}}} = \frac{-(12.5)}{(5)} =$ -2.5

### Angular Resolution

Replace the lens with a circular aperture:
![[4.18.25 Resolution.png]]

![[4.18.25 Resolved.png]]

> [!info] Angular Resolution
> $$\theta_{\text{min}} = \frac{\frac{w}{2}}{f} = \frac{1.22 \lambda}{D}$$
> 
> $w$ is the width between the 2 dots

> [!example]
> The Hubble Space Telescope has a mirror of 2.4 m. Suppose the telescope is used to photograph stars at the center of the galaxy 30,000 light years away using red light with a wavelength of 650 nm. What is the distance between the stars that are marginally resolved?
> 
> The angular resolution is:
> $\theta_{\text{min}} = \frac{1.22 \lambda}{D} = \frac{1.22(650 \times 10^{-9})}{2.4} =$ 3.3 x 10^-7 rad
> 
> For small angles ($\tan\theta = \theta$):
> $s = r\tan\theta = r\theta = (30,000 \hspace{1mm} \text{light years})(3.3 \times 10^{-7})$
> $\hspace{3.5mm} = 9.9 \times 10^{-3} \hspace{1mm} \text{light years} (\frac{9.4 \times 10^{12} \text{km}}{1 \hspace{1mm} \text{light year}})$
> $\hspace{3.5mm} =$ 9.3 x 10^10 km