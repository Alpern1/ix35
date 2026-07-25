# Kendin Kur (DIY) — Montajcı Şart mı?

> 2012 ix35 · Smart Key · Manuel · Prins LPG · Kayseri
> Soru: Biz yapabilir miyiz? Montajcıya neden para verelim?
> Son güncelleme: 2026-07-09

---

## 1. Kısa cevap

| Soru | Cevap |
|------|-------|
| **Biz yapabilir miyiz?** | **Evet.** StarLine ve Pandora amatör montaj için tasarlanmış; üretici kılavuzları bunu kabul ediyor. |
| **Bobin/MAP sensörü gibi mi?** | **Hayır, farklı iş.** Motor mekaniği değil; kablo + CAN + yazılım ayarı. Ama senin tecrüben yeterli başlangıç. |
| **Bir şeyi bozar mıyız?** | **Yanlış kablo = risk var** (BCM, airbag hattı). Doğru şema + multimetre ile risk düşük. |
| **Montajcı şart mı?** | **Hayır.** Kayseri’de bulamaman = DIY yapmanın **nedeni**, engeli değil. |
| **Parçayı neden biz alalım?** | Montajcı yoksa veya pahalıysa **sen alırsın, sen kurarsın** — mantıklı. |
| **Hangisi DIY için daha kolay?** | **StarLine** — `can.starline.ru` şeması + ix35 forum kurulumları. Pandora daha zor. |

---

## 2. Senin tecrüben ne işe yarar, ne yaramaz?

### İşine yarayan
- El becerisi, sök-tak cesareti (konsol, torpido, trim)
- Multimetre ile kablo bulma alışkanlığı
- “Önce oku, sonra bağla” disiplini
- MAP sensörü / bobin: elektrik konnektörüyle çalışmışsın — aynı dikkat burada da şart

### Farklı olan (öğrenmen gereken)
| Bobin / MAP | StarLine / Pandora |
|-------------|-------------------|
| Mekanik erişim | Gösterge paneli altı, BCM, OBD civarı |
| Parça çıkar-tak | **Pinout’a göre** kablo bağla |
| Çalışmazsa motor titrer | Çalışmazsa immo/BCM hata verir |
| Alet: anahtar, soket | Alet: multimetre, kıskaç, **laptop**, USB |
| — | **Windows yazılımı** (StarLine Master / Alarm Studio) |
| — | **Manuel vites güvenlik protokolü** (kritik) |

**Sonuç:** Yapamazsın demiyorum. “Motor işi biliyorum, bu da aynı” da demiyorum — **öğrenilebilir elektrik işi**, 2–3 hafta sonu, acele etme.

---

## 3. StarLine A93 GSM ECO — DIY gerçekçi mi?

### Evet — kanıt: StarLine forumda ix35 DIY kurulumları var

Resmi forum başlığı: *“Starline A93 2CAN+2LIN на Hyundai tucson ix35 2014 Start-Stop / **Самостоятельная установка**”*

- Kullanıcı: *“Сервис свою машину я не отдам”* (arabamı servise vermem)
- Elektronik tecrübesi var, **kendi kurmuş**, fotoğraflı rapor paylaşmış
- ix35 için `can.starline.ru` şeması kullanmış
- iKey: **ix35’te CopyKey gerekmez** — 14 vale + kontak aç, iki bip = öğrenildi

Kaynak: https://support.starline.ru/communities/10/topics/41978-starline-a93-2can2lin-na-hyundai-tucson-ix35-2014-start-stop

2012 ix35 “sile bağlantı” (güç hatları) için de ayrı DIY başlığı var — biri *“схема работает 100%”* demiş.

Kaynak: https://support.starline.ru/communities/10/topics/24327-ix35-2012g-podklyuchenie-po-sile

### Ne yapacaksın (özet)

```
HAZIRLIK (evde, araç kapalı)
  ├─ StarLine Master indir (ücretsiz)
  ├─ can.starline.ru → Hyundai ix35 2012 Start-Stop şemasını aç
  ├─ CAN modül firmware güncelle (USB)
  └─ Kılavuzu baştan sona oku

ARAÇTA — 1. gün (söküm + CAN)
  ├─ Akü eksi sök (güvenlik)
  ├─ Gösterge / direksiyon altı trim sök
  ├─ CAN hattına bağlan (şemadaki pinler)
  ├─ Güç: +12 sürekli, +12 kontak, şasi
  └─ Multimetre ile her pini doğrula (renk şemada farklı çıkabilir!)

ARAÇTA — 2. gün (güç + immo)
  ├─ BCM’de ACC / IGN / START hatları (ix35 push-start için “sile” bağlantı şart)
  ├─ iKey öğrenme (14 vale prosedürü)
  ├─ Manuel vites: F15 / programlı nötr ayarı
  └─ Hood pin (kaput switch)

ARAÇTA — 3. gün (test)
  ├─ Önce kablolu bröle ile marş dene
  ├─ Sonra uzaktan marş
  ├─ Manuel güvenlik: vites boş, el freni, debriyaj testleri
  ├─ GSM modül + Türk SIM + StarLine 2 uygulama
  └─ Klima AUTO test (park ayarıyla)

SÜRE: Deneyimli DIY → 12–20 saat (2–3 hafta sonu)
```

### İx35’e özel kritik notlar (forumdan)

1. **Sadece CAN ile yetmez** — immo bypass için **güç hatlarına** (ACC, IGN1, IGN2, START) bağlanman gerekiyor.
2. **Kablo renkleri** şemadan farklı olabilir → **multimetre ile doğrula**, renge güvenme.
3. **Manuel vites** → her park sonrası programlı nötr / rezervasyon prosedürü; atlamanın bedeli ağır.
4. **Prins LPG** → ECU’ya dokunma; sistem benzinle marş yapar, Prins kendi geçer.
5. **Airbag / direksiyon hattına dokunma** — şemada olmayan yere kablo sokma.

### Ne bozulabilir (dürüst liste)

| Hata | Sonuç | Geri dönüş |
|------|-------|------------|
| Yanlış BCM pini | Sigorta atar, fonksiyon kaybı | Sigorta değişir, kablo düzelt |
| Airbag hattı | **Tehlikeli** — yapma | — |
| iKey yanlış öğrenme | Marş yok, immo hatası | Prosedürü tekrarla |
| Manuel güvenlik atlanırsa | Vitesteyken marş riski | **En tehlikeli** — ayarı doğru yap |
| Firmware yanlış | SLAVE/marş çalışmaz | Doğru ix35 firmware yükle |

**Kalıcı “araç çöp” riski düşük** — modül sökülür, orijinal kablolama geri alınır. Ama immo/BCM uğraştırır; acele etme.

---

## 4. Pandora VX-4G — DIY?

**Yapılabilir ama StarLine’dan zor.**

| | StarLine DIY | Pandora DIY |
|--|-------------|-------------|
| Şema sitesi | can.starline.ru (ix35 var) | Alarm Studio içinde |
| ix35 forum | Çok | Az |
| iOS/Android kurulum sonrası | StarLine 2 | Pandora Connect |
| CLONE | iKey (daha basit ix35’te) | İnternet + Alarm Studio |
| Hands Free ayarı | — | Ek uğraş (BT uygulaması) |
| Türkçe kaynak | Az ama ix35 İngilizce/Rusça forum var | Çok az |

**Öneri:** İki işi tek kutuda istiyorsan Pandora mantıklı ürün — ama **ilk kez DIY yapıyorsan StarLine ile başla**, Pandora’yı ikinci araç / deneyim sonrası düşün.

---

## 5. Montajcı meselesi — senin durumun

```
Kayseri’de Pandora/StarLine ix35 push-start + manuel bilen montajcı: nadir
Montaj ücreti (İstanbul referans): 5.000–15.000 TL
Senin bütçe: montajcıya yetmiyor

→ Sonuç: Parçayı sen al, sen kur. Montajcı satırını plandan çıkar.
```

**“Adam zaten alır takar”** — ancak adam varsa ve fiyatı kabul edilebilirse geçerli. Kayseri + bütçe = **adam yok, o zaman DIY planın doğru.**

Tasarruf: **~5.000–15.000 TL** işçilik (kendi zamanın hariç).

---

## 6. Gerekli araç / malzeme listesi

| Araç | Zorunlu mu? |
|------|-------------|
| Multimetre | **Evet** |
| Laptop (Windows) | **Evet** |
| USB (micro) StarLine CAN programlama | **Evet** |
| Torx / trim sökme seti | Evet |
| Lehim / ekleme konnektörleri (T-tap yerine ek konnektör tercih) | Evet |
| Sigorta maşası | Evet |
| Uzatma lambası | İyi olur |
| OBD-II okuyucu (hata silmek için) | Önerilir |
| Tork anahtarı | Trim için |

**Gerekmez:** Kaynak makinesi, motor lifti, özel Hyundai servis cihazı.

---

## 7. DIY faz planı (montajcısız)

```
FAZ 0 — Öğren (0 TL, araç dokunulmaz)
  · can.starline.ru ix35 şemasını indir/oku
  · StarLine forum ix35 DIY başlıklarını oku (linkler aşağıda)
  · StarLine Master’ı kur, demo modda gez
  · YouTube: "StarLine A93 CAN installation" (genel mantık)

FAZ 1 — Parça gelince (masada)
  · Kutu içeriği kontrol
  · Firmware güncelle (CAN modül + ana ünite)
  · ix35 Start-Stop + Manuel firmware seç

FAZ 2 — Araçta kablolama (akü ekside)
  · CAN + güç + hood pin
  · BCM güç hatları (multimetre!)
  · Hiçbir şeyi test etmeden trim geri takma

FAZ 3 — Programlama
  · iKey öğren
  · Manuel F15
  · GSM SIM

FAZ 4 — Test (açık alan, el freni, vites boş)
  · 10+ başarılı marş/durdurma
  · Kapı açılınca motor ölüyor mu?
  · Uzaktan klima testi

FAZ 5 — Günlük kullanım
  · Park prosedürünü alışkanlık yap (manuel!)
```

---

## 8. StarLine mi Pandora mı — DIY gözlüğüyle

| Hedef | DIY öneri |
|-------|-----------|
| Evden telefon, walk-away ikincil | **StarLine GSM ECO** — kurulumu kolay |
| Telefon + walk-away tek kutu | **Pandora VX-4G v3** — ürün doğru, kurulum zor |
| İlk kez bu iş | **StarLine** |
| İkinci deneme / Pandora alışkınlığı | Pandora |

Walk-away için StarLine’da Hands Free yok — çıkarken telefondan kilitle veya alışkanlık. İkisi de şartsa Pandora ama DIY eğrisi dik.

---

## 9. Forum / kaynak linkleri (DIY)

| Konu | URL |
|------|-----|
| ix35 2014 DIY kurulum (fotoğraflı) | https://support.starline.ru/communities/10/topics/41978-starline-a93-2can2lin-na-hyundai-tucson-ix35-2014-start-stop |
| ix35 2012 güç bağlantısı | https://support.starline.ru/communities/10/topics/24327-ix35-2012g-podklyuchenie-po-sile |
| ix35 2015 start-stop güç | https://support.starline.ru/communities/10/topics/17733-hyundai-ix35-2015-start-stop-podklyuchit-po-sile |
| CAN şemaları | https://can.starline.ru |
| StarLine Master | https://help.starline.ru/slm |
| Teknik analiz (repo) | [teknik-analiz.md](teknik-analiz.md) |
| Pandora detay | [pandora-arastirma.md](pandora-arastirma.md) |

---

## 10. Karar kaydı

| Tarih | Karar |
|-------|-------|
| 2026-07-09 | Montajcı **zorunlu değil** — Kayseri + bütçe nedeniyle DIY ana yol |
| 2026-07-09 | Bobin/MAP tecrübesi **yeterli başlangıç**, CAN+yazılım öğrenilecek |
| 2026-07-09 | DIY için **StarLine öncelik**; Pandora ikinci seçenek |
| 2026-07-09 | Parçayı kullanıcı alır — montajcı yoksa mantıklı |

---

*Son güncelleme: 2026-07-09*
