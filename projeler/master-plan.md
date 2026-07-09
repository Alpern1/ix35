# Master Uygulama Planı

> Gerçek iş fazları — "bayiye sor" değil, "sipariş ver / kur / test et".
> **Güncelleme:** Faz 1 artık **parça tedarik** — StarLine yurtiçi satılmıyor; Fortin MK3 BOM aktif.

---

## Faz haritası

```
Faz 1          Faz 2           Faz 3            Faz 4           Faz 5
KARAR+SİPARİŞ  TESLİM          KUR              AYARLA          YAŞA
│              │               │                │               │
parca-tedarik  Kutu aç         Kablo işi        Flashlink       Günlük ritüel
karar ağacı    eksik kontrol   (en zor)         Ready Mode      RF / OEM
```

---

## Faz 0 — Karar (şimdi, ücretsiz)

**Soru:** Evden telefon için gümrük kabul ediyor musun?

| Cevap | Yol | Dosya |
|-------|-----|-------|
| **Hayır** | Fortin MK3 BOM | [parca-tedarik-tr.md](parca-tedarik-tr.md) Bölüm 2 |
| **Evet** | StarLine ithalat | [satin-alma-kanallari.md](satin-alma-kanallari.md) Plan B |

**Bitti sayılır:** Hangi BOM'u sipariş edeceğin yazılı net.

---

## Faz 1 — Satın al (yurtiçi, internet)

**Ne elde ediyorsun:** Kutular elinde — montaja hazır parça.

### Fortin yolu (gümrük yok)

```
□ EVO-ONE MK20064 — mk3.com.tr
□ Flashlink Mobile MK20126 — mk3.com.tr
□ RFK442 MK20083 — mk3.com.tr
□ T-Harness: Flashlink gelince SKU teyit → KHY3 veya KHY7 sipariş
□ MKON355 ALMA
```

**Bitti sayılır:** EVO-ONE + Flashlink + RF açıldı; eksik parça yok.

**Pes etme?** MK3 tükenirse — Flashlink Mobile ve EVO-ONE stokta; T-harness alternatif SKU dene.

### StarLine yolu (gümrük var)

```
□ A93 v2 2CAN+2LIN
□ LTE Master 4G
□ nano-SIM
```

Kanal: [satin-alma-kanallari.md](satin-alma-kanallari.md) Plan B.

---

## Faz 2 — Teslim ve doğrula

| Görev | Bitti sayılır |
|-------|---------------|
| Kutuları aç, SKU etiketleri fotoğra | parca-tedarik-tr.md checklist |
| Flashlink Mobile şarj / uygulama kur | Telefonda Flashlink açılıyor |
| Fortin: uygulamada **2012 Tucson PTS** ara | Doğru T-harness SKU yazılı |
| Eksik parça varsa | MK3 iade/değişim talebi |

---

## Faz 3 — Kur (asıl iş)

| Alt adım | Zorluk |
|----------|--------|
| Konsol sökme, EVO-ONE montajı | Orta |
| T-harness + guide #23691 kabloları | Zor |
| Hood pin, el freni, debriyaj | Orta |
| Manuel güvenlik loop kontrolü | Kritik — kesilmemiş olmalı |

**Kaynak:** https://fortin.ca/download/23691/EVO-ONE_IG_REG_BI_HYU-Tucson_2010-2013_PTS_B_23691.pdf

**Bitti sayılır:** Akü bağlı, kısa devre yok, modül LED yanıyor.

---

## Faz 4 — Ayarla (Flashlink + ilk çalıştırma)

| Adım | Araç |
|------|------|
| ix35 PTS firmware yükle | Flashlink Mobile |
| Manuel / Ready Mode ayarları | Flashlink seçenekleri |
| Immobilizer öğrenme | Guide #23691 prosedürü |
| İlk Ready Mode testi | Kapı kapanınca motor durmalı |
| İlk uzaktan çalıştırma | RFK442 veya OEM 3× lock |

**Bitti sayılır:** RF'den çalışıyor; klima son AUTO ile devrede.

**Evden telefon:** Fortin yolunda bu fazda **yok** — StarLine seçtiysen GSM testi burada.

---

## Faz 5 — Yaşa (alışkanlık)

### Fortin (RF)

```
Akşam:  N + el freni → Ready Mode prosedürü → kapı kapat → motor durur
Sabah:  RF START veya OEM 3× lock → 10–15 dk → bin → frene bas → PTS bir kez
```

### StarLine (ithalat yolu)

```
Akşam:  program nötr → kapı kapat (F15)
Sabah:  StarLine 2 / Siri → çalıştır
```

Detay: [kullanim-senaryolari.md](kullanim-senaryolari.md)

---

## [Opsiyonel] Faz 6 — Walk-away

Start-Stop TR veya ayrı proximity. [uzaklasinca-otomatik-kilit.md](uzaklasinca-otomatik-kilit.md)

Uzaktan çalıştırma çalıştıktan sonra.

---

## Pes etme rehberi (dürüst)

| Durum | Pes et? | Alternatif |
|-------|---------|------------|
| Yurtiçi + evden telefon ikisi şart | **Plan yok** | Gümrük kabul et veya menzil beklentisini düşür |
| MKON355 aldım, telefon çalışmıyor | Hayır | CCURA GPS'tir — EVO-ONE + RF doğru yol |
| Yanlış T-harness | Hayır | Flashlink teyit, değişim |
| Montaj aşıyor | Belki | Sadece Faz 3'ü ustaya ver |
| StarLine gümrükte takıldı | Hayır | Plan A Fortin'e geç |

---

## Hızlı referans dosyalar

| Dosya | İçerik |
|-------|--------|
| [parca-tedarik-tr.md](parca-tedarik-tr.md) | SKU, stok, karar ağacı |
| [sistem-mimarisi.md](sistem-mimarisi.md) | Mimari diyagram |
| [zorunlu-parcalar.md](zorunlu-parcalar.md) | BOM özet |

---

*Son güncelleme: 2026-07-09*
