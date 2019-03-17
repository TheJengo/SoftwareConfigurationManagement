# Yazılım Konfigürasyon Yönetimi / Software Configuration Management
SWEBOK v3. kitabındaki Yazılım Konfigürasyon Yönetimi bölümünün Türkçe bir özetidir.  / This is an abstraction from SWEBOK v3. in Turkish.

AMAÇ (PURPOSE)
--------------

Bu doküman Yazılım Kalite ve Güvencesi dersi amacıyla hazırlanmış olup SWEBOK
içerisindeki Yazılım Konfigürasyon Yönetimi bölümünün özetini içermektedir.

KAPSAM(SCOPE)
-------------

Bu doküman SWEBOK kitabını ve içerisindekilerin yorumlarını içerir.

HEDEF KİTLESİ(INTENDED AUDIENCE)
--------------------------------

Bu doküman başta Manisa Celal Bayar Üniversitesi’nin yazılımcılarına, teknik ve
akademik kadrosuna ve öğrencilerine hitaben hazırlanmıştır.

SÖZLÜK(GLOSSARY)
----------------

| **Terim(Term)**                                                                     | **Açıklama(Description)**                                       |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Configuration Control Board – CCB                                                   | Konfigürasyon Kontrol Kurulu                                    |
| Configuration Management – CM                                                       | Konfigürasyon Yönetimi                                          |
| Functional Configuration Audit – FCA                                                | Fonksiyonel Konfigürasyon Denetimi                              |
| Physical Configuration Audit – PCA                                                  | Fiziksel Konfigürasyon Denetimi                                 |
| Software Configuration Control Board – SCCB                                         | Yazılım Konfigürasyon Kontrol Kurulu                            |
| Software Configuration Management – SCM                                             | Yazılım Konfigürasyon Yönetimi                                  |
| Software Configuration Management Plan – SCMP                                       | Yazılım Konfigürasyon Yönetim Planı                             |
| Software Configuration Item – SCI                                                   | Yazılım Konfigürasyon Öğesi                                     |
| Software Change Request – SCR                                                       | Yazılım Değişiklik İsteği                                       |
| Software Configuration Status Accounting – SCSA                                     | Yazılım Konfigürasyon Durum Muhasebesi                          |
| Software Design Document – SDD                                                      | Yazılım Tasarım Dokümanı                                        |
| Software Engineering Institute’s Capability Maturity Model Integration – SEI / CMMI | Yazılım Mühendisliği Enstitüsü Tümleşik Yetenek Olgunluk Modeli |
| Software Quality Assurance – SQA                                                    | Yazılım Kalite Güvencesi                                        |
| Software Requirement Specification – SRS                                            | Yazılım Gereksinim Dokümanı/Şartnamesi                          |

1.  YAZILIM KONFİGÜRASYON YÖNETİMİ

    1.  Sistem nedir?

Sistem, ortak bir hedefi olan birbiriyle etkileşim içerisinde bulunan
organizmalar bütünü olarak tanımlayabiliriz.

Konfigürasyon nedir?
--------------------

Konfigürasyon, bir sistemin fonksiyonel ve fiziksel karakteristiklerinin uygun
donanım ve yazılımlarla belirlenmesi ve dokümante edilmesidir.

CM (Configuration Management) nedir?
------------------------------------

Konfigürasyon yönetimi ise bir sistemin yaşam döngüsü içerisinde sistematik bir
şekilde yapılandırılması ve bakımının yapılması dışında sistemin nasıl bu
işlemleri sürdürebileceğini belirleyen/tanımlayan disiplindir.

Literatürdeki tanımı ise şöyledir:

“Bir sistemin fonksiyonel ve fiziksel karakteristiklerini belirleyen, sistemin
değişikliklere olan karakteristiklerini kontrol eden ve bu değişiklik
süreçlerini ve uygulanışlarını kayıt ve rapor eden ve bu özel gereksinimleri
doğrulayan, yönlendiren ve gözetleyen, teknik olarak yöneten disiplindir.”[1]

SCM (Software Configuration Management) nedir?
----------------------------------------------

Yazılım Konfigürasyon Yönetimi, CM disiplininin yazılım ve donanım olarak ikiye
ayrılan tarafındaki yazılım bölümüdür. Bu bölüm içerisinde yazılım yaşam döngüsü
süreçlerini destekler bir biçimde amaç proje yönetimine, geliştirme, bakım,
kalite ve güvence aktivitelerine fayda sağlamak ve ürünü en uygun şekilde
kullanıcılara veya müşterilere sunmayı amaçlar.

SCM ve SQA (Software Quality Assurrance) arasındaki ilişki
----------------------------------------------------------

SCM, SQA ile yakından ilişkilidir. Bilindiği üzere Yazılım Kalite Güvence
süreçleri bir yazılım ürününün proje yaşam döngüsü içerisinde, gereksinimlere
uygun, planlı ve formal aktivitelerin sergilenmesi sonucunda tutarlı bir şekilde
kaliteli yazılım geliştirildiğinin güvencesini sağlamaktır. SCM’in amacı ise
SQA’deki bu hedefler doğrultusunda özel SQA gereksinimlerini sağlamak ve SQA’in
amacını gerçekleştirmesini sağlamaktır.

SCM dalları nelerdir?

Yazılım Konfigürasyon yönetimi, içerisinde 7 dal barındırır bu dallar şöyledir:

-   **Yazılım Konfigürasyonunda Süreç Yönetimi**[2]

-   **Yazılım Konfigürasyon Tanımlaması**[2]

-   **Yazılım Konfigürasyon Kontrolü**[2]

-   **Yazılım Konfigürasyon Durum Muhasebesi**[2]

-   **Yazılım Konfigürasyon Denetimi**[2]

-   **Yazılım Yayınlama ve Teslim Yönetimi**[2]

-   **Yazılım Konfigürasyon Yönetim Araçları**[2]

    1.  Yazılım Konfigürasyonunda Süreç Yönetimi nedir?

SCM bir yazılım ürünündeki, değişimleri ve ürünün geliştirilme aşamalarında;
değişiklerin kontrol edilmesi ve yönetilmesi, doğrulanması, kayıt edilmesi ve
raporlanmasıdır. Bu süreçlerin başarılı bir şekilde yönetilebilmesi için
organizasyonel içeriklerin ve kısıtların iyi anlaşılması, dikkatli bir tasarım,
planlama ve yönetim gerekir.

Yazılım Konfigürasyonunda Süreç Yönetimi beş bölümden oluşur.

#### Yazılım Konfigürasyon Yönetiminde Organizasyonel İçerik

Bu bölümde Yazılım Konfigürasyon Yöneticisi, Uzman Yazılım Mühendisi veya Sistem
Mimarı, diğer Konfigürasyon Yöneticileriyle birlikte planlama aşamasında
organizasyona bağlı olan ilişkilerin, sorumlulukların, içeriklerin ve şartların
neler olduğunu özümseyerek kaliteli bir yazılım çıkartmayı hedefler.

#### Yazılım Konfigürasyon Yönetimi Sürecin için Kısıtlar ve Rehberlik

**Yazılım Konfigürasyon Yönetim Süreçlerinde** genelde şirket poliçeleri,
prosedürleri, şirket organizasyonel hiyerarşi ve bazı emirler tasarım ve
geliştirme aşamasında Yazılım Konfigürasyon Yönetimdeki süreci belirleyen en
etkili kısıtlar ve rehberlerdir.

#### Yazılım Konfigürasyon Yönetimi için Planlama

Yazılım Konfigürasyon Yönetim sürecinde bir proje içerisinde yapılan planlama
organizasyonel içeriğe, kısıtlara, genel kabul edilen yola ve projenin doğasına
(Ör: boyut, kritik güvenlik, güvenlik, vb.) uygun olmalıdır.

Planlama sürecinde **Yazılım Konfigürasyon Yönetimi Organizasyon ve
Sorumlukluk** bazında bakılırsa Yazılım Konfigürasyon Yönetimi aktivitelerini ve
görevlerini kimin üstleneceği konusunda karışıklık yaşanmaması için organizasyon
içerisinde bu süreçleri yönetecek görev tanımı net bir şekilde tanımlanmış bir
rol olmalıdır.

Yazılım Konfigürasyon Yönetimi için planlama yaparken aynı zamanda bu süreçte
çalışanlar ve araçlarda tanımlanmalıdır ve bu tanımlama işlemi de Yazılım
Konfigürasyon Yönetimi görevlerinden birisidir. Proje yönetimi tarafından
yapılan planlama aşamasında kilometre taşlarının ve proje takviminin iyi
anlaşılması gerekir. Her hangi bir eğitim gereksinimine ihtiyaç duyan yeni
çalışanlar olup olmadığı da bu süreç içerisinde belirtilmeli ve gerekli
eğitimler sağlanmalıdır.

Planlama aşamasında ayrıca yazılım mühendisliğindeki her alan gibi yapılacak
işler bütünü için Yazılım Konfigürasyon Yönetim araçları dikkatlice seçilmeli ve
planlanmalıdır. Aşağıdaki sorular bu süreçleri başlatmaya yöneliktir.

-   **Organizasyon** (Organization): Alınacak bir aracın satın alınması için bir
    organizasyonu ne motive eder?

-   **Araçlar** (Tools): Ticari araçları mı kullanmalı yoksa onları kendimiz mi
    geliştirmeliyiz?

-   **Çevre** (Environment): Kurum tarafından teknik içerik için empose edilmiş
    kısıtlar nelerdir?

-   **Miras** (Legacy): Eski projeler yeni araçları nasıl kullanabilir ya da
    kullanamaz?

-   **Finans** (Financing): Araçların satın alımı, bakımı, eğitimi ve
    özelleştirilmesi için parayı kim ödeyecek?

-   **Kapsam** (Scope): Yeni araçlar nasıl sunulacak? Tüm organizasyona mı yoksa
    özel projelere mi?

-   **Sahiplik** (Ownership): Yeni araçların tanıtımından kim sorumlu?

-   **Gelecek** (Future): Gelecekte kullanılacak araçlar için planımız nedir?

-   **Değişim** (Change): Araçlar ne kadar uyumlu?

-   **Dallanma ve Birleştirme** (Branching and merging): Araçlar planlanmış
    dallanma ve birleştirme stratejilerine ne kadar uyumlu?

-   **Entegrasyon** (Integration): Çeşitli Yazılım Konfigürasyon Yönetim
    araçları ile entegre olabilir mi mi? Organizasyon içindeki diğer araçlarla
    entegre olabilir mi?

-   **Geçiş** (Migration): Bir depo Versiyon Kontrol Aracı ile kontrol edilirken
    aynı türdeki başka bir araç ile değiştirildiğinde eski araçtan gelen tüm
    konfigürasyon eşyalarını taşıyacak mı?

>   Yazılım Konfigürasyon Yönetimi tipik bir şekilde bir dizi araç kullanımını
>   gerektirir.

Planlama sürecinde ayrıca dikkat edilmesi gereken bir diğer konu ise **“Satıcı /
Taşeron Kontrolü”** dür. Derleyiciler veya diğer araçlar gibi satın alınmış
yazılım ürünlerinin nasıl konfigüre edileceğini ve aynı kaygılarla Taşeron
(Subcontracted) uygulamaları da yönetilmesi ve kontrol edileceğinin
planlanmasıdır.

Planlama sürecinde son olarak bahsetmemiz gereken konu ise **Arayüz
Kontrolü**’dür. Bu konudan da bir yazılım ürünü ne zaman başka bir yazılım veya
donanım ile birbirlerini etkileyecek bir değişim/iletişim içerisinde olursa
bahsedilir. Yazılım Konfigürasyon Yönetim planlama sürecinde ilgili yazılım
iletişim halinde olduğu yazılım veya donanımlar tanımlanır, aralarındaki
değişiklikler, aktarılacak olan veriler, nasıl yönetileceği ve iletişim kuracağı
planlanır. Bu yüzdendir ki Yazılım Konfigürasyon Yönetimi rolü daha büyük,
sistem seviyesindeki işleyişler için arayüz özelleştirmeleri ve kontrolleri
planlamaktadır.

#### Yazılım Konfigürasyon Yönetimi Planı

Planlama sürecinde yapılan işlemler **Yazılım Konfigürasyon Yönetim Planı**
(Software Configuration Management Plan – SCMP) olarak dokümante edilir. Bu plan
“**yaşayan doküman**” olarak adlandırılır ve Yazılım Konfigürasyon Yönetim
süreçlerinin nasıl yürütüleceği konusunda bir referans hizmeti verir.

**Yazılım Konfigürasyon Yönetim Planı**(SCMP) içerisinde şunları bulundurur:

-   **Giriş** (amaç, kapsam, kullanılan terimler)

-   **SCM Yönetimi** (organizasyon, sorumluluklar, otoriteler, uygulanan
    poliçeler, direktifler ve prosedürler)

-   **SCM Aktiviteleri** (konfigürasyon tanımlamaları, konfigürasyon kontrolleri
    ve diğerleri)

-   **SCM Programı** (diğer proje aktiviteleri ile koordinasyon)

-   **SCM Kaynakları** (araçlar, fiziksel kaynaklar ve insan kaynakları)

-   **SCMP Bakımı**

    1.  Yazılım Konfigürasyon Yönetimi Gözetimi

Yazılım Konfigürasyon Yönetimi süreçlerinden sonra implemente edileleri, bir
dereceye kadar gözetlemek SCMP içerisindekileri taşıdığından emin olmak için
gereklidir. Gözekim gereksinimleri çok çeşitli olabilir bunlar **SQA** sebepleri
olabileceği gibi mühendislik sebepleri, hata ayıklama veya daha iyi
konfigürasyon hedefleri olabilir. Bu yüzden gözetim yaparken verilecek esneklik
düzeyinin belirlenmesi ve doğru araç seçimi yazılım mühendisliği içerisindeki
önemli hususlardandır.

Gözetim içerisinde bulunan bölümlerden birisi de **“Yazılım Konfigürasyon
Yönetimi Ölçüleri ve Ölçümü”’**dür. Ölçüler bizlere yazılımın evrimi hakkında
kritik bilgiler verirken aynı zamanda Yazılım Konfigürasyon Yönetimi
süreçlerininde fonksiyonelliği hakkında iç görüleri ortaya koyar. Bu ölçüleri
monitörize ederek süreçleri geliştirmek ana hedefler arasında yer alır. Bu
ölçüler aynı zamanda SCMP içerisinde yer alan bilgilerin süreç içerisinde
değişmesine veya düzeltilmesine yardımcı olur. Bu süreçler içerisindeki
ölçülerin değerli olabilmesi için ölçümlerin gözetimlerle yapılması gerekir ve
genel yazılım ölçümlerine uyması beklenmelidir.

Gözetimin amaçlarından bir diğeri ise bir süreç devam ederken **“Yazılım
Konfigürasyon Yönetimi İç Süreç Denetimi”’**dir. Denetimler yazılım mühendisliği
süreçleri içerisinde yapılandırmanın spesifik elemanlarının mevcut durumlarını
araştırmak için Yazılım Konfigürasyon Yönetim sürecinin uygulanmasını
değerlendirmek için yapılırlar. İç süreç denetimleri ise daha resmi ve güçlü bir
yapılanma sağlarken aynı zamanda SQA işlevi ile koordinedilmesi amaçlanır.

### Yazılım Konfigürasyonu Tanımlama

Yazılım konfigürasyonu tanımlama içerisindeki adımlar aşağıdaki gibidir,

-   *Kontrol Edilecek Öğeleri Belirleme*

    -   **Yazılım Konfigürasyonu** (Software Configuration)

    -   **Yazılım Konfigürasyon Öğesi** (Software Configuration Item - SCI)

    -   **Yazılım Konfigürasyon Öğesi İlişikileri** (SCI Relationships)

    -   **Yazılım Sürümü** (Software Versions)

    -   **Temel** (Baseline)

    -   **Yazılım Konfigürasyon Öğesi Almak** (Acquiring Software Configuration
        Items)

-   *Yazılım Kütüphanesi*

>   Yukarıdaki konu başlıkları ve içeriklerini özetlersek, kontrol edilecek
öğe/öğelerin belirlenmesinin ardından yazılımı fonksiyonel ve fiziksel
karakteristiklerini belirlemek ve onları koruyarak, ilgili yazılım
konfigürasyon öğelerini (yani donanım, yazılım veya ikisinide tek bir varlık
gibi yöneten yazılımlar) ve bu öğeleri tanımlar. Bu öğe aynı zamanda
içerisinde planlar, şartname ve tasarım dokümanı, test materyalleri, yazılım
araçları, kaynak ve çalıştırılabilir kod, kod kütüphaneleri, veri ve veri
sözlükleri ve yükleme, bakım, işletim ve yazılımı kullanma dokümanları
içerir. O yüzden bu öğenin ilişkileri yakından takip edilir ve yazılım
yapısını korumak amaçlanır. Yazılım evrim geçirdikçe sürümlenir (version) ve
bu sürümler çeşitlilikler gösterebilir. Bir “Temel (Baseline)” oluşturulur
ve bu temel aslında yazılımın geçerli, güvenilir kabul edilen üzerine inşa
edilecek versiyonudur. Bir değişiklik isteği geldiğinde (Software Change
Request) ve onaylandığında temel üzerine bu değişiklik eklenerek devam eder.

Yazılım Kütüphanesi ise günlük hayatta bildiğimiz kendine ait belli bir
temeli olan yazılım geliştirme, tasarım veya bakım aşamalarına yardımcı
olarak kullanılan hali hazırda kod depoları olarak kabul edilebilirler. Bu
kütüphaneler üçüncü parti yani dışarıdan alınmış olabileceği gibi içerde ve
eski projelerden özütlenmiş veya üretilmişde olabilirler.

### Yazılım Konfigürasyon Kontrolü

Yazılım konfigürasyon kontrolü daha çok yazılım yaşam döngüsü içerisindeki
değişiklikleri yönetmek ile ilgilidir. İçerisindeki konularda hangi değişikler
yapılmalı, otoriterler tarafından onaylanan kesin değişiklikler, değişikliğe
karşı açıklık, proje gereksinimlerinden yapılan sapmalar ve feragatlar konusunda
yapılması gerekenleri içerir. Konu başlıkları ise aşağıdaki gibidir:

-   *Yazılımda Değişiklik İstemek, Değerlendirmek ve Onaylamak* (Requesting,
    Evaluating and Approving Software Changes)

    -   **Yazılım Konfigürasyonu Kontrol Kurulu** (Software Configuration
        Control Board)

    -   **Yazılım Değişiklik İsteği Süreci** (Software Changes Request Process)

-   *Değişikliklerin Implementasyonu* (Implementing Software Changes)

-   *Sapmalar ve Feragatlar*

Yukarıdaki konu başlıklarını özetlemek istersek yazılımda değişiklik yapmak için
öncelikle bir Yazılım Değişiklik İsteği (Software Change Request – SCR)
oluşturmamız kapsamını düzenleme poliçelerini, süreçleri, planları veya
prosedürleri, düzenleme maliyeti veya bütçesi ve son olarak revize programı net
olan değişikliklere denir. Normalde olması gereken budur. Bir Yazılım Değişiklik
İsteği dokümanlarını tamamlamışsa yada güncellemişse ön incelemeye alınır. Ön
incelemeye alınan istek daha sonra Konfigürasyon Kontrol Kurulu (Configuration
Control Board – CCB)’na gelir. Bu kurul gelen bir değişiklik isteğini kabul eden
veya etmeyen otoritedir. Eğer değişiklik reddedilirse (rejected) istekte
bulunanlar bilgilendirilir (Inform Requester). Eğer kabul edilirse bir Yazılım
Mühendisine görev olarak atanır ve programı, tasarımı, testi yapılarak,
değişiklik tamamlanır. Bu aşamalar içerisinde gerçekleşen sapmalar ve feragatlar
otoriterler tarafından gözlemlenir ve rapolanır.

![Değişiklik Kontrol Süreci Akış Diagramı](https://github.com/TheJengo/SoftwareConfigurationManagement/blob/master/images/SCR.png)

Şekil 3.1. Değişiklik Kontrol Süreci Akış Diagramı

### Yazılım Konfigurasyon Durum Muhasebesi

Yazılım Konfigurasyon Durum Muhasebesi (Software Configuration Status Accounting
- SCSA), bir konfigürasyonu etkin bir şekilde yönetmek için gereken bilgilerin
kaydedilmesini ve raporlanmasını içeren bir konfigürasyon yönetimi unsurudur.
Konu iki temel başlık altında detaylandırılır:

-   *Yazılım Konfigürasyon Durum Bilgisi* (Software Configuration Status
    Information)

-   *Yazılım Konfigürasyon Durum Raporu* (Software Configuration Status
    Reporting)

Bu iki başlığı ve içeriklerini özetlersek durum bilgisi aşamasında toplanan her
türlü tasarım, geliştirme vb. yazılım yaşam döngüsü süreçleri içerisindeki
olaylar, gelişmeler ve araç destekli bilgiler doğrultusunda bu bilgilerin
organizasyona, geliştirme takımına, bakım takımına, proje yönetimine ve yazılım
kalite ve güvence aktivitelerinde kullanılması üzerine çeşitli araçlarla
süreçleri iyileştirmeye yönelik rapor haline getirilmesidir.

### Yazılım Konfigürasyon Denetimi

Yazılım Konfigürasyon Denetimi (Software Configuration Auditing), iş
ürününe/ürünlerine ait şartname, standartlar, sözleşmeler ve diğer kriterlere
göre yazılımın denetlenmesidir. Denetimlerin tutarlılığı iyi tanımlanmış
süreçlere ve çeşitli denetimci rollerin ve sorumlulukların olmasıyla ölçülür.
Temelde üç alt sürece ayrılır:

-   *Yazılım Fonksiyonel Konfigürasyon Denetimi* (Software Funtional
    Configuration Audit)

-   *Yazılım Fiziksel Konfigürasyon Denetimi* (Software Physical Configuration
    Audit)

-   *Yazılım Temelinin İç Süreç Denetimi* (In-Process Audits of a Software
    Baseline)

Bu alt süreçleri özetlersek, Fonksiyonel Konfigürasyon Denetimi sürecinde
yazılımın şartnamedeki gereksinimlere uygunluğu yazılımın çıktısında doğrulama
ve geçerleme aktiviteleri ile denetlenir. Fiziksel Konfigürasyon Denetimi
sürecinde ise tasarım ve referans belgelerinin, yerleşik yazılım ile tutarlı
olmasını sağlamaktır. Yukarıda bahsettiğimiz bu süreçler içerisinde Temel
Yazılım üzerinde yapılan denetlemeler ve incelemerde İç Süreç Denetimini
oluşturmaktadır. Amaç tutarlı bir yazılım ürünü ortaya koyduğumuzdan emin
olmaktır.

### Yazılım Sürüm Yönetimi ve Teslimi

Yazılım Sürüm Yönetimi ve Teslimi (Software Release Management and Delivery),
bir yazılım ürünündeki farklı sürümlerin doğru paketlenip doğru bir şekilde
teslim edilip edilmediğinin takibinin ve yapılandırılmasının yapıldığı süreçtir.
İki bölümden oluşur:

-   *Yazılım İnşaası* (Software Building)

-   *Yazılım Sürüm Yönetimi* (Software Release Management)

Bu iki bölümde amaç İnşaa edilecek bir yazılımın dağıtıma çıkacak sürümlerinin,
veri bağlantıları, dokümantasyon, sürüm notları ve çalıştırılabilir programın
doğru bir şekilde konfigüre edilmesidir.

### Yazılım Konfigürasyon Yönetim Araçları

**Yazılım Konfigürasyon Yönetim Araçları** (Software Configuration Management
Tools), yönetim işlerini kolaylaştıran ve standartlaştıran bu araçları
sınıflarsak üç sınıf altında incelememiz gerekir:

-   *Tekil Destek Araçları* (Individual Support Tools)

    -   **Sürüm Kontrol Araçları** (Version Control Tools – VCS), kaynak kod
        takibi, dokümantasyonlama ve tekil konfigürasyon öğelerin depolamaya
        yarar. Örnek olarak; SVN, Git, Mercurial araçları verilebilir.

    -   **İnşaa Kontrol Araçları** (Build Handling Tools – Compilers etc.),
        çalıştırılabilir yazılım versiyonunu elde etmek için kullanılan en
        basitinden bir derleyici yada bağlantıdır. İlgili yazılımın
        çalıştırılması esnasındaki hataları, kalite kontrolleri vb. durumları
        takip eder. Bu araçlara örnek olarak, GCC (C Compiler), Jake (Javascript
        Build Tool For NodeJS) verilebilir.

    -   **Değişiklik Kontrol Araçları** (Change Control Tools), Yazılım
        Değişiklik İsteklerinin (SCR) yönetildiği ve bu değişikliklerin takip
        edildiği araçtır. Örnek olarak Jira, Trello, GitHub Projects, YouTrack
        gibi araçlar verilebilir.

Bu araçlar uygun ve tipik bir şekilde küçük organizasyonlar veya geliştirme
grupları tarafından çeşitli yazılım ürünlerinde veya karmaşık Yazılım
Konfigürasyon Yönetim gereksinimlerini yönetmek için kullanılırlar.

-   *Proje-Odaklı Destek Araçları* (Project-related Support Tools)

Bu araçlar genellikle geliştirici takımlarının çalışma ortamı yönetimine entegre
olan ve dağıtık geliştirmeye olanak sağlayan araçlardır. Orta ölçekli
organizasyonlardan büyük ölçekli organizasyonlara kadar çeşitli yazılım yazılım
ürünlerinde, parallel geliştirme ortamını herhangi bir sertifikasyon gereksinimi
olmaksızın sağlamayı amaçlar.

-   *Şirketboyu-Süreç Destek Araçları* (Companywide-process Support Tools)

Bu araçlar genellikle şirket genelindeki bazı süreçlerin otomatize edilmesini,
iş-akışları, roller ve sorumlulukların yönetilmesine destek sağlar. Bir çok
öğeyi, veriyi ve yaşam döngüsünü destekleyebilirler. Bu araçlar, sertifikasyon
gereklilikleri de dahil olmak üzere daha resmi bir geliştirme sürecini
destekleyerek Proje-Odaklı Destek Araçlarına katkıda bulunurlar.

Referanslar
===========

[1] **ISO/IEC/IEEE 24765:2010 Systems and Software
Engineering—Vocabulary**,ISO/IEC/IEEE,2010.

[2] **IEEE Std. 828-2012, Standard for Configuration Management in Systems and
Software Engineering**, IEEE, 2012.
