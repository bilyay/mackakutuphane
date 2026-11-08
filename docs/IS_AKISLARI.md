# Ekranlar ve kullanıcı akışları

Son güncelleme: 8 Kasım 2026

Bu belge, arayüz prototipini gerçek kütüphane süreçlerine dönüştürmek için ekranları, akışları ve gerekli kayıtları tanımlar. Okulun ödünç politikası kesinleştiğinde ilgili kurallar güncellenmelidir.

## 1. Oturum ve erişim

### Öğrenci oturumu

1. Öğrenci okulun belirlediği giriş yöntemiyle oturum açar.
2. Sistem hesabın öğrenci rolünü ve aktifliğini doğrular.
3. Öğrenci katalog, kendi listeleri, kendi ödünç kayıtları ve yorum özelliklerine erişir.
4. Profil menüsünden ödünç listesine, Çantam’a ve okuma listelerine geçer; profil sayfasında sınıf/şube ve iletişim bilgilerini günceller.
5. Profil sayfasından şifresini değiştirir. Gerçek sürümde şifre güncelleme okulun kimlik doğrulama sunucusuna bağlanmalıdır.

### Personel oturumu

1. Personel yetkili hesabıyla oturum açar.
2. Sistem personelin rolünü denetler.
3. Personel kitap, öğrenci, istek, ödünç, iade ve yorum moderasyonu ekranlarına rolü ölçüsünde erişir.
4. Kritik işlem kayıtlarında kullanıcı ve zaman bilgisi tutulur.

## 2. Öğrenci ekranları

### Hatırlatma bildirimleri

- Zil, etkin 24 saatlik ödünç isteklerini (son 6 saatte acil uyarı), yaklaşan teslim tarihlerini (48 saat içinde) ve gecikmiş kitapları gösterir.
- Bildirime tıklamak öğrenciyi ilgili Ödünç listem veya Çantam bölümüne götürür.
- Bildirimler tek tek veya topluca okundu işaretlenebilir; okunmamış sayısı zil üzerinde görünür.
- Prototip bildirimleri uygulama içindedir; tarayıcı kapalıyken gönderilen anlık bildirimler henüz yoktur.

### Yardım ve destek

- Yardım alanı, ödünç isteme ve 24 saatlik teslim alma süreci, istek iptali, Çantam, puan/yorum ve hatırlatmalar hakkında sık sorulan soruları açar.
- Masaüstünde yan menüden, dar ekranda profil menüsündeki **Yardım ve destek** seçeneğinden ulaşılır.

### Kitapları keşfet

- Kitap adı, yazar, tür ve konu metninde arama.
- Keşfet listesini aşağı indikçe üçer kitaplık gruplar halinde yükleme; yeni kartlardan önce kısa bir yükleme animasyonu gösterme.
- Tür, uygunluk ve gerekirse raf konumuna göre filtreleme.
- Kartta kapak, başlık, yazar, tür, puan/yorum özeti ve kopya durumu.
- Kitap kapağına veya adına tıklayarak kitap ayrıntısı ekranına geçiş.
- Yazar adına tıklayarak o yazarın kitaplarının listelendiği sayfaya geçiş.
- Okuma listesine ekleme veya uygun kitapta **Ödünç iste** düğmesini kullanma.

### Kitap ayrıntısı

- Kitap künyesi: başlık, yazar, ISBN/barkod, tür, yayın bilgileri, raf ve açıklama.
- Toplam kopya ve rafta uygun kopya sayısı; aynı başlığın her fiziksel kopyası ayrı barkodla izlenir.
- Öğrenci yorumları ve yorum ekleme alanı. Keşif kartında yalnızca yorum sayısı görünür; kitap kapağına veya adına tıklamak ayrıntı sayfasını açar.
- Öğrenci kitabı 1–5 yıldız arasında puanlayabilir; kendi puanı ayrıntı sayfasında görünür.
- Uygun kitapta **Ödünç iste** düğmesi; uygun değilse durum ve varsa istek/rezervasyon bilgisi.

### Ödünç listem

1. Katalog kartındaki **Ödünç iste** düğmesi, uygun bir kitabı doğrudan öğrencinin ödünç listesine ekler ve o kopya için 24 saatlik ayırmayı başlatır.
2. Öğrencinin aynı anda ödünç listesinde en fazla 3 etkin kitap isteği olabilir.
3. Öğrenci kitabı 24 saat içinde kütüphaneden fiziksel olarak alır. Personel kitap/kopyayı öğrenciye teslim ettiğini sistemde onaylar.
4. Personelin fiziksel teslim onayıyla istek ödünç kaydına dönüşür; son teslim tarihi personel tarafından kaydedilir.
5. 24 saat içinde teslim alınıp personelce onaylanmayan ayırma otomatik sona erer. İstek zaman aşımına uğrar ve kopya yeniden uygun hale gelir.
6. Öğrenci kalan süreyi izleyebilir ve teslim almadan önce isteğini iptal edebilir. İptal edilen kitap ödünç listesinden kaldırılır ve ayrılan kopya yeniden uygun hale gelir.

### Çantam: şu an bende olan kitaplar

- Yalnızca personelin fiziksel teslimini onayladığı ve henüz iade edilmemiş ödünçler burada görünür.
- Son teslim tarihi, kalan süre ve gecikme uyarısı her ödünç kaydında gösterilir.
- İade işlemini personel kaydeder; öğrencinin kitap listesindeki okuma işareti ödünç kaydını kapatmaz. Çantam kartındaki eylem “Okuyorum” olarak adlandırılır.

### Okuma listeleri

- **Okumak istediklerim:** Öğrencinin daha sonra okumayı planladığı kitaplar.
- **Okuduklarım:** Tamamlandı olarak işaretlenen kitaplar. Bu liste, ödünç kaydıyla otomatik eş tutulmaz; öğrenci okuduğunu kendisi işaretleyebilir.
- Öğrenci kendi listelerini düzenler; başkalarının kişisel listelerini göremez.

### Yorumlar

- Giriş yapmış öğrenci kitap için puan ve metin ekleyebilir.
- Yorum düzenleme/silme hakkı ve yorumun herkese açık olup olmayacağı okul kararıyla belirlenir.
- Personel uygunsuz içerik için gizleme ve moderasyon kaydı yapabilir.

## 3. Personel ekranları

### Özet paneli

- Katalogdaki aktif kitap ve kopya sayısı.
- Ödünçteki, iade edilen ve gecikmiş kayıtlar.
- İşlem bekleyen ödünç istekleri.
- Son işlemler ve hızlı arama.

### Kitap kataloğu yönetimi

- Kitap künyesi ekleme/düzenleme ve yayından kaldırma.
- Bir kitap başlığına bağlı birden çok fiziksel kopya/barkod yönetimi.
- Raf, kopya durumu ve sayım düzeltmeleri.
- Silme yerine geçmiş kayıtları koruyan arşivleme.

### Ödünç isteği ve dolaşım yönetimi

- İstekleri tarih, öğrenci ve duruma göre listeleme; 24 saatlik teslim alma süresini izleme.
- Öğrencinin etkin ödünç listesinde en fazla 3 istek bulunmasını sağlama; dolan/iptal edilen istekleri bu sınıra dahil etmeme.
- Öğrencinin aktif ödünç sınırını ve kopya uygunluğunu kontrol etme.
- 24 saatlik ayırmayı gerektiğinde iptal etme; iptal eden personeli ve gerekçeyi kaydetme.
- Öğrencinin fiziksel olarak getirdiği/kütüphaneden aldığı kitabı barkodla eşleyip teslimi onaylama; teslim zamanı ve vadeyi kaydetme.
- Süresi dolan, teslim edilmeyen ayırmayı otomatik kapatma; kopyayı yeniden uygun duruma getirme.
- İadede kopyanın durumunu kontrol ederek kaydı kapatma.
- Gecikmeyi vade tarihine göre hesaplama; kurumsal kurala göre takip etme.

### Öğrenci ve personel yönetimi

- Okul numarası, ad-soyad, sınıf/şube ve hesap aktifliği.
- Personel rolü: yönetici, kütüphaneci veya sınırlı işlem personeli.
- Öğrenci/personel hesabını etkinleştirme ve kapatma; gereksiz kişisel veriyi saklamama.

## 4. Temel kayıtlar

| Kayıt | Önerilen alanlar |
|---|---|
| Kitap | Kitap kimliği, ISBN, başlık, yazar, tür, açıklama, yayın bilgisi, kapak, raf, aktiflik |
| Fiziksel kopya | Kopya kimliği/barkod, kitap kimliği, durum, raf, son işlem zamanı |
| Kullanıcı | Hesap kimliği, okul numarası veya personel kimliği, ad-soyad, rol, sınıf/şube, aktiflik |
| Ödünç isteği/ayırma | İstek kimliği, öğrenci, kitap/kopya, oluşturulma zamanı, 24 saatlik bitiş zamanı, teslim onayı veya zaman aşımı durumu, işlemi yapan personel ve işlem zamanı |
| Ödünç kaydı | Kopya, öğrenci, teslim eden personel, teslim zamanı, vade, iade zamanı, durum |
| Okuma listesi | Öğrenci, kitap, liste türü, eklenme ve tamamlanma zamanı |
| Yorum | Öğrenci, kitap, puan, metin, oluşturma zamanı, görünürlük ve moderasyon durumu |
| İşlem geçmişi | İşlemi yapan kullanıcı, işlem türü, ilgili kayıt, zaman, gerekli değişiklik özeti |

## 5. Akış kuralları

- Terimler: **Ödünç iste** kopyayı 24 saat ayırır ve kitabı **Ödünç listem**e ekler. **Çantam** yalnızca personelin teslimini onayladığı, öğrencide bulunan kitapları gösterir. İstek için ayrı bir personel onay/ret adımı yoktur; personel yalnızca fiziksel teslimi onaylar veya ayırmayı iptal eder.
- Bir kitap başlığının birden çok fiziksel kopyası olabilir; her kopyanın kendine ait barkodu ve durumu bulunur.
- Aynı fiziksel kopya aynı anda en fazla bir etkin 24 saatlik ayırmada veya bir açık ödünç kaydında olabilir.
- Ayırma bir başlığın tüm kopyalarını değil, uygun fiziksel kopyalardan yalnızca birini tutar. Başka uygun kopyalar katalogda ödünç alınabilir durumda kalır.
- Katalog başlık düzeyinde toplam ve uygun kopya adetlerini gösterir; dolaşım ve işlem geçmişi kopya düzeyinde izlenir.
- Öğrenci **Ödünç iste** dediğinde 24 saatlik ayırma başlar; süre bu işlem anından itibaren hesaplanır.
- Süre içinde fiziksel teslim personel tarafından onaylanırsa ayırma ödünç kaydına dönüşür. Teslim onayı yoksa sistem ayırmayı zaman aşımına uğratıp kopyayı yeniden uygun yapar.
- İade sırasında hasarlı/kayıp durumu ayrıca kaydedilmelidir; kopya otomatik olarak rafta görünmemelidir.
- Yorumlar ve öğrencilerin okuma listeleri ödünç işlemi için zorunlu değildir.
- Tarihler yerel saat diliminde gösterilmeli; kayıtların sunucu tarafında tutarlı zaman bilgisi olmalıdır.

## 6. Okul ile netleştirilecekler

- Okulun kullandığı öğrenci/personel kimlik sistemi ve uygulamanın internet erişim sınırı.
- Aynı anda ödünç alınabilecek kitap sayısı, ödünç süresi ve uzatma kuralı.
- 24 saatlik ayırmanın takvim saati olarak uygulanması ve öğrenciye gösterilen kesin bitiş saati biçimi.
- Süresi dolan ayırma sonrası aynı kitaba sırada başka öğrenci varsa nasıl devredileceği.
- Yorumların görünürlüğü, yaşa uygun moderasyon ve şikâyet süreci.
- Okuma listesi/yorum verisinin ne kadar tutulacağı ve mezun/ayrılan kullanıcı hesabının kapatılması.
- Kitap kayıtlarında ISBN ve barkod kullanımının kapsamı.
