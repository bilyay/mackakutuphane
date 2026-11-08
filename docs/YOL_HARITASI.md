# Geliştirme yol haritası

Son güncelleme: 8 Kasım 2026

## Aşama 0 — Arayüz prototipi

Durum: Başlangıç prototipi hazır.

- [x] Öğrenci kitap keşif ekranı ve örnek kitap kartları
- [x] Kaydırmalı yükleme davranışını göstermek için kataloğu 15 örnek kitaba çıkarma
- [x] Keşfet listesini sayfa kaydırıldıkça üçer kitap yükleme ve arada animasyonlu yükleme göstergesi sunma
- [x] Kart ve kitap ayrıntısındaki yazar adından yazara ait kitaplar sayfasını açma
- [x] Profil menüsünü açma/kapatma ve kişisel kütüphane bölümlerine kısayollar ekleme
- [x] Öğrenci profilinde sınıf/şube, e-posta ve telefon bilgilerini düzenleme; prototipte şifre güncelleme arayüzü
- [x] Hatırlatma zilinde ödünç süresi, yaklaşan teslim ve gecikme uyarıları; okundu durumu ve ilgili bölüme geçiş
- [x] Sık sorulan sorularla yardım penceresi ve mobil profil menüsünden erişim
- [x] Footer’da okulun tam adını gösterme
- [x] Arama ve tür filtresi
- [x] Çanta, okuma listesi ve okunanlar görünümleri
- [x] Ödünç isteği ve yorum etkileşimi için prototip akışları
- [x] Okul logosu ve bina fotoğrafını ekleme
- [ ] Prototipi okul kullanıcılarıyla gözden geçirip akış geri bildirimi toplama
- [x] Öğrenci/personel ekranlarını ve kayıt taslağını iş akışı belgesinde tanımlama
- [x] Ödünç alma için 24 saatlik fiziksel teslim ve personel onayı kuralını tanımlama
- [x] Öğrenci prototipinde 24 saatlik ayırma geri sayımı ve isteklerim görünümü
- [x] Prototipte başlık başına birden fazla kopya ve kopya bazlı 24 saatlik ayırma sayacı
- [x] “Ödünç iste” ile en fazla üç kitaplık istek listesi ve teslim onaylı kitaplar için Çantam akışı
- [x] Kitap ayrıntı sayfası: kapak ve başlık bağlantısı, yorumlar, yorum ekleme, 1–5 yıldız puanı ve ödünç iste
- [x] Katalog kartlarında yalnızca yorum sayısını gösterme; ayrıntıda toplam kopya yerine uygun adedi gösterme
- [x] Çantam kartlarından örnek kayıt etiketini kaldırma ve okuma tamamlama eylemini “Okudum” olarak adlandırma
- [x] Görsel dosya adlarını ASCII yapma, eski kayıtların aktif istekleri dışarıda bırakma hatasını giderme
- [x] “Ödünç iste” kaydının listeye eklenmeden kaybolması hatasını giderme (ekleme, ikinci istek ve iptal akışı denendi)
- [x] Öğrenci arayüzü küçük metinlerini büyütme ve mobil punto ayarlarını iyileştirme
- [x] Responsive kartlarda stok etiketini kapak görselinin önünde tutma
- [x] Menüye özgü kitap kartı durumlarını ve eylemlerini ekleme
- [x] Çantam kartındaki tamamlama eylemini “Okudum” olarak gösterme
- [x] Kartlarda yıldız ortalaması yanında yorum sayısını aynı boyut ve hizayla gösterme
- [x] Site yazı karakteriyle küçük “m” favicon oluşturma

## Aşama 1 — Gereksinimleri kesinleştirme

- [ ] Okulun mevcut öğrenci/personel hesaplarıyla oturum açma seçeneğini belirleme
- [ ] Öğrenci kimlik alanlarını ve hangi sınıfların erişeceğini belirleme
- [ ] Ödünç süresi, kitap başına sınır, yenileme ve gecikme kurallarını kararlaştırma
- [ ] Yorumların kimlere görüneceğini ve moderasyon akışını kararlaştırma
- [ ] Uygulamayı barındıracak kurum ortamını ve yedekleme sorumluluğunu belirleme

## Aşama 2 — Sunucu ve veri katmanı

- [ ] Teknoloji yığınını ve barındırma ortamını seçme
- [ ] Kitap, kopya, öğrenci, kullanıcı, ödünç, istek, yorum ve işlem geçmişi veri modelini oluşturma
- [ ] Güvenli oturum açma ve öğrenci/personel/yönetici rollerini kurma
- [ ] Erişim denetimini sunucuda uygulama; istemci kontrollerini tek başına güvenlik sınırı saymama
- [ ] Yedekleme, hata kaydı ve güvenli yapılandırmayı hazırlama

## Aşama 3 — Personel işlemleri

- [ ] Kitap ekleme, düzenleme, arşivleme ve kopya/barkod yönetimi
- [ ] Öğrenci arama ve kayıt yönetimi
- [ ] Bekleyen ayırmaları izleme/iptal etme ve fiziksel teslim onayı kaydı
- [ ] İade, gecikme ve mevcut kopya durumlarını yönetme
- [ ] İşlem geçmişini görüntüleme

## Aşama 4 — Öğrenci özelliklerini sunucuya bağlama

- [ ] Kataloğu gerçek kitap verisine bağlama
- [ ] Kişiye özel ödünç listesi, Çantam ve okuma listelerini sunucuda saklama
- [ ] Ödünç durumlarını ve teslim tarihlerini öğrenciye gösterme
- [ ] Yorum oluşturma, listeleme ve moderasyon akışını ekleme
- [ ] Mobil ve masaüstü kullanılabilirliğini gözden geçirme

## Aşama 5 — Kabul ve yayın

- [ ] Öğrenci ve personel rolleriyle temel senaryoları doğrulama
- [ ] Yetkisiz erişim ve başkasının verisini görme senaryolarını kontrol etme
- [ ] Yedekten geri yükleme adımını doğrulama
- [ ] Okulda sınırlı kullanıcı grubuyla pilot uygulama yapma
- [ ] Geri bildirime göre düzeltip kurum içi erişime açma

## Yayın öncesi kabul ölçütleri

- Öğrenci sadece katalogda erişime açılmış kitapları görür ve kendi listelerini yönetir.
- Öğrenci **Ödünç iste** ile kopya ayırabilir; ayırma uygun kopya sayısını düşürür ama aktif ödünç kaydı oluşturmaz. Süre dolarsa veya öğrenci iptal ederse kopya yeniden uygun olur.
- Personel fiziksel teslimi onaylayıp ayırmayı ödünç kaydına dönüştürebilir; iade kaydı kopya durumunu doğru günceller.
- Ödünç, iade ve katalog değişikliklerinin sorumlusu ve zamanı izlenebilir.
- Yetkisiz kullanıcı yönetim ekranlarına ve başka öğrencilerin kişisel kayıtlarına erişemez.
