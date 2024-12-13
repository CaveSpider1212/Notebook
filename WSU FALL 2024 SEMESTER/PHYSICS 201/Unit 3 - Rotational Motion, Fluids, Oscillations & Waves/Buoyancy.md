---
tags: PHYSICS_201
created: 2024-10-25
---

- **Buoyancy**: net upward force of a fluid on an object

![[10.25.24 Buoyancy Drawing]]

$$F_{net} = F_{up} - F_{down} = F_B$$

> [!info]
> $F_{up} \gt F_{down}$ since the pressure (force per area) increases with depth.

> [!tip] Archimedes' Principle
> ![[10.25.24 Archimedes' Principle Drawing]]
> 
> A fluid exerts an upward buoyant force $\overrightarrow{F}_B$ on an object immersed or floating on the fluid. The magnitude of the buoyant force equals the magnitude of the weight of the displaced fluid.
> 
> $$F_B = m_f g = \rho_f V_f g$$

>  ![[10.25.24 Sink or Float Drawing]]
>
> Will an object float or sink?
> 
> The net force is
> $F_{net} = F_B - w_o$
> $\hspace{9.5mm} = m_fg - m_og$
> $\hspace{9.5mm} = (\rho_fV_f - \rho_oV_o)g$ ($\rho_fV_f - \rho_oV_o$ is the average density of the object)
> 
> Since the object is immerse, then $V_o = V_f$.
> Thus,
> $F_{net} = (\rho_f - \rho_o)V_og$
> 
> Therefore,
> $F_{net} \gt 0$ when $\rho_f \gt \rho_o$ (the object floats)
> $F_{net} \lt 0$ when $\rho_f \lt \rho_o$ (the object sinks)
> $F_{net} = 0$ when $\rho_f = \rho_o$ (the object is in equilibrium, neutral buoyance)

> [!example]
> ![[10.25.24 Rope Tension Drawing]]
> 
> Known values:
> $\rho_f =$ 790 kg/m$^3$
> $V_{Al} =$ 100 cm$^3$
> $\rho_{Al} =$ 2700 kg/m$^3$
> 
> What is the tension in the rope?
> 
> Free-body diagram:
> ![[10.25.24 Rope Tension FBD]]
> 
> Newton's Second Law:
> $F_B + T - w = ma_y$ ($a_y$ = 0 since the object is just sitting there, so no acceleration)
> $T = w - F_B$
> $\hspace{4.5mm} = m_{Al}g - m_fg$
> $\hspace{4.5mm} = (\rho_{Al}V_{Al} - \rho_fV_f)g$ ($V_f = V_{Al}$ since the object is immerse)
> $\hspace{4.5mm} = (\rho_{Al} - \rho_f)V_{Al}g$
> $\hspace{4.5mm} = (2700 - 790)(100)(\frac{1}{100})^3(9.8)$ (converting 100 cm$^3$ to m$^3$)
> $\hspace{4.5mm} =$ 1.87 N

> [!example]
> ![[10.25.24 Can Drawing]]
> 
> Known values:
> $m =$ 20 g
> $d =$ 6.2 cm
> $V =$ 355 mL = 0.355 L
> 
> What length of the can is above the water level?
> 
> Free-body diagram:
> ![[10.25.24 Can FBD]]
> 
> Newton's Second Law:
> $F_B - w = ma_y$ (no acceleration again since the can is sitting there))
> $F_B = w$
> $m_fg = m_og$
> $\rho_fV_f = m_{can} + m_{water}$
> 
> ![[10.25.24 Can Height Drawing]]
> $V_f = (l - h)\pi(\frac{d}{2})^2$ (finding the volume of the displaced fluid using the volume of a cylinder)
> 
> $\rho_f (l - h) \pi (\frac{d}{2})^2 = m_{can} + \rho_f (\frac{1}{2}V_{can})$
> $\rho_f V_{can} - \rho_f h \pi (\frac{d}{2})^2 = m_{can} + \rho_f (\frac{1}{2}V_{can})$
> $h = \frac{\frac{1}{2}\rho_f V_{can} - m_{can}}{\rho_f \pi (\frac{d}{2})^2}$
> $\hspace{4.5mm} =$ 0.0522 m = 5.22 cm (after plugging in values and converting L to m$^3$)