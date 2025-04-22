---
title: 'Chapitre 4 Partie 2 - Commentaires - Portes Quantiques et Circuits'
math: true
---


Nous savons déjà que les bits sont les entités fondamentales que les ordinateurs classiques utilisent pour stocker et traiter l'information, et que les bits ne peuvent prendre qu'une seule valeur : 0 ou 1. Mais comment les bits *savent-ils* quelle valeur adopter ?

Nous disons aux bits quoi faire en leur fournissant des instructions. Lorsque nous utilisons un ordinateur, nous émettons en réalité des commandes qui se répercutent jusqu’aux composants informatiques fondamentaux, lesquels contrôlent les bits et déterminent s’ils valent 0 ou 1 à un instant donné.

Supposons que nous envoyions un message, "Joyeux anniversaire !", à un ami. Nous ouvrons notre application de messagerie, nous tapons chaque lettre, puis nous appuyons sur envoyer. Chaque étape consiste à donner des instructions à notre appareil. Ce sont des instructions de haut niveau que nous comprenons, comme "taper h" ou "appuyer sur entrée". Mais notre appareil informatique décompose chacune de ces instructions en commandes au niveau machine, et à l’échelle la plus fondamentale, ces instructions contrôlent et manipulent des chaînes de bits.

Ces instructions sont exécutées par des *portes logiques*, qui effectuent des opérations sur les bits. Différentes portes peuvent agir sur un ou plusieurs bits à la fois, chacune réalisant une opération spécifique. Combinées, elles produisent le résultat souhaité.

De la même manière, en informatique quantique, il existe des *portes quantiques* qui agissent sur les qubits.

## Portes Quantiques

Les portes quantiques sont le moyen par lequel nous contrôlons les qubits – elles manipulent les états quantiques des qubits. Cela signifie qu’elles modifient les probabilités des résultats que nous obtiendrions si nous mesurions les qubits.

In the Whiskertese marble analogy, a quantum gate changes how likely you are to see red or blue when you directly observe the marble.

Dans l’analogie des billes de Whiskerton, une porte quantique modifie la probabilité de voir du rouge ou du bleu lorsque nous observons directement la bille.

## Circuits Quantiques

Les instructions peuvent être formulées à l’aide de *circuits quantiques*. Un circuit quantique est un modèle représentant une séquence de portes quantiques, de mesures et d’autres actions appliquées à des qubits. Bien qu’il ne s’agisse pas d’un circuit physique à proprement parler, il illustre la manière dont les qubits seront manipulés.

Voici un exemple de ce à quoi ressemble un circuit quantique pour trois qubits :

![](/assets/imgs/ch4_3_qubit_circuit.png){: style="max-width: 500px"}

Ça ressemble un peu à une partition musicale, n’est-ce pas ? Tout comme une partition, on lit le circuit de gauche à droite. Chaque ligne horizontale représente un qubit. Les cases et symboles sur ces lignes sont des portes quantiques, et la case grise à la fin de chaque ligne représente une mesure. Remarquez que certaines portes quantiques s’étendent sur plusieurs lignes – ce sont des portes qui agissent sur plusieurs qubits en même temps.

Souvenez-vous, ce circuit quantique n’est qu’une représentation visuelle des instructions. Pensez-y comme à une abstraction de ce qui se passe dans le matériel physique, et non comme un schéma de circuits électroniques réels. Ces instructions forment ce qu’on appelle un *algorithme quantique*.

À Whiskerton, les chats mettent en œuvre des séquences de portes quantiques à travers la musique, manipulant les états de leurs billes. Ils savent que certaines notes de musique produisent des changements d’état spécifiques avec les billes.

> Si vous souhaitez plonger plus profondément dans les portes quantiques et les circuits d’un point de vue mathématique, continuez à lire ! Sinon, dirigez-vous vers la page suivante : [Ce n'est pas fini...](https://quantum-kittens.github.io/posts/This-is-not-the-end/)
{: .prompt-info }


_______

## Représentation Mathématique des Portes Quantiques

Dans le chapitre 2, nous avons appris qu'il est possible de représenter un état qubit arbitraire à l'aide de cette équation :

\begin{equation}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

où $\alpha_{0}$ et $\alpha_{1}$ sont des amplitudes de probabilité. Ces amplitudes de probabilité nous disent tout sur l'état du qubit. Lorsqu'une porte quantique modifie l'état, elle modifie ces valeurs de $\alpha$ (prononcées ‘alpha’).

Appelons notre porte quantique $G$. Lorsque nous appliquons $G$ à notre état initial $\ket{\psi}$, l'état change de la manière suivante :

\begin{equation} 
\alpha_{0}\ket{0}+\alpha_{1}\ket{1} \rightarrow \beta_{0}\ket{0}+\beta_{1}\ket{1}
\end{equation}

There's another helpful way to represent quantum states and gates if you know a bit of linear algebra. We can write the probability amplitudes as a column of numbers, or a *column vector* like so:

Il existe une autre façon bien utile de représenter les états et les portes quantiques si vous connaissez un peu d'algèbre linéaire. Nous pouvons écrire les amplitudes de probabilité sous forme de colonne de nombres, ou un *vecteur colonne* comme ceci :

\begin{equation} 
v_\psi = \begin{bmatrix} 
\alpha_0 \\\ 
\alpha_1 
\end{bmatrix} 
\end{equation}

Ce vecteur est appelé un *vecteur d'état*. De même, nous pouvons écrire n'importe quelle porte quantique à un seul qubit sous forme d'une petite grille de nombres (une matrice $2 \times 2$) :

\begin{equation} 
G = \begin{bmatrix} 
a & b \\\ 
c & d 
\end{bmatrix} 
\end{equation}

Vous pouvez ensuite utiliser la multiplication matricielle standard pour déterminer l'état résultant :

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

Examinons deux exemples spécifiques de portes couramment utilisées !

### Porte NOT

La porte quantique NOT est similaire à sa cousine classique. En informatique classique, une porte NOT inverse un bit, le passant de 0 à 1 ou de 1 à 0. La version quantique fait quelque chose de similaire : elle échange les amplitudes de probabilité pour $\ket{0}$ et $\ket{1}$. Cela signifie que si votre qubit avait plus de chances de donner 0 lorsqu'il était mesuré, après la porte NOT, il deviendra plus probable de donner 1, et inversement.

Voici ce que fait une porte NOT :


\begin{equation} 
\ket{0} \rightarrow \ket{1}
\end{equation}
\begin{equation} 
\ket{1} \rightarrow \ket{0}
\end{equation}
\begin{equation} 
\alpha_{0}\ket{0}+\alpha_{1}\ket{1} \rightarrow \alpha_{1}\ket{0}+\alpha_{0}\ket{1}
\end{equation}

Nous pouvons écrire la porte NOT sous cette forme de matrice (également appelée porte X ou porte Pauli X) :

\begin{equation} 
X = \begin{bmatrix} 
0 & 1 \\\ 
1 & 0 
\end{bmatrix} 
\end{equation}

Essayez de multiplier cette matrice vous-même avec ces trois états différents pour voir comment cela fonctionne :

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

### Porte Hadamard

Toutes les portes quantiques n'ont pas d'analogues classiques comme la porte NOT – en fait, la plupart n'en ont pas. La porte Hadamard est l'une de ces portes spécifiquement quantiques, et on peut dire qu'elle est l'une des plus importantes en informatique quantique. De nombreux algorithmes quantiques en dépendent pour initialiser les états des qubits. Qu'est-ce qui la rend si spéciale ? Lorsqu'elle est appliquée à $\ket{0}$ ou $\ket{1}$, elle crée une superposition de poids égaux.

Cela vous semble familier ? C'est comme les billes de Whiskerton qui sont par défaut dans une superposition de poids égaux entre le rouge et le bleu !

Voici ce que fait la porte Hadamard :

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

Ces valeurs $\frac{1}{\sqrt{2}}$ signifient qu'il y a une probabilité de 50-50 de mesurer soit 0, soit 1. Remarquez qu'il y a parfois un signe moins. Bien que cela ne change pas les probabilités, cela crée ce qu'on appelle la *phase*, que nous explorerons dans un futur chapitre. C'est comme donner à nos billes un type spécial de spin.

Voici la porte Hadamard sous forme de matrice :

\begin{equation} 
H = \frac{1}{\sqrt{2}}\begin{bmatrix} 
1 & 1 \\\ 
1 & -1 
\end{bmatrix} 
\end{equation}

Essayez de faire la multiplication matricielle vous-même pour voir comment elle crée ces transformations.

Une note importante : les états de superposition à un seul qubit de poids égaux sont tellement significatifs en informatique quantique qu'ils ont leurs propres symboles spéciaux :

\begin{align}
\ket{+}=\frac{1}{\sqrt{2}}\ket{0}+\frac{1}{\sqrt{2}}\ket{1}\\\
\ket{-}=\frac{1}{\sqrt{2}}\ket{0}-\frac{1}{\sqrt{2}}\ket{1}\\\
\end{align}


## Représentation Géométrique des Qubits

If you prefer a more visual mathematical representation, perhaps a geometric representation of a qubit state would be helpful. An arbitrary state $\psi$ can be written in terms of sines and cosines, such that the probability amplitudes are $\alpha_{0} =\cos{\theta}$ and $\alpha_{1} =\sin{\theta}$:

Si vous préférez une représentation mathématique plus visuelle, peut-être qu'une représentation géométrique de l'état d'un qubit serait utile. Un état arbitraire $\psi$ peut être écrit en termes de sinus et de cosinus, de sorte que les amplitudes de probabilité soient $\alpha_{0} = \cos{\theta}$ et $\alpha_{1} = \sin{\theta}$ :

\begin{equation}
\ket{\psi}=\cos{\theta}\ket{0}+\sin{\theta}\ket{1}
\end{equation}
This is a valid representation—remember that the sum of probabilities must always add up to 1[^fn-nth-1].
\begin{equation}
\alpha_{0}^2+\alpha_{1}^2=\cos^2{\theta}+\sin^2{\theta}=1
\end{equation}

[^fn-nth-1]: Il s'agit d'une identité trigonométrique fondamentale.

En conséquence, l'état arbitraire $\ket{\psi}$ peut être représenté visuellement sur un cercle unité (c'est-à-dire un cercle de rayon 1) comme ceci :


![](/assets/imgs/ch4_2D_geo_rep_psi.png){: style="max-width: 500px"}

Le vecteur vert est l'état arbitraire et les deux axes correspondent aux états de base $\ket{0}$ et $\ket{1}$.

Si l'angle $\theta$ est de 45 degrés, vous obtenez l'état $\ket{+}$ :

![](/assets/imgs/ch4_2D_geo_rep_plus.png){: style="max-width: 500px"}


Avec cette représentation, vous pouvez facilement penser à une porte quantique comme agissant sur un état de qubit, de sorte que le vecteur correspondant se déplace autour de ce cercle en fonction des changements dans $\theta$.

Il est important de noter que ce n'est *pas* une représentation complète d'un qubit, car elle ne prend pas en compte ce paramètre supplémentaire que j'ai appelé "phase" plus tôt. Lorsque nous aborderons la phase, vous rencontrerez une représentation plus complète en trois dimensions, appelée la *sphère de Bloch*.


## Exécuter des Circuits Quantiques

Vous comprenez maintenant que les portes quantiques manipulent les probabilités au sein d'un état quantique. Ainsi, une séquence de portes quantiques dans un circuit quantique ou un *algorithme quantique* manipule les probabilités des états. Ou, pour le dire autrement, les algorithmes quantiques manipulent les probabilités associées à chaque résultat possible.

Vous vous demandez peut-être : s'il y a des probabilités associées aux résultats, n'y a-t-il pas une chance d'obtenir un résultat incorrect ou indésirable ? Et vous avez raison !

C'est pourquoi, contrairement aux circuits classiques, nous exécutons des circuits quantiques plusieurs fois et recueillons les résultats sous forme de statistiques. Chaque fois que vous exécutez un circuit, cela s'appelle un *tir* et plus vous effectuez de tirages, plus vos résultats seront précis.

Regardons un circuit avec un seul qubit pour lequel, après l'application de certaines portes, il y a 4 % de chances d'obtenir 0 et 96 % de chances d'obtenir 1 lors de la mesure.

![](/assets/imgs/ch4_Luna_circuit.png){: style="max-width: 500px"}


> Quick disclaimer about the Chapter 4 story: If you’re wondering about the 10 cm distance rule, this is solely a whimsical storytelling device representing quantum measurements. In reality, quantum measurements occur through physical interactions that cause quantum states to settle into one of their definite basis states. Refer to [Chapter 2](https://quantum-kittens.github.io/posts/CHAPTER-2-Story-Schr%C3%B6dinger-Day/) for a description of quantum measurements.
{: .prompt-info }

Cela utilise la porte X montrée ci-dessus, ainsi qu'une autre porte appelée la porte Rotation X ($R_X$) avec un angle de : $\frac{\pi}{8}$ [^fn-nth-2].

[^fn-nth-2]: Cette porte $R_X$ fait tourner l'état du qubit autour de l'axe des x d'un angle de $\frac{\pi}{8}$. Elle introduit également une phase. Nous verrons plus tard une représentation visuelle de cette rotation.

Étant donné la probabilité élevée d'obtenir le résultat 1, si nous associons le bleu à 0 et le rouge à 1, nous avons l'une des représentations possibles du circuit quantique de Luna jouant "Joyeux anniversaire". Rappelez-vous qu'elle a manipulé la bille pour la rendre plus susceptible de devenir rouge après l'observation.

> Petite précision concernant l’histoire du Chapitre 4 : Si vous vous demandez à propos de la règle des 10 cm, il s'agit simplement d'un dispositif narratif fantaisiste représentant les mesures quantiques. En réalité, les mesures quantiques se produisent par des interactions physiques qui provoquent l'effondrement des états quantiques dans l’un de leurs états de base définis. Référez-vous au [Chapitre 2](https://quantum-kittens.github.io/posts/CHAPTER-2-Story-Schr%C3%B6dinger-Day/) pour une description des mesures quantiques.



_____________________________


_____________________________


_____________________________


**[A Suivre : Ce N'est Pas Fini...](https://quantum-kittens.github.io/posts/This-is-not-the-end/)**


## Code Qiskit

Si vous n'étiez pas familier avec les portes quantiques et les circuits avant ce chapitre, et que vous souhaitez essayer de les coder avec Qiskit, revenez aux sections Qiskit dans [Chapitre 2 Partie 2](https://quantum-kittens.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/) et [Chapitre 3 Partie 2](https://quantum-kittens.github.io/posts/CHAPTER-3-Part-2-Multiple-Qubits-Entanglement-and-Bell-States/) pour vous essayer à la programmation de circuits.

Sinon, essayez de coder le circuit "Joyeux anniversaire" de Luna comme un exercice !
