# Master Uygulama Planı

> Gerçek iş fazları — "bayiye sor" değil, "sipariş ver / kur / test et".
> **Bütçe güncellemesi (2026-07-09):** Sıkışık dönem — **Faz 0 = bekle + biriktir**. Parça parça iki sistem kurma.

---

## KESİN KARAR (2026-07-09)

**Sistem: StarLine A93 v2 2CAN+2LIN GSM ECO** — montajcı yok, kendin kur.

| Dosya | Ne için |
|-------|---------|
| [haftasonu-kurulum-plani.md](haftasonu-kurulum-plani.md) | **Cumartesi-Pazar adım adım** — sigorta, kutu, kablo |
| [diy-kurulum.md](diy-kurulum.md) | DIY genel, alet listesi |
| [telefon-kontrol-arastirma.md](telefon-kontrol-arastirma.md) | Sipariş + gümrük ~22–26k TL |

Pandora bu projede **yok** — arşiv: [pandora-arastirma.md](pandora-arastirma.md). Walk-away = çıkarken StarLine 2 ile kilitle.

---

## Önce oku

| Dosya | Ne için |
|-------|---------|
| [fazli-butce-plani.md](fazli-butce-plani.md) | **Parça parça mı, tek seferde mi?** Walk-away vs telefon önceliği |
| [telefon-kontrol-arastirma.md](telefon-kontrol-arastirma.md) | Evden telefon + gümrük ~22–26k TL |
| [uzaklasinca-otomatik-kilit.md](../uzaklasinca-kilit/README.md) | Walk-away ~15–20k TL (SST) |
| [parca-tedarik-tr.md](parca-tedarik-tr.md) | SKU / stok |

---

## Faz haritası (güncel)

```
Faz 0          Faz 1              Faz 2–5
BEKLE+BİRİKTİR TEK SİSTEM SİPARİŞ  KUR → AYARLA → YAŞA
│              │                   │
0 TL           StarLine ~25k       Tek konsol açılışı
plan oku       VEYA SST ~16k       Hepsini bir seferde
               (ikisini birden ALMA)
```

---

## Faz 0 — Bekle + hazırlık (şimdi, 0 TL) ← **aktif faz**

**Durum:** Bütçe sıkışık; StarLine ~22–26k şu an çok.

| Görev | Maliyet | Bitti sayılır |
|-------|---------|---------------|
| Plan dosyalarını oku | 0 | Bu repodaki kararlar net |
| Birikim hedefi koy | — | ~25.000 TL (StarLine + gümrük payı) |
| SST’ye ix35 uyum maili at | 0 | Yazılı cevap var veya yok |
| Çıkarken kilitle alışkanlığı | 0 | Walk-away gelene kadar yedek |

**Karar noktası (bütçe gelince):**

| Öncelik | Sipariş |
|---------|---------|
| **Evden telefon** (asıl hedef) | StarLine GSM ECO — [telefon-kontrol-arastirma.md](telefon-kontrol-arastirma.md) |
| Walk-away, telefon ertelendi | SST-019 — [uzaklasinca-otomatik-kilit.md](../uzaklasinca-kilit/README.md) |
| **İkisini sırayla iki marka** | ❌ Yapma — [fazli-butce-plani.md](fazli-butce-plani.md) |

---

## Faz 1 — Tek sistem siparişi (bütçe olunca)

### Yol A — StarLine (evden telefon)

```
□ A93 v2 2CAN+2LIN GSM ECO (~23.250 RUB + gümrük)
□ nano-SIM (kurulumda)
□ Gümrük müşaviri ayarla
```

Toplam: **~22.000–26.000 TL** — [telefon-kontrol-arastirma.md](telefon-kontrol-arastirma.md)

### Yol B — Start-Stop TR (walk-away + RF, telefon yok)

```
□ SST-019 ($330) — ix35 uyum teyidi sonrası
□ Montaj randevusu (startstopturkiye.com)
```

Toplam: **~15.500–20.000 TL** — [uzaklasinca-otomatik-kilit.md](../uzaklasinca-kilit/README.md)

**Yol A + B birlikte:** ❌

---

## Faz 2 — Teslim ve doğrula

| StarLine | SST |
|----------|-----|
| Kutu, pin-konvert, GSM modül | Kumanda, keypad, modül |
| Gümrük çıkışı tamam | Garanti belgesi |

---

## Faz 3 — Kur (tek seferde bitir)

**“Hazır açmışken hepsini yap”** burada geçerli — **aynı sistemin** tüm özelliklerini bir montajda kur.

| StarLine | Zorluk |
|----------|--------|
| CAN/LIN şema | Zor |
| iKey + manuel F15 | Orta |
| GSM + SIM | Kolay |

| SST | Zorluk |
|-----|--------|
| Profesyonel montaj önerilir | Orta |
| Manuel güvenlik protokolü | Orta |

---

## Faz 4 — Ayarla

**StarLine:** Firmware, F15, ilk uzaktan çalıştırma, evden GSM testi.

**SST:** Walk-away mesafe testi, RF uzaktan test (50–70 m).

---

## Faz 5 — Yaşa

**StarLine akışı:** [kullanim-senaryolari.md](kullanim-senaryolari.md)

**SST:** Yaklaş-aç / uzaklaş-kapat; RF ile ısıtma (evden değil).

---

## Faz 6 — Walk-away (StarLine yolunda)

StarLine kurulduysa ve walk-away hâlâ isteniyorsa:

- SLAVE + proximity tag (aksesuar)
- Veya çıkarken StarLine uygulamasından kilitle

SST zaten walk-away içerir — ayrı Faz gerekmez.

---

## Pes etme / erteleme rehberi

| Durum | Ne yap |
|-------|--------|
| 25k TL yok | **Faz 0’da kal** — plan hazır, acele yok |
| Walk-away önce, telefon sonra (iki marka) | **Dur** — fazli-butce-plani.md oku |
| SST aldım, şimdi StarLine da istiyorum | SST muhtemelen sökülür — ek maliyet |
| Sadece yaz kışın ısıtma lazım | Biriktir → StarLine tek atış |

---

## Hızlı referans

| Hedef | Sistem | Tahmini |
|-------|--------|---------|
| Evden telefon | StarLine GSM ECO | ~22–26k TL |
| Walk-away (yurtiçi) | SST-019 | ~15–20k TL |
| Şimdilik | Hiçbiri | 0 TL |

---

*Son güncelleme: 2026-07-09*
