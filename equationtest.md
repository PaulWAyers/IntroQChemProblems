# equationtest
All three equations have strong resemblance. But, in particular, the Schr&ouml;dinger equation and the Hamilton-Jacobi equation are consistent with each other. Suppose one uses the ansatz,
$$ \Psi(x,t) = \psi_0(x,t) e^{\frac{2 \pi i S(x,t)}{h}} $$
where $\psi_0(x,t)$ and $S(x,t)$ are, without loss of generality, assumed to be real-valued functions. We will insert this expression into the Schr&ouml;dinger equation, but first it is useful to define the quantity 
$$ \hbar = \tfrac{h}{2 \pi} $$
One then can rewrite the wavefunction and the Schr&ouml;dinger equation without the pesky factors of $2 \pi$, respectively,
$$ \Psi(x,t) = \psi_0(x,t) e^{\frac{i S(x,t)}{\hbar}} $$
$$ i \hbar \frac{d \Psi(x,t)}{dt} =  \left( -\frac{\hbar^2}{2m} \frac{d^2 \Psi(x,t)}{dx^2} + V(x,t)\Psi(x,t) \right) $$
Inserting the wavefunction into the Schr&ouml;dinger equation, the left-hand-side is
$$
 i \hbar \frac{d \Psi(x,t)}{dt} =e^{\frac{i S(x,t)}{\hbar}} \left( i \hbar \frac{d \psi_0(x,t)}{dt}-\psi_0(x,t) \frac{d S(x,t)}{dt} \right)
$$
and the right-hand-side is
$$
\left( -\frac{\hbar^2}{2m} \frac{d^2 \Psi(x,t)}{dx^2} + V(x,t)\Psi(x,t) \right) \\\\
= e^{\frac{i S(x,t)}{\hbar}} \left(-\frac{\hbar^2}{2m} \frac{d^2 \psi_0(x,t)}{dx^2} 
- \frac{i \hbar}{m}\frac{d \psi_0(x,t)}{dx}\frac{d S(x,t)}{dx} - \frac{i \hbar}{2m} \psi_0(x,t) \frac{d^2 S(x,t)}{dx^2} + \frac{1}{2m}\psi_0(x,t)\left(\frac{d S(x,t)}{dx}\right)^2 + V(x,t) \psi_0(x,t) \right) $$
Inserting these equations into the Schr&ouml;dinger equation and dividing through by $e^{\frac{i S(x,t)}{\hbar}}$ gives:
$$ \left( i \hbar \frac{d \psi_0(x,t)}{dt}-\psi_0(x,t) \frac{d S(x,t)}{dt} \right) 
= \left(-\frac{\hbar^2}{2m} \frac{d^2 \psi_0(x,t)}{dx^2} 
- \frac{i \hbar}{m}\frac{d \psi_0(x,t)}{dx}\frac{d S(x,t)}{dx} - \frac{i \hbar}{2m} \psi_0(x,t) \frac{d^2 S(x,t)}{dx^2} + \frac{1}{2m}\psi_0(x,t)\left(\frac{d S(x,t)}{dx}\right)^2 + V(x,t) \psi_0(x,t) \right) $$
The real and imaginary parts of this equation must be separately equal to each other. The real part of the equation is 
$$ - \psi_0(x,t) \frac{d S(x,t)}{dt}
= \left(-\frac{\hbar^2}{2m} \frac{d^2 \psi_0(x,t)}{dx^2} 
+ \frac{1}{2m}\psi_0(x,t)\left(\frac{d S(x,t)}{dx}\right)^2 + V(x,t) \psi_0(x,t) \right) $$
Dividing both sides by $\psi_0(x,t)$ and taking the classical limit, where $\hbar \rightarrow 0$, gives back the Hamilton-Jacobi equation,
$$ - \frac{d S(x,t)}{dt}
= \left(\frac{1}{2m}\left(\frac{d S(x,t)}{dx}\right)^2 + V(x,t) \right) $$
The imaginary part of the equation is:
$$ \hbar \frac{d \psi_0(x,t)}{dt} 
= - \left(\frac{\hbar}{m}\frac{d \psi_0(x,t)}{dx}\frac{d S(x,t)}{dx} + \frac{\hbar}{2m} \psi_0(x,t) \frac{d^2 S(x,t)}{dx^2} \right) $$
We notice that this expression is zero in the classical limit. Dividing through by $\hbar$ and using the chain rule, $\frac{d \left(\psi_0(x,t)\right)^2}{dt} = 2 \psi_0(x,t) \frac{d \psi_0(x,t)}{dt}$, we can rewrite this expression as
$$ \frac{d \left(\psi_0(x,t)\right)^2}{dt} 
= - \frac{d}{dx} \left(\psi_0(x,t)\right)^2 \left(\frac{1}{m}\frac{d S(x,t)}{dx}\right) $$
This expression resembles the [*equation of continuity*](https://en.wikipedia.org/wiki/Continuity_equation) from classical physics,
$$ \frac{d \rho(x,t)}{dt} = -\nabla \cdot \rho(x,t) \nabla v(x,t) $$
where $v(x,t)$ is the velocity and $\rho(x,t)$ is the density, the probability of observing a particle at the point $x$ and the time $t$. This (re)confirms that $\nabla S$ is an expression for the momentum, and suggests that $$\rho(x,t) = \psi_0(x,t)^2 = \Psi(x,t) \Psi(x,t)^* = |\Psi(x,t)|^2 $$ is an expression for the probability of observing a particle at a point in space. The identification of the square-magnitude of the quantum-mechanical wavefunction with probability is called the [*Born postulate*](https://en.wikipedia.org/wiki/Born_rule).

