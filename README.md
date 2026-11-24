# Pardus Dosya & Mesaj Gönderici: Aynı Ağdaki Bilgisayarlar Arasında Dosya ve Mesaj Paylaşmanın Kolay Yolu

Aynı ofiste, sınıfta veya evde birden fazla bilgisayar kullanıyorsanız zaman zaman bir bilgisayardan diğerine dosya ya da mesaj göndermeniz gerekebilir. Peki bunun için hâlâ USB bellek kullanmak, e-posta göndermek veya dosyaları bulut servislerine yüklemek zorunda mısınız?

Aslında hayır!

**Pardus Dosya & Mesaj Gönderici**, aynı yerel ağa (LAN veya Wi-Fi) bağlı bilgisayarlar arasında hızlı ve kolay bir şekilde dosya ve metin mesajı paylaşmanızı sağlayan, Python ile geliştirilmiş hafif bir masaüstü uygulamasıdır.

Herhangi bir üyelik, kullanıcı hesabı veya internet bağlantısı gerektirmeden çalışan program sayesinde aynı ağdaki bilgisayarları otomatik olarak keşfedebilir, istediğiniz kişiye dosya gönderebilir ve kısa mesajlar iletebilirsiniz.

Üstelik tüm işlemler yerel ağ üzerinden gerçekleştirilir. Böylece dosyalarınızı üçüncü taraf bulut servislerine yüklemenize gerek kalmaz.

Bu yazımızda Pardus Dosya & Mesaj Gönderici'nin özelliklerini, çalışma mantığını ve nasıl kullanılacağını adım adım inceleyeceğiz.

---

## Pardus Dosya & Mesaj Gönderici Nedir?

Pardus Dosya & Mesaj Gönderici, aynı yerel ağa bağlı bilgisayarlar arasında doğrudan iletişim kurulmasını sağlayan bir dosya ve mesaj paylaşım aracıdır.

Programı çalıştıran kullanıcılar, ağa katıldıklarında birbirlerini otomatik olarak görebilir. Böylece IP adresi öğrenmek, ağ paylaşımı oluşturmak veya karmaşık bağlantı ayarlarıyla uğraşmak gerekmez.

Programın sunduğu temel özellikler şunlardır:

- **Otomatik cihaz keşfi:** Aynı ağda programı çalıştıran kullanıcılar otomatik olarak listelenir.
- **Dosya gönderme:** Seçtiğiniz kullanıcıya doğrudan dosya gönderebilirsiniz. Aktarım hızı yerel ağınızın performansına bağlıdır.
- **Anlık mesajlaşma:** Diğer bilgisayarlara hızlıca metin mesajları gönderebilirsiniz.
- **Mesaj arşivleme:** Gelen mesajlar gönderen bilgisi ve tarih-saat bilgisiyle birlikte otomatik olarak `.txt` dosyası şeklinde kaydedilir.
- **Otomatik dosya kaydetme:** Gelen dosyalar belirlenen klasöre kaydedilir. Aynı isimde dosya varsa mevcut dosyanın üzerine yazılmaz.
- **Modern kullanıcı arayüzü:** Sekmeli yapı, koyu tema, bildirimler ve kolay erişilebilir kontroller sayesinde sade bir kullanım sunar.
- **Çapraz platform desteği:** Pardus, Debian, Ubuntu ve Windows bilgisayarlar arasında aynı protokol üzerinden iletişim kurulabilir.

En önemli avantajı ise bütün bu işlemlerin internet üzerinden değil, doğrudan yerel ağ üzerinden gerçekleştirilmesidir.

## Program Nasıl Çalışır?

Programın çalışma mantığı oldukça basittir.

Aynı yerel ağa bağlı bilgisayarlarda uygulama açıldığında kullanıcılar kendi belirledikleri isimlerle ağa katılır. Program, UDP üzerinden ağdaki diğer kullanıcıları keşfeder ve bağlantı bilgilerini günceller.

Dosya gönderimi ise TCP bağlantısı üzerinden gerçekleştirilir. Böylece dosyalar bilgisayarlar arasında doğrudan aktarılır.

Kısacası:

- UDP: Ağdaki kullanıcıların keşfedilmesi.
- TCP: Dosya aktarımı ve mesaj iletişimi.
- Yerel ağ: Bilgisayarlar arasındaki doğrudan iletişim.

İnternet bağlantınız olmasa bile aynı ağa bağlı bilgisayarlar arasında programı kullanabilirsiniz.

---

## Nasıl Kullanılır? Adım Adım İnceleyelim

### 1. Programa Katılın

Programı açtığınızda sizi sade ve anlaşılır bir kullanıcı arayüzü karşılar.

İlk olarak üst bölümde bulunan **Adınız** alanına ağda görünmesini istediğiniz kullanıcı adını yazın.

Örneğin: `Ahmet`

Ardından **🚀 Katıl** düğmesine basın.

Program ağa katıldığında diğer kullanıcılarla iletişim kurmaya başlar. Bağlantı durumu göstergesi kırmızıdan yeşile döner ve ekranda `Bağlı: Ahmet` bilgisi görünür.

Artık diğer kullanıcılar tarafından görülebilirsiniz.

### 2. Aynı Ağdaki Kullanıcıları Görün

**👥 Kişiler** sekmesine geçtiğinizde aynı ağda programı çalıştıran diğer kullanıcıları otomatik olarak görebilirsiniz.

Kullanıcı listesinde şu bilgiler yer alır:

- **Ad:** Kullanıcının belirlediği isim.
- **IP:** Bilgisayarın yerel ağ IP adresi.
- **Son görülme:** Kullanıcının en son ne zaman aktif olduğuna ilişkin bilgi.

Bir kullanıcı programı kapattığında veya ağ bağlantısı kesildiğinde, yaklaşık 8 saniye içerisinde kullanıcı listesinden otomatik olarak kaldırılır.

Bu sayede güncel kullanıcı listesini takip etmek için herhangi bir işlem yapmanız gerekmez.

### 3. Başka Bir Bilgisayara Dosya Gönderin

Dosya paylaşımı programın en kullanışlı özelliklerinden biridir.

Dosya göndermek için şu adımları izleyin:

1. Kişiler listesinden dosya göndermek istediğiniz kullanıcıyı seçin.
2. **📁 Dosya Gönder** düğmesine tıklayın.
3. Açılan dosya seçim penceresinden göndermek istediğiniz dosyayı belirleyin.
4. Aktarım başladığında ilerleme çubuğundan işlemin durumunu takip edin.

Dosya aktarımı tamamlandığında karşı bilgisayarda bildirim görüntülenir ve dosya otomatik olarak `~/AlinanDosyalar/` klasörüne kaydedilir.

**Dosyalarınızın üzerine yazılmaz!**

Gönderilen dosyayla aynı isimde bir dosya zaten bulunuyorsa program otomatik olarak farklı bir isim oluşturur.

Örneğin:

- rapor.pdf
- rapor_1.pdf
- rapor_2.pdf

Böylece daha önce alınmış dosyalarınızı kaybetme riski ortadan kaldırılır.

### 4. Anlık Mesaj Gönderin

Bazen bir dosya göndermek yerine kısa bir not iletmek yeterlidir.

Örneğin:

- Toplantı saat 10.00'da başlayacak.
- Hazırladığım dosyayı kontrol edebilir misin?
- Yazıcıdaki sorun giderildi.
- Evrakları e-posta ile gönderdim.

Mesaj göndermek için:

1. Kişiler listesinden mesaj göndereceğiniz kullanıcıyı seçin.
2. **💬 Mesaj Gönder** düğmesine tıklayın.
3. Açılan penceredeki alana mesajınızı yazın.
4. **📤 Gönder** düğmesine basın.

Dilerseniz mesajınızı `Ctrl + Enter` kısayoluyla da gönderebilirsiniz.

**Mesaj karşı tarafa ulaştığında ne olur?**

- Karşı bilgisayarda bildirim penceresi görüntülenir.
- Mesajlar sekmesinde yeni mesaj görünür.
- Gelen mesajlar yeşil, gönderilen mesajlar mavi renkle gösterilir.
- Gelen mesaj otomatik olarak metin dosyası şeklinde arşivlenir.

Mesajlar `~/GelenMesajlar/` klasörüne kaydedilir.

Kaydedilen mesaj dosyasında gönderenin adı, mesajın gönderildiği tarih ve saat, gönderenin IP adresi ve mesajın içeriği bulunur.

Örnek mesaj kaydı:

```text
Gönderen : Ahmet
Tarih    : 2026-11-24 14:32:07
IP       : 192.168.1.42
--------------------------------------------------

Merhaba, dosyayı aldım. Teşekkürler!
```

Bu özellik sayesinde önemli mesajlarınızı daha sonra tekrar inceleyebilir, arşivleyebilir veya ihtiyaç duyduğunuzda kullanabilirsiniz.

### 5. Ayarlar ve Hakkında Bölümleri

Program yalnızca dosya ve mesaj gönderme işlevlerinden ibaret değildir. Kullanımı kolaylaştıran bazı yardımcı bölümler de bulunmaktadır.

**⚙️ Ayarlar**

Ayarlar sekmesinden:

- Kullanıcı adınızı görüntüleyebilirsiniz.
- Bağlantı portu bilgilerini görebilirsiniz.
- Bilgisayarınızın yerel IP adresini inceleyebilirsiniz.
- Gelen mesajlar klasörünü açabilirsiniz.
- Alınan dosyalar klasörüne doğrudan ulaşabilirsiniz.

**ℹ️ Hakkında**

Hakkında sekmesinde programın sürümü, geliştirici bilgileri ve web sitesi yer alır.

Web sitesi bağlantısına tıklayarak doğrudan internet tarayıcınız üzerinden ilgili sayfaya ulaşabilirsiniz.

---

## Neden Pardus Dosya & Mesaj Gönderici?

Dosya paylaşımı için kullanılabilecek pek çok yöntem bulunuyor. Ancak bu uygulamayı farklı kılan bazı önemli özellikler var.

| Özellik | Avantajı |
|---|---|
| Yerel ağ üzerinden çalışma | Dosyalar üçüncü taraf bulut servislerine yüklenmez. |
| Üyelik gerektirmeme | Hesap açma veya kayıt işlemi yoktur. |
| İnternet gerektirmeme | Aynı yerel ağ yeterlidir. |
| Otomatik kullanıcı keşfi | IP adresiyle manuel bağlantı kurmanız gerekmez. |
| Mesaj arşivleme | Gelen mesajlar bilgisayarınızda saklanır. |
| Kolay kullanım | Karmaşık ağ ayarlarıyla uğraşmadan kullanılabilir. |
| Windows uyumluluğu | Farklı işletim sistemleri arasında iletişim kurulabilir. |

Özellikle ofisler, eğitim kurumları, bilgisayar laboratuvarları ve aynı yerel ağı kullanan çalışma grupları için pratik bir çözüm sunar.

## Sıkça Sorulan Sorular

**1. Dosya gönderirken boyut sınırı var mı?**

Uygulama tarafından belirlenmiş bir dosya boyutu sınırı bulunmamaktadır. Aktarılabilecek dosya boyutu; kullanılabilir disk alanına, ağ performansına ve işletim sistemi kaynaklarına bağlıdır.

**2. İnternet bağlantısı olmadan çalışır mı?**

Evet. Bilgisayarların aynı yerel ağa bağlı olması yeterlidir. İnternet erişimi olmadan da dosya ve mesaj paylaşabilirsiniz.

**3. Güvenlik duvarı bağlantıyı engeller mi?**

Bazı sistemlerde güvenlik duvarı ayarlarının düzenlenmesi gerekebilir.

Programın kullandığı portlar:

- UDP: 50000
- TCP: 50100–50600

Bu portlara yerel ağ üzerinden iletişim için izin verilmesi gerekebilir.

**4. Gelen dosyalar nereye kaydedilir?**

Gelen dosyalar kullanıcının ev dizinindeki `AlinanDosyalar` klasörüne kaydedilir.

**5. Gelen mesajlar nerede saklanır?**

Mesajlar `GelenMesajlar` klasöründe `.txt` formatında saklanır.

**6. Aynı bilgisayarda iki kez çalıştırılabilir mi?**

Teorik olarak mümkün olsa da gerçek kullanım ve bağlantı testleri için iki ayrı bilgisayarda çalıştırılması önerilir.

**7. Pardus dışında Windows bilgisayarlarda da kullanılabilir mi?**

Evet. Aynı iletişim protokolünü kullanan Windows ve Linux bilgisayarlar arasında dosya ve mesaj paylaşımı yapılabilir.

---

## Güvenlik ve Kullanım Sorumluluğu

Pardus Dosya & Mesaj Gönderici, yerel ağ üzerindeki kullanıcılar arasında dosya ve mesaj paylaşımını kolaylaştırmak amacıyla geliştirilmiştir.

Programı kullanırken aşağıdaki hususlara dikkat edilmelidir:

- Gönderilen dosya ve mesajların içeriğinden gönderen kullanıcı sorumludur.
- Yalnızca paylaşım yetkinizin bulunduğu ve yasal olarak paylaşılması serbest olan içerikleri gönderin.
- Başkalarının gizliliğini ihlal edebilecek bilgileri izinsiz paylaşmayın.
- Aynı ağdaki diğer kullanıcılar tarafından görülebileceğinizi unutmayın.
- Hassas ve gizli bilgileri gönderirken gerekli güvenlik önlemlerini alın.

**Önemli:** Yerel ağ üzerinden iletişim kurulması, tek başına şifreleme veya uçtan uca güvenlik sağlandığı anlamına gelmez. Uygulamanın mevcut sürümünde aktarım güvenliği ayrıca değerlendirilmelidir. Hassas verilerin paylaşımında bu hususu göz önünde bulundurun.

Program eğitim ve kişisel kullanım amacıyla, mevcut haliyle sunulmaktadır. Kesintisiz çalışma, hatasızlık veya belirli bir amaca uygunluk garantisi verilmez. Kullanımdan doğabilecek sorunlar, veri kayıpları ve sistem kaynaklı bağlantı problemlerinde kullanıcı kendi sisteminin güvenliğinden ve işlemlerinden sorumludur.

---

## Sonuç: Dosya Paylaşmak Artık Çok Daha Kolay!

Pardus Dosya & Mesaj Gönderici, aynı yerel ağdaki bilgisayarlar arasında dosya ve mesaj paylaşımını kolaylaştırmak için geliştirilmiş pratik bir masaüstü uygulamasıdır.

USB bellek aramak, e-posta göndermek, bulut servislerine dosya yüklemek veya karmaşık ağ paylaşım ayarlarıyla uğraşmak istemeyen kullanıcılar için alternatif bir çözüm sunar.

İster ofiste çalışma arkadaşlarınızla dosya paylaşın, ister bir bilgisayar laboratuvarında öğrencilerinize doküman gönderin, ister evinizdeki bilgisayarlar arasında hızlıca mesaj iletin...

Yapmanız gereken tek şey programı açmak, kullanıcı adınızı belirlemek ve ağa katılmak.

**Aynı ağdaysanız, paylaşmak artık çok daha kolay!**

### Geliştirici Bilgileri

- **Geliştirici:** Muhammet Ali AKGEL
- **Web sitesi:** https://www.akgel.com
- **Program:** Pardus Dosya & Mesaj Gönderici
- **Sürüm:** 1.1.0
- **Uyumlu işletim sistemleri:** Pardus, Debian, Ubuntu ve türevleri

Bu çalışma, Pardus ekosistemine ve özgür yazılım topluluğuna katkı sağlamak amacıyla geliştirilmiştir.

Görüşleriniz, önerileriniz ve hata bildirimleriniz benim için değerlidir.

**Özgür yazılımla, yerel ağda kolay paylaşım!**
