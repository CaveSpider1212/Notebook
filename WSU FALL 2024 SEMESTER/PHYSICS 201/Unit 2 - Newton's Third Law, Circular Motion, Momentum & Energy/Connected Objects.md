---
tags: PHYSICS_201
created: 2024-09-18
---

> [!example]
> Find the unknown values:
> ![[9.18.24 Box Drawing]]
> 
> Known values:
> $\mu _k$ = 0.30
> $m_1$ = 1.0 kg
> $m_2$ = 2.0 kg
> 
> Unknowns:
> $\overrightarrow{T}_1$ = ?
> $\overrightarrow{a}_2$ = ?
> 
> Free-body diagrams:
> ![[9.18.24 Box FBD]]
> 
> Newton's second law:
> <u>Block 1</u>
> x-component -
> $f_1 - T_1 = m_1a_{1x}$ ($a_{1x}$ = 0 since there is no horizontal acceleration for block 1)
> $\mu _k n_1 - T_1 = 0$
> $T_1 = \mu _k(m_1g)$ (obtained from block 1 y-component)
> $\hspace{6mm} = (0.30)(1.0)(9.8)$ = 2.9 N
> 
> y-component -
> $n_1 - w_1 = m_1a_{1y}$ ($a_{1y}$ = 0 since there is only motion in the x-direction)
> $n_1 - m_1g = 0$
> $n_1 = m_1g$ (use in block 1 x-component part)
> 
> <u>Block 2</u>
> x-component -
> $F - f_2 - f_1 = m_2a_{2x}$
> $F - \mu _k n_2 - \mu _k n_1 = m_2a_{2x}$
> $a_{2x} = \frac{F - \mu _k n_2 - \mu _k n_1}{m_2}$
> $a_{2x} = \frac{F - \mu _k (m_1 + m_2)g - \mu _k m_1g}{m_2}$
> $\hspace{8mm} = \frac{20 - (0.3)(1.0 + 2.0)(9.8) - (0.3)(1.0)(9.8)}{2.0}$ =4.1 m/s$^2$
> 
> y - component -
> $n_2 - n_1 - w_2 = m_2a_{2y}$ ($a_{2y}$ = 0 since there is only motion in the x-direction)
> $n_2 - n_1 - m_2g = 0$
> $n_2 = n_1 + m_2g$
> $\hspace{5mm} = m_1g + m_2g$ (use in x-component block 2 part)
> 
> Answer:
> $T_1$ = 2.9 N
> $a_{2x}$ = 4.1 m/s$^2$

> [!example]
> Find the unknown values:
> ![[9.18.24 Box Hanging Drawing]]
> 
> Knowns:
> $\mu _k$ = 0.30
> $m_1$ = 1.0 kg
> $m_2$ = 2.0 kg
> $m_e$ = 3.0 kg
> 
> Unknown:
> $\overrightarrow{a}_2$ = ?
> 
> Free-body diagrams:
> ![[9.18.24 Box Hanging FBD]]
> 
> Acceleration constraints:
> $a_{1y} = a_{2x} = -a_{3y}$ (block 1 is going up in the y-direction, block 2 is going to the right in the x-direction since block 3 has more mass, and block 3 is going down in the y-direction)
> 
> Newton's second law:
> <u>Block 1</u>
> y-component -
> $T_1 - w_1 = m_1a_{1y}$
> $T_1 = m_1g + m_1a_{1y}$
> 
> <u>Block 2</u>
> x-component -
> $T_3 - T_1 - f_2 = m_2a_{2x}$
> $T_3 - T_1 - \mu _k n_2 = m_2a_{2x}$
> $(m_3g + m_3a_{3x}) - (m_1g + m_1a_{1y}) - \mu _k(m_2g) = m_2a_{2x}$ (substituting known expressions from other equation components for all of the blocks)
> $(m_3g + m_3(-a_{2x})) - (m_1g + m_1a_{2x}) - \mu _k m_2g = m_2a_{2x}$ (substituting in acceleration values to be in terms of $a_{2x}$ from the acceleration constraints)
> $a_{2x} = \frac{m_3g - m_1g - \mu _k m_2g}{m_1 + m_2 + m_3}$
> $\hspace{7.5mm} = \frac{(3.0 - 1.0 - (0.30)(2.0))(9.8)}{1.0 + 2.0 + 3.0}$ = 2.3 m/s$^2$
> 
> y-component -
> $n_2 - w_2 = m_2a_{2y}$
> $n_2 = m_2g$
> 
> <u>Block 3</u>
> y-component -
> $T_3 - w_3 = m_3a_{3y}$
> $T_3 = m_3g + m_3a_{3x}$
> 
> Answer:
> $a_{2x}$ = 2.3 m/s$^2$

> [!example]
> Find the unknowns:
> ![[9.18.24 Box Slope Drawing]]
> 
> Knowns:
> $\mu _k$ = 0.30
> $m_A$ = 1.0 kg
> $m_B$ = 3.0 kg
> 
> Unknown:
> $\overrightarrow{a}_B$ = ?
> 
> Free-body diagrams:
> ![[9.18.24 Box Slope FBD]]
> 
> Acceleration constraint:
> $a_{Ax} = -a_{Bx}$
> 
> Newton's second law:
> <u>Block A</u>
> x-component -
> $T - f_A - w_{Ax} = m_{A}a_{Ax}$
> $T - \mu _k n_A - m_{A}g\sin\theta = m_{A}a_{Ax}$
> $T - \mu _k (m_Ag\cos\theta) - m_A g\sin\theta = m_Aa_{Ax}$ (isolate $T$ and use it in block B x-component)
> 
> y-component -
> $n_A - w_{Ay} = m_{A}a_{Ay}$ ($a_{Ay}$ = 0 because the box isn't moving in the y-direction)
> $n_A = m_Ag\cos\theta$ (use in block A x-component)
> 
> <u>Block B</u>
> x-component -
> $T + f_A + f_B - w_{Bx} = m_Ba_{Bx}$
> $T + \mu _k n_A + \mu _k n_B - m_B g\sin\theta = m_Ba_{Bx}$
> $(\mu _k m_A g\cos\theta + m_A g\sin\theta + m_A(-a_{Bx})) + \mu _k(m_A + m_B)g\cos\theta + \mu _k m_A g - m_B g\sin\theta = m_Ba_{Bx}$
> $a_{Bx}$ = 1.9 m/s$^2$ (did some math)
> 
> y-component -
> $n_B - n_A - w_{By} = m_Ba_{By}$ ($a_{By}$ = 0 because the box isn't moving in the y-direction)
> $n_B = n_A + m_B g\cos\theta$
> $\hspace{4mm} = (m_A + m_B)g\cos\theta$ (subbed in $n_A$ and factored out)
> 
> Answer:
> $a_{Bx}$ = 1.9 m/s$^2$

### Double Pulleys

> [!example]
> ![[9.23.24 Double Pulley Hanging Drawing]]
> 
> Known values:
> $m$ = 10.2 kg
> $\overrightarrow{a}$ = 0
> 
> Unknown values:
> $T_1$ = ?
> $T_2$ = ?
> $T_3$ = ?
> $T_4$ = ?
> $T_5$ = ?
> $F$ = ?
> 
> The ropes and pulleys are massless.
> - $T_2 = T_3 = T_5$
> 
> Free-body diagrams:
> ![[9.23.24 Double Pulley Hanging FBD]]
> 
> Newton's Second Law:
> <u>Block</u>
> $T_1 - w = ma_y$ (no acceleration on the block, so $a_y$ = 0)
> $T_1 = mg$
> 
> <u>Large Pulley</u>
> $T_4 - T_2 - T_3 - T_5 = 0$ (pulleys are massless, so $m$ = 0...acceleration is also 0)
> $T_4 = T_2 + T_3 + T_5$
> $T_4 = 3T_2$
> $\hspace{6mm} = \frac{3}{2}T_1$
> 
> <u>Small Pulley</u>
> $T_2 + T_3 - T_1 = 0$ (pulleys are massless, so $m$ = 0...acceleration is also 0)
> $2T_2 = T_1$
> $T_2 = \frac{T_1}{2}$
> 
> Answer:
> $T_1 = mg$ = 100 N
> $T_2 = \frac{T_1}{2}$ = 50 N
> $T_3 = T_2$ = 50 N
> $T_4 = \frac{3}{2}T_1$ = 150 N
> $T_5 = T_2$ = 50 N
> $F = T_5$ = 50 N

> [!example]
> ![[9.23.24 Double Pulley Drawing]]
> 
> What is the acceleration of Block A?
> 
> Known values:
> $\mu_k$ = 0.30
> $m_A$ = 7.0 kg
> $m_B$ = 7.0 kg
> 
> Free-body diagrams:
> ![[9.23.24 Double Pulley FBD]]
> 
> Acceleration constraint:
> $a_{Ax} = -2a_{By}$
> 
> Newton's Second Law:
> <u>Block A</u>
> x-component -
> $T - f_k = m_A a_{Ax}$
> $T = \mu_k n + m_A a_{Ax}$
> $\hspace{4mm} = \mu_k m_A g + m_A a_{Ax}$ (use in Block B y-component)
> 
> y-component -
> $n - w_A = m_A a_{Ay}$ ($a_{Ay}$ = 0 since the block isn't moving in the y-direction)
> $n = m_A g$ (use in Block A x-component)
> 
> <u>Block B</u>
> y-component -
> $T + T - w_B = m_B a_{By}$
> $2T - m_B g = m_B a_{By}$
> $2(\mu_k m_A g + m_A a_{Ax}) - m_B g = m_B a_{By}$
> $2(\mu_k m_A g + m_A a_{Ax}) - m_B g = m_B(-\frac{a_Ax}{2})$
> $4(\mu_k m_A g + m_A a_{Ax}) - 2m_B g = -m_B a_{Ax}$
> $a_{Ax} = \frac{(2m_B - 4\mu_k m_A)g}{4m_A - m_B}$
> $a_{Ax}$ = 2.4 m/s$^2$ (after plugging in known values into equation above)

> [!example]
> ![[9.23.24 Wedge Drawing]]
> 
> Known values:
> $m_A$ = 800g
> $m_B$ = 200g
> $\theta$ = 40$\degree$
> 
> What does the scale read...
> 
> a) if Block B is not moving?
> 
> Free-body diagrams:
> ![[9.23.24 Wedge FBD]]
> 
> Newton's Second Law:
> <u>Block A</u>
> x-component -
> $f_{sx} - n_{Bx} = m_A a_{Ax}$
> 
> y-component -
> $n_A - w_A - f_{sy} - n_{By} = m_A a_{Ay}$ ($a_{Ay}$ = 0 since Block A isn't moving in the y-direction)
> 
> <u>Block B</u>
> x-component -
> $w_{Bx} - f_s = m_B a_{Bx}$ ($a_{Bx}$ = 0 since Block B is not moving)
> $f_s = m_B g \sin\theta$
> $n_A - m_A g - (m_Bg\sin\theta)\sin\theta - (m_B g \cos\theta)\cos\theta$
> $n_A = m_Ag + m_Bg(\sin^2\theta + \cos^2\theta)$
> $\hspace{7mm} = (m_a + m_B)g$
> $\hspace{7mm} =$ 9.8 N
> 
> y-component -
> $n_B - w_{By} = m_B a_{By}$ ($a_{Bx}$ = 0 since Block B is not moving)
> 
> Answer: 9.8 N
> 
> b) if there is no friction between the blocks? ($f_s \rightarrow 0$)
> $n_A = m_Ag + m_Bg\cos^2\theta$
> $\hspace{7mm} =$ 8.99 N