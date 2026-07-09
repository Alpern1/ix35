# Alternatif Karşılaştırma — Tek Cihaz mı, StarLine Şart mı?

> 2012 Hyundai ix35 · Smart Key · Manuel · Prins LPG
> Soru: Parça parça toplanır mı? Hem telefon hem walk-away tek kutuda var mı? Daha ucuz/sağlam alternatif?
> Son güncelleme: 2026-07-09

---

## 1. Kısa cevaplar

| Soru | Cevap |
|------|-------|
| StarLine’ı parça parça toplayıp sonra mı kurarız? | **Hayır.** GSM ECO tek kutu; modül modül biriktirme yok. Biriktir → tek seferde sipariş + gümrük. |
| StarLine mecburi mi? | **Evden telefon + ix35 2012 push-start + manuel** için yurtiçinde kanıtlı alternatif yok. İthalatta **en iyi belgelenmiş** seçenek StarLine. |
| Hem telefon hem walk-away tek cihaz? | **Evet: Pandora VX-4G v3** (Hands Free) — ix35 CLONE listede; [pandora-arastirma.md](pandora-arastirma.md) |
| Daha ucuz ve daha iyi bir şey var mı? | **İkisini birden yapan başka yok.** Pandora GPS’siz ~1–2k TL StarLine üstü; ucuz olanlar bir özelliği eksik |

---

## 2. “Parça parça topla sonra halledelim” gerçeği

### StarLine modüler değil

```
❌ Önce GSM modül al, sonra ana ünite, sonra bypass…
   → Resmi paket GSM ECO zaten hepsini içeriyor
   → Ayrı parça avcılığı çoğu zaman TOPLAMDA daha pahalı

✅ Doğru yol:
   Faz 0: 0 TL — plan + birikim (~25.000 TL hedef)
   Faz A: Tek sipariş — A93 v2 2CAN+2LIN GSM ECO + gümrük + tek kurulum
```

### İki markayı sırayla kurmak da “parça parça” sayılır — önerilmez

Önce SST walk-away (~15k), sonra StarLine telefon (~24k) ≈ **~39k TL + çift montaj + çakışma riski**.

Detay: [fazli-butce-plani.md](fazli-butce-plani.md)

---

## 3. Tek cihaz: telefon + walk-away

### A — Pandora VX-4G v3 (önerilen — GPS’siz)

| Özellik | Durum |
|---------|--------|
| Evden telefon (4G/LTE, uygulama) | ✅ Pandora Connect (iOS/Android) |
| Uzaktan çalıştırma | ✅ RMD-4M v2 pakette |
| Walk-away benzeri | ✅ **Hands Free** — telefon veya BT metka |
| ix35 2012 | ✅ **loader.alarmtrade.ru:** ix35 Start-Stop **2010–2013** |
| Manuel vites | ✅ Programlı nötr (MKPP) |
| Cihaz fiyatı | **24.599 RUB** (~12.790 TL) |
| StarLine GSM ECO | **23.250 RUB** (~12.090 TL) |
| Gümrük sonrası tahmin | **~23.000–27.000 TL** | StarLine: **~22.000–26.000 TL** |

**Tam araştırma:** [pandora-arastirma.md](pandora-arastirma.md)

### A2 — Pandora VX-4G GPS v3 (GPS isteyenler)

| Özellik | Durum |
|---------|--------|
| GPS takip | ✅ Dahili |
| Cihaz fiyatı | **29.360 RUB** (~15.270 TL) |
| Gümrük sonrası tahmin | **~26.000–32.000 TL** |

**Hands Free ≠ SST walk-away birebir aynı şey değil:**

| | SST-019 | Pandora Hands Free |
|--|---------|-------------------|
| Mantık | Proximity → kapı **kilit** | Proximity → alarm **silahlan** (CAN ile çoğu araçta kilit de olur) |
| Mesafe | ~2–3 m sabit iddia | RSSI/gisterezis ile ayarlanır (~90 dB önerilen) |
| Varsayılan | Açık paket davranışı | **Fabrikada kapalı** — kurulumda açılır |
| Telefon | ❌ (BT modülü yakın mesafe) | ✅ Telefon metka olarak kullanılabilir |

**Sonuç:** İki özelliği **tek marka / tek kurulum** istiyorsan **Pandora VX-4G v3** — StarLine’dan **~1–2k TL** pahalı; GPS’li model +4–6k TL.

Kaynaklar:
- https://alarm.ru/catalog/avtosignalizatsii/pandora-vx-4g-v2.html (VX-4G v3)
- https://alarm.ru/catalog/avtosignalizatsii/pandora-vx-4g-gps-v3.html (GPS v3)
- https://loader.alarmtrade.ru/ (ix35 CLONE listesi)
- Hands Free: https://alarmtrade.ua/ru/news/funktsiya_hands_free_v_signalizatsii_pandora_chto_ona_vypolnyaet_i_kak_rabotaet/

### B — StarLine A93 GSM ECO

| Özellik | Durum |
|---------|--------|
| Evden telefon | ✅ StarLine 2 uygulaması |
| Uzaktan çalıştırma | ✅ iKey bypass, 2CAN+2LIN |
| Walk-away | ❌ SST gibi “uzaklaşınca kilit” **pakette yok** |
| ix35 | ✅ can.starline.ru + forum kurulumları |
| Fiyat | **Daha ucuz** Pandora VX-4G’ye göre |

Walk-away için: telefondan kilitle, SLAVE + fabrika kilit tuşu, veya ayrı SST (çift sistem — önerilmez).

### C — Diğer araştırılanlar (tek kutu değil veya elendi)

| Marka / ürün | Telefon evden | Walk-away | Neden elendi / not |
|--------------|---------------|-----------|-------------------|
| **Start-Stop TR SST-019** | ❌ RF ~50–70 m | ✅ | Yurtiçi; telefon yok |
| **Oto Yapay Zeka** | ❌ ~100 m BT | ✅ iddia | Fabrika start-stop’a önerilmez; iPhone yok |
| **Fortin MK3** | ❌ | ❌ | RF menzil; LTE modül TR’de yok |
| **Scher-Khan Magicar** | ❌ GSM yok | ❌ | Eski RF ekosistem |
| **Compustar + DroneMobile** | ⚠️ | ❌ | Kuzey Amerika LTE; TR operatör uyumsuz |
| **Cyclone L700A** | ❌ | ❌ | Yurtiçi RF; GSM yok |
| **Yuebiz YB30S (Çin)** | ✅ iddia | ❌ | ix35 kanıtı yok; çalışmazsa pahalı hata |
| **Çin plug-and-play (Tiremagic vb.)** | ❌ | ❌ | 2018+ ix35; 2012 push-start + immo farklı |

---

## 4. Fiyat / performans tablosu (hedeflerine göre)

Kur: 1 RUB ≈ 0,52 TL · Gümrük dahil toplam tahmin

| Seçenek | Evden telefon | Walk-away | Cihaz | Toplam (tahmin) | ix35 kanıtı | Öneri |
|---------|---------------|-----------|-------|-----------------|-------------|-------|
| **StarLine A93 GSM ECO** | ✅ | ❌ | ~12.100 TL | **~22–26k** | ⭐⭐⭐⭐⭐ | **Telefon öncelik #1** |
| **Pandora VX-4G v3** | ✅ | ✅ Hands Free | ~12.790 TL | **~23–27k** | ⭐⭐⭐⭐⭐ CLONE | **Tek kutu #1** |
| **Pandora VX-4G GPS v3** | ✅ | ✅ Hands Free | ~15.270 TL | **~26–32k** | ⭐⭐⭐⭐⭐ | GPS + proximity |
| **StarLine Paket C (ucuz GSM)** | ✅ | ❌ | ~9.100 TL | **~19–23k** | ⭐⭐⭐ | Satıcı/GSM versiyonu **teyit şart** |
| **SST-019** | ❌ | ✅ | ~15.500 TL | **~15–20k** | ⭐⭐⭐ | Sadece walk-away; telefon vazgeçilirse |
| **Oto Yapay Zeka** | ❌ | ⚠️ | ~19.000 TL | ~19–24k | ⭐⭐ | **Önerilmez** (fabrika PTS) |
| **Önce SST + sonra StarLine** | ✅ (sonra) | ✅ (önce) | iki sistem | **~35–45k** | — | **Yapma** |

**“Daha ucuz” tuzağı:** StarLine Paket C veya Çin kiti ilk bakışta ucuz; gümrük + çalışmama riski ile StarLine A paketini geçebilir.

---

## 5. StarLine’dan ne kadar emin olmalıyız?

### Güçlü yanlar

- **ix35:** `can.starline.ru` şemaları, forumda 2010’lar ix35 kurulumları
- **Manuel + push-start:** F15 firmware notları
- **iPhone:** StarLine 2 resmi uygulama
- **Türk SIM:** Forumda çalışan kullanıcılar var (üretici garanti vermiyor ama teknik olarak mümkün diyor)
- **Fiyat/özellik:** GSM ECO paketi Pandora’ya göre **~6.000 RUB daha ucuz** cihaz fiyatında

### Zayıf yanlar (dürüst liste)

- **Walk-away yok** — SST kadar “çıktım gitti kilitlendi” değil
- **İthalat + gümrük** — 2026’da 30 € muafiyet yok; müşavir maliyeti var
- **Türkiye distribütörü yok** — forwarder veya Rusya satıcısı
- **LPG (Prins):** StarLine forumda LPG’li araçlar için ek dikkat notları olabilir — kurulumda söyle

### Pandora ne zaman mantıklı?

```
Telefon + walk-away TEK kurulumda, TEK marka
        VE
~4–6k TL ek bütçe sorun değil
        VE
Hands Free davranışı SST’den farklı olsa da kabul
        → Pandora VX-4G değerlendir
```

Aksi halde → **StarLine (telefon) + ücretsiz alışkanlık/telefonla kilitle (walk-away ödünü)**

---

## 6. Karar ağacı

```
Bütçe sıkışık
    │
    ├─ Şimdi parça alma → Faz 0 (0 TL) + birikim
    │
    └─ Para toparlanınca TEK sistem:

        Evden telefon ŞART
            │
            ├─ Walk-away de ŞART, tek kutu istiyorum
            │       → Pandora VX-4G (~26–32k) — ithalat
            │
            ├─ Walk-away ikincil / telefonla kilitle yeter
            │       → StarLine GSM ECO (~22–26k) — ithalat ⭐
            │
            └─ Walk-away şart, telefon vazgeçilebilir
                    → SST-019 (~15–20k) yurtiçi

        İkisini sırayla (SST sonra StarLine)
            → ÖNERİLMEZ (~39k+)
```

---

## 7. İlgili dosyalar

| Dosya | İçerik |
|-------|--------|
| [telefon-kontrol-arastirma.md](telefon-kontrol-arastirma.md) | Yurtiçi/ithalat telefon + gümrük detayı |
| [fazli-butce-plani.md](fazli-butce-plani.md) | Parça parça neden kötü fikir |
| [uzaklasinca-otomatik-kilit.md](uzaklasinca-otomatik-kilit.md) | SST walk-away fiyatları |
| [master-plan.md](master-plan.md) | Aktif faz: Faz 0 |

---

## 8. Karar kaydı

| Tarih | Bulgu |
|-------|-------|
| 2026-07-09 | Tek kutuda telefon+walk-away: **Pandora VX-4G** en yakın; StarLine’dan pahalı |
| 2026-07-09 | Daha ucuz+saglam+ikisi birden: **bulunamadı** |
| 2026-07-09 | StarLine ix35 için hâlâ **en iyi belgelenmiş telefon** seçeneği |
| 2026-07-09 | Parça parça modül biriktirme: **StarLine için yok** |

---

*Son güncelleme: 2026-07-09*
