---
tags: ENES_100
created: 2025-9-14
description: 9/11 notes
---

> [!info] Force
> **Force**: push or pull on an object
> 
> Units: N, lbf
> 
> Have both quantity and direction

### Types of Forces

> [!info] Gravitational Force ($F_G$)
> **Gravitational Force**: Force created between two large objects
> 
> $$F_G = m \times g$$
> $$g = 9.8 \text{N/kg}$$

> [!info] Normal Force ($F_N$)
> **Normal Force**: Contact force between two surfaces
> 
> Always perpendicular to a surface
> 
> Newton's Third Law: Equal and Opposite Reactions applies here

> [!info] Frictional Force ($F_f$)
> **Frictional Force**: Force resisting motion between two surfaces
> 
> Always opposite of direction of motion
> 
> $$F_f = \mu F_N$$
> 
> $\mu$: coefficient of friction

> [!info] Torque ($\tau$)
> **Torque**: Measure of force that causes an object to rotate about an axis
> 
> Units: N\*m, lbf-in
> 
> $$\tau = F \times d$$

> [!info] Rolling Resistance ($F_{RR}$)
> **Rolling resistance** goes against the motion of a wheel/circular object that is rolling.
> 
> $$F_{RR} = C_{RR} \times F_N$$
> 
> $C_{RR}$: coefficient of rolling resistance

> [!info] Tractive Force ($F_{T}$)
> **Tractive force**: force that a vehicle generates to overcome friction, rolling resistance, drag, and gravity

### Speed

> [!info] Linear Motion
> **Position/displacement** (m):
> $$s = x_1 - x_0$$
> 
> **Velocity** (m/s):
> $$v = \frac{x_1 - x_0}{t_1 - t_0}$$
> 
> **Acceleration** (m/s^2):
> $$a = \frac{v_1 - v_0}{t_1 - t_0}$$

> [!info] Angular Motion
> **Angular position** (rad):
> $$\Delta \theta = \theta_1 - \theta_0$$
> 
> **Angular velocity** (rad/s):
> $$\omega = \frac{\theta_1 - \theta_0}{t_1 - t_0}$$
> 
> **Angular acceleration** (rad/s^2):
> $$\alpha = \frac{\omega_1 - \omega_0}{t_1 - t_0}$$
> 
> Note: 1 revolution = 2$\pi$ radians; motor speeds usually in RPM

> [!tip] Relationship between Linear and Angular Motion
> $$x = \theta \times r$$
> $$v = \omega \times r$$

### Motor Selection

Motors convert electrical to rotational (mechanical) energy.

As the load (torque) increases, the speed (rotational velocity) slows down.

> [!info] Motor Curves
> Show the relationship between motor speed (RPM) on y-axis and torque (N-cm) on the x-axis.
> 
> **No load speed** is the motor's speed when there is no load/torque (y-intercept of the graph).
> 
> **Stall torque** is the torque on the motor when the motor stalls (when the motor speed is 0, also x-intercept of the graph).

Things to consider with motors:
- Cost (too cheap/expensive)
- Weight
- Mechanical considerations (how to mount to OTV, connect wheels, etc.)
- Electrical characteristics (can battery connect, do we have enough power/energy, etc.)

### Turning

There are several ways to steer the OTV:
- Spin one wheel forward and another wheel backward
	- Problem: high frictional load on wheels that aren't spinning (because they're being dragged on the floor)
- Turn the wheels on their axle
	- Problem: higher turning radius
- Have wheels (like Mecanum wheels) that can go forward/backward or sideways
	- Problem: expensive
- Have a tank-like design where two wheels/tread spins forward and the other spins backward
	- Problem: complicated design

Other considerations:
- Driven wheels (with a motor) should be grippy while idler wheels should be slick to reduce friction
- Wheel spacing on the chassis matters
	- Longer and less wide spacing: better for driving straight but poor turning radius/control
	- Shorter and wider spacing: better for turning radius and control, but not as good at driving straight
	- Balanced (square): best
- Wheels should be rigidly mounted to the motors with removable hardware (they can turn axially or rotationally)

