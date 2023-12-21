---
title: 'Capítulo 2 Parte 2 - Comentario - Qubits, Superposición y Medición'
math: true
---



Es muy probable que sepas qué es la computación clásica; es lo que la mayoría de la gente quiere decir cuando dice “computación”. Esta es la computación realizada por dispositivos electrónicos cotidianos, como el dispositivo que estás utilizando para leer esto, e incluso la computación realizada por supercomputadoras escondidas en los laboratorios.

En el nivel fundamental de una computadora clásica, la información es transportada por *bits*: unidades individuales de información que pueden tener solo uno de dos valores o *estados*: 0 o 1. De la misma manera, las computadoras cuánticas tienen una unidad computacional fundamental, llamada bits cuánticos o *qubits*. Aquí hay un hecho divertido: ¡las canicas de Whiskerton en realidad representan qubits!

## ¿Qué es un Qubit?

Un qubit es el sistema más simple de la computación cuántica, el bloque de construcción fundamental para la computación cuántica. Físicamente, los qubits pueden tomar varias formas diferentes, según el hardware que utilice una computadora cuántica. Pero, conductualmente, actúan de la misma manera. Entonces, puedes considerar que un ‘'qubit’ es un objeto matemático abstracto que se comporta de una manera curiosa diferente de un bit clásico. Los bits clásicos pueden tomar uno de dos valores, 0 y 1, pero un qubit puede hacer eso y más:

> Los qubits son objetos matemáticos abstractos que tienen la capacidad no solo de estar en los estados 0 o 1, sino en una *superposición* de los dos.
{: .prompt-tip }


## Superposición Cuántica

La superposición cuántica es un fenómeno puramente de la física cuántica que realmente no tiene un análogo en la física clásica. Puedes pensar en ello como una combinación. 

Donde los bits clásicos solo pueden estar en el estado 0 o 1 y nunca una combinación de los dos, los estados cuánticos pueden combinarse y seguir siendo estados válidos. Entonces, el estado de un qubit puede ser una combinación de 0 *y* 1.

![](/assets/imgs/Marble_Animation.png){: style="max-width: 150px" .left} En Whiskerton, las canicas están por defecto en tal estado de superposición: una combinación de igual peso de los colores rojo y azul. Sería incorrecto pensar en estos colores como colores de pintura. En tu experiencia cotidiana clásica, si combinas pintura roja y azul, obtendrás pintura morada. Pero las canicas Whiskertesas no son en realidad moradas; después de que un gato observa directamente una canica, el color puede volverse rojo o azul, con un cincuenta por ciento de probabilidad para cada uno. ¡Definitivamente, no puedes recuperar los colores rojo o azul si tienes pintura morada!

Poder hacer uso de este maravilloso fenómeno es una de las diferencias entre la computación cuántica y la computación clásica. En una computadora clásica, si realizas una operación en un bit, esencialmente estás realizando esa operación ya sea en un 0 o un 1, uno a la vez. Si necesitas realizar una operación en ambos, deberás hacerlo en dos iteraciones, consecutivamente. 

Pero aprovechando la superposición, una computadora cuántica podría realizar esa operación tanto en el 0 como en el 1 al mismo tiempo. Si escalamos esto a muchos qubits, puedes imaginarte cómo esto puede potencialmente resultar en aceleraciones o un aumento en la capacidad de la memoria u otras mejoras.

## Mediciones

Has visto que las canicas tienen un cincuenta por ciento de posibilidades de volverse rojas o azules al observarlas directamente. Un gato que observa una canica es una metáfora de la medición del estado de un qubit, donde el rojo representa un 1 y el azul representa un 0. En la vida real, las mediciones se realizan midiendo cantidades físicas en el laboratorio.

La medición es esencialmente preguntarle al qubit en qué estado se encuentra, pero hay una advertencia: simplemente el acto de medir hace que el qubit se asiente en los estados 0 o 1, por lo que solo obtienes la respuesta 0 o 1. Pero hay una probabilidad asociada con cada resultado posible.

Incluso si sabes todo sobre las probabilidades de antemano, es decir, incluso si conoces el estado de superposición exacto del qubit antes de la medición, no puedes predecir el resultado de una medición.

Esencialmente:

> Incluso si sabes todo sobre el estado de un sistema cuántico, *puede* seguir comportándose aleatoriamente.
{: .prompt-tip }

Por ejemplo, sabes todo sobre el estado de una canica Whiskertesa: está en una superposición de igual peso (cincuenta y cincuenta). Sin embargo, después de la medición, no sabemos si terminará como una canica roja o azul. ¡Esa parte es aleatoria!

La física cuántica es probabilística, lo que significa que hay algo de *incertidumbre*. Una medición mueve el sistema de la incertidumbre a la certeza.

A primera vista, puede parecer que el beneficio de la superposición cuántica se ha desvanecido ya que solo obtienes 0s y 1s como resultados, no diferentes de los bits clásicos. Entremos a los algoritmos de la computación cuántica. 

Un algoritmo es básicamente una serie de operaciones que realizas para obtener un resultado deseado. Lo que hace un algoritmo de computación cuántica es manipular las probabilidades, aumentando la probabilidad asociada con el resultado deseado y disminuyendo todas las demás. [^footnote] De esta manera, si la probabilidad asociada con el estado deseado llega a 1, entonces ese resultado está garantizado, lo que significa que el comportamiento ya no es aleatorio. 

[^footnote]: Las operaciones cuánticas se llevan a cabo aplicando lo que se conoce como *compuertas cuánticas*, operaciones lógicas que son la base de los circuitos cuánticos y análogas a las compuertas lógicas clásicas en los circuitos digitales convencionales. 

Así que ahí lo tienes. Ahora que tienes una descripción general de los qubits, la superposición cuántica y las mediciones, conoces la física detrás de las canicas en Whiskerton. 

>Si deseas profundizar en estos conceptos y ver cómo el predicamento de Blade se relaciona con lo que se conoce como el gato de Schrödinger, ¡sigue leyendo! De lo contrario, dirígete a la siguiente historia:
[Capítulo 3 - Historia - Timbres](https://quantum-kittens-es.github.io/posts/CHAPTER-3-Story-Doorbells/)
{: .prompt-info }

_______

## Representación Matemática de un Estado de Qubit

Los estados cuánticos se representan matemáticamente mediante lo que se conoce como *notación de Dirac*, que hace uso de algo llamado *ket*: $\ket{}$[^fn-nth-1].

[^fn-nth-1]: Un ket denota un objeto matemático con ciertas propiedades llamado *vector*. Un qubit puede considerarse un vector. Se pueden combinar dos vectores para formar otro vector válido. Pero no necesitas saber sobre vectores para leer este texto.

Así es como se representa un estado de qubit arbitrario[^fn-nth-2]:

\begin{equation}
\label{eq:qubit}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

[^fn-nth-2]: Descargo de responsabilidad: Esta ecuación no es la imagen completa de un qubit; hay un grado de libertad llamado 'fase' que puede ser útil para los cálculos, pero está más allá del alcance de este texto.

La letra griega $\psi$, pronunciada "psi", es una representación simbólica del estado. El símbolo $\ket{}$ se escribe, no se pronuncia. Cuando te refieres al qubit, puedes expresar "Tengo un qubit en el estado psi” o escribir “Tengo un qubit en el estado $\ket{\psi}$", después de haber definido $\ket{\psi}$ en una ecuación.

Ten en cuenta que $\psi$ no es lo único que hay dentro de un ket. También tienes $\ket{0}$ y $\ket{1}$ en la ecuación, que son los estados 0 y 1. Estos se llaman los *estados base* de los qubits; es decir, los posibles estados a los que un qubit puede reducirse después de la medición, al igual que una canica Whiskertesa puede reducirse a rojo o azul. Dado que un qubit tiene *dos* estados base, un qubit es un sistema de dos niveles.

El signo más indica una combinación o una superposición. Los parámetros $\alpha_{0}$ y $\alpha_{1}$ se denominan *amplitudes* y nos permiten saber la probabilidad de que el qubit se encuentre en el estado $\ket{0}$ o $\ket{1}$ después de la medición, donde $\alpha$ es la letra griega alfa. El subíndice del símbolo $\alpha$ es una etiqueta para indicar a qué estado base corresponde. 

Matemáticamente, si elevamos al cuadrado las amplitudes, obtendremos las probabilidades asociadas con cada estado base. Entonces, si mides un qubit en el estado $\ket{\psi}$, obtendrás el resultado 0 con una probabilidad $\alpha_{0}^2$, u obtendrás el resultado 1 con una probabilidad $\alpha_{1}^2$. [^fn-nth-3]

[^fn-nth-3]: El superíndice 2 indica un 'cuadrado', lo que significa que el número se multiplica por sí mismo. Es decir, $\alpha_{0}^2=\alpha_{0}*\alpha_{0}$.

Es posible que te preguntes con razón por qué estos cuadrados aparecen repentinamente en la imagen. Es simplemente una convención matemática que nos recuerda que las amplitudes $\alpha_{0}$ y $\alpha_{1}$ pueden ser negativas. Los cuadrados de cada una de estas amplitudes son probabilidades, y las probabilidades son siempre positivas, ¡al igual que los cuadrados!

Esto significa que cada estado cuántico está sujeto a una restricción. La teoría de la probabilidad tiene una regla estricta: todas las probabilidades deben sumar 1, así que $\alpha_{0}^2+\alpha_{1}^2=1$ *siempre*. 

Veamos un ejemplo específico. Supongamos que tenemos un qubit en el estado:

\begin{equation}
\ket{\psi}=\sqrt{\frac{2}{3}}\ket{0}-\sqrt{\frac{1}{3}}\ket{1}
\end{equation}

Aquí, $\alpha_{0}=\sqrt{\frac{2}{3}}$, lo que significa que la probabilidad de obtener el resultado 0 después de la medición es $\frac{2}{3}$. De manera similar para $\alpha_{1}=-\sqrt{\frac{1}{3}}$, y una probabilidad de $\frac{1}{3}$ asociada con el resultado 1. Es decir, si tienes un tonelada de qubits en este estado, y los mides todos, estadísticamente hablando, aproximadamente un tercio de ellos produciría el resultado 1. Cuanto mayor sea la amplitud, $\alpha$, mayor será la probabilidad y más posible es encontrar el qubit en el estado asociado después de la medición.[^fn-nth-4]

[^fn-nth-4]: Nota para los matemáticos: aquí nos referimos a $mod(\alpha)$.

## Una Nota sobre la Estadística

Lo que pasa con los qubits es que no puedes determinar $\alpha_{0}$ y $\alpha_{1}$ para un estado arbitrario $\ket{\psi}$ a través de mediciones; la única forma de saber exactamente qué números son estas $\alpha$s es haber creado el estado tu mismo, o conocer a la persona que lo creó. Esto se debe a que una medición siempre da como resultado una sola salida: 0 o 1, por lo que ninguna medición puede conducir al conocimiento de las $\alpha$s. Si alguien más creó el estado, puedes pedirle miles de qubits en estados idénticos y después de miles de mediciones, descifrar estadísticamente cuáles son las amplitudes y, por lo tanto, las probabilidades del estado. [^fn-nth-5]

[^fn-nth-5]: Esta es precisamente la razón por la que los circuitos cuánticos se ejecutan varias veces: para recopilar estadísticas. Los circuitos cuánticos son modelos de computación cuántica que tienen secuencias de compuertas, mediciones y similares.

Sin embargo, no necesariamente necesitas saber cuáles son las $\alpha$s para que los estados de qubit sean útiles. La belleza del estado de qubit radica en cómo se puede cambiar y manipular $\alpha_{0}$ y $\alpha_{1}$ con compuertas cuánticas antes de la medición. Como se mencionó anteriormente, el objetivo es aumentar las probabilidades asociadas con el resultado deseado. Si el resultado deseado es 0, entonces se puede diseñar el algoritmo para aumentar $\alpha_{0}$, independientemente de lo que sea. Y si $\alpha_{0} = 1$, entonces se garantizará el resultado 0.

## Qubits Físicos

Como se indicó anteriormente, los estados de qubit son construcciones matemáticas, lo que hace que sea más fácil trabajar con ellos matemáticamente para desarrollar algoritmos y similares sin hacer una declaración sobre el sistema físico que se utiliza. Esto es importante, porque no importa si construyes físicamente estados de qubit en el laboratorio como, por ejemplo, espines de electrones, estados polarizados de fotones o cualquier otra cosa.

¿No sabes qué son los electrones o los fotones? Hagamos una breve digresión:

> Un electrón es una partícula subatómica cargada negativamente. Tiene una propiedad llamada 'espín' que no necesitamos discutir en detalle. Basta decir que el espín de un electrón puede ser $+\frac{1}{2}$ o $-\frac{1}{2}$, que matemáticamente se puede representar como los estados $\ket{0}$ y $\ket{1}$.
{: .prompt-info }

>Un fotón es el componente básico de la radiación electromagnética, que incluye la luz visible. Todo lo que ves se debe a estos fotones que golpean tus retinas. Cuando los fotones están *polarizados*, vibran en una dirección específica en lugar de en todas las direcciones. En términos de qubits, la polarización en dirección horizontal, por ejemplo, se puede representar con $\ket{0}$ y la polarización en dirección vertical, por ejemplo, se puede representar con $\ket{1}$. Es posible una superposición de los dos, y corresponde al fotón que vibra en una dirección entre vertical y horizontal, de forma análoga al sureste que se encuentra entre el sur y el este en una brújula.
{: .prompt-info }

Una cosa importante a tener en cuenta sobre los estados de qubit es que no son estables. Pequeñas perturbaciones en el entorno de un qubit pueden reducirlo a $\ket{0}$ o $\ket{1}$: perturbaciones como calor, vibraciones, etc.[^fn-nth-6] E incluso *eso* es inestable; después de un tiempo, un qubit puede volver a saltar a una superposición. Es este pequeño tira y afloja de los estados lo que hace que los qubits sean un poco difíciles de manipular en el laboratorio, ¡y lo que mantiene intrigados a los gatos de Whiskerton!

[^fn-nth-6]: Esta sensibilidad de los estados cuánticos es uno de los obstáculos para fabricar qubits físicos estables y perfectos, y dispositivos con una gran cantidad de qubits. Pero esta es un área de investigación emocionante con muchos avances prometedores.

## El Gato de Schrödinger

Esto nos lleva a Blade en la caja con la máquina de brillantina. Su predicamento es una especie de homenaje a un experimento mental del físico Erwin Schrödinger en 1935[^fn-nth-7].

[^fn-nth-7]: Schrödinger, Erwin (November 1935). "Die gegenwärtige Situation in der Quantenmechanik (La situación actual de la mecánica cuántica)". Naturwissenschaften. 23 (48): 807-812. 

Los qubits son sistemas de dos niveles y tienen dos estados base, pero hay otras partículas y sistemas cuánticos que pueden tener aún más. Sin embargo, todos estos sistemas, qubits y más, se adhieren a la misma regla: al medir, el resultado es solo una de todas las posibilidades.

Nadie sabe realmente por qué sucede esto. Una posible explicación es la interpretación de Copenhague de la mecánica cuántica, en la que el acto mismo de medir reduce todas las posibilidades a una sola. En 1935, el físico Erwin Schrödinger publicó un artículo que describía su famoso experimento mental como un retroceso a esta interpretación, extrapolando hipotéticamente los efectos cuánticos a nivel microscópico a un objeto macroscópico cotidiano: un gato.

En el experimento mental original, se usa una sustancia radiactiva en lugar de un qubit (o una canica Whiskertesa). Las sustancias radiactivas se descomponen según las probabilidades, al igual que un qubit se reduce a un determinado estado según las probabilidades.

Un gato se coloca en una caja con una sustancia radiactiva que está vinculada a un frasco de veneno. Si alguno de los átomos se desintegra, el frasco se rompe y envenena al gato. Así, el estado del gato está acoplado con el del sistema del veneno, que se rige por la probabilidad de que al menos un átomo se desintegre. De esta forma, antes de abrir la caja, se puede considerar que el gato está vivo o muerto, porque cada una de las posibilidades es probable. Es decir, la realidad del gato es indeterminada antes de la apertura de la caja. 

Schrödinger argumentó que este es un 'caso ridículo' y que uno realmente no puede creer que antes de abrir la caja el gato está en una superposición de vivo y muerto. Él tenia razón, por supuesto. Este escenario no puede considerarse *verdaderamente* cuántico. El gato no es una partícula cuántica, por ejemplo. Entonces, si bien el gato no está realmente en una superposición de vivo y muerto, el experimento mental al menos demuestra un sistema probabilístico.

Este experimento mental se ha convertido rápidamente en una de las iconografías más reconocidas del fenómeno cuántico en la cultura popular y, naturalmente, tenía que aparecer en Whiskerton. Con brillantina, por supuesto, porque no hay motivo para ponerse morboso en un pueblito tan pintoresco. Ten en cuenta que Schrödinger en realidad no envenenó gatos, ¡simplemente pensó en ello!

Ahora, hay otro aspecto curioso de este experimento mental: se podría decir que el estado del gato está *entrelazado* con el de la sustancia radiactiva. 

¡El entrelazamiento cuántico es en realidad nuestra próxima parada! Saltemos a ello: [Siguiente: Capítulo 3 - Historia - Timbres](https://quantum-kittens-es.github.io/posts/CHAPTER-3-Story-Doorbells/)

_____________________________


_____________________________


_____________________________




## Qiskit Code

This section is for those of you who want to get started with Qiskit, IBM Quantum’s open source python framework to program quantum computers.

You can simulate a Whiskerton marble using this supplementary Qiskit code. This code walks you through creating and running a quantum circuit with a single qubit.

You can run this code in two ways:

- On the cloud: copy and paste the code into a jupyter notebook in the [IBM Quantum Lab](https://quantum-computing.ibm.com/lab) 
- Locally: you can [install Qiskit](https://qiskit.org/) and run the code on your local machine 




 ```python
# Import necessary Qiskit libraries
from qiskit import QuantumCircuit, transpile
from qiskit.visualization import *
from qiskit import BasicAer

#Load your IBM Quantum account(s)
#provider = IBMQ.load_account()

#Create Marble Circuit

marble_circuit = QuantumCircuit(1, 1) # Add one qubit (Whiskerton marble) and one classical bit (to store the measurement outcome)

marble_circuit.h(0) # Add H-gate or Hadamard gate to the qubit (this is the quantum gate that puts the marble in superposition)

marble_circuit.measure(0,0) # Add a measurement operator (this is equivalent to a cat looking directly at a marble)

marble_circuit.draw('mpl') # See what the circuit looks like
```



 ```python

#Run Marble Circuit,
#That is, see if the marble turns red or blue

marble_state = {'1': 'red', '0': 'blue'}

simulator = BasicAer.get_backend("qasm_simulator") # Identify the quantum computer to run this on. In this case it's a simulator not a real device.

compiled_circuit = transpile(marble_circuit, simulator) # Compile the circuit down to low-level QASM instructions.

job = simulator.run(compiled_circuit, shots=1000) # Run the circuit on the simulator 1000 times to gather statistics.

# Fetch and print the outcome:

result = job.result() 
counts = result.get_counts(compiled_circuit)

ans = str(max(counts, key=counts.get))

print('The marble is ' + marble_state[ans] +'.') # The outcome is the one associated with the highest count.


```

 ```python

# Examine the statistics and plot histogram

print("Your result in the form of counts:", counts)
print("Thus, in 1000 shots, you get blue " + str(counts['0']) + " times, and red " + str(counts['1']) + " times.")

plot_histogram(counts)

```

The above code is also available as a jupyter notebook [here](https://github.com/quantum-kittens/quantum-kittens.github.io/blob/main/jupyter_notebooks/QK_Chapter_2.ipynb).

*Note: the Qiskit code provided is open source, and does not fall under the copyright of Quantum Kittens.*