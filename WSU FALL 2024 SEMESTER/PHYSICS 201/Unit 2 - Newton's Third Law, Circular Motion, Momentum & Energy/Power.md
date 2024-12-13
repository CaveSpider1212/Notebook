---
tags: PHYSICS_201
created: 2024-10-7
---

### Power

- **Power**: rate of energy being transformed or transferred (in Watts, W)

$$P = \frac{dE}{dt}$$

> [!tip] Power
> For energy transferred due to work:
> 
> $$P = \frac{dW}{dt}$$
> 
> For constant forces, ($W = \overrightarrow{F} \cdot \Delta\overrightarrow{r}$):
> 
> $$P = \frac{d}{dt}(\overrightarrow{F} \cdot \Delta\overrightarrow{r})$$
> $$= \overrightarrow{F} \cdot \frac{d\overrightarrow{r}}{dt}$$
> $$= \overrightarrow{F} \cdot \overrightarrow{v}$$

> [!example]
> ![[10.7.24 Crate Drawing]]
> 
> Known values:
> $m =$ 10 kg
> $\mu_k =$ 0.20
> 
> How much power does a person need to supply to pull the crate at a constant speed of 1.0 m/s?
> 
> Free-body diagram:
> ![[10.7.24 Crate FBD]]
> 
> Newton's Second Law:
> <u>x-component</u>
> $F_x - f_k = ma_x$ ($a_x$ = 0 because there is no acceleration since the speed is constant)
> $F\cos\theta - \mu_k n = 0$
> $F\cos\theta - \mu_k (mg - F\sin\theta) = 0$
> $F = \frac{\mu_k mg}{\cos\theta + \mu_k \sin\theta}$
> $\hspace{5mm} = \frac{(0.20)(10)(9.8)}{\cos{30\degree} + (0.20)\sin{30\degree}}$
> $\hspace{5mm} =$ 20.3 N (use this in power formula)
> 
> <u>y-component</u>
> $n + F_y - w = ma_y$ ($a_y$ = 0 because there is no vertical acceleration or movement)
> $n + F\sin\theta - mg = 0$
> $n = mg - F\sin\theta$ (use in x-component part)
> 
> Power:
> $P = \overrightarrow{F} \cdot \overrightarrow{v} = Fv\cos\theta = (20.3)(1.0)\cos{30\degree} =$ 17.6 W