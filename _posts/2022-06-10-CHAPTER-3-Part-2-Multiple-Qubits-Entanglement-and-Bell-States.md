---
title: 'Chapter 3 Part 2 - Commentary - Multiple Qubits, Entanglement, and Bell States'
math: true
---


There isn’t much you can do with a single classical bit. Information processing and algorithms usually require more units of information. For instance, down at the machine level, an image on your social media feed is not represented by a single bit. It is represented by *many* bits, many 0’s and 1’s, long strings of bits, and it is those bit strings that are transmitted across the internet and processed by your devices.

In a similar fashion, there isn’t much you can do with a single qubit, no matter how fancy a qubit may seem. In fact, the potential advantage of quantum computing over classical computing in certain contexts lies in being able to one day create processors with hundreds and maybe thousands of stable, perfect qubits.

Therefore, most quantum computing protocols involve more than one qubit, the way the doorbells of Whiskerton involve more than one marble. Granted, the doorbells of Whiskerton are still very simple quantum systems with only two marbles, whereas some of the algorithms designed for future quantum computers involve loads more. Nonetheless, these doorbells illustrate something that even more complex protocols make use of: a quantum phenomenon that has no analog in the classical world, *quantum entanglement*.

## What is Quantum Entanglement?

Quantum entanglement describes a peculiar connection or relationship between quantum systems. If two quantum systems are entangled, they are connected in such a way that their states cannot be described independently, and performing measurements on one system will affect the other, even if the second system isn’t nearby. 

In essence, the following is possible in the quantum world:

> Even if two qubits (or quantum systems) are too far apart to influence each other, they can still be correlated in such a way that tampering with one immediately affects the other.
{: .prompt-tip }

The two marbles in a Whiskertese doorbell are entangled. Remember that if one turns red, the second one does as well, even though the two are in separate boxes. No one needs to look directly at the second marble in order for it to reduce to a single color.  

This entanglement isn’t quite like the correlations we see in our everyday lives. In our classical world, if you have two marbles in an opaque bag, one red and one blue, and you pull out the blue one, you would know immediately that the red one was still in the bag. That’s classical correlation, the type of correlation we experience on the daily. 

However, quantum entanglement doesn’t behave like classical correlations. There are nuances to it that don’t translate to our everyday experience. For one, if the marbles were Whiskertese marbles, then they wouldn’t be a single color in the first place. The marble you pull out of the bag would be in a superposition until you looked at it. Only once the marble in your hand reduces to a single color would the marble in the bag change, even if the bag was taken far away from you. [^fn-nth-1]

[^fn-nth-1]: There are other nuances to entanglement as well, and two quantum systems that are very, very far apart must also be what is known as *non-local* to influence one another, but those are explorations for another day.

Since we’re talking about two entities immediately influencing one another despite distance between them, at this point you may rightfully wonder: does this mean we can send information faster than light? Unfortunately, the answer is no.

The catch is that simply performing any old type of measurement won’t work—yes, there are different *types* of measurements! The varying types of measurements are beyond the scope of the current text, but suffice it to say that if you and a friend who lives far away share an entangled pair, then the type of measurement you perform on your part of the pair must be conveyed to your friend somehow. If your friend doesn’t know which type of measurement to perform on their part, they won’t be able to ‘see’ the expected result! So some sort of communication must take place, say, through a telephone call. Which…cannot happen faster than light.

>If you’d like to dive a little deeper into quantum entanglement, read on! Otherwise, head on over to the next page: [This is Not the End](https://quantum-kittens.github.io/posts/This-is-not-the-end/).
{: .prompt-info }

_______

## Mathematical Representation of Multi-Qubit States

Multiple qubit states are represented in a similar manner to single qubit states. We’ll focus on two-qubit states since Whiskerton doorbells have two qubits, but the representation holds for even higher numbers.


Recall the equation for an arbitrary single qubit state from [Chapter 2](https://quantum-kittens.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/):


\begin{equation}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

In this equation, the basis states are analogous to the two values a classical bit can have: 0 and 1. And a qubit can be in a superposition of the two basis states. 

In order to understand how to represent a two-qubit state, let’s look at all the possible values of two classical bits. Two bits, combined, can have one of four values: 00, 01, 10, or 11. Just like the single qubit case, these four values correspond to four basis states. Two qubits can be in one of these four states or they can be in a superposition of these states! Therefore, an arbitrary two-qubit state can be represented by the following equation:

\begin{equation}
\ket{\psi}=\alpha_{00}\ket{00}+\alpha_{01}\ket{01}+\alpha_{10}\ket{10}+\alpha_{11}\ket{11}
\end{equation}

Just like the equation for a single qubit, $\alpha_{00}^2$ is the probability that the two qubits will yield the outcome 00 after measurement. Similarly for the other three basis states. Once again, the laws of probability dictate that $\alpha_{00}^2+\alpha_{01}^2+\alpha_{10}^2+\alpha_{11}^2=1$. 

## Entanglement and Bell States

Simply having two qubits in hand is not enough to consider them entangled. The qubits have to be in specific states in order to be considered entangled, which means there are certain $\alpha$ values that imply entanglement. 

For instance, in order to represent the entangled state of a Whiskertese doorbell, $\alpha_{01}=\alpha_{10}=0$ and the other two, $\alpha_{00}$ and $\alpha_{11}$, must be equal with their squares adding up to 1.

Let’s break this down. In a Whiskertese doorbell, the marbles become the same color after the outer marble is directly observed. If the marbles can only become the same color, then only two possible states are allowed: $\ket{red, red}$ and $\ket{blue, blue}$. The first position in each $\ket{}$ represents the outer marble, and the second position represents the inner marble. The state $\ket{red, blue}$ is illegal and can never happen within the doorbell apparatus, and so, the probability associated with it is zero. Same for $\ket{blue, red}$.

This means the only non-zero probabilities are the ones associated with $\ket{red, red}$ and $\ket{blue, blue}$, and since Whiskertese marbles have a 50-50 chance of becoming either color, the two probabilities must be equal.

So here is what that state looks like:


\begin{equation}
\ket{\phi^+}=\frac{1}{\sqrt{2}}\ket{00}+\frac{1}{\sqrt{2}}\ket{11}
\label{eq:bellstate}
\end{equation}

The marbles are in what is known as a "Bell state”—named after the physicist John S. Bell, and *not* because this is the state of the doorbells in Whiskerton. The above equation is what this particular Bell state looks like mathematically, where $\phi^+$ is a naming convention. [^fn-nth-2]

[^fn-nth-2]: This is what the Bell state looks like mathematically in the *computational basis*, which is a reference to the type of measurement required to ‘see’ the outcome. There are different bases associated with different types of measurements.

As you can see, there's an equal probability for either of the two basis states $\ket{00},\ket{11}$ to occur, before the first qubit is measured. But when the first qubit becomes either $\ket{0}$ or $\ket{1}$, then the second one has no choice but to follow. In this manner the outcomes are correlated, and the qubits are entangled. 

At this point it is important to note that this isn't the only Bell state; there are others. For instance, one of the other Bell states involves the second qubit always becoming the *opposite* of what the first becomes! But that's not how the entangled marbles of Whiskerton's doorbells behave.

These two-qubit pairs that are in Bell states are called EPR pairs, after physicists Albert Einstein, Boris Podolsky, and Nathan Rosen. EPR pairs and entanglement are a valuable resource for theoretical and potential quantum computing applications like quantum cryptography, superdense coding, and quantum teleportation. [^fn-nth-3]

[^fn-nth-3]: Teleportation in this context is not the teleportation you find in Star Trek. We plan to explore this application in a future story!
 
## Quick Note on Physical Entangled Qubits
 
Physically constructing entangled qubits in the lab depends on what you use for qubits. For instance, two photons from a single source, generated in a specific manner, may emerge entangled. There's no single universal 'entangler' the way there is in Whiskerton. And, more accurately, no one actually calls these sources 'entanglers'! Well, apart from cats.
 
_____________________________


_____________________________


_____________________________


**[Next: This is Not the End](https://quantum-kittens.github.io/posts/This-is-not-the-end/)**
 
________

## Qiskit Code

You can simulate a Whiskerton doorbell using the following code. By using this code, you will learn how to create the quantum circuit corresponding to the Bell state.

 ```python
# Importing standard Qiskit libraries
from qiskit import QuantumCircuit, transpile, Aer, IBMQ
from qiskit.tools.jupyter import *
from qiskit.visualization import *
from qiskit.providers.aer import QasmSimulator


#Create Doorbell Entangler Circuit

doorbell_circuit = QuantumCircuit(2, 2) # Create a circuit with two qubits (Whiskerton marbles) and two classical bits (to store the measurement outcome).

doorbell_circuit.h(0) # Add a Hadamard gate to the first qubit/ 

doorbell_circuit.cx(0,1) # Add a cnot gate with the first qubit as the control and the second qubit as the target. The target flips its state when the control is in the 1 state.

doorbell_circuit.measure([0,1],[0,1]) # Add measurement operators (this is equivalent to a cat looking directly at the outer marble).

doorbell_circuit.draw('mpl') # See how the circuit looks.

```

As an exercise, run this circuit in a similar way to the marble circuit in [Chapter 2](https://quantum-kittens.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/)!

*Note: the Qiskit code provided is open source, and does not fall under the copyright of Quantum Kittens.*


