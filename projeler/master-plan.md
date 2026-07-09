# Master Uygulama Planı — Adım Adım

> Hedef: 2012 ix35'te **telefondan uzaktan çalıştırma + klima**; isteğe bağlı **walk-away kilit**.
> İlke: Her faz **tek başına tamamlanabilir**; bir faz bitmeden sonrakine geçme.
> Referans mimari: [sistem-mimarisi.md](sistem-mimarisi.md)

---

## Genel bakış

```
Faz 0 ──► Faz 1 ──► Faz 2 ──► Faz 3 ──► Faz 4 ──► Faz 5 ──► Faz 6 ──► [Faz 7]
Bilgi      Satıcı     Parça      SIM +      Montaj     Yazılım    Kullanım   Walk-away
hazırlık   teyidi     sipariş    hesap      & kablo    & iKey     testleri   (opsiyonel)
  │          │          │          │          │          │          │
  └──────────┴──────────┴──────────┴──────────┴──────────┴──────────┘
                    Her fazda "bitti" kutusu işaretlenir
```

**Toplam zorluk:** Orta–zor (CAN bus + push-start; ama ix35 için hazır şema var).
**DIY seviyesi:** Elektronik okuma + sabır varsa montaj DIY mümkün; iKey öğrenme ve fonksiyon tabloları için kurulumcu desteği veya StarLine forum/yetkili önerilir.

---

## Faz 0 — Bilgi hazırlığı (şu an)

**Amaç:** Ne yapacağını bilerek masaya otur.

| # | Görev | Çıktı | Durum |
|---|-------|-------|-------|
| 0.1 | Araç özelliklerini doğrula | [araba/ozellikler.md](../araba/ozellikler.md) | ✅ |
| 0.2 | Sistem mimarisini kilitle | [sistem-mimarisi.md](sistem-mimarisi.md) | ✅ |
| 0.3 | Günlük ritüeli öğren (telefon-only) | [kullanim-senaryolari.md](kullanim-senaryolari.md) | ✅ |
| 0.4 | Klima beklentisini kabullen | Son ayar stratejisi; °C uygulaması yok | ✅ |

**Faz 0 bitti kriteri:** "Hangi paketi alacağım ve her gün ne yapacağım?" sorusuna cevap verebiliyorsun.

---

## Faz 1 — Satıcı teyidi (1 telefon / WhatsApp)

**Amaç:** Paraya geçmeden uyumluluğu kilitle.

**Yapılacak:** TR'de StarLine veya alarm satan en az **2 bayiye** aynı metni gönder ([sistem-mimarisi.md §10](sistem-mimarisi.md#10-satıcıya-sorulacak-son-teyit-sipariş-öncesi)).

**Alınacak cevaplar:**

| Soru | Beklenen |
|------|----------|
| A93 v2 2CAN+2LIN + LTE ix35 2012 manuel? | Evet |
| Push-start / smart key? | Evet, iKey |
| Telefondan program nötr (silahlanma)? | Evet |
| Montaj süresi? | ~4–8 saat (bayiye göre) |
| Garanti? | Yazılı |

**Faz 1 bitti kriteri:** En az bir bayi "evet, bu paketi kurduk / kurarız" dedi + fiyat teklifi (fiyat konuşmak zorunda değilsin ama sipariş için lazım).

**Tıkanırsan:** İkinci bayi; StarLine Türkiye distribütör listesi veya ix35 forum referansı göster.

---

## Faz 2 — Parça siparişi

**Amaç:** Kutunun içeriği tam gelsin.

### Sipariş listesi (minimum)

```
□ StarLine A93 v2 ECO 2CAN+2LIN (autostart açık paket)
□ StarLine LTE Master 4G  (pakette yoksa veya 2G yerine)
□ Montaj tüketimi: kablo bağı, korumalı bant, korugan (montajcı sağlarsa atla)
□ FlashLink DEĞİL — StarLine Master yazılımı kullanılır
```

### Kutu açılış kontrolü

| Parça | Var mı? |
|-------|---------|
| Ana alarm ünitesi | □ |
| 2CAN+2LIN modülü | □ |
| LCD kumanda | □ |
| LTE/GSM modülü | □ |
| Servis butonu | □ |
| Siren | □ |
| Pin-konvert (login, şifre, servis kodu) | □ |
| Montaj kılavuzu | □ |

**Faz 2 bitti kriteri:** Tüm parçalar fiziksel olarak elinde.

---

## Faz 3 — SIM ve telefon hesabı

**Amaç:** Ağ ve uygulama hazır olsun; montaj günü sadece araca odaklan.

| # | Adım | Detay |
|---|------|-------|
| 3.1 | nano-SIM al | Mevcut hat veya yeni hat; **veri açık**, ses şart değil |
| 3.2 | SIM'i LTE modüle tak | Montajcı da yapabilir; PIN kilidini kapat veya not al |
| 3.3 | StarLine 2 uygulamasını yükle | App Store / Google Play |
| 3.4 | Pin-konvert bilgilerini sakla | Login, şifre, servis kodu — güvenli yere |
| 3.5 | (Montaj sonrası) Hesap bağla | Kurulumcu veya StarLine Master ile aktivasyon |

**Faz 3 bitti kriteri:** SIM çalışıyor (montajcı test eder); uygulama telefonda yüklü.

---

## Faz 4 — Fiziksel montaj

**Amaç:** Kutular araca, teller doğru yere.

**Zorluk:** Bu fazın en yoğun kısmı. DIY yapacaksan StarLine ix35 forum konusunu ([support.starline.ru ix35 2014](https://support.starline.ru/communities/10/topics/41978-starline-a93-2can2lin-na-hyundai-tucson-ix35-2014-start-stop)) ve [can.starline.ru](https://can.starline.ru) şemasını takip et.

### Montaj sırası (mantıksal)

```
1. Akü çıkar (negatif) — iş bitene kadar
2. Ana üniteyi sakin yere monte et (torpido arkası / direksiyon altı)
3. 2CAN+2LIN modülünü şemaya göre CAN/LIN noktalarına bağla
4. LTE modülünü ana üniteye tak; antenleri yerleştir (cam üstü / gövde)
5. Servis butonunu sürücü erişimine monte et
6. Sireni motor odasına
7. Kaput switch'ini doğrula (fabrika veya ek)
8. START/STOP, el freni, kapı, debriyaj — şemada işaretli noktalar
9. Aküyü bağla
```

### Dokunulacak bölgeler (ix35)

| Bölge | İş |
|-------|-----|
| OBD-II / kick panel | CAN tap |
| START/STOP düğmesi konnektörü | Push-start simülasyonu |
| El freni / debriyaj switch | Manuel güvenlik |
| Smart key anten bölgesi | iKey öğrenme |

**Faz 4 bitti kriteri:** Tüm bağlantılar şemada; kısa devre yok; akü bağlı; ünite açılıyor (LED/self-test).

**Usta mı DIY mi?**

| DIY | Usta |
|-----|------|
| Elektronik okuma rahat | Konsol sökümü ilk kez |
| StarLine forumda soru sorabilirsin | Garanti + sorumluluk usta |
| Maliyet düşük | 4–8 saat işçilik |

---

## Faz 5 — Yazılım, iKey ve fonksiyon ayarları

**Amaç:** Araç "tanısın" ve manuel + telefon prosedürü çalışsın.

| # | Adım | Kim |
|---|------|-----|
| 5.1 | StarLine Master ile firmware güncelle | Sen / montajcı |
| 5.2 | can.starline.ru'dan ix35 firmware yükle | Sen / montajcı |
| 5.3 | Fonksiyon tabloları — [sistem-mimarisi §6](sistem-mimarisi.md#6-kurulumda-programlanacak-kritik-ayarlar) | Montajcı |
| 5.4 | iKey öğrenme: 14× servis butonu + kontak | Şemaya göre |
| 5.5 | Program nötr testi: motor çalışırken in → telefondan silahlan | Sen |
| 5.6 | Uzaktan çalıştırma testi: 3 m mesafeden | Sen |
| 5.7 | GSM testi: evden / farklı şebekeden telefonla çalıştır | Sen |

**Faz 5 bitti kriteri:**

- [ ] Telefondan silahlanınca motor duruyor, uygulamada **N** görünüyor
- [ ] Telefondan çalıştırınca motor çalışıyor, klima devrede
- [ ] Kaput açıkken çalışmıyor
- [ ] El freni çekili değilken çalışmıyor

---

## Faz 6 — Kullanım alışkanlığı ve sınır testleri

**Amaç:** Günlük hayata geç; sürpriz kalmasın.

### İlk hafta checklist

| Gün | Test |
|-----|------|
| 1 | Tam A prosedürü + sabah telefonla çalıştır |
| 2 | Binme: frene bas → START/STOP devral → sür |
| 3 | Program nötr iptali: silahlandıktan sonra kapı aç → tekrar A |
| 4 | Normal park (START/STOP ile kapat) → uzaktan çalışmamalı |
| 5 | 15 dk rölanti üst sınır gözlem |
| 6 | Prins: benzinle başladığını doğrula |
| 7 | Kış senaryosu: park öncesi AUTO + sıcaklık ayarla |

### Kalıcı kurallar

- Uzaktan çalıştırma gecesi: **A prosedürü** (telefon silahlanma)
- Kapalı garaj: **asla**
- Rölanti: **10–15 dk**, max **20 dk**
- Depoda **benzin** olsun

**Faz 6 bitti kriteri:** 1 hafta sorunsuz günlük kullanım; `araba/yapilanlar.md` güncellendi.

---

## Faz 7 — Walk-away otomatik kilit (opsiyonel, sonra)

**Amaç:** Kumandaya basmadan uzaklaşınca kilit.

**Ön koşul:** Faz 6 tamam.

| Yol | İş |
|-----|-----|
| StarLine SLAVE + tag ayarı | Mevcut sisteme yazılım/küçük ekleme |
| TR proximity modülü | Anahtarcı; smart key CAN |

Detay: [uzaklasinca-otomatik-kilit.md](uzaklasinca-otomatik-kilit.md)

**Faz 7 bitti kriteri:** 1,5–2 m uzaklaşınca kilit; yaklaşınca açılma.

---

## Pes etmemek için kurallar

1. **Tek faz** — "her şeyi bir anda" yok.
2. **Faz 1'de durmak serbest** — satıcı hayır derse para harcanmadı.
3. **Montajı bölmek OK** — önce kablo, sonra yazılım günü.
4. **Forum / bayi desteği** — ix35 StarLine konusu mevcut; yalnız değilsin.
5. **İlk hedef:** Telefondan çalıştırma. Walk-away sonra.

---

## Hızlı referans — günlük akış

```
Park → N + el freni → motor AÇIK → in → kapı kapat
     → TELEFON: Güvenlik kur → motor durur (N hazır)
Sabah → TELEFON: Çalıştır → 10–15 dk → bin → fren → START/STOP → sür
```

---

## İlgili dosyalar

| Dosya | İçerik |
|-------|--------|
| [sistem-mimarisi.md](sistem-mimarisi.md) | Parçalar, GSM, kurulum ayarları |
| [kullanim-senaryolari.md](kullanim-senaryolari.md) | İnme/binme detayı |
| [zorunlu-parcalar.md](zorunlu-parcalar.md) | Parça özet tablosu |
| [teknik-analiz.md](teknik-analiz.md) | Derin teknik arka plan |
| [uzaktan-calisma-ve-klima.md](uzaktan-calisma-ve-klima.md) | Klima & motivasyon |

---

*Son güncelleme: 2026-07-09*
