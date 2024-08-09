---
title: 'Chapitre 3 Partie 2 - Commentaires - Qubits Multiples, Intrication, et Etats de Bell'
math: true
---


Il n'y a pas grand-chose que vous puissiez faire avec un seul bit classique. Le traitement de l'information et les algorithmes nécessitent généralement plusieurs unités d'information. Par exemple, au niveau de la machine, une image sur votre fil d'actualité des réseaux sociaux n'est pas représentée par un seul bit. Elle est représentée par *plusieurs* bits, de nombreux 0 et 1, et ce sont ces chaînes de bits qui sont transmises sur internet et traitées par vos appareils.

De la même manière, il n'y a pas grand-chose que vous puissiez faire avec un seul qubit, aussi sophistiqué soit-il. En réalité, l'avantage potentiel de l'informatique quantique par rapport à l'informatique classique dans certains contextes réside dans la possibilité de créer un jour des processeurs avec des centaines, voire des milliers de qubits stables et parfaits.

Par conséquent, la plupart des protocoles de calcul quantique impliquent plus d'un qubit, tout comme les sonnettes de Whiskerton impliquent plus d'une bille. Certes, les sonnettes de Whiskerton sont encore des systèmes quantiques très simples avec seulement deux billes, alors que certains des algorithmes conçus pour les futurs ordinateurs quantiques en nécessitent beaucoup plus. Néanmoins, ces sonnettes illustrent un phénomène quantique dont même les protocoles plus complexes tirent parti : un phénomène quantique qui n'a pas d'équivalent dans le monde classique, *l'intrication quantique*.

## Qu'est ce que l'Intrication Quantique ?

L'intrication quantique décrit une connexion ou une relation particulière entre des systèmes quantiques. Si deux systèmes quantiques sont intriqués, ils sont connectés de telle manière que leurs états ne peuvent pas être décrits indépendamment, et effectuer des mesures sur l'un des systèmes affectera l'autre, même si le second système n'est pas à proximité.

Pour faire court, ce qui suit est possible dans le monde quantique :

> Même si deux qubits (ou systèmes quantiques) sont trop éloignés pour s'influencer directement, ils peuvent encore être corrélés de manière à ce que manipuler l'un affecte immédiatement l'autre.
{: .prompt-tip }

Les deux billes dans une sonnette de Whiskerton sont intriquées. Rappelez-vous que si l'une devient rouge, la seconde le devient aussi, même si les deux sont dans des boîtes séparées. Il n'est pas nécessaire de regarder directement la seconde bille pour qu'elle se réduise à une seule couleur.

Cet enchevêtrement n’est pas tout à fait comme les corrélations que nous voyons dans notre vie quotidienne. Dans notre monde classique, si vous avez deux billes dans un sac opaque, une rouge et une bleue, et que vous sortez la bleue, vous sauriez immédiatement que la rouge est encore dans le sac. C'est une corrélation classique, le type de corrélation que nous expérimentons quotidiennement.

Cependant, l'intrication quantique ne se comporte pas comme les corrélations classiques. Il y a des subtilités qui ne se traduisent pas dans notre expérience quotidienne. Par exemple, si les billes étaient des billes de Whiskerton, elles ne seraient pas d'une seule couleur au départ. La bille que vous sortez du sac serait en superposition jusqu'à ce que vous la regardiez. Ce n'est qu'une fois que la bille dans votre main se réduit à une seule couleur que la bille dans le sac changerait, même si le sac était emporté loin de vous. [^fn-nth-1]

[^fn-nth-1]: Il y a d'autres subtilités liées à l'intrication, et deux systèmes quantiques qui sont très, très éloignés doivent également être ce qu'on appelle *non-locaux* pour s'influencer mutuellement, mais ce sont des explorations à garder pour un autre jour.

Puisqu'il s'agit de deux entités qui s'influencent instantanément malgré la distance qui les sépare, vous pourriez légitimement vous demander : cela signifie-t-il que nous pouvons envoyer de l'information plus rapidement que la lumière ? Malheureusement, la réponse est non.

Le hic, c'est que faire n'importe quel type de mesure ne fonctionnera pas—oui, il existe différents *types* de mesures ! Les types de mesures sont variées, et cela dépassent le cadre de ce texte, mais disons simplement que si vous et un ami qui habite loin, partagez une paire intriquée, alors le type de mesure que vous effectuez sur votre partie de la paire doit être communiqué à votre ami d'une manière ou d'une autre. Si votre ami ne sait pas quel type de mesure effectuer sur sa partie, il ne pourra pas "voir" le résultat attendu ! Donc, une sorte de communication doit avoir lieu, par exemple, via un appel téléphonique. Ce qui… ne peut pas se faire plus rapidement que la lumière.

> Si vous souhaitez approfondir un peu plus l'intrication quantique, continuez à lire ! Sinon, passez à la page suivante : [Ce N'est Pas Tout](https://quantum-kittens.github.io/posts/This-is-not-the-end/)
{: .prompt-info }

_______

## Représentation Mathématique d'Etats de Plusieurs Qubits

Les états de plusieurs qubits sont représentés de manière similaire aux états d'un seul qubit. Nous allons nous concentrer sur les états de deux qubits, car les sonnettes de Whiskerton ont deux qubits, mais cette représentation s'applique également à un nombre plus élevé de qubits.

Souvenez-vous de l'équation arbitraire concernant l'état d'un simple qubit du [Chapitre 2](https://quantum-kittens.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/):

\begin{equation}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

Dans cette équation, les états de base sont analogues aux deux valeurs qu'un bit classique peut avoir : 0 et 1. Un qubit peut être dans une superposition des deux états de base.

Pour comprendre comment représenter un état à deux qubits, examinons toutes les valeurs possibles de deux bits classiques. Deux bits, combinés, peuvent avoir l'une des quatre valeurs suivantes : 00, 01, 10 ou 11. Tout comme dans le cas d'un seul qubit, ces quatre valeurs correspondent à quatre états de base. Deux qubits peuvent être dans l'un de ces quatre états ou dans une superposition de ces états ! Par conséquent, un état arbitraire à deux qubits peut être représenté par l'équation suivante :

\begin{equation}
\ket{\psi}=\alpha_{00}\ket{00}+\alpha_{01}\ket{01}+\alpha_{10}\ket{10}+\alpha_{11}\ket{11}
\end{equation}

Tout comme l'équation pour un seul qubit, $\alpha_{00}^2$ représente la probabilité que les deux qubits donneront le résultat 00 après la mesure. De même pour les trois autres états de base. Une fois de plus, les lois de la probabilité dictent que $\alpha_{00}^2+\alpha_{01}^2+\alpha_{10}^2+\alpha_{11}^2=1$.

## Intrication et Etats de Bell

Avoir simplement deux qubits en main ne suffit pas à les considérer comme étant intriqués. Les qubits doivent être dans des états spécifiques pour être considérés comme intriqués, ce qui signifie qu'il existe certaines valeurs de $\alpha$ qui impliquent l'intrication.

Par exemple, pour représenter l'état enchevêtré d'une sonnette de Whiskerton, $\alpha_{01}=\alpha_{10}=0$ et les deux autres, $\alpha_{00}$ et $\alpha_{11}$, doivent être égaux, avec la somme de leurs carrés égale à 1.

Décomposons cela. Dans une sonnette de Whiskerton, les billes deviennent de la même couleur après que la bille extérieure a été directement observée. Si les billes ne peuvent devenir que de la même couleur, alors seulement deux états possibles sont autorisés : $\ket{rouge, rouge}$ et $\ket{bleu, bleu}$. La première position dans chaque $\ket{}$ représente la bille extérieure, et la deuxième position représente la bille intérieure. L'état $\ket{rouge, bleu}$ est interdit et ne peut jamais se produire dans l'appareil de la sonnette, donc la probabilité qui lui est associée est nulle. Il en va de même pour $\ket{bleu, rouge}$.

Cela signifie que les seules probabilités non nulles sont celles associées à $\ket{rouge, rouge}$ et $\ket{bleu, bleu}$, et puisque les billes de Whiskerton ont une chance de 50-50 de devenir d'une couleur ou de l'autre, les deux probabilités doivent être égales.

Voici donc à quoi l'état ressemble :

\begin{equation}
\ket{\phi^+}=\frac{1}{\sqrt{2}}\ket{00}+\frac{1}{\sqrt{2}}\ket{11}
\label{eq:bellstate}
\end{equation}

Les billes sont dans ce que l'on appelle un "État de Bell"—nommé d'après le physicien John S. Bell, et *non pas* parce que c'est l'état des sonnettes à Whiskerton. L'équation ci-dessus est la représentation mathématique de cet État de Bell particulier, où $\phi^+$ est une convention de nommage.[^fn-nth-2]

[^fn-nth-2]: Voici à quoi ressemble l'état de Bell mathématiquement dans la *base computationnelle*, qui fait référence au type de mesure nécessaire pour 'voir' le résultat. Il existe différentes bases associées à différents types de mesures.

Comme vous pouvez le voir, il y a une probabilité égale pour que l'un ou l'autre des deux états de base $\ket{00}$ ou $\ket{11}$ se produise avant que le premier qubit ne soit mesuré. Mais lorsque le premier qubit devient soit $\ket{0}$, soit $\ket{1}$, alors le deuxième n'a d'autre choix que de suivre. De cette manière, les résultats sont corrélés et les qubits sont intriqués.

À ce stade, il est important de noter qu'il ne s'agit pas du seul état de Bell ; il en existe d'autres. Par exemple, l'un des autres états de Bell implique que le deuxième qubit devient toujours l'*opposé* de ce que devient le premier ! Mais ce n'est pas ainsi que les billes intriqués des sonnettes de Whiskerton se comportent.

Les paires de qubits qui se trouvent dans les états de Bell sont appelées paires EPR, d'après les physiciens Albert Einstein, Boris Podolsky et Nathan Rosen. Les paires EPR et l'intrication sont des ressources précieuses pour des applications théoriques et potentielles de l'informatique quantique, telles que la cryptographie quantique, le codage superdense et la téléportation quantique.[^fn-nth-3]

[^fn-nth-3]: La téléportation dans ce contexte n'est pas la téléportation que l'on trouve dans Star Trek. Nous prévoyons d'explorer cette application dans une future histoire !

## Note Rapide sur les Qubits Physiquement Intriqués
 
La construction physique de qubits intriqués en laboratoire dépend de ce que vous utilisez pour les qubits. Par exemple, deux photons d'une seule source, générés d'une manière spécifique, peuvent émerger intriqués. Il n'existe pas de « dispositif universel » d'intrication comme il y en a à Whiskerton. Et, plus précisément, personne n'appelle réellement ces sources des « intricateurs » ! Enfin, sauf les chats.

_____________________________


_____________________________


_____________________________


**[A Suivre : Ce N'est Pas Tout](https://quantum-kittens.github.io/posts/This-is-not-the-end/)**
 
________

## Code Qiskit

Vous pouvez simuler une sonnette de Whiskerton en utilisant le code suivant. En utilisant ce code, vous apprendrez à créer le circuit quantique correspondant à l'état de Bell.

 ```python
#Importation des librairies Qiskit nécessaires
from qiskit import QuantumCircuit, transpile
from qiskit.visualization import *
from qiskit import BasicAer

#Charge votre (vos) compte(s) IBM Quantum
#provider = IBMQ.load_account()


#Crée un Circuit d'Intrication de Sonnettes

doorbell_circuit = QuantumCircuit(2, 2) # Crée un circuit avec 2 qubits (des billes de Whiskerton) et deux bits classiques (pour enregistrer les résultats).

doorbell_circuit.h(0) # Ajoute une porte d'Hadamard au premier qubit.

doorbell_circuit.cx(0,1) # Ajout d'une porte CNOT avec le premier qubit comme contrôle et le deuxième qubit comme cible. La cible change d'état lorsque le contrôle est dans l'état 1.

doorbell_circuit.measure([0,1],[0,1]) # Ajoute les opérateurs de mesure (c'est l'équivalent pour un chat de regarder directement la bille extérieur).

doorbell_circuit.draw('mpl') # Affiche ce à quoi ressemble le circuit


```

Le code ci-dessus est également disponible en tant que notebook jupyter [ici](https://github.com/quantum-kittens/quantum-kittens.github.io/blob/main/jupyter_notebooks/QK_Chapter_3.ipynb).

En tant qu'exercice, exécutez ce circuit de façon similaire au circuit de la bille dans le [Chapitre 2](https://quantum-kittens.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/) !

*Note : Le code Qiskit fournit est open source, et n'est pas sous la license de Quantum Kittens.*
