# Genel Notlar

> Unutulmaması gereken ama tek bir kategoriye sığmayan bilgiler.

## Tercihler & Kısıtlar

- **DIY öncelikli:** Mümkün olduğunca kendim yapmak istiyorum.
- **Usta:** Yapamayacağım durumlarda usta devreye girer; ancak Türkiye'de usta maliyeti ve işçilik kalitesi riskli — dikkatli seçim gerekir.
- **Bütçe:** Henüz net sınır belirlenmedi.
- **Uzaktan çalıştırma:** Telefon şart değil ama **tercih edilen yöntem** — kumanda menzili kısa (~10 m), evden çalıştırma için LTE telefon modülü (DroneMobile vb.) mantıklı.

## Önemli Hatırlatmalar

- Araç **LPG'li (Prins)** — uzaktan çalıştırmada Prins VSI sistemi **her zaman benzinle** çalıştırır; depoda benzin olmalı. Motor ısındıktan sonra LPG'ye geçer — ısınma için uzaktan çalıştırma aslında uyumlu.
- **Manuel şanzıman** — uzaktan çalıştırma için rezervasyon modu şart; MyKeyPremium gibi plug-and-play kitler **manuel vitesle uyumlu değil**.
- **Smart Key + START/STOP** — walk-away otomatik kilit için uygun donanım mevcut.
- **Otomatik klima** — uzaktan çalıştırmada avantaj sağlar ama Blue Link tarzı uygulamadan sıcaklık ayarı bu araçta mümkün değil (detay: proje dosyası).
- **2012 model** — fabrika telematik (Blue Link) yok.
- **Manuel vites göstergesi (GSI):** Hız göstergesi ortasındaki sayı “şu anki vites” değil; **önerilen vites** (▲/▼). Vites konum sensöründen okumaz; devir+hız tahminidir. Sürekli gösterim için beyin yazılımı yolu yok / peşine düşülmeyecek.
- **Akü bakıcı:** Evde yok; akü bitme şikâyeti yok → “evden akü şarj / bakım prizi” peşine düşülmeyecek (yanlış hafta sonu önerisiydi).
- **Android yan kamera:** 360 ($500–600) istenmiyor; hedef teypte canlı sağ/sol. Teyp marka/model + soket foto bekleniyor.
- **Cam stor / park güneşliği:** Katlanır karton yok. Motor/otomatik yok. Sadece park; ön + 4 yan; siyah ince manuel stor. Kapıya vida yok.
- **1.6 GDI yağ yakar mı?** Her ix35 otomatik yağ yakan motor değil. Gamma **G4FD** (atmosferik, ~135 hp) ABD’deki Theta 2.4 “motor erir” hikâyesi değil. Ama GDI ailesinde yağ eksiltme **görülebiliyor** (karbon + segman, PCV, yakıtın yağa karışması). Bu araçta ölçülmedi — varsayma. LPG yağ yakmanın sebebi değil. Yağ lambasına güvenme; çubukla bak. Detay: aşağıda.

## 1.6 GDI yağ tüketimi (2026-08-16)

Bu araçta henüz düz zemin litre/km ölçümü yok. 2026-08-16 gözlem: yağ **~12.000 km önce** değişmiş; araç **%4–5 yokuş yukarı** parkken çubuk **L altı**. Bu, “motor bitti” demek değil — aşağıda neden.

| | |
|--|--|
| Motor | Gamma **G4FD**, atmosferik 1.6 GDI (~135 hp). Turbo 1.6T değil. |
| “Hepsi yakar” mı? | **Hayır.** Aynı motorda (ix35 / Sportage 1.6 GDI) hem hiç eksiltmeyen hem 4–5 bin km’de ~1 L eksilten örnek var. |
| Neden bazıları eksiltir? | GDI: emme subabında yakıt yıkaması yok → karbon; düşük gerilimli yağ segmanı kilitlenebilir; PCV tıkanırsa karter gazı yağı emme tarafına taşır; kısa yol + soğuk = benzinin yağa karışması (yağ incelir). |
| LPG (Prins) | Yağ yakmayı başlatmaz. LPG’de yağ genelde daha temiz kalır. Asıl LPG riski **kuru subap** (yanlış kit / sürekli gaz). Prins ısınana kadar benzinde çalışır — bu kısım GDI için normal. |
| Üretici “normal” | Hyundai/Kia bazı kılavuz/TSB’de **0,5–1 L / 1000 km**’ye kadar tolerans yazar. Pratikte bu geniş; senin için **1000 km’de 0,2 L altı** iyi, **~0,5 L** takip, **1 L+** fazla. |
| Kapasite | **3,6 L** servis (filtreyle). Filtresiz 3,3 L. L→F ≈ 0,6–1,0 L. **Üstüne 4 L dökme.** |

**Ne yap:** Bakımdan sonra çubuğu işaretle → 1000 km sonra düz zeminde, motor ılık, 2–3 dk bekle, ölç. Dış kaçak (conta, karter, PCV hortumu) yoksa içeride yanıyor demektir.

**Alarm:** Egzozda mavi duman, buji yağlı, rölanti dalgalı, yağ kokusu / benzin kokulu yağ (seyreltme). Yağ basınç lambası yanınca karter zaten tehlikeli derecede boştur.

GDI pratik: değişim **8.000 km veya 12 ay** (hangisi önce). Fabrika 15–30 bin bu motorda uzun. Seviye: yakıtta veya her 1.000 km çubuk.

### 2026-08-16 gözlem — L altı, yokuş, 12 bin km

| | |
|--|--|
| Ne görüldü | Çubuk L altı |
| Park | %4–5 eğim, burun yukarı |
| Motor | **Soğuk** (ılık değil) |
| Usul | Çubuğu taktı, **~30 sn** bekledi, çekti (sil-tak-çek net değil) |
| Yağ yaşı | ~12.000 km (değişim yok / seviye bakılmamış) |

**En olası:** 12 bin km boyunca bakılmamış yağ + GDI’nin hafif tüketimi. F→L arası kılavuzda **~0,6–1,0 L**. 12 bin km’de 1 L civarı eksilme ≈ **0,08 L / 1000 km** — segman ölümü değil, mütevazı tüketim + uzun aralık.

**Eğim:** Hyundai ölçümü **düz zemin** ister (ısınmış motor, stop, ~5 dk, sil-tak-çek). %4–5 yokuş, transvers motorda karterde ~1 cm yağ kaydırır; L–F bandının büyük kısmı kadar. Orta seviye yokuşta L altı görünebilir. F dolu yağ yokuşta L altına düşmez; net L altıysa düz zeminde de L civarı çıkar.

**Soğuk + 30 sn:** Kılavuzdaki ~5 dk, çubuğun ıslanması için değil — **ılık motoru kapattıktan sonra** yağın kafa/kanallardan kartere inmesi için. Araç zaten soğuksa yağ saatlerdir karterde; 30 sn vs 5 dk **seviyeyi değiştirmez**. Çubukta 30 sn beklemeye gerek yok: sil → tam tak → hemen çek.

Soğuk ölçüm Hyundai usulünden (ılık + 5 dk) ayrı: soğuk yağ büzülür, çubuk **biraz düşük** okunabilir (~0,2–0,3 L, L–F’nin bir kısmı). Yokuş + soğuk birlikte, gerçekte L üstü olan yağı L altı gösterebilir.

**Şimdi:** Düz yerde, kılavuz usulü bak — ılık motor, stop, **5 dk**, sil-tak-çek (30 sn yok). Hâlâ L altıysa **5W-30** ekle (yokuşta / soğukta F’ye doldurma). Sonra 12 bin km’lik yağı **değiştir**. 1000 km sonra düz + aynı usulle litre not et.

**Kriko / işe gitmek (2026-08-16):** Kullanıcı **tam değişim** yapacak — kirli yağın üstüne Castrol yok. Eklemek kriko istemez; boşaltmak ister (sehpa). L civarında kısa yol idare eder; yağdanlık yanmazsa işe gidilebilir. Değişim: boşalt + filtre → hedef **3,6 L** (önce 3,4–3,5, çubukla F). 1 L şişe yetmez; 4 L bidon.

**Litre (kaynak, 2026-08-16):**

G4FD 1.6 GDI. Erken UK ix35 kılavuzu (2010) sadece 2.0 benzin yazar (4,1 L) — 1.6 GDI o basımda yok.

| Kaynak | Miktar | Ne |
|--------|--------|-----|
| G4FD teknik / Motorreviewer / i30 G4FD | **3,6 L** filtreyle, **3,3 L** filtresiz | Motor ailesi |
| Kroon-Oil, cararac, Hyundai servis tabloları — ix35 1.6 GDI 2WD | **3,6 L** servis dolumu (filtre 0,3 L) | Bu kasa |
| 2019 Tucson kılavuzu (aynı 1.6 GDI satırı) | **3,6 L** drain and refill | Hyundai tablosu |
| garage.wiki ix35 “1.6 133 hp” | 3,3 L | Muhtemel MPI/filtresiz karışımı — **alma** |

**Yanlış viskozite (2026-08-18):** Son değişimde 5W-30 konmamış olması **katkı** olabilir, tek başına 10 bin km’de ~1 L’nin nedeni değil.

| Konmuşsa | Tüketim |
|----------|---------|
| **5W-30** sentetik (kitap) | Viskozite suçlu değil |
| **5W-40** | Kitapta alternatif. Genelde daha az eksiltir, daha fazla değil |
| **5W-20 / 0W-20** | İnce; GDI + km’de biraz daha yakabilir |
| Ucuz **10W-40** mineral (TR usta sık) | Uçucu/kalitesizse yanma artar; soğukta da akış kötü |

Fatura / kalan bidon / ustaya sor. Bu değişim: aldığın Castrol **5W-30** doğru. F’ye doldur, 1000 km ölç. Tüketim durursa viskozite+aralık; durmazsa motor (GDI). 5W-40’ı şimdi deneme — bidon 5W-30 ise onu koy.

### 2026-08-18 — değişim yapıldı

Çıkarılan yağ siyah. **Sorun işareti değil.** GDI 10–12 bin km’de neredeyse hep simsiyah olur (kurum + yakıt). Metal parıltı, süt/mayonez (su), benzin gibi ince kokulu ayrı şey — onları söylemedin.

**Şimdi (bugün/yarın):**
1. Düz zemin, stop, ~5 dk, sil-tak-çek. F ile L arası, tercihen F’ye yakın. Düşükse aynı 5W-30 ile az ekle; F’yi geçirme.
2. Motor 30–60 sn çalıştır (filtre dolar, seviye biraz iner), yine 5 dk, çubuk. Yağdanlık sönük kalsın.
3. İlk sürüşten sonra tapa + filtre altı: damlama yok.
4. **1.000 km** sonra aynı usulle bak — bu motorun litre/km’si o zaman çıkar.

**Aralık:** **8.000 km veya 12 ay.** 15 bin yapma. Çubuğu unutma; lambayı bekleme.

**Yağdanlık (2026-08-16):** Bu benzinde yağdanlık **seviye değil, basınç** lambası. Dizelde ayrı “seviye” lambası olabiliyor; 1.6 GDI’de yok. Lamba, pompa basıncı düşünce yanar — genelde karter neredeyse boş / pickup hava alınca. **Hiç yanmaması iyi:** basınç krizi olmamış. Çubuk L altı ile çelişmez; L’de hâlâ ~2,5 L yağ vardır, basınç durur. Seviyeyi çubukla bak; lambayı bekleme.

**Değil (ilk teşhis):** Theta 2.4 motor erimesi, LPG’nin yağ yakması, acil segman revizyonu.

### Yağ nereye gitti? (2026-08-16)

İlk değişimden sonra ~10–12 bin km, çubuk L altı (kötümser ölçüm). “Bir litre bir yerde duruyor” değil — ya **yandı** ya **dışarı sızdı** ya da **hiç konmadı**.

| Nereye | Nasıl | Bu araçta |
|--------|--------|-----------|
| Yanma (en sık GDI) | Segman / subap keçesi / PCV → emme → egzoz | 10 bin km’de ~0,5–1 L = **0,05–0,10 L/1000 km**. Mavi duman olmayabilir. |
| Dış kaçak | Tapa, filtre, kapak contas, karter, muhafaza üstünde | Parkta gölle yoksa yolda damlıyor veya yok. |
| Hiç dolmadı | İlk değişimde F’ye kadar konmamış | Sık. Çubuk orta + 10 bin km tüketim = L altı. |
| Filtre “yuttu” | **Yok.** Filtre döngüde ~0,2–0,3 L tutar; kayıp litre orada birikmez. | Filtreyi söküp kayıp yağı bulamazsın. |

Hissin doğru: “hiç eksilmesin” beklenir. Sayı: 10 bin km’de 1 L **felaket değil**, GDI’de görülür; 2 L+ veya mavi duman ayrı konu. Ölçüm yokuş+soğuk → gerçek kayıp 1 L’den az olabilir.

**Ulaşılır kontrol (kriko/değişim gecesi):**

1. Gece düz zeminde karton — sabah ıslak = kaçak. Kuru = büyük kaçak yok (alt muhafaza üstünde birikebilir; bak).
2. Üstten: siyah külbütör kapağı kenarı, buji kuyuları, hortumlu **PCV** (kapak üstü/yanı). Islak/yağlı mı.
3. Alttan (sehpa şart): tapa + conta, **vidalı yağ filtresi** (OEM 26300-35503), karter kenarı. İlk değişimin tapası gevşek/conta yoksa yavaş kaçak.
4. Egzoz: soğuk çalıştırma veya gaza basınca mavi duman.
5. Yağ kapağını aç: benzin kokusu = GDI seyreltme (yakma değil ama yağı incelterek tüketimi artırır).

PCV kapak üzerindeki hortumlu valf; sökülür, evde bakılır. Bu gece sökme. Tıkalı PCV tüketimi artırır ama “kayıp litre orada” değil.

**Asıl ölçüm:** yarın akşam F’ye kadar doldur (düz zemin), 1000 km sonra aynı usulle bak. O zaman bu motorun litre/km’si belli olur.

## Araştırma Linkleri

- _Proje dosyalarında toplanacak_

---

*Son güncelleme: 2026-08-16 — 1.6 GDI yağ yakma notu*
