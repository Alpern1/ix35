# Koltuk Soğutma / Havalandırma (OEM görünüm)

> Ön koltuklara (şoför ± yolcu) hava geçişli soğutma hissi — fabrika gibi görünsün.  
> Araç: 2012 ix35 · **koltuk ısıtma var** · Smart Key · Kayseri  
> **Durum:** 💡 Fikir / araştırma  
> **Oluşturulma:** 2026-07-22

Araç: [araba/ozellikler.md](../../araba/ozellikler.md) · [araba/notlar.md](../../araba/notlar.md)

---

## Kısa hüküm

**Yapılabilir.** 2012 ix35’te fabrika ventilated seat yok; aftermarket / döşemeci ile ekleniyor.  
“OEM gibi” istiyorsan **koltuk kılıfı / minder değil** — koltuğun içine fan + delikli yüzey + gizli anahtar.

Ama dil önemli: Çoğu insanın “koltuk soğutma” dediği şey aslında **havalandırma (ventilated)**. Gerçek **soğutulmuş hava (cooled / climate seat)** daha pahalı ve nadir.

| | Ventilated (yaygın) | Cooled / Climate (premium) |
|--|---------------------|----------------------------|
| Ne yapar | Kabin havasını koltuktan geçirir; teri kurutur | Havayı **aktif soğutur** (Peltier) |
| His | Serinlik / kuruluk | Gerçekten daha soğuk hava |
| Güncel araçlarda | Çoğu SUV/sedan “ventilated” | Genesis, lüks, bazı üst Hyundai |
| ix35 retrofit | **En gerçekçi OEM yolu** | Mümkün ama pahalı / güçlü / zor |
| TR’de isim | “Koltuk soğutma” diye satılır | Gerçek TED’li paket az |

**Öneri (senin araç + OEM hedef):** Önce **ventilated (fan)** düşün. Gerçek Peltier ancak bütçe ve beklenti çok yüksekse.

---

## Güncel araçlarda hangi teknoloji?

### 1) Ventilated seats (en yaygın OEM)

```
Kabin havası → koltuk altı fan(lar)
            → sünger kanalları / reticulated foam
            → delikli deri (perforasyon)
            → sırt + oturma yüzeyinden dışarı (veya içeri emiş)
```

- Klima soğuk havayı kabine basınca koltuk da o havayı taşır → etki artar  
- Klimasız / sıcak kabinde sadece “fan” hissi kalır  
- BMW gibi bazı markalar **emiş** (ter + nemi çeker), çoğu **üfleme** kullanır  

Hyundai/Kia’nın çoğu “koltuk havalandırma”sı bu sınıf.

### 2) Climate Control Seat / aktif soğutma (Gentherm CCS vb.)

```
Fan → Peltier (TED) soğuk yüzeyi
    → kanallardan delikli yüzeye soğuk hava
    → sıcak yüzeyi (waste heat) koltuk altına atılır
```

- Polarite ters → aynı ünite **ısıtma** da yapabilir  
- Gerçek ΔT: kabin havasından birkaç–on derece daha serin his  
- Daha çok akım çeker; atık ısı kabine gider (klima yükü)  
- Hyundai Genesis servis kılavuzunda “Climate Seat Unit + TED” diye geçer  
- Fabrika adı bazen “ventilated” yazsa da içinde TED vardır — pazarlama karışık  

### 3) Klima kanallarını koltuğa bağlamak

Nadir / özel; fabrika HVAC’ye tap. OEM gibi zor, sızıntı/ses riski. Aftermarket’te tercih edilmez.

---

## Soğutma için ne lazım? (parça listesi)

### Ventilated (OEM görünüm hedefi)

| Parça | Neden |
|-------|--------|
| **Delikli deri / perforasyon** | Hava çıkışı — düz deride fan işe yaramaz |
| **Kanalı sünger / mesh foam** | Havayı yüzeye dağıtır |
| **Blower fan** (oturma + sırt, genelde 2–4 adet/koltuk) | Hava hareketi |
| **Kablo + röle / kontrol kutusu** | IGN ACC, sigorta, kademe |
| **Anahtar** | Koltuk yanına OEM tarzı rocker veya klima paneli entegrasyonu |
| **Mevcut ısıtma** | Korunmalı — mat kesilmeden / üstüne bozmadan plan |

Senin araçta **ısıtma zaten var** → artı: güç hattı / anahtar yeri düşüncesi kolaylaşır.  
Eksi: ısıtma matı ile fan süngeri aynı katmanda çakışabilir; usta doğru sırayı bilmeli.

### Aktif cooled (TED) ekstra

| Parça | Neden |
|-------|--------|
| **Peltier TED modül** (+ heatsink) | Havayı soğutur |
| Daha güçlü fan / egzoz yolu | Atık ısıyı koltuktan uzaklaştır |
| Daha kalın kablo / sigorta | Akım yüksek |
| Isıtma matı genelde **çıkar** veya TED ısıtma kullanır | Çift sistem çakışır |

ABD’de “Sanctum / LeatherSeats TED kit” tarzı paketler: perforasyon + flow foam **şart** diyor.

---

## OEM görünecek şekilde nasıl yapılır?

### İyi yol (tavsiye)

1. Koltukları sök (veya döşemeci yerinde)  
2. Kılıfı aç → süngere kanal / fan yuvası  
3. Fanları gizli bağla (koltuk altı görünmez)  
4. Deriyi **delikli** yap (makine ile düzenli delik) veya delikli kılıf değiştir  
5. Anahtarı koltuk yanına / konsola **fabrika gibi** göm  
6. Isıtma çalışmaya devam etsin (ayrı kademe)  
7. Kablo IGN ACC’ten, uygun sigorta  

Kore’de Tucson/Santa Fe “seat climate retrofit” fotoğrafları bu mantıkta; süre ~3–4 saat/koltuk iddiası (profesyonel).

### Kötü yol (OEM değil)

- Üstten minderle fanlı kılıf (AliExpress ~ucuz)  
- Görünür kablo, kayar, “takılmış aksesuar” duruşu  

Sen “OEM görünecek” dedin → minder yolu **ele**.

### “Tam Audi klima paneli + kodlama” yolu (TR’de satılıyor)

Ender Elektronik vb. paketler: Audi orijinal parça, klima paneli revize, deri delme, fan, **kodlama** — liste **~72.000–100.000+ TL** (+ montaj opsiyonları).  
Bu genelde **Audi/VAG entegrasyonu** için; ix35’e birebir uymayabilir. Fiyat da StarLine bütçesini geçer. ix35 için **abartılı / yanlış platform** olabilir — önce Kayseri döşemeci + fan kiti sor.

---

## Türkiye’de nasıl yapılır? (pratik)

### Yol A — Yerel döşemeci + fan kiti (en mantıklı OEM hissi)

| Adım | Ne |
|------|-----|
| 1 | Kayseri / Konya / Ankara’da **araç döşeme + koltuk havalandırma** yapan usta bul |
| 2 | “İki ön koltuk, ısıtma kalsın, delikli deri, gizli anahtar, OEM görünsün” de |
| 3 | Fan kiti: TR oto elektrik / AliExpress “seat ventilation blower kit” (kalite seç) |
| 4 | Deri: mevcut deriyi del veya yeni delikli kılıf |
| 5 | Elektrik: ACC + sigorta; airbag / yan airbag kablosuna dokunma |

**Tahmini bütçe (kaba, 2026):**  
- Sadece fan + işçilik + delme (2 koltuk): **~15.000–40.000 TL** bandı (usta/kaliteye göre çok değişir)  
- Premium TED + tam klima paneli hikâyesi: **50.000–100.000+ TL** (çoğu ix35 için gereksiz)

Net fiyat için 2–3 ustadan keşif şart — bu rakamlar yön gösterici.

### Yol B — DIY

Mümkün (koltuk sökme, kılıf açma, fan vida, anahtar deliği).  
**Risk:** Yan airbag, oturma sensörü, ısıtma matı, dikiş kalitesi. Bobin/MAP’ten farklı — döşeme işi. OEM görünüm için dikiş/deri deneyimi lazım → çoğu kişi **Yol A**.

### Yol C — Hazır “soğutmalı minder”

Ucuz, hızlı, **OEM değil**. Bu hedef için hayır.

### Yol D — Başka araçtan OEM climate seat takmak

ix35 LM’de fabrika ventilated trim nadir/yok. Sonraki nesil Tucson koltuğu **oturmaz** (ray, airbag, konektör). Pratik değil.

---

## Senin araçta özel notlar

| Konu | Not |
|------|-----|
| Isıtma var | Koru; soğutma ayrı kademe olsun |
| Deri mi kumaş mı? | **Doğrulanacak** — havalandırma için delikli yüzey şart |
| Kayseri yazı | Ventilated yazın çok işe yarar |
| StarLine / uzaktan marş | Ayrı proje; koltuk fanı ACC’de çalışır, uzaktan marşta klima + fan stratejisi sonra konuşulur |
| Bütçe | StarLine (~25k) ile çakışırsa öncelik netleştir |

---

## Ne kadar “soğutur”? Beklenti yönetimi

| Sistem | Beklenti |
|--------|----------|
| Ventilated | Ter yapmaz, yapışmaz; klima açıkken belirgin rahatlık |
| TED cooled | Dokununca daha soğuk hava; hâlâ “buz gibi klima üflemesi” değil |
| Minder | Zayıf / gürültülü / çirkin |

Yazın Kayseri’de ventilated çoğu sürücü için **yeterli ve doğru hedef**.

---

## Karar ağacı

```
OEM görünüm istiyor musun?
 ├─ Hayır → minder (önermiyoruz)
 └─ Evet
      ├─ Bütçe orta, yazın rahatlık → VENTİLATED (fan) ← önerilen
      └─ “Gerçek soğuk hava” + yüksek bütçe → TED / climate seat
```

---

## Açık sorular (sen cevapla)

- [ ] Koltuklar **deri / suni deri / kumaş**?
- [ ] Sadece **şoför** mü, **ön iki** mi?
- [ ] Isıtma anahtarı nerede (koltuk yanı / konsol)? Foto varsa iyi  
- [ ] Hedef: “yapışmasın” mı, “buz gibi” mi?  
- [ ] Bütçe tavanı? (StarLine ile aynı anda mı?)

---

## Kaynaklar

| Kaynak | Ne |
|--------|-----|
| [KBB: ventilated vs cooled](https://www.kbb.com/car-advice/ventilated-seats-vs-cooled-seats-difference/) | Fan vs aktif soğutma |
| [OEMSeats: Peltier anlatımı](https://www.oemcarandtruckseats.com/blogs/knowledge-base/how-air-conditioned-car-truck-seats-work-the-basics) | TED + waste heat |
| [Hyundai Genesis climate seat (TED)](https://www.hgenesisdh.com/hyundai_genesis_dh_climate_seat_unit_description_and_operation-945.html) | Fabrika climate seat mantığı |
| [Gentherm CCS / EPA Hyundai](https://www.epa.gov/sites/default/files/2020-03/documents/hyundai-request-ghg-credit-gentherm-climate-seat-2019-12-13.pdf) | OEM aktif soğutma teknolojisi |
| [OhCar Tucson seat ventilation retrofit](https://oh-car.jp/en/car/hyundai-tucson-tl-seat-ventilation-review-848801) | Profesyonel fan ekleme örneği |
| [Ender Elektronik koltuk soğutma](https://enderelektronik.com.tr/urun/koltuk-sogutma-sistemi/) | TR yüksek fiyatlı “OEM panel” paketi (~72k+) |

---

## Kararlar

| Tarih | Karar | Gerekçe |
|-------|-------|---------|
| 2026-07-22 | Araştırma açıldı | OEM görünümlü koltuk soğutma merakı |
| 2026-07-22 | Öncelik adayı: ventilated | Gerçekçi, OEM hissi, maliyet/fayda |

---

*Son güncelleme: 2026-07-22*
