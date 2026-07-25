# Parça Tedarik — Türkiye (Yurtiçi, 2026-07-09)

> 2012 Hyundai ix35 · Smart Key · Manuel · Prins LPG
> **Amaç:** Gümrüksüz, Türkiye'den online sipariş verilebilir parçaları SKU ve link ile netleştirmek.
> Fiyat yok — sadece **ne alınır**, **nereden**, **stok**, **ne işe yarar**, **ne eksik kalır**.

---

## 0. Telefon kontrolü (evden GSM) — güncel araştırma

**Evden telefon şartsa:** yurtiçinde kanıtlı SKU **yok**. Detaylı fiyat + gümrük hesabı:

→ **[telefon-kontrol-arastirma.md](telefon-kontrol-arastirma.md)**

Özet: StarLine A93 GSM ECO ithalat ~12.100 TL ürün + ~9.000–14.000 TL kargo/gümrük/müşavir ≈ **~22.000–26.000 TL toplam**.

---

## 1. Dürüst özet (önce bunu oku)

Önceki plan **StarLine A93** üzerine kuruluydu. StarLine teknik olarak ix35'e uyuyor; fakat **Türkiye'de doğrudan satan güvenilir e-ticaret sitesi yok** — Rusya/ukrayna kargo + gümrük gerekir. **Yurtdışından alamayız** kısıtıyla StarLine **şu an satın alınamaz**.

Yurtiçinde araştırınca tablo şöyle:

| İhtiyaç | StarLine (ithalat) | Fortin MK3 | Start-Stop TR |
|---------|-------------------|------------|---------------|
| ix35 push-start + immo bypass | ✅ kanıtlı | ✅ guide #23691 | ⚠️ model teyidi yok |
| Manuel program nötr | ✅ telefonla (F15) | ⚠️ Ready Mode — çoğunlukla kumanda/OEM | ⚠️ farklı protokol |
| **Evden telefonla çalıştırma** | ✅ LTE + StarLine 2 | ❌ **TR'de GSM telematik yok** | ❌ sadece BT ~50 m |
| Walk-away kilit | ⚙️ ayrı faz | ❌ ayrı modül | ✅ pakette |
| Yurtiçi online sipariş | ❌ gümrük | ✅ mk3.com.tr | ✅ fsatuning.com |

**Sonuç:** Evden telefon + yurtiçi satın alma + ix35 push-start üçünü **aynı anda** karşılayan tek paket **yok**.

İki gerçek yol:

1. **Öncelik evden telefon ise** → StarLine (ithalat) veya Fortin EVO-START LTE (ithalat + Kuzey Amerika ağı — TR'de çalışması belirsiz).
2. **Öncelik yurtiçi parça ise** → Fortin EVO-ONE paketi (MK3) — uzaktan çalıştırma **RF kumanda** veya **OEM 3× kilit** menzilinde; evden telefon **bu listede yok**.

Bu dosya **yol 2'nin** sipariş listesidir. StarLine ithalat yolunu [satin-alma-kanallari.md](satin-alma-kanallari.md) içinde “Plan B (gümrük)” olarak tutuyoruz.

---

## 2. Önerilen yurtiçi paket — Fortin EVO-ONE (MK3)

Fortin resmi kılavuz: Hyundai Tucson **Smart-Key Push-Start 2010–2013** → ix35 (LM = Tucson) ile aynı platform.

- Kılavuz PDF: https://fortin.ca/download/23691/EVO-ONE_IG_REG_BI_HYU-Tucson_2010-2013_PTS_B_23691.pdf
- Push-start için plug-and-play T-harness **her zaman yok**; kılavuzda wire-to-wire noktaları var. T-harness kurulumu kolaylaştırır ama **Flashlink ile araç doğrulaması şart**.

### 2.1 Zorunlu parçalar (BOM)

| # | Parça | Stok kodu | Satıcı | URL | Stok (09.07.2026) | Görev |
|---|-------|-----------|--------|-----|-------------------|-------|
| 1 | **Fortin EVO-ONE** (bypass + remote start + alarm) | MK20064 | MK3 | https://www.mk3.com.tr/urun/fortin-evo-one-uzaktan-araba-calistirm-guvenlik-sistemi-ve-bilgi-data-modulu | ✅ Satışta | Ana beyin; immobilizer bypass, START/STOP simülasyonu |
| 2 | **Flashlink Mobile** (BT programlama) | MK20126 | MK3 | https://www.mk3.com.tr/urun/fortin-flashlink-mobile-bluetooth-yazilimi-guncelleme-modulu-ios-ve-android-platformlari-icin | ✅ Satışta | ix35 firmware yükleme; iOS/Android Flashlink uygulaması |
| 3 | **T-Harness** Hyundai/Kia push-start | MK20139 (KHY3) **veya** MK20141 (KHY7) | MK3 | KHY3: https://www.mk3.com.tr/urun/fortin-thar-one-khy3-t-harness-hyundai-kia-start-stoplu-araclar-icin · KHY7: https://www.mk3.com.tr/urun/fortin-thar-one-khy7-t-harness-hyundai-kia-start-stoplu-araclar-icin | ✅ Satışta | OEM konnektör — **hangisi olduğunu Flashlink araç sihirbazıyla doğrula** |
| 4 | **RFK442** 2 yönlü RF kit (2×4 buton kumanda) | MK20083 | MK3 | https://www.mk3.com.tr/urun/fortin-evo-4-series-rfk442-2-adet-4-butonlu-uzaktan-kumandali-2-yonlu-rf-kiti | ✅ Satışta | Uzaktan çalıştırma menzili (~yüzlerce m; bina/RF'e bağlı) |
| 5 | **Kaput switch** | — | Pakette | EVO-ONE kutusunda | ✅ Dahil | Kaput açıkken uzaktan çalışmayı engeller |
| 6 | **Uyarı etiketi** | — | Pakette | EVO-ONE kutusunda | ✅ Dahil | Yasal/zorunlu etiket |

### 2.2 Programlama alternatifi (USB)

| Parça | Stok kodu | URL | Stok | Not |
|-------|-----------|-----|------|-----|
| Flashlink 4 (USB) | MK20125 | https://www.mk3.com.tr/urun/fortin-flashlink-4-baypas-modulu-firmware-guncelleme-ve-bootloader-usb-flash-baglantisi | ❌ **TÜKENDİ** | PC + Flashlink Manager; Mobile yoksa gerekli |

**Karar:** Flashlink Mobile (MK20126) al — USB sürümü MK3'te tükenmiş.

### 2.3 ALMA — yanıltıcı / işe yaramaz

| Ürün | Stok kodu | Neden alma |
|------|-----------|------------|
| EVO-ONE + “ücretsiz GPS” paketi | MKON355 | ❌ **TÜKENDİ** — ve hediye **CCURA** cihazı sadece **GPS takip** (12gps.net); **uzaktan marş komutu yok** |
| EVO-ALL tek başına | MK20066 | RF kit ve telematik ayrı; EVO-ONE daha uygun |
| RF olmadan sadece EVO-ONE | — | OEM 3× kilit ile çalışabilir ama menzil fabrika kumandası kadar; pratikte RF şart |

### 2.4 Evden telefon için eksik parça (yurtiçi yok)

| Parça | Durum |
|-------|-------|
| **Fortin EVO-START LTE** | MK3'te **listelenmiyor**; Fortin resmi: ağ kapsamı **Kuzey Amerika** — TR SIM ile çalışacağı kanıtlanmamış |
| **StarLine LTE Master** | Sadece ithalat — [satin-alma-kanallari.md](satin-alma-kanallari.md) Plan B |
| **CCURA / 12gps.net** | Konum takibi; motor çalıştırma değil |

---

## 3. Alternatif yurtiçi paket — Start-Stop Türkiye

Walk-away ve anahtarsız giriş isteyenler için; **evden telefon hedefiyle uyumsuz**.

| # | Parça | Kod | Satıcı | URL | Stok | Görev |
|---|-------|-----|--------|-----|------|-------|
| 1 | SST tam paket (anahtarsız + RF uzaktan) | SST-019 | FSA Tuning | https://fsatuning.com/urun/start-stop-turkiye-anahtarsiz-giris-anahtarsiz-calistirma-uzaktan-calistirma-sistemi-sst-019/ | ✅ | RF menzil 50–70 m; walk-away ~1,5 m |
| 2 | Bluetooth telefon modülü (ek) | — | FSA Tuning | https://fsatuning.com/urun/start-stop-kiti-telefon-kontrol-sistemi-bluetooth-modulu/ | ✅ | **Bluetooth menzil** — evden değil, araç yanı |

**Eksi:** 2012 ix35 push-start + manuel + Prins için **model uyumu site üzerinde doğrulanmıyor** — sipariş öncesi satıcıya “2012 ix35 1.6 GDI manuel smart key” yazılı sorulmalı (bayi ziyareti değil; e-posta/WhatsApp yeter).

**Artı:** Türkiye'de kurulum ağı var (startstopturkiye.com).

---

## 4. Elendi — yurtiçi ama hedefe uymuyor

| Seçenek | Neden |
|---------|-------|
| **Oto Yapay Zeka** | Fabrika start-stop'lara önerilmez; iPhone desteği zayıf/yok; paket farklı segment |
| **Durer / generic Çin kit** | ix35 CAN/iKey kanıtı yok |
| **MyKeyPremium** | Manuel vites uyumsuz |
| **Pandora TR mağaza** | Doğrulanabilir .tr e-ticaret bulunamadı |
| **Blue Link** | 2012'de donanım yok |

---

## 5. StarLine — teknik referans, satın alma Plan B (gümrük)

ix35 uyumu kanıtlı; **yurtiçi satın alma yok**. Gümrük kabul edilirse:

| Parça | Nereden |
|-------|---------|
| A93 v2 ECO 2CAN+2LIN | store.starline.ru / alarmstarline.com |
| LTE Master 4G | store.starline.ru |
| nano-SIM | Türkiye operatör |

Detay: [satin-alma-kanallari.md](satin-alma-kanallari.md) — **Plan B** bölümü.

**Gümrük notu:** Rusya/ABD/Kanada'dan elektronik → gümrük vergisi + KDV + gümrük müşavirliği maliyeti; süre 2–6 hafta değişken. Bu maliyet StarLine'ı “ucuz paket” olmaktan çıkarır — kısıtın nedeni bu.

---

## 6. Sipariş öncesi kontrol listesi (Fortin yolu)

Sipariş vermeden önce:

```
□ Flashlink Mobile veya Flashlink 4 elinde / siparişte
□ EVO-ONE (MK20064) — MKON355 DEĞİL (GPS hediyesi marş yapmaz)
□ T-harness: Flashlink uygulamasında 2012 ix35/Tucson PTS seç → KHY3 mü KHY7 mi yazıyor
□ RFK442 veya en azından OEM 3× lock ile yetinirim kararı
□ Hood pin pakette — ek alma
□ nano-SIM: Fortin RF yolunda GEREKMEZ (sadece ithalat telematik için)
□ Manuel vites: EVO-ONE üzerindeki güvenlik loop'u KESME (manuel için fabrika ayarı)
```

Kutu açılınca:

```
□ EVO-ONE modül
□ 20-pin + 6-pin + CAN harness
□ Hood pin switch
□ Uyarı etiketi
□ Flashlink Mobile kutusu ayrı geldi
□ RFK442: 2 kumanda + anten
```

---

## 7. Karar ağacı

```
Evden telefon ŞART mı?
├─ EVET + gümrük OK → StarLine Plan B (satin-alma-kanallari.md)
├─ EVET + gümrük YOK → Şu an satın alınabilir parça YOK (dürüst cevap)
└─ HAYIR / RF menzil yeter → Fortin BOM (Bölüm 2) — MK3'ten sipariş

Walk-away öncelik mi?
├─ EVET + telefon ikincil → Start-Stop TR (Bölüm 3) — model teyidi şart
└─ HAYIR → Fortin veya StarLine
```

---

## 8. İlk gerçek iş adımı (Faz 1)

1. Bu dosyadaki **karar ağacını** uygula — evden telefon için gümrük kabul ediyor musun?
2. **Hayır** ise → MK3'ten Bölüm 2 BOM'u sipariş et (MKON355 alma).
3. **Evet** ise → StarLine Plan B kanalını seç; Fortin BOM'u ertele.
4. Flashlink Mobile gelince → uygulamada **2012 Tucson/ix35 PTS** seç → doğru T-harness SKU'sunu teyit et → sonra T-harness sipariş et (yanlış harness para kaybı).

---

## 9. Hızlı linkler

| Kaynak | URL |
|--------|-----|
| MK3 Fortin kategori | https://www.mk3.com.tr/kategori/fortin-uzaktan-calistirma |
| Fortin ix35/Tucson PTS kılavuz | https://fortin.ca/download/23691/EVO-ONE_IG_REG_BI_HYU-Tucson_2010-2013_PTS_B_23691.pdf |
| Start-Stop TR mağaza | https://fsatuning.com/magaza/ |
| StarLine ix35 şema (ithalat yolu) | https://can.starline.ru |

---

*Son güncelleme: 2026-07-09 — mk3.com.tr ve fsatuning.com canlı stok kontrolü*
