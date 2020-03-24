# Cheat Sheet

## Coulomb's Law
This gives the force on point 2 due to 1,

$$\vec{F}_{1,2} = k\frac{q_1 q_2}{r^2}\hat{r}_{1,2},$$

while the electric field arising from a test charge $p$ is

$$\vec{E}_p=\frac{\vec{F}}{q}.$$

Fore more charges, the law of superposition applies.


## Electric flux
The electric flux that goes through a surface is given as

$$d\Phi = \vec{E}\cdot \hat{n}dA = \vec{E}\cdot \vec{dA} =  E \, dA \cos \theta,$$ 

where $\theta$ is the angle between $\vec{E}$ and $\hat{n}$. 

## Gauss’s Law

The electric flux going through a closed surface $S$ is mainly dependent on the charges within this surface, i.e.,

$$\Phi=\oint_S \vec{E}\cdot\vec{dA}=\frac{\sum Q}{\epsilon_0}.$$

## Electrostatis potential energy, eletric potential

If we have a charge of $+Q$, and a test charge of $+q$ in point $p$ just $R$ distance away, the **electrostatic potential energy** is

$$U = \frac{q\, Q}{4\pi \epsilon_0 R}.$$

This is the work I have to do to bring the charge $+q$ to point $p$. The **electric potential** is the work *per unit charge* that I have to do to go from $\infty \rightarrow p$. This will be 

$$V_p = \frac{Q}{4\pi \epsilon_0 R}.$$

Note that **potential is work per unit charge**, where if I put the amount of charge I need to carry back into the equation, I get **work**,

$$W_{WL}=q\,V_p.$$

## Movement between potentials

In an electric field, positive charges will move from a higher potential to a lower potential. If we have a point $A$ and $B$, their appropriate potentials are defined as

$$V_A-V_B=\int_{A}^{B}\vec{E} \cdot \vec{dr}, \\
V_B-V_A=-\int_{A}^{B}\vec{E} \cdot \vec{dr}.$$

How much energy is released during this journey? A change in potential energy will be

$$q(V_A-V_B)=K_B-K_A.$$

## Equipotential surfaces
They are always perpendicular to $\vec{E}$, i.e.,

$$E= - \nabla V.$$