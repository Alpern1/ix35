# Master Uygulama Planı

> Gerçek iş fazları — "bayiye sor" değil, "yap / öğren / kur / test et".
> Pes etme anın: teknik olarak imkânsız çıktığında veya inancını yitirdiğinde; adım listesi değil.

---

## Faz haritası

```
Faz 1          Faz 2           Faz 3            Faz 4           Faz 5
ANLA           SATIN AL        KUR              AYARLA          YAŞA
│              │               │                │               │
can.starline   Kutu + SIM      Kablo işi        Firmware+iKey   Günlük ritüel
Forum oku      elinde          (en zor kısım)   Fonksiyon 15    Sabah Siri
```

Her faz **somut bir beceri** veya **fiziksel çıktı** — "birine mesaj at" değil.

---

## Faz 1 — Anla (şu an, ücretsiz)

**Ne öğreniyorsun:** Bu iş gerçekten senin aracında yapılmış mı, neye benziyor?

| Görev | Nereden | Bitti sayılır |
|-------|---------|---------------|
| ix35 bağlantı şemasını indir | [can.starline.ru](https://can.starline.ru) → Hyundai → ix35/Tucson → 2012 → Start-Stop | PDF elinde |
| Forum kurulumunu oku | [ix35 2014 Start-Stop](https://support.starline.ru/communities/10/topics/41978-starline-a93-2can2lin-na-hyundai-tucson-ix35-2014-start-stop) | "CAN ile çalışıyor" kafanda oturdu |
| Günlük akışı içselleştir | [kullanim-senaryolari.md](kullanim-senaryolari.md) | Akşam/sabah ne yapacağını biliyorsun |
| Satın alma kanalını seç | [satin-alma-kanallari.md](satin-alma-kanallari.md) | Hangi siteden alacağın net |

**Bu fazda pes eder misin?** Sadece okuma. can.starline.ru'da ix35 şeması yoksa pes et — ama **var**.

---

## Faz 2 — Satın al (internet, kargo)

**Ne elde ediyorsun:** Kutu + SIM.

```
□ StarLine A93 v2 ECO 2CAN+2LIN
□ LTE Master 4G (veya GSM dahil paket)
□ nano-SIM (Türkiye operatör)
□ StarLine 2 uygulaması yüklü (henüz bağlanmasa da)
```

Kanal listesi: [satin-alma-kanallari.md](satin-alma-kanallari.md)

**Bitti sayılır:** Kutuyu açtın, pin-konvert kartı var, parçalar eksiksiz.

**Bu fazda pes eder misin?** Kargo/gümrük sürprizi olursa alternatif satıcı dene — tek satıcıya bağlı kalma.

---

## Faz 3 — Kur (asıl iş — burası zor)

**Ne yapıyorsun:** Telleri şemaya göre bağlıyorsun.

Bu fazın zorluğu montaj karmaşıklığında; adım sayısında değil.

| Alt adım | Zorluk |
|----------|--------|
| Konsol sökme, ünite montajı | Orta |
| CAN/LIN tap noktaları | Zor — şemaya harfiyen uy |
| START/STOP, el freni, debriyaj | Orta |
| LTE anten yerleşimi | Kolay |

**Kaynak:** can.starline.ru şeması + ix35 forum fotoğrafları.

**Bitti sayılır:** Akü bağlı, ünite açılıyor, kısa devre yok.

**Bu fazda pes eder misin?** En olası yer burası. Çözüm: bir günde bitirme; önce kablo, sonra konsol. Takılırsan foruma foto at — bayi değil, topluluk.

**Usta?** İstersen sadece bu fazı ustaya yaptır; geri kalanı sen. Tam DIY de mümkün.

---

## Faz 4 — Ayarla (yazılım + ilk çalıştırma)

**Ne yapıyorsun:** Arabayı sisteme tanıtıyorsun.

| Adım | Araç |
|------|------|
| Firmware güncelle | StarLine Master (PC) |
| ix35 CAN firmware yükle | can.starline.ru |
| Fonksiyon tabloları | Manuel şanzıman, **F15=kapı kapanınca**, turbo timer kapalı |
| iKey öğrenme | 14× servis butonu + kontak |
| İlk program nötr testi | Motor çalışırken in → kapı kapat → motor durmalı |
| İlk uzaktan çalıştırma | Uygulamadan veya kumandadan |
| GSM testi | Evden telefonla çalıştır |

Kritik ayarlar: [sistem-mimarisi.md](sistem-mimarisi.md), otomasyon: [telefon-otomasyon.md](telefon-otomasyon.md)

**Bitti sayılır:** Kapı kapanınca motor duruyor; evden telefonla çalışıyor; klima devrede.

**Bu fazda pes eder misin?** iKey 4 bip verirse bağlantı hatası — forumda çözüm var ([ix35 obhod](https://support.starline.ru/communities/9/topics/85429-hyundai-ix35-ne-rabotaet-obhod)). Donanım doğruysa yazılım tarafı tekrarlanabilir.

---

## Faz 5 — Yaşa (alışkanlık)

**Ne yapıyorsun:** Günlük hayata geçiriyorsun.

| Hafta | Odak |
|-------|------|
| 1 | Akşam kapı-kapanınca ritüel |
| 1 | Sabah telefon veya Siri çalıştır |
| 2 | Siri cümlesi kaydet (sabah) |
| 2 | Normal park vs uzaktan park farkını içselleştir |

**Bitti sayılır:** Düşünmeden yapıyorsun; `araba/yapilanlar.md` güncellendi.

---

## [Opsiyonel] Faz 6 — Walk-away

Ayrı modül / SLAVE proximity. [uzaklasinca-otomatik-kilit.md](uzaklasinca-otomatik-kilit.md)

Uzaktan çalıştırma çalıştıktan sonra.

---

## Pes etme rehberi (dürüst)

| Durum | Pes et? | Alternatif |
|-------|---------|------------|
| can.starline.ru'da ix35 yok | Evet | — (ama var) |
| Kutu gelmedi / sahte ürün | Hayır | Başka satıcı |
| Kablo bağlantısı anlaşılmıyor | Hayır | Forum + bir gün mola |
| iKey öğrenmiyor | Hayır | Bağlantı kontrol + forum |
| Montaj seni aşıyor | **Belki** | Sadece Faz 3'ü ustaya ver, Faz 4–5 sen |
| "Her akşam telefonla uğraşırım" korkusu | Hayır | Fonksiyon 15 — telefon yok akşam |

---

## Hızlı referans

```
Akşam:  N + el freni → START bir kez → in → kapı kapat → motor durur
Sabah:  Telefon / Siri → çalıştır → 15 dk → bin → sür
```

---

*Son güncelleme: 2026-07-09*
