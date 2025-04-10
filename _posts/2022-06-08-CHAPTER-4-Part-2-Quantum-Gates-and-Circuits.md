---
title: 'Chapter 4 Part 2 - Commentary - Quantum Gates and Circuits'
math: true
---


You already know bits are the fundamental entities that classical computers use to store and process information, and that bits can take on only one value: 0 or 1. But how do the bits *know* which values to assume?

You tell the bits what to do by providing instructions. When you use a computer, you're essentially issuing commands that cascade down to the fundamental computing components that control the bits and determine whether they're 0 or 1 at any given instant.

Suppose you send a text "Happy birthday!" to a friend. You open your messaging app, type out each letter, and hit send. Each step involves giving your device instructions. These are high-level instructions that you understand, like "type h" or "press enter." But your computing device breaks down each of these instructions into machine-level commands, and at the most fundamental level, these instructions control and manipulate strings of bits.

These instructions are carried out by *logic gates*, which perform operations on bits. Different gates can act on single or multiple bits at a time, each performing a specific operation. Combined, they produce the result you want.
Similarly, in quantum computing, there are *quantum gates* that act on qubits.

## Quantum Gates

Quantum gates are how we control qubits – they manipulate the quantum states of qubits. This means changing the probabilities of what you'd get if you measured the qubits.

In the Whiskertese marble analogy, a quantum gate changes how likely you are to see red or blue when you directly observe the marble.

## Quantum Circuits

Instructions can be written out using *quantum circuits*. A quantum circuit is a model depicting a sequence of quantum gates, measurements, and other actions on your qubits. While it isn't an actual physical circuit, it represents how the qubits will be manipulated.

Here's an example of what a quantum circuit looks like for three qubits:

![](/assets/imgs/ch4_3_qubit_circuit.png){: style="max-width: 500px"}

It looks sort of like a musical score, doesn't it? Just like sheet music, you read the circuit from left to right. Each horizontal line represents one qubit. The boxes and symbols on those lines are quantum gates, and the gray box at the end of each line represents a measurement. Notice how some quantum gates span multiple lines – these are gates that act on multiple qubits at once.

Remember, this quantum circuit is just a visual representation of instructions – think of it as an abstraction of what will happen in the physical hardware, not a diagram of actual electronic circuits. These instructions make up a *quantum algorithm.*
In Whiskerton, cats implement sequences of quantum gates through music, manipulating the states of their marbles. They know that specific musical notes create specific state changes in the marbles.

> If you’d like to dive deeper into quantum gates and circuits from a mathematical perspective, read on! Otherwise, head on over to the next page: [This is Not the End.](https://quantum-kittens.github.io/posts/This-is-not-the-end/)
{: .prompt-info }

_______

## Mathematical Representation of Quantum Gates

In chapter 2, you learned that we can represent an arbitrary qubit state using this equation:
\begin{equation}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

where $\alpha_{0}$ and $\alpha_{1}$ are probability amplitudes. These probability amplitudes tell us everything about the state. When a quantum gate changes the state, it changes these $\alpha$ (pronounced ‘alpha’) values.

Let's call our quantum gate $G$. When we apply $G$ to our initial state $\ket{\psi}$, the state changes like this:
\begin{equation} 
\alpha_{0}\ket{0}+\alpha_{1}\ket{1} \rightarrow \beta_{0}\ket{0}+\beta_{1}\ket{1}
\end{equation}

The new $\beta$ values (pronounced 'beta') are the probability amplitudes of our final state.

There's another helpful way to represent quantum states and gates if you know a bit of linear algebra. We can write the probability amplitudes as a column of numbers, or a *column vector* like so:

\begin{equation} 
v_\psi = \begin{bmatrix} 
\alpha_0 \\ 
\alpha_1 
\end{bmatrix} 
\end{equation}

This vector is called a *state vector*. Similarly, we can write any single-qubit quantum gate as a small grid of numbers (a $2 \times 2$ matrix):

\begin{equation} 
G = \begin{bmatrix} 
a & b \\ 
c & d 
\end{bmatrix} 
\end{equation}

You can then use standard matrix multiplication to determine the resulting state:
\begin{equation} 
\begin{bmatrix} 
a & b \\ 
c & d 
\end{bmatrix}  \begin{bmatrix} 
\alpha_0 \\ 
\alpha_1 
\end{bmatrix}  =  \begin{bmatrix} 
\beta_0 \\ 
\beta_1 
\end{bmatrix} 
\end{equation}

Let’s look at two specific examples of commonly used gates!

### NOT Gate
The quantum NOT gate is similar to its classical cousin. In classical computing, a NOT gate flips a bit from 0 to 1 or from 1 to 0. The quantum version does something similar – it swaps the probability amplitudes for $\ket{0}$ and $\ket{1}$. This means if your qubit was more likely to give you 0 when measured, after the NOT gate it becomes more likely to give you 1, and vice versa.

Here's what the NOT gate does:
\begin{equation} 
\ket{0} \rightarrow \ket{1} \\
\ket{1} \rightarrow \ket{0} \\
\alpha_{0}\ket{0}+\alpha_{1}\ket{1} \rightarrow \alpha_{1}\ket{0}+\alpha_{0}\ket{1}
\end{equation}

We can write the NOT gate as this matrix (also called the X gate or Pauli X gate):
\begin{equation} 
X = \begin{bmatrix} 
0 & 1 \\ 
1 & 0 
\end{bmatrix} 
\end{equation}

Try multiplying this matrix yourself with these three different states to see how it works:
\begin{equation} 
 \begin{bmatrix} 
0 \\ 
1 
\end{bmatrix} , \begin{bmatrix} 
1 \\ 
0 
\end{bmatrix} , \begin{bmatrix} 
\alpha_0 \\ 
\alpha_1 
\end{bmatrix} 
\end{equation}

### Hadamard Gate
Not all quantum gates have classical analogs like the NOT gate – in fact, most do not. The Hadamard gate is one of these uniquely quantum gates, and it's arguably one of the most important in quantum computing. Many quantum algorithms rely on it for initializing qubit states. What makes it so special? When applied to either $\ket{0}$ or $\ket{1}$, it creates an equally weighted superposition. 

Sound familiar? It's just like the marbles of Whiskerton that are by default in an equally weighted superposition of red and blue!

Here's what the Hadamard gate does: 
\begin{align} 
\ket{0} \rightarrow \frac{1}{\sqrt{2}}\ket{0}+\frac{1}{\sqrt{2}}\ket{1} \\
\ket{1} \rightarrow \frac{1}{\sqrt{2}}\ket{0}-\frac{1}{\sqrt{2}}\ket{1} \\
\frac{1}{\sqrt{2}}\ket{0}+\frac{1}{\sqrt{2}}\ket{1} \rightarrow \ket{0}  \\
\frac{1}{\sqrt{2}}\ket{0}-\frac{1}{\sqrt{2}}\ket{1} \rightarrow  \ket{1}
\end{align}

Those $\frac{1}{\sqrt{2}}$ values mean there's a 50-50 chance of measuring either 0 or 1. Notice that sometimes there's a minus sign. While this doesn't change the probabilities, it creates something called *phase* that we'll explore in a future chapter. It's like giving our marbles a special kind of spin.

Here's the Hadamard gate as a matrix:
\begin{equation} 
H = \frac{1}{\sqrt{2}}\begin{bmatrix} 
1 & 1 \\ 
1 & -1 
\end{bmatrix} 
\end{equation}

Try working through the matrix multiplication yourself to see how it creates these transformations.

An important note: the equally weighted single-qubit superposition states are so significant in quantum computing they get their own special symbols:
\begin{align}
\ket{+}=\frac{1}{\sqrt{2}}\ket{0}+\frac{1}{\sqrt{2}}\ket{1}\\
\ket{-}=\frac{1}{\sqrt{2}}\ket{0}-\frac{1}{\sqrt{2}}\ket{1}\\
\end{align}
——

## Special Note: Geometric Representation of Qubits
If you prefer a more visual mathematical representation, then perhaps a geometric representation of a qubit state would be helpful. An arbitrary state $\psi$ can be written in terms of sines and cosines such that the probability amplitudes are $\alpha_{0} =\cos{\theta}$ and $\alpha_{1} =\sin{\theta}$:
\begin{equation}
\ket{\psi}=\cos{\theta}\ket{0}+\sin{\theta}\ket{1}
\end{equation}
This is a valid representation—remember that the sum of probabilities must always add up to 1.
\begin{equation}
\alpha_{0}^2+\alpha_{1}^2=\cos^2{\theta}+\sin^2{\theta}=1
\end{equation}[^fn-nth-1]
[^fn-nth-1]: This is a fundamental trigonometric identity.

As a result, the arbitrary state $\ket{\psi}$ can be visually represented on a unit circle (that is, a circle of radius 1) like so:

![](/assets/imgs/ch4_2D_geo_rep_psi.png){: style="max-width: 500px"}

The green vector is the arbitrary state and the two axes correspond to the basis states $\ket{0}$ and $\ket{1}$.

If the angle $\theta$ is 45 degrees, you get the $\ket{+}$ state:

![](/assets/imgs/ch4_2D_geo_rep_plus.png){: style="max-width: 500px"}


With this representation, you can easily think of a quantum gate as acting on a qubit state such that the corresponding vector moves around this circle according to changes in $\theta$. 

It is important to not that this is *not* a complete representation of a qubit, because it doesn’t take into account that additional parameter I called ‘phase’ earlier. When we cover phase, you will encounter a more complete representation in three dimensions, called the *Bloch sphere*.

## Running Quantum Circuits
You now understand that quantum gates manipulate the probabilities within a quantum state. Thus a sequence of quantum gates in a quantum circuit or  a *quantum algorithm* manipulates state probabilities. Or, to phrase it in a different way, quantum algorithms manipulate the probabilities associated with each possible outcome.

You may naturally wonder: if there are probabilities associated with the results, then isn’t there a chance you may get an incorrect or undesirable result? And you’d be correct!

This is why, unlike classical circuits, we run quantum circuits multiple times and gather the results as statistics. Each time you run a circuit is called a *shot* and the more shots you run, the more accurate your results will be. 

Let’s take a look at a circuit in which there is a single qubit for which, after application of certain gates, it has a 4% chance of yielding 0 and a 96% chance of yielding 1 upon measurement. 

![](/assets/imgs/ch4_Luna_circuit.png){: style="max-width: 500px"}


This makes use of the X gate shown above, and another gate called the Rotation X ($R_X$) gate with an angle of $\frac{\pi}{8}$. [^fn-nth-2] 

[^fn-nth-2]: This $R_X$ gate rotates the qubit’s state around the x-axis by an angle of $\frac{\pi}{8}$. It also introduces a phase. We’ll see a visual representation of this rotation later.

Given how likely we are to get the result 1, if we associate blue with 0 and red with 1, then we have one of the possible quantum circuit representations of Luna playing Happy Birthday—remember that she manipulated the marble to be more likely to be red after observation!




_____________________________


_____________________________


_____________________________


**[Next: This is Not the End](https://quantum-kittens.github.io/posts/This-is-not-the-end/)**


## Qiskit Code

If you weren't familiar with quantum gates and circuits prior to this chapter, and would like to try coding them with Qiskit, return to the Qiskit sections in [Chapter 2 Part 2]() and [Chapter 3 Part 3]() to try your hands at coding circuits. 

Otherwise, try to code Luna's Happy Birthday circuit as an exercise!