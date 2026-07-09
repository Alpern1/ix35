# Zorunlu Parçalar — 2012 ix35 (Smart Key, Manuel, Prins LPG)

> Fiyat yok. Sadece: ne şart, ne işe yarar.
> **Kesin karar:** StarLine A93 v2 ECO 2CAN+2LIN + LTE telematik — detay [sistem-mimarisi.md](sistem-mimarisi.md)

---

## Aracın kısıtları (değişmez)

| Kısıt | Sonuç |
|-------|-------|
| Smart Key + START/STOP | iKey immobilizer bypass (StarLine 2CAN) |
| Manuel vites | Program nötr prosedürü şart |
| 2012 ix35 (LM = Tucson) | can.starline.ru bağlantı şeması mevcut |
| Prins LPG | Ekstra LPG modülü şart değil; benzinle başlar |
| Telefon kontrolü isteniyor | GSM/LTE modül şart |
| Walk-away kilit isteniyor | Faz 2 — ayrı modül veya StarLine ayarı |

---

## GRUP 1 — Ana paket (zorunlu, tek seferde)

### 1. StarLine A93 v2 ECO 2CAN+2LIN

**Ne işe yarar:** Alarm + uzaktan çalıştırma beyni + CAN/LIN arayüzü + iKey bypass.

**Şart:** Autostart özellikli paket; manuel şanzıman profili.

**Olmadan:** Sistem yok.

---

### 2. StarLine LTE Master 4G (veya eşdeğer dahili LTE)

**Ne işe yarar:** Evden / sınırsız menzil telefon kontrolü.

**Şart:** Türkiye nano-SIM; StarLine 2 uygulaması.

**Olmadan:** Sadece kumanda menzili (~50–150 m) — senin istediğin olmaz.

---

### 3. nano-SIM (Türkiye operatörü)

**Ne işe yarar:** LTE modülün ağa bağlanması.

**Şart:** Veri açık; minimal GB tarifesi yeter.

---

### 4. Kaput switch (hood pin)

**Ne işe yarar:** Kaput açıkken uzaktan çalışmayı engeller.

**Şart:** Zorunlu güvenlik.

**Bağlantı:** Fabrika kaput switch'i veya ek switch.

---

### 5. Kurulum yazılımı — StarLine Master

**Ne işe yarar:** Firmware, fonksiyon tabloları, iKey öğrenme.

**Şart:** Kurulum günü (PC).

**Not:** Arabada kalmaz.

---

### 6. Kablolama (modül değil ama şart)

| Sinyal | Neden |
|--------|-------|
| CAN / LIN (2CAN+2LIN şeması) | Immobilizer, START/STOP, kilit, klima |
| El freni switch | Program nötr + güvenlik |
| Debriyaj switch | Manuel marş güvenliği |
| Kapı switch'leri | Silahlanma / iptal |
| START/STOP hattı | Push-start simülasyonu |
| Servis butonu | iKey öğrenme, valet |

**T-harness:** ix35 push-start için plug-and-play yok — şemaya göre kablo.

---

## GRUP 2 — Pakete dahil, ayrıca alınmaz

| Parça | Not |
|-------|-----|
| LCD kumanda | Yakın mesafe yedek; günlük ritüelde zorunlu değil |
| Siren | Alarm |
| Servis butonu | iKey |
| Antenler | LTE + (varsa) GPS |

---

## GRUP 3 — Walk-away (Faz 2, ayrı)

### Proximity lock modülü

**Ne işe yarar:** Uzaklaşınca kilit, yaklaşınca aç.

**Remote start ile aynı parça mı?** StarLine paketinde varsayılan değil; SLAVE/tag veya TR modül.

**MyKeyPremium:** Manuel uyumsuz — **elendi**.

---

## GRUP 4 — Opsiyonel (şimdilik gerek yok)

| Parça | Ne işe yarar |
|-------|--------------|
| Kabin sıcaklık sensörü | Uygulamada sıcaklık gösterme |
| Koltuk ısıtma aux | Uzaktan koltuk ısıtma tetikleme |
| GPS modülü | Konum takibi (LTE paketine bağlı) |

---

## Kesin mimari

```
[1] StarLine A93 v2 ECO 2CAN+2LIN
        ↓
[2] StarLine LTE Master 4G + nano-SIM
        ↓
[3] Hood pin + şema kabloları
        ↓
[4] StarLine Master (kurulum, bir kez)
        ↓
[5] StarLine 2 uygulaması (telefon)
```

**Ayrı (Faz 2):** Walk-away proximity modülü

---

## Kesinlikle OLMAYACAKLAR

| Parça / Yol | Neden |
|-------------|-------|
| Compustar + Fortin modüler yol | Telefon-only program nötr için StarLine daha uygun |
| MyKeyPremium | Manuel vites desteklemiyor |
| Start-Stop TR (tek başına) | Evden GSM menzili yok |
| DroneMobile | TR LTE uyumsuz |
| Blue Link | 2012'de donanım yok |
| Aftermarket kumanda START ritüeli | Telefon silahlanma yeterli |

---

## Sonraki adım

1. [master-plan.md](master-plan.md) → **Faz 1:** Satıcı teyidi
2. Sipariş → Faz 2
3. Kurulum → Faz 4–5

---

*Son güncelleme: 2026-07-09*
