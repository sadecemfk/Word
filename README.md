# Kantar Yönetim Sistemi

Araç/şoför ve operatör seçip **dara ve brüt değerlerini elle girdiğiniz**, net ağırlığı
otomatik hesaplayan ve tartım fişini A5 / 80mm rulo / A4 iki nüsha olarak yazdırabilen
tek dosyalık (statik) bir web uygulaması. Tüm veriler tarayıcıda (`localStorage`) tutulur;
sunucu gerekmez.

## Özellikler

- **Manuel tartım girişi:** Dara ve brüt kantardan okunan gerçek değer olarak girilir,
  **Net = Brüt − Dara** otomatik hesaplanır.
- **Otomatik (ve düzenlenebilir) alanlar:** Plaka kayıtlı araçtan, kantarcı/kepçe operatörü
  listeden, tarih-saat "şu an" olarak önden dolar; istenirse elle değiştirilir.
- **Sıralı belge no:** Her fişte artan sayaç (`localStorage`), elle de değiştirilebilir.
- **Araç ve operatör yönetimi:** Ayarlar ekranından kalıcı olarak eklenip silinir.
- **Baskı:** A5 fiş, 80mm termal rulo, veya A4'e işletme + şoför iki nüsha.
- **Operatör imzası:** `imzalar/` klasörüne görsel koyup eşleştirerek fişe basılabilir.

## Canlı Yayın (GitHub Pages)

1. Bu depoyu/dalı GitHub'a gönderin.
2. Repo **Settings → Pages**.
3. **Source:** "Deploy from a branch" seçin.
4. **Branch:** yayınlamak istediğiniz dalı ve `/ (root)` klasörünü seçin, **Save**.
5. Birkaç dakika sonra `https://<kullanıcı-adı>.github.io/<repo>/` adresinden açılır.

Uygulama `index.html` olduğundan Pages onu otomatik servis eder.

## Giriş Kodu

Açılışta haftalık bir giriş kodu istenir. Kod `HHAA` biçimindedir:
- `HH` = ayın kaçıncı haftası (`01`=1–7, `02`=8–14, `03`=15–21, `04`=22+)
- `AA` = ay (iki hane)

Örnek: ayın 7'si ve 11. ay → `0111`. Bu basit erişim kilidini kaldırmak isterseniz
`index.html` içindeki lisans kontrolünü çıkarabilirsiniz.

## Yerel Çalıştırma

`index.html` CDN'den React/Tailwind/Babel yüklediğinden dosyayı doğrudan çift tıklayıp
tarayıcıda açabilirsiniz (internet bağlantısı gerekir).
