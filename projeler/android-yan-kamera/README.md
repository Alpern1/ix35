# Android’de sağ / sol kamera

> Android teypte manevrada sağı solu canlı görmek. 360 kuş bakışı değil.

## Durum

- **Durum:** 📋 Planlama
- **Öncelik:** Yüksek
- **Tahmini bütçe:** ~1.500–4.000 TL (teyp girişine göre)
- **Zorluk:** Orta (kablo + montaj; lehim şart değil)
- **Oluşturulma:** 2026-07-22
- **Son güncelleme:** 2026-07-22

## Araç bilgisi (ortak)

[araba/ozellikler.md](../../araba/ozellikler.md) · [araba/notlar.md](../../araba/notlar.md)

- Android aftermarket teyp **var** (marka/model henüz net değil → Adım 0 şart)
- 360 kamera **istenmiyor** (500–600$ teklif reddedildi / gereksiz)

## Motivasyon

Park / dar yer / şerit değişiminde kör nokta. Dashcam ayrı iş (kayıt); senin istediğin **ekranda canlı yan görüş**.

## Hedef

İki küçük kamera (sol + sağ) → kablo → Android teyp. Ekranda sol/sağ görüntü; tercihen sinyalle otomatik veya menüden elle.

## Mantık (çok kısa)

```
[Sol kamera] --video kablosu--> [Android teyp kamera girişi]
[Sağ kamera] --video kablosu--> [Android teyp kamera girişi]
     |                                |
  +12V (ACC veya teypten)          Ekranda gösterir
```

Teyp bir **TV gibi**: kamera “yayın” gönderir, teyp ekrana basar. 360’taki pahalı kısım (4 görüntüyü birleştirip kuş bakışı yapmak) yok.

Detay: [nasil-yapilir.md](nasil-yapilir.md) · [malzemeler.md](malzemeler.md)

## Önce şart: teybi tanı

Aşağıdakiler **bilinmeden parça alma**.

| Soru | Neden |
|------|--------|
| Marka / model / foto (arka soketler) | Giriş tipi değişir |
| Geri kamera girişi var mı? | Çoğu teypte en az 1 RCA/AHD var |
| Sol / sağ / ön giriş var mı? | Yoksa splitter veya sadece 1 ek kamera |
| Ayarlarda “Camera / 360 / AHD” menüsü? | AHD mi CVBS mi, tetik nasıl |
| Halihazırda geri kamera takılı mı? | Kablo yolu / güç ortak olabilir |

## Seçenekler

| Yol | Ne | Artı | Eksi |
|-----|----|------|------|
| **A — Önerilen** | Sol+sağ AHD → teybin left/right girişine | Temiz, 360 değil | Teypte 2 yan giriş lazım |
| **B** | Tek yan kamera (sürücü tarafı / park tarafı) | Ucuz, kolay | Tek taraf |
| **C** | Ucuz “360 kit” + 360 app | Kuş bakışı hayali | Kalibrasyon, kalite, çoğu teypte app yok |
| **D** | Sadece dashcam yan aynası | Kayıt | Android’de canlı yok — senin hedefin değil |

**Şu an seçim:** A (teyp uygunsa). Teypte yan giriş yoksa B veya giriş genişletme araştırılır.

## Açık sorular

- [ ] Android teyp marka/model + arka soket foto
- [ ] Kaç kamera girişi / AHD mı?
- [ ] Montaj yeri tercihi: ayna altı / çamurluk / kapı
- [ ] Otomatik (sinyal) mi, elle mi açılsın?

## Plan özeti

1. Teyp keşfi (Adım 0)
2. Kamera + kablo al
3. Güç + video çek
4. Montaj + teyp ayarı
5. Test

## Kararlar

| Tarih | Karar | Gerekçe |
|-------|-------|---------|
| 2026-07-22 | 360 (500–600$) yok | Pahalı; hedef canlı yan görüş |
| 2026-07-22 | Dashcam opsiyonel / ayrı | Kayıt ≠ Android canlı |
| 2026-07-22 | Bagaj organizer iptal | Tüp yanı dolu |
| 2026-07-22 | USB-C şimdilik yok | Gerek yok dendi |
| 2026-07-22 | Akü bakıcı fikri rafa / muhtemel iptal | Evde bakıcı yok; akü sorunu da yok |

## Notlar

- Kapı yalıtımı: kullanıcı “belki yaparım, haber ederim” → kenarda (`haftasonu-fikirler`)
