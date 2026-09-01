# Ön park sensörleri (kesik kesik)

> Ön ultrasonik park sensörleri kuruyken/bozukken susuyor; yağmur + ıslak yoldan sonra yeniden ses veriyor. Arıza “sihirli düzelme” değil — tipik kesik kesik PDC davranışı.

## Durum

- **Durum:** 📋 Planlama (teşhis)
- **Öncelik:** Düşük–orta (park yardımı; güvenlik değil ama can sıkıcı)
- **Tahmini bütçe:** Temizlik ~0 TL; soket temizliği ucuz; sensör değişimi sonra
- **Zorluk:** Kolay (yüzey) / orta (soket) / orta–zor (değişim)
- **Oluşturulma:** 2026-09-01
- **Son güncelleme:** 2026-09-01

## Araç bilgisi (ortak)

[ozellikler.md](../../araba/ozellikler.md) · [notlar.md](../../araba/notlar.md) — 2012 ix35, ön tamponda ultrasonik park sensörleri.

## Gözlem (2026-09-01)

- Ön sensörler bir süre **çalışmıyordu**.
- Birkaç gün yağmur, sulu yol → **yeniden çalışmaya başladı**.
- Tahmin: sıcak + kuru yol olunca **yine susacak**.

Bu tahmin **mantıklı** — özellikle kir/film senaryosunda.

## Ne alaka (neden yağmur “düzeltir”)

Ön tampondaki yuvarlak başlıklar **ultrason** atar/duyar. Yüzey veya soket bozulunca sistem o sensörü susturur veya tüm ön hattı keser.

Senin patern: **ıslak → açılır, kuru → kapanır** (veya kapanacağını düşünüyorsun). Literatürde sık görülen tersi de var (ıslakta bozulur). Senin yön için en güçlü aday:

| Olasılık | Neden yağmurda düzelir | Kuruyunca yine bozulur mu? |
|----------|------------------------|----------------------------|
| **1. Sensör yüzeyi kir / film / tuz** (en sık, senin tarife uyuyor) | Yağmur + lastik suyu yüzeyi yıkar; ultrason geçer | Evet — toz/kurum yeniden birikir |
| **2. Sıcaklık / genleşme (çatlak lehim, gevşek soket)** | Serin/nemli havada temas kapanır | Evet — sıcakta açılır |
| **3. Sokette korozyon** | Genelde **ıslakta bozulur**, kuruda düzelir | Senin paterne **ters** — ilk değil |
| **4. Sensör içine su** | Bazen kısa süreli garip davranış | Kalıcı arızaya gider; “düzeldi” güvenilir değil |

Yani: yağmur “tamir etmedi”. Büyük ihtimalle **yüzeyi temizledi** veya **soğuk/nemli temas** geçici tuttu. Kuruyunca bozulursa bu teşhisi güçlendirir — “bence yine bozulur” demen boş değil.

## Ne yapılmaz (şimdilik)

- Dört sensörü körlemesine yenileme
- “Beyin gitti” varsayımı
- Bodykit / tampon boya ile sensör deliğini kapatma

## Ne yapılır (sırayla)

1. **Şimdi çalışırken not et:** hangi sensörler (sol dış / sol iç / sağ iç / sağ dış)? Hepsi mi, biri mi? bip mesafesi normal mi?
2. **Kuruyunca bozulursa (deney):** bozulduğu gün ön tampondaki dört yuvarlak başlığı **yumuşak bez + su** (gerekirse az bulaşık deterjanı) ile sil; kuru bezle kurula. 5 dk sonra park sensörünü aç / duvara yaklaş. Düzelirse → kir/film, düzenli sil yeter; parça şart değil.
3. **Silmek yetmezse:** tampon arkasından soketlere bak (yeşil/beyaz toz = korozyon). Kontakt spreyi + dielektrik gres. Bu DIY orta zorluk.
4. **Hâlâ kesik kesik:** OBD/park modülü hata kodu (mümkünse). Tek sensör ölüyse o başlık değişir — önce hangisi tıklamıyor dinlenir (PDC açıkken sağlıklı sensör hafif “tık tık” yapar).

## Açık sorular

- [ ] Kuruyunca gerçekten yine sustu mu? (tarih not)
- [ ] Silince düzeldi mi?
- [ ] Arka park sensörleri de aynı mı, yoksa sadece ön mü?
- [ ] Gösterge / sesli uyarı “park sistemi arızası” veriyor mu, yoksa sessiz mi?

## Kararlar

| Tarih | Karar | Gerekçe |
|-------|-------|---------|
| 2026-09-01 | Önce kir/film + kuru tekrar testi; parça sonra | Yağmurda düzelme paterni yüzey temizliğine uyuyor |
| 2026-09-01 | Kullanıcı tahmini (kuru = yine bozuk) kabul edilebilir hipotez | Kir birikimi veya sıcaklık genleşmesi ile uyumlu |

## Notlar

“Yağmur düzeltti” = tamir değil. Kuru olunca bozulursa önce sil. Soket/korozyon ikinci. Değişim üçüncü.
