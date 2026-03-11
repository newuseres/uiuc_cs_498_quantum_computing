# Problem 1

**(a)**

We write the nth quantum qubit's system state as $|\psi> = \alpha |0> \otimes |\psi_0> + \beta |1> \otimes |\psi_1>$

For situation of origin circuits.

Then put measurement on the first bit: 

Probability of (b=0) = $|\alpha|^2$ 

after measurement, the state will become $|0>\otimes|\psi_0>$

Probability of (b=1) = $|\beta|^2$ 

For circuit of using CNOT gate:

$|\psi> =  |\psi> \otimes |0> = \alpha|0>|\psi_0>|0> + \beta|1>|\psi_1>|0> $

after the measurement, the state will become $|0>\otimes|\psi_1>$

Then put CNOT, the state became:

$ \alpha|0>|\psi_0>|0> + \beta|1>|\psi_1>|1> $

Using measurement on n+1 bit:

Probability of (b=0) = $ |\alpha|^2 $

The state of first n bits will become $ |0>|\psi_0> $

Probability of (b=1) = $|\beta|^2$

The state of first n bits will become $ |1>|\psi_1> $

**(b)**

We set the state after applying CNOT gate as  $ \alpha|0>|\psi_0>|0> + \beta|1>|\psi_1>|1> $

If we measure the (n+1) qubit immediately, the situation will be same as the situation we have analyzed before.

If we measure the (n+1) qubit after very end. We can know in that time, the state will become (we set U as the circuit after CNOT, U will only perform on first n qubits)

$ \alpha U(|0>|\psi_0> ) |0> +   \beta( U(|1>|\psi_1>) )|1> $

Then we measure the (n+1) qubit, 

The probability of (b=0) = $ || \alpha U(|0>|\psi_0> )  ||^2 = |\alpha|^2 $

The first n state will become $ U(|0>|\psi_0> ) $

And the probability of b=1 is as well $|\beta|^2$

The first n state will become $ U(|1>|\psi_0> ) $

They are the same.

**(c)**

We set the controlled U as $C_U$

$C_U(|0>|\psi>) = |0>|\psi>$

$C_U(|1>|\psi>) = |1>(U|\psi>) $

So $C_U = |0><0| \otimes I + |1><1| \otimes U $

So we write its transposed conjugated  $C_U^\dagger = |0><0|\otimes I + |1><1| \otimes U^\dagger  $
$$
 C_U^\dagger  C_U = (|0><0|\otimes I) + (|1><1|\otimes(U^\dagger U)) \\
 = (|0><0| + |1><1|) \otimes I  = I \otimes I = I
$$


**(d)**

It's right that. If we measure the (n+1)-the qubit or not, the first n bits is a mixed state. It doesn't change them at all.

**(e)**

We do not need to do the CNOT. Since we have used the controlled-U, we actually use the first qubit to control the U gate after that. It's equal to "CNOT to (n+1)-th bit, measure it, then control the U by (n+1)bit's result".

Since the different procedures we get the same state, same answer, there is no need to add a additional CNOT.

# Problem 2

**(a)**

For classical algorithm to determine the answer for the problem, it's possible that until $2^{n-1} times$ we still get all the same. Only when we use $2^{n-1}+1$, we can know it is constant or balanced.

**(b)**

We randomly select 8 input, and if there are different output values, we know f is balanced. And if 8 output values are same, we guess f is constant.

For f is constant, the correct probability is 100%. For f is balanced. the only situation we are wrong is that 8 output values is the same, the probability is $$(\frac{1}{2})^7 = \frac{1}{128} \approx 0.0078$$ So the correct probability is larger than $ \frac{127}{128} $. It satisfy the requirements.

**(c)** 

We add a auxiliary (n+1)-th bit $|1> $ after $|x>$, Then we describe this circuit.

1. Apply Hadamard gate H on this auxiliary bit, state becomes $|x>|->$

2. Apply $U_f$ for these (n+1) bits. We can get 
   $$
   U_f |x>|-> = |x> \frac{ |0\otimes f(x)> - |1 \otimes f(x) > }{\sqrt{2}}
   $$

3. Then apply Hadamard gate H on this auxiliary bit, last bit return to |1>

   We can know that if f(x) = 0, the first n bits will remain $|x>|1>$ , if f(x) = 1, the first n bits will become $-|x>|1>$ 

   So this circuit achieve $ O_f |x> = (-1)^{f(x)} |x> $

4. d 

# Problem 3



# Problem 4

