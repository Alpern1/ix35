# Zorunlu Parçalar — 2012 ix35 (Smart Key, Manuel, Prins LPG)

> Fiyat yok. Sadece: ne şart, ne işe yarar, nereden alınır.
> **Kesin karar (yurtiçi):** Fortin EVO-ONE paketi — detay [parca-tedarik-tr.md](parca-tedarik-tr.md)
> **Evden telefon (ithalat):** StarLine Plan B — [satin-alma-kanallari.md](satin-alma-kanallari.md)

---

## Aracın kısıtları (değişmez)

| Kısıt | Sonuç |
|-------|-------|
| Smart Key + START/STOP | Immobilizer bypass şart (Fortin EVO-ONE veya StarLine 2CAN) |
| Manuel vites | Program nötr / Ready Mode prosedürü şart |
| 2012 ix35 (LM = Tucson) | Fortin guide #23691; StarLine can.starline.ru |
| Prins LPG | Ekstra LPG modülü şart değil; benzinle başlar |
| Evden telefon | **Yurtiçi Fortin paketinde yok** — StarLine ithalat veya ödün ver |
| Yurtdışı / gümrük yok | StarLine ve EVO-START LTE elenir (satın alma aşamasında) |
| Walk-away kilit | Faz 2 — SST veya ayrı modül |

---

## YOL A — Yurtiçi Fortin (aktif BOM)

Tam tablo: [parca-tedarik-tr.md](parca-tedarik-tr.md)

### GRUP 1 — Sipariş listesi (MK3)

| # | Parça | SKU | Olmadan |
|---|-------|-----|---------|
| 1 | Fortin EVO-ONE | MK20064 | Sistem yok |
| 2 | Flashlink Mobile | MK20126 | ix35 firmware yüklenemez |
| 3 | T-Harness KHY3 veya KHY7 | MK20139 / MK20141 | Kablo işi çok artar |
| 4 | RFK442 2-yönlü RF kit | MK20083 | Uzaktan menzil yok (sadece OEM 3× lock) |
| 5 | Hood pin | Pakette | Güvenlik ihlali |

### GRUP 2 — Pakete dahil / ayrıca alınmaz

| Parça | Not |
|-------|-----|
| Harness setleri (20-pin, CAN, relay) | EVO-ONE kutusunda |
| Uyarı etiketi | Kutuda |
| nano-SIM | Fortin RF yolunda **gerekmez** |

### GRUP 3 — Bilerek alınmayacaklar

| Parça | Neden |
|-------|-------|
| MKON355 (EVO-ONE + CCURA GPS) | Tükendi; CCURA marş yapmaz |
| Flashlink 4 USB (MK20125) | Tükendi — Mobile kullan |
| EVO-START LTE | MK3'te yok; ithalat + NA ağı |

### GRUP 4 — Kablolama (modül değil, şart)

| Sinyal | Neden |
|--------|-------|
| CAN (OBD veya T-harness) | Immobilizer, START/STOP |
| PTS (START/STOP düğmesi) | Push-start simülasyonu |
| El freni + debriyaj | Manuel güvenlik |
| Kaput pin | Uzaktan çalışma kilidi |
| Kapı switch | Ready Mode / alarm |

Kılavuz: Fortin guide #23691 (wire-to-wire noktaları).

---

## YOL B — StarLine (ithalat, evden telefon)

Gümrük kabul edilirse:

| # | Parça | Olmadan |
|---|-------|---------|
| 1 | StarLine A93 v2 ECO 2CAN+2LIN | Sistem yok |
| 2 | StarLine LTE Master 4G | Evden telefon yok |
| 3 | nano-SIM (TR operatör) | Ağ yok |
| 4 | Hood pin | Güvenlik |
| 5 | StarLine Master (PC, kurulum) | Firmware yüklenemez |

Detay: önceki StarLine GRUP 1–4 içeriği geçerli — [satin-alma-kanallari.md](satin-alma-kanallari.md).

---

## Kesin mimari (yurtiçi)

```
[1] EVO-ONE MK20064
        ↓
[2] Flashlink Mobile MK20126 (kurulum)
        ↓
[3] T-Harness KHY3/KHY7 + guide #23691 kabloları
        ↓
[4] RFK442 MK20083
        ↓
[5] RF kumanda veya OEM 3× lock ile çalıştır
```

**Evden telefon bu listede yok.**

---

## Kesinlikle OLMAYACAKLAR

| Parça / Yol | Neden |
|-------------|-------|
| MKON355 “GSM hediyeli” paket | GPS takip; uzaktan marş değil |
| Start-Stop TR (tek başına, evden hedef) | GSM yok; BT menzil |
| MyKeyPremium | Manuel uyumsuz |
| DroneMobile | TR LTE uyumsuz |
| Blue Link | 2012'de donanım yok |
| Generic evrensel push-start | ix35 iKey/CAN yok |

---

## Sonraki adım

1. [parca-tedarik-tr.md](parca-tedarik-tr.md) → karar ağacı: evden telefon vs yurtiçi
2. [master-plan.md](master-plan.md) → **Faz 1:** Parça siparişi
3. Flashlink gelince → T-harness SKU teyidi → kurulum

---

*Son güncelleme: 2026-07-09*
