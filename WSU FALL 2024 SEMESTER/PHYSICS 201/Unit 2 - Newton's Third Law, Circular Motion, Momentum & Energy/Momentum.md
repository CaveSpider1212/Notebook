---
tags: PHYSICS_201
created: 2024-09-30
---

### Newton's Second Law

> $F(t) = ma = m \frac{dv}{dt}$
> $mdv = F(t)dt$
> $\displaystyle m\int_{v_i}^{v_f} dv = \int_{t_i}^{t_f} F(t)dt$
> $mv_f - mv_i = \int_{t_i}^{t_f} F(t)dt$

> [!info] Momentum
> $$\overrightarrow{p} = m\overrightarrow{v}$$
> 
> Thus,
> $\displaystyle\overrightarrow{F} = m\overrightarrow{a} = m \frac{d\overrightarrow{v}}{dt} = \frac{d(m\overrightarrow{v})}{dt} = \frac{d\overrightarrow{p}}{dt}$
> 
> Also,
> $\displaystyle\Delta \overrightarrow{p} = \overrightarrow{p}_f - \overrightarrow{p}_i = \int_{t_i}^{t_f} \overrightarrow{F}dt$ (this is impulse)

> [!info] Impulse
> **Impulse**: area under the $F(t)$ curve between $t_i$ and $t_f$
> 
> $$\overrightarrow{J} = \int_{t_i}^{t_f} \overrightarrow{F}(t)dt = \overrightarrow{J} = \overrightarrow{F}_{avg} \Delta t$$

> [!tip] Impulse-Momentum Theorem
> $$\Delta \overrightarrow{p} = \overrightarrow{J}$$
> 
> Use this when relating mass or velocity (momentum) to the average force or length in time of the force.

> [!example]
> A 2.0 kg object is moving to the right with a speed of 1.0 m/s when it experiences the force below. What is the object's speed after the force ends?
> 
> ![[9.30.24 Object Force Graph]]
> 
> Impulse-Momentum Theorem:
> $\Delta p = J$
> $mv_f - mv_i = F\Delta t$
> $v_f = \frac{F\Delta t + mv_i}{m}$
> $\hspace{6mm} = \frac{(2.0)(0.5) + (2.0)(1.0)}{2.0}$
> $\hspace{6mm} =$ 1.5 m/s

> [!example]
> A 200 g ball is dropped from a height of 2.0 m, bounces and rebounds to a height of 1.5 m. The impulse is shown below. What maximum force is exerted on the ball?
> 
> ![[9.30.24 Ball Force Graph]]
> 
> ![[9.30.24 Ball Diagram]]
> 
> Initial velocity of contact (kinematic equations):
> $v_{fy}^2 = v_{iy}^2 + 2a_y \Delta y$ ($v_{iy}$ = 0 since it starts from rest)
> $v_2^2 = 2a_y\Delta y$
> $v_2 = \pm\sqrt{2a_y \Delta y}$
> $\hspace{6mm} = -\sqrt{2(-9.8)(-2.0)}$ (velocity should be negative since the ball is going down)
> $\hspace{6mm} =$ -6.26 m/s
> 
> Final velocity of contact:
> $v_{fy}^2 = v_{iy}^2 + 2a_y \Delta y$
> $0 = v_3^2 + 2a_y \Delta y$ ($v_{fy}$ = 0 since the final velocity would be 0 in the air)
> $v_3 = \pm\sqrt{-2a_y\Delta y}$
> $\hspace{6mm} = +\sqrt{-2(-9.8)(1.5)}$ (velocity should be positive since the ball is going up)
> $\hspace{6mm} =$ 5.42 m/s
> 
> Impulse-Momentum Theorem:
> $\Delta p = J$
> $mv_3 - mv_2 = \frac{1}{2}F_{max}\Delta t$ ($J$ is the area of a triangle as shown in the graph)
> $F_{max} = \frac{2m(v_3 - v_2)}{\Delta t}$
> $\hspace{12mm} = \frac{2(0.200)(5.42 - (-6.26))}{0.0050}$
> $\hspace{12mm} =$ 936 N

### Conservation of Momentum

> ![[9.30.24 Conservation Momentum Diagram]]
> 
> Newton's Second Law:
> <u>Object 1</u>
> $\overrightarrow{F}_{2\hspace{1mm}on\hspace{1mm}1} = \frac{d\overrightarrow{p}_1}{dt}$
> 
> <u>Object 2</u>
> $\overrightarrow{F}_{1\hspace{1mm}on\hspace{1mm}2} \frac{d\overrightarrow{p}_2}{dt}$
> 
> By Newton's Third Law:
> $\overrightarrow{F}_{1\hspace{1mm}on\hspace{1mm}2} = -\overrightarrow{F}_{2\hspace{1mm}on\hspace{1mm}1}$
> 
> Thus,
> $\frac{d\overrightarrow{p}_1}{dt} + \frac{d\overrightarrow{p}_2}{dt} = \overrightarrow{F}_{2\hspace{1mm}on\hspace{1mm}1} + \overrightarrow{F}_{1\hspace{1mm}on\hspace{1mm}2}$
> $\frac{d}{dt}(\overrightarrow{p}_1 + \overrightarrow{p}_2) = \overrightarrow{F}_{2\hspace{1mm}on\hspace{1mm}1} - \overrightarrow{F}_{2\hspace{1mm}on\hspace{1mm}1}$
> $\overrightarrow{p}_1 + \overrightarrow{p}_2 =$ const.
> $\overrightarrow{p}_{1f} + \overrightarrow{p}_{2f} = \overrightarrow{p}_{1i} + \overrightarrow{p}_{2i}$ (when the net force is 0)

> [!info] Conservation of Momentum
> $$\overrightarrow{p}_{1f} + \overrightarrow{p}_{2f} = \overrightarrow{p}_{1i} + \overrightarrow{p}_{2i} = m_1v_{1f} + m_2v_{2f} = m_1v_{1i} + m_2v_{2i}$$

> [!example]
> Bob throws a rock on frictionless ice. Bob has a mass of 75 kg and can throw a 500 g rock with a speed of 30 m/s. What is Bob's recoil speed?
> 
> Conservation of momentum:
> $P_f = P_i$ (total momentum, capital P's)
> $P_{Bf} + P_{Rf} = P_{Bi} + P_{Ri}$ ($P_{Bi}$ and $P_{Ri}$ are both 0 since they have no initial momentum)
> $m_Bv_{Bf} + m_Rv_{Rf} = 0$
> $v_{Bf} = \frac{-m_R}{m_B}v_{Rf}$
> $\hspace{8mm} = \frac{-0.500}{75}(30)$
> $\hspace{8mm} =$ -0.2 m/s

> [!example]
> A 1500 kg car is rolling at 2.0 m/s. You would like to stop the car by firing a 10 kg blob of sticky clay at it. How fast should we fire the clay?
> 
> Conservation of momentum:
> $P_f = P_i$
> $m_Av_{Ai} + m_Cv_{Ci} = m_Av_{Af} + m_Cv_{Cf}$ (final velocities are 0 since they both stop)
> $v_{ci} = -\frac{m_A}{m_C}v_{Ai}$
> $\hspace{6mm} = -\frac{1500}{10}(2.0)$
> $\hspace{6mm} =$ -300 m/s

> [!example]
> A 5000 kg open train car is rolling on frictionless rails at 22 m/s when it starts to rain. A few minutes later the car's speed is 20 m/s. What mass of water collected in the car?
> 
> ![[10.2.24 Train Car Drawing]]
> 
> Conservation of momentum:
> $P_f = P_i$
> $m_tv_{tf} + m_wv_{wf} = m_tv_{ti} + m_wv_{wi}$ ($v_{wi}$ = 0 because there is no velocity of the water, and $v_{wf} = v_{tf} = v_f$ since the water and train are moving at the same velocity)
> $(m_t + m_w)v_f = m_tv_{ti}$
> $m_w = \frac{m_tv_{ti}}{v_f} - m_t$
> $\hspace{8.5mm} = \frac{(5000)(22)}{20} - (5000)$
> $\hspace{8.5mm} = 500$ kg

> [!example]
> A two stage rocket is traveling at 1200 m/s. The first stage pushes the second stage backwards with a speed of 35 m/s relative to the second stage. The first stage is three times more massive than the second stage. What is the speed of the second stage?
> 
> ![[10.2.24 Rocket Drawing]]
> 
> Conservation of momentum:
> $P_f = P_i$
> $m_1v_{1f} + m_2v_{2f} = m_1v_{1i} + v_2v_{2i}$ ($v_{1i} = v_{2i} = v_i$ because the first and second stages are moving together)
> $m_1v_{1f} + m_2v_{2f} = (m_1 + m_2)v_i$ (where $v_{1f} = v_{2f} - 35$ because of the relative motion)
> $m_1(v_{2f} - 35) + m_2v_{2f} = (m_1 + m_2)v_i$
> $v_{2f} = \frac{(m_1 + m_2)v_i - m_1(35)}{m_1 + m_2}$
> $\hspace{8mm} = \frac{(3m_2 + m_2)(1200) - 3m_2(35)}{3m_2 + m_2}$ ($m_2$ cancels out)
> $\hspace{8mm} = \frac{4(1200) + 3(35)}{4}$
> $\hspace{8mm} = 1230$ m/s

> [!example]
> A 20 g ball of clay traveling east at 2.0 m/s collides with a 30 g ball of clay traveling 30$\degree$ south of west at 1.0 m/s. What is the speed and direction of the resulting 50 g blob of clay?
> 
> ![[10.2.24 Clay Diagram 1]]
> 
> Conservation of momentum:
> $\overrightarrow{P}_f = \overrightarrow{P}_i$
> 
> <u>x-component</u>
> $P_{fx} = P_{ix}$
> $m_3v_{3x} = m_1v_{1i} - m_2v_{2i}\cos{30\degree}$
> $v_{3x} = \frac{m_1v_{1i} - m_2v_{2i}\cos{30\degree}}{m_3}$
> $\hspace{8mm} = \frac{(20)(2.0) - (30)(1.0)\cos{30\degree}}{(50)}$
> $\hspace{8mm} = 0.28$ m/s
> 
> <u>y-component</u>
> $P_{fy} = P_{iy}$
> $m_3v_{3y} = -m_2v_{2i}\sin{30\degree}$
> $v_{3y} = \frac{-m_2v_{2i}\sin{30\degree}}{m_3}$
> $\hspace{8mm} = \frac{-(30)(1.0)\sin{30\degree}}{(50)}$
> $\hspace{8mm} = -0.30$ m/s
> 
> Speed:
> $v_3 = \sqrt{v_{3x}^2 + v_{3y}^2} = 0.41$ m/s
> 
> Direction:
> $\theta = \tan^-1{\frac{v_{3y}}{v_{3x}}} = 47\degree$ south of east

> [!example]
> ![[10.2.24 Clay Diagram 2]]
> 
> What is the speed and direction of the resulting blob of clay?
> 
> Conservation of momentum:
> $\overrightarrow{P}_f = \overrightarrow{P}_i$
> 
> <u>x-component</u>
> $Mv_{fx} = m_1v_1\cos{45\degree} - m_2v_2$
> $v_{fx} = \frac{m_1v_1\cos{45\degree} - m_2v_2}{M}$
> $\hspace{8mm} = \frac{(40)(4.0)\cos{45\degree} - (30)(3.0)}{90}$
> $\hspace{8mm} = 0.26$ m/s
> 
> <u>y-component</u>
> $Mv_{fy} = -m_1v_1\sin{45\degree} + m_3v_3$
> $v_{fy} = \frac{-m_1v_1\sin{45\degree} + m_3v_3}{M}$
> $\hspace{8mm} = -(40)(4.0)\sin{45\degree} + (20)(2.0)$
> $\hspace{8mm} = -0.81$ m/s
> 
> Speed:
> $v_f = \sqrt{v_{fx}^2 + f_{fy}^2} = 0.85$ m/s
> 
> Direction:
> $\theta = \tan^-1{\frac{v_{fy}}{v_{fx}}} = 72\degree$ south of east

> [!info]
> In order for momentum to be conserved, $P_f$ must equal $P_i$.