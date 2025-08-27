---
title: 'Bölüm 2 Kısım 2 - Açıklama - Kübitler, Süperpozisyon ve Ölçüm'
math: true
---



Klasik hesaplamanın ne olduğuna muhtemelen aşinasınızdır; neticede "hesaplama" denildiğinde çoğu insanın aklına bu gelir. Bahsedilen, bunu okumak için kullandığınız cihaz ve hatta laboratuvarlarda tutulan süper bilgisayarlar gibi elektronik aletler tarafından yapılan hesaplamalardır.

Derinlerde, klasik bilgisayarların temelinde bilgi, *bitler* tarafından taşınır: yalnızca iki değer veya *durumlardan* (0 veya 1) birine sahip olabilen tekil bilgi birimleri. Aynı şekilde, kuantum bilgisayarlar da kuantum bitleri ya da *kübitler* denilen temel hesaplama birimlerine sahiptirler. İlginç bir nokta: Bıyıkkent'in bilyeleri aslında kübitleri temsil ediyor!

## Kübit nedir?

Bir kübit kuantum hesaplamadaki en basit sistemdir, kuantum hesaplama için temel bileşendir. Fiziksel olarak, kuantum bilgisayarın kullandığı donanıma bağlı olarak kübitler, çeşitli farklı biçimlerde bulunabilirler. Ancak davranışsal olarak, aynı hareket ederler. Yani bir 'kübit'i, klasik bir bitten farklı olarak ilginç bir şekilde davranan soyut bir matematiksel nesne olarak düşünebilirsiniz. Klasik bitler iki değerden birini alabilir, 0 ve 1, ancak bir kübit bunu ve daha fazlasını yapabilir:

> Kübitler, yalnızca 0 veya 1 durumlarında değil, aynı zamanda ikisinin *süperpozisyonunda1* olma yeteneğine sahip soyut matematiksel nesnelerdir.
{: .prompt-tip MK}

## Kuantum Süperpozisyonu

Kuantum süperpozisyonu, klasik fizikte benzeri olmayan, muntazam bir kuantum fiziği olgusudur. Bunu bir kombinasyon olarak düşünebilirsiniz.

Klasik bitler yalnızca 0 veya 1 durumunda olabilir ve asla ikisinin bir kombinasyonu olamazken, kuantum durumları birleştirilebilir ve yine de geçerli durumlar olabilir. Dolayısıyla bir kübitin durumu 0 *ve* 1'in bir kombinasyonu olabilir.

![](/assets/imgs/Marble_Animation.png){: style="max-width: 150px" .left} Bıyıkkent'te bilyeler, varsayılan olarak böyle bir süperpozisyon (üst üste binme) durumundadır: kırmızı ve mavi renklerin eşit ağırlıkta bir kombinasyonu şeklinde. Bu renkleri boya renkleri olarak düşünmek yanlış olur. Günlük hayatında, klasik deneyimde, eğer kırmızı ve mavi renk boyayı birleştirirsen, mor renk boya elde edersin. Ancak Bıyıkkent bilyeleri mor renk değildir; bir kedi bilyeyi gözlemledikten sonra bilye, her biri için yüzde elli ihtimalle ya kırmızı renge ya da mavi renge dönüşür. Eğer mor renk boyanız varsa kırmızı ve mavi renkleri geri elde etme şansınız yoktur!

Bu harika olgudan yararlanabilmek, kuantum hesaplamanın klasik hesaplamadan farklılaştığı noktalardan biridir. Klasik bir bilgisayarda, eğer bir bit üzerinde bir işlem gerçekleştirirseniz, tek seferde 0 ya da 1 üzerinde bir işlem gerçekleştirmiş olursunuz. Eğer ikisi üzerinde de bir işlem gerçekleştirmeniz gerekiyorsa, bunu ardışık olarak iki seferde yapmanız gerekir.

Ama süperpozisyondan yararlanarak, bir kuantum bilgisayarda bu işlemi aynı anda 0 ve 1 üzerinde gerçekleştirebilirsiniz. Bunu birçok kübite ölçeklendirecek olursak, potansiyel olarak hızlanmalara veya bellek kapasitesinde artışa veya diğer iyileştirmelere nasıl yol açabileceğini hayal edebilirsiniz.

## Ölçümler

Bilyelerin doğrudan bakıldığında yüzde elli ihtimalle kırmızı veya mavi olma ihtimalinin olduğunu gördünüz. Bir kedinin bir bilyeyi gözlemlemesi, kübitin durumunun ölçülmesinde, kırmızı renk bilyenin 1'i ve mavi renk bilyenin 0'ı temsil etmesiyle ilgili bir metafor. Gerçek hayatta ölçümler, laboratuvarda fiziksel büyüklüklerin ölçülmesiyle yapılır.

Ölçüm esasen kübite hangi durumda olduğunun sorulmasıdır, ancak dikkat edilmesi gereken bir şey: ölçüm davranışı bir kübitin 0 ya da 1 durumlarından birine yerleşmesini sağlar, böylece yalnızca 0 ya da 1 sonucunu elde edebilirsiniz. Ancak her bir olası çıktı için (0 ve 1) tanımlanmış bir olasılık vardır.

Olasılıklar hakkında önceden her şeyi bilseniz bile--yani, ölçümden önce kübitin süperpozisyon durumunu tam olarak bilseniz bile--ölçümün sonucunu tahmin edemezsiniz.

Esasen:

> Bir kuantum sisteminin durumu hakkında her şeyi bilseniz bile, *yine de* rastgele davranabilir.
{: .prompt-tip }

Örneğin, bir Bıyıkkent bilyesi hakkında her şeyi biliyorsunuz: eşit ağırlıklı(yarı-yarıya) bir süperpozisyonda. Ancak, ölçümden sonra, kırmızı bilyede mi yoksa mavi bilyede mi sonlanacağını bilmiyoruz. Bu kısım rastgele!

Kuantum fiziği olasılıksal, yani bu *belirsizlik* var demek. Bir ölçüm, sistemi belirsizlikten belirginliğe taşır.

İlk bakışta kuantum süperpozisyonunun faydası, çıktı olarak klasik bitlerden farklı olmaksızın 0'lar ve 1'ler elde edildiğinden ötürü, yok oluyormuş gibi görünebilir. İşte tam bu noktada kuantum hesaplama algoritmaları devreye girer.

Algoritma temel olarak, istenilen sonuçları elde etmek için gerçekleştirilen bir dizi işleme denir. Bir kuantum hesaplama algoritmasının yaptığı şey ise olasılıkları manipüle etmektir, istenilen sonuca ait olasılığı artırıp diğerlerini azaltmak. [^footnote] Bu şekilde, istenilen duruma ilişkin olasılık 1'e ulaşırsa, o sonuç garanti altına alınmış olur, yani davranış artık rastgele değildir.

[^footnote]: Kuantum işlemleri, kuantum devrelerinin yapı taşı olan ve geleneksel dijital devrelerdeki klasik mantık kapılarıyla benzerlik gösteren *kuantum kapıları* adı verilen mantık işlemlerinin uygulanmasıyla gerçekleştirilir.

Şimdi kübitler, kuantum süperpozisyonu ve ölçümler hakkında genel bir bakışa sahip olduğunuza göre, Bıyıkkent bilyelerinin arkasındaki fiziği biliyorsunuz.

>Daha derin kavramları öğrenmek ve Blade'in çıkmazının Schrödinger'in kedisiyle nasıl alakalı olduğunu görmek isterseniz, okumaya devam edin! Aksi halde, yeni hikaye ile devam  edebilirsiniz: [Bölüm 3 - Hikaye - Kapı Zilleri](https://quantum-kittens.github.io/posts/CHAPTER-3-Story-Doorbells/)
{: .prompt-info }
_______

## Bir Kübit Durumunun Matematiksel Gösterimi

Kuantum durumları matematiksel olarak *Dirac gösterimi* olarak bilinen ve *ket* adı verilen bir şeyi kullanan bir gösterimle temsil edilir: $\ket{}$[^fn-nth-1].

[^fn-nth-1]: Ket, belirli özelliklere sahip matematiksel bir nesneyi ifade eder ve buna *vektör* denir. Bir kübit bir vektör olarak düşünülebilir. İki vektör birleştirilerek yeni bir vektör oluşturulabilir. Ancak bu metni okumak için vektörler hakkında bilgi sahibi olmanıza gerek yok.

Keyfi bir kübit durumu bu şekilde temsil edilir[^fn-nth-2]:

\begin{equation}
\label{eq:qubit}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

[^fn-nth-2]: Uyarı: Bu denklem bir kübitin tam gösterimi değildir; hesaplama için yararlı olabilecek 'faz' adı verilen bir serbestlik derecesi vardır ancak bu metnin kapsamı dışındadır.

Yunan harfi $\psi$, "sī" şeklinde okunur, bir durumun sembolik gösterimidir. $\ket{}$ sembolü yazılır ama okunmaz. Kübiti belirtirken, $\ket{\psi}$ 'yi denklemde tanımladıktan sonra, "Psi durumunda bir kübitim var" diyebilirsiniz ya da "$\ket{\psi}$ durumunda bir kübitim var" yazabilirsiniz.

Dikkat ederseniz ketin içerisindeki tek şey $\psi$ değildir. Denklemde 0 ve 1 durumlarının temsili, $\ket{0}$ ve $\ket{1}$ de bulunur. Bunlar kübitlerin *temel durumları* olarak adlandırılır; yani bir kübitin ölçümden sonra indirgenebileceği olası durumlar, tıpkı Bıyıkkent bilyelerinin kırmızı ve maviye indirgenebilecekleri gibi.

Artı işareti bir kombinasyon olduğunu belirtiyor, ya da süperpozisyon. $\alpha_{0}$ ve $\alpha_{1}$ parametrelerine *genlikler* deniliyor, ve bunlar bize kübitin ölçümden sonra $\ket{0}$ durumunda ya da $\ket{1}$ durumunda olmaya ne kadar yatkın olduğunu bildiriyor. Buradaki $\alpha$ ile Yunan harfi olan alpha belirtiliyor.

Matematiksel olarak, eğer genliklerin karesini alırsak, her bir temel duruma karşılık gelen olasılıkları elde ederiz. Yani, $\ket{\psi}$ durumundaki bir kübiti ölçerseniz, 0 durumunu $\alpha_{0}^2$ olasılıkla, veya 1 durumunu $\alpha_{1}^2$ olasılıkla edersiniz. [^fn-nth-3]

[^fn-nth-3]: Üst simge 2, bir "kare" belirtir, bu bir sayının kendisiyle olan çarpımına denir. Bu da, $\alpha_{0}^2=\alpha_{0}*\alpha_{0}$ olur.

Haklı olarak neden karelerin kullanıldığını merak ediyor olabilirsin. Bu bize genliklerin, $\alpha_{0}$ ve $\alpha_{1}$ negatif olabileceklerini hatırlatan basit bir matematiksel kuraldır. Her bir genliğin karesi bir olasılıktır ve olasılıklar her zaman pozitiftir, tıpkı kareler gibi!

Bu, her kuantum durumunun bir kısıtlamaya tabi olduğu anlamına gelir. Olasılık teorisinin katı bir kuralı vardır: tüm olasılıkların toplamı 1 olmalıdır, yani *her zaman* $\alpha_{0}^2+\alpha_{1}^2=1$ olmalıdır.

Şimdi bir örnekle birlikte inceleyelim. Varsayalım ki, aşağıdaki durumda bir kübitimiz var:

$\begin{equation}
\ket{\psi}=\sqrt{\frac{2}{3}}\ket{0}-\sqrt{\frac{1}{3}}\ket{1}
\end{equation}$

Burada, $\alpha_{0}=\sqrt{\frac{2}{3}}$ yani ölçümden sonra 0 sonucuna ulaşma olasılığı $\frac{2}{3}$ olacaktır. Benzer şekilde $\alpha_{1}=-\sqrt{\frac{1}{3}}$, ve 1 sonucuna ulaşma olasılığı $\frac{1}{3}$ olacaktır. Yani, eğer bu durumda bir sürü kübitin varsa ve hepsini ölçersen, istatiksel olarak yaklaşık üçte biri 1 sonucunu verir. Genlik ne kadar büyükse, olasılık o kadar yüksektir ve ölçümden sonra kübitin ilişkili durumda bulunması daha olasıdır.[^fn-nth-4]

[^fn-nth-4]: Matematikçiler için not: burada $;mod(\alpha);$ ifadesine atıfta bulunuyoruz.

## İstatistik Üzerine Bir Not

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
