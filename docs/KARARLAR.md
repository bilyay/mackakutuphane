# Karar kaydı

Bu dosyada ürün ve teknik kararlar, nedenleri ve durumlarıyla tutulur. Kesinleşmemiş teknik tercihler karar olarak işaretlenmez.

## 2026-10-31 — Öğrenci ve personel alanları birlikte tasarlanacak

- **Karar:** Ürün hem öğrencilere açık katalog/okuma özelliklerini hem de yetkili personelin kitap ve ödünç yönetimini kapsayacak.
- **Gerekçe:** İstenen süreçler öğrencinin keşif ve okuma deneyimini, kütüphane personelinin operasyonlarıyla birleştiriyor.
- **Durum:** Ürün kapsamı kararı.

## 2026-10-31 — Ödünç için fiziksel teslim alma penceresi 24 saat

- **Karar:** Öğrenci **Ödünç iste** dediğinde kopya 24 saat öğrenciye ayrılır. Öğrenci bu süre içinde kütüphaneden fiziksel teslim almalı ve personel teslimi sistemde onaylamalıdır.
- **Süre bitimi:** Onay gelmezse ayırma zaman aşımına uğrar ve kitap yeniden uygun duruma geçer.
- **Gerekçe:** Uzaktan istek ile fiziksel kütüphane teslimini birbirinden ayırmak ve kopyaların uzun süre sahipsiz rezerve kalmasını önlemek.
- **Durum:** Kullanıcı tarafından belirlenmiş iş kuralı. Gerçek sistemde süre ve kopya kilidi sunucu tarafında uygulanmalı.

## 2026-10-31 — Stok ve ayırma fiziksel kopya düzeyinde izlenecek

- **Karar:** Aynı başlığın birden fazla kopyası ayrı fiziksel envanter kayıtları olarak tutulacak. Her kopyanın kendine ait barkodu ve durumu olacak.
- **Ayırma etkisi:** 24 saatlik istek yalnızca uygun fiziksel kopyalardan birini ayırır; aynı başlığın diğer uygun kopyaları erişilebilir kalır.
- **Gerekçe:** Başlık düzeyinde tek bir uygunluk işareti birden fazla kopyanın durumunu doğru yansıtmaz.
- **Durum:** Kullanıcı tarafından netleştirilen ürün kuralı; prototipte adet bazlı örnekle modellenmiştir. Gerçek uygulama kopya barkodlarını ayrı kaydetmelidir.

## 2026-10-31 — Ödünç listesi ve Çantam farklı amaçlara sahip

- **Karar:** Kitap kartında **Ödünç iste** düğmesi bulunur; tıklama uygun kopyayı 24 saat ayırıp öğrencinin ödünç listesine ekler. Etkin ödünç listesi en fazla 3 kitap tutar.
- **Karar:** **Çantam**, bekleyen istekleri değil, personelin teslimini onayladığı ve halen öğrencide bulunan kitapları gösterir. Teslim tarihi ve gecikme uyarıları burada bulunur.
- **Karar:** Öğrenci bekleyen isteği iptal ettiğinde kitap Ödünç listem görünümünden kaldırılır ve kopyanın ayırması bırakılır.
- **Gerekçe:** İstek/rezervasyon ile fiziksel olarak ödünç alınmış kitabı arayüzde ayırmak.
- **Durum:** Kullanıcı tarafından belirlenmiş ürün akışı. Aktif ödünçlerin üst sınırı ayrıca tanımlanmadı; üç kitap kuralı ödünç isteği listesine uygulanır.

## 2026-10-31 — Ödünç isteği teslim onayından ayrı tutulacak

- **Karar:** Öğrencinin ödünç isteği tek başına ödünç verilmiş sayılmayacak. İstek anında kopya 24 saat ayrılır; personel onayı yalnızca fiziksel teslimde verilir. İstek için ayrıca onay/ret adımı yoktur; personel gerekirse ayırmayı iptal edebilir.
- **Gerekçe:** Kopya mevcudu ve kimin sorumlu olduğu doğru takip edilmeli.
- **Durum:** Önerilen iş kuralı; okulun ödünç prosedürüyle doğrulanmalı.

## 2026-10-31 — İlk arayüz prototipi istemci tarafında

- **Karar:** İlk ekran denemesi düz HTML, CSS ve JavaScript ile, örnek veri ve tarayıcı `localStorage` kullanılarak hazırlandı.
- **Gerekçe:** Kullanıcı akışlarını sunucu kurulumundan önce görünür kılmak.
- **Sonuç:** Bir cihazdaki deneme verileri başka cihazlarla paylaşılmaz; bu yaklaşım yayın sürümü için yeterli değildir.
- **Durum:** Prototip kararı; üretim teknolojisi seçimi değildir.

## 2026-10-31 — Terimler ve kitap ayrıntı sayfası

- **Karar:** Düğme ve belgelerde tek ifade kullanılır: **Ödünç iste**. Üç kavram ayrı tutulur: Ödünç listem (24 saatlik ayırmalar), Çantam (teslim alınmış kitaplar), okuma listeleri.
- **Karar:** Yorumlar tarayıcı `prompt()` penceresi yerine kitap ayrıntı sayfasında yazılır; yorum metni HTML olarak değil düz metin olarak gösterilir.
- **Karar:** Görsel dosya adları boşluksuz ve ASCII olur (`okul_logosu.jpg`, `okul_gorseli.jpg`).
- **Hata düzeltmesi:** **Ödünç iste** ile eklenen kayıt, kopya numarası hesaplanırken istek listesi yeniden oluşturulduğu için kayboluyordu. Kopya numarası artık kayıt eklenmeden önce hesaplanıyor ve kayıt yeni bir diziyle ekleniyor.
- **Durum:** Prototip ve belge tutarlılığı kararı.

## 2026-10-31 — Yorumlar kitap ayrıntı sayfasında

- **Karar:** Kitap kartlarında yorum yazma alanı bulunmaz; yalnızca yorum sayısı gösterilir. Kitap kapağı veya başlığı ayrıntı sayfasını açar; yorumlar bu sayfada okunur ve yeni yorum eklenir.
- **Karar:** Ayrıntı sayfasında mevcut uygun kopya sayısı gösterilir; toplam kopya sayısı ayrıca yazılmaz. Ödünç iste düğmesi bu sayfada da bulunur.
- **Gerekçe:** Keşif ekranını sade tutup yorum akışını kitabın açıklama ve uygunluk bilgileriyle aynı yerde toplamak.
- **Durum:** Kullanıcı tarafından belirlenmiş arayüz tercihi; prototipte uygulandı.

## 2026-10-31 — Kitaba 1–5 yıldız puanı verme

- **Karar:** Öğrenci kitap ayrıntı sayfasından kitaba 1–5 yıldız arasında puan verebilir ve kendi seçimini değiştirebilir.
- **Durum:** Prototipte öğrenci puanı bu tarayıcıda saklanır; ortak puan ortalaması sunucuya bağlı değildir.

## 2026-10-31 — Çantam kartlarındaki okuma metni

- **Karar:** Çantam kartlarında “Örnek ödünç kaydı” etiketi gösterilmez. (Okuma eylemi metni 2026-11-01 tarihli kararla güncellendi.)
- **Durum:** Örnek etiketini kaldırma kararı prototipte uygulandı; eylem metni için aşağıdaki güncel karar geçerlidir.

## 2026-11-01 — Öğrenci kitap kartları menüye göre içerik gösterecek

- **Karar:** Kitap kartlarının temel görsel yapısı ortak kalacak; kartın durum bilgisi ve eylemi seçili menüye göre değişecek. Ödünç listem ayırma süresi ve iptal eylemini, Çantam son teslim/gecikme bilgisini ve “Okudum” eylemini, Okumak istediklerim liste durumunu ve ödünç isteğini, Okuduklarım ise okundu durumunu ve puanlama/yorum bağlantısını gösterir.
- **Karar:** Yıldız ortalaması ile yorum adedi kartın aynı satırında ve eşit yazı boyutunda gösterilir.
- **Gerekçe:** Ortak kart görünümünü korurken her listenin amacı ve ilgili eylemleri belirgin olsun.
- **Durum:** Kullanıcı tarafından belirlenmiş arayüz tercihi; prototipte uygulandı.

## 2026-11-08 — Keşfet listesinde kademeli yükleme

- **Karar:** Keşfet ekranında ilk üç kitap gösterilir; öğrenci sayfayı aşağı kaydırdıkça kısa bir yükleme animasyonundan sonra sonraki üç kitap eklenir.
- **Gerekçe:** Uzun kataloglarda tüm kitapları ilk anda yüklemeden keşif akışını sürdürmek.
- **Durum:** Prototipte uygulandı.

## 2026-11-08 — Yazar adına göre kitapları keşfetme

- **Karar:** Kitap kartı ve ayrıntı sayfasındaki yazar adı tıklanabilir olur; tıklama yalnızca o yazara ait kitapları gösteren bir sayfa açar.
- **Durum:** Prototipte uygulandı.

## 2026-11-08 — Profil menüsü kısayolları

- **Karar:** Profil alanı açılır menü olur; menüde öğrencinin adı/sınıfı ve Ödünç listem, Çantam, Okumak istediklerim, Okuduklarım kısayolları bulunur.
- **Gerekçe:** Öğrenci hesabı bilgilerini gösterirken kişisel kitap bölümlerine üst menüden de erişmek.
- **Durum:** Prototipte uygulandı; hesap doğrulama ve çıkış işlemleri gerçek kimlik doğrulama eklendiğinde bağlanacak.

## 2026-11-08 — Öğrenci profil bilgilerini düzenleme

- **Karar:** Öğrenci profil sayfasında sınıf düzeyi, şube, e-posta ve telefon bilgilerini güncelleyebilir; şifresini de değiştirebilir.
- **Durum:** Prototipte bilgiler tarayıcıda saklanır. Şifre yerel prototip kaydı olarak özetlenir; gerçek okul hesabı şifresi için sunucu kimlik doğrulaması gerekir.

## 2026-11-08 — Hatırlatma zili

- **Karar:** Zil, 24 saatlik ödünç istekleri için etkin uyarı, son 6 saatte acil uyarı, 48 saat içinde yaklaşan teslim tarihleri ve gecikmiş kitaplar için uygulama içi bildirim listesi açar. Okunmamış bildirim sayısı zilde görünür; bildirime tıklamak ilgili listeyi açar.
- **Durum:** Okundu bilgisi bu tarayıcıda saklanır. Tarayıcı kapalıyken anlık bildirim gönderimi sunucu altyapısı gerektirir ve prototip kapsamı dışındadır.

## 2026-11-08 — Yardım ve destek alanı

- **Karar:** Yardım alanı; ödünç isteği, 24 saatlik teslim, iptal, Çantam, yorum/puan ve hatırlatma konularını açıklayan SSS penceresi açar. Dar ekranda profil menüsünden de erişilir.
- **Gerekçe:** Öğrencilerin temel işlemleri ek destek almadan anlayabilmesi ve yardımın mobil görünümde de bulunması.
- **Durum:** Prototipte uygulandı.

## 2026-11-08 — Footer okul adı

- **Karar:** Footer’da okul adı “Yıldız Teknik Üniversitesi Maçka Mesleki ve Teknik Anadolu Lisesi” olarak gösterilir.
- **Durum:** Kullanıcı tarafından belirlenmiş kurumsal adlandırma tercihi; prototipte uygulandı.

## 2026-11-01 — Görsel okunabilirlik ve favicon

- **Karar:** Öğrenci arayüzünde küçük metinler büyütülüp mobil ölçülere göre ayarlanır; stok etiketi kitap kapağının arkasında kalmaz.
- **Karar:** Favicon, okul logosuna eşlik eden koyu yeşil zemin üzerinde küçük “m” harfini kullanır. Harf site arayüzünün ana yazı tipi DM Sans ile çizilir; SVG içinde Arial/sans-serif yedeği bulunur.
- **Gerekçe:** Metinlerin farklı ekranlarda okunması ve sitenin görsel diliyle uyumlu bir sekme simgesi.
- **Durum:** Kullanıcı tarafından belirlenmiş görsel tercihler; prototipte uygulandı.

## 2026-11-01 — Çantamda okuma eylemi

- **Karar:** Çantam kartındaki “Okuyorum” eylemi “✓ Okudum” olarak adlandırılır; eylem kitabı Okuduklarım listesine ekler.
- **Gerekçe:** Eylem, kullanıcı kitabı bitirdiğinde kullanılacağı için görünen metin sonucu açıkça anlatır.
- **Durum:** Kullanıcı tarafından belirlenmiş arayüz tercihi; prototipte uygulandı.

## Açık kararlar

- Okul hesabı entegrasyonu mu, uygulama içi hesap mı kullanılacak?
- Uygulama hangi kurum sunucusunda veya barındırma ortamında çalışacak?
- Yorumlar herkese mi, giriş yapan öğrencilere mi açık olacak; moderasyonu kim yapacak?
- Ödünç süresi, uzatma, aynı anda alınabilecek kitap sayısı ve gecikme yaklaşımı ne olacak?
- 24 saatlik ayırma sona erince sırada bekleyen öğrenciye kopya otomatik teklif edilecek mi?
- Öğrenci kayıtlarını hangi yetkili oluşturacak ve hesaplar okuldan ayrılınca nasıl kapatılacak?
