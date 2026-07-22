# Hafta sonu fikirleri — detaylı anlatım

> Amaç: Hafta sonu vakit geçir, bitsin, **her gün kullanasın**.  
> Araç: 2012 ix35 · DIY · Kayseri · LPG Prins · Smart Key  
> 2026-07-22

Kısa liste: **dashcam · bagaj düzen · kapı yalıtımı · USB-C PD** (+ **akü bakım prizi / voltmetre** ne alaka).

---

# 1) Dashcam (ön + arka) — sabit tesisat

## Nedir?

Aracın ön camına (ve tercihen arkaya) sürekli kayıt yapan kamera.  
**Sabit tesisat** = çakmaklık adaptörüyle değil; sigorta kutusundan çekilen kablo ile sürekli/ACC’li besleme.

## Ne işe yarar?

| Durum | Fayda |
|-------|--------|
| Trafik kazası | Kimin hatalı olduğu netleşir |
| Parkta çizik / ayna kırığı | “Kim vurdu” kaydı (park modu varsa) |
| Sigorta / savcılık | Kanıt |
| Garip olay | Yol kenarı tartışma, kırmızı ışık vs. |

ix35’te Blue Link / fabrika kamera yok (veya zayıf) → bu boşluğu doldurur.

## Nasıl olur? (DIY)

```
1. Cihaz seç: ön + arka, mümkünse “park mode” (akü korumalı)
2. Sigorta kutusundan Add-A-Circuit ile:
   - Sarı: sürekli +12V (park kaydı)
   - Kırmızı: ACC (kontak açıkken)
   - Siyah: şasi
3. Kabloyu A sütunu / tavan kenarı trimlerinin altından gizle
4. Arka kamera: bagaja kablo (sol veya sağ eşik altı)
5. Kamerayı dikiz arkasına / cam üstüne gizle (görüşü kesme)
```

**Hafta sonu:** Cumartesi ön + kablo; Pazar arka.  
**Maliyet:** ~3–8k TL (70mai, Viofo, 70mai benzeri sınıf).  
**Dikkat:** Park modu aküyü yer — düşük voltaj kesmeli model al (aşağıdaki voltmetre/akü bakımıyla da ilişkili).

---

# 2) Bagaj düzen + sabit 12V / USB

## Nedir?

Bagajın tabanına / kenarına **sabit düzen**: kutu, kayış, bölmeli organizer.  
Yanına veya paneline **sabit priz**: 12V çakmak ve/veya USB-C — çakmaklıktan uzatma kablosu değil.

## Ne işe yarar?

SUV bagajı boş bırakılınca:

- Jumper kablosu, üçgen, yelek, kompresör, alet, market poşeti **kayar dağılır**
- LPG’li araçta bazen hortum/adaptör/yedek parça da bagajda gezer
- Gece bir şey ararken her şeyi boşaltırsın

Düzen + priz olunca:

- Her şey yerinde  
- Bagajda lastik şişirme, telefon/tablet, küçük soğutucu (opsiyon) beslenir  
- “Nerede bu kablo?” bitar

## Nasıl olur? (DIY)

```
1. Bagaj taban ölçüsü al (ix35: tekerlek yuvaları / eşik)
2. Seçenek A: Hazır kayışlı organizer (hızlı)
   Seçenek B: 9–12 mm kontrplak + halı kaplama + bölmeler (daha “proje”)
3. 12V hattı: arka sigorta / bagaj lambası ACC veya sürekli (sigortalı)
4. USB-C PD soketi panela göm
5. Vida / cırt — sökülebilir olsun (stepne erişimi)
```

**Hafta sonu:** Ölç + kes + monte = 1 gün.  
**Maliyet:** 500–3k TL.  
**DIY keyfi:** Yüksek — kendi düzenin.

---

# 3) Kapı ses yalıtımı (kısmi)

## Nedir?

Kapı sacının içine / döşeme arkasına **butil (yumuşak kauçuk tabaka)** + üzerine **keçe / köpük**.  
Tüm arabayı “ses stüdyosu” yapmak değil — **4 kapı** (istersen önce ön 2).

## Ne işe yarar?

| Önce | Sonra |
|------|--------|
| Yol, rüzgâr, yan araç gürültüsü net | Daha boğuk, yorgunluk azalır |
| Kapı “teneke” kapanır | Daha dolu kapanma sesi |
| Müzik / konuşma boğulur | Biraz daha net |

Kayseri–yol kombinasyonunda uzun yolda gerçekten hissedilir. Performans artışı yok; **konfor**.

## Nasıl olur? (DIY)

```
1. Kapı panelini sök (vida + klips — klips seti al)
2. Nem bariyeri / naylon varsa dikkatli aç
3. Dış sacın düz yerlerine butil yapıştır (hava kabarcığı olmadan)
4. Üzerine keçe
5. Speker çevresini abartma (titreşim/akustik)
6. Paneli tak — cam/kilit kabloları sıkışmasın
```

**Hafta sonu:** 1 kapı = yarım–1 gün → 2 hafta sonu 4 kapı.  
**Maliyet:** 2–5k TL malzeme (STP, Comfortmat tarzı).  
**Dikkat:** Ağırlık artar (az); su tahliye deliklerini kapama.

---

# 4) Konsol USB-C PD + kablo düzeni

## Nedir?

Eski çakmak / zayıf USB yerine **gerçek telefon şarjı**: USB-C Power Delivery (ör. 30–45–60W).  
Kabloyu konsol içinden geçirip telefon standına gizli götürmek.

## Ne işe yarar?

| Eski | Yeni |
|------|------|
| Çakmak + kalın adaptör, dağınık | Tek soket, hızlı şarj |
| “Şarj olmuyor / yavaş” | Navigasyon açıkken bile besler |
| Kablo vites/kol dayama arası | Gizli hat, tek uç dışarı |

Her gün en az bir kez telefon kullanıyorsun — bu doğrudan günlük iş. StarLine/telefon dönemi gelince de konsolda temiz güç olur.

## Nasıl olur? (DIY)

```
1. Çakmak soketinin arkasındaki + / − bul (ACC olmalı)
2. PD QC soket modülü tak (veya çakmak→PD dönüştürücü göm)
3. Sigorta değerini aşma (genelde 10A hat)
4. İnce USB-C kabloyu konsol boşluğundan telefon yerine çek
5. Mıknatıs / vent stand (camı kaplama)
```

**Hafta sonu:** ½–1 gün.  
**Maliyet:** 300–1.5k TL.  
**Dikkat:** Ucuz “PD yazıyor ama 5W” adaptör alma; gerçek PD çipli olsun.

---

# 5) Sabit akü bakım prizi + voltmetre — ne alaka?

Bu dörtlüden ayrı ama **senin arabana özel mantıklı**; onun için ayrıca anlattım.

## Senin araçta akü neden yorulur?

| Ne | Aküyü yer (kontak kapalıyken bile) |
|----|-------------------------------------|
| **Smart Key / SMK** | Anahtarı sürekli dinler |
| **Prins LPG beyni** | Küçük standby |
| Alarm / radyo bellek | Klasik çekiş |
| İleride dashcam park modu | Ciddi çekiş |
| İleride StarLine GSM | Ciddi çekiş |

Araba 3–4 gün durunca (iş seyahati, kış) akü eşiğe gelir → start zorlar veya Smart Key saçmalar.  
Bu “araba bozuk” değil; **elektronik + bekleme akımı**.

## Sabit bakım prizi nedir?

Motor bölmesine (veya bagaja) **kalıcı bir soket** (çoğu CTEK / NOCO uyumlu “comfort connect” tipi).

```
Akü kutupları ──sigorta──► sabit priz (ön kaput yanında)
                              ▲
                         Evdeki akü bakıcı
                      (haftada bir tak-çıkar)
```

**Ne işe yarar?**  
Her seferinde akü borusunu söküp krokodil takmazsın. Kaputu aç, bakıcıyı tak, sabah çıkar. Özellikle kış / uzun park.

## Voltmetre ne alaka?

Kabinde (veya çakmakta) **küçük volt göstergesi**:

| Gösterge | Anlam |
|----------|--------|
| Kontak açık, motor kapalı ~12.0–12.5 V | Normal dinlenme civarı |
| Motor çalışırken ~13.8–14.5 V | Şarj (alternatör) çalışıyor |
| Motor çalışırken 12.5 V altı | Şarj zayıf / kayış / alternatör |
| Sabah 11.8 V | Akü bitmiş sayılır |

**Ne işe yarar?**  
- “Bu hafta akü yumuşak”ı arıza lambasından önce görürsün  
- Dashcam park modu / ek elektronik takınca “aküyü öldürdü mü?” diye bakarsın  
- LPG + Smart Key kombinasyonunda **erken uyarı**

Bakım prizi = **doldur/koru**.  
Voltmetre = **gör, karar ver**.  
İkisi birlikte: “neden start zor?” sorusunun yarısını çözer.

## Nasıl olur? (DIY)

```
1. Akü + yakınına sigortalı kablo (kısa mesafe)
2. CTEK comfort plug / benzeri paneli çamurluk / su tutmayan yer
3. Kabinde: çakmak tipi USB+voltmetre VEYA gömülü mini display
4. İsteğe bağlı: akıllı bakıcı (CTEK, NOCO) evde kalır
```

**Hafta sonu:** ½ gün.  
**Maliyet:** Priz + kablo ~300–800 TL; bakıcı cihaz ~1.5–4k; voltmetre ~100–400 TL.

## Dörtlüyle bağlantısı

- Dashcam park modu alacaksan → **voltmetre + bakıcı** neredeyse şart  
- USB-C / bagaj 12V eklersen → çekiş artar → yine aynı mantık  
Yani süs değil; senin elektronik profiline **altyapı**.

---

# Hangisini seçmeli?

| İstediğin | Seç |
|-----------|-----|
| “Her gün somut güvenlik” | **Dashcam** |
| “Bagaj çöplüğünden bıktım + DIY zevki” | **Bagaj düzen** |
| “Yolda yoruluyorum, sessizlik” | **Kapı yalıtımı** |
| “Küçük iş, hemen bitsin, her gün şarj” | **USB-C PD** |
| “Akü / Smart Key / ileride kamera korkusu” | **Bakım prizi + voltmetre** |

İkisini birleştirmek de mantıklı: örn. **USB-C (kolay) + voltmetre** aynı gün; veya **dashcam + bakım prizi**.

Birini söyle → `projeler/<isim>/` açıp malzeme + Cumartesi-Pazar adımlarını yazarız.

---

*StarLine / koltuk soğutma / walk-away’e karışmaz.*
