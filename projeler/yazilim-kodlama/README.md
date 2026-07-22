# Yazılım / Kodlama — 2012 ix35’te Beyinden Yapılabilecekler

> Araç: 2012 Hyundai ix35 · 1.6 GDI (G4FD) · Manuel · Smart Key · Prins LPG · Kayseri  
> Amaç: İnsanların yazılımla ne yaptığını, bu araçta neyin gerçekçi olduğunu netleştirmek.  
> **Durum:** 💡 Fikir / araştırma  
> **Oluşturulma:** 2026-07-22

Araç bilgisi: [araba/ozellikler.md](../../araba/ozellikler.md) · [araba/notlar.md](../../araba/notlar.md)

---

## Kısa cevap

2012 ix35 **VW/BMW kadar “gizli özellik cenneti” değil**. Yine de üç ayrı dünyada yazılım işi var:

| Dünya | Ne yapılır | Bu araçta? |
|-------|------------|------------|
| **A — BCM / GDS kodlama** | Donanımı var, yazılım kapalı özellikleri aç | Sınırlı ama gerçek |
| **B — ECU chip tuning** | Motor beyin haritasını değiştir | Yaygın (1.6 GDI) |
| **C — Servis programlama** | Anahtar, immobilizer, PCM update | Gerekince yapılır |
| **D — Multimedya** | CarPlay / Android Auto | Genelde **donanım değişimi**, beyin kodlama değil |

VW’deki gibi “VCDS ile 30 gizli özellik” beklentisi yanlış. Hyundai LM’de menü daha kısa; asıl popüler işler **chip tuning** ve birkaç **BCM seçeneği**.

---

## Motor beyni (ECU)

| | |
|--|--|
| Motor | 1.6 GDI · G4FD · ~135 hp / ~164–165 Nm |
| ECU | **Bosch MED17.9.8** (tuning dosya sitelerinde bu aile) |
| Yöntem | OBD veya bench flash (KESS, Autotuner, Flex, Dimsport vb.) |

### İnsanlar ne yapıyor?

| İşlem | Tipik sonuç | Not |
|-------|-------------|-----|
| **Stage 1 / performans** | ~+10–16 hp, ~+15–20 Nm | TR satıcıları 150–151 hp bandı iddia ediyor |
| **Yakıt odaklı map** | Daha düz tork, düşük devirde çekiş | “%15 tasarruf” iddiaları abartılı olabilir |
| **Vmax limiter kaldırma** | Hız sınırı (varsa) | SUV’da pratik değeri düşük |
| **Start/Stop OFF** | ISG kapatma | Bu araçta ISG yoksa anlamsız |
| **Pop & bang / crackle** | Gaz bırakınca patırtı | Turbo’lu GDI’larda daha çok; **NA 1.6’da az anlamlı**, katalizör riski |
| **EGR OFF / DECAT / DTC sil** | Emisyon bypass | Yasal/muayene riski; benzinli GDI’da “DPF OFF” genelde **dizel** dünyası |

### LPG (Prins) uyarısı — kritik

Prins **ayrı bir gaz beyni**. Benzin ECU map’i değişince:

- Gaz beyni hâlâ eski yakıt/devir mantığına göre çalışabilir
- Zengin/fakir karışım, tekleme, yüksek egzoz sıcaklığı riski
- Chip sonrası **Prins kalibrasyonu / log** şart sayılmalı

**Sonuç:** LPG’li araçta “sadece chip at, bitir” riskli. Tuningci + LPG ustası birlikte düşünülmeli.

### Bu araç için değerlendirme

| | |
|--|--|
| Yapılabilir mi? | Evet — dosya/servis bol |
| DIY? | Zor — brick riski, immobilizer, LPG |
| Değer? | Performans artışı mütevazı (~%10); “wow” beklenmemeli |
| Öncelik | Merak / deneme — zorunlu değil |

---

## Gövde beyni (BCM / IPM) — “kodlama”

Servis kılavuzunda Tucson/ix35 LM BCM’de tanımlı fonksiyonlardan senin için anlamlı olanlar:

### Gerçekten konuşulan / açılabilenler

| Özellik | Ne | Kaynak / gerçeklik |
|---------|----|-------------------|
| **Hıza bağlı otomatik kapı kilidi** | ~15 km/s üzeri kilitle | Forum + BCM: *Vehicle Speed Linked Auto Door Lock*. Birçok ix35’te **kapalı gelir**, bayi GDS ile açar |
| **Otomatik kilit açma** | Kontak OFF / sürücü kapısı / (otomatikte) P | Menü veya GDS; donanıma göre |
| **DRL (gündüz farı) seçeneği** | Dedicated DRL / NA DRL | BCM’de *DRL OPTION* var — **donanım (ayrı DRL lambası) yoksa** kodlama yetmez |
| **Escort / follow-me-home** | Farlar IGN OFF sonrası kısa süre yanık | BCM: HEADLAMP ESCORT (bazı pazarlarda) |
| **Welcome light** | Kumanda unlock’ta far/stop kısa yanma | BCM: HEADLAMP WELCOME — pazar/opsiyon bağımlı |
| **Ayna otomatik katlanır** | Kilitleyince katla | BCM’de *OUTSIDE MIRROR AUTOFOLDING* yazıyor ama **elektrikli katlanır ayna donanımı** şart. Yoksa aftermarket modül |

### Senin araçta önce doğrulanacaklar

```
□ Otomatik katlanır ayna var mı? (henüz araba/ozellikler’de belirsiz)
□ Ayrı DRL lambası / LED şerit var mı?
□ Trip/ayar menüsünde “otomatik kapı kilidi” satırı var mı?
□ ISG (start-stop) var mı? (1.6 GDI’da genelde yok)
```

### VW tarzı “gizli özellik” beklentisi

Hyundai kodlama piyasası VAG kadar zengin değil. TR’de “gizli özellik açma” reklamları çoğunlukla:

- Yeni nesil araçlar, veya
- Aslında **chip tuning / DPF** satışı

2012 LM için gerçekçi paket: **otomatik kapı kilidi + (donanım varsa) DRL/ayna**.

---

## Anahtar / Smart Key (SMK) — programlama

Bu “tuning” değil; **servis yazılımı**:

| İşlem | Ne zaman |
|-------|----------|
| Yeni Smart Key öğretme | Anahtar kaybı / yedek |
| SMK / ECM / PDM / ESCL neutral | Modül değişimi sonrası |
| Immobilizer eşleme | Beyin veya SMK değişince |

Araç: Smart Key + START/STOP → SMK programlama yolu var (OBDSTAR vb. araç listelerinde ix35 EL/LM geçiyor).

**Günlük “özellik açma” değil** — bozulunca / anahtar alınca lazım.

---

## Gösterge (cluster)

| İstek | Gerçekçi mi? |
|-------|----------------|
| Sürekli vites göstergesi | **Hayır** — GSI öneri sistemi; peşine düşülmedi ([araba/notlar.md](../../araba/notlar.md)) |
| Km / dil / birim | Serviste cluster ayarı / değişimde kodlama |
| Ek gösterge (yağ basıncı vb.) | Fabrika yazılımıyla genelde **yok** |

Cluster arızalarında (hız/devir gitmez) bazen kart onarımı anlatılıyor — bu yazılım “özellik” değil, tamir.

---

## Multimedya — insanlar en çok bunu yapıyor

Fabrika ekrana CarPlay **kodlayarak** açmak 2012 ix35’te pratikte yok (Blue Link / modern head unit yok).

Yaygın yol:

| Yöntem | Tür |
|--------|-----|
| Android / CarPlay **aftermarket teyp** | Donanım değişimi + CAN bus adaptör |
| Plug & play kit (fasya + kablo) | Direksiyon tuşu / kamera korunur |

Bu **beyin yazılımı projesi değil**; ayrı proje konusu olabilir.

---

## İnsanların yaptıkları — özet harita

```
                    2012 ix35 yazılım dünyası
┌──────────────────────────────────────────────────────────┐
│  POPÜLER                                                  │
│  • Stage 1 chip (MED17.9.8)                               │
│  • Aftermarket CarPlay teyp (donanım)                     │
│  • GDS ile hızda otomatik kapı kilidi                     │
│  • Yedek Smart Key programlama                            │
├──────────────────────────────────────────────────────────┤
│  DONANIM VARSA KODLAMA                                    │
│  • DRL option                                             │
│  • Ayna autofold                                          │
│  • Welcome / escort light                                 │
├──────────────────────────────────────────────────────────┤
│  AZ MANTIKLI / RİSKLİ                                     │
│  • Pop & bang (NA + LPG)                                  │
│  • Emisyon kapatma (muayene)                              │
│  • “Sürekli vites” cluster hack                           │
│  • LPG’siz düşünülmüş agresif map                         │
└──────────────────────────────────────────────────────────┘
```

---

## Araçlara göre “kim ne kullanır?”

| Araç | Ne için |
|------|---------|
| **Hyundai/Kia GDS** (bayi) | BCM seçenek, PCM update, teşhis |
| **Launch / Autel / benzeri** | Kod okuma, bazen sınırlı coding |
| **KESS / Autotuner / Flex** | ECU okuma-yazma (chip) |
| **OBDSTAR / VVDI** | Anahtar / SMK |
| **VCDS / Carly “her şey”** | Bu araçta VW kadar işe yaramaz |

---

## Senin profiline göre öneri sırası

1. **Ücretsiz / ucuz kontrol:** Trip menüde otomatik kapı kilidi var mı? Yoksa GDS ile açtırılabilir mi sor.
2. **Donanım teyidi:** Elektrikli katlanır ayna? DRL? → `araba/ozellikler.md` güncelle.
3. **Chip:** Sadece gerçekten tork/tepki istiyorsan; **Prins ile birlikte** planla. Beklenti: +10–15 hp civarı.
4. **Multimedya:** Yazılım değil ayrı proje (CarPlay teyp).
5. **Yapma:** Pop & bang, emisyon silme, “sürekli vites” peşine düşme.

---

## Açık sorular (senin cevabın lazım)

- [ ] Elektrikli **otomatik katlanır** ayna var mı?
- [ ] Ayrı **DRL / gündüz LED** var mı?
- [ ] Ayar menüsünde **otomatik kapı kilidi** satırı görüyor musun?
- [ ] Chip / performans ilgisi var mı, yoksa sadece konfor kodlama mı?
- [ ] CarPlay / yeni teyp ayrı fikir olarak konuşulsun mu?

---

## Kaynaklar

| Kaynak | Ne |
|--------|-----|
| [BCM fonksiyon listesi (Tucson LM)](https://www.htmanual.net/body_control_module_bcm_description_and_operation-1145.html) | Auto lock, DRL, mirror fold, welcome… |
| [Forum: ix35 auto lock / mirror](https://www.hyundai-forums.com/threads/ix35-questions-automatic-door-locking-electric-folding-mirrors-compass.232345/) | Bayide auto lock açtırma |
| [ix35 1.6 GDI Stage 1 örnek](https://www.dyno-chiptuningfiles.com/chiptuning-file/hyundai-ix35-16-gdi-135hp/) | MED17.9.8, ~+10 hp |
| [TR Remaps 1.6 GDI](https://www.remaps.com.tr/chip-tuning/hyundai/ix-35/2010-ve-sonrasi/1.6-gdi/stage-1/GafCeaRbJ) | ~150 hp iddiası |
| Kullanım kılavuzu GSI | Önerilen vites (sürekli değil) |

---

## Kararlar

| Tarih | Karar | Gerekçe |
|-------|-------|---------|
| 2026-07-22 | Araştırma dosyası açıldı | “Yazılımla ne yapılır?” merakı |
| 2026-07-22 | Sürekli vites göstergesi elendi | GSI tahmin; konum sensörü yok |

---

*Son güncelleme: 2026-07-22*
