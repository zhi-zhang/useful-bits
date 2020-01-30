# Least Squares

TLDR:
Linear least square for **y<sub>i</sub>=β<sub>1</sub>x<sub>1</sub>+β<sub>2</sub>x<sub>2</sub>+...+β<sub>j</sub>x<sub>j</sub>+ε**.
Where **x** is the indepent variable, **y** is the dependent variable, **β** is the unknown parameters, **ε** is some random error.

The optimial values for the unknown parameters can be found by taking the [Moore Penrose inverse](https://en.wikipedia.org/wiki/Moore%E2%80%93Penrose_inverse)
**β = (X<sup>T</sup>X)<sup>-1</sup>X<sup>T</sup>y**


Explain: (incomplete).
Problem: 
Suppose for a set of obbservation that can be modeled using **y<sub>i</sub> = f(x<sub>i</sub>,β)**,
where **β** is a set of **m** **β**, ** **parameters,
find **β** that produce the best fitting model.
Optimal **β** can be found by minimising is the sum of squared residual **S = Σr<sub>i</sub><sup>2</sup>** , 
where **r<sub>i</sub>** is the residual **r<sub>i</sub> = y<sub>i</sub> - f(x<sub>i</sub>,β)**.

Solution:

The objective function **S = Σr<sub>i</sub><sup>2</sup>** is convex, 
therefor the minimum can be found by setting the gradients to zero

**∂S/∂β<sub>j</sub> = 2Σr<sub>i</sub>(∂r<sub>i</sub>/∂β<sub>j</sub>)=0**

subs **r<sub>i</sub> = y<sub>i</sub> - f(x<sub>i</sub>,β)** give
**-2Σr<sub>i</sub>(∂f(x<sub>i</sub>,β)/∂β<sub>j</sub>)=0**



Source:https://en.wikipedia.org/wiki/Least_squares
