# Uzaktan Çalıştırma & Klima Kontrolü

> Telefon veya kumandayla aracı uzaktan çalıştırıp kabini ısıtmak/soğutmak.

## Durum

- **Durum:** 📋 Planlama (detaylı klima araştırması tamamlandı)
- **Öncelik:** Orta
- **Tahmini bütçe:** Kurulum dahil ~10.000–25.000+ TL (Türkiye, kaliteye göre değişir)
- **Zorluk:** Zor (manuel vites + LPG + eski model)
- **Oluşturulma:** 2026-07-09
- **Son güncelleme:** 2026-07-09

## Motivasyon

Kışın ısıtılmış, yazın serinletilmiş araca binmek. **Evden / uzaktan** telefonla çalıştırmak — kumanda menzili (~10 m) yeterli değil.

## Araç bilgileri (doğrulandı)

| Özellik | Değer |
|---------|-------|
| Anahtar | Smart Key + START/STOP |
| Klima | **Otomatik** |
| Koltuk ısıtma | **Var** |
| LPG | **Prins** |
| Şanzıman | Manuel |
| Telefon tercihi | Evet — LTE modül ile sınırsız menzil |

---

## Klima araştırması — önemli sonuç

### İstediğin şey: Uygulamadan sıcaklık ayarlama

Yeni Hyundai'lerde (Blue Link / myHyundai) şunlar mümkün:
- Uygulamadan "22°C'ye ayarla ve çalıştır"
- Ön cam buğu çözücü, arka cam, direksiyon ısıtma, koltuk ısıtma/havalandırma seçimi

**2012 ix35'te bu imkân yok** — araçta telematik modem ve Blue Link donanımı hiç yok. Bu özellik fabrikadan da, sonradan da "tam olarak" eklenemiyor.

### Peki otomatik klimayla ne kazanırız?

Otomatik klima **avantaj** sağlar ama farklı şekilde:

| Senaryo | Ne olur? |
|---------|----------|
| Park ederken AUTO + 24°C bıraktın → uzaktan çalıştırdın | Klima **son bırakılan ayarlarla** (AUTO, 24°C) devreye girer |
| Park ederken klima kapalı bıraktın | Uzaktan çalıştırmada klima çalışmayabilir |
| Uygulamadan "şimdi 18°C yap" | **Mümkün değil** (Blue Link yok) |

Fortin/Compustar dokümantasyonu da bunu söylüyor: *"Klima kontrollerini uzaktan çalıştırma öncesinde hazırla; uzaktan çalıştırmada son ayarlar kullanılır."*

### Aftermarket ile yapılabilecekler (klima ekosistemi)

```
┌─────────────────────────────────────────────────────────────┐
│  YAPILABİLİR                    │  YAPILAMAZ               │
├──────────────────────────────────┼──────────────────────────┤
│ Evden telefonla motor çalıştırma │ Uygulamadan °C ayarlama  │
│ Klima son ayarında çalışır       │ Blue Link tarzı profil   │
│ Kabin sıcaklığını GÖRME*         │ Fabrika climate start    │
│ Koltuk ısıtma aux ile tetikleme │ Kumandadan 100m+ menzil  │
│ Arka cam buğu aux ile (kablolama)│                          │
│ Sıcaklık eşiğinde otomatik start**│                         │
└──────────────────────────────────┴──────────────────────────┘
* DroneMobile + thermistor sensörü — sadece ölçüm, ayarlama değil
** Compustar Hot/Cold Start — kabin -5°C altına düşünce otomatik çalıştır
```

### Koltuk ısıtma — ek kablolama ile mümkün

Hyundai'lerde koltuk ısıtma "soft touch" — yani son konumu hatırlamaz, her seferinde tuşa basmak gerekir. Forumlarda çözüm:

- Remote start modülünün **aux çıkışı** + röle
- Koltuk ısıtma modülüne kısa pulse (tuşa basma simülasyonu)
- DroneMobile uygulamasından aux butonu ile tetiklenebilir

**Zorluk:** Orta — DIY mümkün ama doğru kablolama şart; yanlış bağlantı modülü yakabilir.

### Bazı kullanıcıların bildirdiği risk

Bazı push-start Hyundai'lerde aftermarket uzaktan çalıştırmada AUTO modda fan hemen üflemeyebilir; frene basıp aracı "tam aktif" edene kadar. Kurulum sonrası **test edilmeli**.

---

## Prins LPG notları

Prins VSI sistemi:
- Motor **her zaman benzinle** çalıştırır
- Isınınca otomatik LPG'ye geçer
- Depoda benzin olmalı (pompa kurumasın)

Uzaktan ısınma senaryosu için bu aslında **iyi** — soğuk LPG ile çalıştırma riski yok. Yine de LPG'ye hakim birinden "remote start ile uyumlu mu?" teyidi alınmalı.

---

## Manuel vites — kritik güvenlik

- **Rezervasyon modu** her seferinde gerekli (vites boşta + el freni + özel prosedür)
- Push-to-start + manuel için ek adımlar var (2.5 sn kumanda basma vb.)
- **MyKeyPremium uyumlu değil** — manuel vites desteklemiyor (uzaktan çalıştırma + walk-away paketi elendi)

---

## Önerilen sistem mimarisi

```
[Telefon — DroneMobile App]
        ↓ LTE (sınırsız menzil)
[DroneMobile X1-LTE modülü]
        ↓
[Compustar CMX serisi — manuel vites uyumlu remote start]
        ↓
[Fortin EVO-ALL / EVO-ONE — immobilizer bypass + CAN]
        ↓
[2012 ix35 — Smart Key + Push Start]
```

| Bileşen | Tahmini maliyet | Not |
|---------|-----------------|-----|
| Compustar manuel kit | $300–500 USD | CMX serisi, rezervasyon modu |
| Fortin EVO-ALL + harness | $150–250 USD | 2012 push-start için firmware/harness doğrulanacak |
| DroneMobile DR-5400 | ~$150 USD | LTE telefon kontrolü |
| Aylık abonelik | ~$6–12/ay | DroneMobile Basic |
| Kurulum (DIY değilse) | 3.000–8.000+ TL | Manuel + LPG bilgisi olan usta |

**Kumanda:** 2-yönlü Compustar kumanda yedek olarak kalabilir (apartman/yakın mesafe). Asıl kullanım telefon.

---

## Pratik kullanım senaryosu (en iyi sonuç)

### Kış
1. Eve park: klima **AUTO, 24°C**, fan orta
2. Rezervasyon modunu aktif et (manuel prosedür)
3. Sabah evden DroneMobile ile çalıştır (10–15 dk)
4. İsteğe bağlı: uygulamadan aux ile koltuk ısıtma
5. Araca bin → hazır kabin

### Yaz
1. Park: klima **AUTO, 22°C** veya MAX soğutma
2. Öğlen evden çalıştır
3. Bindiğinde serin kabin

### İleri seviye (opsiyonel)
- Compustar **Hot/Cold Start:** kabin sıcaklığı eşiği aşılınca otomatik çalıştır (sensör gerekir)
- Arka cam buğu: aux + sıcaklık tetiklemeli röle

---

## Seçenek karşılaştırması

| Seçenek | Telefon | Klima kontrolü | Manuel uyum | DIY |
|---------|---------|----------------|-------------|-----|
| **Compustar + Fortin + DroneMobile** | ✅ LTE | Son ayar + aux | ✅ | Zor |
| Fortin + OEM kumanda 3x kilit | ❌ ~10m | Son ayar | ✅ | Zor |
| MyKeyPremium | ❌ manuel uyumsuz | — | ❌ | — |
| TR anahtarcı paketi | Değişken | Değişken | Sorulmalı | Hayır |
| Hyundai OEM kit | ❌ | Son ayar | ❌ (otomatik) | Hayır |

---

## Güvenlik gereksinimleri (vazgeçilmez)

- [ ] Kaput pin switch (hood pin)
- [ ] El freni sensörü
- [ ] Kapı sensörleri
- [ ] Manuel vites rezervasyon modu
- [ ] Prins LPG uyum teyidi
- [ ] Benzin deposu minimum seviye kontrolü (alışkanlık)
- [ ] Çalışma süre limiti (15–20 dk)

## Açık sorular

- [x] Smart key — evet (START/STOP)
- [x] Otomatik klima — evet
- [x] LPG — Prins
- [x] Koltuk ısıtma — var
- [x] Telefon tercihi — evet
- [ ] Prins sistem versiyonu? (VSI, VSI-2, VSI-3 DI…)
- [ ] Otomatik katlanır ayna var mı?
- [ ] Aylık abonelik (~200–400 TL) kabul edilebilir mi?
- [ ] Türkiye'de Compustar/Fortin kurulumu yapabilen güvenilir yer var mı?

## Kararlar

| Tarih | Karar | Gerekçe |
|-------|-------|---------|
| 2026-07-09 | Fabrika app çözümü mümkün değil | 2012 ix35'te telematik yok |
| 2026-07-09 | Aftermarket + manuel uyumlu kit gerekli | Manuel vites + immobilizer |
| 2026-07-09 | MyKeyPremium elendi | Manuel vites desteklemiyor |
| 2026-07-09 | Telefon kontrolü önerildi | DroneMobile LTE — evden çalıştırma |
| 2026-07-09 | Uygulamadan °C ayarı bu araçta mümkün değil | Blue Link donanımı yok; aftermarket de CAN HVAC komutu göndermiyor |
| 2026-07-09 | Otomatik klima avantajı: son ayar korunur | Park ederken doğru ayarı bırakma stratejisi |

## Linkler

- [Fortin EVO-ALL — Hyundai push-to-start kurulum](https://manualspro.net/259911-fortin-108601-evo-all-and-hyundai-push-to-start-installation-guide)
- [Compustar DroneMobile](https://www.compustar.com/dronemobile-smartphone-car-control)
- [Compustar Hot/Cold Start](https://help.compustar.com/s/article/How-to-Use-Hot-Cold-Start-Feature-to-Remote-Start-Your-Vehicle-Automatically)
- [Hyundai Forum — koltuk ısıtma + remote start](https://www.hyundai-forums.com/threads/turn-seat-warmers-on-with-remote-start.225553/)
- [Prins VSI servis kılavuzu](https://www.prinsautogas.com/en/service-your-vsi-system)
- [Manuel vites remote start — Compustar](https://www.compustar.com/blog/can-you-remote-start-a-manual-transmission-stick-shift-vehicle/)

## Notlar

- Otomatik klima olması "uygulamadan ayar" getirmez ama "son ayarı koruma" konusunda manuel klimadan çok daha iyi.
- İki proje birleştirilebilir ama MyKeyPremium tek paket olarak düşünülemez (manuel uyumsuz).
- Walk-away kilit için ayrı çözüm: TR anahtarcı veya Shark Racing (ayrı proje dosyası).
