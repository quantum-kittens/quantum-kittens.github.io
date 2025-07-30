---
title: 'Chapter 2 Part 2 - Commentary - Qubits, Superposition, and Measurement'
math: true
---



You very likely know what classical computing is; it’s what most people mean when they say “computing”. This is the computing done by everyday electronic gadgets like the device you’re using to read this, and even the computing done by supercomputers tucked away in labs.

Deep down at the fundamental level of a classical computer, information is carried by *bits*: single units of information that can have only one of two values or *states*: 0 or 1.  In much the same way, quantum computers have a fundamental computing unit, called quantum bits or *qubits*. Here’s a fun fact: the marbles of Whiskerton actually represent qubits!

## What is a Qubit?

A qubit is the simplest system in quantum computing, the fundamental building block for quantum computation. Physically, qubits can take a number of different forms, depending on the hardware a quantum computer uses. But, behaviorally, they act the same way. So you can consider a ‘qubit’ to be an abstract mathematical object that behaves in a curious manner different from a classical bit. Classical bits can take on one of two values, 0 and 1, but a qubit can do that and more:

> Qubits are abstract mathematical objects that have the ability to not only be in the states 0 or 1, but in a *superposition* of the two. 
{: .prompt-tip }

## Quantum Superposition

Quantum superposition is a neat quantum physics phenomenon that doesn’t really have an analog in classical physics. You can think of it as a combination. 

Where classical bits can only ever be in state 0 or 1 and never a combination of the two, quantum states can be combined and still be valid states. So the state of a qubit can be a combination of 0 *and* 1.

![](/assets/imgs/Marble_Animation.png){: style="max-width: 150px" .left} In Whiskerton, the marbles are by default in such a superposition state: an equally weighted combination of the colors red and blue. It would be incorrect to think of these colors as paint colors. In your everyday, classical experience, if you combine red and blue paint, you would get purple paint. But Whiskertese marbles aren’t actually purple; after a cat directly observes a marble, the color can turn either red or blue, with a fifty percent chance for each. You definitely cannot get the colors red or blue back if you have purple paint!

Being able to make use of this wondrous phenomenon is one of the ways quantum computing differs from classical computing. In a classical computer, if you perform an operation on a bit, you’re essentially performing that operation on either a 0 or 1, one at a time. If you need to perform an operation on both, you’d have to do so in two shots, consecutively. 

But by harnessing superposition, a quantum computer could perform that operation on both 0 and 1 at the same time. If we scale this up to many qubits, you can imagine how this may potentially result in speed-ups or an increase in memory capacity or other improvements.

## Measurements

You’ve seen that the marbles have a fifty percent chance of becoming red or blue upon direct observation. A cat observing a marble is a metaphor of measuring a qubit’s state, where red represents a 1 and blue represents a 0. In real life, measurements are conducted by measuring physical quantities in the lab.

Measurement is essentially asking the qubit what state it’s in, but there’s a caveat: simply the act of measurement makes the qubit settle into either the 0 or 1 states, so you only ever get the answer 0 or 1. But there’s a probability associated with each possible outcome.

Even if you happen to know everything about the probabilities beforehand--that is, even if you know the exact superposition state of the qubit before measurement--you cannot predict the outcome of a measurement.

Essentially:

> Even if you know everything about the state of a quantum system, it *can* still behave randomly.
{: .prompt-tip }

For instance, you know everything about the state of a Whiskertese marble: it's in an equally weighted (fifty-fifty) superposition. Yet, after measurement, we don't know if it will end up as a red marble or a blue one. That part is random!

Quantum physics is probabilistic, which means there is some *uncertainty*. A measurement moves the system from uncertainty to certainty.

At first glance, it may appear that the benefit of quantum superposition has vanished since you only ever get 0’s and 1’s as your outcomes, no different from classical bits. Enter quantum computing algorithms. 

An algorithm is basically a series of operations you perform to get a desired result. What a quantum computing algorithm does is manipulate the probabilities, increasing the probability associated with the desired outcome and decreasing all others. [^footnote] In this way, if the probability associated with the desired state hits 1, then that outcome is guaranteed, which means the behavior is no longer random. 

[^footnote]: Quantum operations are carried out by applying what are known as *quantum gates,* logic operations that are the building block of quantum circuits, and analogous to classical logic gates in conventional digital circuits. 

So there you have it. Now that you have an overview of qubits, quantum superposition, and measurements, you know the physics behind the marbles in Whiskerton. 

>If you’d like to dive deeper into these concepts and see how Blade’s predicament is related to what is known as Schrödinger’s cat, read on! Otherwise, head on over to the next story: [Chapter 3 - Story - Doorbells](https://quantum-kittens.github.io/posts/CHAPTER-3-Story-Doorbells/)
{: .prompt-info }
_______

## Mathematical Representation of a Qubit State

Quantum states are mathematically represented by what is known as *Dirac notation*, which makes use of something called a *ket*: $\ket{}$[^fn-nth-1].

[^fn-nth-1]: A ket denotes a mathematical object with certain properties called a *vector*. A qubit can be considered a vector. Two vectors can be combined to form another valid vector. But you don't need to know about vectors to read this text.

This is how an arbitrary qubit state is represented[^fn-nth-2]:

\begin{equation}
\label{eq:qubit}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

[^fn-nth-2]: Disclaimer: This equation is not the complete picture of a qubit; there's a degree of freedom called 'phase' that can be useful for computation but is beyond the scope of this text.

The Greek letter $\psi$, pronounced "sigh", is a symbolic representation of the state. The $\ket{}$ symbol is written, not spoken. When you refer to the qubit, you can voice, "I have a qubit in the state psi,” or write, “I have a qubit in the state  $\ket{\psi}$," after having defined $\ket{\psi}$ in an equation.

Notice that $\psi$ isn't the only thing tucked within a ket. You have $\ket{0}$ and $\ket{1}$ in the equation as well, which are the 0 and 1 states. These are called the *basis states* of the qubits; that is, the possible states a qubit can reduce to after measurement, just as a Whiskertese marble can reduce to a red or a blue.  Since a qubit has *two* basis states, a qubit is a two-level system.

The plus sign indicates a combination, or a superposition. The parameters $\alpha_{0}$ and $\alpha_{1}$ are called *amplitudes*, and let us know how likely it is the qubit will be in the state $\ket{0}$ or $\ket{1}$ after measurement, where $\alpha$ is the Greek letter, alpha. The subscript of the symbol $\alpha$ is a label to indicate to which basis state it corresponds. 

Mathematically, if we square the amplitudes, we’ll get the probabilities associated with each basis state. So, if you measure a qubit in the state $\ket{\psi}$, you will get the result 0 with a probability $\alpha_{0}^2$, or get the result 1 with a probability $\alpha_{1}^2$. [^fn-nth-3] 

[^fn-nth-3]: The superscript 2 indicates a 'square', which means the number is being multiplied by itself. That is, $\alpha_{0}^2=\alpha_{0}*\alpha_{0}$.

You may rightfully be wondering why these squares are suddenly popping into the picture. It is simply a mathematical convention that reminds us the amplitudes $\alpha_{0}$ and $\alpha_{1}$ may be negative. The squares of each of these amplitudes are probabilities, and probabilities are always positive, as are squares!

This means that each quantum state is subject to a constraint. Probability theory has a strict rule: all probabilities should add up to 1, so $\alpha_{0}^2+\alpha_{1}^2=1$ *always*. 

Let's look at a specific example. Suppose we have a qubit in the state:

\begin{equation}
\ket{\psi}=\sqrt{\frac{2}{3}}\ket{0}-\sqrt{\frac{1}{3}}\ket{1}
\end{equation}

Here, $\alpha_{0}=\sqrt{\frac{2}{3}}$, which means the probability of getting the result 0 after measurement is $\frac{2}{3}$. Similarly for $\alpha_{1}=-\sqrt{\frac{1}{3}}$, and a probability of  $\frac{1}{3}$ associated with result 1. That is, if you have a ton of qubits in this state, and you measure them all, statistically speaking, approximately one third of them would yield the outcome 1. The larger the amplitude, $\alpha$, the higher the probability, and the more likely it is to find the qubit in the associated state after measurement.[^fn-nth-4]

[^fn-nth-4]: Note for the mathematicians: we refer to $mod(\alpha)$ here.

## A Note on Statistics

The thing about qubits is that you cannot determine $\alpha_{0}$ and $\alpha_{1}$ for an arbitrary state $\ket{\psi}$ through measurements--the only way to know exactly what numbers these $\alpha$'s are is to have created the state yourself, or to know the person who created it. This is because a measurement always results in a single outcome: 0 or 1, so no measurement can lead to the knowledge of the $\alpha$'s. If someone else created the state, you can ask them for thousands of qubits in identical states and after thousands of measurements, statistically decipher what the amplitudes and thus the probabilities of the state are. [^fn-nth-5]

[^fn-nth-5]: This is precisely why quantum circuits are run multiple times: to gather statistics. Quantum circuits are quantum computation models that have gate sequences, measurements, and the like.

However, you don't necessarily need to know what the $\alpha$'s are in order for qubit states to be useful. The beauty of the qubit state lies in how one can change and manipulate $\alpha_{0}$ and $\alpha_{1}$ with quantum gates before measurement. As mentioned earlier, the goal is to boost the probabilities associated with the desired outcome. If the desired outcome is 0,  then the algorithm can be designed to boost $\alpha_{0}$, regardless of what it is. And if $\alpha_{0} = 1$, then the outcome 0 will be guaranteed.

## Physical Qubits

As stated earlier, qubit states are mathematical constructs, which make them easier to work with mathematically to develop algorithms and the like without making a statement on the physical system that is used. This is important, because it doesn't matter whether you physically construct qubit states in the lab as, say, electron spins, polarized states of photons, or something else.

Don’t know what electrons or photons are? Let’s digress briefly:

> An electron is a negatively charged subatomic particle. It has a property called 'spin' that we needn't discuss in detail. Suffice it to say that the spin of an electron can be $+\frac{1}{2}$ or $-\frac{1}{2}$, which mathematically can be represented as the states $\ket{0}$ and $\ket{1}$.
{: .prompt-info }

>A photon is the building block of electromagnetic radiation, which includes visible light. Everything that you see is due to these photons hitting your retinae. When photons are *polarized*, they vibrate in a specific direction rather than all directions. In terms of qubits, polarization in the horizontal direction, say, can be represented by $\ket{0}$ and polarization in the vertical direction, say, can be represented by $\ket{1}$. A superposition of the two is possible, and corresponds to the photon vibrating in a direction between vertical and horizontal, analogous to Southeast lying between South and East on a compass.
{: .prompt-info }

One important thing to note about qubit states is that they are not stable. Little disturbances in a qubit's environment can reduce it to either $\ket{0}$ or $\ket{1}$: disturbances like heat, vibrations, etc.[^fn-nth-6] And even *that* is unstable; after some time a qubit can jump back into a superposition. It's this little tug of war of states that makes qubits a little tricky to manipulate in the lab--and what keeps the cats of Whiskerton intrigued!

[^fn-nth-6]: This sensitivity of quantum states is one of the obstacles in fabricating stable, perfect physical qubits, and devices with a large number of qubits. But this is an exciting research area with lots of promising progress. 

## Schrödinger's Cat

This brings us to Blade in the box with the glitter machine. His predicament is a homage of sorts to a thought experiment by physicist Erwin Schrödinger in 1935[^fn-nth-7].

[^fn-nth-7]: Schrödinger, Erwin (November 1935). "Die gegenwärtige Situation in der Quantenmechanik (The present situation in quantum mechanics)". Naturwissenschaften. 23 (48): 807-812.

Qubits are two-level systems and have two basis states, but there are other quantum particles and systems that can have even more. Yet all of these systems, qubits and beyond, adhere to the same rule: upon measurement, the outcome is only one out of all the possibilities. 

No one really knows why this happens. One possible explanation is the Copenhagen interpretation of quantum mechanics, in which the act of measurement itself collapses all possibilities to a single one. In 1935, physicist Erwin Schrödinger published a paper that outlined his famous thought experiment as a push-back to this interpretation, by hypothetically extrapolating quantum effects on a microscopic level to an everyday macroscopic object: a cat.

In the original thought experiment, a radioactive substance is used instead of a qubit (or a Whiskertese marble). Radioactive substances decay according to probabilities, just like a qubit reduces to a certain state according to probabilities.

A cat is placed in a box with a radioactive substance that is linked to a vial of poison. If any one of the atoms decays, then the vial shatters, poisoning the cat. Thus, the state of the cat is coupled with that of the poison system, which is governed by the probability that at least one atom will decay. In this way, before the box is opened, the cat can be considered to be both dead or alive, because each of the possibilities is likely. That is, the cat's reality is undetermined prior to the opening of the box. 

Schrödinger argued that this is a 'ridiculous case' and that one can't really believe that before one opens the box the cat is in a superposition of dead and alive. He was right, of course. This scenario can't be considered *truly* quantum. The cat isn't a quantum particle, for one. So while the cat isn't actually in a superposition of dead and alive, the thought experiment at the very least demonstrates a probabilistic system.

This thought experiment has fast become one of the most recognized iconographies of quantum phenomenon in popular culture, and naturally had to make an appearance in Whiskerton. With glitter, of course, because there's no reason to get morbid in such a quaint little town. Note that Schrödinger didn't actually poison cats--he merely thought about it!

Now, there’s one more curious aspect to this thought experiment: you could say that the state of the cat is *entangled* with that of the radioactive substance. 

Quantum entanglement is actually our next stop! Let’s hop to it: **[Next: Chapter 3 - Story - Doorbells](https://quantum-kittens.github.io/posts/CHAPTER-3-Story-Doorbells/)**

_____________________________


_____________________________


_____________________________




## Qiskit Code

This section is for those of you who want to get started with Qiskit, IBM Quantum’s open source python framework to program quantum computers.

You can simulate a Whiskerton marble using this supplementary Qiskit code. This code walks you through creating and running a quantum circuit with a single qubit.

You can run this code in two ways:

- On the cloud: you can choose use a cloud-based tool like [Google Colab](https://colab.research.google.com/) or [qBraid](https://www.qbraid.com/). 
- Locally: you can [install Qiskit](https://qiskit.org/) and run the code on your local machine

See this blog post for further setup details: [
Explore newly recommended notebook environments for Qiskit](https://www.ibm.com/quantum/blog/qiskit-notebook-environments)

The below code is also available as a jupyter notebook [here](https://github.com/quantum-kittens/quantum-kittens.github.io/blob/main/jupyter_notebooks/QK_Chapter_2.ipynb).

November 2024 note: this code has now been updated to Qiskit 1.0. If you've used an earlier version of Qiskit before, this blog post may be useful for you: [Best practices for transitioning to Qiskit SDK v1.0](https://www.ibm.com/quantum/blog/transition-to-1)





 ```python
# Install Qiskit along with some optional dependencies useful for visualization 
# by uncommenting the instruction below if you don't have Qiskit installed already

#pip install'qiskit[visualization]'

# Install the Qiskit Runtime Service if you don't have it installed already by uncommenting the instruction below

#pip install qiskit-ibm-runtime

# Install the Qiskit Aer Simulator if you don't have it installed already by uncommenting the instruction below

#pip install qiskit-aer

# Import necessary Qiskit libraries

from qiskit import QuantumCircuit

#Create Marble Circuit

marble_circuit = QuantumCircuit(1, 1) # add one qubit (Whiskerton marble) and one classical bit (to store the measurement outcome)

marble_circuit.h(0) # add H-gate or Hadamard gate to the qubit (this is the quantum gate that puts the marble in superposition)

marble_circuit.measure(0,0) # add a measurement operator (this is equivalent to a cat looking directly at a marble)

marble_circuit.draw('mpl') # see how the circuit looks
```



 ```python

 # Import necessary Qiskit libraries for running the circuit on a simulator

from qiskit.transpiler.preset_passmanagers import generate_preset_pass_manager
from qiskit_ibm_runtime import QiskitRuntimeService
from qiskit_aer import AerSimulator
from qiskit_ibm_runtime import SamplerV2 as Sampler
from qiskit.visualization import plot_histogram


#Run Marble Circuit,
#That is, see if the marble turns red or blue

marble_state = {'1': 'red', '0': 'blue'}

aer_sim = AerSimulator() # Identify the quantum computer to run this on. In this case it's a simulator not a real device.
pm = generate_preset_pass_manager(backend=aer_sim, optimization_level=1) 
isa_marble_circuit = pm.run(marble_circuit) # This line and the line above essentially prepare the circuit to be executed on the device you selected. For for more technical details, please see: https://docs.quantum.ibm.com/api/qiskit/transpiler#transpiler

# fetch and print the outcome:
sampler = Sampler(mode=aer_sim)

result = sampler.run([isa_marble_circuit], shots=1000).result() # Run the circuit on the simulator 1000 times to gather statistics.
counts = result[0].data.c.get_counts()

ans = str(max(counts, key=counts.get))

print('The marble is ' + marble_state[ans] + '.') # The outcome is the one associated with the highest count.



```

```python

# Examine the statistics and plot histogram

print("Your result in the form of counts:", counts)
print("Thus, in 1000 shots, you get blue " + str(counts['0']) + " times, and red " + str(counts['1']) + " times.")

plot_histogram(counts)

```

```python
# If you want to run the circuit on a real device then you can use the following 

#from qiskit_ibm_runtime import QiskitRuntimeService
 
#service = QiskitRuntimeService(channel="ibm_quantum", token="<insert your token here>")
```



*Note: the Qiskit code provided is open source, and does not fall under the copyright of Quantum Kittens.*