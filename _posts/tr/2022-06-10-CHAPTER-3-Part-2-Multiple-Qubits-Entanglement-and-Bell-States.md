---
title: 'Bölüm 3 Kısım 2 - Açıklama - Birden Fazla Kübit, Dolanıklık, ve Bell Durumları'
math: true
---


Tek bir klasik bit ile yapabileceğiniz çok bir şey yoktur. Bilgi işlem ve algoritmalar genellikle daha fazla bilgi birimine ihtiyaç duyar. Mesela, makine seviyesinde, sosyal medya akışınızdaki bir görsel tek bir bit ile gösterilmez. *Birçok* kübit ile gösterilir, birçok 0 ve 1'le, uzun bit dizileriyle ve bu bit dizileri internet üzerinden iletildikten sonra, cihazlarınız tarafından işlenir.

Her ne kadar havalı görünse de, benzer bir yapıda, tek bir kübit ile de yapabileceğiniz pek bir şey yoktur. Hatta, kuantum hesaplamanın belirli bağlamlarda klasik hesaplama üzerindeki potansiyel avantajı, bir gün yüzlerce hatta binlerce kararlı ve mükemmel kübite sahip işlemciler üretebilme olasılığında yatmaktadır.

Bu sebepten, çoğu kuantum hesaplama protokolü birden fazla kübit içermektedir, Bıyıkkent'in kapı zillerinin birden fazla bilye içermesindeki gibi. Bıyıkkent'in kapı zilleri yalnızca iki bilye içeren basit sistemler, oysa gelecekteki kuantum bilgisayarlar için tasarlanan bazı algoritmalar çok daha fazlasını gerektiriyor. Bununla birlikte, bu kapı zilleri çok daha karmaşık bir şeyi temsil ediyor: klasi dünyada karşılığı olmayan bir kuantum olgusu, *kuantum dolanıklığı*.

## Quantum Dolanıklığı Nedir?

Kuantum dolanıklığı, kuantum sistemleri arasındaki tuhaf bir bağlantıyı ya da ilişkiyi tanımlar. İki kuantum sistemi dolanık ise, öyle bir şekilde birbirine bağlıdırlar ki, durumlarından bağımsız olarak tanımlanamazlar ve bir sistem üzerinde ölçüm yapmak, diğeri yakında olmasa bile onu etkiler.

Esasen, kuantum dünyasında mümkün olan şeyler şunlardır:

> İki kübit (ya da kauntum sistemleri) birbirlerini etkileyemeyecek kadar bile birbirinden uzak olsalar, öyle bir şekilde korelasyonludurlar ki, birine müdahale edildiğinde hemen diğerini etkiler.
{: .prompt-tip }

Bıyıkkent kapı zilindeki iki bilye dolanıktı. Hatırlayın biri kırmızı renge döndüğünde, ikisi farklı kutularda oldukları halde diğeri de kırmızı renge dönüyordu. İkinci bilyenin tek bir renge dönüşmesi için, kimsenin ikinci bilyeyi gözlemlemesine gerek kalmıyordu.

Bu dolanıklık, günlük hayatımızda karşılaştığımız korelasyonlara tam olarak benzemiyor. Bizim klasik dünyamızda, saydam bir poşette biri kırmızı biri mavi iki bilyen varsa, mavi olanı çıkarttığında, kırmızı olanın hala poşette olup olmadığını o anda bilebilirsin. Bu klasik korelasyon, bizim günlük hayatta karşılaştığımız çeşitte bir korelasyon.

Ancak, kuantum dolanıklığı klasik korelasyon gibi davranmıyor. Günlük yaşantımıza doğrudan çevrilemeyecek bazı farklılıklara sahip. Bu farklılıklardan biri, eğer bilyeler Bıyıkkent bilyesi olsaydı, öncelikle tek bir renkte olmazlardı. Poşetten çektiğin bilye, doğrudan bakana kadar (gözlemleyene kadar) süperpozisyonda olurdu. Elindeki bilye tek bir renge indirgenir indirgenmez, poşetteki bilye de değişecektir, poşet senden çok uzağa götürülmüş olsa bile. [^fn-nth-1]

[^fn-nth-1]: Dolanıklık için daha başka farklılıklar da mevcut, birbirinden çok ama çok uzak iki kuantum sistemi birbirini etkileyebilmek için *yerel olmama (non-local)* denilen özelliğe de sahip olmalıdır, fakat bunlar başka bir günün konusudur.

Aralarındaki mesafeye rağmen birbirini anında etkileyen iki varlıktan bahsettiğimize göre, bu noktada haklı olarak şunu merak edebilirsiniz: Bu, bilgiyi ışıktan daha hızlı gönderebileceğimiz anlamına mı geliyor?Maalesef cevap hayır.

The catch is that simply performing any old type of measurement won’t work—yes, there are different *types* of measurements! The varying types of measurements are beyond the scope of the current text, but suffice it to say that if you and a friend who lives far away share an entangled pair, then the type of measurement you perform on your part of the pair must be conveyed to your friend somehow. If your friend doesn’t know which type of measurement to perform on their part, they won’t be able to ‘see’ the expected result! So some sort of communication must take place, say, through a telephone call. Which…cannot happen faster than light.

>If you’d like to dive a little deeper into quantum entanglement, read on! Otherwise, head on over to the next page: [Who Gets the Cardboard Box?](https://quantum-kittens.github.io/posts/Who-Gets-the-Cardboard-Box/).
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


**[Next: Who Gets the Cardboard Box?](https://quantum-kittens.github.io/posts/Who-Gets-the-Cardboard-Box/)**
 
________

## Qiskit Code

You can simulate a Whiskerton doorbell using the following code. By using this code, you will learn how to create the quantum circuit corresponding to the Bell state.

The below code is also available as a jupyter notebook [here](https://github.com/quantum-kittens/quantum-kittens.github.io/blob/main/jupyter_notebooks/QK_Chapter_3.ipynb).

 ```python
# Import necessary Qiskit libraries

from qiskit import QuantumCircuit, QuantumRegister, ClassicalRegister

#Create Doorbell Entangler Circuit

qubits = QuantumRegister(2, name='q') # Create a quantum register with 2 qubits (Whiskertese marbles) and name the register 'q'

classical_bits = ClassicalRegister(2, name='c') # Create a classical register with 2 bits and name the register 'c' (to eventually store the measurement outcome)

q0, q1 = qubits # Label the two qubits in the register 'q0' and 'q1'

c0, c1 = classical_bits

doorbell_circuit = QuantumCircuit(qubits, classical_bits) # Create a circuit with the quantum and classical registers.

doorbell_circuit.h(q0) # Add a Hadamard gate to the first qubit 

doorbell_circuit.cx(q0,q1) # Add a cnot gate with the first qubit as the control and the second qubit as the target. The target flips its state when the control is in the 1 state.

doorbell_circuit.measure([q0,q1],[c0,c1]) # Add measurement operators (this is equivalent to a cat looking directly at the outer marble).

doorbell_circuit.draw('mpl') # See how the circuit looks.

```


As an exercise, run this circuit in a similar way to the marble circuit in [Chapter 2](https://quantum-kittens.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/)!

*Note: the Qiskit code provided is open source, and does not fall under the copyright of Quantum Kittens.*


