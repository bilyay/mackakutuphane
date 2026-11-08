# Proje kapsamı

Son güncelleme: 1 Kasım 2026

## Amaç

Lise kütüphanesindeki kitap kayıtlarını ve ödünç/iade işlemlerini düzenli takip etmek; öğrencilere katalog, okuma listesi ve yorum özellikleri sunmak.

## Kullanıcı grupları

### Öğrenci

- Kitap kataloğunu uzaktan görüntüler; başlık, yazar ve türe göre arar.
- Kitabın uygunluk durumunu inceler.
- Uygun kitapta **Ödünç iste** düğmesini kullanır; kitap 24 saatlik ayırmayla Ödünç listesine eklenir.
- Okumak istediklerini ve okuduklarını listeler.
- Kitap ayrıntı sayfasında 1–5 yıldız arasında puan verir.
- Kitaplara yorum yazar.

### Kütüphane personeli

- Yetkili hesapla giriş yapar.
- Kitap ve kopya kayıtlarını oluşturur, günceller ve arşivler.
- Öğrenci kayıtlarını ve ödünç/iade işlemlerini yönetir.
- Bekleyen 24 saatlik ayırmaları izler, gerekirse iptal eder; fiziksel teslimi onaylar, vade ve iade tarihlerini kaydeder.
- Gecikenleri ve mevcut kitap durumlarını izler.

### Yönetici

- Personel hesaplarını ve yetki rollerini yönetir.
- Sistem ayarları ile işlem kayıtlarına erişir.

## İlk sürümde hedeflenen özellikler

1. Öğrenci ve personel için rol bazlı oturum açma.
2. Kitap kataloğu: ad, yazar, ISBN, tür, raf, açıklama ve kapak; her fiziksel kopya için ayrı barkod ve durum.
3. Öğrenci görünümü: arama, tür filtresi, uygunluk, kitap ayrıntısı, yazara ait kitaplar ve yorumlar.
4. Öğrenci listeleri: 3 kitaba kadar olan 24 saatlik ödünç listesi, çanta (personelin onayladığı ve öğrencideki kitaplar), okumak istediklerim ve okuduklarım.
   - Kitap kartlarının ortak görsel düzeni korunur; her menü kendi durum bilgisini ve ilgili eylemi gösterir. Kartlarda yıldız ortalaması yanında yorum sayısı yer alır.
5. Ödünç akışı: 24 saat içinde fiziksel teslim ve personel onayı, vade, iade ve gecikme durumu.
6. Personel paneli: katalog, öğrenci kayıtları, bekleyen istekler, ödünçtekiler ve gecikenler.
7. İşlem geçmişi: işlemi yapan personel ve zaman bilgisi.

## Kurallar ve sınırlar

- Öğrenci **Ödünç iste** dediğinde seçilen kopya 24 saat için öğrenciye ayrılır. Bu işlem tek başına fiziksel teslim veya tamamlanmış ödünç anlamına gelmez.
- Öğrenci 24 saat içinde kitabı kütüphaneden fiziksel olarak almalı; personel teslimi sistemde onaylamalıdır. Onay gelmezse ayırma sona erer ve kopya yeniden uygun olur.
- Öğrenci kataloğunda **Ödünç iste** düğmesini kullanır; istek doğrudan ödünç listesine eklenir. Etkin ödünç listesinde en fazla 3 kitap olabilir.
- Öğrenci isteği iptal ettiğinde kitap ödünç listesinden kaldırılır ve kopya yeniden uygun olur.
- **Çantam**, istek sepeti değildir. Sadece personelin fiziksel teslimini onayladığı, henüz iade edilmemiş kitapları ve bunların son teslim/gecikme durumlarını gösterir.
- Etkin ayırma sırasında yalnızca ayrılan fiziksel kopya başka öğrenciye verilemez. Aynı başlıktaki diğer uygun kopyalar erişilebilir kalır. Fiziksel teslim onayında o kopya ödünçteye geçer; iade onayında yeniden uygun olur.
- Yalnızca giriş yapmış yetkili personel yönetim işlemlerini yapabilir. Öğrenci hesapları kendi profillerine ve listelerine erişir.
- Öğrenci bilgileri için yalnızca okul akışının gerektirdiği veriler tutulur. Yorumlar yayımlanmadan önce moderasyon/şikâyet ihtiyacı değerlendirilir.
- Öğrenci profili, yorum görünürlüğü, kitap ödünç süresi, uzatma ve gecikme kuralları okul yönetimiyle netleştirilmelidir. Kitabı teslim almak için tanınan ayırma süresi 24 saattir.

## Prototip ile gerçek sistem arasındaki fark

Mevcut `app.js` 15 örnek kitap kullanır ve kullanıcı verisini aynı tarayıcıda `localStorage` ile saklar. Keşfet kataloğu ilk üç kitabı gösterir, sayfa aşağı kaydırıldıkça kısa bir animasyonun ardından üçer kitap daha yükler. Profil menüsü ödünç ve okuma bölümlerine kısayol verir. Profil sayfasında sınıf/şube, e-posta ve telefon bilgileri düzenlenebilir; şifre güncelleme prototip kaydı olarak saklanır ve gerçek okul hesabına bağlı değildir. Hatırlatma zili, aktif ödünç istekleri, yaklaşan teslim tarihleri ve gecikmeler için uygulama içi uyarılar gösterir; tarayıcı kapalıyken bildirim göndermez. Yardım alanı temel kullanım sorularını yanıtlayan bir SSS penceresi açar. Footer’da “Yıldız Teknik Üniversitesi Maçka Mesleki ve Teknik Anadolu Lisesi” adı gösterilir. İlk açılışta Çantam’da biri süresi yaklaşan, biri gecikmiş iki örnek ödünç kaydı ve Okuduklarım’da iki örnek kitap gösterilir. Kitap ayrıntı sayfasında yorumlar okunup eklenebilir, 1–5 yıldız puanı verilebilir ve ödünç isteği oluşturulabilir; katalog kartında yalnızca yorum sayısı görünür. Ayrıntıda yalnızca uygun kopya adedi gösterilir. Çantam kartlarında örnek ödünç etiketi gösterilmez. Öğrenci görünümünde ödünç seçimi 24 saatlik yerel bir ayırma ve geri sayım örneği oluşturur. Kimlik doğrulama, ortak sunucu/veritabanı, personel tarafından gerçek teslim onayı, eş zamanlı kopya kilidi, kalıcı kullanıcıya bağlı puan/yorumlar ve kurum dışı erişim henüz uygulanmamıştır. Bu nedenle prototip ayırması gerçek öğrenciler arasında kopya rezerve etmez.

## İlk sürüm dışında

Kitap satın alma, çevrim içi ödeme, otomatik SMS/e-posta, dış kütüphane kataloglarına entegrasyon ve gelişmiş raporlama ilk sürümün zorunlu kapsamına dahil değildir.
