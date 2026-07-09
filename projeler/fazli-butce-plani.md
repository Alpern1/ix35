# Fazlı Bütçe Planı — Önce Ne, Sonra Ne?

> 2012 ix35 · Smart Key · Manuel · Prins LPG
> Durum: **Sıkışık dönem** — parça parça mı, tek seferde mi?
> Son güncelleme: 2026-07-09

---

## 1. Kısa cevap (senin soruna)

| Soru | Cevap |
|------|-------|
| Walk-away önce, telefon sonra olur mu? | **Teknik olarak kötü fikir** — iki ayrı marka sistemi aynı araca sırayla takmak çoğu zaman çift montaj + çakışma |
| Walk-away StarLine kadar pahalı mı? | **Hayır** — yurtiçi Start-Stop TR paketi StarLine’dan **~%30–40 ucuz**; ama **evden telefon vermez** |
| Şimdi ne yap? | **Parça satın alma** — plan dosyaları hazır; bütçe toparlanınca **tek sistem** seç |
| Hazır açmışken hepsini mi? | **Evet — ama tek sistemin içinde.** İki farklı sistemi “parça parça” kurma |

---

## 2. Bütçe tablosu (elimizdeki rakamlar)

Kur: 1 USD ≈ 46,87 TL (TCMB 09.07.2026)

| Proje / paket | Ne verir | Tahmini toplam | Gümrük | Evden telefon | Walk-away |
|---------------|----------|----------------|--------|---------------|-----------|
| **A — StarLine GSM ECO (ithalat)** | Uzaktan çalıştırma + alarm + GSM | **~22.000–26.000 TL** | Evet | ✅ | ⚠️ SST gibi değil — bkz. Bölüm 9 |
| **B — Start-Stop TR SST-019** | Anahtarsız + walk-away + RF uzaktan (~50–70 m) | **~15.500–20.000 TL** | Hayır | ❌ | ✅ |
| **C — Oto Yapay Zeka** | Telefon iddiası (~100 m) | ~19.000 TL + montaj | Hayır | ❌ gerçek GSM değil | ✅ |
| **D — Fortin MK3 (RF)** | RF uzaktan menzil | ~15.000–18.000 TL (tahmin) | Hayır | ❌ | ❌ |
| **E — Şimdilik hiçbir şey** | Plan + araştırma | **0 TL** | — | — | — |

Detay: [telefon-kontrol-arastirma.md](telefon-kontrol-arastirma.md) · [parca-tedarik-tr.md](parca-tedarik-tr.md)

### Walk-away fiyatı araştırıldı mı?

**Evet — ama “sadece kilit” diye ayrı ucuz SKU yok** (yurtiçi).

| Kaynak | Ürün | Liste fiyatı | Walk-away | Not |
|--------|------|--------------|-----------|-----|
| fsatuning.com | SST-019 | **$330** (~15.500 TL) | ✅ 2–3 m uzaklaşınca kilit | Tam paket; ix35 teyit şart |
| fsatuning.com | + BT modül | +$112 (~5.250 TL) | — | Evden değil, ~50 m |
| startstopturkiye.com | Aynı marka | Site $330 bandı | ✅ | Montaj fiyatı **“iletişime geç”** |
| MyKeyPremium | Walk-away paket | İthalat | ✅ | ❌ **Manuel elendi** |
| Shark / Boyo | Sadece proximity | ~$150–250 + gümrük | ✅? | ix35 kanıtı yok |
| StarLine SLAVE + tag | Proximity | Pakete ek / aksesuar | ⚙️ | StarLine alırsan düşünülür |

**Montaj (SST):** Sitede sabit fiyat yok; çoğu ilde montaj var — **2.000–5.000 TL** bandı varsay (teyit: startstopturkiye.com iletişim).

---

## 3. Parça parça mı, tek seferde mi?

### ❌ Önerilmeyen: “Önce SST walk-away, sonra StarLine telefon”

```
SST kurulumu (BCM, immo, start-stop hatları)
        ↓ 1–2 yıl sonra
StarLine kurulumu (aynı hatlara tekrar müdahale)
        ↓
= İki kez konsol sökümü
= İki ayrı bypass mantığı
= Biri sökülmeden diğeri düzgün çalışmayabilir
= Toplam para: ~15k + ~24k ≈ 39k TL (iki sistem)
```

**Sonuç:** Bütçe sıkışıkken **iki sisteme para vermek** en kötü senaryo.

### ✅ Önerilen: Önceliğe göre **tek sistem**, doğru zamanda

```
ŞİMDİ (0 TL)
  └─ Plan dosyaları, ix35 uyum teyidi (e-posta), birikim

SONRA — önceliğine göre TEK yol:

  Yol 1: Evden telefon öncelik (senin asıl hedefin)
  └─ Biriktir → StarLine GSM ECO (~22–26k tek sefer)
  └─ Walk-away: StarLine SLAVE/tag veya manuel kilitle alışkanlığı (ücretsiz)

  Yol 2: Walk-away öncelik, telefon ertelenir
  └─ SST-019 (~15–20k) — ix35 uyumu yazılı teyit sonrası
  └─ Telefon hedefini ertele veya BT modülle “apartman önü” ödünü kabul et
  └─ StarLine’ı sonra eklemeyi planlama (SST muhtemelen sökülür)
```

### “Hazır açmışken hepsini yap” ne demek?

| Durum | Tavsiye |
|-------|---------|
| StarLine sipariş ettin, kutu geldi | **Bir kurulum seansında:** alarm + GSM + iKey + manuel ayar + (istersen) hood pin — hepsini bitir |
| SST aldın | **Bir montajda:** walk-away + RF uzaktan + keypad — paket zaten birlikte |
| İki sistemi ayrı aylarda kur | **Yapma** — para ve işçilik çift |

---

## 4. Öncelik matrisi (senin durumuna göre)

Sen **telefon kontrolü** istiyorsun; fiyat **şu an çok**; **walk-away** da isteniyor.

| Öncelik | Şimdi | Sonra (bütçe olunca) |
|---------|-------|----------------------|
| **1 — Telefon (evden)** | Bekle, planı oku | StarLine GSM ECO |
| **2 — Walk-away** | Ücretsiz: çıkarken uygulama/kumanda kilitle alışkanlığı | StarLine SLAVE **veya** SST (telefon vazgeçilirse) |
| **3 — Klima önceden ısıtma** | Parkta AUTO ayarla (ücretsiz) | Uzaktan çalıştırma ile gelir |

**Sıkışık dönemde en mantıklı hamle:** **Hiç parça alma.** Plan repoda duruyor; fiyatlar güncellenince `telefon-kontrol-arastirma.md` revize edilir.

---

## 5. Faz haritası (bütçe dostu)

```
┌─────────────────────────────────────────────────────────────┐
│ FAZ 0 — ŞİMDİ (0 TL)                          ← buradasın   │
│ · Plan dosyaları oku                                        │
│ · SST’ye “2012 ix35 1.6 GDI manuel smart key uyumlu mu?” yaz│
│ · StarLine için birikim hedefi: ~25.000 TL                  │
└───────────────────────────┬─────────────────────────────────┘
                            │ bütçe
                            ▼
┌─────────────────────────────────────────────────────────────┐
│ FAZ A — Telefon öncelik (hedef)                             │
│ · StarLine GSM ECO ithalat (~22–26k)                        │
│ · Tek kurulum hafta sonu                                    │
│ · Walk-away: SLAVE sonra veya alışkanlık                    │
└───────────────────────────┬─────────────────────────────────┘
              VEYA (telefon ertelenirse)
                            ▼
┌─────────────────────────────────────────────────────────────┐
│ FAZ B — Walk-away öncelik                                   │
│ · SST-019 (~15–20k) yurtiçi                                 │
│ · Evden telefon hedefinden vazgeç veya BT ile sınırlı ödün  │
│ · StarLine sonra EKLEME — muhtemelen SST sökülür            │
└─────────────────────────────────────────────────────────────┘
```

---

## 6. Walk-away projesi güncellemesi

Walk-away **ayrı proje dosyasında** vardı; fiyat araştırması eksikti — **tamamlandı:**

→ [uzaklasinca-otomatik-kilit.md](uzaklasinca-otomatik-kilit.md)

**Özet:** Walk-away tek başına ~5.000 TL’lik bir “modül” olarak satılmıyor. En net yurtiçi paket **SST-019 ~15.500 TL** (walk-away dahil, RF uzaktan da dahil ama evden değil).

---

## 7. İlgili dosyalar

| Dosya | İçerik |
|-------|--------|
| [telefon-kontrol-arastirma.md](telefon-kontrol-arastirma.md) | Yurtiçi/ithalat telefon + gümrük ~22–26k |
| [alternatif-karsilastirma.md](alternatif-karsilastirma.md) | Pandora vs StarLine; tek kutu telefon+walk-away |
| [pandora-arastirma.md](pandora-arastirma.md) | Pandora VX-4G detaylı araştırma (ix35, Hands Free, fiyat) |
| [parca-tedarik-tr.md](parca-tedarik-tr.md) | Yurtiçi SKU listesi |
| [uzaklasinca-otomatik-kilit.md](uzaklasinca-otomatik-kilit.md) | Walk-away seçenekleri + SST fiyat |
| [master-plan.md](master-plan.md) | Uygulama fazları |
| [sistem-mimarisi.md](sistem-mimarisi.md) | Teknik mimari |

---

## 8. Karar kaydı

| Tarih | Karar | Gerekçe |
|-------|-------|---------|
| 2026-07-09 | Şimdilik satın alma yok | Bütçe sıkışık |
| 2026-07-09 | İki marka sistemi sırayla kurma | Çift montaj, para israfı |
| 2026-07-09 | Hedef sistem: StarLine (telefon) | Evden GSM; birikim sonrası |
| 2026-07-09 | Walk-away: SST alternatif (~15k) | StarLine’dan ucuz ama telefon yok; sadece telefon vazgeçilirse |

---

## 9. StarLine’da walk-away var mı? (sık sorulan)

**Kısa cevap:** StarLine paketinin içinde **Start-Stop TR’deki gibi** “uzaklaşınca kapı kendi kilitlendi” **standart olarak yok**.

| Ne istiyorsun | StarLine ile | SST ile |
|---------------|-------------|---------|
| Uzaklaşınca **otomatik** kilit (tuşa basmadan) | ❌ fabrika özelliği değil; A93’te SST kadar net değil | ✅ ~2–3 m |
| Çıkarken **telefondan** kilitle | ✅ StarLine 2 uygulaması | ❌ (BT modülü yakın mesafe) |
| Çıkarken **fabrika kilit** tuşuna bas | ✅ SLAVE modu — alarm da silahlanır | — |
| Sürüşte otomatik kilit (kalkınca) | ⚙️ CAN ayarı (farklı şey) | — |

**SLAVE / tag ne yapar?** Fabrika kumandayla StarLine’ı birlikte yönetir veya güvenlik (anti-hırsızlık). **Walk-away auto lock değildir** — yine de çoğu gün kilit tuşuna basıyorsan pratikte iş görür.

**ix35 notu:** StarLine forumda ix35 push-start + SLAVE “çoğu zaman çalışır” deniyor; %100 fabrika walk-away garantisi yok.

**Sonuç:** StarLine = **evden telefon + uzaktan çalıştırma**. Walk-away “unutmayayım” için ya telefonla kilitle, ya fabrika kilit (SLAVE), ya da SST gibi ayrı sistem — **üçü birden pahalı/tekrarlı**.

---

*Son güncelleme: 2026-07-09*
