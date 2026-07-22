# Nasıl yapılır — sade anlatım

> Elektronik jargon yok gibi yazıldı. Önce oku, sonra parça al.

---

## Bu iş ne?

Arabaya iki küçük kamera takıyorsun (sol + sağ).  
Her kameranın arkasından ince bir **video kablosu** Android teybe gidiyor.  
Teyp o görüntüyü ekranda açıyor — geri vites kamerası gibi, ama yan taraflar için.

**360 değil.** Üstten birleşik “kuş bakışı” yok. Sadece “şu an sol” / “şu an sağ” (veya ikisi ayrı kanal).

---

## Adım 0 — Teybi kontrol et (alışverişten önce)

1. Kontağı aç, Android teybi aç.
2. Ayarlar / Factory / Car settings içinde **Camera**, **AHD**, **CVBS**, **360** ara.
3. Mümkünse teybi sökmeden arkadan bak (veya eski kurulum foto): RCA dişi soketler (sarı video) veya “CAM IN” yazan fişler.
4. Şunu not et / foto çek:
   - Marka-model
   - “Rear / Front / Left / Right” yazan giriş var mı
   - Zaten geri kamera takılı mı

### Üç olası sonuç

| Sonuç | Ne yaparsın |
|-------|-------------|
| Left + Right girişi var | Klasik yol — iki kamera direkt |
| Sadece Rear (ve belki Front) var | Önce tek yan kamera **veya** teypte menüden “AV / USB kamera” var mı bak; yoksa giriş sınırlı |
| Hiç kamera girişi yok / sadece USB | USB kamera veya teyp değişimi gerekir — ayrı konu |

**Bu adım bitmeden Trendyol/AliExpress’ten kamera alma.**

---

## Adım 1 — Parça al (teyp uygunsa)

Detay liste: [malzemeler.md](malzemeler.md)

Özet:
- 2× yan kamera (tercihen **AHD 720p** — teybin AHD destekliyorsa; yoksa CVBS/analog)
- Yeterli uzunlukta video kablosu (ön kapı / ayna → konsol ~5–8 m genelde yeter)
- Güç için +12V / toprak (çoğu kamera setinde ince kırmızı-siyah kablo gelir)
- Bağlantı: RCA erkek-dişi, gerekirse ek adaptör
- Montaj: vida / 3M / ayna altı braket (kameranın tipine göre)

---

## Adım 2 — Kameraları nereye koyacaksın?

| Yer | Artı | Eksi |
|-----|------|------|
| **Yan ayna altı / gövde** | Kör nokta iyi | Ayna katlanınca hareket (sende katlanır ayna var) |
| **Çamurluk / kapı önü** | Sabit açı | Delik / yapıştırma; yıkamada dikkat |
| **Ayna üçgeni (A sütunu yanı)** | Kablo kısa olabilir | Görüş açısı dar kalabilir |

Pratik öneri: önce **yapışkanlı / vidalı ayna altı** tip; delik delmeden dene. Beğenmezsen yer değiştirirsin.

Katlanır ayna: kamera aynanın **gövdesine** (araca sabit parçaya) gelsin, katlanan kapağa değil — yoksa her kilitte görüntü kayar.

---

## Adım 3 — Kabloyu çekmek (mantık)

Her kamera için kabaca 3 şey:

1. **Video** (genelde tek koaksiyel / RCA) → teybin ilgili kamera girişine  
2. **+12V güç** → kontakla gelen hat (ACC) veya teybin “camera power” çıkışı  
3. **Toprak (GND)** → metal gövde veya teyp toprağı  

```
Kapı / ayna bölgesi          Kapı lastiği içinden          Konsol arkası
   KAMERA  ----video+güç------------------------------>  TEYP CAM IN
```

- Kabloyu kapı fitilinden / eşikten gizleyerek çek (dışarıda sarkmasın).
- Kapı menteşesinde **esnek bırak** — kapı açılınca kopmasın.
- Video RCA’yı teypte **Left** / **Right** (veya Front) yazan dişiye tak.
- Gücü rastgele sürekli aküye bağlama: araba kapalıyken kamera açık kalır, akü yer. **ACC** (kontak açıkken 12V) kullan.

---

## Adım 4 — Ekranda ne zaman açılsın?

| Mod | Nasıl | Ne zaman mantıklı |
|-----|-------|-------------------|
| **Elle** | Teyp menüsünden Camera → Left/Right | En kolay başlangıç |
| **Sinyalle** | Sol sinyal → sol kamera (tetik kablosu veya ayar) | Şerit değişimi |
| **Geri + yan** | Geri viteste arka + yan split (teyp destekliyorsa) | Park |

İlk kurulumda **elle aç** yeter. Sinyal otomatiği sonra.

---

## Adım 5 — Test checklist

- [ ] Kontak açık, kamera güç alıyor (objektif hafif ısınıyor / IR LED bazı modellerde yanar)
- [ ] Teypte doğru giriş seçili (AHD 720p vs CVBS — yanlışsa siyah ekran / karıncalı)
- [ ] Sol kamera gerçekten sol, sağ sağ (kablolar karışmış olabilir)
- [ ] Kapı tam açık/kapalı kablo gerilmiyor
- [ ] Yağmurda / yıkamada montaj oynamıyor

---

## Sık takılan yerler

| Belirti | Muhtemel sebep |
|---------|----------------|
| Siyah ekran | Yanlış giriş / AHD-CVBS uyumsuz / güç yok |
| Görüntü var ama pembe-yeşil | CVBS/AHD karışık veya bozuk kablo |
| Sadece geri çalışıyor, yan yok | Teypte yan kanal kapalı (factory ayar) veya giriş yok |
| Kontak kapalı akü düşüyor | Güç ACC’ye değil sürekli +12V’ye gitmiş |

---

## Senin için sıra (bu hafta)

1. Teyp marka/model + ayar menüsü / arka soket **foto** (sohbete atman yeterli)  
2. Ona göre “AHD mi CVBS mi, kaç giriş” netleşir  
3. Malzeme listesi kilitle → sipariş  
4. Hafta sonu: kablo + montaj  

Parça almadan önce foto gelirse yanlış alışveriş olmaz.
