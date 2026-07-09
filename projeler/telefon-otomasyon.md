# Program Nötr & Silahlanma — Otomasyon Seçenekleri

> "Telefondan güvenlik kur" adımı saçma geliyorsa — haklısın. Çözüm **kurulum ayarında**; telefon opsiyonel kalır.
> Son güncelleme: 2026-07-09

---

## Sorunun özü

Program nötr (manuel vites güvenlik prosedürü) **bir "silahlanma olayı" ile biter**. Bu olay şunlardan biri olabilir:

- Telefon uygulaması
- Fabrika smart key KİLİT tuşu (SLAVE modu)
- Kapı kapanması (Fonksiyon 15 ayarı) ← **en temiz çözüm**
- StarLine kumandası
- SMS / Telegram bot

**Telefon zorunlu değil.** Daha önce telefonu ana yol diye yazmamız, Compustar alternatifinden kalan alışkanlıktı. StarLine'da kurulumda başka bitiş seçilir.

---

## Çözüm A — Kapı kapanınca otomatik (ÖNERİLEN)

StarLine **Fonksiyon 15** (programlama tablosu №2):

| Varyant | Ne olur |
|---------|---------|
| V1 | Silahlanınca biter (telefon/kumanda/fabrika kilit) |
| **V2** | **Kapı kapanınca biter** |
| **V3** | **Kapı kapanınca + 20 sn gecikme** (eşya almak için süre) |

**V2 veya V3 seçilirse akış:**

```
Park → vites boş + el freni
→ (push-start) START/STOP'a BİR KEZ bas, pedallar boş — motor çalışır kalır
→ in → kapıyı kapat
→ motor KENDİ DURUR + program nötr tamamlanır
→ telefona dokunmadın
```

Push-start'ta START'a **bir kez** basma: StarLine forumunun push-start açıklaması — kontağı simüle eder, motor durmamalı. Pedallara basılmaz.

**Kurulumda iste:** Fonksiyon 15 = **V2** (kapı) veya **V3** (kapı + 20 sn).

---

## Çözüm B — Fabrika kilit tuşu (SLAVE modu)

**SLAVE modu** açıksa: fabrika smart key'den **KİLİT** basınca StarLine da silahlanır.

```
Motor çalışırken in → kapı kapat → fabrika kumandadan KİLİT (zaten yaptığın şey)
→ motor durur, program nötr biter
```

Telefon yok. Zaten her gün kilit basıyorsan ekstra adım yok.

**Kurulumda iste:** SLAVE modu açık + SUPER SLAVE / tag (güvenlik için).

---

## Çözüm C — Telefon / ses (sabah çalıştırma için)

Akşam ritüelde telefon **gerekmez**. Sabah evden çalıştırma için telefon (veya ses) kullanılır — bu zaten istediğin şey.

### StarLine uygulaması — yerleşik Siri

StarLine resmi olarak **Siri entegrasyonu** sunuyor ([starline.ru/assistant](https://www.starline.ru/starline-assistant-instructions/)):

| Uygulama içi komut | Örnek Siri cümlesi |
|--------------------|-------------------|
| Güvenlik kur | "Siri, arabayı kilitle" (kendi kaydettiğin cümle) |
| Çalıştır | "Siri, arabayı çalıştır" |
| Durdur | "Siri, arabayı durdur" |

**Kurulum:** StarLine 2 uygulaması → Ayarlar → Siri ses kontrolü → komut seç → cümle kaydet.

**Not:** Bu, iOS **Kestirmeler** uygulamasından ayrı — StarLine kendi Siri köprüsünü kullanıyor (uygulama v5.5+).

### StarLine uygulaması — uygulama içi kısayollar

App Store açıklaması: *"Sık kullanılan komutlar için kısayol oluştur"* — ana ekranda tek dokunuş.

### Telegram bot

StarLine'ın resmi Telegram botu var — silahlanma ve çalıştırma komutları. iPhone'da Telegram bildiriminden tek dokunuş.

### iOS Kestirmeler (Shortcuts) — sınırlar

| Yöntem | Akşam (program nötr) | Sabah (çalıştır) |
|--------|----------------------|------------------|
| Fonksiyon 15 kapı | ✅ Gerek yok | — |
| StarLine Siri | Opsiyonel | ✅ "Hey Siri, çalıştır" |
| iOS Kestirmeler otomasyonu | ⚠️ StarLine URL şeması yok | Siri üzerinden dolaylı |
| Konum tetikleyici + Siri | Teorik ama güvenilmez | Evden çıkınca çalıştır riskli |

**Sonuç:** iPhone Kestirmeler ile **doğrudan** StarLine API çağrısı yok. En iyi yol:
1. Akşam → Fonksiyon 15 (telefon yok)
2. Sabah → StarLine Siri veya uygulama widget/kısayol

İstersen sabah için Kestirmeler'de **"Siri'ye söyle"** adımı koyabilirsin — ama StarLine'ın kendi Siri kaydı daha basit.

---

## Önerilen günlük akış (nihai)

### Akşam (uzaktan çalıştırma hazırlığı)

```
Park → N + el freni
→ START/STOP bir kez (pedalsız, motor açık kalır)
→ in → kapı kapat
→ [Fonksiyon 15 V2/V3: motor durur, N hazır]
```

Telefon, kumanda, güvenlik kur — **hiçbiri**.

### Sabah

```
Seçenek 1: StarLine uygulama kısayolu — tek dokunuş
Seçenek 2: "Hey Siri, [kayıtlı cümle]" — eller serbest
Seçenek 3: Telegram StarLine bot
```

---

## Kurulumda montajcıya / kendine yazılacak not

```
Fonksiyon 15 = V2 veya V3 (kapı kapanınca program nötr bitsin)
Fonksiyon 12 = push-start uyumlu kontak desteği
Şanzıman = Manuel (МКПП)
SLAVE = açık (yedek: fabrika kilit tuşu da çalışsın)
Turbo timer = kapalı
```

---

## İlgili dosyalar

- [kullanim-senaryolari.md](kullanim-senaryolari.md) — günlük akış
- [sistem-mimarisi.md](sistem-mimarisi.md) — fonksiyon tablosu
- [master-plan.md](master-plan.md) — uygulama fazları

---

*Son güncelleme: 2026-07-09*
