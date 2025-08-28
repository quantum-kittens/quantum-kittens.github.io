---
title: 'Bölüm 2 Kısım 2 - Açıklama - Kübitler, Süperpozisyon ve Ölçüm'
math: true
---



Klasik hesaplamanın ne olduğuna muhtemelen aşinasınızdır; neticede "hesaplama" denildiğinde çoğu insanın aklına bu gelir. Bahsedilen, bunu okumak için kullandığınız cihaz ve hatta laboratuvarlarda tutulan süper bilgisayarlar gibi elektronik aletler tarafından yapılan hesaplamalardır.

Derinlerde, klasik bilgisayarların temelinde bilgi, *bitler* tarafından taşınır: yalnızca iki değer veya *durumlardan* (0 veya 1) birine sahip olabilen tekil bilgi birimleri. Aynı şekilde, kuantum bilgisayarlar da kuantum bitleri ya da *kübitler* denilen temel hesaplama birimlerine sahiptirler. İlginç bir nokta: Bıyıkkent'in bilyeleri aslında kübitleri temsil ediyor!

## Kübit nedir?

Bir kübit kuantum hesaplamadaki en basit sistemdir, kuantum hesaplama için temel bileşendir. Fiziksel olarak, kuantum bilgisayarın kullandığı donanıma bağlı olarak kübitler, çeşitli farklı biçimlerde bulunabilirler. Ancak davranışsal olarak, aynı hareket ederler. Yani bir 'kübiti', klasik bir bitten farklı olarak ilginç bir şekilde davranan soyut bir matematiksel nesne olarak düşünebilirsiniz. Klasik bitler iki değerden birini alabilir, 0 ve 1, ancak bir kübit bunu ve daha fazlasını yapabilir:

> Kübitler, yalnızca 0 veya 1 durumlarında değil, aynı zamanda ikisinin *süperpozisyonunda* olma yeteneğine sahip soyut matematiksel nesnelerdir.
{: .prompt-tip MK}

## Kuantum Süperpozisyonu

Kuantum süperpozisyonu, klasik fizikte benzeri olmayan, muntazam bir kuantum fiziği olgusudur. Bunu bir kombinasyon olarak düşünebilirsiniz.

Klasik bitler yalnızca 0 veya 1 durumunda olabilir ve asla ikisinin bir kombinasyonu olamazken, kuantum durumları birleştirilebilir ve yine de geçerli durumlar olabilirler. Dolayısıyla bir kübitin durumu 0 *ve* 1'in bir kombinasyonu olabilir.

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

Matematiksel olarak, eğer genliklerin karesini alırsak, her bir temel duruma karşılık gelen olasılıkları elde ederiz. Yani, $\ket{\psi}$ durumundaki bir kübiti ölçerseniz, 0 durumunu $\alpha_{0}^2$ olasılıkla, veya 1 durumunu $\alpha_{1}^2$ olasılıkla elde edersiniz. [^fn-nth-3]

[^fn-nth-3]: Üst simge 2, bir "kare" belirtir, bu bir sayının kendisiyle olan çarpımına denir. Bu da, $\alpha_{0}^2=\alpha_{0}*\alpha_{0}$ olur.

Haklı olarak neden karelerin kullanıldığını merak ediyor olabilirsiniz. Bu bize genliklerin, $\alpha_{0}$ ve $\alpha_{1}$'in negatif olabileceklerini hatırlatan basit bir matematiksel kuraldır. Her bir genliğin karesi bir olasılıktır ve olasılıklar her zaman pozitiftir, tıpkı kareler gibi!

Bu, her kuantum durumunun bir kısıtlamaya tabi olduğu anlamına gelir. Olasılık teorisinin katı bir kuralı vardır: tüm olasılıkların toplamı 1 olmalıdır, yani *her zaman* $\alpha_{0}^2+\alpha_{1}^2=1$ olmalıdır.

Şimdi bir örnekle birlikte inceleyelim. Varsayalım ki, aşağıdaki durumda bir kübitimiz var:

\begin{equation}
\ket{\psi}=\sqrt{\frac{2}{3}}\ket{0}-\sqrt{\frac{1}{3}}\ket{1}
\end{equation}

Burada, $\alpha_{0}=\sqrt{\frac{2}{3}}$ yani ölçümden sonra 0 sonucuna ulaşma olasılığı $\frac{2}{3}$ olacaktır. Benzer şekilde $\alpha_{1}=-\sqrt{\frac{1}{3}}$, ve 1 sonucuna ulaşma olasılığı $\frac{1}{3}$ olacaktır. Yani, eğer bu durumda bir sürü kübitin varsa ve hepsini ölçersen, istatiksel olarak yaklaşık üçte biri 1 sonucunu verir. Genlik ne kadar büyükse, olasılık o kadar yüksektir ve ölçümden sonra kübitin ilişkili durumda bulunması daha olasıdır.[^fn-nth-4]

[^fn-nth-4]: Matematikçiler için not: burada $;mod(\alpha);$ ifadesine atıfta bulunuyoruz.

## İstatistik Üzerine Bir Not

Kübitlerle ilgili mesele, $\ket{\psi}$ gibi rastgele bir durumda $\alpha_{0}$ ve $\alpha_{1}$ katsayılarını ölçüm yaparak belirleyemezsiniz—-$\alpha$ değerlerinin tam olarak ne olduklarını bilmenin yolu ya bu durumu kendiniz yaratmış olmanızdır ya da onu yaratan kişiyi tanıyor olmanızdır. Bunun sebebi ölçümün her zaman tek bir sonuç vermesidir:0 ya da 1, bu nedenle hiçbir ölçüm $\alpha$'ların bilgisine yol açamaz. Durumu bir başkası yaratmışsa, onlardan binlerce özdeş durumda kübit isteyebilir ve binlerce ölçüm yaptıktan sonra istatistiksel olarak genlikleri ve dolayısıyla durumun olasılıklarını çözümleyebilirsiniz. [^fn-nth-5]

[^fn-nth-5]: Bu tam olarak kuantum devrelerinin birçok kez çalışmasının sebebidir: istatistik toplamak. Kuantum devreleri kapı dizileri, ölçümler ve buna benzer başka öğeler içeren kuantum hesaplama modelleridir.

Yine de kübit durumlarının kullanışlı olması için $\alpha$'ların ne olduğunu bilmenize gerek yoktur. Kübit durumunun güzelliği, ölçümden önce kuantum kapılarındaki $\alpha_{0}$ ve $\alpha_{1}$ değerlerinin değiştirilebilmesinde ve manipüle edilebilmesinde yatar. Eğer istenilen çıktı 0 ise, o zaman algoritma, değerine bakılmaksızın $\alpha_{0}$'ın değerini yükseltme amacıyla tasarlanabilir. Eğer $\alpha_{0} = 1$ ise sonucun 0 olması kesindir.

## Fiziksel Kübitler

Önceden belirtilidiği gibi, kübit durumları matematiksel yapılardır; bu da onlarla, kullanılan fiziksel sistem hakkında bir açıklama yapmadan matematiksel olarak algoritmalar ve benzeri şeyler geliştirmek için çalışmayı kolaylaştırır. Bu önemlidir, çünkü kübit durumlarını laboratuvarda ister elektron spinlerini, ister fotonların kutuplaşmış durumlarını ya da başka bir şey, fiziksel olarak inşa etmeniz fark etmez.

Elektron ve fotonların ne olduklarını bilmiyor musunuz? Hadi kısaca konudan sapalım:

>Elektron, negatif yüklü bir atom altı parçacıktır. Ayrıntıya girmeden, "spin(dönüş)" adı verilen bir özelliğe sahiptir. Elektronun spinin $+\frac{1}{2}$ ya da $-\frac{1}{2}$ olduğunu söylemek yeterlidir, bu da matematiksel olarak $\ket{0}$ ve $\ket{1}$ durumları ile gösterilebilir.
{: .prompt-info }

>Foton, görünür ışık da dahil olmak üzere, elektromanyetik radyasyonun yapı taşıdır. Gördüğünüz her şey, retinanıza çarpan bu fotonlar sayesindedir. Fotonlar *polarize* olduklarında, tüm yönler yerine belirli bir yönde titreşmeye başlarlar. Kübitler açısından, yatay yöndeki polarizasyonun $\ket{0}$ ile temsil edildiğini ve dikey yöndeki polarizasyonun da $\ket{1}$ ile temsil edildiğini varsayalım. İkisinin süperpozisyonu mümkündür ve fotonun dikey ve yatay yönleri arasında bir yönde titreşmesine karşılık gelir, bu tıpkı bir pusulada Güney ve Doğu arasında yer alan Güneydoğu'ya benzer.
{: .prompt-info }

Kübit durumlarıyla ilgili bir başka önemli bilgi de kararlı olmamalarıdır. Kübitin çevresindeki küçük bozulmalar onun $\ket{0}$ ya da $\ket{1}$ durumuna indirgenmesine yol açabilir: sıcaklık, titreşim vb. bozulmalar.[^fn-nth-6] Dahası bu bozulmalar bile kararsızdır; bir süre sonra kübit süperpozisyona geri dönebilir. İşte durumların bu minik çekişmesi, kübitlerin laboratuvarda manipüle edilmesini zorlaştırır--Bıyıkkent kedilerini merakta tutan şey de budur!

[^fn-nth-6]: Kuantum durumlarının bu hassaslığı, kararlı, mükemmel fiziksel kübitler ve çok sayıda kübit içeren büyük cihazların üretilmesine engel olan şeylerden biridir. Ancak bu, fazlaca umut vaad edici ilerlemelere sahip, heyecan veren bir araştırma alanıdır. 

## Schrödinger'in Kedisi

Bu konu bizi Blade'in sim makinesiyle birlikte içinde bulunduğu kutuya götürüyor. Bulunduğu durum, fizikçi Erwin Schrödinger'in 1935'te yaptığı bir düşünce deneyine bir tür saygı duruşudur.[^fn-nth-7].

[^fn-nth-7]: Schrödinger, Erwin (November 1935). "Die gegenwärtige Situation in der Quantenmechanik (Kuantum mekaniğindeki mevcut durum)". Naturwissenschaften. 23 (48): 807-812.

Kübitler, iki temel duruma sahip iki-seviyeli sistemlerdir, ama daha fazla durum içeren diğer kuantum parçacıkları ve sistemleri de vardır. Ancak tüm bu sistemler, kübitler ve ötesi, aynı kurala uymaktadır: ölçüm yapıldığında sonuç, tüm olasılıklardan yalnızca biridir.

Kimse bunun neden gerçekleştiğini bilmiyor. Olası açıklamalardan bir tanesi, ölçme eyleminin kendisinin, tüm olasılıkları tek bir olasılıkta birleştirdiğini belirten quantum mekaniğinin Kopenhag yorumudur. 1935'te fizikçi Erwin Schrödinger, bu yoruma karşı bir itiraz olarak ünlü düşünce deneyini özetleyen bir makale yayınladı, mikroskobik düzeydeki kuantum etkilerinin günlük, makroskobik bir nesneyle varsayımsal olarak genelleştirdi: bir kedi.

Düşünce deneyinin aslında, kübit yerine(ya da bir Bıyıkkent bilyesi) radyoaktif bir madde kullanıldı. Radyoaktif maddeler olasılıklara göre bozunabilirdi, tıpkı bir kübitin olasılıklara göre belirli bir duruma indirgenebilmesi gibi. 

Bir kedi, bir şişe zehire bağlı radyoaktif bir maddeyle dolu bir kutunun içine koyulur. Eğer atomların biri bozunursa, şişe çatlar ve kediyi zehirler. Böylece, kedinin durumu, en az bir atomun bozunma olasılığıyla yönetilen zehir sistemiyle bağlantılı hale gelir. Böylece kutu açılmadan önce, kedi hem ölü hem diri şeklinde değerlendirilir, çünkü olasılıkların her biri mümkündür. Yani, kedinin gerçekliği, kutunun açılışından önce belirsizdir.

Schrödinger bunun "saçma bir durum" olduğunu ve birinin kutu açılmadan önce kedinin ölü ve dirinin süperpozisyonunda olduğuna gerçekten inanılamayacağını savur. Tabii ki haklı. Bu senaryo *tamamen* kuantum olarak değerlendirilemezdi. Kedi bir kuantum parçacığı değildi bir kere. Yani kedi gerçekten ölü ve dirinin süperpozisyonunda olmasa da, düşünce deneyi en azından olasılıksal sistemin altını çiziyordu.

Bu düşünce deneyi, popüler kültürde kuantum olgusunun en çok tanınan ikonografilerinden biri haline geldi ve doğal olarak Bıyıkkent'te de yerini buldu. Sim ile tabii ki, böylesine şirin bir kasabada kasvetli olmanın bir anlamı yok. Schrödinger'in gerçekten kedileri zehirlemediğinin altını çizelim--sadece düşündü!

Şimdi, bu düşünce deneyinin bir ilgi çekici yanı daha var: kedinin durumunun radyoaktif maddenin durumu ile *dolanık* hale geldiğini söyleyebiliriz.

Kuantum dolanıklık aslında bir sonraki durağımız! Hadi başlayalım: **[Sonraki: Bölüm 3 - Hikaye - Kapı Zilleri](https://quantum-kittens.github.io/posts/CHAPTER-3-Story-Doorbells/)**

_____________________________


_____________________________


_____________________________




## Qiskit Kodu

Bu bölüm, kuantum bilgisayarları programlamak için IBM Quantum'un açık kaynaklı Python çerçevesi(framework) olan Qiskit'i kullanmaya başlamak isteyenler içindir.

Bu ek Qiskit kodunu kullanarak bir Whiskerton bilyesini simüle edebilirsiniz. Bu kod, tek bir kübitle bir kuantum devresi oluşturma ve çalıştırma konusunda size yol gösterir.

Bu kodu iki şekilde çalıştırabilirsiniz:

- Bulutta: bulut tabanlı bir araç kullanmayı seçebilirsiniz [Google Colab](https://colab.research.google.com/) veya [qBraid](https://www.qbraid.com/). 
- Yerel olarak: [Qiskit](https://qiskit.org/) kurup kodu yerel cihazınızda çalıştırabilirsiniz.

Daha fazla kurulum ayrıntısı için bu blog gönderisine bakabilirsiniz: [
Explore newly recommended notebook environments for Qiskit](https://www.ibm.com/quantum/blog/qiskit-notebook-environments)

Aşağıdaki kod aynı zamanda jupyter notebook için de mevcuttur [buradan](https://github.com/quantum-kittens/quantum-kittens.github.io/blob/main/jupyter_notebooks/QK_Chapter_2.ipynb).

Kasım 2024 not: bu kod Qiskit 1.0 için güncellenmiştir. Eğer daha önce Qiskit'in daha erken bir versiyonunu kullandıysanız, bu blog gönderisi sizin için yardımcı olabilir: [Best practices for transitioning to Qiskit SDK v1.0](https://www.ibm.com/quantum/blog/transition-to-1)





 ```python
# Görselleştirme için yararlı bazı isteğe bağlı bağımlılıklarla birlikte Qiskit'i yükleyin 
# Qiskit henüz yüklü değilse aşağıdaki talimatın yorum satırını kaldırın

#pip install'qiskit[visualization]'

# Eğer Qiskit Runtime Service hâlâ yüklü değilse, aşağıdaki talimatın yorum satırını kaldırarak yükleyin

#pip install qiskit-ibm-runtime

# Eğer Qiskit Aer Simülatör hâlâ yüklü değilse, aşağıdaki talimatın yorum satırını kaldırarak yükleyin

#pip install qiskit-aer

# Gerekli Qiskit kütüphanelerini içe aktarın

from qiskit import QuantumCircuit

#Bilye Devresi Oluşturma

bilye_devresi = QuantumCircuit(1, 1) # bir kübit ekleyin (Bıyıkket bilyesi) ve bir klasik bit (ölçüm sonucunu saklamak için)

bilye_devresi.h(0) # kübite H-kapısı veya Hadamard kapısı ekleyin (bu bilyeyi süperpozisyona sokan kuantum kapısı)

bilye_devresi.measure(0,0) # bir ölçüm operatörü ekleyin (bu kedinin doğrudan bilyeye bakmasına denktir)

bilye_devresi.draw('mpl') # devrenin nasıl göründüğüne bakın
```



 ```python

 # Devreyi simülatörde çalıştırmak için gerekli Qiskit kütüphanelerini içeri aktarın

from qiskit.transpiler.preset_passmanagers import generate_preset_pass_manager
from qiskit_ibm_runtime import QiskitRuntimeService
from qiskit_aer import AerSimulator
from qiskit_ibm_runtime import SamplerV2 as Sampler
from qiskit.visualization import plot_histogram


#Bilye Devresini Çalıştırın,
#Bu bilyenin kırmızıya mı maviye mi döndüğünü görmek için
bilye_durumu = {'1': 'kirmizi', '0': 'mavi'}

aer_sim = AerSimulator() # Bunu çalıştırmak için kuantum bilgisayar tanımla. Bu durumda bir simülatör kullanıyoruz, gerçek bir cihaz değil.
pm = generate_preset_pass_manager(backend=aer_sim, optimization_level=1) 
bilye_devresi_mi = pm.run(bilye_devresi) # Bu satır ve aşağısındaki satır devreyi seçilen cihazda çuygulanmaya hazırlamak için kullanılıyor. Daha fazla teknik detay için, lütfen bu link ile devam edin: https://docs.quantum.ibm.com/api/qiskit/transpiler#transpiler

# sonuçları çekme ve yazdırma:
sampler = Sampler(mode=aer_sim)

result = sampler.run([bilye_devresi_mi], shots=1000).result() # İstatistik toplamak için devreyi simülatörde 1000 kez çalıştır.
counts = result[0].data.c.get_counts()

ans = str(max(counts, key=counts.get))

print('Bilye ' + bilye_durumu[ans] + 'renktir.') # Bu çıktı, en yüksek sayıma sahip olanı verir.



```

```python

# İstatistik ve histogram grafiğini inceleyelim

print("Sayım şeklinde sonuçların:", counts)
print("Dolayısıyla, 1000 atışta, " + str(counts['0']) + " kez mavi renk bilye elde ettin ve " + str(counts['1']) + " kez kırmızı renk bilye elde ettin.")

plot_histogram(counts)

```

```python
# Devreyi gerçek bir cihazda çalıştırmak için aşağıdaki kodu kullanabilirsiniz

#from qiskit_ibm_runtime import QiskitRuntimeService
 
#service = QiskitRuntimeService(channel="ibm_quantum", token="<insert your token here>")
```



*Not: Kullanılan Qiskit kodu açık kaynaklıdır, ve Quantum Kittens'ın telif hakkı kapsamına girmez.*
