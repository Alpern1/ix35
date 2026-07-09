# Uzaklaşınca Otomatik Kilitlenme

> Kumandayla/anahtarla uzaklaşınca kapıların kendiliğinden kilitlenmesi (walk-away auto lock).

## Durum

- **Durum:** 📋 Planlama
- **Öncelik:** Orta
- **Tahmini bütçe:** ~$150–250 USD (aftermarket modül) veya Türkiye'de anahtarcı fiyatı değişken
- **Zorluk:** Orta–Zor (anahtar tipine bağlı)
- **Oluşturulma:** 2026-07-09
- **Son güncelleme:** 2026-07-09

## Motivasyon

Araçtan inip uzaklaşırken kilit tuşuna basmayı unutmak. Fabrika özelliği olarak yok; aftermarket veya anahtarcı çözümü gerekir.

## Önemli ön bilgi — henüz doğrulanmadı

2012 ix35'te **iki farklı anahtar sistemi** var (donanıma göre):

| Tip | Nasıl anlaşılır? | Walk-away lock için |
|-----|------------------|---------------------|
| **Smart Key** (varsa) | Kontağa anahtar sokmuyorsun; START/STOP düğmesi var; kapı kolundan dokunarak kilitleme | Aftermarket proximity modüller **uygun aday** |
| **Klasik kumandalı anahtar** | Anahtarı kontağa takıp çeviriyorsun; kumandada kilit/aç/kaput tuşları | Gerçek "uzaklaşınca kilit" zor; farklı çözüm gerekir |

**→ Kullanıcıdan doğrulanacak: Hangi anahtar tipi var?**

## Araştırma Özeti

### Fabrika durumu

- 2012 Hyundai ix35'te **walk-away auto lock fabrikadan gelmiyor**.
- Yeni nesil Tucson/Palisade gibi modellerde bu özellik var; ix35'te yok.

### Seçenek A — Smart Key varsa: Aftermarket proximity modül

Yurtdışında Hyundai/Kia için popüler modüller:

| Ürün | Ne yapıyor? | Not |
|------|-------------|-----|
| **MyKeyPremium** | Uzaklaşınca kilit, yaklaşınca aç; bazı modellerde OEM kumandayla remote start | 2012 ix35 uyumluluğu **net değil** — satıcıya sorulmalı |
| **Shark Racing Proximity Smart Door Lock** | Benzer walk-away lock/unlock | Model yılı uyumluluğu kontrol edilmeli |
| **Boyo iKeyFree Pro** | Telefon + proximity kilitleme | Forumda kullanılmış; hata/bug bildirimi var |

**Nasıl çalışıyor (genel):** Modül aracın akıllı anahtar / CAN bus sistemine bağlanıyor; anahtar veya telefon belirli mesafeden uzaklaşınca kilitliyor.

**Artıları:** Tam istenen özellik (gerçek walk-away)
**Eksileri:** Türkiye'de bulmak/zor olabilir; kurulum teknik; uyumluluk riski

### Seçenek B — Türkiye anahtarcı: Smart key yükseltme

Türkiye'deki oto anahtarcılar (Hech, Rem Anahtar vb.) şu hizmetleri reklam ediyor:

- Keyless Go / anahtarsız giriş
- **Yaklaşınca kilit açılma — uzaklaşınca kilit kapama**
- Uzaktan çalıştırma (bazı paketlerde)

Bu genelde **yeni nesil smart anahtar + modül + kodlama** paketi demek. Anahtarcıda "modül" dediğin şey büyük ihtimalle bu.

**Artıları:** Yerel destek, kodlama dahil
**Eksileri:** Fiyat belirsiz; kalite usta/parçaya bağlı; immobilizer kodlama riski

### Seçenek C — Klasik kumanda varsa: Zamanlayıcılı otomatik kilit

Smart key yoksa "anahtar cebindeyken uzaklaşınca kilit" **teknik olarak mümkün değil** (araç anahtarı algılayamaz).

Alternatifler:
- Kapı kapandıktan X saniye sonra otomatik kilitleme modülü (Ioniq Guy tarzı — ama onlar yeni Hyundai modelleri için)
- Sadece "unutma" çözümü: mevcut kumandadaki kilit tuşu alışkanlığı

## Açık sorular

- [ ] Arabada **smart key mi** yoksa **klasik kontak anahtarı + kumanda** mı var?
- [ ] Otomatik katlanır ayna var mı? (bazı modüllerde yaklaşınca açma ile birlikte geliyor)
- [ ] Mevcut kumanda kaç tuşlu? (kilit / aç / bagaj / panic)
- [ ] Türkiye'de güvenilir bir oto anahtarcı önerisi var mı?

## İlk değerlendirme

| Kriter | Puan |
|--------|------|
| DIY uygunluğu | Düşük–Orta (smart key modülü kablolama gerektirir) |
| Maliyet riski (TR usta) | Orta–Yüksek |
| İstenen özelliğe yakınlık | Smart key varsa yüksek; klasik anahtarda düşük |

## Linkler

- [Hyundai Forum — Walk Away Lock tartışması](https://www.hyundai-forums.com/threads/walk-away-automatic-door-locking.677371/)
- [MyKeyPremium — walk-away lock](https://mykeypremium.com/blogs/news/forgot-to-lock-car-walk-away-auto-lock-hyundai-kia)
- [Shark Racing — Proximity Door Lock](https://sharkracing.com) _(model uyumluluğu sorulacak)_
- [Hech — ix35 yedek anahtar / keyless seçenekleri (TR)](https://hech.com.tr/urun/hyundai-ix35-yedek-anahtar-fiyati/)

## Kararlar

| Tarih | Karar | Gerekçe |
|-------|-------|---------|
| 2026-07-09 | Önce anahtar tipi netleştirilecek | Çözüm yolu tamamen buna bağlı |

## Notlar

- Kullanıcı anahtarcıda modül olduğunu duymuş — bu muhtemelen smart key upgrade paketinin parçası.
- Bu proje, Proje 2 (uzaktan çalıştırma) ile **aynı anahtarcı/modül paketinde** birleştirilebilir; fiyat araştırmasında ikisini birlikte sormak mantıklı.
