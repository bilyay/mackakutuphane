# Maçka Kütüphane

Maçka Mesleki ve Teknik Anadolu Lisesi için öğrencilerin kitapları keşfedebildiği, en fazla üç kitaplık ödünç isteği listesi oluşturabildiği ve teslim alınan kitapları son teslim tarihleriyle izleyebildiği; yetkili personelin de katalog ve ödünç süreçlerini yönettiği bir kütüphane uygulaması.

## Proje durumu

Proje şu anda tarayıcıda açılabilen bir arayüz prototipidir. Kitap kataloğu ve ekran tasarımı örnek veriler kullanır. İlk açılışta Çantam ve Okuduklarım görünümlerinde arayüzü göstermek için örnek kayıtlar eklenir. Çanta, okuma listesi, yorum ve ödünç isteği kayıtları tarayıcıdaki `localStorage` alanında tutulur. Bu kayıtlar kullanıcılar ve cihazlar arasında paylaşılmaz. Kitap kartındaki **Ayrıntı ve yorumlar** düğmesi kitap ayrıntısını ve yorum alanını açar. Gerçek uzaktan kullanım için sunucu, ortak veritabanı ve kimlik doğrulama gerekir.

## Başlatma

Bu prototipi denemek için `index.html` dosyasını güncel bir tarayıcıda açın. Okul logosu ve fotoğrafı göreli dosya yolu ile yüklendiğinden, `okul_logosu.jpg` ve `okul_gorseli.jpg` dosyaları proje klasöründe kalmalıdır.

## Bilinen sınırlar

Prototipte ayırmalar yalnızca bu tarayıcıda geçerlidir. Başka bir cihazda veya tarayıcıda aynı kopya başka bir öğrenciye ayrılmış görünebilir. Eski kayıtlar takılırsa sayfayı Ctrl+Shift+R ile yenileyin.

## Dosyalar

- `index.html`, `styles.css`, `app.js`: Öğrenci arayüzü prototipi
- `okul_logosu.jpg`, `okul_gorseli.jpg`: Kurum görselleri
- `docs/PROJE_KAPSAMI.md`: Gereksinimler, kullanıcılar ve sınırlar
- `docs/IS_AKISLARI.md`: Öğrenci/personel ekranları, süreç adımları ve kayıt modeli taslağı
- `docs/YOL_HARITASI.md`: Önerilen geliştirme aşamaları ve tamamlanma ölçütleri
- `docs/KARARLAR.md`: Ürün ve uygulama kararlarının kaydı

## Belgeler nasıl güncel tutulur?

Kapsam veya kullanıcı akışı değiştiğinde `docs/PROJE_KAPSAMI.md` güncellenir. Teknoloji ve veri tasarımı kararları `docs/KARARLAR.md` dosyasına tarih ve gerekçeleriyle eklenir. Yeni aşama, tamamlanma ölçütleri ve ilerleme `docs/YOL_HARITASI.md` dosyasında izlenir. README, uygulamanın mevcut durumunu yansıtacak şekilde tutulur.
