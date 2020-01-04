Title: Calculus of variations and Euler–Lagrange equation
description: Euler–Lagrange equation
hero: Calculus of variations
authors:
    - Abhishek Aggarwal
date: 2020-01-04

# **Calculus of variations: Euler-Lagrange Equation**

Did you know that you could derive Newton's laws of motions from Lagrangian formulation? Incidentally, there is an even general principal in Physics called "Principal of least action". Although, I won't go into the physics of it here, I think the math involved in applying this principal is a beautiful mathematical technique called Calculus of variations. 

Variational Calculus is concerned with finding a extremum of an integral. There can be multiple paths between the end points of the integral. This technique allows us to find a path where this integral is at its maximum, or put it differently, where small variation in the path, does not change the value of the integral.

![Source: https://www.storyofmathematics.com/18th.html](./path_variations.gif#right)

## Problem Statement
We are given a _functional_ J (a fancy word for mapping that maps a function to a scalar). So J is a scalar value given by the integration of $f(x, \dot{x}, t)$ where $t$ is an independent variable. For now assume that $x$ is 1-dimensional.

$$ J = \int_{a}^{b} f(x, \dot{x}, t) dt$$

We are given $f$ is given to you, which exists [^1] across the paths between $a$ and $b$. So $J$ is a functional that maps $x(t)$ to a scalar number (say, in $\mathbb{R}$). We wish to find $x(t)$ which finds the stational point of $J$. 

So really, the equation should be rewritten as 

$$ J(x(t)) = \int_{a}^{b} f(x(t), \dot{x}(t), t) dt$$

Where $\dot{x} = \dot{x}(t)$ is a short hand for $\frac{dx(t)}{dt}$.

## Solution
So how do we find the stational point of $J$. In ordinal calculus, if we are to find a stationary point, say a minima, of a function $f(x)$, we can do that by equating $f'(x) = 0$. This is because, at a stationary point is one where a miniscule variation along $x$ does not change $f(x)$

But the problem here is different. $J(x(t))$ is not a function of independent variable $t$ but function of function $x(t)$ and we don't know what $x(t)$. Different x(t) should result in different paths between $t=a$ and $t=b$. And we don't know how to differentiate wrt a function now, do we?

The trick is to change dependence of $J$ to a variable $\alpha$ such that varying alpha in turn means plugging in different functions $x(t)$. To this end, lets write write an auxilliary function for $x(t)$

$$g(t, \alpha) = x(t) + \alpha \eta(t)$$

At $\alpha = 0$, $x(t, \alpha)$ reduces to $x(t)$. $\eta(t)$ can be any arbitrary function of $t$ such that $\eta(a)=\eta(b)=0$. Notice for a given $x(t), by varying $\alpha$ and $\eta(t)$, one can obtain any path $g(t, \alpha)$.

So without loss of generality, we can write

$$ J(g(t, \alpha)) = \int_{a}^{b} f(g(t, \alpha), \dot{g}(t, \alpha), t) dt$$


Now, the stationary point should exist where variation in the path should result in no change in $J$. Assume, that $x(t)$. Then variation in $x(t)$ is precisely given by varying alpha in $g(t, \alpha)$. So we have managed to quantify this variation to a variable wrt which we know how to differentiate. Thus, to find the stationary point we should have $\frac{\partial{J}}{\partial{\alpha}}) = 0$

$$ \frac{\partial{J}}{\partial{\alpha}} = \int_{a}^{b} \frac{\partial{f(g,\dot{g},t)}}{\partial{\alpha}}dt$$

We could move the derivative inside the integral since, the integral is wrt $t$ while the derivative is wrt $\alpha$. Expanding further, and applying chain rule, we have

$$ \frac{\partial{J}}{\partial{\alpha}} = \int_{a}^{b} \frac{\partial{f}}{\partial{g}}\frac{\partial{g}}{\partial{\alpha}}dt + \frac{\partial{f}}{\partial{\dot{g}}}\frac{\partial{\dot{g}}}{\partial{\alpha}}dt$$


We are going to need more mathematical juggling to simplify above. To this end, lets consider each of the addands inside the integral on the right hand side. The first term is easy, since $\frac{\partial{g}}{\partial{\alpha}} = \eta(t)$.


$$ \int_{a}^{b} \frac{\partial{f}}{\partial{g}}\frac{\partial{g}}{\partial{\alpha}} dt = \int_{a}^{b}  \frac{\partial{f}}{\partial{g}}\eta(t) dt$$

As for second term, recall that $\dot{g} = \frac{dg}{dt}$, which yields

$$\int_{a}^{b} \frac{\partial{f}}{\partial{\dot{g}}}\frac{\partial{\dot{g}}}{\partial{\alpha}}dt = \int_{a}^{b} \frac{\partial{f}}{\partial{\dot{g}}}\frac{\partial^2 {g}}{\partial{t}\partial{\alpha}}dt$$

Writing it this way, makes it look like we could use [integration by part][1] to further simplify this.

$$\int_{a}^{b} \frac{\partial{f}}{\partial{\dot{g}}}\frac{\partial{\dot{g}}}{\partial{\alpha}}dt = \frac{\partial{f}}{\partial{\dot{g}}} \frac{\partial{g}}{\partial{\alpha}} \bigg\rvert_{a}^{b} - \int_{a}^{b} \frac{d(\frac{\partial{f}}{\partial{\dot{g}}})}{dt} \frac{\partial{g}}{\partial{\alpha}}dt$$

Again, by substituing $\frac{\partial{g}}{\partial{\alpha}} = \eta(t)$, we get

$$\int_{a}^{b} \frac{\partial{f}}{\partial{\dot{g}}}\frac{\partial{\dot{g}}}{\partial{\alpha}}dt = \frac{\partial{f}}{\partial{\dot{g}}} \eta(t) \bigg\rvert_{a}^{b} - \int_{a}^{b} \frac{d(\frac{\partial{f}}{\partial{\dot{g}}})}{dt} \eta(t)dt$$

Now, since we are only concerned with paths that start from $a$ and end in $b$, we chose $\eta(t)$ that vanishes on both of these point. Consequently, we can get rid of the first term


$$\int_{a}^{b} \frac{\partial{f}}{\partial{\dot{g}}}\frac{\partial{\dot{g}}}{\partial{\alpha}}dt = - \int_{a}^{b} \frac{d(\frac{\partial{f}}{\partial{\dot{g}}})}{dt} \eta(t)dt$$


Substituting this result into our original equation, we get

$$ \frac{\partial{J}}{\partial{\alpha}} = \int_{a}^{b}  (\frac{\partial{f}}{\partial{g}} - \frac{d(\frac{\partial{f}}{\partial{\dot{g}}})}{dt} ) \eta(t)dt$$

Again recall, that at $\alpha = 0$, we the value of $g(t, \alpha = 0) = x(t)$ where $x(t)$ is the path of stationary point for the functional $J$. Therefore, we have

$$ \frac{\partial{J}}{\partial{\alpha}} \bigg\rvert_{\alpha=0} = \int_{a}^{b}  (\frac{\partial{f}}{\partial{x}} -  \frac{d(\frac{\partial{f}}{\partial{\dot{x}}})}{dt} ) \eta(t)dt = 0$$

Now we have situation, where for any arbitrary $\eta(t)$, the above integral is zero. This **must** [^2] mean that

$$\frac{\partial{f}}{\partial{x}} -  \frac{d(\frac{\partial{f}}{\partial{\dot{x}}})}{dt}  = 0 $$

which is the famous Euler-Lagrange Equation.


[^1]: _exists_ means that $f$ is continuous and differentiable. Also, $f$ could have been dependent of higher order differentials if we choose, but I am restricting this discussion to a special case of Euler-Langrange equation only.

[^2]: The fundamental lemma of caculus of variation states that if $\int M(x)N(x) = 0$ for arbitrary $N(x)$, the $M(x)$ must be zero. Intuitively, since integration is like summation, essentially, what one is saying is that is the production of two variables $a$ and $b$ is such that $ab = 0$ for arbitrary choice of $b$, then $a$ must be zero.

[1]: https://www.khanacademy.org/math/ap-calculus-bc/bc-integration-new/bc-6-11/v/deriving-integration-by-parts-formula
