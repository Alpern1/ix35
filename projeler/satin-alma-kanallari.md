# Satın Alma Kanalları — İnternet Araştırması

> Son güncelleme: 2026-07-09
> **Öncelik:** Yurtiçi, gümrüksüz → [parca-tedarik-tr.md](parca-tedarik-tr.md)
> StarLine ve yurtdışı kanallar → **Plan B (gümrük)** — bilinçli seçim için tutulur.

---

## Özet (tek bakış)

| Soru | Cevap |
|------|-------|
| Yurtiçi online, gümrüksüz parça var mı? | **Evet** — Fortin MK3 BOM |
| Evden telefon yurtiçi pakette var mı? | **Hayır** — doğrulanabilir satıcı yok |
| StarLine TR'den alınır mı? | **Hayır** — ithalat şart |
| İlk sipariş ne? | [parca-tedarik-tr.md](parca-tedarik-tr.md) Bölüm 2 veya karar ağacı |

---

## PLAN A — Yurtiçi (önerilen satın alma)

### MK3.com.tr — Fortin yetkili satıcı

| | |
|--|--|
| **Artı** | Türkiye kargo; fatura; Fortin orijinal; SKU net |
| **Eksi** | EVO-START LTE yok; MKON355 tükendi; Flashlink USB tükendi |
| **URL** | https://www.mk3.com.tr/kategori/fortin-uzaktan-calistirma |
| **BOM** | [parca-tedarik-tr.md](parca-tedarik-tr.md) |

Sipariş edilecekler (özet):

| SKU | Ürün |
|-----|------|
| MK20064 | EVO-ONE |
| MK20126 | Flashlink Mobile |
| MK20139 veya MK20141 | T-Harness KHY3/KHY7 |
| MK20083 | RFK442 |

**Alma:** MKON355 (GPS hediyesi marş yapmaz).

### fsatuning.com — Start-Stop Türkiye

| | |
|--|--|
| **Artı** | Walk-away pakette; Türkiye kargo |
| **Eksi** | Evden telefon yok (BT ~50 m); ix35 uyumu site üzerinde yok |
| **URL** | https://fsatuning.com/magaza/ |
| **Ürün** | SST-019 (+ isteğe bağlı BT modülü) |

### nano-SIM

| | |
|--|--|
| **Fortin yolu** | Gerekmez |
| **StarLine Plan B** | nano-SIM, veri tarifesi — operatör e-SIM veya mağaza |

---

## PLAN B — İthalat (gümrük — bilinçli seçim)

> Kullanıcı kısıtı: yurtdışından alamayız. Bu bölüm **sadece** gümrük kabul edilirse geçerli.

### Gümrük gerçeği (Türkiye)

| Kalem | Not |
|-------|-----|
| Gümrük vergisi | Elektronik ithalatta oran değişken; GTİP ve menşe ülkeye bağlı |
| KDV | İthalat üzerine |
| Gümrük müşavirliği | Çoğu kargo bu aşamada ek maliyet |
| Süre | Rusya 2–6 hafta; gümrükte bekleme eklenir |
| Risk | Yanlış paket, firmware Rusça arayüz, iade zor |

**Sonuç:** StarLine teknik olarak en iyi evden-telefon çözümü; **maliyet ve lojistik** nedeniyle şu an pasif.

### StarLine — uyumluluk (internet, bayi değil)

**Kaynak:** [can.starline.ru](https://can.starline.ru) → Hyundai → Tucson/ix35 → 2012 → Start-Stop

| Parça | Aranacak isim |
|-------|---------------|
| Ana ünite | StarLine A93 v2 ECO 2CAN+2LIN |
| Telematik | StarLine LTE Master 4G |
| Tam paket | `A93 2CAN+2LIN GSM ECO` veya GSM/LTE dahil varyant |

**Forum kanıtı:**
- [ix35 2014 Start-Stop](https://support.starline.ru/communities/10/topics/41978-starline-a93-2can2lin-na-hyundai-tucson-ix35-2014-start-stop)
- [ix35 2012 Start-Stop](https://support.starline.ru/communities/10/topics/62980-hyundai-ix35-2012-knopka-start-stop)

### StarLine online kanallar (yurtdışı)

| Site | URL | TR kargo |
|------|-----|----------|
| Resmi mağaza (RU) | https://store.starline.ru/catalog/avtosignalizatsii/starline_a93_v2_2can_2lin/ | Sipariş öncesi kontrol |
| alarmstarline.com | https://www.alarmstarline.com/car-security-systems/ | Sipariş öncesi kontrol |
| starlin-security.ru | https://starlin-security.ru/ | Belirsiz |

### Fortin EVO-START LTE (ithalat)

| | |
|--|--|
| **Ne işe yarar** | Fortin resmi evden telefon uygulaması |
| **Eksi** | MK3'te satılmıyor; ağ kapsamı **Kuzey Amerika**; TR SIM kanıtı yok |
| **Kaynak** | https://fortin.ca/en/resources/evo-start-lte/ |

### Türkiye'de "StarLine" isim karışıklığı

Google `Starline site:.tr` → çoğu **iş güvenliği** (eldiven, baret). Rus otomobil alarmı **değil**.

---

## Elendi kanallar

| Site / ürün | Neden |
|-------------|-------|
| Oto Yapay Zeka | Fabrika start-stop uyarısı; iPhone zayıf |
| durer.com.tr generic kit | ix35 kanıtı yok |
| guvenix / smartrole ev alarmı | Araba değil |
| Pandora .tr mağaza | Doğrulanamadı |

---

## Sipariş öncesi kutu kontrolü

### Fortin (Plan A)

```
□ MK20064 EVO-ONE (MKON355 değil)
□ MK20126 Flashlink Mobile
□ Doğru T-harness (Flashlink teyidi sonrası)
□ MK20083 RFK442 (uzaktan menzil için)
```

### StarLine (Plan B)

```
□ A93 v2 + 2CAN+2LIN dahil
□ GSM veya LTE modülü net
□ Pin-konvert kartı
□ Autostart destekli paket
```

---

## Karar

| Hedef | Kanal |
|-------|-------|
| Parça elinde, gümrük yok | **Plan A** → MK3 BOM |
| Evden telefon şart, gümrük OK | **Plan B** → StarLine |
| Walk-away öncelik, telefon ikincil | Start-Stop TR (Plan A alt) |

Detaylı BOM ve stok: [parca-tedarik-tr.md](parca-tedarik-tr.md)

---

*Son güncelleme: 2026-07-09*
