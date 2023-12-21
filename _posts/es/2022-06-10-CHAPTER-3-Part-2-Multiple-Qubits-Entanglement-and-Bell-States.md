---
title: 'Capítulo 3 Parte 2 - Comentario - Múltiples Qubits, Entrelazamiento y Estados de Bell'
math: true
---


No hay mucho que puedas hacer con un solo bit clásico. El procesamiento de la información y los algoritmos suelen requerir más unidades de información. Por ejemplo, a nivel de máquina, una imagen en tu muro de redes sociales no está representada por un solo bit. Está representado por *muchos* bits, muchos 0s y 1s, largas cadenas de bits, y son esas cadenas de bits las que se transmiten a través de Internet y son procesadas por tus dispositivos.

De manera similar, no hay mucho que puedas hacer con un solo qubit, sin importar cuán elegante pueda parecer un qubit. De hecho, la ventaja potencial de la computación cuántica sobre la computación clásica en ciertos contextos radica en poder algún día crear procesadores con cientos y tal vez miles de qubits estables y perfectos.

Por lo tanto, la mayoría de los protocolos de computación cuántica involucran más de un qubit, de la misma manera que los timbres de las puertas de Whiskerton involucran más de una canica. Por supuesto, los timbres de Whiskerton siguen siendo sistemas cuánticos muy simples con solo dos canicas, mientras que algunos de los algoritmos diseñados para futuras computadoras cuánticas involucran mucho más. No obstante, estos timbres ilustran algo de lo que hacen uso incluso protocolos más complejos: un fenómeno cuántico que no tiene análogo en el mundo clásico, el *entrelazamiento cuántico*.

## ¿Qué es el Entrelazamiento Cuántico?

El entrelazamiento cuántico describe una conexión o relación peculiar entre sistemas cuánticos. Si dos sistemas cuánticos están entrelazados, están conectados de tal manera que sus estados no pueden describirse de forma independiente, y realizar mediciones en un sistema afectará al otro, incluso si el segundo sistema no está cerca. 

En esencia, lo siguiente es posible en el mundo cuántico:

> Incluso si dos qubits (o sistemas cuánticos) están demasiado separados para influirse entre sí, aún pueden estar correlacionados de tal manera que la manipulación de uno afecte inmediatamente al otro.
{: .prompt-tip }

Las dos canicas en un timbre Whiskerteso están entrelazadas. Recuerda que si una se vuelve roja, la segunda también lo hace, aunque las dos están en casillas separadas. Nadie necesita mirar directamente a la segunda canica para que se reduzca a un solo color.  

Este entrelazamiento no es como las correlaciones que vemos en nuestra vida cotidiana. En nuestro mundo clásico, si tienes dos canicas en una bolsa opaca, una roja y otra azul, y sacas la azul, sabrás inmediatamente que la roja todavía está en la bolsa. Esa es la correlación clásica, el tipo de correlación que experimentamos a diario. 

Sin embargo, el entrelazamiento cuántico no se comporta como las correlaciones clásicas. Hay matices que no se traducen en nuestra experiencia cotidiana. Por un lado, si las canicas fueran canicas Whiskertesas, entonces no serían de un solo color en primer lugar. La canica que sacas de la bolsa estaría superpuesta hasta que la miraras. Solo una vez que la canica en tu mano se reduzca a un solo color, la canica en la bolsa cambiará, incluso si la bolsa se la llevaran lejos de ti. [^fn-nth-1]

[^fn-nth-1]: También hay otros matices en el entrelazamiento, y dos sistemas cuánticos que están muy, muy separados también deben ser lo que se conoce como *no locales* para influirse mutuamente, pero esas son exploraciones para otro día.

Dado que estamos hablando de dos entidades que se influyen mutuamente de inmediato a pesar de la distancia entre ellas, en este punto puedes preguntarte con razón: ¿significa esto que podemos enviar información más rápido que la luz? Desafortunadamente, la respuesta es no.

El problema es que simplemente realizar cualquier antiguo tipo de medición no funcionará; sí, ¡hay diferentes *tipos* de mediciones! Los diferentes tipos de mediciones están más allá del alcance del texto actual, pero basta decir que si tú y un amigo que vive lejos comparten un par entrelazado, entonces el tipo de medición que realizas de tu parte debe transmitirse a tu amigo de alguna manera. Si tu amigo no sabe qué tipo de medición debe realizar, por su parte, ¡no podrá ‘ver’ el resultado esperado! Por lo tanto, debe tener lugar algún tipo de comunicación, digamos, a través de una llamada telefónica. Lo cual... no puede suceder más rápido que la luz.

>Si deseas profundizar un poco más en el entrelazamiento cuántico, ¡sigue leyendo! De lo contrario, dirígete a la siguiente página: [This is Not the End](https://quantum-kittens.github.io/posts/This-is-not-the-end/).
{: .prompt-info }


_______

## Representación Matemática de Estados Multi-Qubit

Los estados de varios qubits se representan de manera similar a los estados de un solo qubit. Nos centraremos en los estados de dos qubits, ya que los timbres de Whiskerton tienen dos qubits, pero la representación es válida incluso para cantidades más altas.


Recuerda la ecuación para un estado de qubit único arbitrario del [Capítulo 2](https://quantum-kittens-es.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/):

\begin{equation}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

En esta ecuación, los estados básicos son análogos a los dos valores que puede tener un bit clásico: 0 y 1. Y un qubit puede estar en una superposición de los dos estados base. 

Para entender cómo representar un estado de dos qubits, veamos todos los valores posibles de dos bits clásicos. Dos bits, combinados, pueden tener uno de cuatro valores: 00, 01, 10 o 11. Al igual que en el caso de un solo qubit, estos cuatro valores corresponden a cuatro estados base. ¡Dos qubits pueden estar en uno de estos cuatro estados o pueden estar en una superposición de estos estados! Por lo tanto, un estado arbitrario de dos qubits se puede representar mediante la siguiente ecuación:

\begin{equation}
\ket{\psi}=\alpha_{00}\ket{00}+\alpha_{01}\ket{01}+\alpha_{10}\ket{10}+\alpha_{11}\ket{11}
\end{equation}

Al igual que la ecuación para un solo qubit, $\alpha_{00}^2$ es la probabilidad de que los dos qubits produzcan el resultado 00 después de la medición. Análogamente para los otros tres estados base. Una vez más, las leyes de la probabilidad dictan que $\alpha_{00}^2+\alpha_{01}^2+\alpha_{10}^2+\alpha_{11}^2=1$. 

## Estados Entrelazados y de Bell

El simple hecho de tener dos qubits en la mano no es suficiente para considerarlos entrelazados. Los qubits deben estar en estados específicos para que se consideren entrelazados, lo que significa que hay ciertos valores $\alpha$ que implican entrelazamiento. 

Por ejemplo, para representar el estado entrelazado de un timbre Whiskerteso, $\alpha_{01}=\alpha_{10}=0$ y los otros dos, $\alpha_{00}$ y $\alpha_{11}$, deben ser igual a sus cuadrados sumando 1.

Analicemos esto. En un timbre Whiskerteso, las canicas se vuelven del mismo color después de observar directamente la canica exterior. Si las canicas solo pueden volverse del mismo color, entonces solo se permiten dos estados posibles: $\ket{rojo, rojo}$ y $\ket{azul, azul}$. La primera posición en cada $\ket{}$ representa la canica exterior y la segunda posición representa la canica interior. El estado $\ket{rojo, azul}$ es ilegal y nunca puede ocurrir dentro del timbre de la puerta, por lo que la probabilidad asociada con él es cero. Lo mismo para $\ket{azul, rojo}$.

Esto significa que las únicas probabilidades distintas de cero son las asociadas con $\ket{rojo, rojo}$ y $\ket{azul, azul}$, y dado que las canicas Whiskertesas tienen una probabilidad de 50-50 de convertirse en cualquier color, las dos probabilidades deben ser iguales.

Así que así es como se ve ese estado:


\begin{equation}
\ket{\phi^+}=\frac{1}{\sqrt{2}}\ket{00}+\frac{1}{\sqrt{2}}\ket{11}
\label{eq:bellstate}
\end{equation}

Las canicas se encuentran en lo que se conoce como un "estado de Bell”, llamado así por el físico John S. Bell, y *no* porque este es el estado de los timbres en Whiskerton. La ecuación anterior es el aspecto matemático de este estado particular de Bell, donde $\phi^+$ es una convención de nomenclatura. [^fn-nth-2]

[^fn-nth-2]: Así es como se ve matemáticamente el estado de Bell en la *base computacional*, que es una referencia al tipo de medida requerida para ‘ver’ el resultado. Hay diferentes bases asociadas con diferentes tipos de mediciones.

Como puedes ver, existe la misma probabilidad de que ocurra cualquiera de los dos estados base $\ket{00},\ket{11}$, antes de que se mida el primer qubit. Pero cuando el primer qubit se convierte en $\ket{0}$ o $\ket{1}$, el segundo no tiene más remedio que seguirlo. De esta manera, los resultados se correlacionan y los qubits se entrelazan. 

En este punto, es importante tener en cuenta que este no es el único estado de Bell; hay otros. Por ejemplo, uno de los otros estados de Bell implica que el segundo qubit siempre se convierte en el *opuesto* de lo que se convierte el primero. Pero no es así como se comportan las canicas entrelazadas de los timbres de Whiskerton.

Estos pares de dos qubits que se encuentran en los estados de Bell se denominan pares EPR, en honor a los físicos Albert Einstein, Boris Podolsky y Nathan Rosen. Los pares EPR y el entrelazamiento son un recurso valioso para las aplicaciones teóricas y potenciales de computación cuántica, como la criptografía cuántica, la codificación superdensa y la teleportación cuántica. [^fn-nth-3]

[^fn-nth-3]: La teleportación en este contexto no es la teletransportación que encuentras en Star Trek. ¡Planeamos explorar esta aplicación en una historia futura!
 
## Nota Rápida sobre Qubits Físicos Entrelazados
 
La construcción física de qubits entrelazados en el laboratorio depende de lo que uses para los qubits. Por ejemplo, dos fotones de una sola fuente, generados de una manera específica, pueden emerger entrelazados. No hay un único 'enredador' universal como lo hay en Whiskerton. Y, más exactamente, ¡nadie llama realmente a estas fuentes 'enredadores'! Bueno, aparte de los gatos.
 
_____________________________


_____________________________


_____________________________


**[Next: This is Not the End](https://quantum-kittens-es.github.io/posts/This-is-not-the-end/)**
 
________

## Qiskit Code

You can simulate a Whiskerton doorbell using the following code. By using this code, you will learn how to create the quantum circuit corresponding to the Bell state.

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

The above code is also available as a jupyter notebook [here](https://github.com/quantum-kittens/quantum-kittens.github.io/blob/main/jupyter_notebooks/QK_Chapter_3.ipynb).

As an exercise, run this circuit in a similar way to the marble circuit in [Chapter 2](https://quantum-kittens-es.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/)!

*Note: the Qiskit code provided is open source, and does not fall under the copyright of Quantum Kittens.*

