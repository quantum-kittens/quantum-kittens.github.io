---
title: 'Capítulo 4 Parte 2 - Comentario - Compuertas y Circuitos Cuánticos'
math: true
---


Ya sabes que los bits son las entidades fundamentales que utilizan las computadoras clásicas para almacenar y procesar información, y que los bits solo pueden tomar un valor: 0 o 1. Pero, ¿cómo *saben* los bits qué valores asumir?

Les indicas a los bits qué hacer proporcionándoles instrucciones. Cuando usas una computadora, básicamente estás emitiendo comandos que llegan en cascada a los componentes computacionales fundamentales que controlan los bits y determinan si están en 0 o 1 en un instante dado.

Supongamos que envías un mensaje de texto, "¡Feliz cumpleaños!", a un amigo. Abres tu aplicación de mensajería, escribes cada letra y pulsas enviar. Cada paso implica dar instrucciones a tu dispositivo. Estas son instrucciones de alto nivel que entiendes, como 'escribir h' o 'pulsar Entrar'. Pero tu dispositivo computacional descompone cada una de estas instrucciones en comandos a nivel de máquina, y en el nivel más básico, estas instrucciones controlan y manipulan cadenas de bits.

Estas instrucciones se ejecutan mediante *compuertas lógicas*, que realizan operaciones sobre bits. Diferentes compuertas pueden actuar sobre uno o varios bits a la vez, cada una realizando una operación específica. Combinadas, producen el resultado deseado.

De manera similar, en la computación cuántica, existen *compuertas cuánticas* que actúan sobre los qubits.


## Compuertas Cuánticas

Las compuertas cuánticas son la forma en que controlamos los qubits: manipulan sus estados cuánticos. Esto implica cambiar las probabilidades de lo que obtendrías si midieras los qubits.

En la analogía de la canica Whiskertesa, una compuerta cuántica cambia la probabilidad de ver rojo o azul cuando observas la canica directamente.

## Circuitos Cuánticos

Las instrucciones se pueden escribir usando *circuitos cuánticos*. Un circuito cuántico es un modelo que representa una secuencia de compuertas cuánticas, mediciones y otras acciones sobre los qubits. Si bien no es un circuito físico real, representa cómo se manipularán los qubits.

He aquí un ejemplo de cómo se ve un circuito cuántico para tres qubits:

![](/assets/imgs/ch4_3_qubit_circuit.png){: style="max-width: 500px"}

Parece una partitura musical, ¿verdad? Al igual que una partitura musical, el circuito se lee de izquierda a derecha. Cada línea horizontal representa un qubit. Los recuadros y símbolos en esas líneas son compuertas cuánticas, y el recuadro gris al final de cada línea representa una medición. Observa cómo algunas compuertas cuánticas abarcan varias líneas; estas compuertas actúan sobre varios qubits a la vez.

Recuerda, este circuito cuántico es solo una representación visual de instrucciones. Considéralo una abstracción de lo que ocurrirá en el hardware físico; no un diagrama de circuitos electrónicos reales. Estas instrucciones conforman un *algoritmo cuántico*.

En Whiskerton, los gatos implementan secuencias de compuertas cuánticas mediante la música, manipulando el estado de sus canicas. Saben que ciertas notas musicales generan cambios de estado específicos en las canicas.


> Si quieres profundizar en las compuertas y circuitos cuánticos desde una perspectiva matemática, ¡sigue leyendo! Si no, ve a la página siguiente: [This is Not the End.](https://quantum-kittens.github.io/posts/This-is-not-the-end/)
{: .prompt-info }

_______

## Representación Matemática de las Compuertas Cuánticas

En el capítulo 2, aprendiste que podemos representar un estado de qubit arbitrario usando esta ecuación:

\begin{equation}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

donde $\alpha_{0}$ y $\alpha_{1}$ son amplitudes de probabilidad. Estas amplitudes de probabilidad nos indican todo sobre el estado. Cuando una compuerta cuántica cambia el estado, cambia estos valores de $\alpha$ (se pronuncia 'alfa').

Llamemos a nuestra compuerta cuántica $G$. Al aplicar $G$ a nuestro estado inicial $\ket{\psi}$, el estado cambia de este modo:

\begin{equation} 
\alpha_{0}\ket{0}+\alpha_{1}\ket{1} \rightarrow \beta_{0}\ket{0}+\beta_{1}\ket{1}
\end{equation}

Los nuevos valores $\beta$ (pronunciados 'beta') son las amplitudes de probabilidad de nuestro estado final.

Existe otra forma útil de representar estados y compuertas cuánticas si conoces un poco de álgebra lineal. Podemos escribir las amplitudes de probabilidad como una columna de números o un *vector columna*, como se muestra a continuación:


\begin{equation} 
v_\psi = \begin{bmatrix} 
\alpha_0 \\\ 
\alpha_1 
\end{bmatrix} 
\end{equation}

Este vector se denomina *vector de estado*. De forma similar, podemos escribir cualquier compuerta cuántica de un solo qubit como una pequeña cuadrícula de números (una matriz de $2 \times 2$):

\begin{equation} 
G = \begin{bmatrix} 
a & b \\\ 
c & d 
\end{bmatrix} 
\end{equation}

Luego puedes utilizar la multiplicación de matrices estándar para determinar el estado resultante:
\begin{equation} 
\begin{bmatrix} 
a & b \\\ 
c & d 
\end{bmatrix}  \begin{bmatrix} 
\alpha_0 \\\ 
\alpha_1 
\end{bmatrix}  =  \begin{bmatrix} 
\beta_0 \\\ 
\beta_1 
\end{bmatrix} 
\end{equation}

¡Veamos dos ejemplos específicos de compuertas de uso común!

### Compuerta NOT
La compuerta NOT cuántica es similar a su prima clásica. En la computación clásica, una compuerta NOT cambia un bit de 0 a 1 o de 1 a 0. La versión cuántica hace algo similar: intercambia las amplitudes de probabilidad de $\ket{0}$ y $\ket{1}$. Esto significa que si tu qubit tenía más probabilidades de darte 0 al medirlo, después de la compuerta NOT es más probable que te dé 1, y viceversa.


Esto es lo que hace la compuerta NOT:
\begin{equation} 
\ket{0} \rightarrow \ket{1}
\end{equation}
\begin{equation} 
\ket{1} \rightarrow \ket{0}
\end{equation}
\begin{equation} 
\alpha_{0}\ket{0}+\alpha_{1}\ket{1} \rightarrow \alpha_{1}\ket{0}+\alpha_{0}\ket{1}
\end{equation}

Podemos escribir la compuerta NOT como esta matriz (también llamada compuerta X o compuerta Pauli X):
\begin{equation} 
X = \begin{bmatrix} 
0 & 1 \\\ 
1 & 0 
\end{bmatrix} 
\end{equation}

Intenta multiplicar esta matriz por tí mismo con estos tres estados diferentes para ver cómo funciona:
\begin{equation} 
 \begin{bmatrix} 
0 \\\ 
1 
\end{bmatrix} , \begin{bmatrix} 
1 \\\ 
0 
\end{bmatrix} , \begin{bmatrix} 
\alpha_0 \\\ 
\alpha_1 
\end{bmatrix} 
\end{equation}

### Compuerta Hadamard
No todas las compuertas cuánticas tienen análogos clásicos como la compuerta NOT; de hecho, la mayoría no los tienen. La compuerta Hadamard es una de estas compuertas exclusivamente cuánticas, y posiblemente una de las más importantes en computación cuántica. Muchos algoritmos cuánticos se basan en ella para inicializar los estados de los qubits. ¿Qué la hace tan especial? Al aplicarla a $\ket{0}$ o $\ket{1}$, crea una superposición con el mismo peso.

¿Te suena familiar? ¡Es como las canicas de Whiskerton, que por defecto tienen una superposición de rojo y azul con el mismo peso!

Esto es lo que hace la compuerta Hadamard:

\begin{equation} 
\ket{0} \rightarrow \frac{1}{\sqrt{2}}\ket{0}+\frac{1}{\sqrt{2}}\ket{1}
\end{equation} 
\begin{equation} 
\ket{1} \rightarrow \frac{1}{\sqrt{2}}\ket{0}-\frac{1}{\sqrt{2}}\ket{1}
\end{equation} 
\begin{equation} 
\frac{1}{\sqrt{2}}\ket{0}+\frac{1}{\sqrt{2}}\ket{1} \rightarrow \ket{0}
\end{equation} 
\begin{equation} 
\frac{1}{\sqrt{2}}\ket{0}-\frac{1}{\sqrt{2}}\ket{1} \rightarrow  \ket{1}
\end{equation} 

Esos valores de $\frac{1}{\sqrt{2}}$ significan que hay una probabilidad del 50-50 de medir ya sea 0 o 1. Observa que a veces hay un signo menos. Si bien esto no altera las probabilidades, crea algo llamado *fase*, que exploraremos en un capítulo posterior. Es como darle a nuestras canicas un tipo de giro especial.

Aquí está la compuerta Hadamard como una matriz:
\begin{equation} 
H = \frac{1}{\sqrt{2}}\begin{bmatrix} 
1 & 1 \\\ 
1 & -1 
\end{bmatrix} 
\end{equation}

Intenta resolver tú mismo la multiplicación de matrices para ver cómo se crean estas transformaciones.

Una nota importante: los estados de superposición de un solo qubit igualmente ponderados son tan significativos en la computación cuántica que reciben sus propios símbolos especiales:

\begin{align}
\ket{+}=\frac{1}{\sqrt{2}}\ket{0}+\frac{1}{\sqrt{2}}\ket{1}\\\
\ket{-}=\frac{1}{\sqrt{2}}\ket{0}-\frac{1}{\sqrt{2}}\ket{1}\\\
\end{align}


## Representación Geométrica de los Qubits
Si prefieres una representación matemática más visual, quizás sea útil una representación geométrica de un estado de qubit. Un estado arbitrario $\psi$ puede escribirse en términos de senos y cosenos, de modo que las amplitudes de probabilidad sean $\alpha_{0} =\cos{\theta}$ y $\alpha_{1} =\sin{\theta}$:
\begin{equation}
\ket{\psi}=\cos{\theta}\ket{0}+\sin{\theta}\ket{1}
\end{equation}
Esta es una representación válida: recuerda que la suma de probabilidades siempre debe resultar en 1[^fn-nth-1].
\begin{equation}
\alpha_{0}^2+\alpha_{1}^2=\cos^2{\theta}+\sin^2{\theta}=1
\end{equation}

[^fn-nth-1]: Esta es una identidad trigonométrica fundamental.

Como resultado, el estado arbitrario $\ket{\psi}$ se puede representar visualmente en un círculo unitario (es decir, un círculo de radio 1) de la siguiente manera:


![](/assets/imgs/ch4_2D_geo_rep_psi.png){: style="max-width: 500px"}

El vector verde es el estado arbitrario y los dos ejes corresponden a los estados base $\ket{0}$ y $\ket{1}$.

Si el ángulo $\theta$ es de 45 grados, obtienes el estado $\ket{+}$:

![](/assets/imgs/ch4_2D_geo_rep_plus.png){: style="max-width: 500px"}


Con esta representación, puedes pensar fácilmente en una compuerta cuántica como si actuara sobre un estado de qubit, de modo que el vector correspondiente se mueve alrededor de este círculo según los cambios en $\theta$.

Es importante tener en cuenta que esta *no* es una representación completa de un cúbit, ya que no considera el parámetro adicional que llamé 'fase' anteriormente. Al abordar la fase, encontrarás una representación más completa en tres dimensiones, llamada *esfera de Bloch*.


## Ejecución de Circuitos Cuánticos
Ahora comprendes que las compuertas cuánticas manipulan las probabilidades dentro de un estado cuántico. Así, una secuencia de compuertas cuánticas en un circuito cuántico o un *algoritmo cuántico* manipula las probabilidades de estado. O, para decirlo de otra manera, los algoritmos cuánticos manipulan las probabilidades asociadas a cada resultado posible.

Naturalmente te preguntarás: si existen probabilidades asociadas a los resultados, ¿no existe la posibilidad de obtener un resultado incorrecto o indeseable? ¡Y tendrías razón!

Por eso, a diferencia de los circuitos clásicos, ejecutamos circuitos cuánticos varias veces y recopilamos los resultados como estadísticas. Cada vez que se ejecuta un circuito se llama *shot* y cuantas más iteraciones se ejecuten, más precisos serán los resultados.

Echemos un vistazo a un circuito con un solo qubit que, después de la aplicación de ciertas compuertas, tiene un 4% de posibilidades de obtener 0 y un 96% de posibilidades de obtener 1 tras la medición. 

![](/assets/imgs/ch4_Luna_circuit.png){: style="max-width: 500px"}


Esto hace uso de la compuerta X que se muestra arriba y otra compuerta llamada Rotación X ($R_X$) con un ángulo de: $\frac{\pi}{8}$ [^fn-nth-2] 

[^fn-nth-2]: Esta compuerta $R_X$ rota el estado del qubit alrededor del eje x en un ángulo de $\frac{\pi}{8}$. También introduce una fase. Veremos una representación visual de esta rotación más adelante.

Dada la probabilidad que tenemos de obtener el resultado 1, si asociamos el azul con 0 y el rojo con 1, tenemos una de las posibles representaciones del circuito cuántico de Luna tocando Feliz Cumpleaños; recuerda que ella manipuló la canica para que fuera más probable que se volviera roja después de la observación.



> Breve aclaración sobre la historia del Capítulo 4: Si te preguntas sobre la regla de la distancia de 10 cm, esta es simplemente un recurso narrativo ficticio que representa las mediciones cuánticas. En realidad, las mediciones cuánticas se producen mediante interacciones físicas que hacen que los estados cuánticos se asienten en uno de sus estados base definidos. Consulta el [Capítulo 2](https://quantum-kittens-es.github.io/posts/CHAPTER-2-Story-Schr%C3%B6dinger-Day/) para una descripción de las mediciones cuánticas.
{: .prompt-info }


_____________________________


_____________________________


_____________________________


**[Next: This is Not the End](https://quantum-kittens.github.io/posts/This-is-not-the-end/)**


## Código Qiskit

Si no estabas familiarizado con las compuertas y circuitos cuánticos antes de este capítulo, y te gustaría intentar codificarlos con Qiskit, regresa a las secciones de Qiskit en el [Capítulo 2 Parte 2](https://quantum-kittens-es.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/) y en el [Capítulo 3 Parte 2](https://quantum-kittens-es.github.io/posts/CHAPTER-3-Part-2-Multiple-Qubits-Entanglement-and-Bell-States/) para probar tus habilidades codificando circuitos. 

Por otra parte, ¡intenta codificar el circuito de Feliz Cumpleaños de Luna como ejercicio!