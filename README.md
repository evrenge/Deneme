# Deneme

---
Gaz türbini performans modellemesi konusunda **TEI'nin stratejisi**, mevcut uygulamaları (özellikle **NPSS**) derinlemesine öğrenmeye odaklanmak ve temel seviyede şirket içi yazılımlarla kendi gaz türbinlerini modelleyebilme yeteneğini geliştirmektir. **NPSS gibi sektörde yaygın olarak kullanılan ve etkili bir uygulamadan uzaklaşmak yerine, bu tür araçlarla kurulacak modellemelerin doğruluğunu bir doğrulama planı ile teyit etmek kritik öneme sahiptir.** Bu doğrulama sürecinde motor testleri ve rig çalışmalarıyla modellerin valide edilmesi hedeflenmelidir, zira modelleme validasyonları zaman alsa da, gelecekteki projeler ve geliştirmeler için temel oluşturacaktır.

---

**Kendi modelleme programımızı geliştirme fikri, yakın vadede gerçekçi bir hedef olarak görülmemektedir.** Bu yönde bir adım atılmadan önce, **GasTurb ve NPSS dışındaki muadil uygulamaların detaylıca incelenmesi ve NPSS'in henüz tam olarak kullanılmayan veya anlaşılmayan kısımlarının aydınlatılması gerekmektedir.** Eğer ileride kendi yazılımımızı geliştirme kararı alınırsa, bu yazılımın kapsamlı bir **yazılım geliştirme ve doğrulama sürecinden geçmesi şarttır.** Bu süreç, termodinamik kanunlarının doğrulanması gibi absürt adımlardan ziyade, **altyapıya ve kodun işleyişine odaklanmalıdır.** Doğrulama için **literatürdeki ve mevcut uygulamaların cevaplarına eşdeğer bir kod geliştirildikten sonra, unit testler ve güvenlik kontrolleri (memory leak, backdoor vb.) ile sağlaması yapılmalıdır.** Her modelin ayrı ayrı test edilmesi gerektiğinden, **test matrisi modellere göre farklılık gösterecektir.**

---

**NPSS kullanılmadığında gaz tablolarının implementasyonu, Walsh & Fletcher gibi kaynaklardaki denklemlerle mümkün olabilir, ancak yüksek sıcaklıklarda bu fonksiyonların davranışları bozulabilir.** Yakıtın işin içine girmesi bu tabloları elde etmeyi zorlaştırabilir ve termodinamik kitaplarındaki gaz tablolarında yakıt bilgisi genellikle bulunmaz. Bu konuda **JANAF tabloları gibi dış kaynaklara erişim sağlanabilir.**

---

**TEI'ye böyle bir yazılım geliştirme çalışmasının maliyeti oldukça yüksek olacaktır.** Projenin tamamlanması için **büyük bir mühendis ekibinin yıllarca çalışması gerekecektir.** Tahmini olarak, NPSS kalitesine ulaşmak için gaz modeli çıkarma (200-2500K, 5-5000 kPa, 0-0.067 FAR, 0-100% bağıl nem aralıklarını tarama), optimize bir solver yapısı kurma (matematik mühendisleri), object-oriented altyapı oluşturma (bilgisayar mühendisleri) ve NPSS arayüz fonksiyonları geliştirme (bilgisayar mühendisleri) gibi kalemler önemli maliyetler doğuracaktır. Ancak, **düzenli bir plan ve hedefle yaklaşık 5 yıl gibi bir sürede NPSS'in yeteneklerinin önemli bir kısmı şirket içi yazılıma entegre edilebilir ve valide edilebilir.** TEI içinde geliştirilecek bir uygulamanın hem **turbomakina tasarımı hem de performans modellemesi yapabilmesi gerektiği vurgulanmaktadır.** Bu konuda **PxTurb, PYTurbo, PyCycle ve Modelica gibi açık kaynaklı yazılımlar alternatif olarak incelenmelidir.** Özellikle **Modelica**, Simulink'e kıyasla endüstriyel geçerliliği yüksek bir açık kaynak platform olarak öne çıkmaktadır.
