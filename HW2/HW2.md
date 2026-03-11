HW2 Jinhao Luo jinhao4



# Problem 1

**(a)**

Let ${ |a_0>, |a_1> }$ as a pair of orthonormal basis in C^2

So, any vector $\phi \in C^2$ can be written as $\sum <ai| \phi |a_i>  $

Then we substitute $\phi$ as $\psi$, we can get the Alice to get result of |a_i >'s probability is
$$
|\psi> = \frac{1}{\sqrt{2}} ( <a_0|0>|a_0> + <a1|0>|a1> )\otimes |0>_B + ( <a_0|1><a_0> + <a_1|1>|a_1> )\otimes |1>_B \\
|\psi> = |a_0>_A \otimes [ \frac{1}{\sqrt{2}} (<a_0|0>|0>_B + <a_0|1>|1>_B ] + |a_1>_A \otimes [ \frac{1}{\sqrt{2}} (<a_1|0>|0>_B + <a_1|1>|1>_B ] \\
$$
So we can know the probability of getting a0 = 
$$
(1/\sqrt{2})^2 \times (|<a0|0>|^2 * <0|0> +　|＜a_0|1>|^2 * <1|1> + cross \ term )
$$
Because we know <1|0> = 0 , so the cross term = 0, and <0|0>, <1|1> = 1

And we know |<a0|0>|^2  +　|＜a_0|1>|^2  = 1, any unit vector project on any pair of orthonormal basis's sum always equals 1.

So P(a_i) = 1/2

**(b)**

After measurement, We know 
$$
|\psi'> = \frac{ (|a_i><a_i|\otimes I)|\psi> }{\sqrt{P(a_i)}} \\
 = \frac{1}{\sqrt{2}} *（|a_i><a_|0> \otimes |0> + |a_i><a_i|1> \otimes |1>　） / (1/\sqrt(2))\\
 = |ai> \otimes (<ai|0>|0> + <ai|1>|1>)
$$
If we set $|a_i> = c_0|0> + c1|1>$

So its bra is $ <a_i| = c_0^*<0| + c1^*<1| $

Then $ <ai|0> =    c0^* \ <a_i|1> = c_1^* $

So the Bob's state =  $  c_0^*|0> + c1^*|1>$ $

So we successfully prove that the post measurement state of EPR pair is $ |a_i> \otimes |a_i>^* $

**(c)**

Because we know that $|\phi_B> = |a_i>^*$ based on (b)'s result.

So knowing the Alice get |a_i>, the Bob get |b_j>'s probability =  P(b_j|a_i) = $ |<b_j|\phi_B>|^2$ = $|<b_j|a_i^*>|^2$

So for Bob $P(b_0|a_i) = |<b_0|a_i^*>|^2$

$P(b_1|a_i) = |<b_1|a_i^*>|^2$

**(d)**

As we know, First A then B, $P_{A\to B}(a_i,b_j) = P(a_i) \ P(b_j|a_i) = \frac{1}{2} |<bj|a_i^*>|^2$

Then if Bob measure it firstly.
We know Bob get the result of |b_j>'s probability is 1/2

Then we know that Alice's quantum bit will collapse to state $|b_j>^*$

Then we measure the Alice, we can get the conditional probability $P(a_i|b_j) = |<a_i|b_j^*>|^2 $

So their joint probability = $P(b_j|a_i) = \frac{1}{2} |<a_i|b_j^*>|^2 $

if we set $|a_i> = \sum c_k|k> \ |b_j> = \sum d_k |k>$

Because  $<a_i|b_j^*> = \sum c_k^*d_k^* = <bj|a_i^*> $

So we know they are same, the joint probability distribution of their outcomes is same.

**(e)**

No. We can not use quantum entanglement and quantum steering as a method for faster-than-light communication.

As we can know P(b_j) = 1/2, no matter Alice choose any basis or no measurement, in bob's perspective, there is always 1/2 probability. And if Alice choose a way to control Bob's result to particular basis, Alice can not control which result (a0 or a1) he can get. So, the probability is still 1/2. If there is no traditional channel for Alice to tell Bob what his result is, Bob will no way to find the connection.

# Problem 2

**(a)**

For (0,0,0), we need $ 0 \lor 0 \lor 0 = 0  $ $a \oplus b \oplus c = 0$

(1,1,0) $1 \lor 1 \lor 0 = 1$ $a \oplus b \oplus c = 1$

(1,0,1) $1 \lor 0 \lor 1 = 1$ $a \oplus b \oplus c = 1$

(0,1,1)  $0 \lor 1 \lor 1 = 1$ 

In best strategy, in (000), abc should have even 0, in others ones, abc should have odd 1.

While a0,a1,b0,b1,c0,c1 (answer based on what bit they get) happen twice. So their xor contirbution for 1 in these 4 games must be a even number. So there mast be a game lose. And if we set a0=0,a1=1,b0=0,b1=0,c0=0,c1=0, We can win 3 out of 4 games. So the winning probability is 3/4

**(b)**

Upon receiving question 0, we set their gate is X, upon receiving question 1, we set their gate  Y, and three bit quantum is $\phi$. 

So when we measure the 000, every one measure on the basis {|+>,|->}

So we know the state $1/\sqrt{2}( |000>+|111> ) = 1/\sqrt{2} (|+++> +  |---> )$

So the result will be 111 or 000, a=  b = c, win.

When we measure the 110, 101, 011,\

Two people measure under ${ 1/\sqrt{2}(|+>+|->), 1/\sqrt{2}(|+>-|->) }$, one measure under { |+>, |-> }

We can also know that  for (110) the operator is $(Y\otimes Y\otimes X)$, the same ones follow the symmetric calculations. We know that

$ X|0> = |1> X|1> = |0> $

$ Y|0> = i|1> Y|1> = -i|0> $

$(Y\otimes Y\otimes X) |\phi> = 1/\sqrt{2}( (Y|0>Y|0>X|0>) + Y|1>Y|1>X|1> )$

$= 1/\sqrt{2} ( i^2|111> +(-i)^2|000> ) = -1|\phi>$

Their satisfy that 100% we get -1.

P = (1+1+1+1) / 4 = 1

So the winning probability = 100%.

# Problem 3

$$
|\theta> = 1/\sqrt{3}|00> - 1/\sqrt{6}|01> + 1/\sqrt{6}|10> +1/\sqrt{3}|11> \\
|\theta> = 1/\sqrt{2}[ (|0>_A \otimes(2/\sqrt{3}|0> - 1/\sqrt{3}|1>)_B + |1>_A\otimes(1/\sqrt{3}|0> + 2/\sqrt{3}|1>)_B] \\
$$

 So we can find that for standard state $ \phi = 1/\sqrt{2}[ |00> + |11> ]$
$$
So |\theta> = (I \otimes V)|\phi> , V =   \begin{pmatrix} \sqrt{2/3} & \sqrt{1/3} \\ -\sqrt{1/3} & \sqrt{2/3} \end{pmatrix}
$$
Then
$$
\text{ As we know } (M \otimes I) |\phi> = ( I \otimes M^T )|\phi> \\
So  |\theta> = (V^T \otimes I)|\phi> = (V^T \otimes I)|\phi> \\
\text{And we need perform a unitary } U  = (V^T)^{-1} \text{ on Alice} \\
\text{So } U_A =  (V^T)^{-1} = V \\
\text{In this case } (U_A \otimes I)|\theta> = (V \otimes I)(V^T\otimes I)|\phi> = (VV^T  \otimes I)|\phi> = |\phi>
$$
In this way, state is recovered to standard Bell state.

So Alice then use its' gift quantum bit |phi> to measure, then send the measurement's result to Bob, Bob get the result based on standard protocal.



# Problem 4



Firstly, Alice and Bob share a EPR, Bob and Carol share a EPR 

 We set Alice have qubit A, Bob have qubits B, B' (we assume that qubit B is Bob sharing with Alice, and qubit B' is Bob sharing with Carol), Carol has C.

Bob measure its two qubits B , B' will project them into 

Their are four possible $|\Phi^\pm>$ or $|\Psi^\pm>$ bell state

Then Bob will inform the result of 2 classical bit's result  to Carol.

When Bob measures $|\Phi^+>$ , Carol perform I

Bob $|\Phi^->$ Carol Z gate

Bob $|\Psi^+>$ Carol X gate

Bob $|\Psi^->$ Carol XZ gate

Now Alice and Carol are sharing the Standard EPR $|\Phi^+>$

