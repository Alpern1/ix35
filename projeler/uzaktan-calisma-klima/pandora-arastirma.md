# Pandora VX-4G — Detaylı Araştırma (ix35 2012)

> 2012 Hyundai ix35 · 1.6 GDI · Smart Key · **Manuel** · Prins LPG
> Hedef: Evden telefon + walk-away **tek cihazda** — StarLine alternatifi mi?
> Araştırma tarihi: 2026-07-09
> Kur: 1 RUB ≈ 0,52 TL · 1 USD ≈ 46,87 TL

---

## 1. Yönetici özeti

| Soru | Cevap |
|------|-------|
| ix35 2012 için Pandora uyumlu mu? | **Evet** — resmi CLONE listesinde `Hyundai ix35 (кнопка Start-Stop) 2010–2013` |
| Telefon + walk-away tek kutuda? | **Evet** — GSM (4G) + **Hands Free** (Bluetooth proximity) |
| StarLine’dan daha iyi mi? | **İki işi tek kutuda yapıyorsa evet**; walk-away şart değilse StarLine hâlâ yeterli ve biraz ucuz |
| StarLine’dan ucuz mu? | **Hayır** — cihaz fiyatı StarLine’a yakın veya **~700–3.000 TL daha pahalı** (modele göre) |
| Türkiye’de satılıyor mu? | **Hayır** — Rusya ithalat; Türk SIM takılır |
| Önerilen model | **Pandora VX-4G v3** (GPS’siz, 24.599 RUB) — ix35 için CAN-FD gereksiz |

**Tek cümle:** İki özelliği tek kurulumda istiyorsan Pandora **mantıklı ve kanıtlı**; sadece evden telefon için StarLine biraz daha ucuz ve ix35 forum ekosistemi daha geniş.

---

## 2. Model ailesi — hangisini almalı?

Pandora VX-4G serisi 2022’den beri “bütçe 4G telematik” platformu. ix35 (2012) için **CAN-FD gerekmez** — FD modelleri yeni Çin/Kore araçları içindir.

### Fiyat tablosu (alarm.ru, 09.07.2026)

| Model | Fiyat (RUB) | TL (~) | GPS | Otomotiv modülü | BT metka | GSM 4G | ix35 için |
|-------|-------------|--------|-----|-----------------|----------|--------|-----------|
| **VX-4G Light** | 19.320 | ~10.050 | ❌ | ❌ RMD-4M **yok** | 1 adet | ✅ | ⚠️ uzaktan marş için RMD-4M ayrı al |
| **VX-4G v3** | **24.599** | **~12.790** | ❌ | ✅ RMD-4M v2 | 2× BT-760V | ✅ | **⭐ Önerilen** |
| StarLine A93 GSM ECO | 23.250 | ~12.090 | ❌ | ✅ (paket) | — | ✅ 2G/3G | Referans |
| **VX-4G GPS v3** | 29.360 | ~15.270 | ✅ | ✅ RMD-4M v2 | 2× BT-760V | ✅ | GPS istiyorsan |
| VX-4G GPS FD | 33.695 | ~17.520 | ✅ | ✅ | BT-760V + R-500BT | ✅ | ❌ ix35 için gereksiz pahalı |

**Light tuzağı:** 19.320 RUB ucuz görünür ama kutuda **uzaktan çalıştırma modülü yok**; RMD-4M (~3.000–5.000 RUB) eklenince v3’e yaklaşır.

**GPS gerekli mi?** Evden çalıştırma ve Hands Free için **hayır**. GPS = konum takibi + harita; gümrükte de fark yaratır.

Kaynaklar:
- https://alarm.ru/catalog/avtosignalizatsii/pandora-vx-4g-v2.html (VX-4G v3, 24.599 ₽)
- https://alarm.ru/catalog/avtosignalizatsii/pandora-vx-4g-gps-v3.html (GPS v3, 29.360 ₽)
- https://alarm.ru/catalog/avtosignalizatsii/vx-4g-light.html (Light, 19.320 ₽)

---

## 3. Teknik özellikler (VX-4G v3 / GPS v3)

| Özellik | Detay |
|---------|--------|
| GSM | 4G LTE / 3G / 2G |
| SIM | **Çift kaynak:** SIM-chip (fabrika) + nano-SIM yuvası |
| Bluetooth | 5.0 — telefon, metka, bröle |
| CAN | 2×CAN + LIN |
| İmmo bypass | **Pandora CLONE** — algoritmik, ikinci anahtar gerekmez |
| Uzaktan marş | RMD-4M v2 röle modülü (pakette) |
| Uygulama | **Pandora Connect** (iOS 15+ / Android) |
| Web | pro.p-on.ru |
| PC yazılım | Pandora Alarm Studio (Windows) — kurulum şart |
| Siren | PS-330 piezo (pakette) |
| Garanti | 3 yıl (Rusya resmi satış) |

Resmi kullanım kılavuzu: https://www.pandora-system.ru/downloads/pandora-vx-4g-gps-v3-user.pdf

---

## 4. ix35 2012 uyumluluğu — kanıtlar

### 4.1 Pandora CLONE resmi araç listesi

`loader.alarmtrade.ru` veritabanında **senin aracın açıkça var:**

| Marka | Model | Yıl | Not |
|-------|-------|-----|-----|
| Hyundai | **ix35 (кнопка Start-Stop)** | **2010–2013** | ✅ 2012 burada |
| Hyundai | ix35 (кнопка Start-Stop) | 2014–2015 | Farklı nesil |
| Hyundai | ix35 | 2010–2013 | Anahtarlı versiyon |

Kaynak: https://loader.alarmtrade.ru/ (Hyundai → ix35)

**Sonuç:** Push-start 2012 ix35, Pandora CLONE ile **resmi olarak desteklenen** araçlardan biri. StarLine `can.starline.ru` kadar tek sayfa şema yok ama **üretici listesinde net.**

### 4.2 Kurulum örnekleri

| Kaynak | Araç | Sistem | Not |
|--------|------|--------|-----|
| pandora.tomsk.ru | Hyundai ix35 | Pandect X-1800L | CAN 2×, otomotiv, SLAVE |
| drive2.ru (ix35 sahibi) | ix35 2012 | Pandora DXL-5000 | “Pandora styling” blog yazıları |
| pandoraprolab.ru | ix35 2010–2015 | DXL 4710 | Site geçici kapalı; arşivde paket ~56k RUB kurulumlu |

### 4.3 Manuel vites — kritik

Pandora fabrika ayarı **MKPP (manuel)**. Uzaktan çalıştırma için her seferinde **“programlı nötr”** algoritması gerekir:

```
1. El freni çek
2. Vites nötr
3. Programlı nötr aktif (el freni veya bröle 3 sn)
4. Çık → alarm silahlan → uzaktan marş izinli
```

Bu StarLine manuel F15 mantığıyla **aynı sınıf güvenlik** — manuel araçta “apartmandan tek tuş marş” yok, önce nötr protokolü var.

Kaynak: Pandora DX50 programlama kılavuzu (MKPP/РКПП ayarı)

### 4.4 Prins LPG

Pandora veya ix35 forumlarında **LPG + Pandora** özel uyarı bulunamadı. Kurulumda montajcıya **Prins LPG** olduğunu söyle; gaz kesici/röle hattı kontrol edilmeli. StarLine’da da aynı önlem geçerli.

---

## 5. Hands Free = walk-away mi?

### Ne yapar?

Resmi kılavuz (VX-4G GPS v3 user PDF):

> **Hands Free (свободные руки):** Uzaklaşınca veya yaklaşınca **otomatik olarak alarmı devreye al / devre dışı bırak.**

| Davranış | Hands Free | SST-019 walk-away |
|----------|------------|-------------------|
| Tetikleyici | BT metka veya telefon (yakınlık) | RF proximity |
| Uzaklaşınca | Alarm **silahlanır** | Kapılar **kilitlenir** |
| Yaklaşınca | Alarm **devre dışı** | Kapılar **açılır** |
| Fabrika ayarı | **Kapalı** — kurulumda açılır | Paket davranışı |
| Mesafe | RSSI + gisteresis ayarı (~90 dB önerilir) | ~2–3 m sabit iddia |
| Kapı kilidi | CAN üzerinden **mümkün** (merkezi kilit bağlıysa) | Ana işlev |

**Pratikte:** ix35’te CAN merkezi kilit doğru bağlanırsa, Hands Free silahlanırken **kapılar da kilitlenir** — SST’ye çok yakın deneyim. %100 fabrika walk-away garantisi değil; mesafe ayarı gerekebilir.

RealZvuk incelemesi Pandora VX-4G için şunu yazıyor: *“Hands free — **otomatik kapı ve motor kilidi**”* — https://realzvuk.ru/stati/luchshie-avtosignalizacii-v-2025-godu

Uygulama notu: Bazı kullanıcılar **Hands Free ayarının Pandora Connect’te değil, Pandora BT uygulamasında** yapıldığını bildiriyor (Google Play yorumları).

### Hands Free kurulum adımları (özet)

1. Alarm Studio veya Pandora BT / Pandora Pro → **Hands Free** menüsü
2. RSSI eşiği ayarla (başlangıç ~90 dB)
3. Gisteresis aç (fabrikada kapalı)
4. Mod seç: sadece silahlan / sadece devre dışı / ikisi birden
5. Telefonu metka olarak kaydet VEYA BT-760V taşı

Kaynaklar:
- https://alarmtrade.ua/ru/news/funktsiya_hands_free_v_signalizatsii_pandora_chto_ona_vypolnyaet_i_kak_rabotaet/
- https://avtodigitals.ru/chto-takoe-gisterezis-v-signalizacii-pandora/

---

## 6. Evden telefon — Pandora Connect

### Uygulama

| | Pandora Connect | StarLine 2 |
|--|-----------------|------------|
| iOS | ✅ (iOS 15+) | ✅ |
| Uzaktan marş | ✅ | ✅ |
| Kilitle/aç | ✅ (uygulamadan) | ✅ |
| GPS harita | ✅ (GPS modellerde) | Opsiyonel modül |
| Otomatik marş (sıcaklık/zaman) | ✅ 1°C adım | ✅ 3°C adım |
| Klima önceden | Marş + AUTO ayar | Aynı mantık |
| App Store puanı | **~2,8/5** (24 değerlendirme, GB) | Genelde daha iyi |
| Bilinen sorunlar | Sunucu 500 hatası, pil voltajı yanlış, push sesi iOS 17 | Daha az şikâyet |

**Dürüst not:** Pandora Connect özellik zengin ama **uygulama kalitesi StarLine’dan zayıf** görünüyor. Temel marş/kilit çoğu kullanıcıda çalışıyor; ara sıra sunucu/ bağlantı sorunu raporları var.

Kaynak: https://apps.apple.com/gb/app/pandora-connect/id1510941006

### GSM / Türk SIM

| Konu | Durum |
|------|--------|
| Rusya SIM-chip | Türkiye’de **roaming yok** — kullanılmaz |
| nano-SIM | **Turkcell / Vodafone / Türk Telekom** takılır |
| PIN | SIM PIN kapatılmalı |
| APN | Operatör APN (genelde otomatik) |
| Aylık veri | ~50–150 TL (düşük GB) |
| Pandora abonelik | **VX-4G için pro.p-on.ru temel kullanım ücretsiz** (tek araç) |
| Pandora-Спутник | Opsiyonel ~19–43k RUB/yıl — **gerekmez** |

Forum (AutoStudio): *“Komplekt SIM’lerde uluslararası roaming yok; yurt dışında başka SIM takın.”* — https://forum.autostudio.ru/topic6491.html

Eski DXL modellerde bazı kullanıcılar **350 RUB/ay** abonelik anmış; VX-4G serisi için resmi kaynaklar temel telematikte **sadece SIM maliyeti** diyor.

---

## 7. Pandora CLONE — ikinci anahtar gerekir mi?

**Hayır** — desteklenen araçlarda (ix35 2010–2013 Start-Stop dahil):

- Şoför anahtarı IMMO/KEY portuna bağlanır
- Alarm Studio + internet ile **algoritmik klonlama** (~15 sn – 2 dk)
- Salonda ikinci anahtar bırakmaya gerek yok
- StarLine iKey ile benzer mantık

Kaynak: https://alarmtrade.ru/functions/obhodchik-immobilajzera-s-klonirovaniem-klyucha/

**Kurulumda internet şart** (CLONE prosedürü için).

---

## 8. StarLine vs Pandora — dürüst karşılaştırma

### 8.1 Özellik matrisi (senin hedeflerin)

| Özellik | StarLine A93 GSM ECO | Pandora VX-4G v3 |
|---------|----------------------|-------------------|
| Evden telefon (GSM) | ✅ | ✅ 4G |
| Uzaktan çalıştırma | ✅ | ✅ |
| Walk-away / proximity | ❌ (SLAVE ≠ walk-away) | ✅ **Hands Free** |
| Telefonla kilitle | ✅ | ✅ |
| ix35 resmi kanıt | ⭐⭐⭐⭐⭐ can.starline.ru | ⭐⭐⭐⭐ loader.alarmtrade.ru |
| Manuel vites marş | ✅ F15 | ✅ programlı nötr |
| iPhone uygulama | ✅ iyi | ⚠️ orta |
| GPS (opsiyonel) | Ayrı modül | GPS v3’te dahil |
| İkinci anahtar | Gerekmez (iKey) | Gerekmez (CLONE) |
| Sıcaklık adımı otomatik marş | 3°C | **1°C** (daha hassas) |
| CAN-FD | Gerekmez | Gerekmez (FD model alma) |

### 8.2 Fiyat (cihaz + gümrük tahmini)

| Paket | Cihaz (RUB) | Cihaz (TL) | Gümrük dahil toplam |
|-------|-------------|------------|---------------------|
| StarLine GSM ECO | 23.250 | ~12.090 | **~22.000–26.000** |
| **Pandora VX-4G v3** | 24.599 | ~12.790 | **~23.000–27.000** |
| Pandora VX-4G GPS v3 | 29.360 | ~15.270 | **~26.000–32.000** |

**Fark:** GPS’siz Pandora, StarLine’dan cihazda **~700 TL**, toplamda **~1.000–2.000 TL** daha pahalı — “çok daha pahalı” değil; **GPS’li model** +4.000 TL civarı fark yaratır.

### 8.3 Güvenilirlik — forum özeti

| Konu | Pandora | StarLine |
|------|---------|----------|
| Montaj kalitesi | Sorunların **%80’i kötü montaj** (termomir.com) | Aynı |
| CAN hassasiyeti | “Montaj zayıfsa CAN arızası” şikâyetleri | Daha fazla ix35 örneği |
| Ekosistem TR | Yok | Forum + Türk SIM deneyimleri |
| Üretici garanti TR dışı | Sınırlı garanti (amatör montaj) | Benzer ithalat riski |

Kaynak: https://termomir.com/kakaya-signalizacziya-luchshe-pandora-ili-starlajn/

---

## 9. Montaj — Türkiye gerçeği

### Resmi ağ

- Pandora’nın Türkiye **yetkili distribütör / montajcı listesi yok** (StarLine gibi)
- Kurulum **Alarm Studio** ile araç modeli seçilerek yapılır — ix35 listede
- Rusya dışı amatör montaj: üretici **sınırlı garanti** veriyor (İngilizce kılavuz)

### Montaj maliyeti (referans — Rusya)

| Kaynak | İş | Fiyat |
|--------|-----|-------|
| alarm.ru | VX-4G v3 + kurulum | 33.600 RUB (~17.500 TL) |
| ugona.net | VX-4G GPS v3 + kurulum | 43.000–43.360 RUB |
| pandora-install.ru | Otomotiv aktivasyonu | +4.200 RUB’den |
| Forum (genel) | Basit Japon/Kore | 7.000–10.000 RUB |
| Forum (genel) | Smart-key + şehir | 9.000–15.000 RUB |

**Türkiye’de:** Montajcı **zorunlu değil** — DIY ana yol; detay: [diy-kurulum.md](diy-kurulum.md)

### DIY (kendin kur) — önerilen yol

- `can.starline.ru` + StarLine Master + ix35 forum DIY başlıkları
- StarLine forumda ix35’e **kendi kuran** kullanıcılar var
- Süre: ~12–20 saat (2–3 hafta sonu)
- Montajcı tasarrufu: ~5.000–15.000 TL

---

## 10. İthalat (Rusya → Türkiye)

StarLine ile **aynı prosedür:**

```
1. alarm.ru veya pandora-alarm.ru → sipariş (TR’ye kargo sor)
2. Forwarder (Pochtoy / Shopfans) alternatif
3. Gümrük 2026 — 30 € muafiyet yok
4. GTİP ~8531.10 · müşavir ~2.500–5.000 TL
5. Teslim → Türk nano-SIM · Alarm Studio · CLONE · Hands Free ayarı
```

**Kutu kontrol (VX-4G v3):**
- Ana ünite
- 2× BT-760V metka
- RMD-4M v2 otomotiv modülü
- L3000 sıcaklık sensörü
- IMMO kablosu
- PS-330 siren
- BS4 servis düğmesi

---

## 11. Riskler ve bilinen sorunlar

| Risk | Şiddet | Azaltma |
|------|--------|---------|
| Montajcı Pandora bilmiyor | Yüksek | Deneyimli montajcı bul / Rusya’da kurup getir (ekstrem) |
| Hands Free mesafe tutarsız | Orta | RSSI/gisteresis ayarı; telefon BT kapatma |
| Pandora Connect çökmesi | Orta | DTMF telefon komutları yedek (kılavuzda var) |
| CLONE prosedürü başarısız | Düşük-orta | loader.alarmtrade.ru’da ix35 listede — düşük |
| LPG entegrasyonu | Bilinmiyor | Montajda Prins belirt |
| İki sistem çakışması | Yüksek | SST + Pandora **takma** |
| Gümrük sürprizi | Orta | ~25–28k TL bandı planla (v3) |

---

## 12. Karar — hangi senaryoda Pandora?

```
Walk-away + evden telefon TEK kutuda ŞART
        │
        ├─ Bütçe ~23–27k TL (GPS’siz) → Pandora VX-4G v3 ⭐
        │
        ├─ GPS takip de istiyorum → VX-4G GPS v3 (~26–32k)
        │
        └─ Montajcı / uygulama riski kabul → devam

Sadece evden telefon; walk-away telefonla kilitle yeter
        → StarLine GSM ECO (biraz ucuz, daha iyi ix35 ekosistem)

Walk-away şart; telefon vazgeçilebilir
        → SST-019 yurtiçi (~15–20k) — Pandora’ya gerek yok
```

### Güncellenmiş öneri (StarLine “cepte” varsayımıyla)

| Öncelik sırası | Sistem | Neden |
|----------------|--------|-------|
| **1 (iki iş tek kutu)** | **Pandora VX-4G v3** | Hands Free + GSM; ix35 CLONE listede; StarLine’dan ~1–2k TL fark |
| 2 (sadece telefon) | StarLine GSM ECO | Walk-away yok ama kanıt/uygulama/forum üstün |
| 3 (ucuz walk-away) | SST-019 | Telefon yok |

---

## 13. Sipariş öncesi kontrol listesi

- [ ] Model: **VX-4G v3** (GPS’siz) — FD/Light değil
- [ ] Kutuda **RMD-4M v2** var mı?
- [ ] 2× **BT-760V** metka var mı?
- [ ] Satıcı Türkiye’ye gönderim / forwarder uyumu
- [ ] Montajcı: Alarm Studio + Hyundai CAN deneyimi
- [ ] Türk **nano-SIM** + veri paketi
- [ ] Kurulumda: MKPP, programlı nötr, CLONE, Hands Free RSSI
- [ ] Prins LPG bilgisi montajcıya yazılı

**Satıcıya örnek mesaj:**

```
Merhaba, Pandora VX-4G v3 (GPS olmayan, RMD-4M dahil tam paket) sipariş etmek istiyorum.
Teslimat: Türkiye. Kutuda RMD-4M v2 ve 2 adet BT-760V olduğunu teyit eder misiniz?
Araç: 2012 Hyundai ix35 1.6 GDI benzin, manuel vites, smart key (push-start), Prins LPG.
```

---

## 14. Kaynaklar

| Konu | URL |
|------|-----|
| VX-4G v3 fiyat | https://alarm.ru/catalog/avtosignalizatsii/pandora-vx-4g-v2.html |
| VX-4G GPS v3 fiyat | https://alarm.ru/catalog/avtosignalizatsii/pandora-vx-4g-gps-v3.html |
| VX-4G Light | https://alarm.ru/catalog/avtosignalizatsii/vx-4g-light.html |
| Kullanım kılavuzu PDF | https://www.pandora-system.ru/downloads/pandora-vx-4g-gps-v3-user.pdf |
| CLONE araç listesi | https://loader.alarmtrade.ru/ |
| CLONE açıklama | https://alarmtrade.ru/functions/obhodchik-immobilajzera-s-klonirovaniem-klyucha/ |
| Hands Free | https://alarmtrade.ua/ru/news/funktsiya_hands_free_v_signalizatsii_pandora_chto_ona_vypolnyaet_i_kak_rabotaet/ |
| Pandora vs StarLine | https://alarmauto70.ru/starline-ili-pandora-kakaya-signalizaciya-luchshe/ |
| Roaming / SIM | https://forum.autostudio.ru/topic6491.html |
| Pandora Connect iOS | https://apps.apple.com/gb/app/pandora-connect/id1510941006 |
| ix35 + Pandect kurulum | https://pandora.tomsk.ru/proekty/hyundai-ix35-pandect-1800l/ |
| StarLine karşılaştırma (repo) | [alternatif-karsilastirma.md](alternatif-karsilastirma.md) |

---

## 15. Karar kaydı

| Tarih | Bulgu |
|-------|-------|
| 2026-07-09 | ix35 2010–2013 Start-Stop **Pandora CLONE listesinde** |
| 2026-07-09 | Tek kutu telefon+walk-away: **VX-4G v3 yeterli**; GPS v3 opsiyonel |
| 2026-07-09 | StarLine’dan **~1–2k TL** pahalı (GPS’siz); GPS’li **~4–6k TL** |
| 2026-07-09 | Hands Free ≈ walk-away (CAN kilit bağlıysa); SST birebir değil |
| 2026-07-09 | Pandora Connect uygulama kalitesi **zayıf nokta** |
| 2026-07-09 | İki iş tek kutuda isteniyorsa Pandora **StarLine’dan daha iyi**; sadece telefon için StarLine yeterli |

---

*Son güncelleme: 2026-07-09*
