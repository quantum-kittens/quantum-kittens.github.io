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

İşin can alıcı noktası şu ki, rastgele uygulanan eski tip bir ölçümün işe yaramayacağıdır, ve evet başka *tür* ölçümler de vardır! Çeşitli ölçüm türleri konumuz dışında ama şunu söylemek yeterli, sen ve senden çok uzakta yaşayan bir arkadaşın dolanık bir çift paylaşıyorsanız, o zaman senin parçacığına uyguladığın ölçüm türünü bir şekilde arkadaşına iletmen gerekir. Arkadaşın hangi ölçüm türünü uygulayacağından bihaberse, beklenen sonucu 'göremez'. Yani telefon görüşmesi gibi başka bir yolla bir şekilde iletişimde olmanız gerekir. Ki...bu da ışıktan daha hızlı olamaz.

>Kuantum dolanıklığını daha detaylı incelemek isterseniz, okumaya devam edin. Aksi takdirde, yeni sayfaya geçelim: [Karton Kutu Kimin Olacak?](https://quantum-kittens.github.io/posts/Who-Gets-the-Cardboard-Box/).
{: .prompt-info }

_______

## Birden Fazla Kübit İçeren Durumların Matematiksel Gösterimi

Birden fazla kübit içeren durumlar, tek kübit içeren durumlara benzer bir gösterime sahiptir. Bıyıkkent kapı zilleri iki kübite sahip olduğundan biz de iki kübitli durumlara odaklanacağız ama gösterim daha fazla sayıda kübit için de geçerlidir.


[Bölüm 2](https://quantum-kittens.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/)'de verilen keyfi, tek kübit durumu için olan denklemi hatırlayalım:


\begin{equation}
\ket{\psi}=\alpha_{0}\ket{0}+\alpha_{1}\ket{1}
\end{equation}

Bu denklemde, temel durumlar klasik bir bitin sahip olabileceği iki değere benzemektedir: 0 ve 1. Ve bir kübit, iki temel(baz) durumun süperpozisyonunda bulunabilir. 

İki kübitlik bir durumun nasıl gösterildiğini anlamak için, iki klasik bitin tüm olası değerlerini inceleyelim. Birleştirilmiş, iki bit, bu dört değerden birini alabilir: 00, 01, 10, ya da 11. Tek kübitlik durumda olduğu gibi, bu dört değer de dört temel duruma karşılık gelir. İki kübit, bu dört durumdan birinde ya da bu durumların süperpozisyonunda olabilir! Dolayısıyla, keyfi iki kübitlik bir durum şu denklem ile gösterilebilir:

\begin{equation}
\ket{\psi}=\alpha_{00}\ket{00}+\alpha_{01}\ket{01}+\alpha_{10}\ket{10}+\alpha_{11}\ket{11}
\end{equation}

Tıpkı tek kübit için olan denklem gibi $\alpha_{00}^2$, iki kübitin ölçümden sonra 00 çıktısını getirmesinin olasığını gösterir. Bu, diğer üç temel durum için benzerdir. Bir kez daha olasılık yasaları $\alpha_{00}^2+\alpha_{01}^2+\alpha_{10}^2+\alpha_{11}^2=1$ olmasını gerektirir.

## Dolanıklık ve Bell Durumları

Elinizde sadece iki kübit olması, bunların dolanık olduğunu düşünmeniz için yeterli değildir. Kübitlerin dolanık olduğunu söylemek için özel durumlarda bulunmaları gerekir, bu da dolanıklığı gerektiren belirli $\alpha$ durumları olduğu anlamına gelir.

Örneğin, Bıyıkkent'in kapı zillerininin dolanık durumunu temsil etmek için $\alpha_{01}=\alpha_{10}=0 ile diğer ikisinin $\alpha_{00}$ ve $\alpha_{11}$ karelerinin toplamının 1'e eşit olması gerekir.

Hadi bunu adım adım inceleyelim. Bir Bıyıkkent kapı zilinde bilyeler, dışarıdaki bilye doğrudan gözlemlendiğinde (bakıldığında) aynı renk olurlar. Eğer ki bilyeler yalnızca aynı renk olabiliyorsa o zaman yalnızca iki olası durum vardır: $\ket{kırmızı, kırmızı}$ and $\ket{mavi, mavi}$. Her iki $\ket{}$'te de birinci değerler dışarıdaki bilyeyi temsil eder, ve ikinci değerler içerideki bilyeyi temsil eder. $\ket{kırmızı, mavi}$ durumu yasaktır ve kapı zili aparatında asla gerçekleşemez, dolayısıyla bu duruma tanımlanan olasılık sıfırdır. Aynısı $\ket{mavi, kırmızı}$ için de geçerlidir.

Bu yalnızca sıfır-olmayan olasılıkların $\ket{kırmızı, kırmızı}$ ile $\ket{mavi, mavi}$'ye tanımlandığı anlamına gelir ve Bıyıkkent bilyelerinin renklerden birine dönme şansı yarı-yarıya olduğundan, olasılıklar eşit olmalıdır.

Yani durumlar böyle görünmektedir:


\begin{equation}
\ket{\phi^+}=\frac{1}{\sqrt{2}}\ket{00}+\frac{1}{\sqrt{2}}\ket{11}
\label{eq:bellstate}
\end{equation}

Bilyeler, "Bell durumundadır" bu durum Bıyıkkent'in kapı zillerinden('zil' kelimesinin İngilizce karşılığı 'bell' dir) dolayı *değil*, fizikçi John S. Bell'in adından dolayı "Bell durumu" olarak isimlendirilmiştir. Yukarıdaki denklem, bu özel Bell durumunun matematiksel olarak nasıl göründüğünü gösterir; burada $\phi^+$ bir adlandırma kuralıdır.[^fn-nth-2]

[^fn-nth-2]: Bu, Bell durumunun *hesaplama temelinde(bazında)* matematiksel olarak nasıl göründüğüdür; ki bu da sonucu ‘görmek’ için gereken ölçüm türüne bir göndermedir. Farklı ölçüm türleriyle ilişkili farklı bazlar mevcuttur.

Gördüğünüz üzere, ilk kübit ölçülmeden önce, iki baz durumundan $\ket{00},\ket{11}$ herhangi birinin oluşma olasılığı eşittir. Ama ne zaman ilk kübit $\ket{0}$ ya da $\ket{1}$ olursa, o zaman ikinci kübitin diğerini takip etmekten başka seçeneği yoktur. Bu şekilde sonuçlar birbirleriyle ilişkilenir (korele olur) ve kübitler dolanık hale gelir.

Bu noktada şunu belirtmek önemli ki tek Bell durumu bu değil, başka Bell durumları da mevcuttur. Örneğin, diğer Bell durumlarından birinde ikinci kübit her zaman birincisinin aldığı değerin *zıttı* olur! Ancak, Bıyıkkent'in kapı zillerinin dolanık bilyelerinin davranışları böyle değildir.

Bell durumlarındaki ikili-kübit çiftleri, fizikçiler Albert Einstein, Boris Podolsky, ve Nathan Rosen'a ithafen, ERP çiftleri olarak adlandırılmışlardır. ERP çiftleri ve dolanıklık, teorik fizik ile kuantum kriptografi, süper yoğun kodlama ve kuantum ışınlanma(teleportasyon) gibi potansiyel kuantum hesaplama uygulamaları için değerli kaynaklardır. [^fn-nth-3]

[^fn-nth-3]: Burada belirtilen ışınlanma, Star Trek'de bulabileceğin bağlamda bir ışınlanma değildir. Bu uygulama alanından, ileriki bir hikayede bahsetmeyi planlıyoruz!
 
## Fiziksel Dolaşık Kübitler Hakkında Kısa Bir Not
 
Laboratuvarda dolaşık kübitleri fiziksel olarak oluşturmak, hangi tür kübit kullandığınıza bağlıdır. Örneğin, tek bir kaynaktan çıkan, özel bir şekilde üretilen iki foton, dolanık halde ortaya çıkabilir. Bıyıkkent'te olduğu gibi genel, tek bir 'dolanıklaştırıcı' yoktur. Ve doğrusu, aslında kimse bu kaynaklara ‘dolanıklaştırıcı’ demez! Kediler hariç.
 
_____________________________


_____________________________


_____________________________


**[Sırada: Karton Kutu Kimin Olacak?](https://quantum-kittens.github.io/posts/Who-Gets-the-Cardboard-Box/)**
 
________

## Qiskit Kodu

Sıradaki kodu kullanarak bir Bıyıkkent kapı zilini simüle edebilirsiniz. Bu kodu kullandığınızda, Bell durumlarına karşılık gelen kuantum devrelerini oluşturmayı öğreneceksiniz.

Aşağıdaki kod aynı zamanda jüpyter notebook olarak da mevcuttur [buradan ulaşabilirsiniz](https://github.com/quantum-kittens/quantum-kittens.github.io/blob/main/jupyter_notebooks/QK_Chapter_3.ipynb).

 ```python
# Gerekli Qiskit kütüphanelerini içeri aktaralım

from qiskit import QuantumCircuit, QuantumRegister, ClassicalRegister

#Kapı Zili Dolanıklaştırıcı Devresi Oluştur 

kubitler = QuantumRegister(2, name='q') # İki kübit(Bıyıkkent bilyeleri) ile bir kuantum kaydı oluştur ve kaydı 'q' olarak isimlendir 

classical_bits = ClassicalRegister(2, name='c') # İki bit ile bir klasik kayıt oluştur ve kaydı 'c' olarak isimlendir (Ölçüm sonuçlarını saklamak için)

q0, q1 = kubitler # Kayıttaki iki kübiti 'q0' ve 'q1' olarak etiketle

c0, c1 = klasik_bitler

kapizili_devresi = QuantumCircuit(kubitler, klasik_bitler) # Kuantum ve klasik kayıtlarla bir devre oluştur.

kapizili_devresi.h(q0) # İlk kübite bir Hadamard kapısı uygula

kapizili_devresi.cx(q0,q1) # İlk kübit kontrol ve ikinci kübit hedef kübit olacak şekilde bir cnot kapısı uygula. Kontrol kübit 1 durumundaysa, hedef kübitin durumu ters çevrilir.

kapizili_devresi.measure([q0,q1],[c0,c1]) # Ölçüm operatörleri ekle (bu bir kedinin dışarıdaki bilyeye doğrudan bakmasına eşdeğerdir).

kapizili_devresi.draw('mpl') # Devrenin nasıl göründüğüne bak.

```


Alıştırma olarak, bu devreyi Bölüm 2'deki bilye devresine benzer bir şekilde çalıştırın [Bölüm 2](https://quantum-kittens.github.io/posts/CHAPTER-2-Part-2-Qubits-Superposition-and-Measurements/)!

*Not: Kullanılan Qiskit kodu açık kaynaklıdır, ve Quantum Kittens'ın telif hakkı kapsamına girmez.*


