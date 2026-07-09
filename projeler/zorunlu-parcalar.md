# Zorunlu Parçalar — 2012 ix35 (Smart Key, Manuel, Prins LPG)

> Fiyat yok. Sadece: ne şart, ne işe yarar, ne değil.
> Karar: modüler yol (Fortin + manuel uyumlu remote start + GSM) vs tek paket (TR/Rus) — uyumluluk doğrulanacak.

---

## Aracın kısıtları (değişmez)

| Kısıt | Sonuç |
|-------|-------|
| Smart Key + START/STOP | Immobilizer bypass şart |
| Manuel vites | Manuel uyumlu remote start şart; rezervasyon modu şart |
| 2012 ix35 (LM = Tucson) | Fortin firmware: Tucson 2010–2013 Push-Start |
| Prins LPG | Ekstra LPG modülü şart değil; benzinle başlar |
| Telefon kontrolü isteniyor | GSM/LTE telematik modül şart |
| Walk-away kilit isteniyor | Ayrı modül (remote start paketinin parçası değil) |

---

## GRUP 1 — Uzaktan çalıştırma (zorunlu)

### 1. Remote Start Beyni (manuel uyumlu)

**Ne işe yarar:** Motoru uzaktan çalıştırır/durdurur; rezervasyon modunu yönetir; güvenlik kontrollerini yapar.

**Şart:** "Manuel transmission" veya "reservation mode" desteklemeli. Otomatik vites kiti **kullanılmaz**.

**Aday markalar:** Compustar CMX serisi, Viper/Clifford manuel serisi, Fortin EVO-ONE (manuel modda)

---

### 2. Immobilizer Bypass + CAN Arayüzü

**Ne işe yarar:** Smart key immobilizer'ı uzaktan çalıştırma sırasında geçici olarak devreye sokar; CAN bus üzerinden araca konuşur.

**Şart:** 2012 ix35/Tucson Smart-Key için doğru firmware.

**Kesin aday:** Fortin EVO-ONE veya EVO-ALL  
**Firmware:** Hyundai Tucson Smart-Key 2010–2013 (Fortin guide #23691)

**Olmadan:** Motor çalışmaz — immobilizer keser.

---

### 3. Kaput Switch'i (Hood Pin)

**Ne işe yarar:** Kaput açıkken uzaktan çalışmayı engeller.

**Şart:** Zorunlu güvenlik — Fortin kılavuzu "MANDATORY INSTALL" diyor.

**Olmadan:** Kurulmamalı.

---

### 4. Kablolama / Sinyal Bağlantıları (modül değil ama şart)

| Sinyal | Neden şart |
|--------|------------|
| Debriyaj switch | Manuel vites — marş için debriyaj bypass |
| El freni switch | Vites boşta + el freni doğrulaması |
| Kapı switch'leri | Rezervasyon modu — kapı açılınca iptal |
| Tachometre (devir) | Manuel vites remote start — motor devrini algılar |
| START/STOP düğmesi | Push-start simülasyonu |
| Fren pedalı switch | Güvenlik + takeover |
| CAN bus (OBD veya kick panel) | Immobilizer + kilit entegrasyonu |

**T-harness:** 2012 ix35 push-start için plug-and-play yok. Kablo kablo bağlantı (Fortin guide #23691).

---

### 5. Programlama Aracı

**Ne işe yarar:** Fortin modüle araç firmware'i yükler.

**Şart:** Fortin FlashLink Updater (veya FlashLink Mobile)

**Not:** Kurulum için bir kez gerekir; arabada kalmaz.

---

## GRUP 2 — Telefon kontrolü (zorunlu — senin isteğin)

### 6. GSM / LTE Telematik Modül

**Ne işe yarar:** Telefon uygulamasından sınırsız menzille çalıştır/durdur/kilit.

**Şart:** Türkiye SIM / operatör uyumu.

**Seçenekler (biri seçilecek):**

| Seçenek | Yapı | TR uyumu |
|---------|------|----------|
| A | Fortin EVO-ONE + ayrı GSM modül (MK3 paketleri) | Sorulacak |
| B | StarLine / Pandora (GSM entegre alarm) | TR'de satılıyor; ix35 CAN uyumu sorulacak |
| C | Start-Stop TR SST serisi | Yerli; ix35 manuel uyumu sorulacak |
| D | DroneMobile | TR LTE zayıf — **önerilmez** |

**Olmadan:** Sadece kumanda menzili (~50–150 m) kalır — senin istediğin "evden çalıştırma" olmaz.

---

## GRUP 3 — Walk-away otomatik kilit (ayrı proje, ayrı modül)

### 7. Proximity Lock Modülü

**Ne işe yarar:** Uzaklaşınca kilit, yaklaşınca aç.

**Şart:** Smart key CAN entegrasyonu.

**Remote start ile aynı parça mı?** Hayır — ayrı modül veya anahtarcı paketi.

**MyKeyPremium:** Manuel vites uyumsuz — **bu araç için elendi**.

---

## GRUP 4 — Opsiyonel (şimdilik karar verme)

| Parça | Ne işe yarar | Zorunlu mu? |
|-------|--------------|-------------|
| 2-yönlü uzaktan kumanda | Menzil + geri bildirim (telefon yedeği) | Hayır ama faydalı |
| Koltuk ısıtma aux kablosu | Uzaktan koltuk ısıtma tetikleme | Hayır |
| Kabin sıcaklık sensörü (thermistor) | Uygulamada sıcaklık gösterme | Hayır |
| Alarm/siren | Güvenlik | Hayır |

---

## Önerilen mimari (karar taslağı)

Modüler ve dokümantasyonu net olan yol:

```
[1] Compustar CMX (manuel remote start beyin)
        ↓
[2] Fortin EVO-ONE (immobilizer bypass, Tucson 2010-2013 PTS firmware)
        ↓
[3] Hood pin switch
        ↓
[4] Kablolama (debriyaj, el freni, kapı, tach, START/STOP, CAN)
        ↓
[5] GSM modül (TR uyumlu — seçim bekliyor)
        ↓
[6] FlashLink (kurulum aracı, bir kez)
```

**Ayrı:** [7] Walk-away modül (TR anahtarcı veya import — ayrı karar)

---

## Kesinlikle OLMAYACAKLAR

| Parça / Yol | Neden |
|-------------|-------|
| MyKeyPremium | Manuel vites desteklemiyor |
| Otomatik vites remote start kiti | Güvenlik riski |
| DroneMobile (TR için) | LTE/TR servis uyumsuz |
| Blue Link / myHyundai | 2012 ix35'te donanım yok |
| LPG'ye özel bypass modülü | Prins zaten benzinle başlıyor |

---

## Sonraki adım (fiyattan önce)

1. **GSM modül seçimi:** Fortin GSM paketi mi, StarLine/Pandora mı, Start-Stop TR mi? → Satıcıya "2012 ix35 manuel smart key" diye sor
2. **Walk-away:** Aynı satıcıdan mı, ayrı mı?
3. **Uyumluluk teyidi** gelince parça listesi kesinleşir → o zaman fiyat

---

*Son güncelleme: 2026-07-09*
