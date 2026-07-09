# Uzaklaşınca Otomatik Kilitlenme

> Kumandayla/anahtarla uzaklaşınca kapıların kendiliğinden kilitlenmesi (walk-away auto lock).

## Durum

- **Durum:** 📋 Planlama
- **Öncelik:** Orta
- **Tahmini bütçe:** ~$150–250 USD (aftermarket) veya TR anahtarcı fiyatı değişken
- **Zorluk:** Orta (smart key var — avantaj)
- **Oluşturulma:** 2026-07-09
- **Son güncelleme:** 2026-07-09

## Motivasyon

Araçtan inip uzaklaşırken kilit tuşuna basmayı unutmak. Fabrika özelliği olarak yok; aftermarket veya anahtarcı çözümü gerekir.

## Araç durumu (doğrulandı)

- **Smart Key + START/STOP düğmesi** — walk-away lock için doğru donanım mevcut
- Proximity algılama altyapısı zaten var (kapı kolundan dokunarak kilitleme çalışıyor)
- **Manuel vites** — bazı all-in-one paketleri (MyKeyPremium) bu yüzden eleniyor

## Araştırma Özeti

### Fabrika durumu

- 2012 Hyundai ix35'te **walk-away auto lock fabrikadan gelmiyor**.
- Smart key donanımı var ama özellik yazılımla aktif değil.

### ❌ Elenen: MyKeyPremium

MyKeyPremium (walk-away + remote start paketi):
- Manuel vitesle **uyumlu değil** — üretici açıkça belirtiyor
- Forumda manuel vitesli araç sahibi sipariş edip iade etmiş
- Bizim araç manuel → bu paket **kullanılamaz** (hem kilit hem uzaktan çalıştırma için)

### Seçenek A — Türkiye anahtarcı paketi (en olası TR çözümü)

Anahtarcıda duyduğun "modül" büyük ihtimalle bu:

- Keyless Go / smart key modülü
- **Yaklaşınca açılma — uzaklaşınca kapanma**
- Bazen uzaktan çalıştırma da aynı pakette

**Artıları:** Yerel destek, kodlama dahil, smart key zaten var
**Eksileri:** Fiyat/kalite usta bağımlı; manuel vites + uzaktan çalıştırma birlikte sorulmalı

**Anahtarcıya sorulacak sorular:**
1. 2012 ix35 manuel vites + smart key — walk-away lock yapılabilir mi?
2. Uzaktan çalıştırma da aynı modülde mi?
3. Prins LPG ile uyumlu mu?
4. Garanti / geri dönüşüm (orijinal sisteme dönebilir miyiz?)

### Seçenek B — Shark Racing Proximity Smart Door Lock

- Hyundai/Kia için aftermarket proximity modül
- Walk-away lock/unlock
- **2012 ix35 uyumluluğu** satıcıya sorulmalı

### Seçenek C — Boyo iKeyFree Pro

- Telefon + proximity kilitleme
- Forumda kullanılmış; bug bildirimi var
- Daha az tercih edilir

### Seçenek D — Sadece "gecikmeli otomatik kilit"

Gerçek walk-away değil; kapı kapandıktan X saniye sonra kilitler. Smart key proximity kadar şık değil ama daha basit olabilir.

## Açık sorular

- [x] Smart key — evet (START/STOP)
- [ ] Otomatik katlanır ayna var mı?
- [ ] Mevcut kumanda kaç tuşlu?
- [ ] Türkiye'de güvenilir oto anahtarcı önerisi?
- [ ] Anahtarcıya fiyat araştırması yapıldı mı?

## İlk değerlendirme

| Kriter | Puan |
|--------|------|
| DIY uygunluğu | Düşük–Orta |
| Smart key avantajı | Yüksek — doğru donanım var |
| MyKeyPremium | ❌ Manuel uyumsuz |
| En olası TR yolu | Anahtarcı modül paketi |

## Linkler

- [Hyundai Forum — Walk Away Lock](https://www.hyundai-forums.com/threads/walk-away-automatic-door-locking.677371/)
- [MyKeyPremium — walk-away lock (otomatik vites)](https://mykeypremium.com/blogs/news/forgot-to-lock-car-walk-away-auto-lock-hyundai-kia)
- [MyKeyPremium technicals — manuel uyumsuz](https://mykeypremium.com/pages/technicals)
- [Hech — ix35 keyless seçenekleri (TR)](https://hech.com.tr/urun/hyundai-ix35-yedek-anahtar-fiyati/)

## Kararlar

| Tarih | Karar | Gerekçe |
|-------|-------|---------|
| 2026-07-09 | Smart key doğrulandı | START/STOP düğmesi var |
| 2026-07-09 | MyKeyPremium elendi | Manuel vites desteklemiyor |
| 2026-07-09 | TR anahtarcı öncelikli araştırma | Yerel çözüm + kodlama |

## Notlar

- Walk-away kilit, uzaktan çalıştırma projesinden **bağımsız** çözülebilir.
- Anahtarcı paketinde ikisi birlikte sorulursa fiyat avantajı olabilir.
- Uzaktan çalıştırma için Compustar+DroneMobile yolu ayrı değerlendiriliyor (bkz. diğer proje dosyası).
