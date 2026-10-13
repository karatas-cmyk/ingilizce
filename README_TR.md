# English Orbit - Tam site ve kaynak kod dışa aktarımı

Bu paket, 13 Ekim 2026 tarihinde mevcut sitenin son sürümünden alınmıştır.

## İçerik

- index.html: sitenin giriş sayfası.
- style.css: görünüm ve mobil düzen.
- course.js: altı seviyedeki 24 dersin içeriği.
- beginner.js: Türkçe destekli 16 başlangıç dersi ve eğitim hedefleri.
- coach.js: rehberli ders akışı, cevap kontrolü ve aralıklı tekrar.
- app.js: ayrıntılı beceri çalışmaları, ses, kayıt, kitaplar ve diğer temel işlemler.
- orbit.js: Three.js öğrenme haritası.
- vendor/: yerel Three.js dosyaları ve kütüphanenin lisansı.
- books/: toplu kurs kitabı, altı seviye kitabı ve dilbilim kitabı; toplam sekiz PDF.
- export_info.json: kaynak sürüm ve dışa aktarılan dosya bilgileri.
- SHA256SUMS.txt: özgün site dosyalarını doğrulamak için özetler.

## Bilgisayarda çalıştırma

1. ZIP dosyasını açın ve English_Orbit klasörüne girin.
2. Bu klasörde terminal açın.
3. Şu komutu çalıştırın:

    python3 -m http.server 8000 --bind 127.0.0.1

Windows'ta Python kurulumu uygunsa şu komut kullanılabilir:

    py -m http.server 8000 --bind 127.0.0.1

4. Tarayıcıda http://localhost:8000 adresini açın.
5. Sunucuyu durdurmak için terminalde Ctrl+C kullanın.

Python yüklüyse start_macos.command veya start_windows.bat dosyaları aynı işlemi başlatır. macOS dosyayı çalıştırmayı engellerse terminal komutunu kullanın.

index.html dosyasını doğrudan çift tıklamak yerine yerel sunucuyu kullanın. Three.js modül yüklemesi ve mikrofon özellikleri dosya adresinde kısıtlanabilir.

## Başka bir sunucuda yayınlama

Bu klasörün index.html, JavaScript, CSS, vendor ve books içeriklerini birlikte statik yayın dizinine yükleyin. index.html bu dizinin kökünde olmalıdır. npm kurulumu veya derleme adımı gerekmez. Klasörler arasındaki göreli yolları koruyun.

Sites hesabındaki giriş ve paylaşım koruması bu statik paketin parçası değildir. Başka bir sunucuda erişim ayarları o sunucudan yönetilir.

## Ses ve ilerleme

Seslendirme cihazın/tarayıcının İngilizce seslerine bağlıdır. Mikrofon için izin gerekir; yerel localhost veya HTTPS üzerinden kullanın. Tarayıcıların ses özellikleri değişebilir. Ses çalışmazsa okuma alternatifi vardır. PDF'lerde gömülü ses bulunmaz.

Öğrenci ilerlemesi tarayıcının localStorage alanında, englishOrbit anahtarıyla tutulur. Bu ZIP canlı tarayıcınızdaki kişisel ilerleme verilerini veya ses kayıtlarını içermez. Başka tarayıcı ya da alan adında ayrı bir ilerleme kaydı oluşur.

Three.js dosyaları pakette yereldir. Google Fonts yazı tipleri internetten istenir; internet yokken yedek yazı tipi kullanılır. Seçilen bazı sesler de internet bağlantısına bağlı olabilir.

## Düzenleme

Ders içeriğini course.js ve beginner.js içinde; rehberli öğretim akışını coach.js içinde; görünümü style.css içinde değiştirebilirsiniz. PDF dosyaları tamamlanmış kitaplar olarak dahildir. Three.js lisansı vendor/THREE-LICENSE.txt dosyasındadır.
