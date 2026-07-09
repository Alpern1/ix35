# Sistem Mimarisi — Kesin Tasarım Kararı

> 2012 Hyundai ix35 · Smart Key · Manuel · Prins LPG · Telefon kontrolü şart
> Bu dosya **açık soru bırakmadan** hangi sistemin, hangi parçalarla kurulacağını tanımlar.

---

## 1. Tek cümlelik karar

**StarLine A93 v2 ECO 2CAN+2LIN + GSM/LTE telematik** — ix35/Tucson push-start için kanıtlı, program nötrü **telefondan** yapılabilen, Türkiye SIM ile çalışan entegre paket.

Walk-away otomatik kilit **aynı markadan zorunlu değil**; ikinci fazda TR proximity modülü veya StarLine SLAVE/proximity ayarı ile eklenir.

---

## 2. Neden bu sistem? (elenenler dahil)

| Seçenek | Telefon (evden) | ix35 push-start | Manuel program nötr | Walk-away | Karar |
|---------|-----------------|-----------------|---------------------|-----------|-------|
| **StarLine A93 v2 2CAN+2LIN + GSM/LTE** | ✅ | ✅ (forum + can.starline.ru) | ✅ telefonla silahlanma | ⚙️ ayrı ayar | **SEÇİLDİ** |
| Fortin EVO-ONE + Compustar + MK3 GSM | ✅ (MK3) | ✅ (guide #23691) | ⚠️ çoğunlukla kumanda START 2.5 sn | ❌ ayrı | Elendi — telefon-only ritüel zor |
| Start-Stop TR SST serisi | ❌ (RF 50–200 m; BT modülü ~50 m) | ⚠️ sorulmalı | ⚙️ farklı protokol | ✅ pakette | Elendi — evden menzil yok |
| DroneMobile | ❌ TR LTE | — | — | — | Elendi |
| MyKeyPremium | — | — | ❌ manuel uyumsuz | ✅ | Elendi |
| Blue Link / myHyundai | — | — | — | — | 2012'de donanım yok |

---

## 3. Blok diyagramı

```
┌─────────────────────────────────────────────────────────────────┐
│                        SEN (ev / iş)                            │
│                   StarLine mobil uygulama                       │
│              (iOS / Android — StarLine 2)                     │
└───────────────────────────┬─────────────────────────────────────┘
                            │ GSM / LTE (sınırsız menzil)
                            ▼
┌─────────────────────────────────────────────────────────────────┐
│  StarLine LTE Master 4G  (veya pakette dahili GSM/LTE)          │
│  + Türkiye nano-SIM (Turkcell / Vodafone / Türk Telekom)        │
└───────────────────────────┬─────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────────┐
│  StarLine A93 v2 ECO — ana alarm + uzaktan çalıştırma beyni     │
└───────────────────────────┬─────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────────┐
│  StarLine 2CAN+2LIN modülü                                      │
│  · ix35/Tucson 2010–2014 CAN/LIN bağlantı şeması                │
│  · iKey immobilizer bypass (push-start, CopyKey gerekmez)       │
│  · START/STOP simülasyonu                                       │
│  · Klima / kilit / dörtlü entegrasyonu                          │
└───────────────────────────┬─────────────────────────────────────┘
                            │ CAN / LIN / düşük akım
                            ▼
┌─────────────────────────────────────────────────────────────────┐
│  2012 Hyundai ix35                                              │
│  Smart Key · START/STOP · Manuel · Otomatik klima · Prins LPG   │
└─────────────────────────────────────────────────────────────────┘

[İsteğe bağlı — Faz 2]
┌─────────────────────────────────────────────────────────────────┐
│  Walk-away proximity modülü (TR anahtarcı veya StarLine tag)    │
└─────────────────────────────────────────────────────────────────┘
```

---

## 4. Parça listesi (kesin SKU mantığı)

| # | Parça | Görev | Not |
|---|-------|-------|-----|
| 1 | **StarLine A93 v2 ECO 2CAN+2LIN** | Alarm + uzaktan çalıştırma ana ünite | Autostart fonksiyonu açık paket |
| 2 | **2CAN+2LIN modülü** | ix35 CAN/LIN konuşması | Pakete dahil |
| 3 | **GSM/LTE telematik** | Telefon kontrolü | Tercih: **StarLine LTE Master 4G** (A93 ile uyumlu); pakette dahili GSM varsa LTE tercih et |
| 4 | **nano-SIM** | Ağ bağlantısı | Türkiye operatörü; sadece veri, minimal tarife |
| 5 | **LCD kumanda** | Yakın mesafe yedek | Pakete dahil; günlük ritüelde zorunlu değil |
| 6 | **Servis butonu** | iKey öğrenme, valet, PIN | Pakete dahil |
| 7 | **Siren** | Alarm | Pakete dahil |
| 8 | **Kaput switch (hood pin)** | Kaput açıkken çalıştırmayı engelle | Fabrika switch'e bağlanır veya ek switch |
| 9 | **StarLine Master yazılımı** | Kurulum / firmware / fonksiyon tabloları | PC; kurulumda bir kez |
| 10 | **StarLine 2 uygulaması** | Günlük kullanım | Ücretsiz |

**Olmayacaklar:** Compustar beyin, Fortin EVO-ONE (ayrı), DroneMobile, MyKeyPremium, Blue Link modem.

---

## 5. GSM / SIM — net spec

| Konu | Karar |
|------|-------|
| Modül | **StarLine LTE Master 4G** (2G kapanma riskine karşı; A93 v2 ile resmi uyumlu) |
| SIM formatı | nano-SIM |
| Operatör | Turkcell, Vodafone veya Türk Telekom — **herhangi biri** (StarLine dokümantasyonu operatör bağımsız) |
| Tarife | Aylık düşük veri (komut + durum; GB'a gerek yok) |
| Uygulama | **StarLine** (Android / iOS) |
| Hesap | Kurulumda pin-konvertteki login/şifre ile starline.online / uygulama |
| Aylık maliyet | SIM tarifesi (tek rakam değil; operatöre göre ~düşük GB paketi) |

**Komutlar telefondan:** Çalıştır, Durdur, Güvenlik kur/çöz, Kapı kilitle/aç, Konum (GPS modülü varsa).

---

## 6. Kurulumda programlanacak kritik ayarlar

Kurulumcuya **yazılı** verilecek liste (StarLine Fonksiyon tabloları):

| Fonksiyon | Değer | Neden |
|-----------|-------|-------|
| Şanzıman tipi | **Manuel (МКПП)** | Otomatik seçilirse güvenlik bozulur |
| Fonksiyon 1 (autostart) | Seçenek 2, 3 veya 4 | Uzaktan çalıştırma açık |
| Fonksiyon 12 (kontak desteği) | **El freni** veya **Otomatik** | Push-start ix35; kumanda START gerektirmez |
| Fonksiyon 15 (program nötr bitiş) | **Silahlanma** (telefon/kumanda/SLAVE) | Telefondan "Güvenlik kur" ile biter |
| iKey / immobilizer bypass | Açık | Smart key bypass |
| Motor çalışma süresi | 10–15 dk (max 20) | Yağ seyreltmesi + Prins benzin başlangıcı |
| SLAVE modu | İstenirse açık | Fabrika smart key ile kilit uyumu |
| Turbo timer | **Kapalı** | Benzin 1.6 GDI — gereksiz |

**iKey öğrenme (push-start):** Servis butonu 14× → 5 sn içinde kontak aç → CAN üzerinden öğrenme (CopyKey **gerekmez** — ix35 forum doğrulaması).

**Bağlantı şeması:** [can.starline.ru](https://can.starline.ru) → Hyundai → Tucson / ix35 → 2010–2014 → Start-Stop.

---

## 7. Prins LPG etkisi

| Konu | Sonuç |
|------|-------|
| Ek LPG modülü | **Gerekmez** |
| Uzaktan çalıştırma yakıtı | **Benzin** (Prins VSI her zaman benzinle başlar) |
| Depoda benzin | Uzaktan çalıştırma öncesi benzin olmalı |
| Rölanti LPG'ye geçiş | Motor ısındıktan sonra normal Prins davranışı |

---

## 8. Klima beklentisi (değişmez gerçek)

| Yapılır | Yapılmaz |
|---------|----------|
| Son bırakılan AUTO/sıcaklık ile çalışır | Uygulamadan °C ayarı |
| Park öncesi AUTO + istenen dereceyi ayarla | Blue Link profili |
| İsteğe bağlı: kabin sıcaklık sensörü (StarLine) | Koltuk ısıtma hafızası (soft touch — ayrı aux gerekir) |

---

## 9. Walk-away stratejisi (Faz 2)

| Yol | Açıklama |
|-----|----------|
| **A — StarLine SLAVE + tag** | Fabrika kumanda davranışı korunur; proximity tag ile tanıma |
| **B — TR proximity modülü** | Start-Stop TR / anahtarcı "yaklaş aç uzaklaş kapat" |
| **C — Sadece telefon** | Çıkarken uygulamadan kilitle (walk-away değil ama çalışır) |

**Faz 1'de walk-away zorunlu değil** — uzaktan çalıştırma öncelik.

---

## 10. Satıcıya sorulacak son teyit (sipariş öncesi)

Sipariş vermeden önce TR StarLine bayisine **tek mesaj**:

> "2012 Hyundai ix35, 1.6 benzin+LPG, **manuel**, Smart Key push-start. StarLine **A93 v2 ECO 2CAN+2LIN + LTE Master 4G** paketi uyumlu mu? Program nötr **telefon uygulamasından** silahlanma ile bitecek şekilde ayarlanacak. Montaj dahil mi?"

Beklenen cevap: Evet + ix35 referansı. Hayır ise alternatif bayi.

---

## 11. Riskler ve önlemler

| Risk | Önlem |
|------|-------|
| Yanlış şanzıman profili | Kurulumda manuel seçimi yazılı teyit |
| Program nötr unutma | A prosedürünü her parkta; uygulamada N ikonu kontrol |
| 2G SIM / modül | LTE Master 4G kullan |
| DIY kablo hatası | CAN şemasına harfiyen uy; multimetre ile doğrula |
| Kapalı garaj CO | Asla uzaktan çalıştırma |
| Immobilizer öğrenme başarısız | 14× prosedür + bağlantı kontrolü; max 5 dk bekle |

---

*Son güncelleme: 2026-07-09*
