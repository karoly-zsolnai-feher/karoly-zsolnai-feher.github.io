# Divergence

###  Intuition
* Divergence is something that we call on *a vector field* and produces a *scalar field*. When it is positive, we have a source, when negative, we have a sink a system. If it is zero, we have exactly as much outflow as inflow.
* In a bathtub, the faucet would behave as a source of water (all vectors pointing outwards, positive divergence), and the drain would behave as a sink (all vectors pointing inwards, negative divergence).

### Definition
Divergence measures *change*, and therefore we expect that it has to use derivatives. Also, a sink is a sink - it does not matter which direction this change happens, therefore, these derivatives have to be added together. Consider the input vector field $F$ as

$$\mathbf{F}=\big(Fx,Fy,Fz\big),$$

then its divergence is defined as

$$\nabla \cdot \mathbf{F}(x)=\Big( \frac{\partial}{\partial x},\, \frac{\partial}{\partial y},\, \frac{\partial}{\partial z}\Big) \cdot \mathbf{F}(x),$$

or perhaps more conveniently,

$$\nabla \cdot \mathbf{F}(x)=\frac{\partial Fx}{\partial x} + \frac{\partial Fy}{\partial y} + \frac{\partial Fz}{\partial z}.$$

### Applications
* For a simple fluid simulation, the velocity field has to be kept divergence free. This means that no mass (and therefore energy) is created or destroyed in the system.

### Sources:
* Doyub Kim's [Fluid Engine Development](https://fluidenginedevelopment.org/)
* Wikipedia article on [Divergence](https://en.wikipedia.org/wiki/Divergence)
