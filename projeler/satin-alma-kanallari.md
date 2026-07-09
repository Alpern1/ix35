# Satın Alma Kanalları — İnternet Araştırması

> Bayi aramadan, internetten doğrulanabilir bilgiler.
> Son güncelleme: 2026-07-09

---

## Önemli uyarı: Türkiye'de "StarLine" isim karışıklığı

Google'da `Starline site:.tr` aratınca çıkan sitelerin **çoğu iş güvenliği** (eldiven, baret, ayakkabı) satıyor. Bunlar **Rus otomobil alarm markası StarLine ile aynı değil**.

| Aradığın | Değil |
|---------|-------|
| StarLine A93 / 2CAN+2LIN otomobil alarmı | Starline iş eldiveni, baret |
| can.starline.ru bağlantı şemaları | Varol Elektrik iş güvenliği bayii |

---

## Uyumluluk — bayi olmadan internetten doğrula

**Tek kaynak:** [can.starline.ru](https://can.starline.ru)

```
Hyundai → Tucson / ix35 → 2012 → Start-Stop (smart key)
```

**Ne indirirsin:**
- Bağlantı noktaları (hangi kablo nereye)
- CAN/LIN firmware dosyası
- iKey bypass prosedürü

**Kanıt (forum):**
- [ix35 2014 Start-Stop kurulum](https://support.starline.ru/communities/10/topics/41978-starline-a93-2can2lin-na-hyundai-tucson-ix35-2014-start-stop)
- [ix35 2012 Start-Stop](https://support.starline.ru/communities/10/topics/62980-hyundai-ix35-2012-knopka-start-stop)
- [iKey Hyundai/Kia 2012–2016](http://www.alarmstarline.com/2016/02/09/ikey-bypass-for-the-whole-model-range/)

2012 ix35 push-start için can.starline.ru'da şema mevcut — bu, bayiye sormanın internet karşılığı.

---

## Alınacak paket (SKU mantığı)

Tek paket hedefi — modüler parça avcılığına gerek yok:

| Parça | Aranacak isim |
|-------|---------------|
| Ana ünite | **StarLine A93 v2 ECO 2CAN+2LIN** |
| Telematik | **StarLine LTE Master 4G** VEYA pakette **GSM/LTE dahil** versiyon |
| Tam paket örneği | `A93 2CAN+2LIN GSM ECO` / `A93 2CAN+2LIN GSM GPS` |

**Resmi mağaza paket fiyatı (Rusya, 2026):** A93 v2 2CAN+2LIN ≈ 20.650 RUB (GSM/LTE ayrı veya paket) — [store.starline.ru](https://store.starline.ru/catalog/avtosignalizatsii/starline_a93_v2_2can_2lin/)

LTE Master uyumlu modeller: A93 v2, A93 v2 2CAN+2LIN — [store.starline.ru LTE Master](https://store.starline.ru/catalog/dopolnitelnoe_oborudovanie/starline_lte_master_3_test/)

---

## Online satın alma kanalları

### 1. Resmi — store.starline.ru (Rusya)

| | |
|--|--|
| **Artı** | Doğru ürün, güncel firmware, LTE Master ayrıca satılıyor |
| **Eksi** | Türkiye'ye kargo / gümrük / Rus ödeme — sipariş öncesi site kargo politikasını kontrol et |
| **URL** | https://store.starline.ru/catalog/avtosignalizatsii/starline_a93_v2_2can_2lin/ |

### 2. Uluslararası — alarmstarline.com

| | |
|--|--|
| **Artı** | İngilizce; A93 2CAN+2LIN **GSM** paketleri listeleniyor; SLAVE açıklaması var |
| **Eksi** | Türkiye kargo ve gümrük — sipariş öncesi "ships to Turkey" kontrol et |
| **URL** | https://www.alarmstarline.com/car-security-systems/ |

Listelenen varyantlar: A93 2CAN+2LIN, A93 2CAN+2LIN GSM, A93 2CAN+2LIN GSM GPS+GLONASS

### 3. Rusya / Ukrayna e-ticaret

| Site | Not |
|------|-----|
| [starlin-security.ru](https://starlin-security.ru/catalog/signalizatsii_s_avtozapuskom/701/) | A93 + montaj odaklı; kargo TR belirsiz |
| [mircaraudio.com](https://mircaraudio.com/avtosignalizaciya-starline-a93-v2-2can-2lin/) | Ukrayna; TR kargo kontrol |

### 4. Türkiye — yerli alternatifler (farklı ürün!)

| Site | Ürün | Evden telefon? | ix35 push-start? |
|------|------|----------------|------------------|
| [startstopturkiye.com](https://startstopturkiye.com/) | SST serisi | ❌ RF 50–200 m | Sorulmalı; GSM yok |
| [durer.com.tr](https://www.durer.com.tr/) | Çin evrensel kit | Uygulama var ama generic | Profesyonel montaj şart; ix35 kanıtı yok |
| guvenix, smartrole vb. | Ev/iş alarmı | Ev alarmı — **araba değil** | ❌ |

**Sonuç:** Türkiye'de StarLine A93'ü doğrudan satan güvenilir .tr e-ticaret sitesi **bulamadık**. TR pazarı çoğunlukla montajcı üzerinden işliyor. Online yol: **resmi Rus mağaza veya uluslararası satıcı + kargo**.

### 5. SIM kart (Türkiye — kesin online)

| | |
|--|--|
| **Ne alırsın** | nano-SIM, sadece veri, düşük GB |
| **Nereden** | Operatör e-sim / online başvuru veya market |
| **Not** | StarLine her operatör SIM'i ile çalışır (M21/M31/LTE dokümantasyonu) |

---

## Sipariş öncesi kutu kontrol listesi (internetten sipariş verirken)

Satıcı sayfasında şunlar **yazılı** olmalı:

```
□ StarLine A93 v2 (ECO değilse de olur ama v2 olmalı)
□ 2CAN+2LIN modülü DAHİL (sadece "A93 base" değil)
□ Uzaktan çalıştırma (autostart) destekli
□ GSM veya LTE modülü — hangisi olduğu net
□ LCD kumanda dahil
□ Pin-konvert (login/şifre kartı) gelecek
```

**Alma:**
- Sadece "Starline" yazan generic alarm
- "Evrensel push start kit" (ix35 CAN/iKey yok)
- GSM modülü olmadan paket (evden çalıştırma olmaz)

---

## Gümrük / kargo notu

Rusya veya Ukrayna'dan elektronik ithalat:
- Gümrük vergisi ve kargo süresi değişken
- Türkiye'ye gönderim yapan satıcıyı seç; göndermeyen satıcıdan alma
- Bu belirsizlik "pes etme" sebebi değil — sipariş öncesi tek kontrol: **kargo adresine geliyor mu?**

---

## Özet karar

| Soru | İnternet cevabı |
|------|-----------------|
| ix35 uyumlu mu? | **Evet** — can.starline.ru + forum |
| TR'den online StarLine alarm sitesi? | **Nadiren**; resmi/uluslararası kargo yolu |
| Hangi paket? | A93 v2 2CAN+2LIN + LTE/GSM |
| Bayi şart mı? | **Hayır** — uyumluluk can.starline.ru'dan; montaj DIY veya sonra usta |

---

*Son güncelleme: 2026-07-09*
