# Hafta Sonu Kurulum Planı — KESİN KARAR + Adım Adım

> 2012 ix35 · 1.6 GDI · Smart Key · **Manuel** · Prins LPG · Kayseri · **Kendin kur**
> Tarih: 2026-07-09

---

## KESİN KARAR (bundan sonra değişmiyor)

```
┌─────────────────────────────────────────────────────────────┐
│  SİSTEM: StarLine A93 v2 2CAN+2LIN GSM ECO                  │
│  NEDEN:   Evden telefon ✅ · ix35 DIY kanıtı ✅ · 1 hafta sonu │
│  PANDORA: Bu projede YOK — farklı ürün, kurulumu daha zor   │
│  WALK-AWAY: Çıkarken StarLine 2 uygulamasından kilitle      │
│             (30 sn; otomatik proximity bu pakette yok)      │
└─────────────────────────────────────────────────────────────┘
```

### Neden StarLine, neden Pandora değil?

| | StarLine (seçtik) | Pandora (bu projede hayır) |
|--|-------------------|---------------------------|
| Senin 1. hedef: evden telefon | ✅ | ✅ |
| Senin 2. hedef: walk-away | ⚠️ uygulamadan kilitle | ✅ Hands Free |
| **Hafta sonu DIY** | Forumda ix35 kuranlar var | Daha az kaynak, daha çok ayar |
| Şema | can.starline.ru — ix35 2012 Start-Stop | Alarm Studio, daha kapalı |
| Karışıklık | Tek cevap: **bunu al, bunu kur** | İki iş için iyi ama ilk kurulum riski |

**Pandora kötü değil** — yanlış zaman. Önce StarLine’ı kur, telefon + uzaktan marş çalışsın. Walk-away “uzaklaşınca kendi kilitlesin” 6 ay sonra hâlâ canını sıkıyorsa **o zaman** Pandora’ya bakarsın; şimdi iki marka arasında gidip gelmeyi bırakıyoruz.

**Yapamazsın demiyorum.** Bobin, MAP sensörü yapan adam, dikkatli okuyup multimetre kullanırsa **bunu da yapar**. Zor = imkansız değil.

---

## Zor mu? Alet sıkıntısı var mı?

| Soru | Cevap |
|------|-------|
| Çok mu zor? | **Orta-zor.** Motor sökmek yok. 2 gün, acele yok. |
| Özel Hyundai aleti? | **Hayır.** |
| Pahalı ekipman? | **Hayır.** ~500–1.500 TL alet (çoğu zaten var). |
| Laptop? | **Evet** — Windows şart (StarLine Master). |
| İnternet? | Kurulum günü + iKey öğrenme için lazım. |

### Alışveriş listesi (kurulumdan önce)

| # | Alet / malzeme | Nereden | Tahmini |
|---|----------------|---------|---------|
| 1 | **Multimetre** (buzzer ile) | Hırdavat / online | 150–400 TL |
| 2 | **Plastik sökme takımı** (trim) | Oto aksesuar | 80–200 TL |
| 3 | **Tornavida seti** (yıldız + düz) | Var | — |
| 4 | **Kıskaç seti** | Var / hırdavat | 50 TL |
| 5 | **Kablo bağı** (zip tie) | Hırdavat | 30 TL |
| 6 | **İzolasyon bandı** + shrink | Hırdavat | 50 TL |
| 7 | **Butt connector / ek konnektör** | Hırdavat | 50 TL |
| 8 | **Uzatma kablosu + fener** | Var | — |
| 9 | **Laptop (Windows)** | Evde | — |
| 10 | **USB micro kablo** | Genelde kutuda | — |
| 11 | **nano-SIM** (Turkcell/Vodafone/TT) | Kurulum günü | ~50–150 TL/ay |
| 12 | OBD okuyucu (opsiyonel, hata silmek) | Online | 200–500 TL |

**Gerekmez:** kaynak, lift, oscilloscope, Hyundai servis tableti.

---

## Kutuda ne var? (StarLine GSM ECO)

Kutu gelince **eksik parça kontrolü** — kuruluma başlamadan:

| Parça | Ne işe yarar | Neye benziyor |
|-------|--------------|---------------|
| **Ana ünite** (siyah kutu ~10×8 cm) | Beyin | Küçük alarm modülü, çok kablo çıkışı |
| **2CAN+2LIN modülü** | CAN/LIN konuşur | Daha küçük kutu, micro-USB var |
| **GSM anteni** | Telefon bağlantısı | İnce kablo + küçük siyah stick |
| **LCD bröle** | Yakın mesafe kumanda | Ekranlı anahtarlık |
| **İkinci bröle** (yedek) | — | Düğmesiz veya basit |
| **Siren** | Alarm sesi | Küçük hoparlör |
| **Servis düğmesi** (vale) | Programlama | Küçük push buton |
| **Sıcaklık sensörü** | Motor sıcaklığı | İnce kablo + metal baş |
| **Kaput switch** (hood pin) | Kaput açıkken marş yok | Uzun pimli switch |
| **Kablo demeti** | Ana bağlantı | Kalın siyah kablo, X1 X2… konnektörler |

Eksikse satıcıya yaz — kurmaya başlama.

---

## Arabada nereye dokunacaksın? (ix35 — sözlük)

### 1) İç sigorta kutusu

```
NEREDE: Sürücü koltuğu · direksiyonun SOL ALTı · plastik kapak
NASIL AÇILIR: Parmağınla çentikten çek — klips sesi normal
İÇİNDE: Sigortalar + bazı röleler · kapak içinde ŞEMA var (foto çek)
```

**Senin araç için önemli sigortalar** (etiket kapakta yazar):

| Etiket | Amper | Ne besler |
|--------|-------|-----------|
| **SMART KEY** (26) | 10A | Smart key, START/STOP |
| **MODULE 5** (18) | 7.5A | BCM, akıllı anahtar modülü |
| **CLUSTER** (6) | 10A | Gösterge paneli |
| **A/CON** (23) | 7.5A | Klima |

StarLine sürekli güç için genelde **sürekli +12V** (sigorta her zaman canlı) ve **kontak +12V** (anahtar açıkken) arar — şemada hangi pin yazıyorsa onu multimetre ile bul.

### 2) OBD-II soketi

```
NEREDE: Direksiyon altı · sol · trapez 16 pinli SİYAH soket
NE İŞE YARAR: CAN High / CAN Low buradan da okunur
NOT: Bazı kurulumlar gösterge arkası CAN’ı tercih eder — can.starline.ru şemasına uy
```

### 3) Gösterge paneli arkası (CAN — ana bağlantı)

```
NEREDE: Gösterge çerçevesi sökülünce · sol tarafta kablo demetleri
NE YAPACAKSIN: StarLine şemasındaki CAN-H ve CAN-L pinlerine bağlan
DİKKAT: Airbag sarı kablolarına DOKUNMA
```

Rus kaynak (ix35 alarm kurulumu): CAN hattı **sol gösterge konnektörü** demetinde. Renk şemada yazacak — **multimetre ile doğrula.**

### 4) BCM / kick panel (sürücü sol ayak)

```
NEREDE: Sürücü kapısı açık · pedal üstü plastik panel sökülünce
NE VAR: Kalın beyaz konnektörler (24 pin civarı) · güç hatları (ACC, IGN)
PUSH-START İÇİN: "Sile bağlantı" — şemadaki ACC/IGN/START burada veya BCM’de
```

### 5) Fren pedalı switch

```
NEREDE: Fren pedalının ÜSTÜnde · küçük 4 pinli beyaz konnektör
NEDEN: ix35’te fren CAN’da yok — marş için fren basılı sinyali buradan alınır
```

### 6) START/STOP düğmesi

```
NEREDE: Direksiyon sağı · konsol üstü
NASIL: Üst panel dikkatli sökülür · arkada 10 pinli beyaz konnektör
NE ZAMAN: Şema “düğme simülasyonu” diyorsa — 2. gün, dikkatli
```

### 7) Kaput (hood pin)

```
NEREDE: Kaput kenarı · yeni delik veya mevcut nokta
NE: Kutudaki hood switch — kaput açıkken uzaktan marş YASAK (güvenlik)
```

### 8) Ana ünite gizli yeri

```
ÖNERİ: Direksiyon altı · torpido içi · gösterge arkası
KURAL: Su almaz, sallanmaz, OBD’den kolay ulaşılmaz (hırsızlık)
```

---

## Yazılım — kurulumdan ÖNCE (Cuma akşamı)

| Adım | Ne yap | Link |
|------|--------|------|
| 1 | **StarLine Master** indir + kur (Windows) | https://help.starline.ru/slm |
| 2 | **can.starline.ru** aç → Hyundai → ix35 → **2012 → Start-Stop** | https://can.starline.ru |
| 3 | Şemayı PDF indir · **ekran görüntüsü al** · telefona at | Aynı site |
| 4 | **StarLine 2** uygulamasını telefona kur (iOS/Android) | App Store / Play |
| 5 | nano-SIM al · PIN kapat · küçük veri paketi aç | Turkcell / Vodafone |
| 6 | Forum oku (1 saat): ix35 2012 DIY | https://support.starline.ru/communities/10/topics/62980-hyundai-ix35-2012-knopka-start-stop |

**can.starline.ru’da araç kodu:** ix35 2012 Start-Stop için forumda **7382** veya güncel firmware sayfası — kurulum günü siteden **en güncel Ready** sürümü seç.

---

## Hafta sonu takvimi

### CUMA (parça yoksa bile — hazırlık, 2–3 saat)

- [ ] StarLine Master kuruldu
- [ ] can.starline.ru ix35 şeması indirildi
- [ ] Alet listesi tamam
- [ ] Arabada: sigorta kapağını aç/kapa — yerini öğren
- [ ] OBD nerede — bul
- [ ] Trim sökme: sol alt paneli **sadece sök-tak** alıştırma (kablosuz)
- [ ] Foto: sigorta şeması, OBD, pedal switch

### CUMARTESİ — Kablo günü (8–10 saat)

**08:00 — Güvenlik**
```
□ Akü EKSİ kabloyu sök (10 mm anahtar)
□ Sigorta çekme yok — eksiyi sökmek yeter
□ Airbag sarı kablolara dokunma
```

**09:00 — Ana ünite + CAN**
```
□ Ana üniteyi geçici yere sabitle (henüz gizleme)
□ 2CAN modülü micro-USB ile laptop’a · firmware güncelle (StarLine Master)
□ can.starline.ru’dan ix35 Start-Stop firmware yükle
□ Gösterge çerçevesini sök (plastik alet)
□ CAN-H, CAN-L bağla — şemadaki pin (multimetre!)
□ Her bağlantıyı foto + not
```

**12:00 — Güç**
```
□ Sürekli +12V (her zaman canlı hat)
□ Kontak +12V (kontak açıkken)
□ Şasi toprak (temiz metal)
□ Sigorta tap veya şemadaki nokta — multimetre
```

**14:00 — Analog sinyaller**
```
□ Fren pedalı switch (+12V fren basılı)
□ El freni / debriyaj (manuel — şemada varsa)
□ Kaput switch montajı
□ Servis (vale) düğmesi — kolay erişilir yere
```

**17:00 — Güç hatları (push-start immo için)**
```
□ BCM/kick panel aç
□ Şemadaki ACC, IGN1, IGN2, START pinlerini multimetre ile BUL
   · Kontak aç → ölç · START’a bas simülasyonu → ölç
□ Renk uyuşmazsa ŞEMAYA güven, renge değil
□ Bağla · henüz aküyü takma
```

**19:00 — Gün sonu**
```
□ Tüm kablolar sabit (zip tie)
□ Trim GERİ tak — garajda bırak
□ Not defteri: hangi pin nereye gitti
```

### PAZAR — Yazılım + test (6–8 saat)

**09:00 — Akü + programlama**
```
□ Akü eksiyi tak
□ StarLine Master ile bağlan
□ Araç: ix35 · Start-Stop · MANUEL (MKPP) seç
□ iKey öğrenme:
   · 14 kez vale düğmesine bas
   · Kontağı aç (START’a basmadan ACC)
   · İki kısa ötüş = tamam (ix35’te CopyKey gerekmez)
□ Manuel vites güvenlik: programlı nötr / F15 ayarları (kılavuz Tablo 2)
```

**11:00 — İlk marş (BRÖLE ile, uzaktan değil)**
```
□ Kaput kapalı
□ Vites BOŞ · el freni ÇEKİLİ
□ Bröleden marş dene
□ Olursa: durdur · tekrar
□ Olmazsa: hata kodu not · forum / şema kontrol
```

**13:00 — GSM**
```
□ GSM anten tak
□ nano-SIM modüle
□ StarLine Master: APN (operatör otomatik çoğu zaman)
□ StarLine 2 uygulama: araç ekle
□ Evden / mobil veri KAPALI test — sadece WiFi değil, GSM test
```

**15:00 — Uzaktan test protokolü**
```
□ 10× uzaktan marş / durdur (açık alan)
□ Kapı açılınca motor ölüyor mu?
□ Klima: parkta AUTO 24°C açık bırak → uzaktan marş → üfleme var mı?
□ 15 dk limit ayarlı mı?
```

**17:00 — Toparlama**
```
□ Ana üniteyi kalıcı gizle
□ Trim tamam
□ Eşya topla
□ Başarılı marş sayısını yaz (hedef: 10/10)
```

---

## Günlük kullanım — manuel vites ritüeli (her park)

Uzaktan marş **çalışsın** diye her seferinde:

```
1. Vites N (boş)
2. El freni çek
3. Debriyaj bırak
4. Programlı nötr / rezervasyon (bröle veya prosedür — kılavuz)
5. Çık · kilitle
6. Artık telefondan marş OK
```

Atlarsan marş çalışmaz — **bozuk değil, güvenlik.**

Walk-away yok; çıkarken **StarLine 2 → kilitle** (2 saniye).

---

## Takılırsan — panik yok

| Belirti | Muhtemel neden | Ne yap |
|---------|----------------|--------|
| Marş yok, immo lambası | iKey öğrenmedi | 14 vale prosedürünü tekrarla |
| Marş yok, fren hatası | Fren pedalı kablosu | Switch’i multimetre ile kontrol |
| CAN hatası / garip uyarılar | Yanlış CAN pin | Bağlantıyı kes · doğru pini bul |
| GSM yok | SIM / APN | Telefonda SIM çalışıyor mu test et |
| SLAVE ara sıra çalışmıyor | Firmware | can.starline.ru güncel Ready sürüm |

**Geri dönüş:** Akü eksiyi sök · StarLine kablolarını sök · orijinal konnektörler aynı — araç fabrika haline döner.

---

## Pandora ne oldu?

Bu dosyada **yok.** Karar: StarLine. `pandora-arastirma.md` arşiv — ileride belki, şimdi değil.

---

## İlgili dosyalar

| Dosya | İçerik |
|-------|--------|
| [diy-kurulum.md](diy-kurulum.md) | DIY genel |
| [telefon-kontrol-arastirma.md](telefon-kontrol-arastirma.md) | Sipariş + gümrük |
| [teknik-analiz.md](teknik-analiz.md) | Araç mimarisi |
| [pandora-arastirma.md](pandora-arastirma.md) | Arşiv (şimdilik kullanılmıyor) |

---

## Karar kaydı

| Tarih | Karar |
|-------|-------|
| 2026-07-09 | **Kesin sistem: StarLine A93 GSM ECO** |
| 2026-07-09 | Pandora bu proje dışı — walk-away = uygulama kilidi |
| 2026-07-09 | Montajcı yok — hafta sonu DIY planı |
| 2026-07-09 | Alet bariyeri düşük (~500–1500 TL) |

---

*Son güncelleme: 2026-07-09*
