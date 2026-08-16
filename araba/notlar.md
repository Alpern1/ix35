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
| Kapasite | Servis dolumu kabaca **3,6 L** + filtre; çubuk F–L arası ~1 L civarı (kılavuzdan teyit). Yağ: **5W-30** sentetik (ACEA C2/C3 / API SM+). |

**Ne yap:** Bakımdan sonra çubuğu işaretle → 1000 km sonra düz zeminde, motor ılık, 2–3 dk bekle, ölç. Dış kaçak (conta, karter, PCV hortumu) yoksa içeride yanıyor demektir.

**Alarm:** Egzozda mavi duman, buji yağlı, rölanti dalgalı, yağ kokusu / benzin kokulu yağ (seyreltme). Yağ basınç lambası yanınca karter zaten tehlikeli derecede boştur.

GDI pratik: değişim **7–8 bin km** (fabrika 15–30 bin uzun); yağ seviyesini yakıt alırken bak.

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

**Değil (ilk teşhis):** Theta 2.4 motor erimesi, LPG’nin yağ yakması, acil segman revizyonu.

## Araştırma Linkleri

- _Proje dosyalarında toplanacak_

---

*Son güncelleme: 2026-08-16 — 1.6 GDI yağ yakma notu*
