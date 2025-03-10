---
tags: PHYSICS_202
created: 2025-2-10
---

### Drude Model (1900)

![[2.10.25 Drude Model]]

> Define the drift velocity $\vec{v}_d$ as the net velocity of the electrons.
> 
> If $\vec{E}$ = 0, then $\vec{v}_d$ = 0.
> 
> Define the electron current, $i_e$, as the number electrons per second that pass through a cross section of wire.

> [!tip] Electron Current
> $$i_e = \frac{N_e}{\Delta t}$$
> 
> ![[2.10.25 Current Wire Drawing]]
> $\Delta x = v_d \Delta t$
> 
> $$i_e = \frac{N_e}{\frac{\Delta x}{v_d}} = \frac{N_e v_d}{\Delta x} = \frac{N_e A v_d}{A \Delta x} = \frac{N_e A v_d}{V} = n_e A v_d$$
> 
> $n_e$: number of electrons per unit volume (electron density)

> [!example]
> What is the electron density of aluminum? The density of aluminum is 2700 kg/m^3 and the mass of an aluminum atom is 27 u.
> 
> The number of atoms per cubic meter is:
> $n = \frac{\rho}{m} = \frac{2700}{(27)(1.661 \times 10^{-27})} = 6.02 \times 10^{28}$ atoms/m^3 
> 
> Each aluminum atom contributes one electron, so $n_e = n = 6.02 \times 10^{28}$ electrons/m^3 

> Now, apply an electric field.
> 
> Let $\Delta t$ be the time between collisions, then the change in momentum is
> 
> $$\Delta \vec{p} = \int \vec{F} dt = eE \Delta t$$
> $$\rightarrow \vec{v} = \frac{eE \Delta t}{m}$$
> 
> Let $\tau$ be the average time between collisions (mean free time), so
> 
> $$v_d = \frac{eE\tau}{m}$$
> 
> Therefore,
> $$i_e = \frac{n_e e \tau A}{m}E$$

> [!example] 
> The mean free time between collisions is 4.2 x 10^-15 s. What electric field strength causes a 5.0 x 10^19 s$^{-1}$ electron current in a 1.8-mm-diameter iron wire?
> 
> $i_e = \frac{n_e e \tau A}{m}E$
> $E = \frac{i_e m}{n_e e \tau A}$
> $\hspace{4.75mm} = \frac{(9.11 \times 10^{-31}) (5.0 \times 10^{19})}{(8.5 \times 10^{28}) (1.6 \times 10^{19}) (4.2 \times 10^{-15}) (\pi (0.0009)^2)}$
> $\hspace{4.75mm} =$ 0.31 N/C

> Define the current as the rate charge flows.
> $$I = \frac{dQ}{dt}$$
> 
> For steady current
> $$Q = I\Delta t$$
> 
> The direction of current is defined to be the direction positive charges seem to move.


> [!info] Current
> $$I = \frac{Q}{\Delta t} = \frac{e N_e}{\Delta t} = e i_e = n_e e v_d A$$
> 
> SI unit: ampere (1 ampere = 1 A = 1 C/s)


> [!info] Current Density
> $$J = \frac{I}{A} = n_e e v_d$$

^964316

> [!tip] Kirchhoff's Junction Law
> The current entering a junction equals the current exiting the same junction.
> 
> $$\sum I_{in} = \sum I_{out}$$

> [!example]
> You need to design a 1.0 A fuse that blows if the current exceeds 1.0 A. The fuse material melts at a current density of 500 A/cm^2. What diameter of wire of this material will do the job?
> 
> $J = \frac{I}{A} = \frac{I}{\pi r^2}$
> $\rightarrow r = \sqrt{\frac{I}{\pi J}}$
> $\hspace{9.5mm} = \sqrt{\frac{1.0}{\pi (500)}}$
> $\hspace{9.5mm} =$ 0.025 cm
> 
> $d =$ 0.050 cm = 0.50 mm

> [!example]
> ![[2.10.25 Drift Speed Example.png]]
> 
> What is the electron drift speed in the 2.0-mm-diameter end of the wire?
> 
> Finding number of electrons:
> $I = n_e e v_{d1} A_1$
> $\rightarrow n_e = \frac{I}{e v_{d1} \pi r_1^2}$
> $\hspace{12.5mm} = \frac{2.0}{(1.6 \times 10^{-19}) (2.0 \times 10^{-4}) \pi (0.5 \times 10^{-3})}$
> $\hspace{12.5mm} =$ 7.96 x 10^28 electrons
> 
> Finding drift velocity through 2.0-mm-diamter end:
> $I = n_e e v_{d2} \pi r_2^2$ <--- current and number of electrons both stay the same through both ends of the wire
> $\rightarrow v_{d2} = \frac{I}{n_e e \pi r_2^2}$
> $\hspace{13.5mm} = \frac{2.0}{(7.96 \times 10^{28}) (1.6 \times 10^{-19}) \pi (1.0 \times 10^{-3})}$
> $\hspace{13.5mm} =$ 5.0 x 10^-5 m/s = 50 $\micro$m/s