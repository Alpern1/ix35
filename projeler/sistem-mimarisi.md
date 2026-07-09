# Sistem Mimarisi — Kesin Tasarım Kararı

> 2012 Hyundai ix35 · Smart Key · Manuel · Prins LPG · Telefon kontrolü şart
> **Güncelleme (2026-07-09):** Yurtiçi tedarik kısıtı eklendi. StarLine teknik olarak ideal; **satın alma yurtiçi değil**. Aktif yurtiçi mimari: **Fortin EVO-ONE (MK3)** — evden telefon bu pakette **yok**.

---

## 1. Tek cümlelik karar

**Yurtiçi (gümrüksüz):** Fortin **EVO-ONE + Flashlink Mobile + T-Harness + RFK442** — mk3.com.tr'den sipariş edilebilir; ix35 push-start guide #23691 ile uyumlu.

**Evden telefon (hedef):** StarLine A93 v2 2CAN+2LIN + LTE — **sadece ithalat** (Plan B). Türkiye'de doğrudan satış yok.

Walk-away otomatik kilit **bu paketlerde varsayılan değil**; ikinci fazda Start-Stop TR proximity veya ayrı modül.

---

## 2. Kısıt matrisi (neden böyle)

| Kısıt | Etki |
|-------|------|
| Yurtdışından alamayız (gümrük) | StarLine, EVO-START LTE → **Plan B** |
| Evden telefonla çalıştırma | StarLine ✅ · Fortin MK3 ❌ · SST BT ❌ |
| ix35 push-start 2012 | StarLine ✅ · Fortin ✅ (#23691) · SST ⚠️ |
| Manuel program nötr | StarLine F15 ✅ · Fortin Ready Mode ⚠️ · SST ⚠️ |
| DIY | Her iki yol da mümkün; Fortin wire-to-wire zor |

---

## 3. Aktif mimari — Fortin (yurtiçi)

```
┌─────────────────────────────────────────────────────────────────┐
│                        SEN                                     │
│     RF kumanda (RFK442)  VEYA  OEM smart key 3× kilit          │
│     Menzil: ~50–500 m (RF); fabrika kumanda menzili (OEM)       │
│     ❌ Evden telefon bu pakette yok                             │
└───────────────────────────┬─────────────────────────────────────┘
                            │ 433 MHz RF / OEM RF
                            ▼
┌─────────────────────────────────────────────────────────────────┐
│  Fortin EVO-ONE (MK20064)                                        │
│  · Immobilizer bypass (push-start)                              │
│  · Remote start / alarm                                         │
│  · Manuel: Ready Mode (kapı kapanınca motor durur — seçenek)    │
└───────────────────────────┬─────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────────┐
│  THAR-ONE-KHY3 veya KHY7 + Fortin kılavuz #23691 kabloları      │
└───────────────────────────┬─────────────────────────────────────┘
                            │ CAN / PTS / brake / clutch / park
                            ▼
┌─────────────────────────────────────────────────────────────────┐
│  2012 Hyundai ix35                                              │
│  Smart Key · START/STOP · Manuel · Otomatik klima · Prins LPG   │
└─────────────────────────────────────────────────────────────────┘

[Kurulum — bir kez]
┌─────────────────────────────────────────────────────────────────┐
│  Flashlink Mobile (MK20126) + iOS/Android Flashlink uygulaması  │
└─────────────────────────────────────────────────────────────────┘
```

**Parça listesi (SKU):** [parca-tedarik-tr.md](parca-tedarik-tr.md)

---

## 4. Hedef mimari — StarLine (ithalat, Plan B)

Gümrük kabul edilirse evden telefon için bu mimari geçerli kalır:

```
Telefon (StarLine 2) → LTE Master 4G + nano-SIM → A93 v2 2CAN+2LIN → ix35 CAN/LIN
```

Detay: önceki StarLine blok diyagramı ve fonksiyon tabloları geçerli — [satin-alma-kanallari.md](satin-alma-kanallari.md) Plan B.

| Fonksiyon | Değer | Neden |
|-----------|-------|-------|
| Şanzıman | Manuel (МКПП) | Güvenlik |
| Fonksiyon 15 | Kapı kapanınca | Akşam telefon gerekmez |
| iKey bypass | Açık | Smart key |
| LTE | Master 4G | 2G riski |

---

## 5. Seçenek karşılaştırması (güncel)

| Seçenek | Yurtiçi sipariş | Evden telefon | ix35 PTS | Manuel | Walk-away |
|---------|-----------------|---------------|----------|--------|-----------|
| **Fortin EVO-ONE MK3** | ✅ | ❌ | ✅ #23691 | ⚠️ Ready Mode | ❌ |
| **StarLine A93 2CAN+2LIN** | ❌ gümrük | ✅ | ✅ | ✅ F15 | ⚙️ |
| **Start-Stop TR SST-019** | ✅ | ❌ (BT ~50 m) | ⚠️ | ⚠️ | ✅ |
| **MKON355 (CCURA GPS)** | ❌ tükendi | ❌ GPS only | — | — | — |
| **EVO-START LTE** | ❌ ithalat + NA ağ | ⚠️ TR? | ✅ | ✅ | ❌ |

---

## 6. Fortin — kurulumda programlanacak ayarlar

Flashlink ile ix35/Tucson 2010–2013 **Push-to-Start** firmware:

| Ayar | Değer | Neden |
|------|-------|-------|
| Araç | Tucson/ix35 PTS 2010–2013 | Guide #23691 |
| Şanzıman | **Manuel** — güvenlik loop kesilmemiş | Otomatik seçilirse tehlikeli |
| Manuel sequence bitiş | **Kapı kapanınca** (mümkünse) | StarLine F15 benzeri ritüel |
| Turbo timer | Kapalı | 1.6 GDI benzin |
| Hood pin | Açık | Zorunlu güvenlik |
| T-harness | KHY3 veya KHY7 | Flashlink sihirbazıyla doğrula |

**Ready Mode (manuel):** El freni + nötr + kapı kapanınca motor durur → sonra RF/OEM ile uzaktan çalıştır. Detay: RFK442 kullanım kılavuzu.

**iKey:** Fortin push-start prosedürü — PTS düğmesi ile programlama (guide #23691).

---

## 7. Prins LPG

| Konu | Sonuç |
|------|-------|
| Ek LPG modülü | Gerekmez |
| Uzaktan çalıştırma yakıtı | Benzin (Prins VSI) |
| Depoda benzin | Uzaktan çalıştırmadan önce olmalı |

---

## 8. Klima beklentisi

| Yapılır | Yapılmaz |
|---------|----------|
| Son AUTO/sıcaklık ile çalışır | Uygulamadan °C (Fortin'de evden app yok) |
| Park öncesi AUTO ayarla | Blue Link |

---

## 9. Walk-away (Faz 2)

| Yol | Yurtiçi? | Not |
|-----|----------|-----|
| Start-Stop TR SST | ✅ | Uzaktan çalıştırma hedefiyle çelişir |
| StarLine SLAVE/tag | ❌ ithalat | StarLine seçilirse |
| Telefonla kilitle | ✅ | Walk-away değil |

---

## 10. Riskler

| Risk | Önlem |
|------|-------|
| Yanlış T-harness | Flashlink'te araç seç, sonra harness sipariş et |
| MKON355 sanılması | CCURA = GPS; marş yapmaz |
| Evden telefon beklentisi | Fortin BOM'da telematik yok — karar ağacına bak |
| Manuel güvenlik loop | Kesme = otomatik mod; manuelde kesme |
| Gümrük sürprizi | StarLine Plan B'yi bilinçli seç |

---

## 11. Kaynaklar

| Kaynak | URL |
|--------|-----|
| Yurtiçi BOM | [parca-tedarik-tr.md](parca-tedarik-tr.md) |
| İthalat kanalları | [satin-alma-kanallari.md](satin-alma-kanallari.md) |
| Fortin PTS kılavuz | https://fortin.ca/download/23691/EVO-ONE_IG_REG_BI_HYU-Tucson_2010-2013_PTS_B_23691.pdf |
| StarLine şema | https://can.starline.ru |

---

*Son güncelleme: 2026-07-09*
