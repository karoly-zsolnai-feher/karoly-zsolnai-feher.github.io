# Electrostatic Potential, Electric Energy, Equipotential Surfaces

# Example of electrostatic potential

Consider two positive charges $q_1,q_2$. Let's place $q_1$ somewhere in space, and start coming towards it from very far away (we'll use $\infty$ in the example) with $q_2$ in our hand. We will have to do some work $F_{WL}$ pushing, since $q_1$ will want to repel it with force $F_{e}$. The target distance is between the charges is $R$, while we are $r$ away. 

How much work do we have to do to accomplish this? Time to whip out the integrals.

<img src="4-Electrostatic_Potential/work_against_electric_field.png" width="450" align="middle" style="display:block; margin: auto">

$$W_{WL}= \int_{\infty}^{R} \vec{F}_{WL} \, \vec{dr}=\int_{R}^{\infty} \vec{F}_{e} \, \vec{dr}.$$

Note that $\vec{dr}$ is an infinitesimally small displacement - a tiny step that we think of as a vector, and the term within the integral on both sides is a dot product, i.e., $\vec{F} \vec{dr} = \lVert \vec{F} \rVert \, \lVert \vec{dr} \rVert  \cos \theta$.

The two forces have to be in equilibrium (i.e., the we have to counteract the electric field with the same amount of work), but in opposite directions. Hence the integration domains have been flipped. This is useful, because we will be able to evaluate the right side with relative ease.

But wait a second, what really happened here?

## The Magic Switcheroo

This is an additional note I added here, because I think the integration boundary flipping above is a little more involved than it might seem at first. At first sight, switching from $\int_{\infty}^R$ to $\int_R^{\infty}$ sounds fine. After all, we just walk along the function and add together things, does it really matter in what order we do it? *Yes it does!* Let me explain. If we would be doing a normal addition, no, it wouldn't matter, however, integration gives us the **signed area** under the function, which is different when walking from left to right, or right to left. Not intuitive? This is a great lesson - sometimes, intuition only takes us so far, and we have to derive and prove our statements properly to really understand what is going on.

In this case, we have two beautiful ways of doing this.

### Explanation one

Consider the [fundamental theorem of calculus](https://en.wikipedia.org/wiki/Fundamental_theorem_of_calculus), where given $F'(x)=f(x)$, then a definite integral is defined as

$$\int_a^b f(x) \, dx = F(b) - F(a).$$

Now let's switch the integration domains to go from $b$ to $a$. We get

$$F(b) - F(a)=-(F(a) - F(b))=-\int_b^a f(x) \, dx,$$

therefore we can perform this switcheroo, provided that we multiply the integral by $-1$, because of the signed area argument above,

$$\int_a^b f(x) \, dx = -\int_b^a f(x) \, dx.$$

Thank you for [this source](https://math.stackexchange.com/questions/1316529/why-does-an-integral-change-signs-when-flipping-the-boundaries). It can also be explained in a different way, which is quite cool.

### Explanation two
A fundamental property of integrals if we have $a \leq b \leq c$, then we can break up the integration bounds as

$$\int_a^b f(x) \, dx + \int_b^c f(x) \, dx = \int_a^c f(x) \, dx$$

Now let's use the substitution of $a \leftarrow c$, i.e., swap both $c$'s for $a$'s,

$$\int_a^b f(x) \, dx + \int_b^a f(x) \, dx = \int_a^a f(x) \, dx.$$

Note that $\int_a^a f(x) \, dx=0$, therefore by reordering, we immediately get 

$$\int_a^b f(x) \, dx = -\int_b^a f(x) \, dx.$$

Very elegant and absolutely beautiful. Again, thank you for [this source](https://math.stackexchange.com/questions/1316529/why-does-an-integral-change-signs-when-flipping-the-boundaries) for the explanation.

# Back to the example of electrostatic potential

But we are still not done yet. There is no sign change between the two integrals we wrote, i.e.,
<img src="4-Electrostatic_Potential/work_against_electric_field.png" width="450" align="middle" style="display:block; margin: auto">

$$\int_{\infty}^{R} \vec{F}_{WL} \, \vec{dr}=\int_{R}^{\infty} \vec{F}_{e} \, \vec{dr}.$$

<<<<<<< HEAD
Where did the minus sign go? If you look at the image above, you'll see that $F_{WL}$ and $F_{e}$ look in the opposite direction, therefore the $-1$ multiplier is "baked in". So this is the story of the Magic Switcheroo. **All hail the Magic Switcheroo!** This was not trivial for me, at least not for the first sight, and hence I put here this explanation. If it was trivial for you, please stop reading this - go and build a time machine or something.
=======
	Where did the minus sign go? If you look at the image above, you'll see that $F_{WL}$ and $F_{e}$ look in the opposite direction, therefore the $-1$ multiplier is "baked in". So this is the story of the Magic Switcheroo. **All hail the Magic Switcheroo!** This was not trivial for me, at least not for the first sight, and hence I put here this explanation. If it was trivial for you, please stop reading this - go and build a time machine or something.
>>>>>>> origin/master

Now let's start evaluating this. On the right side, the electric force $\vec{F}_e$ can be computed via Coulomb's Law, and it will point in the same direction as $\vec{dr}$, which means that $\cos\theta=1$, we can forget about the vectors there, and we can move $\vec{F}_e$ out of the integral, thus, the electrostatic potential energy $U$ will be

$$U=\int_{R}^{\infty} \vec{F}_{e} \, \vec{dr} = \frac{q_1 q_2}{4\pi \epsilon_0} \int_{R}^{\infty}\frac{1}{r^2}dr=\frac{q_1 q_2}{4\pi \epsilon_0} \, \frac{1}{r}\Big\rvert_{R}^{\infty},$$

and continuing the substitution, we get that the work we have to do to bring that charge to the prescribed position is

$$U = \frac{q_1 q_2}{4\pi \epsilon_0 R}.$$

If $q_1,q_2$ are of the same sign, this is going to be a lot of work because we have to push against the will of the electric field. If they are of the opposite polarity, it will be easier, because the electric field will push the two charges together. Everything is pretty nice and *linear* here. Note that we are talking about work here, so the unit will be Joule. Much like gravity fields, the electric forces are also conservative, therefore the work being done is independent of the path taken. I can come in a straight line, or in some crazy staggering trajectory, the required work will be the same.

<sup>**Note:** If we have multiple charges, we can write up the same equations with them and use superposition.</sup>

# Electric potential

For the configuration below, we have a charge of $+Q$, and a test charge of $+q$ in point $p$ just $R$ distance away.

<img src="4-Electrostatic_Potential/electrostatic_potential_general.png" width="400" align="middle" style="display:block; margin: auto">

We already know the electrostatic potential energy, which was

$$U = \frac{q\, Q}{4\pi \epsilon_0 R}.$$

This is the work I have to do to bring the charge $+q$ to point $p$. The **electric potential** is the work *per unit charge* that I have to do to go from $\infty \rightarrow p$. This will be 

$$V_p = \frac{Q}{4\pi \epsilon_0 R}.$$

And is also a scalar and has a unit of $J/C$, or $V$, in short (yes, this is Volt). This makes sense, as the further away $p$ is, the bigger $R$ is, the less work we have to do. Of course, the higher $Q$ is, the more work we have to do. Both are nice and linear, hooray! 

<sup>**Note:** that this potential can be negative, of course, when we have a negative $Q$.</sup>

Now, we would like to know the electric potential around a Van de Graaff generator, a hollow sphere with the radius $R=0.3$ and and the charge of $+10 \mu C$, uniformly distributed (which follows from the fact that it is a conductor). What is the eletric potential at any point is space? Let's take the example of a point $p$ a distance $r$ away.

<img src="4-Electrostatic_Potential/electric_potential_example.png" width="400" align="middle" style="display:block; margin: auto">

$$V_p=\int_{r}^{\infty}\frac{\vec{F}_e}{q}\vec{dr}=\int_{r}^{\infty}\vec{E}\,\vec{dr}=\frac{Q}{4\pi \epsilon_0 r},$$
which is, of course, only true outside of the sphere, $r>R$. If we substitute the $r=R=0.3$ (we're on the surface of the sphere) and $Q=+10 \mu C$, we get $V_p=3.10^5V$. The work I have to do to bring the charge $q$ in my pocket to the Van de Graaff would be

$$W_{WL}=q\,V_p.$$

Note that **potential is work per unit charge**, where if I put the amount of charge I need to carry back into the equation, I get **work**. Approaching this Van de Graaff generator will be a lot of work - the same amount as climbing the Empire State Building. Better start working out!

As we approach the sphere, inside, due to the lack of the electric field, it will suddenly become much easier to carry this charge forward.

<img src="4-Electrostatic_Potential/van_de_graaff_potential.png" width="400" align="middle" style="display:block; margin: auto">