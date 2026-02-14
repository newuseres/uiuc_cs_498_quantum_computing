# <center> HW1</center>

<center> made by Jinhao Luo, netID: jinhao4, 2026 Feb 13 </center>

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
To prove such linear transformation T exisits.
We know T is a linear transformation, so we can write T as a matrix A.
$$
\langle u , Tv \rangle = u^\dagger Av = ( A^\dagger u )^\dagger v = \langle A^\dagger u , v \rangle
$$
Therefore, if we define $T^\dagger$ as the linear transformation represented by $A^\dagger$, we can get that $\langle u , Tv \rangle = \langle T^\dagger u , v \rangle$.

To prove such linear transformation is unique, we can assume that there are two linear transformations $T_1$ and $T_2$ that satisfy the condition $\langle u , Tv \rangle = \langle T_1^\dagger u , v \rangle= \langle T_2^\dagger u , v \rangle$.
$$
\therefore \langle T_1^\dagger u , v \rangle = \langle T_2^\dagger u , v \rangle \\
\langle (T_1^\dagger - T_2^\dagger) u , v \rangle = 0
$$
because for all $u$ and $v \in \mathbb{C}^n$, it satisfied.
So, we know $T_1^\dagger = T_2^\dagger$.

Thus, we can conclude that such linear transformation exists and is unique.

**(c)**

*(ii)*
By the definition of unitary transformation, we know that for any u,v $\in \mathbb{C}^n$, $\langle Uu,Uv \rangle = \langle u,v \rangle$.
$$
\langle Uu,Uv \rangle = u^*U^*Uv = \langle u,U^*Uv \rangle \\
 = \langle u,v \rangle
\therefore U^*U = UU^* = I
$$

*(iii)*

if we define the column of U as $u_1,u_2,...,u_n$, we can get that $U = [u_1,u_2,...,u_n]$.

from (ii), we can get that $U^*U = I$, so we can get that 

$$
\begin{bmatrix}
u_1^*u_1 & u_1^*u_2 & ... & u_1^*u_n \\
u_2^*u_1 & u_2^*u_2 & ... & u_2^*u_n \\
... & ... & ... & ... \\
u_n^*u_1 & u_n^*u_2 & ... & u_n^*u_n
\end{bmatrix} = I
$$
Therefore, we can get that $u_i^*u_j = 0$ when $i \neq j$ and $u_i^*u_i = 1$ when $i = j$.
From the definition of 
orthonormal basis (a set of vectors that are mutually orthogonal and each of them has unit length)
, we can conclude that the column of U forms an orthonormal basis of $\mathbb{C}^n$.

*(iv)*
if we define the row of U as $r_1,r_2,...,r_n$, we can get that $U = [r_1^T,r_2^T,...,r_n^T]^T$.
from (ii) we can get that $UU^* = I$, so we can get that $(UU^*)_{ij} = r_i r_j^*$,
So only when $i = j$, $r_i r_j^* = 1$, and when $i \neq j$, $r_i r_j^* = 0$.
From the definition of orthonormal basis (a set of vectors that are mutually orthogonal and each of them has unit length), we can conclude that the row of U forms an orthonormal basis of $\mathbb{C}^n$.

**(d)**
We know that $M(x,y) = \prod_{i=1}^n (-1)^{x_i y_i} = (-1)^{\sum_{i=1}^n x_i y_i}$ = $(-1)^{x \cdot y}$.
So when x and y have the odd number of same 1s, $M(x,y) = -1$, and when x and y have the even number of same 1s, $M(x,y) = 1$.
we know for every column of M, it has $2^n$ -1 or 1, and if we want to make M correspond to a scalar multiple of unitary transformation, we set M = $cU$.

and M = {m_i,m_2,...,}, where $m_i$ is the column of M.

we can calculate that $m_i^* m_i = 2^n$. so |m_i| = $\frac{1}{\sqrt{2^n}}$.

now we need to calculate $m_x^* m_y$ when $x \neq y$.
This time 
$$
m_y^* m_z = \sum_{x=\{0,1\}^n} M (x,y) M(x,z) \\
= \sum_{x=\{0,1\}^n} (-1)^{x \cdot y} (-1)^{x \cdot z} \\
= \sum_{x=\{0,1\}^n} (-1)^{x \cdot (y\oplus z)} \\
$$
because $y \neq z$, there is at least one bit that is different between y and z, so we substitute $y\oplus z$ with $w$ and $w \neq 0$.
Then we can get 
$$
m_y^* m_z = \sum_{x=\{0,1\}^n} (-1)^{x \cdot w} \\
= \sum_{x=\{0,1\}^n} \prod_{i=1}^n (-1)^{x_i w_i} \\
= \prod_{i=1}^n \sum_{x_i = \{0,1\}} (-1)^{x_i w_i} \\
$$
because $w \neq 0$, there is at least one $i$ such that $w_i = 1$, so $\sum_{x_i = \{0,1\}} (-1)^{x_i w_i} = 0$.
Therefore, $m_y^* m_z = 0$ when $y \neq z$.

Thus, we can conclude that M corresponds to a scalar multiple of unitary transformation, and the scalar is $\frac{1}{\sqrt{2^n}}$.
In this case ,$U = \frac{1}{\sqrt{2^n}} M$, and we can verify that $U^*U = I$.

<div style="page-break-after: always;"></div>

## 3 Projectors and Reflections

**(a)**
d = 2 
$$
Q = |\phi\rangle \langle \psi | \\

\text{when } |\psi\rangle = | 0 \rangle = (1 \ 0 )^T \\ and \ |\phi \rangle = | + \rangle = \frac{1}{\sqrt{2}} (1 \ 1)^T \\
Q = \begin{bmatrix}\frac{1}{\sqrt{2}} & 0 \\ \frac{1}{\sqrt{2}} & 0 \end{bmatrix}
\\ 
\text{when } |\psi\rangle = | + \rangle = \frac{1}{\sqrt{2}} (1 \ 1)^T \\ and \ |\phi \rangle = | 0 \rangle = (1 \ 0 )^T \\
Q = \begin{bmatrix}\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\ 0 & 0 \end{bmatrix}
$$
**(b)**
**(c)**
$|\phi\rangle$ 

0

**(d)**
The transformation P will project any vector to the one-dimensional subspace spanned by $|\phi\rangle$ -- remain the component of the vector in the direction of $|\phi\rangle$ and remove the component of the vector that is orthogonal to $|\phi\rangle$.

**(e)**
This transformation is a reflection transformation that reflects any vectors across the hyperplane perpendicular to $|\phi\rangle$.

Because I is a hermitian matrix and $(|\phi\rangle \langle \phi |)^* = (|\phi\rangle \langle \phi |)$
,so P is also a hermitian matrix.
And $R^* = (I - 2P)^* = I - 2P = R$, So I - 2P is a hermitian matrix as well.

we want to prove that $(I - 2P)^* (I - 2P) = I$.

We set R = I - 2P, so we need to prove that $R^* R = I$, i.e. $R^2 = I$.

$$
R^2 = (I - 2P)^2 = I - 4P + 4P^2 \\
= I - 4P + 4P = I
$$
Thus, we can conclude that R is a unitary transformation.

**(f)**
*(i)*
if we can prove that for any basis vector $|\psi_i\rangle$, U$|\psi_i\rangle$ = |$\phi_i\rangle$, then we can conclude that U is a matrix that maps the basis $\{|\psi_i\rangle\}$ to the basis $\{|\phi_i\rangle\}$.

$$
U|\psi_i\rangle = \sum_{j=1}^d |\phi_j\rangle \langle \psi_j | \psi_i \rangle \\
= \sum_{j=1}^d |\phi_j\rangle \delta_{ji} = |\phi_i\rangle
$$

So U can be written as $U = \sum_{i=1}^d |\phi_i\rangle \langle \psi_i |$.

Then we want to prove that U is a unitary transformation, i.e. $U^*U = I$.

U^* = $\sum_{i=1}^d |\psi_i\rangle \langle \phi_i |$.
$$
U^*U = \sum_{i=1}^d \sum_{j=1}^d |\psi_i\rangle \langle \phi_i | \phi_j\rangle \langle \psi_j | \\
= \sum_{i=1}^d \sum_{j=1}^d |\psi_i\rangle \delta_{ij} \langle \psi_j | \\
= \sum_{i=1}^d |\psi_i\rangle \langle \psi_i | = I
$$
Therefore, we can conclude that U is a unitary transformation.

*(ii)*

$I = \sum_{i=1}^d |\phi_i\rangle \langle \phi_i|$

It reflect any basis vector $|\psi_i\rangle$ to itself.

<div style="page-break-after: always;"></div>
## 4 Quantum Anti-Zeno Effect

set a integer n, and we set the $\epsilon = \frac{\pi}{2*n}$. Then every time, we perform a measurement on the state based on the basis $\{|\psi_k\rangle, |\psi_k^\perp\rangle\}$, where $|\psi_k\rangle = \cos(k\epsilon)|0\rangle + \sin(k\epsilon)|1\rangle$ and $|\psi_k^\perp\rangle = -\sin(k\epsilon)|0\rangle + \cos(k\epsilon)|1\rangle$.

Every time we perform a measurement, we expect to get the state $|\psi_k\rangle$.

For the first measurement, the k = 1, then k = 2 for the second measurement, and so on.  Ater the n-th measurement, k = n. Then we can get this qubit's state will be $|\psi_n\rangle = \cos(n\epsilon)|0\rangle + \sin(n\epsilon)|1\rangle = 1$.

When n is large enough, we can get that $\epsilon$ is small enough. And the ability of success in every process is $\cos^2(\epsilon)$. When n is large enough, $\cos^2(\epsilon) \approx 1-\epsilon^2/2$ and it's close to 1. So the probability of success in every process is close to 1, and the total probability of success is close to 1 as well. 

<div style="page-break-after: always;"></div>
## 5 Composite Quantum Systems
**(a)**
we know that 

$$
I = \begin{bmatrix}
    1 & 0 \\
    0 & 1
\end{bmatrix} \\
H = \frac{1}{\sqrt{2}} \begin{bmatrix}
    1 & 1 \\
    1 & -1  
\end{bmatrix} \\
I \otimes H = \frac{1}{\sqrt{2}} \begin{bmatrix}
    1 & 1 & 0 & 0 \\
    1 & -1 & 0 & 0 \\
    0 & 0 & 1 & 1 \\
    0 & 0 & 1 & -1  
\end{bmatrix} \\
H \otimes I = \frac{1}{\sqrt{2}} \begin{bmatrix}
    1 & 0 & 1 & 0 \\
    0 & 1 & 0 & 1 \\
    1 & 0 & -1 & 0 \\
    0 & 1 & 0 & -1
\end{bmatrix} \\
H \otimes H = \frac{1}{2} \begin{bmatrix}
    1 & 1 & 1 & 1 \\
    1 & -1 & 1 & -1 \\
    1 & 1 & -1 & -1 \\
    1 & -1 & -1 & 1
\end{bmatrix}
$$

**(b)**
$$
(I \otimes H)|0,1\rangle = ( I |0\rangle ) \otimes ( H |1\rangle )  = |0\rangle \otimes \frac{1}{\sqrt{2}} (|0\rangle - |1\rangle) \\
= \frac{1}{\sqrt{2}}(|0,0\rangle - |0,1\rangle) \\
(H \otimes I)|0,1\rangle = ( H |0\rangle ) \otimes ( I |1\rangle ) \\ = \frac{1}{\sqrt{2}} (|0\rangle + |1\rangle) \otimes |1\rangle \\   
= \frac{1}{\sqrt{2}}(|0,1\rangle + |1,1\rangle) \\
$$

**(c)**

We now set two qubits in the basis for $\mathbb{C}^{de}$
$$
|\phi_{ij}\rangle = |u_i\rangle \otimes |v_j\rangle \\
|\phi_{kl}\rangle = |u_k\rangle \otimes |v_l\rangle \\
\text{Their inner product =} \langle \phi_{ij} | \phi_{kl} \rangle \\
= (\langle u_i | \otimes \langle v_j |) (|u_k\rangle \otimes |v_l\rangle) \\
\\
= \langle u_i | u_k \rangle \cdot \langle v_j | v_l \rangle
\\ = \delta_{ik} \cdot \delta_{jl} 
$$
So if and only if $i = k$ and $j = l$, the inner product is 1, otherwise, the inner product is 0. So this set is a orthonormal sets. And we know that the number of vectors in this set is $de$, which is the same as the dimension of $\mathbb{C}^{de}$, so this set is an orthonormal basis for $\mathbb{C}^{de}$.

**(d)**
For every element in matrix $A \otimes B$, we can write it as
$$
(A \otimes B)_{ij,kl} = (\langle u_i | \otimes \langle v_j |) (A \otimes B) (| u_k \rangle \otimes | v_l \rangle) \\
= \langle u_i | A | u_k \rangle \cdot \langle v_j | B | v_l \rangle = A_{ik} \cdot B_{jl}
$$
We know that
$$
A = \sum_{i,k} A_{ik} |u_i\rangle\langle u_k|,  B = \sum_{j,l} B_{jl} |v_j\rangle\langle v_l|
$$

So we can get that 
$$
A \otimes B = \sum_{i,k} \sum_{j,l} \langle u_i | A | u_k \rangle \cdot \langle v_j | B | v_l \rangle \cdot (|u_i\rangle\langle u_k|) \otimes (|v_j\rangle\langle v_l|) \\
$$

**(e)**
No.
$$
|\psi\rangle = (\frac{1}{\sqrt{2}}(|0\rangle + |1\rangle) )^{\otimes n} = (|+\rangle)^{\otimes n} \\
$$
We can write the Alice part as $|\phi_A\rangle$ = $(|+\rangle)^{\otimes j}$
, and the Bob part as $|\phi_B\rangle$ = $(|+\rangle)^{\otimes n-j}$.
Then we can get that $|\psi\rangle = |\phi_A\rangle \otimes |\phi_B\rangle$.

By the definition of entangled state, we can conclude that $|\psi\rangle$ is not an entangled state, because it can be written as a tensor product of two states.