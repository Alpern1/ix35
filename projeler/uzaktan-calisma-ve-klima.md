# Uzaktan Çalıştırma & Klima Kontrolü

> Telefon veya kumandayla aracı uzaktan çalıştırıp kabini ısıtmak/soğutmak.

## Durum

- **Durum:** 📋 Planlama
- **Öncelik:** Orta
- **Tahmini bütçe:** Kurulum dahil ~8.000–20.000+ TL (Türkiye, kaliteye göre değişir)
- **Zorluk:** Zor (manuel vites + LPG + eski model)
- **Oluşturulma:** 2026-07-09
- **Son güncelleme:** 2026-07-09

## Motivasyon

Kışın ısıtılmış, yazın serinletilmiş araca binmek. Telefondan kontrol — modern Hyundai'lerdeki Blue Link / myHyundai deneyimine yakın bir şey.

## Gerçekçi beklenti ayarı

2012 ix35'te **fabrika uygulaması veya Blue Link ile klima ayarlama yok**. Yapılabilecek olan:

| Özellik | Mümkün mü? | Nasıl? |
|---------|------------|--------|
| Uzaktan motor çalıştırma | Evet (aftermarket) | Remote start modülü |
| Kumandayla çalıştırma | Evet | OEM kumanda 3x kilit veya ayrı kumanda |
| Telefondan çalıştırma | Evet | DroneMobile, Viper SmartStart vb. (aylık abonelik) |
| Uygulamadan sıcaklık **ayarlama** | **Hayır** (bu araçta) | Yeni Hyundai'lerde Blue Link ile var; 2012 ix35'te yok |
| Çalışınca klima çalışması | Kısmen | Motor çalışınca klima **son bırakılan ayarda** devreye girer |
| Koltuk ısıtma uzaktan | Belki | Aux çıkışı olan sistemlerle; ek kablolama |

**Yani:** Motoru uzaktan çalıştırırsın, klima son ayarında çalışır. Uygulamadan "22 derece yap" demek bu araçta gerçekçi değil — önceden doğru ayarı bırakman gerekir.

## Araç özel zorluklar

### 1. Manuel şanzıman

Manuel vitesli araçlarda uzaktan çalıştırma **özel güvenlik prosedürü** ister:

- **Rezervasyon modu:** Vites boşta, el freni çekili, kapıdan çıkınca motor kapanır → sonra uzaktan çalıştırılabilir
- **"M" serisi** veya manuel uyumlu kit şart (otomatik kit **asla** takılmamalı — vites takılıyken çalışma riski!)
- Debriyaj sensörü, el freni, kapı sensörü kablolaması gerekir

### 2. LPG

- Uzaktan çalıştırmada genelde **benzinle** çalıştırma tercih edilir (LPG sistemi soğukken / güvenlik)
- LPG ECU ile uyum araştırılmalı; bazı sistemlerde LPG relay kesmesi gerekebilir
- **Mutlaka** LPG'ye hakim bir usta veya detaylı DIY araştırması

### 3. Immobilizer / smart key

- 2012 ix35'te immobilizer var → bypass modülü gerekir (Fortin EVO-ALL gibi)
- Smart key varsa push-to-start prosedürü; klasik anahtar varsa farklı kit

## Seçenekler

### Seçenek A — Compustar + DroneMobile (telefon uygulaması)

| Bileşen | İşlev |
|---------|-------|
| Compustar remote start (manuel uyumlu) | Motor çalıştırma, güvenlik |
| Fortin EVO-ALL veya benzeri bypass | Immobilizer atlama |
| DroneMobile X1-LTE modülü | Telefon uygulaması, sınırsız menzil |
| Aylık abonelik | ~$6–12/ay |

**Artıları:** Olgun ekosistem, uygulama iyi, GPS (premium)
**Eksileri:** Türkiye'de parça/bulma; aylık ücret; profesyonel kurulum önerilir

### Seçenek B — Fortin EVO-ALL tek başına (OEM kumanda)

- Mevcut kumandada **3x kilit** ile çalıştırma
- Telefon yok; sınırlı menzil (kumanda menzili)
- Daha ucuz ama daha az özellik

### Seçenek C — Türkiye anahtarcı paketi

- "Uzaktan çalıştırma + anahtarsız giriş" paketleri
- Yerel kurulum ve kodlama
- **Risk:** Usta kalitesi, LPG uyumu, manuel vites güvenliği

### Seçenek D — Hyundai OEM kit (2B056-ADU01)

- 2012–2015 Hyundai için OEM remote start kiti mevcut
- **ix35 uyumluluğu net değil** — çoğunlukla Santa Fe vb. için listeleniyor
- Bayi kurulumu önerilmiş; Türkiye'de bulunabilirlik düşük

## Klima pratik kullanım senaryosu

1. Eve park ederken: klima **max soğutma** veya **max ısıtma** + fan ayarını bırak
2. Sabah/akşam: telefondan veya kumandadan çalıştır (5–15 dk)
3. Araca bindiğinde kabin hazır
4. **Otomatik klima** varsa daha iyi; **manuel klima** ise son bırakılan konumda çalışır

→ Arabada **otomatik klima var mı?** öğrenilmeli.

## Güvenlik gereksinimleri (vazgeçilmez)

- [ ] Kaput pin switch (hood pin) — kaput açıkken çalışmasın
- [ ] El freni sensörü
- [ ] Kapı sensörleri
- [ ] Manuel vites: rezervasyon modu veya nötr algılama
- [ ] LPG güvenlik kesmesi
- [ ] Uzaktan çalışma süre limiti (genelde 15–20 dk)

## Açık sorular

- [ ] Smart key mi, klasik anahtar mı?
- [ ] Otomatik klima mı, manuel klima mı?
- [ ] LPG sistemi markası/modeli? (Lovato, Tartarini, Atiker…)
- [ ] Koltuk ısıtıcı var mı?
- [ ] Öncelik: telefon mu, sadece kumanda yeterli mi?
- [ ] Aylık abonelik (DroneMobile vb.) kabul edilebilir mi?

## DIY değerlendirmesi

| Bölüm | DIY? |
|-------|------|
| Araştırma & parça seçimi | Evet |
| Kablolama & montaj | Zor — deneyim gerekir |
| Immobilizer bypass programlama | Orta–Zor |
| Manuel vites güvenlik ayarı | Kritik — hata tehlikeli |
| LPG entegrasyonu | Uzman önerilir |

**Kullanıcı tercihi:** DIY öncelikli ama güvenlik kritik olduğu için en azından manuel vites + immobilizer kısmında deneyimli birinden doğrulama alınmalı.

## Linkler

- [Fortin EVO-ALL — Hyundai push-to-start kurulum](https://manualspro.net/259911-fortin-108601-evo-all-and-hyundai-push-to-start-installation-guide)
- [Compustar DroneMobile](https://www.compustar.com/dronemobile-smartphone-car-control)
- [Manuel vites remote start güvenliği (Lifewire)](https://www.lifewire.com/remote-car-starters-manual-transmissions-534880)
- [Hyundai OEM Remote Start Kit 2012–2015](https://hyundai.worldoemparts.com/oem-parts/hyundai-2012-2015-hyundai-remote-start-vehicle-security-system-2b056adu01)

## Kararlar

| Tarih | Karar | Gerekçe |
|-------|-------|---------|
| 2026-07-09 | Fabrika app çözümü mümkün değil | 2012 ix35'te telematik yok |
| 2026-07-09 | Aftermarket + manuel uyumlu kit gerekli | Manuel vites + immobilizer |

## Notlar

- İki proje (otomatik kilit + uzaktan çalıştırma) **tek pakette** anahtarcıdan alınabilir — fiyat karşılaştırmasında birlikte sor.
- DroneMobile sıcaklık göstergesi için ekstra sensör (thermistor) gerekebilir; bu sadece **ölçüm**, ayarlama değil.
