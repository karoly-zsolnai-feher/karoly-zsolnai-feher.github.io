# $E= - \nabla V$, Conductors, Electrostatic Shielding

<img src="5-E=-gradV_Conductors_Electrostatic_Shielding/closed_line.png" width="300" align="middle" style="display:block; margin: auto">

If we take a closed line in a static electric field with no charges moving around,

$$\oint \vec{E}\cdot\vec{dl}=0$$

will hold. This is a little more interesting than it seems at the first sight - for instance, if we march around in a closed surface, but ending up at the same point as seen below, the work (potential difference) we have to do is zero, i.e.,

$$V_A-V_A=0=\oint_A^A \vec{E}\cdot\vec{dl}$$

Again, note that this is an integral along a closed line, not a closed surface. Now, as potentials are defined as integrals over the electric field, if we are given potentials and would like to obtain the field, we will have to use derivatives. Let's try to produce this for a point charge.

<img src="5-E=-gradV_Conductors_Electrostatic_Shielding/electric_field_of_a_charge.png" width="400" align="middle" style="display:block; margin: auto">

We know the electric field 

$$\vec{E} = \frac{Q}{4 \pi \epsilon_0 r^2}\hat{r}$$

and the potential in each point from before,

$$V = \frac{Q}{4\pi \epsilon_0 r}.$$

Now what we are looking for $(dV/dr)\hat{r}$, and since everyone else but $r$ is a constant, the derivative will be

$$\frac{dV}{dr}\hat{r}=-\frac{Q\hat{r}}{4\pi \epsilon_0 r^2}.$$

The star of the show is the negative sign here. Intuitively, in $V$, $r$ is in the denominator, therefore if I increase $r$, $V$ will decrease, so $dV/dr$ has to have a negative sign. Mathematically, all we did was use the fact that 

$$\frac{d}{dx}x^n=nx^{n-1}$$

and here, $n=-1$ as $1/r=r^{-1}$. I know this is kindergarten mathematics, but just wanted to make sure. Also, $\hat{r}$ materialized on both sizes, not due to some forbidden wizardry, but it was just a mutiplication on both sides with a unit vector. No arcane magic was used here. We'll have to wait until Maxwell's equations for that.

Now, this is almost the same as $\vec{E}$, but there is a minus sign. Those pesky minus signs often come up when computing derivatives.

$$\vec{E}=\frac{dV}{dr}\hat{r}.$$

Let's not just stare at this, but try to build a small piece of intuition, which would be that the electric field and potentials are closely related, and both can be computed from each other.