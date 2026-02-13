# <center> HW1 Jinhao Luo</center>


<div style="page-break-after: always;"></div>

## 1 Ket notation
**(a)**
It should satisfy that $|\psi\rangle$ is normalized:
$\langle \psi | \psi \rangle = 1$
$$
\because |\frac{3}{C}|^2 + |\frac{-5i}{C}|^2 = 1 \\
\therefore  C = \sqrt{34} \\
|\psi\rangle = \frac{3}{\sqrt{34}}|0\rangle + \frac{-5i}{\sqrt{34}}|1\rangle
$$
**(b)**
if two basis are orthonomal, they should satisfy that $\langle i | -i \rangle = 0$ and $\langle i | i \rangle = 1$ and $\langle -i | -i \rangle = 1$.
$$
\because \langle i | -i \rangle = 0 \\
\langle i | i \rangle = 1 \\
\langle -i | -i \rangle = 1 \\
\therefore \text{the basis is orthonormal}
$$
For the possible outcomes, we can calculate the probability of each outcome:
$$
\text{the probability of outcome } i = \langle i | \psi \rangle^2 \\
\langle i | \psi \rangle = \frac{1}{\sqrt{34}}\cdot \frac{1}{\sqrt{2}}\left(\langle 0 | - i \langle 1 | \right) \left( 3 |0\rangle + -5i|1\rangle \right) \\
= -\frac{2}{\sqrt{68}} \\
\therefore P(i) = |\langle i | \psi \rangle|^2 = \frac{1}{17} \\
$$
Calculating the probability of outcome $-i$ as well:
$$
\langle -i | \psi \rangle = \frac{1}{\sqrt{34}}\cdot \frac{1}{\sqrt{2}}\left(\langle 0 | + i \langle 1 | \right) \left( 3 |0\rangle + -5i|1\rangle \right) \\
= \frac{8}{\sqrt{68}} \\
\therefore P(-i) = |\langle -i | \psi \rangle|^2 = \frac{16}{17}
$$

<div style="page-break-after: always;"></div>

## 2 Unitary transformations.
**(a)**
For (i) -> (ii), if we know that T is unitary, $T^*T = I$
$$
\langle Tu,Tv \rangle = (Tu)^*Tv\\ = u^*T^*Tv \\= u^*Iv\\ = \langle u,v \rangle

$$
For (ii) -> (iii)
We know that
$$
||u||^2 = \langle u,u \rangle = 1 \\
\langle u,u \rangle = \langle Tu,Tu \rangle \\
||Tu||^2 = ||u||^2 = 1
$$
Therefore, T maps unit vectors $u$ to unit vectors $Tu$.

For (iii) -> (i)
if a linear transformation T maps unit vectors to unit vectors, so for any unit vector $u$,
$$
||Tu||^2 = \langle Tu,Tu \rangle \\
= u^*T^*Tu \\
= \langle u|T^*Tu \rangle \\
  = 1
$$
only when $T^*T = I$, this situation can be satisfied by any uni vector. Therefore, T is unitary.

**(b)**

**(c)**

**(d)**


<div style="page-break-after: always;"></div>
## 3 Projectors and Reflections

**(a)**

**(b)**

**(c)**

**(d)**

**(e)**

**(f)**
