---
title: 'Chapitre 2 Partie 2 - Commentaire - Qubits, Superposition, et Mesures'
math: true
---


Vous savez très probablement ce qu'est l'informatique classique ; c'est ce que la plupart des gens entendent par "informatique". C'est le type de calcul effectué par les appareils électroniques quotidiens comme celui que vous utilisez pour lire ceci, et même les calculs effectués par les superordinateurs cachés dans les laboratoires.

Au niveau fondamental d'un ordinateur classique, l'information est transportée par des *bits* : des unités d'information uniques qui ne peuvent avoir que l'une des deux valeurs ou *états* : 0 ou 1. De la même manière, les ordinateurs quantiques ont une unité de calcul fondamentale, appelée bits quantiques ou *qubits*. Voici un fait amusant : les billes de Whiskerton représentent en réalité des qubits !

## Qu'est ce qu'un Qubit ?

Un qubit est le système le plus simple en informatique quantique, c'est la brique fondamentale pour le calcul quantique. Physiquement, les qubits peuvent prendre différentes formes selon le matériel utilisé par l'ordinateur quantique. Mais, du point de vue comportemental, ils agissent tous de la même manière. Vous pouvez donc considérer un 'qubit' comme un objet mathématique abstrait qui se comporte d'une manière curieusement différente d'un bit classique. Les bits classiques peuvent prendre l'une des deux valeurs, 0 ou 1. Mais un qubit peut aussi faire cela et même plus encore :

> Les qubits sont des objets mathématiques abstraits qui ont la capacité non seulement d'être dans les états 0 ou 1, mais aussi dans une *superposition* des deux.
{: .prompt-tip }

## La Superposition Quantique

La superposition quantique est un phénomène remarquable de la physique quantique qui n'a pas vraiment d'équivalent en physique classique. Vous pouvez la concevoir comme une combinaison.

Alors que les bits classiques ne peuvent être que dans l'état 0 ou 1 et jamais une combinaison des deux, les états quantiques peuvent être combinés et rester des états valides. Ainsi, l'état d'un qubit peut être une combinaison de 0 *et* de 1.

![](/assets/imgs/Marble_Animation.png){: style="max-width: 150px" .left} 

À Whiskerton, les billes sont par défaut dans cet état de superposition : une combinaison également pondérée des couleurs rouge et bleue. Il serait incorrect de penser à ces couleurs comme à des couleurs de peinture. Dans votre expérience quotidienne de physique classique, si vous mélangez de la peinture rouge et bleue, vous obtiendriez de la peinture violette. Mais les billes de Whiskerton ne sont pas réellement violettes ; après qu'un chat observe directement une bille, la couleur peut devenir soit rouge soit bleue, avec une chance de cinquante pour cent pour chaque couleur. Vous n'arriverez certainement pas à retrouver les couleurs rouge et bleue si vous avez de la peinture violette !

Le fait de pouvoir utiliser ce merveilleux phénomène est l'une des façons dont l'informatique quantique diffère de l'informatique classique. Dans un ordinateur classique, si vous effectuez une opération sur un bit, vous effectuez alors cette opération soit sur un 0 soit sur un 1. Si vous devez effectuer une opération sur les deux états, vous devriez le faire en deux temps, consécutivement.

Mais en exploitant la superposition, un ordinateur quantique pourrait effectuer cette opération sur un 0 et un 1 en même temps. Si nous étendons cela à de nombreux qubits, vous pouvez imaginer comment cela pourrait potentiellement entraîner des accélérations de calcul, une augmentation de la capacité de mémoire ou même d'autres améliorations.

## Mesures

Nous avons vu que les billes ont une chance de cinquante pour cent de devenir rouges ou bleues lors d'une observation directe. Un chat observant une bille est une métaphore de la mesure de l'état d'un qubit, où le rouge représente un 1 et le bleu un 0. Dans la réalité, les mesures sont effectuées en mesurant des quantités physiques en laboratoire.

La mesure consiste essentiellement à demander au qubit dans quel état il se trouve, mais il y a un hic : l'acte même de la mesure fait que le qubit se fixe soit dans l'état 0, soit dans l'état 1, donc vous n'obtenez jamais que la réponse 0 ou 1. Cependant, il y a une probabilité associée à chaque résultat possible.

Même si vous connaissez tout sur les probabilités à l'avance - c'est-à-dire même si vous connaissez l'état exact de superposition du qubit avant la mesure - vous ne pouvez pas prédire le résultat d'une mesure.

Essentiellement :

> Même si vous connaissez tout sur l'état d'un système quantique, il *peut* encore se comporter de manière aléatoire.
{: .prompt-tip }

Par exemple, vous savez tout sur l'état d'une bille de Whiskerton : elle est dans une superposition également pondérée (cinquante-cinquante). Pourtant, après la mesure, nous ne savons pas si elle deviendra une bille rouge ou bleue. Cette partie est aléatoire !

La physique quantique est probabiliste, ce qui signifie qu'il y a une certaine *incertitude*. Effectuer une mesure fait passer le système de l'incertitude à la certitude.

À première vue, le bénéfice de la superposition quantique semble inexistant puisque l'on n'obtient que des 0 et des 1 comme résultats, rien de différent des bits classiques. C'est là où les algorithmes de calcul quantique entrent en jeu.

Un algorithme est essentiellement une série d'opérations que vous effectuez pour obtenir un résultat souhaité. Ce que fait un algorithme de calcul quantique, c'est manipuler les probabilités, augmentant la probabilité associée au résultat souhaité et diminuant toutes les autres.[^footnote] De cette manière, si la probabilité associée à l'état désiré atteint 1, alors ce résultat est garanti, ce qui signifie que le comportement n'est plus aléatoire.

[^footnote]: Les opérations quantiques sont effectuées en appliquant ce que l'on appelle des *portes quantiques*, des opérations logiques qui sont les éléments de base des circuits quantiques, similaires aux portes logiques classiques dans les circuits numériques conventionnels.

Voilà. Maintenant que vous avez une vue d'ensemble des qubits, de la superposition quantique et des mesures, vous connaissez la physique derrière les billes de Whiskerton.

> Si vous souhaitez approfondir ces concepts et voir comment le dilemme de Blade est lié à ce qu'on appelle le chat de Schrödinger, continuez la lecture ! Sinon, passez à l'histoire suivante : [Chapitre 3 - Histoire - Les Sonnettes](https://quantum-kittens.github.io/fr/posts/CHAPTER-3-Story-Doorbells/)
{: .prompt-info }
_______

## Représentation Mathématique de l'Etat d'un Qubit

Les états quantiques sont représentés mathématiquement par ce que l'on appelle la *notation de Dirac*, qui utilise un terme que l'on appelle un *ket* : $\ket{}$[^fn-nth-1].

[^fn-nth-1]: Un ket désigne un objet mathématique avec certaines propriétés appelées *vecteurs*. Un qubit peut être considéré comme un vecteur. Deux vecteurs peuvent être combinés pour former un autre vecteur valide. Mais vous n'avez pas besoin de connaître les vecteurs pour lire ce texte.

Voici comment un état de qubit est représenté de façon arbitraire[^fn-nth-2] :

\begin{equation}
\label{eq:qubit}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

[^fn-nth-2]: Avertissement : Cette équation ne donne pas une image complète d'un qubit ; il existe une liberté appelée "phase" qui peut être utile pour le calcul mais qui dépasse le cadre de ce texte.

La lettre grecque $\psi$, prononcée "psi", est une représentation symbolique de l'état. Le symbole $\ket{}$ est écrit, mais non prononcé. Lorsque vous faites référence au qubit, vous pouvez dire : "J'ai un qubit dans l'état psi", ou écrire : "J'ai un qubit dans l'état $\ket{\psi}$", après avoir défini $\ket{\psi}$ dans une équation.

Remarquez que $\psi$ n'est pas la seule chose contenue dans un ket. Vous avez également $\ket{0}$ et $\ket{1}$ dans l'équation, qui sont les états 0 et 1. Ceux-ci sont appelés les *états de base* des qubits ; c'est-à-dire les états possibles auxquels un qubit peut se réduire après mesure, tout comme une bille de Whiskerton peut se réduire à rouge ou bleu. Puisqu'un qubit a *deux* états de base, un qubit est un système à deux niveaux.

Le signe $\+$ indique une combinaison, ou une superposition. Les paramètres $\alpha_{0}$ et $\alpha_{1}$ sont appelés *amplitudes* et nous indiquent la probabilité que le qubit se trouve dans l'état $\ket{0}$ ou $\ket{1}$ après mesure, où $\alpha$ est la lettre grecque alpha. Le subscript du symbole $\alpha$ est une étiquette pour indiquer à quel état de base il correspond.

Mathématiquement, si nous élevons les amplitudes au carré, nous obtenons les probabilités associées à chaque état de base. Ainsi, si vous mesurez un qubit dans l'état $\ket{\psi}$, vous obtiendrez le résultat 0 avec une probabilité $\alpha_{0}^2$, ou le résultat 1 avec une probabilité $\alpha_{1}^2$. [^fn-nth-3]

[^fn-nth-3]: Le superscript 2 indique un 'carré', ce qui signifie que le nombre est multiplié par lui-même. C'est-à-dire, $\alpha_{0}^2 = \alpha_{0} \times \alpha_{0}$.

Vous vous demandez peut-être pourquoi ces carrés apparaissent soudainement. C'est simplement une convention mathématique qui nous rappelle que les amplitudes $\alpha_{0}$ et $\alpha_{1}$ peuvent être négatives. Les carrés de chacune de ces amplitudes sont des probabilités, et les probabilités sont toujours positives, tout comme les résultats des carrés !

Cela signifie que chaque état quantique est soumis à une contrainte. La théorie des probabilités a une règle stricte : toutes les probabilités additionnées doivent donner un résultat égal à 1, donc $\alpha_{0}^2 + \alpha_{1}^2 = 1$ sera *toujours* vrai.

Regardons un exemple spécifique. Supposons que nous avons un qubit dans l'état :

\begin{equation}
\ket{\psi}=\sqrt{\frac{2}{3}}\ket{0}-\sqrt{\frac{1}{3}}\ket{1}
\end{equation}

Ici, $\alpha_{0} = \sqrt{\frac{2}{3}}$, ce qui signifie que la probabilité d'obtenir le résultat 0 après mesure est $\frac{2}{3}$. De même, pour $\alpha_{1} = -\sqrt{\frac{1}{3}}$, la probabilité associée au résultat 1 est $\frac{1}{3}$. Autrement dit, si vous avez une tonne de qubits dans cet état, et que vous les mesurez tous, statistiquement parlant, environ un tiers d'entre eux donneraient le résultat 1. Plus l'amplitude, $\alpha$, est grande, plus la probabilité est élevée, et plus il est probable de trouver le qubit dans l'état associé après mesure.[^fn-nth-4]

[^fn-nth-4]: Remarque pour les mathématiciens : nous faisons ici référence à $mod(\alpha)$.

## Une Note sur les Statistiques

Le problème avec les qubits est que vous ne pouvez pas déterminer $\alpha_{0}$ et $\alpha_{1}$ pour un état arbitraire $\ket{\psi}$ avec des mesures — la seule façon de connaître exactement ces valeurs $\alpha$ est d'avoir créé l'état vous-même, ou de connaître la personne qui l'a créé. Cela est dû au fait qu'une mesure donne toujours un seul résultat : 0 ou 1, donc aucune mesure ne peut fournir la connaissance des $\alpha$. Si quelqu'un d'autre a créé l'état, vous pouvez lui demander des milliers de qubits dans des états identiques et, après des milliers de mesures, déchiffrer statistiquement les amplitudes et donc les probabilités de l'état.[^fn-nth-5]

[^fn-nth-5]: C'est précisément pour cette raison que les circuits quantiques sont exécutés plusieurs fois : pour collecter des statistiques. Les circuits quantiques sont des modèles de calcul quantique qui comprennent des séquences de portes, des mesures, et autres fonctionnements similaires.

Cependant, vous n'avez pas nécessairement besoin de connaître les valeurs des $\alpha$ pour que les états de qubit soient utiles. La beauté de l'état de qubit réside dans la façon dont on peut changer et manipuler $\alpha_{0}$ et $\alpha_{1}$ avec des portes quantiques avant la mesure. Comme mentionné précédemment, l'objectif est d'augmenter les probabilités associées au résultat souhaité. Si le résultat souhaité est 0, alors l'algorithme peut être conçu pour augmenter $\alpha_{0}$, peu importe sa valeur. Et si $\alpha_{0} = 1$, alors le résultat 0 sera garanti.

## Qubits Physiques

Comme indiqué précédemment, les états de qubit sont des constructions mathématiques, ce qui les rend plus faciles à manipuler mathématiquement pour développer des algorithmes et autres, sans faire de déclaration sur le système physique utilisé. C'est important, car il n'y a pas d'impact sur les états des qubits, qu'ils soient construits physiquement en laboratoire sous forme de spins d'électrons, d'états polarisés de photons, ou d'une autre façon.

Vous ne savez pas ce que sont les électrons ou les photons ? Faisons une brève déviation :

> Un électron est une particule subatomique chargée négativement. Il possède une propriété appelée 'spin' que nous n'avons pas besoin de détailler. Il suffit de savoir que le spin d'un électron peut être $\+\frac{1}{2}$ ou $\-\frac{1}{2}$, ce qui peut être mathématiquement représenté par les états $\\ket{0}$ et $\\ket{1}$.
{: .prompt-info }

> Un photon est le constituant de base de la radiation électromagnétique, qui inclut la lumière visible. Tout ce que vous voyez est dû à ces photons frappant vos rétines. Lorsque les photons sont *polarisés*, ils vibrent dans une direction spécifique plutôt que dans toutes les directions. En termes de qubits, la polarisation dans la direction horizontale, par exemple, peut être représentée par $\\ket{0}$ et la polarisation dans la direction verticale, par exemple, peut être représentée par $\\ket{1}$. Une superposition des deux est possible et correspond à un photon vibrant dans une direction entre verticale et horizontale, similaire au Sud-Est se trouvant entre le Sud et l'Est sur une boussole.
{: .prompt-info }

Une chose importante à noter sur les états de qubit est qu'ils ne sont pas stables. De petites perturbations dans l'environnement d'un qubit peuvent le réduire à $\ket{0}$ ou $\\ket{1}$ : des perturbations comme la chaleur, les vibrations, etc.[^fn-nth-6] Et même *cela* est instable ; après un certain temps, un qubit peut revenir à une superposition. C'est ce petit jeu de va-et-vient des états qui rend les qubits un peu difficiles à manipuler en laboratoire — et ce qui garde les chats de Whiskerton intrigués !

[^fn-nth-6]: Cette sensibilité des états quantiques est l'un des obstacles à la fabrication de qubits physiques stables et parfaits, ainsi que de dispositifs avec un grand nombre de qubits. Mais c'est un domaine de recherche passionnant avec de nombreux progrès prometteurs.

## Le Chat de Schrödinger

Cela nous amène à Blade qui est dans la boîte avec la machine à paillettes. Sa situation est en quelque sorte un hommage à une expérience de pensée du physicien Erwin Schrödinger en 1935[^fn-nth-7].

[^fn-nth-7]: Schrödinger, Erwin (Novembre 1935). "Die gegenwärtige Situation in der Quantenmechanik (La situation actuelle en mécanique quantique)". Naturwissenschaften. 23 (48): 807-812.

Les qubits sont des systèmes à deux niveaux et ont deux états de base, mais il existe d'autres particules et systèmes quantiques qui peuvent en avoir encore plus. Pourtant, tous ces systèmes, qubits et au-delà, respectent la même règle : lors de la mesure, le résultat est unique parmi toutes les possibilités.

Personne ne sait vraiment pourquoi cela se produit. Une explication possible est l'interprétation de Copenhague de la mécanique quantique, selon laquelle l'acte de mesure lui-même réduit toutes les possibilités à une seule. En 1935, le physicien Erwin Schrödinger publia un article dans lequel il exposait son célèbre expérience de pensée comme une objection à cette interprétation, en extrapolant hypothétiquement les effets quantiques d'un niveau microscopique à un objet quotidien macroscopique : un chat.

Dans cette expérience de pensée originale, une substance radioactive est utilisée au lieu d'un qubit (ou d'une bille de Whiskerton). Les substances radioactives se désintègrent selon des probabilités, tout comme un qubit se réduit à un certain état selon des probabilités.

Un chat est placé dans une boîte avec une substance radioactive liée à un flacon de poison. Si un des atomes se désintègre, le flacon se brise, empoisonnant le chat. Ainsi, l'état du chat est couplé à celui du système de poison, qui est régi par la probabilité qu'au moins un atome se désintègre. De cette manière, avant l'ouverture de la boîte, le chat peut être considéré comme étant à la fois mort et vivant, car chacune des possibilités est plausible. Autrement dit, l'état du chat est indéterminée avant l'ouverture de la boîte.

Schrödinger a soutenu que c'était un "cas ridicule" et qu'on ne peut vraiment croire qu'avant d'ouvrir la boîte, le chat est dans une superposition de mort et vivant. Il avait raison, bien sûr. Ce scénario ne peut pas être considéré comme *vraiment* quantique. Le chat n'est pas une particule quantique, pour commencer. Mais, bien que le chat ne soit pas réellement dans une superposition de mort et vivant, l'expérience de pensée démontre tout de même un système probabiliste.

Cette expérience de pensée est rapidement devenue l'une des iconographies les plus reconnues des phénomènes quantiques dans la culture populaire et devait naturellement faire son apparition à Whiskerton. Avec des paillettes, bien sûr, car il n'y a pas de raison de devenir morbide dans une si charmante petite ville. Notez que Schrödinger n'empoisonnait pas réellement les chats — il ne faisait qu'y penser !

D'ailleurs, il y a un autre aspect curieux de cette expérience : on pourrait dire que l'état du chat est *intriqué* avec celui de la substance radioactive.

L’intrication quantique est justement notre prochaine étape ! Allons-y : **[A suivre: Chapitre 3 - Histoire - Les Sonnettes](https://quantum-kittens.github.io/posts/CHAPTER-3-Story-Doorbells/)**

_____________________________


_____________________________


_____________________________


## Code Qiskit

Cette section est destinée à ceux d'entre vous qui souhaitent commencer avec Qiskit, le framework open source en Python d'IBM Quantum pour programmer des ordinateurs quantiques.

Vous pouvez simuler une bille de Whiskerton en utilisant ce code Qiskit complémentaire. Ce code vous guide à travers la création et l'exécution d'un circuit quantique avec un seul qubit.

Vous pouvez exécuter ce code de deux façons différentes :

- Sur le cloud : vous pouvez choisir d'utiliser un outil situé sur le cloud comme [Google Colab](https://colab.research.google.com/) ou [qBraid](https://www.qbraid.com/).
- Localement : vous pouvez [installer Qiskit](https://qiskit.org/) et exécuter le code sur votre machine locale.

Vous pouvez lire ce blog (*en anglais*) pour davantage de détails concernant l'installation : [
Explore newly recommended notebook environments for Qiskit](https://www.ibm.com/quantum/blog/qiskit-notebook-environments).

Le code qui suit est également disponible en tant que notebook jupyter [ici](https://github.com/quantum-kittens/quantum-kittens.github.io/blob/main/jupyter_notebooks/QK_Chapter_2.ipynb) (*commentaires en anglais*).

Note de Novembre 2024 : ce code a maintenant été mis à jour pour Qiskit 1.0. Si vous utilisiez une version antérieur de Qiskit auparavant, ce blog (*en anglais*) peut vous être utile : [Best practices for transitioning to Qiskit SDK v1.0](https://www.ibm.com/quantum/blog/transition-to-1).



 ```python
# Installez Qiskit avec des dépendances optionnelles utiles pour la visualisation en
# dé-commentant les lignes suivantes is vous n'avez pas encore Qiskit d'installé

#pip install'qiskit[visualization]'

# Installez 'Qiskit Runtime Service' si vous ne l'avez pas encore fait en dé-commentant la ligne suivante 

#pip install qiskit-ibm-runtime

# Installez 'Qiskit Aer Simulator' si vous ne l'avez pas encore fait en dé-commentant la ligne suivante

#pip install qiskit-aer


# Importation des modules Qiskit nécessaires
from qiskit import QuantumCircuit

#Charge votre(vos) compte(s) IBM Quantum
#provider = IBMQ.load_account()

# Création d'un circuit de bille de Whiskerton

marble_circuit = QuantumCircuit(1, 1) # Ajoute un qubit (bille de Whiskerton) et un bit classique (pour enregistrer le résultat de la mesure)

marble_circuit.h(0) # Ajout d'une H-gate ou porte d'Hadamard au qubit (c'est la porte quantique qui mets la bille en superposition)

marble_circuit.measure(0,0) # Add a measurement operator (this is equivalent to a cat looking directly at a marble)
marble_circuit.measure(0,0) # Ajout d'une opération de mesure (c'est l'équivalent pour un chat de regarder directement une bille)

marble_circuit.draw('mpl') # Montre ce à quoi ressemble le circuit
```



 ```python

# Importe les librairies nécessaires à Qiskit pour exécuter le circuit sur un simulateur

from qiskit.transpiler.preset_passmanagers import generate_preset_pass_manager
from qiskit_ibm_runtime import QiskitRuntimeService
from qiskit_aer import AerSimulator
from qiskit_ibm_runtime import SamplerV2 as Sampler
from qiskit.visualization import plot_histogram

# Exécute le circuit avec la bille de Whiskerton,
# Ca signifie regarder si la bille devient rouge ou bleue

marble_state = {'1': 'rouge', '0': 'bleue'}

aer_sim = AerSimulator() # Identifie l'ordinateur quantique sur lequel exécuter ce code. Dans ce cas, il s'agit d'un simulateur, et non pas d'un appareil réel
pm = generate_preset_pass_manager(backend=aer_sim, optimization_level=1) 
isa_marble_circuit = pm.run(marble_circuit) # Cette ligne ainsi que la ligne précédente prépare le circuit à être exécuté sur la machine que vous avez sélectionné. Pour plus de détails techniques, vous pouvez consulter : https://docs.quantum.ibm.com/api/qiskit/transpiler#transpiler

# Récupère et affiche le résultat :
sampler = Sampler(mode=aer_sim)

result = sampler.run([isa_marble_circuit], shots=1000).result() # Exécute le circuit sur le simulateur 1000 fois pour générer des statistiques.
counts = result[0].data.c.get_counts()

ans = str(max(counts, key=counts.get))

print('La bille est ' + marble_state[ans] + '.') # Le résultat final est celui associé au plus grand cumul de points.



```

```python

# Examine les statistiques et affiche l'histogramme

print("Votre résultat sous forme de nombre :", counts)
print("Cela signifie qu'en 1000 essais, la bille devient bleue " + str(counts['0']) + " fois, et rouge " + str(counts['1']) + " fois.")

plot_histogram(counts)

```

```python
# Si vous voulez exécuter ce circuit sur une vrai machine, vous pouvez exécuter les lignes suivante :

#from qiskit_ibm_runtime import QiskitRuntimeService
 
#service = QiskitRuntimeService(channel="ibm_quantum", token="<insert your token here>")
```



*Note : Le code Qiskit fournit est open source, et n'est pas sous la license de Quantum Kittens.*
