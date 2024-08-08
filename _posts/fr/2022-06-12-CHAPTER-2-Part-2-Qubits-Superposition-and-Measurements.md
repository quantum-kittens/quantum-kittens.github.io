---
title: 'Chapitre 2 Partie 2 - Commentaire - Qubits, Superposition, et Mesures'
math: true
---


Vous savez très probablement ce qu'est l'informatique classique ; c'est ce que la plupart des gens entendent par "informatique". C'est le type de calcul effectué par les appareils électroniques quotidiens comme celui que vous utilisez pour lire ceci, et même les calculs effectués par les superordinateurs cachés dans les laboratoires.

___Deep down at the fundamental level of a classical computer, information is carried by *bits*: single units of information that can have only one of two values or *states*: 0 or 1.  In much the same way, quantum computers have a fundamental computing unit, called quantum bits or *qubits*. Here’s a fun fact: the marbles of Whiskerton actually represent qubits!___

Au niveau fondamental d'un ordinateur classique, l'information est transportée par des *bits* : des unités d'information uniques qui ne peuvent avoir que l'une des deux valeurs ou *états* : 0 ou 1. De la même manière, les ordinateurs quantiques ont une unité de calcul fondamentale, appelée bits quantiques ou *qubits*. Voici un fait amusant : les billes de Whiskerton représentent en réalité des qubits !

## What is a Qubit?

## Qu'est ce qu'un Qubit ?

___A qubit is the simplest system in quantum computing, the fundamental building block for quantum computation. Physically, qubits can take a number of different forms, depending on the hardware a quantum computer uses. But, behaviorally, they act the same way. So you can consider a ‘qubit’ to be an abstract mathematical object that behaves in a curious manner different from a classical bit. Classical bits can take on one of two values, 0 and 1, but a qubit can do that and more:___

Un qubit est le système le plus simple en informatique quantique, la brique fondamentale pour le calcul quantique. Physiquement, les qubits peuvent prendre différentes formes selon le matériel utilisé par l'ordinateur quantique. Mais, du point de vue comportemental, ils agissent tous de la même manière. Vous pouvez donc considérer un 'qubit' comme un objet mathématique abstrait qui se comporte d'une manière curieusement différente d'un bit classique. Les bits classiques peuvent prendre l'une des deux valeurs, 0 ou 1, mais un qubit peut aussi faire cela et même plus encore :

>___Qubits are abstract mathematical objects that have the ability to not only be in the states 0 or 1, but in a *superposition* of the two.___
{: .prompt-tip }

>Les qubits sont des objets mathématiques abstraits qui ont la capacité non seulement d'être dans les états 0 ou 1, mais aussi dans une *superposition* des deux.
{: .prompt-tip }

## Quantum Superposition

## La Superposition Quantique

___Quantum superposition is a neat quantum physics phenomenon that doesn’t really have an analog in classical physics. You can think of it as a combination.___

La superposition quantique est un phénomène remarquable de la physique quantique qui n'a pas vraiment d'équivalent en physique classique. Vous pouvez la concevoir comme une combinaison.

___Where classical bits can only ever be in state 0 or 1 and never a combination of the two, quantum states can be combined and still be valid states. So the state of a qubit can be a combination of 0 *and* 1.___

Alors que les bits classiques ne peuvent être que dans l'état 0 ou 1 et jamais une combinaison des deux, les états quantiques peuvent être combinés et rester des états valides. Ainsi, l'état d'un qubit peut être une combinaison de 0 *et* de 1.

![](/assets/imgs/Marble_Animation.png){: style="max-width: 150px" .left} 
___In Whiskerton, the marbles are by default in such a superposition state: an equally weighted combination of the colors red and blue. It would be incorrect to think of these colors as paint colors. In your everyday, classical experience, if you combine red and blue paint, you would get purple paint. But Whiskertese marbles aren’t actually purple; after a cat directly observes a marble, the color can turn either red or blue, with a fifty percent chance for each. You definitely cannot get the colors red or blue back if you have purple paint!___

À Whiskerton, les billes sont par défaut dans cet état de superposition : une combinaison également pondérée des couleurs rouge et bleue. Il serait incorrect de penser à ces couleurs comme à des couleurs de peinture. Dans votre expérience quotidienne de physique classique, si vous mélangez de la peinture rouge et bleue, vous obtiendriez de la peinture violette. Mais les billes de Whiskerton ne sont pas réellement violettes ; après qu'un chat observe directement une bille, la couleur peut devenir soit rouge soit bleue, avec une chance de cinquante pour cent pour chaque couleur. Vous n'arriverez certainement pas à retrouver les couleurs rouge et bleue si vous avez de la peinture violette !

___Being able to make use of this wondrous phenomenon is one of the ways quantum computing differs from classical computing. In a classical computer, if you perform an operation on a bit, you’re essentially performing that operation on either a 0 or 1, one at a time. If you need to perform an operation on both, you’d have to do so in two shots, consecutively.___

Le fait de pouvoir utiliser ce merveilleux phénomène est l'une des façons dont l'informatique quantique diffère de l'informatique classique. Dans un ordinateur classique, si vous effectuez une opération sur un bit, vous effectuez alors cette opération soit sur un 0 soit sur un 1. Si vous devez effectuer une opération sur les deux, vous devriez le faire en deux temps, consécutivement.

___But by harnessing superposition, a quantum computer could perform that operation on both 0 and 1 at the same time. If we scale this up to many qubits, you can imagine how this may potentially result in speed-ups or an increase in memory capacity or other improvements.___

Mais en exploitant la superposition, un ordinateur quantique pourrait effectuer cette opération sur un 0 et un 1 en même temps. Si nous étendons cela à de nombreux qubits, vous pouvez imaginer comment cela pourrait potentiellement entraîner des accélérations, une augmentation de la capacité de mémoire ou même d'autres améliorations.

## Measurements

## Mesures

___You’ve seen that the marbles have a fifty percent chance of becoming red or blue upon direct observation. A cat observing a marble is a metaphor of measuring a qubit’s state, where red represents a 1 and blue represents a 0. In real life, measurements are conducted by measuring physical quantities in the lab.___

Nous avons vu que les billes ont une chance de cinquante pour cent de devenir rouges ou bleues lors d'une observation directe. Un chat observant une bille est une métaphore de la mesure de l'état d'un qubit, où le rouge représente un 1 et le bleu un 0. Dans la réalité, les mesures sont effectuées en mesurant des quantités physiques en laboratoire.

___Measurement is essentially asking the qubit what state it’s in, but there’s a caveat: simply the act of measurement makes the qubit settle into either the 0 or 1 states, so you only ever get the answer 0 or 1. But there’s a probability associated with each possible outcome.___

La mesure consiste essentiellement à demander au qubit dans quel état il se trouve, mais il y a un hic : l'acte même de la mesure fait que le qubit se fixe soit dans l'état 0, soit dans l'état 1, donc vous n'obtenez jamais que la réponse 0 ou 1. Cependant, il y a une probabilité associée à chaque résultat possible.

___Even if you happen to know everything about the probabilities beforehand--that is, even if you know the exact superposition state of the qubit before measurement--you cannot predict the outcome of a measurement.___

Même si vous connaissez tout sur les probabilités à l'avance - c'est-à-dire même si vous connaissez l'état exact de superposition du qubit avant la mesure - vous ne pouvez pas prédire le résultat d'une mesure.

___Essentially:___

Essentiellement :

> ___Even if you know everything about the state of a quantum system, it *can* still behave randomly.___
{: .prompt-tip }

> Même si vous connaissez tout sur l'état d'un système quantique, il *peut* encore se comporter de manière aléatoire.
{: .prompt-tip }

___For instance, you know everything about the state of a Whiskertese marble: it's in an equally weighted (fifty-fifty) superposition. Yet, after measurement, we don't know if it will end up as a red marble or a blue one. That part is random!___

Par exemple, vous savez tout sur l'état d'une bille de Whiskerton : elle est dans une superposition également pondérée (cinquante-cinquante). Pourtant, après la mesure, nous ne savons pas si elle deviendra une bille rouge ou bleue. Cette partie est aléatoire !

___Quantum physics is probabilistic, which means there is some *uncertainty*. A measurement moves the system from uncertainty to certainty.___

La physique quantique est probabiliste, ce qui signifie qu'il y a une certaine *incertitude*. Effectuer une mesure fait passer le système de l'incertitude à la certitude.

___At first glance, it may appear that the benefit of quantum superposition has vanished since you only ever get 0’s and 1’s as your outcomes, no different from classical bits. Enter quantum computing algorithms.___

À première vue, le bénéfice de la superposition quantique semble inexistant puisque l'on n'obtient que des 0 et des 1 comme résultats, rien de différent des bits classiques. C'est là où les algorithmes de calcul quantique entrent en jeu.

___An algorithm is basically a series of operations you perform to get a desired result. What a quantum computing algorithm does is manipulate the probabilities, increasing the probability associated with the desired outcome and decreasing all others. [^footnote] In this way, if the probability associated with the desired state hits 1, then that outcome is guaranteed, which means the behavior is no longer random.___

Un algorithme est essentiellement une série d'opérations que vous effectuez pour obtenir un résultat souhaité. Ce que fait un algorithme de calcul quantique, c'est manipuler les probabilités, augmentant la probabilité associée au résultat souhaité et diminuant toutes les autres. [^footnote] De cette manière, si la probabilité associée à l'état désiré atteint 1, alors ce résultat est garanti, ce qui signifie que le comportement n'est plus aléatoire.

[^footnote]: ___Quantum operations are carried out by applying what are known as *quantum gates,* logic operations that are the building block of quantum circuits, and analogous to classical logic gates in conventional digital circuits.___

[^footnote]: Les opérations quantiques sont effectuées en appliquant ce que l'on appelle des *portes quantiques*, des opérations logiques qui sont les éléments de base des circuits quantiques, analogues aux portes logiques classiques dans les circuits numériques conventionnels.

___So there you have it. Now that you have an overview of qubits, quantum superposition, and measurements, you know the physics behind the marbles in Whiskerton.___

Voilà. Maintenant que vous avez une vue d'ensemble des qubits, de la superposition quantique et des mesures, vous connaissez la physique derrière les billes de Whiskerton.

> ___If you’d like to dive deeper into these concepts and see how Blade’s predicament is related to what is known as Schrödinger’s cat, read on! Otherwise, head on over to the next story: [Chapter 3 - Story - Doorbells](https://quantum-kittens.github.io/posts/CHAPTER-3-Story-Doorbells/)___
{: .prompt-info }

> Si vous souhaitez approfondir ces concepts et voir comment le dilemme de Blade est lié à ce qu'on appelle le chat de Schrödinger, continuez la lecture ! Sinon, passez à l'histoire suivante : [Chapitre 3 - Histoire - Les Sonnettes](https://quantum-kittens.github.io/fr/posts/CHAPTER-3-Story-Doorbells/)
{: .prompt-info }
_______

## Mathematical Representation of a Qubit State

## Représentation Mathématique de l'Etat d'un Qubit

___Quantum states are mathematically represented by what is known as *Dirac notation*, which makes use of something called a *ket*: $\ket{}$[^fn-nth-1].___

Les états quantiques sont représentés mathématiquement par ce que l'on appelle la *notation de Dirac*, qui utilise un terme que l'on appelle un *ket* : $\ket{}$[^fn-nth-1].

[^fn-nth-1]: ___A ket denotes a mathematical object with certain properties called a *vector*. A qubit can be considered a vector. Two vectors can be combined to form another valid vector. But you don't need to know about vectors to read this text.___

[^fn-nth-1]: Un ket désigne un objet mathématique avec certaines propriétés appelées *vecteurs*. Un qubit peut être considéré comme un vecteur. Deux vecteurs peuvent être combinés pour former un autre vecteur valide. Mais vous n'avez pas besoin de connaître les vecteurs pour lire ce texte.

___This is how an arbitrary qubit state is represented[^fn-nth-2]:___

Voici comment un état de qubit est représenté arbitrairement[^fn-nth-2] :

\begin{equation}
\label{eq:qubit}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

[^fn-nth-2]: ___Disclaimer: This equation is not the complete picture of a qubit; there's a degree of freedom called 'phase' that can be useful for computation but is beyond the scope of this text.___

[^fn-nth-2]: Avertissement : Cette équation ne donne pas une image complète d'un qubit ; il existe une liberté appelée "phase" qui peut être utile pour le calcul mais qui dépasse le cadre de ce texte.

___The Greek letter $\psi$, pronounced "sigh", is a symbolic representation of the state. The $\ket{}$ symbol is written, not spoken. When you refer to the qubit, you can voice, "I have a qubit in the state psi,” or write, “I have a qubit in the state  $\ket{\psi}$," after having defined $\ket{\psi}$ in an equation.___

La lettre grecque $\psi$, prononcée "psi", est une représentation symbolique de l'état. Le symbole $\ket{}$ est écrit, mais non prononcé. Lorsque vous faites référence au qubit, vous pouvez dire : "J'ai un qubit dans l'état psi", ou écrire : "J'ai un qubit dans l'état $\ket{\psi}$", après avoir défini $\ket{\psi}$ dans une équation.

___Notice that $\psi$ isn't the only thing tucked within a ket. You have $\ket{0}$ and $\ket{1}$ in the equation as well, which are the 0 and 1 states. These are called the *basis states* of the qubits; that is, the possible states a qubit can reduce to after measurement, just as a Whiskertese marble can reduce to a red or a blue.  Since a qubit has *two* basis states, a qubit is a two-level system.___

Remarquez que $\psi$ n'est pas la seule chose contenue dans un ket. Vous avez également $\ket{0}$ et $\ket{1}$ dans l'équation, qui sont les états 0 et 1. Ceux-ci sont appelés les *états de base* des qubits ; c'est-à-dire les états possibles auxquels un qubit peut se réduire après mesure, tout comme une bille de Whiskerton peut se réduire à rouge ou bleu. Puisqu'un qubit a *deux* états de base, un qubit est un système à deux niveaux.

___The plus sign indicates a combination, or a superposition. The parameters $\alpha_{0}$ and $\alpha_{1}$ are called *amplitudes*, and let us know how likely it is the qubit will be in the state $\ket{0}$ or $\ket{1}$ after measurement, where $\alpha$ is the Greek letter, alpha. The subscript of the symbol $\alpha$ is a label to indicate to which basis state it corresponds.___

Le signe $\+$ indique une combinaison, ou une superposition. Les paramètres $\alpha_{0}$ et $\alpha_{1}$ sont appelés *amplitudes* et nous indiquent la probabilité que le qubit se trouve dans l'état $\ket{0}$ ou $\ket{1}$ après mesure, où $\alpha$ est la lettre grecque alpha. Le subscript du symbole $\alpha$ est une étiquette pour indiquer à quel état de base il correspond.

___Mathematically, if we square the amplitudes, we’ll get the probabilities associated with each basis state. So, if you measure a qubit in the state $\ket{\psi}$, you will get the result 0 with a probability $\alpha_{0}^2$, or get the result 1 with a probability $\alpha_{1}^2$. [^fn-nth-3]___

Mathématiquement, si nous élevons les amplitudes au carré, nous obtenons les probabilités associées à chaque état de base. Ainsi, si vous mesurez un qubit dans l'état $\ket{\psi}$, vous obtiendrez le résultat 0 avec une probabilité $\alpha_{0}^2$, ou le résultat 1 avec une probabilité $\alpha_{1}^2$. [^fn-nth-3]

[^fn-nth-3]: ___The superscript 2 indicates a 'square', which means the number is being multiplied by itself. That is, $\alpha_{0}^2=\alpha_{0}*\alpha_{0}$.___

[^fn-nth-3]: Le superscript 2 indique un 'carré', ce qui signifie que le nombre est multiplié par lui-même. C'est-à-dire, $\alpha_{0}^2 = \alpha_{0} \times \alpha_{0}$.

___You may rightfully be wondering why these squares are suddenly popping into the picture. It is simply a mathematical convention that reminds us the amplitudes $\alpha_{0}$ and $\alpha_{1}$ may be negative. The squares of each of these amplitudes are probabilities, and probabilities are always positive, as are squares!___

Vous vous demandez peut-être pourquoi ces carrés apparaissent soudainement. C'est simplement une convention mathématique qui nous rappelle que les amplitudes $\alpha_{0}$ et $\alpha_{1}$ peuvent être négatives. Les carrés de chacune de ces amplitudes sont des probabilités, et les probabilités sont toujours positives, tout comme les carrés !

___This means that each quantum state is subject to a constraint. Probability theory has a strict rule: all probabilities should add up to 1, so $\alpha_{0}^2+\alpha_{1}^2=1$ *always*.___

Cela signifie que chaque état quantique est soumis à une contrainte. La théorie des probabilités a une règle stricte : toutes les probabilités additionnées doivent donner un résultat égal à 1, donc $\alpha_{0}^2 + \alpha_{1}^2 = 1$ sera *toujours* vrai.

___Let's look at a specific example. Suppose we have a qubit in the state:___

Regardons un exemple spécifique. Supposons que nous avons un qubit dans l'état :

\begin{equation}
\ket{\psi}=\sqrt{\frac{2}{3}}\ket{0}-\sqrt{\frac{1}{3}}\ket{1}
\end{equation}

___Here, $\alpha_{0}=\sqrt{\frac{2}{3}}$, which means the probability of getting the result 0 after measurement is $\frac{2}{3}$. Similarly for $\alpha_{1}=-\sqrt{\frac{1}{3}}$, and a probability of  $\frac{1}{3}$ associated with result 1. That is, if you have a ton of qubits in this state, and you measure them all, statistically speaking, approximately one third of them would yield the outcome 1. The larger the amplitude, $\alpha$, the higher the probability, and the more likely it is to find the qubit in the associated state after measurement.___[^fn-nth-4]

Ici, $\alpha_{0} = \sqrt{\frac{2}{3}}$, ce qui signifie que la probabilité d'obtenir le résultat 0 après mesure est $\frac{2}{3}$. De même, pour $\alpha_{1} = -\sqrt{\frac{1}{3}}$, la probabilité associée au résultat 1 est $\frac{1}{3}$. Autrement dit, si vous avez une tonne de qubits dans cet état, et que vous les mesurez tous, statistiquement parlant, environ un tiers d'entre eux donneraient le résultat 1. Plus l'amplitude, $\alpha$, est grande, plus la probabilité est élevée, et plus il est probable de trouver le qubit dans l'état associé après mesure. [^fn-nth-4]

[^fn-nth-4]: ___Note for the mathematicians: we refer to $mod(\alpha)$ here.___

[^fn-nth-4]: Remarque pour les mathématiciens : nous faisons référence à $mod(\alpha)$ ici.

## A Note on Statistics

## Une Note sur les Statistiques

___The thing about qubits is that you cannot determine $\alpha_{0}$ and $\alpha_{1}$ for an arbitrary state $\ket{\psi}$ through measurements--the only way to know exactly what numbers these $\alpha$'s are is to have created the state yourself, or to know the person who created it. This is because a measurement always results in a single outcome: 0 or 1, so no measurement can lead to the knowledge of the $\alpha$'s. If someone else created the state, you can ask them for thousands of qubits in identical states and after thousands of measurements, statistically decipher what the amplitudes and thus the probabilities of the state are.___ [^fn-nth-5]

Le problème avec les qubits est que vous ne pouvez pas déterminer $\alpha_{0}$ et $\alpha_{1}$ pour un état arbitraire $\ket{\psi}$ avec des mesures — la seule façon de connaître exactement ces valeurs $\alpha$ est d'avoir créé l'état vous-même, ou de connaître la personne qui l'a créé. Cela est dû au fait qu'une mesure donne toujours un seul résultat : 0 ou 1, donc aucune mesure ne peut fournir la connaissance des $\alpha$. Si quelqu'un d'autre a créé l'état, vous pouvez lui demander des milliers de qubits dans des états identiques et, après des milliers de mesures, déchiffrer statistiquement les amplitudes et donc les probabilités de l'état.

[^fn-nth-5]: ___This is precisely why quantum circuits are run multiple times: to gather statistics. Quantum circuits are quantum computation models that have gate sequences, measurements, and the like.___

[^fn-nth-5]: C'est précisément pour cette raison que les circuits quantiques sont exécutés plusieurs fois : pour collecter des statistiques. Les circuits quantiques sont des modèles de calcul quantique qui comprennent des séquences de portes, des mesures, et autres fonctionnements similaires.

___However, you don't necessarily need to know what the $\alpha$'s are in order for qubit states to be useful. The beauty of the qubit state lies in how one can change and manipulate $\alpha_{0}$ and $\alpha_{1}$ with quantum gates before measurement. As mentioned earlier, the goal is to boost the probabilities associated with the desired outcome. If the desired outcome is 0,  then the algorithm can be designed to boost $\alpha_{0}$, regardless of what it is. And if $\alpha_{0} = 1$, then the outcome 0 will be guaranteed.___

Cependant, vous n'avez pas nécessairement besoin de connaître les valeurs des $\alpha$ pour que les états de qubit soient utiles. La beauté de l'état de qubit réside dans la façon dont on peut changer et manipuler $\alpha_{0}$ et $\alpha_{1}$ avec des portes quantiques avant la mesure. Comme mentionné précédemment, l'objectif est d'augmenter les probabilités associées au résultat souhaité. Si le résultat souhaité est 0, alors l'algorithme peut être conçu pour augmenter $\alpha_{0}$, peu importe ce qu'il est. Et si $\alpha_{0} = 1$, alors le résultat 0 sera garanti.

## Physical Qubits

## Qubits Physiques

___As stated earlier, qubit states are mathematical constructs, which make them easier to work with mathematically to develop algorithms and the like without making a statement on the physical system that is used. This is important, because it doesn't matter whether you physically construct qubit states in the lab as, say, electron spins, polarized states of photons, or something else.___

Comme indiqué précédemment, les états de qubit sont des constructions mathématiques, ce qui les rend plus faciles à manipuler mathématiquement pour développer des algorithmes et autres, sans faire de déclaration sur le système physique utilisé. C'est important, car il n'y a pas d'impact sur les états des qubits, qu'ils soient construits physiquement en laboratoire sous forme de spins d'électrons, d'états polarisés de photons, ou d'une autre façon.

___Don’t know what electrons or photons are? Let’s digress briefly:___

Vous ne savez pas ce que sont les électrons ou les photons ? Faisons une brève déviation :

> ___An electron is a negatively charged subatomic particle. It has a property called 'spin' that we needn't discuss in detail. Suffice it to say that the spin of an electron can be $+\frac{1}{2}$ or $-\frac{1}{2}$, which mathematically can be represented as the states $\ket{0}$ and $\ket{1}$.___
{: .prompt-info }

> Un électron est une particule subatomique chargée négativement. Il possède une propriété appelée 'spin' que nous n'avons pas besoin de détailler. Il suffit de savoir que le spin d'un électron peut être $\+\frac{1}{2}$ ou $\-\frac{1}{2}$, ce qui peut être mathématiquement représenté par les états $\\ket{0}$ et $\\ket{1}$.
{: .prompt-info }


>___A photon is the building block of electromagnetic radiation, which includes visible light. Everything that you see is due to these photons hitting your retinae. When photons are *polarized*, they vibrate in a specific direction rather than all directions. In terms of qubits, polarization in the horizontal direction, say, can be represented by $\ket{0}$ and polarization in the vertical direction, say, can be represented by $\ket{1}$. A superposition of the two is possible, and corresponds to the photon vibrating in a direction between vertical and horizontal, analogous to Southeast lying between South and East on a compass.___
{: .prompt-info }

> Un photon est le constituant de base de la radiation électromagnétique, qui inclut la lumière visible. Tout ce que vous voyez est dû à ces photons frappant vos rétines. Lorsque les photons sont *polarisés*, ils vibrent dans une direction spécifique plutôt que dans toutes les directions. En termes de qubits, la polarisation dans la direction horizontale, par exemple, peut être représentée par $\\ket{0}$ et la polarisation dans la direction verticale, par exemple, peut être représentée par $\\ket{1}$. Une superposition des deux est possible et correspond à un photon vibrant dans une direction entre verticale et horizontale, similaire au Sud-Est se trouvant entre le Sud et l'Est sur une boussole.
{: .prompt-info }

___One important thing to note about qubit states is that they are not stable. Little disturbances in a qubit's environment can reduce it to either $\ket{0}$ or $\ket{1}$: disturbances like heat, vibrations, etc.[^fn-nth-6] And even *that* is unstable; after some time a qubit can jump back into a superposition. It's this little tug of war of states that makes qubits a little tricky to manipulate in the lab--and what keeps the cats of Whiskerton intrigued!___

Une chose importante à noter sur les états de qubit est qu'ils ne sont pas stables. De petites perturbations dans l'environnement d'un qubit peuvent le réduire à $\ket{0}$ ou $\\ket{1}$ : des perturbations comme la chaleur, les vibrations, etc.[^fn-nth-6] Et même *cela* est instable ; après un certain temps, un qubit peut revenir à une superposition. C'est ce petit jeu de va-et-vient des états qui rend les qubits un peu difficiles à manipuler en laboratoire — et ce qui garde les chats de Whiskerton intrigués !

[^fn-nth-6]: ___This sensitivity of quantum states is one of the obstacles in fabricating stable, perfect physical qubits, and devices with a large number of qubits. But this is an exciting research area with lots of promising progress.___

[^fn-nth-6]: Cette sensibilité des états quantiques est l'un des obstacles à la fabrication de qubits physiques stables et parfaits, ainsi que de dispositifs avec un grand nombre de qubits. Mais c'est un domaine de recherche passionnant avec de nombreux progrès prometteurs.

## Schrödinger's Cat

## Le Chat de Schrödinger

___This brings us to Blade in the box with the glitter machine. His predicament is a homage of sorts to a thought experiment by physicist Erwin Schrödinger in 1935[^fn-nth-7].___

Cela nous amène à Blade qui est dans la boîte avec la machine à paillettes. Sa situation est en quelque sorte un hommage à une expérience de pensée du physicien Erwin Schrödinger en 1935[^fn-nth-7].

[^fn-nth-7]: ___Schrödinger, Erwin (November 1935). "Die gegenwärtige Situation in der Quantenmechanik (The present situation in quantum mechanics)". Naturwissenschaften. 23 (48): 807-812.___

[^fn-nth-7]: Schrödinger, Erwin (Novembre 1935). "Die gegenwärtige Situation in der Quantenmechanik (La situation actuelle en mécanique quantique)". Naturwissenschaften. 23 (48): 807-812.

___Qubits are two-level systems and have two basis states, but there are other quantum particles and systems that can have even more. Yet all of these systems, qubits and beyond, adhere to the same rule: upon measurement, the outcome is only one out of all the possibilities.___

Les qubits sont des systèmes à deux niveaux et ont deux états de base, mais il existe d'autres particules et systèmes quantiques qui peuvent en avoir encore plus. Pourtant, tous ces systèmes, qubits et au-delà, respectent la même règle : lors de la mesure, le résultat est unique parmi toutes les possibilités.

___No one really knows why this happens. One possible explanation is the Copenhagen interpretation of quantum mechanics, in which the act of measurement itself collapses all possibilities to a single one. In 1935, physicist Erwin Schrödinger published a paper that outlined his famous thought experiment as a push-back to this interpretation, by hypothetically extrapolating quantum effects on a microscopic level to an everyday macroscopic object: a cat.___

Personne ne sait vraiment pourquoi cela se produit. Une explication possible est l'interprétation de Copenhague de la mécanique quantique, selon laquelle l'acte de mesure lui-même réduit toutes les possibilités à une seule. En 1935, le physicien Erwin Schrödinger publia un article dans lequel il exposait son célèbre expérience de pensée comme une objection à cette interprétation, en extrapolant hypothétiquement les effets quantiques d'un niveau microscopique à un objet quotidien macroscopique : un chat.

___In the original thought experiment, a radioactive substance is used instead of a qubit (or a Whiskertese marble). Radioactive substances decay according to probabilities, just like a qubit reduces to a certain state according to probabilities.___

Dans l'expérience de pensée originale, une substance radioactive est utilisée au lieu d'un qubit (ou d'une bille de Whiskerton). Les substances radioactives se désintègrent selon des probabilités, tout comme un qubit se réduit à un certain état selon des probabilités.

___A cat is placed in a box with a radioactive substance that is linked to a vial of poison. If any one of the atoms decays, then the vial shatters, poisoning the cat. Thus, the state of the cat is coupled with that of the poison system, which is governed by the probability that at least one atom will decay. In this way, before the box is opened, the cat can be considered to be both dead or alive, because each of the possibilities is likely. That is, the cat's reality is undetermined prior to the opening of the box.___

Un chat est placé dans une boîte avec une substance radioactive liée à un flacon de poison. Si un des atomes se désintègre, le flacon se brise, empoisonnant le chat. Ainsi, l'état du chat est couplé à celui du système de poison, qui est régi par la probabilité qu'au moins un atome se désintègre. De cette manière, avant l'ouverture de la boîte, le chat peut être considéré comme étant à la fois mort et vivant, car chacune des possibilités est plausible. Autrement dit, l'état du chat est indéterminée avant l'ouverture de la boîte.

___Schrödinger argued that this is a 'ridiculous case' and that one can't really believe that before one opens the box the cat is in a superposition of dead and alive. He was right, of course. This scenario can't be considered *truly* quantum. The cat isn't a quantum particle, for one. So while the cat isn't actually in a superposition of dead and alive, the thought experiment at the very least demonstrates a probabilistic system.___

Schrödinger a soutenu que c'était un "cas ridicule" et qu'on ne peut vraiment croire qu'avant d'ouvrir la boîte, le chat est dans une superposition de mort et vivant. Il avait raison, bien sûr. Ce scénario ne peut pas être considéré comme *vraiment* quantique. Le chat n'est pas une particule quantique, pour commencer. Donc, bien que le chat ne soit pas réellement dans une superposition de mort et vivant, l'expérience de pensée démontre au moins un système probabiliste.

___This thought experiment has fast become one of the most recognized iconographies of quantum phenomenon in popular culture, and naturally had to make an appearance in Whiskerton. With glitter, of course, because there's no reason to get morbid in such a quaint little town. Note that Schrödinger didn't actually poison cats--he merely thought about it!___

Cette expérience de pensée est rapidement devenue l'une des iconographies les plus reconnues des phénomènes quantiques dans la culture populaire et devait naturellement faire son apparition à Whiskerton. Avec des paillettes, bien sûr, car il n'y a pas de raison de devenir morbide dans une si charmante petite ville. Notez que Schrödinger n'empoisonnait pas réellement les chats — il ne faisait qu'y penser !

___Now, there’s one more curious aspect to this thought experiment: you could say that the state of the cat is *entangled* with that of the radioactive substance.___

D'ailleurs, il y a un autre aspect curieux de cette expérience : on pourrait dire que l'état du chat est *intriqué* avec celui de la substance radioactive.

___Quantum entanglement is actually our next stop! Let’s hop to it: **[Next: Chapter 3 - Story - Doorbells](https://quantum-kittens.github.io/posts/CHAPTER-3-Story-Doorbells/)**___

L’intrication quantique est justement notre prochaine étape ! Allons-y : **[A suivre: Chapitre 3 - Histoire - Les Sonnettes](https://quantum-kittens.github.io/posts/CHAPTER-3-Story-Doorbells/)**

_____________________________


_____________________________


_____________________________




## Qiskit Code

## Code Qiskit

___This section is for those of you who want to get started with Qiskit, IBM Quantum’s open source python framework to program quantum computers.___

Cette section est destinée à ceux d'entre vous qui souhaitent commencer avec Qiskit, le framework open source en Python d'IBM Quantum pour programmer des ordinateurs quantiques.

___You can simulate a Whiskerton marble using this supplementary Qiskit code. This code walks you through creating and running a quantum circuit with a single qubit.___

Vous pouvez simuler une bille de Whiskerton en utilisant ce code Qiskit complémentaire. Ce code vous guide à travers la création et l'exécution d'un circuit quantique avec un seul qubit.

___You can run this code in two ways:___

Vous pouvez exécuter ce code de deux façons différentes :

___- On the cloud: copy and paste the code into a jupyter notebook in the [IBM Quantum Lab](https://quantum-computing.ibm.com/lab) 
- Locally: you can [install Qiskit](https://qiskit.org/) and run the code on your local machine___

- Sur le cloud : copiez et collez le code dans un notebook Jupyter sur le [IBM Quantum Lab](https://quantum-computing.ibm.com/lab).
- Localement : vous pouvez [installer Qiskit](https://qiskit.org/) et exécuter le code sur votre machine locale.



 ```python
# Importation des modules Qiskit nécessaires
from qiskit import QuantumCircuit, transpile
from qiskit.visualization import *
from qiskit import BasicAer

#Charge vo(s) compte(s) IBM Quantum
#provider = IBMQ.load_account()

# Création d'un circuit de bille de Whiskerton

marble_circuit = QuantumCircuit(1, 1) # Ajoute un qubit (bille de Whiskerton) et un bit classique (pour enregistrer le résultat de la mesure)

marble_circuit.h(0) # Ajout d'une H-gate ou porte d'Hadamard au qubit (c'est la porte quantique qui mets la bille en superposition)

marble_circuit.measure(0,0) # Add a measurement operator (this is equivalent to a cat looking directly at a marble)
marble_circuit.measure(0,0) # Ajout d'une opération de mesure (c'est l'équivalent pour un chat de regarder directement une bille)

marble_circuit.draw('mpl') # Montre ce à quoi ressemble le circuit
```



 ```python

# Exécute le circuit avec la bille de Whiskerton,
# Ca signifie regarder si la bille devient rouge ou bleue

marble_state = {'1': 'rouge', '0': 'bleue'}

simulator = BasicAer.get_backend("qasm_simulator") # Identifie l'ordinateur quantique sur lequel exécuter ce code. Dans ce cas, il s'agit d'un simulateur, et non pas d'un appareil réel

compiled_circuit = transpile(marble_circuit, simulator) # Compile le circuit pour des instructions de bas niveau QASM

job = simulator.run(compiled_circuit, shots=1000) # Exécute le circuit sur le simulateur 1000 fois pour faire des statistiques

# Récupère et affiche le résultat :

result = job.result() 
counts = result.get_counts(compiled_circuit)

ans = str(max(counts, key=counts.get))

print('The marble is ' + marble_state[ans] +'.') # The outcome is the one associated with the highest count.
print('La bille est ' + marble_state[ans] +'.') # Le résultat est celui associé au plus grand nombre de comptages.


```

 ```python

# Examine les statistiques et affiche l'histogramme

print("Votre résultat sous forme de nombre :", counts)
print("Cela signifie qu'en 1000 essais, la bille devient bleue " + str(counts['0']) + " fois, et rouge " + str(counts['1']) + " fois.")

plot_histogram(counts)

```

___The above code is also available as a jupyter notebook [here](https://github.com/quantum-kittens/quantum-kittens.github.io/blob/main/jupyter_notebooks/QK_Chapter_2.ipynb).___

Le code précédent est également disponible en notebook Jupyter [ici](https://github.com/quantum-kittens/quantum-kittens.github.io/blob/main/jupyter_notebooks/QK_Chapter_2.ipynb).

___*Note: the Qiskit code provided is open source, and does not fall under the copyright of Quantum Kittens.*___

*Note : Le code Qiskit fournit est open source, et n'est pas sous la license de Quantum Kittens.*
