# Teknik Analiz — Uzaktan Sistemler (Tam Rapor)

> Anahtarcıya gitmeden önce: yapılabilirlik, dokunulacak yerler, parçalar, sonuç, riskler.
> Araç: 2012 Hyundai ix35, 1.6 GDI, benzin+Prins LPG, manuel, 2WD, Smart Key, otomatik klima, koltuk ısıtma.

**Tarih:** 2026-07-09

---

## 1. Kısa cevap: Yapılır mı?

| Proje | Yapılır mı? | Güven | Engel |
|-------|-------------|-------|-------|
| Uzaklaşınca otomatik kilit | **Evet** | Yüksek | Manuel vites MyKeyPremium'u eledi; alternatif modül gerekir |
| Uzaktan çalıştırma | **Evet** | Yüksek | Manuel vites güvenlik prosedürü; karmaşık kurulum |
| Telefondan çalıştırma (evden) | **Evet** | Yüksek | LTE modül + aylık abonelik |
| Uygulamadan klima °C ayarı | **Hayır** | Kesin | 2012'de telematik yok; aftermarket CAN HVAC komutu göndermiyor |
| Klima çalışması (son ayar) | **Evet** | Orta-Yüksek | Otomatik klima avantajı; park ederken ayar bırakılır |
| Koltuk ısıtma uzaktan | **Evet** | Orta | Ek kablolama (aux + röle) |
| Walk-away + remote start tek paket | **Kısmen** | Orta | MyKeyPremium uyumsuz; farklı markalar veya anahtarcı |

---

## 2. Aracının mevcut elektrik mimarisi

2012 ix35 (LM platform = Tucson ile aynı altyapı) şu modüllerle çalışır:

```
┌─────────────────────────────────────────────────────────────┐
│                    2012 ix35 ELEKTRİK AĞI                   │
├─────────────────────────────────────────────────────────────┤
│  SMK ECU (Smart Key)  ←→  125kHz antenler  ←→  Kumanda     │
│       ↓ CAN bus                                              │
│  BCM (Gövde kontrol)  ←→  Kapı kilitleri, aydınlatma, alarm │
│       ↓                                                      │
│  PDM (Güç dağıtım)    ←→  START/STOP, immobilizer, start röle│
│       ↓                                                      │
│  ECM (Motor beyin)    ←→  1.6 GDI enjeksiyon                │
│       ↓                                                      │
│  A/C Control Module   ←→  Otomatik klima                      │
│       ↓                                                      │
│  Seat Heater Module   ←→  Koltuk ısıtma (soft-touch)        │
│                                                              │
│  Prins VSI/AFC ECU    ←→  LPG (benzinle başlar, ısınca geçer)│
└─────────────────────────────────────────────────────────────┘
```

### Smart Key sistemi nasıl çalışıyor?

- Kumanda arabayla **125 kHz LF** (kısa menzil) ve **433 MHz RF** ile konuşur
- Kapı kolundaki sensör: yakındayken "dokun → kilit/aç" (bu zaten var)
- **Walk-away lock fabrikada kapalı** — donanım var, yazılım/protokol aktif değil
- Aftermarket modül CAN bus üzerinden SMK/BCM'e "kilit" komutu gönderir; anahtar uzaklaşınca tetiklenir

### İlgili sigortalar (iç panel)

| Sigorta | Amper | Beslediği |
|---------|-------|-----------|
| SMART KEY (26) | 10A | PDM, SMK ECU, START/STOP düğmesi |
| MODULE 5 (18) | 7.5A | BCM, SMK ECU, PDM |
| CLUSTER (6) | 10A | Gösterge, BCM, SMK ECU |
| A/CON (23) | 7.5A | A/C Control Module |

---

## 3. PROJE A — Uzaklaşınca otomatik kilit

### 3.1 Teknik olarak ne oluyor?

```
Sen uzaklaşıyorsun
    → Modül anahtar sinyalini kaybediyor (LF/RF algılama)
    → Tüm kapılar kapalı mı kontrol
    → CAN bus: LOCK komutu → BCM → kapılar kilitlenir
    → Yaklaşınca: UNLOCK komutu
```

Fabrika kapı kolu kilidi = **pasif kilit** (sen basıyorsun).
Walk-away = **otomatik pasif kilit** (modül tetikliyor).

### 3.2 Dokunulacak yerler

| Bölge | Ne yapılır | Kalıcı mı? |
|-------|------------|------------|
| **OBD-II konnektörü** (direksiyon altı) | CAN bus bağlantısı (High/Low) | Hayır — tak-çıkar veya T-tap |
| **SMK ECU konnektörü** veya **BCM** | Bazı modüller buraya bağlanır | Yarı kalıcı |
| **Sürücü kick panel** (ayak boşluğu) | Modül montajı, kablo geçişi | Delik gerekebilir |
| **PDM** (nadiren) | Kilit sinyali | Nadiren |

**Motor/mechanik parçaya dokunulmaz.** Şanzıman, debriyaj, motor fiziksel değişmez.

### 3.3 Seçenekler (manuel vites uyumlu)

| Seçenek | Manuel uyum | ix35 2012 | DIY | Not |
|---------|-------------|-----------|-----|-----|
| MyKeyPremium | ❌ | Smart key | Kolay | **Elendi** — manuel desteklemiyor |
| Shark Racing Proximity | ? | Sorulmalı | Orta | Yurtdışı |
| TR anahtarcı modülü | Genelde evet | ix35 listeleniyor | Hayır | Kodlama gerekir |
| Boyo iKeyFree | ? | Forumda var | Orta | Bug bildirimi |

### 3.4 Sonuç (walk-away)

- Arabadan inip uzaklaşınca **3–10 sn içinde** kapılar kilitlenir
- Geri yaklaşınca **otomatik açılır** (modüle bağlı)
- Mevcut kumandalar çalışmaya devam eder
- Kapı kolundan kilitleme de çalışır
- **Anahtar arabada unutulursa:** iyi modüller kilitlenmez (güvenlik)

---

## 4. PROJE B — Uzaktan çalıştırma + klima + telefon

### 4.1 Fortin onayı: ix35/Tucson 2010–2013 Smart Key

Fortin resmi kılavuzu: **Hyundai Tucson Smart-Key 2010–2013** için EVO-ONE kurulumu mevcut.
ix35 = aynı LM platform → **uyumluluk çok yüksek**.

Kılavuz: `fortin.ca/download/23691/EVO-ONE_IG_REG_BI_HYU-Tucson_2010-2013_PTS_B_23691.pdf`

**Önemli:** Push-start için plug-and-play T-harness **YOK**. Kablo kablo bağlantı (wire-to-wire).

### 4.2 Sistem mimarisi (önerilen)

```
┌──────────────┐     LTE      ┌─────────────────┐
│  Telefon     │ ──────────→  │ DroneMobile     │
│  (DroneApp)  │              │ X1-LTE modülü   │
└──────────────┘              └────────┬────────┘
                                       │ RS-232 / data
                              ┌────────▼────────┐
                              │ Compustar CMX   │ ← Manuel vites güvenlik
                              │ (remote start)  │
                              └────────┬────────┘
                                       │
                              ┌────────▼────────┐
                              │ Fortin EVO-ONE  │ ← Immobilizer bypass
                              │ + firmware      │    CAN bus entegrasyon
                              └────────┬────────┘
                                       │
                    ┌──────────────────┼──────────────────┐
                    ▼                  ▼                  ▼
              START/STOP          OBD-II CAN          Kapı/el freni
              düğmesi             bus                  debriyaj
```

### 4.3 Dokunulacak yerler (detaylı)

Fortin Tucson 2010–2013 Push-Start kılavuzuna göre:

| # | Bölge | Konnektör | Bağlanan sinyaller | Erişim zorluğu |
|---|-------|-----------|-------------------|----------------|
| 1 | **START/STOP düğmesi arkası** | 10-pin beyaz | PTS1, PTS2 (düğme basma simülasyonu) | Orta — konsol sökümü |
| 2 | **Fren pedalı switch** | 4-pin beyaz | Foot brake (+12V) | Kolay — pedal üstü |
| 3 | **Sürücü kick panel** | 24-pin beyaz | Kapı tetik, key sense, ignition | Orta |
| 4 | **Yolcu kick panel** | 24-pin beyaz | Yardımcı sinyaller | Orta |
| 5 | **OBD-II** | 16-pin siyah | CAN1 High/Low, CAN2 High/Low | Kolay |
| 6 | **Sigorta kutusu** | I/P ön/arka | +12V besleme, ignition | Orta |
| 7 | **Kaput** | Yeni montaj | Hood pin switch (**zorunlu**) | Kolay — delik |
| 8 | **Gösterge paneli arkası** | 24-pin (bazı modeller) | Park lambası | Zor |
| 9 | **Klima paneli / koltuk modülü** | Opsiyonel | Koltuk ısıtma aux | Orta |
| 10 | **Debriyaj pedalı switch** | — | Clutch bypass (manuel) | Orta |
| 11 | **El freni switch** | — | Park brake sinyali | Kolay-Orta |

**Toplam:** ~15–25 kablo bağlantısı, 2 diyot, 1–2 röle, 1 kaput switch, 1 güvenlik etiketi.

### 4.4 Manuel vites güvenlik prosedürü (rezervasyon modu)

Her park sonrası şu ritual gerekir:

```
1. Vitesi BOŞA al
2. El frenini ÇEK
3. Ayağı debriyajdan çek
4. START/STOP ile motoru kapat (veya prosedüre göre kumandaya 2.5 sn bas)
5. Kumandadan "rezervasyon" aktif et
6. Araçtan çık, kapıyı kapat
7. Motor kapanır → sistem "güvenli" modda bekler
8. Artık uzaktan çalıştırabilirsin
```

**Güvenlik mantığı:** Motor çalışırken çıktıysan vites boştu → güvenli.
Kapı açılırsa rezervasyon iptal → uzaktan çalışmaz.

**Push-to-start + manuel için ek ayar:** Fortin ayar 1-06 = 2 (yanlışlıkla rezervasyon önleme)

### 4.5 Immobilizer bypass

- 2012 ix35'te immobilizer + smart key var
- Fortin EVO-ONE, anahtar kodunu modüle öğretir (programlama prosedürü)
- Push-to-start 2x bas → ignition ON → modül öğrenir
- FlashLink Updater ile firmware yüklenir (PC veya telefon)

### 4.6 Klima — otomatik klima ile ne olur?

| Durum | Sonuç |
|-------|-------|
| Park ederken AUTO + 24°C açık | Uzaktan çalışınca klima **AUTO 24°C** devreye girer |
| Park ederken klima kapalı | Muhtemelen çalışmaz |
| Uygulamadan "20°C yap" | **Mümkün değil** |
| Uzaktan çalışınca ekran | Kapalı kalır (normal — frene basınca açılır) |
| Lastik basınç uyarısı | Uzaktan çalışmada yanar (normal, frene basınca söner) |

**Bilinen risk:** Bazı Hyundai'lerde aftermarket uzaktan çalıştırmada AUTO modda fan hemen üflemeyebilir; kurulum sonrası test şart.

**En iyi pratik:**
- Kış: AUTO, 24°C, fan orta
- Yaz: AUTO, 22°C veya MAX soğutma
- 10–15 dk uzaktan çalıştır
- Sonra normal sürüşe geç (yağ ısınır, LPG'ye geçer)

### 4.7 Koltuk ısıtma (opsiyonel ek)

Hyundai'de koltuk ısıtma **soft-touch** — son konumu hatırlamaz.

**Çözüm:**
- Remote start modülünün **aux çıkışı** → röle → koltuk ısıtma modülüne pulse
- Tuşa basma simülasyonu (momentary ground pulse)
- DroneMobile uygulamasından aux butonu ile tetiklenir
- **3 kablo** koltuk modülüne, doğru polarite şart

### 4.8 Prins LPG entegrasyonu

| Konu | Durum |
|------|-------|
| Prins VSI başlangıç | Her zaman **benzinle** |
| Uzaktan çalıştırma | Benzinle çalışır → **uyumlu** |
| LPG'ye geçiş | Motor ısındıktan sonra otomatik (~30–50°C) |
| 10–15 dk rölanti | Benzinle başlar, ısınca LPG'ye geçer — normal |
| Depoda benzin | **Şart** — pompa kurumasın |
| LPG ECU'ya müdahale | Genelde gerekmez; Prins kendi yönetir |
| Risk | Uzun rölantide LPG reducer soğuyabilir (nadir, ısıtma senaryosunda düşük risk) |

### 4.9 Telefon kontrolü (DroneMobile)

| Özellik | Var mı? |
|---------|---------|
| Sınırsız menzil (LTE) | ✅ |
| Uzaktan çalıştır/durdur | ✅ |
| Kilit/aç | ✅ |
| GPS takip | ✅ (premium) |
| Kabin sıcaklığı görme | ✅ (thermistor ile) |
| Klima °C ayarlama | ❌ |
| Koltuk ısıtma aux | ✅ (kablolama ile) |
| Aylık ücret | ~$6–12 |

### 4.10 Sonuç (uzaktan çalıştırma)

**Sabah senaryosu:**
1. Telefondan "Start" → motor çalışır (benzinle)
2. Klima son ayarında devreye girer
3. 10–15 dk sonra araca bin
4. Kumanda ile kilidi aç (veya smart key proximity)
5. Frene bas → START/STOP → sür

**Görsel/işitsel geri bildirim:**
- Dörtlüler 2 sn'de bir yanıp söner (çalışıyor göstergesi)
- Motor sesi (çevrede)
- Ekran kapalı (bindiğinde açılır)

---

## 5. Parça listesi (tahmini)

### Walk-away lock (tek başına)

| Parça | Tahmini fiyat |
|-------|---------------|
| Proximity lock modülü | $150–250 USD veya TR anahtarcı fiyatı |
| Bağlantı kabloları | Dahil |

### Uzaktan çalıştırma (tam paket)

| Parça | Tahmini fiyat |
|-------|---------------|
| Compustar CMX (manuel uyumlu) | $300–500 USD |
| Fortin EVO-ONE | $150–200 USD |
| FlashLink Updater | ~$30 USD |
| DroneMobile DR-5400 LTE | ~$150 USD |
| Hood pin switch | ~$15 USD |
| Diyotler, kablo, röle | ~$30 USD |
| Thermistor (opsiyonel) | ~$20 USD |
| Koltuk ısıtma kablolama (opsiyonel) | ~$20 USD |
| **Toplam parça** | **~$700–950 USD** (~25.000–35.000 TL) |
| DroneMobile abonelik | ~$6–12/ay |
| Kurulum (DIY değilse) | 3.000–8.000 TL |

---

## 6. Kurulum zorluk değerlendirmesi

| Bölüm | DIY? | Süre (deneyimli) |
|-------|------|------------------|
| Araştırma & parça siparişi | ✅ | — |
| Fortin firmware yükleme | ✅ (PC gerekir) | 30 dk |
| Push-start kablolama | ⚠️ Zor | 4–8 saat |
| Manuel vites güvenlik ayarı | ⚠️ Kritik | 1–2 saat |
| Hood pin montajı | ✅ | 30 dk |
| DroneMobile kurulum | ✅ | 30 dk |
| Koltuk ısıtma aux | ⚠️ Orta | 1–2 saat |
| Walk-away modül | ⚠️ Orta | 1–3 saat |
| **Toplam (uzaktan çalıştırma)** | | **6–12 saat** |

**Öneri:** Elektrik/kablo tecrüben yoksa en azından **manuel vites güvenlik testini** deneyimli birinden yaptır. Yanlış kurulum = vites takılıyken çalışma riski.

---

## 7. RÖLANTI SORUSU — Zarar verir mi?

### Kısa cevap

**10–15 dakikalık uzaktan ısınma, doğru kullanımda genelde sorun yaratmaz** — ama 1.6 GDI motorun doğası gereği bazı noktalara dikkat et.

### Detaylı analiz

#### Motor (1.6 GDI)

| Risk | Açıklama | Senin senaryonda |
|------|----------|------------------|
| **Yağ seyreltmesi** | GDI motorlarda yakıt, piston segmanlarından yağa karışabilir | 10–15 dk rölanti + sonra sürüş = düşük-orta risk |
| **Soğuk rölanti** | Motor ısınmadan uzun rölanti kötü | 10–15 dk genelde ısınmaya yeter |
| **Katalizör** | Rölantide daha az verimli | Kısa süre sorun değil |
| **Yakıt tüketimi** | ~0.8–1.5 L/saat rölanti | 15 dk ≈ 0.2–0.4 L benzin |
| **Karbon birikimi** | Uzun süreli sürekli rölanti kötü | Günde 1–2 kez 15 dk = kabul edilebilir |

**GDI özel not:** 1.6 GDI (Gamma) motorlarda yağ seyreltmesi **kısa mesafe + soğuk hava** kombinasyonunda daha belirgin. Senin kullanımın (bilinçli 10–15 dk ısınma + sonra sürüş) daha az riskli.

**Öneriler:**
- Rölantiyi **15–20 dk ile sınırla** (zaten modül bunu yapar)
- Günde **1–2 kez** uzaktan çalıştır; sürekli saatlerce bırakma
- Yağ değişimini **10.000 km yerine 7.000–8.000 km** düşün (GDI için iyi pratik)
- Mümkünse yağ seviyesini/kokusunu ara sıra kontrol et (benzin kokusu = seyreltme)
- Isındıktan sonra **normal sürüşe geç** — yağdaki yakıt buharlaşır

#### LPG (Prins)

| Risk | Açıklama |
|------|----------|
| Soğuk LPG ile çalıştırma | Prins **benzinle** başlar → sorun yok |
| Uzun rölantide LPG | Isınınca LPG'ye geçer; reducer buharlaştırıcı soğuyabilir (çok uzun rölantide) |
| 10–15 dk ısınma | Genelde sorunsuz |
| Benzin deposu | Rölantide benzin tüketilir; depo boşalmamalı |

#### Akü

| Risk | Açıklama |
|------|----------|
| 15 dk çalıştırma | ~5–10 Ah tüketim; akü genelde kaldırır |
| Kışın zayıf akü | Uzaktan çalıştırma başarısız olabilir |
| Çözüm | Akü sağlıklı tut; gerekirse CCA yüksek akü |

#### Çevre / yasal

- Kapalı garajda **asla** uzaktan çalıştırma (CO zehirlenmesi)
- Site/apartman kuralları (gürültü, emisyon)
- Türkiye'de rölanti yasaları (genelde kısa ısınma sorun değil)

### Rölanti karar tablosu

| Süre | Sıklık | Risk | Öneri |
|------|--------|------|-------|
| 5–10 dk | Günde 1–2 | Düşük | ✅ İdeal |
| 10–15 dk | Günde 1–2 | Düşük-Orta | ✅ Kabul edilebilir |
| 15–20 dk | Günde 1 | Orta | ⚠️ Üst sınır |
| 30+ dk | Herhangi | Orta-Yüksek | ❌ Yapma |
| Sürekli saatlerce | — | Yüksek | ❌ Kesinlikle yapma |

---

## 8. Riskler ve önlemler

| Risk | Olasılık | Önlem |
|------|----------|-------|
| Vites takılıyken çalışma | Düşük (doğru kurulumda) | Manuel kit + rezervasyon modu + profesyonel test |
| Immobilizer arızası | Düşük | Fortin firmware doğru + programlama |
| Akü bitmesi | Orta (kış) | Akü kontrolü |
| Yağ seyreltmesi | Orta (GDI + kış) | Kısa rölanti, düzenli yağ değişimi |
| LPG sorunu | Düşük | Prins benzinle başlar; benzin deposu dolu |
| Klima çalışmaması | Orta | Kurulum sonrası test; park ayarı stratejisi |
| Modül arızası | Düşük | Kaliteli marka; sigorta koruma |
| Usta kalitesi (TR) | Değişken | Referans, garanti, yazılı teklif |
| Geri dönüş (orijinale) | İyi | Modül çıkarılabilir; çoğu bağlantı geri alınabilir |

---

## 9. Anahtarcıya gitmeden kontrol listesi

Kendin arabada şunları doğrula:

- [ ] START/STOP düğmesi var mı? (evet)
- [ ] Kapı kolundan dokunarak kilitleme çalışıyor mu?
- [ ] Otomatik katlanır ayna var mı?
- [ ] Kumanda kaç tuşlu? (fotoğraf çek)
- [ ] Prins sistem tipi? (VSI, VSI-2, VSI-3 — gösterge panelinde veya LPG kutusunda yazar)
- [ ] Benzin deposu genelde ne kadar dolu?
- [ ] Akü yaşı/ durumu?
- [ ] OBD-II portu nerede? (direksiyon altı — kontrol et)

---

## 10. Sonuç özeti

### Yapılacak iş (büyük resim)

```
MEVCUT ARAÇ                    EKLENEN SİSTEMLER              SONUÇ
─────────────                  ─────────────────              ─────
Smart Key          ──────→    Walk-away modülü      ──→    Uzaklaşınca kilit
START/STOP         ──────→    Fortin EVO-ONE        ──→    Immobilizer bypass
Manuel vites       ──────→    Compustar CMX         ──→    Güvenli uzaktan çalıştırma
Otomatik klima     ──────→    (değişiklik yok)      ──→    Son ayarla çalışır
Koltuk ısıtma      ──────→    Aux kablolama         ──→    Uygulamadan tetiklenebilir
Prins LPG          ──────→    (değişiklik yok)      ──→    Benzinle başlar, ısınca LPG
—                  ──────→    DroneMobile LTE       ──→    Evden telefonla kontrol
—                  ──────→    Hood pin switch       ──→    Güvenlik
```

### Gerçekçi beklenti

| Beklenti | Karşılanır mı? |
|----------|----------------|
| "Evden çalıştırayım, ısınmış binsin" | ✅ Evet |
| "Telefondan 22°C yapayım" | ❌ Hayır |
| "Uzaklaşınca kilitlensin" | ✅ Evet (ayrı modül) |
| "Koltuk ısınsın" | ✅ Evet (ek kablo ile) |
| "Hiç uğraşmayayım, plug-play" | ❌ Manuel vites + push-start = karmaşık |
| "15 dk rölanti zarar verir mi" | ⚠️ Doğru kullanımda hayır; abartma |

---

## Kaynaklar

- [Fortin Tucson 2010–2013 Push-Start kılavuzu](https://fortin.ca/download/23691/EVO-ONE_IG_REG_BI_HYU-Tucson_2010-2013_PTS_B_23691.pdf)
- [Fortin Tucson 2010–2015 Key kılavuzu](https://fortin.ca/download/61121/evo-one_ig_thr_bi_hyu2-tucson_2010-2015_key_a_61121.pdf)
- [Compustar manuel vites remote start](https://www.compustar.com/blog/can-you-remote-start-a-manual-transmission-stick-shift-vehicle/)
- [Smart Key sistem açıklaması](https://www.hexorcism.com/16veloster/Hyundai%20files/html/10_1_6_3.html)
- [Prins VSI servis kılavuzu](https://www.prinsautogas.com/en/service-your-vsi-system)
- [MyKeyPremium — manuel uyumsuz](https://mykeypremium.com/pages/technicals)
