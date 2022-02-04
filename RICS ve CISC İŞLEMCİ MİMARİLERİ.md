**RICS ve CISC İŞLEMCİ MİMARİLERİ**

​      Günümüze kadar geliştirilen işlemci mimarisi RISC ve CISC’dir. Bu işlemci türleri önemli özellikleri bulunan komut sayılarıdır.

CISC’de, RISC’e göre daha çok komut kullanılır. Bu da onlara avantaj ve dezavantaj gibi özellikler kazandırıyor.

**CISC NEDİR?**

CISC mimarisinin açılımı Complex Instruction Set Computer (Karmaşık komut kümeli Bilgisayar). CISC’de komut sayısı çoktur ve karmaşıktır.

Bu özellik yazılımda kolaylık ve Derleyici’ye daha az iş yükü sağlamaktadır. Çok sayıdaki komutları kontrol etmek için kullanılan kontrol birimlerinin daha da karmaşık yapıya arttırmasına neden olur. Düşük hacimli bellekler kullanılması bu karmaşıklığın azaltılmasına çözüm olabilmektedir.

**RISC NEDİR?**

RISC mimarisinin açılımı Reduced Instruction Set Computer (İndirgenmiş komut kümeli Bilgisayar) anlamına gelir. Komut sayısı azdır bu yönüyle CISC mimarisine göre daha basittir.

Birçok komut için birden fazla birimde işlendiği için pipeline tekniğine sahiptir. Ayrıca, Superscalar tekniği kullanıldığı için çok yüksek performans elde edilmektedir.

Komutların sayısı az olması bu tekniklerin kullanılmasına olanak sağlamaktadır. Bu mimarinin çok hızlı olmasının asıl sebepleri komut sayısının az olması, pipeline ve Superscalar gibi tekniklerin kullanılması olduğunu söyleyebiliriz.

 

**Tp = S  x  A  x  Ta**

Tp= Programın icra süresi

S: Komutların Sayısı

A: Bir komutun sürüldüğü aşamaların ortalama sayısı

Ta: Bir aşamayı sürdürme süresi

Tp nin en minumum değeri doğal olarak S , A ve Ta nın minumum değerlerinde elde edilir. Ancak takdir edersiniz ki bu 3 parametrenin aynı anda minumum olma şansı yoktur. Bilgisayarın yapı ve çalışma özelliğinden dolayı buradaki bir parametre düşerken diğeri yükselmekte, diğeri düşerken başka bir parametre yükselmektedir. Burada CISC ve RISC mimarileri iki ayrı yöntem kullanmıştır.

**CISC Mimarili İşlemciler**

Tp’yi en aza indirmek için, CISC mimari, S’i minimumlaştırmak yolunu seçmiş ve bu sırada A ve Ta değerlerinin yükselmesinden doğacak kayıpların kazanca nispeten daha az olacağını iddia etmektedir. Uygulama alanında yoğun olarak rastlanması tahmin edilen ve nispeten karmaşık olan işlemler içinde komutlara sahiptir. Bu komutlar asembler dilinde kolay ve hızlı programlama ortamı sağlarlar. Yüksek seviyeli programlama dillerini destekler ve yüksek performanslı derleyiciler tasarlamak gerektiğini iddia eder.

Örnek:
 C yi 1 azalt
 Eğer C =! 0 döngü başına atla

gibi elementar işler uygun olarak DEC ve JNZ komutlarıyla gerçekleştirilir. Fakat programlamalarda bu iki işlem çok yoğun olarak birlikte rastlandığından dolayı 8086 dan başlayarak Intel in bütün mikroişlemcileri bu iki komutu birlikte icra eden LOOPNZ komutu ile donatılmaktadır. Bunun gibi bir çok örnek vardır.

**RISC Mimarili İşlemciler**

A x Ta  çarpımını minimumlaştırmak yolunu seçmiş, bu sırada S’in değerinin yükselmesinden doğacak kayıpların kazanca nispeten az olacağını iddia etmektedir. Hatırlatalım ki bunlar alternatif gibi görünse de birbirini reddeden mimariler değil, hatta bir sistem dahilinde bir araya gelebilen mimarilerdir.

CISC mikroişlemciler tarafından her biri tek bir çok fonksiyonlu komutla gerçekleştirilebilen işlemler RISC mikroişlemciler tarafından birkaç komutla gerçekleştirilir. Derleyici için kolay olmasına ve basit donanımla hızla gerçekleştirilmesine özellikle dikkat edilir.

Aynı problem için tipik bir RISC ve tipik bir CISC işlemcisine yönelik olarak tertiplenmiş olan iki program karşılaştırıldığında, kullandıkları komutların toplam sayısına göre birinci program ikinciden ortalama olarak 1.66 kat uzun olur. Burada RISC mimari yapısının verimlilik kaybı olduğu kanaatine varılabilir, bu teorik olarak doğru gibi gözükse de gerçekte böyle değildir. Çünkü RISC mimarisi, söz konusu kayıpları kısmen önlemek, kısmen de telafi etmek için kendine özgü ilkeler bulmuştur.

Bir çok özel amaçlı kontrol kartlarının merkezinde RISC işlemcileri durur. Bunlardan en yaygın olanı : PIC, 80×86, IBM 801, MIPS ailesi, SPRAS ailesi, POWER PC ailesi, Motorola 88000 ailesi, ARM vb.

**RISC VE CISC MİMARİ KARŞILAŞTIRMASI**

İlk mikroişlemciler CISC mimarisine uygun tasarlanmışlardır. Belli bir mikroişlemci teknik kısıtlamaların izin verdiği ölçüde her iki mimariden de özellikleri barındırabilir. Örneğin Intel’in son dönem işlemcileri pek çok RISC özelliğini de barındırmaktadır. Bu nedenle CISC ve RISC mimarilerini var yok biçiminde değil bir özellik barındırma biçiminde düşünmek daha uygundur.

**![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image002.png)**

 

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image004.png)

⦁ CISC mimarisinde daha fazla makine komutu RISC mimarisinde daha az makine komutu bulunma eğilimindedir. RISC mimarisinde **daha az komut daha hızlı ve etkin** çalışacak biçimde mantık devreleriyle oluşturulmuştur. Dolayısıyla **komutların hemen hepsi tek bir mantık devresiyle** doğrudan çalıştırılır. Halbuki CISC mimarisinde **mikrokod programlamayla** karmaşık komutlar daha yalın parçalara ayrılarak çalıştırılır.

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image006.png)

⦁ CISC mimarisinde makine komutları farklı uzunluklarda olma eğilimindedir. Halbuki RISC mimarisinde tüm makine komutları aynı uzunluktadır. CISC mimarisinde **çok kullanılam makine kamutları az byte’la az kullanılan makine komutları çok byte’la** ifade edilmeye çalışılmıştır. İlk zamanlar bunun iyi bir teknik olduğu sanılmışsa da daha sonraları bazı problemler göze çarpmıştır. Komutlar farklı uzunluklarda olursa genel olarak komutu alıp yorumlama (*fetch ve decode*) işlemi yavaş yapılmaktadır. Ayrıca komut seviyesinde *pipeline mekanizması* komutlar eşit uzunluktaysa daha etkin yapılabilmektedir.

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image008.png)

⦁ RISC mimarisinde çok sayıda yazmaç (*register*) bulunma eğilimindedir. Halbuki CISC mimarisinde daha az sayıda yazmaç vardır. Ayrıca RISC mimarisinde her yazmaçla her şey yapılabilmektedir. Halbuki CISC mimarisinde bazı işlemler ancak bazı özel yazmaçlarla yapılabilmektedir.

⦁ RISC mimarisinde belleğe erişen makine komutları ile işlem yapan makine komutları ayrı tutulmuştur. Bu nedenle RISC işlemcilerine ***Load/Store\*** işlemcileri de denir.

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image010.png)



⦁ RISC mimarisinde toplama, çıkartma, çarpma gibi tüm işlemler operandlarını yazmaçlardan alacak biçimde tasarlanmıştır. Halbuki CISC mimarisinde komutların bir operandı yazmaç iken diğer operandı bellek adresi olabilmektedir.
 ⦁ RISC mimarisinde **Load/Store** komutları dışındaki komutlar üç operandlı olma eğilimindedir. Halbuki CISC mimarisinde neredeyse tüm komutlar iki operandlıdır. RISC’te her iki operandın yazmaç olması zorunludur. Toplamda RISC’teki tasarımın daha faydalı ve etkin olduğu ispatlanmıştır. Bu nedenle artık **yeni işlemcilerin hepsi RISC mimarisinde** tasarlanmaktadır.
 ⦁ ***RISC işlemcileri pipeline işleminin etkinliğiyle ünlüdür\***. Pipeline işlemci'nin bir komutu yaparken diğerleri üzerinde de bazı hazırlık işlemlerini **yapabilmesi** anlamına gelir. Şüphesiz Intel gibi CISC işlemcileri de pipeline mekanizmasına sahiptir. Ancak RISC tasarımı pipeline mekanizmasının daha etkin yapılabilmesine yol açmaktadır.

 **Hız:** İki işlemci mimarisinin karşılaştırılmasından ilk önemli farkın; hızları olduğu bulunur. İki işlemci mimarisi arasındaki hız farkı, kullanılan komut işleme teknikleri sonucu oluşur. RISC işlemciler, genellikle aynı saat frekansında çalışan CISC işlemcilere göre daha hızlıdır.

 

·    CISC talimatları RISC’den daha fazla çevrim kullanır.

·    Azaltılmış komut kümesi sayesinde daha hızlı çalışırlar.

·    RISC ‘de CPU’daki komut işleme daha hızlı olacağından bu hızda çalışan CPU’ya hızlı RAM ve büyük önbelleklere ihtiyaç vardır.

 

 **Komut İşleme Tekniği:** Mimariler arasındaki ikinci önemli fark; komut işleme tekniğidir. CISC işlemcilerde ‘kademeli komut işleme’ tekniği kullanılırken, RISC işlemcilerde ‘kanal komut işleme tekniği’ (pipeline) kullanılır. CISC tekniği ile aynı anda tek bir komut işlenebildiği ve komutun, işlenmesi bitmeden yeni bir komut üzerinde çalışmaya başlanamaz. RISC tekniğinde ise, aynı anda çok sayıda komut işlenmektedir. Komutların birbirini takip etmesi nedeni ile her bir komut bir birim uzunluktadır ve her işlem adımında bir komuta ait işlemler bitirilir.

 

·    CISC’de farklı komutlar farklı sayıda saat çevrimine gerek duyacaklarından performans düşmesi gözlenir.

·    RISC işlemcilerin komut kümeleri basitleştirildiklerinden çok az yonga kullanırlar.

·    RISC’de bütün komutlar tek bir çevrimde çalıştırılmalıdır.

·    RISC’de program derlenince daha fazla makine kodu olacağından CISC’e göre daha fazla alan kapsar.

 

 

 **Transistör Sayısı:** CISC ve RISC yapıları arasındaki üçüncü önemli fark; işlemcilerde kullanılan transistor sayısıdır. CISC işlemcilerde kullanılan transistor sayısı, RISC işlemcilere göre daha fazladır. Daha fazla sayıda transistor kullanılması, daha geniş alan gereksinimi ve daha fazla ısı ortaya çıkarır, Oluşan daha fazla ısı nedeniyle soğutma ihtiyacı ortaya çıkar ve soğutma işlemi, ısı dağıtıcısı veya fanlar kullanılarak gerçekleştirilir.

 

·    CISC’de karmaşık işlemci yapısına bağlı olarak ihtiyaç duyulan transistör sayısı da artmıştır.

 

 

**Donanımsal Yapı (Tasarım Şekli):** İki mimari arasındaki bir diğer fark; donanımsal yapıları ve tasarım şekilleridir. RISC işlemciler, CISC işlemcilere göre daha basit yapıda olduklarından daha kolay tasarlanırlar.

 

·    CISC için CPU yapısı her kuşak işlemci ile beraber daha karmaşıklaşmıştır.

 

**Komut yapısı:** RISC mimarisi, CISC’in güçlü komutlarından yoksundur ve aynı işlemi yapmak için daha fazla komuta gereksinim duyar. RISC mimaride aynı uzunlukta basit komutlar kullanılırken CISC mimaride karmaşık yapıda değişken uzunlukta komutlar kullanılır.

 

·    RISC’de belleğe sadece “Load” ve “Store” komutlarıyla erişilmelidir.

·    RISC’in bütün icra birimleri mikrokod kullanılmadan donanımsal olarak çalışmaktadır.

·    RISC’de komutlar sabit 32 bitliktir. CISC’de komutların boyutu sabit değildir.

 

**TASARIM:**

​      Basit işlemci tasarımı yapmamız gerekiyor. Bunun için gerekli işlemleri yapacak bir ALU, Register ve Ram’e ihtiyacımız var.

**ALU:** Aritmetik mantık birimi anlamına gelir. Aritmetik ve mantık işlemlerini gerçekleştiren bir devredir.

**Register:** Register, küçük hafıza birimleridir. bir işlemcinin, mikro denetleyicinin veya bir entegrenin işlemleri nasıl yapacağı hakkında bilgilerin yazıldığı alanlardır. Bir işlem öncesi bakılması gereken hafıza bölümünü, hesaplamalar sonucu bulunan değerleri ve giriş-çıkış işlemlerinde yönlendirme bilgisi gibi kayıtlar tutulur.

**Ram:** İhtiyacımız olan bilgileri geçici olarak tutan hızlı bir bellek. RAM bellek her biri 1 ya da 0 bulunduran kutulardan oluşur. Bu kutulardan her biri eşsiz bir adrese sahip olur, sıralar ve sütunlar halinde yer alırlar. Set halinde bulunan RAM kutuları dizi olarak bulunur ve her bir kutuya da hücre denir.RAM bellek bu hücrelerde bilgisayarınızın kısa süre içerisinde ihtiyaç duyabileceğini düşündüğü her türden bilgiyi depolar ve ihtiyaç anında iletir. Bu sayede oyun oynarken ya da bir görsel üzerinde çalışırken yavaşlama olmadan sürecin devam etmesini sağlar.

 

 

​      Basit bir işlemci tasarlamak için elimizde olan bu 3 devre birleşik halinde çalışmalıdır. ALU işlemleri içinde “+, -, and, or … vb” işlemler yapılırken. Registerlarımızın bellek boyutları ve Ram in bellek boyutları aynı olmalıdır. Bunun nedenlerinden biri hücreler arasındaki büyüklük farkından kaynaklanabilir. 16 bitlik bir hücre de sakladığımız veriyi yine en az 16 bitlik bir hücrede saklayabilir. 

 

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image012.png)                 

Ram ve register boyutları aynı olmalı. Şimdi bu yapıları nasıl koda aktaracağımıza ve kodu nasıl simülasyonla gerçekleştireceğimize bakalım.

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image014.png) İlk olarak gerekli kütüphanelerimizi tanımladık. Bu kütüphaneler gerekli bağlantıları yapmamıza ve aritmetik işlemlerimizin gerçekleşmesini sağlayacak. 

​      Ardından 16 bitlik bir komut satırı oluşturmak istedik. İşlemciye sadece oluşturduğumuz 16 bit girip işlem yapacak.

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image016.png)

Adından yaptığımız işlemleri hafıza tutması için Ram ve Reg. tanımlaması yaptık. 64 hücreli ve 8 bitlik bir Ram ve 16 hücreli 8 bitlik bir reg. oluşturduk.

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image018.png) Ardından komutlarımızı yazmaya başladık. Fakat komutları yazmadan önce process içinde saat ve reset sinyalleri tanımladık. Böylece her saat sinyalinin yükselen ya da isteğimize göre alçalan darbesinde işlemcimiz çıktı üretecek.

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image020.png)

Ardından 16 değerli bir işlemci tasarlamaya başladık. “15 to 0” tasarımımızın tamamını oluştururken . 15 -12 bitleri bizim için en anlamlı 4 biti oluşturdu. 

Kodumuzun da yer alan ilk emrimiz “0000” yani null emri. Bu emir geldiği zaman işlemci herhangi bir hareket gerçekleştirmez. Sadece yeni emir gelmesini bekler. 

Sıradaki kullanabileceğimiz emir ise “0001” load emri . Şimdi bu emirlerimizin işlemcide nasıl karşılık bulduğuna bakalım. 

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image022.png)      Load             Reg.               Komut

Komutta girdiğimiz bir sayı dizisini istediğimiz reg.’a atayabiliriz. Örnek kod bloğu gelin emirle şu şekilde çalışır.

0001 0011 00000111 0 

İlk 4 emrimizi. Sonraki 4 hedef registerı . Sonraki 8 bit ise girilen değeri ifade eder. Bunun simülasyon önceki ve sonraki haline bakalım.

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image024.png)

Simülasyon için gerekli ayarlamaları yaptıktan sonra saat sinyalimizi ve komutlarımızı sıfırlıyoruz. Buradan da registerlarımızın içi değiştirebilir ama biz gösterdiğimiz gibi yapalım.

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image025.png)

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image027.png)![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image029.png)3. registremıza 0111 değerini atamış olduk.

 Görüldüğü gibi 3. register değerlerimiz değişti. 

Şimdi birkaç kod bloğunu daha inceleyip yaptığımız simülasyonlara geçelim.

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image031.png)

Sırasıyla reg. değerini başka bir reg.’a kopyalama ; Ram deki değeri Reg.’a kopyalam ; Reg’dan Ram e yazma ve Ram değerini Reg.’a kopyalama gibi devam etmekte.

Şimdi yazdığımız diğer işlemlerden bahsedelim. Biri Registerlar arası Not ve Reg.’lar arası lojik kapı işlemleri.

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image033.png)

Bir regdeki hücre içerisini tersini alıp hedef hücreye yazma. 

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image034.png)

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image036.png)

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image038.png)

Sırasıyla önceki ve sonraki halleri kodun doğruluğunu test emiş olduk.

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image040.png)

Şimdide bir çıkarma işlemini görelim. Yine aynı şekilde kod satırlarımızı dolduracağız. İlk 4 emrimiz sonraki 4bit hedef reg. sonraki iki tane 4 bit de işlem yapacağımız reg.’ları göstericek. Bunun için iki reg. ımı önceden dolduruyorum birine 12 birine 7 değerlerini atayacağım ve iki değer arasında işlem yapmasını sağlayıp çıktı olarak 5 sonucunu alacağız.

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image042.png)

\6. ve 7. Reg. ‘a “0001” komutuyla değer atamalarımızı yaptık. Şimdi işlem komutumuzu yazıyoruz.

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image043.png)

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image045.png)

​      Emir           Hedef Reg.        1.Reg           2. Reg

​       1001              1000                0110             0111     

![img](file:///C:/Users/ucakm/AppData/Local/Temp/msohtmlclip1/01/clip_image047.png)

6. Reg değerimizden 7. Reg değerimizi çıkarma işlemi yapıp 8. Reg. yazdık.

  

VHDL ile işlemci tasarımı videosu:

https://www.youtube.com/watch?v=RckTsu9PGDo&ab_channel=MertUcak

​      **Kaynaklar**

https://assemblylearningtutorial.blogspot.com/2016/10/cisc-ve-risc-mimarileri.html

https://www.bizimgri.com/bilim/risc-ve-cisc-mimari-karsilastirilmasi.html

https://otomasyonadair.com/2016/01/27/cisc-ve-risc-mimarileri-nedir/

http://www.enderunix.org/docs/risc.php

https://hobidenfazlasi.blogspot.com/2019/01/register-yazmac-nedir.html

https://shiftdelete.net/ram-nedir

 