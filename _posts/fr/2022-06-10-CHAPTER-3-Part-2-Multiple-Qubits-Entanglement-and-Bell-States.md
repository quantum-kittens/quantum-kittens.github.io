---
title: 'Chapitre 3 Partie 2 - Commentaires - Qubits Multiples, Intrication, et Etats de Bell'
math: true
---


___There isn’t much you can do with a single classical bit. Information processing and algorithms usually require more units of information. For instance, down at the machine level, an image on your social media feed is not represented by a single bit. It is represented by *many* bits, many 0’s and 1’s, long strings of bits, and it is those bit strings that are transmitted across the internet and processed by your devices.___

Il n'y a pas grand-chose que vous puissiez faire avec un seul bit classique. Le traitement de l'information et les algorithmes nécessitent généralement plusieurs unités d'information. Par exemple, au niveau de la machine, une image sur votre fil d'actualité des réseaux sociaux n'est pas représentée par un seul bit. Elle est représentée par *plusieurs* bits, de nombreux 0 et 1, et ce sont ces chaînes de bits qui sont transmises sur internet et traitées par vos appareils.

___In a similar fashion, there isn’t much you can do with a single qubit, no matter how fancy a qubit may seem. In fact, the potential advantage of quantum computing over classical computing in certain contexts lies in being able to one day create processors with hundreds and maybe thousands of stable, perfect qubits.___

De la même manière, il n'y a pas grand-chose que vous puissiez faire avec un seul qubit, aussi sophistiqué soit-il. En réalité, l'avantage potentiel de l'informatique quantique par rapport à l'informatique classique dans certains contextes réside dans la possibilité de créer un jour des processeurs avec des centaines, voire des milliers de qubits stables et parfaits.

___Therefore, most quantum computing protocols involve more than one qubit, the way the doorbells of Whiskerton involve more than one marble. Granted, the doorbells of Whiskerton are still very simple quantum systems with only two marbles, whereas some of the algorithms designed for future quantum computers involve loads more. Nonetheless, these doorbells illustrate something that even more complex protocols make use of: a quantum phenomenon that has no analog in the classical world, *quantum entanglement*.___

Par conséquent, la plupart des protocoles de calcul quantique impliquent plus d'un qubit, tout comme les sonnettes de Whiskerton impliquent plus d'une bille. Certes, les sonnettes de Whiskerton sont encore des systèmes quantiques très simples avec seulement deux billes, alors que certains des algorithmes conçus pour les futurs ordinateurs quantiques en nécessitent beaucoup plus. Néanmoins, ces sonnettes illustrent un phénomène quantique dont même les protocoles plus complexes tirent parti : un phénomène quantique qui n'a pas d'équivalent dans le monde classique, *l'intrication quantique*.

## What is Quantum Entanglement?

## Qu'est ce que l'Intrication Quantique ?

___Quantum entanglement describes a peculiar connection or relationship between quantum systems. If two quantum systems are entangled, they are connected in such a way that their states cannot be described independently, and performing measurements on one system will affect the other, even if the second system isn’t nearby.___

L'intrication quantique décrit une connexion ou une relation particulière entre des systèmes quantiques. Si deux systèmes quantiques sont intriqués, ils sont connectés de telle manière que leurs états ne peuvent pas être décrits indépendamment, et effectuer des mesures sur l'un des systèmes affectera l'autre, même si le second système n'est pas à proximité.

___In essence, the following is possible in the quantum world:___

En essence, ce qui suit est possible dans le monde quantique :

> ___Even if two qubits (or quantum systems) are too far apart to influence each other, they can still be correlated in such a way that tampering with one immediately affects the other.___
{: .prompt-tip }



___The two marbles in a Whiskertese doorbell are entangled. Remember that if one turns red, the second one does as well, even though the two are in separate boxes. No one needs to look directly at the second marble in order for it to reduce to a single color.___

___This entanglement isn’t quite like the correlations we see in our everyday lives. In our classical world, if you have two marbles in an opaque bag, one red and one blue, and you pull out the blue one, you would know immediately that the red one was still in the bag. That’s classical correlation, the type of correlation we experience on the daily.___

___However, quantum entanglement doesn’t behave like classical correlations. There are nuances to it that don’t translate to our everyday experience. For one, if the marbles were Whiskertese marbles, then they wouldn’t be a single color in the first place. The marble you pull out of the bag would be in a superposition until you looked at it. Only once the marble in your hand reduces to a single color would the marble in the bag change, even if the bag was taken far away from you.___ [^fn-nth-1]

[^fn-nth-1]: ___There are other nuances to entanglement as well, and two quantum systems that are very, very far apart must also be what is known as *non-local* to influence one another, but those are explorations for another day.___

___Since we’re talking about two entities immediately influencing one another despite distance between them, at this point you may rightfully wonder: does this mean we can send information faster than light? Unfortunately, the answer is no.___

___The catch is that simply performing any old type of measurement won’t work—yes, there are different *types* of measurements! The varying types of measurements are beyond the scope of the current text, but suffice it to say that if you and a friend who lives far away share an entangled pair, then the type of measurement you perform on your part of the pair must be conveyed to your friend somehow. If your friend doesn’t know which type of measurement to perform on their part, they won’t be able to ‘see’ the expected result! So some sort of communication must take place, say, through a telephone call. Which…cannot happen faster than light.___

>___If you’d like to dive a little deeper into quantum entanglement, read on! Otherwise, head on over to the next page: [This is Not the End](https://quantum-kittens.github.io/posts/This-is-not-the-end/).___
{: .prompt-info }

_______

## Mathematical Representation of Multi-Qubit States

___Multiple qubit states are represented in a similar manner to single qubit states. We’ll focus on two-qubit states since Whiskerton doorbells have two qubits, but the representation holds for even higher numbers.___


___Recall the equation for an arbitrary single qubit state from [Chapter 2](https://quantum-kittens.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/):___


\begin{equation}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

___In this equation, the basis states are analogous to the two values a classical bit can have: 0 and 1. And a qubit can be in a superposition of the two basis states.___

___In order to understand how to represent a two-qubit state, let’s look at all the possible values of two classical bits. Two bits, combined, can have one of four values: 00, 01, 10, or 11. Just like the single qubit case, these four values correspond to four basis states. Two qubits can be in one of these four states or they can be in a superposition of these states! Therefore, an arbitrary two-qubit state can be represented by the following equation:___

\begin{equation}
\ket{\psi}=\alpha_{00}\ket{00}+\alpha_{01}\ket{01}+\alpha_{10}\ket{10}+\alpha_{11}\ket{11}
\end{equation}

___Just like the equation for a single qubit, $\alpha_{00}^2$ is the probability that the two qubits will yield the outcome 00 after measurement. Similarly for the other three basis states. Once again, the laws of probability dictate that $\alpha_{00}^2+\alpha_{01}^2+\alpha_{10}^2+\alpha_{11}^2=1$.___

## Entanglement and Bell States

___Simply having two qubits in hand is not enough to consider them entangled. The qubits have to be in specific states in order to be considered entangled, which means there are certain $\alpha$ values that imply entanglement.___

___For instance, in order to represent the entangled state of a Whiskertese doorbell, $\alpha_{01}=\alpha_{10}=0$ and the other two, $\alpha_{00}$ and $\alpha_{11}$, must be equal with their squares adding up to 1.___

___Let’s break this down. In a Whiskertese doorbell, the marbles become the same color after the outer marble is directly observed. If the marbles can only become the same color, then only two possible states are allowed: $\ket{red, red}$ and $\ket{blue, blue}$. The first position in each $\ket{}$ represents the outer marble, and the second position represents the inner marble. The state $\ket{red, blue}$ is illegal and can never happen within the doorbell apparatus, and so, the probability associated with it is zero. Same for $\ket{blue, red}$.___

___This means the only non-zero probabilities are the ones associated with $\ket{red, red}$ and $\ket{blue, blue}$, and since Whiskertese marbles have a 50-50 chance of becoming either color, the two probabilities must be equal.___

___So here is what that state looks like:___


\begin{equation}
\ket{\phi^+}=\frac{1}{\sqrt{2}}\ket{00}+\frac{1}{\sqrt{2}}\ket{11}
\label{eq:bellstate}
\end{equation}

___The marbles are in what is known as a "Bell state”—named after the physicist John S. Bell, and *not* because this is the state of the doorbells in Whiskerton. The above equation is what this particular Bell state looks like mathematically, where $\phi^+$ is a naming convention.___ [^fn-nth-2]

[^fn-nth-2]: ___This is what the Bell state looks like mathematically in the *computational basis*, which is a reference to the type of measurement required to ‘see’ the outcome. There are different bases associated with different types of measurements.___

___As you can see, there's an equal probability for either of the two basis states $\ket{00},\ket{11}$ to occur, before the first qubit is measured. But when the first qubit becomes either $\ket{0}$ or $\ket{1}$, then the second one has no choice but to follow. In this manner the outcomes are correlated, and the qubits are entangled.___

___At this point it is important to note that this isn't the only Bell state; there are others. For instance, one of the other Bell states involves the second qubit always becoming the *opposite* of what the first becomes! But that's not how the entangled marbles of Whiskerton's doorbells behave.___

___These two-qubit pairs that are in Bell states are called EPR pairs, after physicists Albert Einstein, Boris Podolsky, and Nathan Rosen. EPR pairs and entanglement are a valuable resource for theoretical and potential quantum computing applications like quantum cryptography, superdense coding, and quantum teleportation.___ [^fn-nth-3]

[^fn-nth-3]: ___Teleportation in this context is not the teleportation you find in Star Trek. We plan to explore this application in a future story!___
 
## Quick Note on Physical Entangled Qubits
 
___Physically constructing entangled qubits in the lab depends on what you use for qubits. For instance, two photons from a single source, generated in a specific manner, may emerge entangled. There's no single universal 'entangler' the way there is in Whiskerton. And, more accurately, no one actually calls these sources 'entanglers'! Well, apart from cats.___
 
_____________________________


_____________________________


_____________________________


**[Next: This is Not the End](https://quantum-kittens.github.io/posts/This-is-not-the-end/)**
 
________

## Qiskit Code

___You can simulate a Whiskerton doorbell using the following code. By using this code, you will learn how to create the quantum circuit corresponding to the Bell state.___

 ```python
# Import necessary Qiskit libraries
from qiskit import QuantumCircuit, transpile
from qiskit.visualization import *
from qiskit import BasicAer

#Load your IBM Quantum account(s)
#provider = IBMQ.load_account()


#Create Doorbell Entangler Circuit

doorbell_circuit = QuantumCircuit(2, 2) # Create a circuit with two qubits (Whiskerton marbles) and two classical bits (to store the measurement outcome).

doorbell_circuit.h(0) # Add a Hadamard gate to the first qubit/ 

doorbell_circuit.cx(0,1) # Add a CNOT gate with the first qubit as the control and the second qubit as the target. The target flips its state when the control is in the 1 state.

doorbell_circuit.measure([0,1],[0,1]) # Add measurement operators (this is equivalent to a cat looking directly at the outer marble).

doorbell_circuit.draw('mpl') # See what the circuit looks like.


```

___The above code is also available as a jupyter notebook [here](https://github.com/quantum-kittens/quantum-kittens.github.io/blob/main/jupyter_notebooks/QK_Chapter_3.ipynb).___

___As an exercise, run this circuit in a similar way to the marble circuit in [Chapter 2](https://quantum-kittens.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/)!___

___*Note: the Qiskit code provided is open source, and does not fall under the copyright of Quantum Kittens.*___


