# Kullanım Senaryoları — İnme & Binme

> Sistem kurulu ve çalışıyor varsayımıyla. Manuel vites + Smart Key + START/STOP.
> **Kontrol tercihi: telefon (evden).** Aftermarket kumanda START tuşu günlük ritüelde **kullanılmaz**.
> Referans sistem: **StarLine A93 v2 2CAN+2LIN + GSM/LTE** (ix35/Tucson kanıtlı yol).

---

## Temel kural

| Durum | Ne yaparsın |
|-------|-------------|
| **Uzaktan çalıştırma istediğin her park** | Program nötr + telefondan silahlanma (A prosedürü) |
| **Uzaktan çalıştırma istemediğin park** | Normal in: START/STOP ile kapat |
| **Evden çalıştırma** | Sadece telefon uygulaması |
| **Yakın mesafe yedek** | StarLine kumandası veya telefon (opsiyonel; zorunlu değil) |

**Önemli düzeltme (2026-07-09):** Daha önce yazılan *"kumanda START 2.5 sn"* adımı **Compustar/Fortin** yoluna özgüydü. Senin istediğin **telefon-only** akış StarLine **program nötr** prosedürüyle uyumludur; günlük kullanımda aftermarket kumandaya basmana gerek yok.

---

## A) ARAÇTAN İNME — uzaktan çalıştırmaya hazırlık

### Şu an yaptığın (sistem yokken)

```
Yere park → Vites boş → El freni → START/STOP → motor KAPANIR → İn
```

### Sistem kurulduktan sonra (uzaktan çalıştırma istediğin her park)

Kurulumcunun **Fonksiyon 12 = "El freni ile"** veya **"Otomatik"** olarak ayarladığı StarLine program nötr prosedürü:

```
1. Yere park et
2. Vitesi BOŞA al
3. El frenini ÇEK
4. Debriyaj ve frenden ayağını çek
5. START/STOP'a BASMA ❌  (motoru sen kapatmıyorsun; rölantide kalır)
6. Araçtan İN — smart key cebinde/çantanda
   → Araç kısa süre uyarı verebilir (anahtar içeride algısı); bu normal
7. Kapıyı KAPAT
8. Telefonda StarLine uygulamasından "Güvenlik kur" / "Koruma aç" komutunu ver
   (veya kurulumda ayarlandıysa: fabrika kumandayla kilitleme = SLAVE modu)
9. Motor KENDİ KAPANIR + kapılar KİTLENİR + uygulamada "N" (nötr hazır) ikonu görünür
```

**START/STOP'a basmayacaksın.** Motor çalışırken inip kapıyı kapatıyorsun; silahlanma komutu gelince sistem motoru durdurup uzaktan çalıştırmaya hazırlıyor.

### Neden böyle?

Manuel viteslerde fabrikada "vites boşta mı?" sensörü yok. StarLine **program nötr** şunu doğrular: "Motor çalışırken güvenli şekilde çıktın → vites boş kabul edilir." Bu, dünya genelinde manuel vites uzaktan çalıştırmanın standart güvenlik prosedürüdür.

### Kumanda START tuşu ne zaman devreye girer?

| Yöntem | Günlük ritüelde gerekli mi? |
|--------|----------------------------|
| Telefon → Güvenlik kur | **Evet — bu senin ana yolun** |
| StarLine LCD kumanda → silahlanma | Hayır (yedek) |
| Kumanda START 2.5 sn (Compustar) | **Hayır — bu sistemde yok** |

Kurulumda **Fonksiyon 12 = "El freni ile"** seçilirse: motor çalışırken el freni zaten çekiliyse prosedür sadece "in → kapat → telefondan silahlan" olur. **"Otomatik"** seçilirse sistem CAN üzerinden kontağı simüle kapatır (push-start araçlarda anahtar çıkarma yerine geçer); yine START/STOP'a basmazsın.

### Unutursan ne olur?

| Hata | Sonuç |
|------|-------|
| START/STOP ile motoru kendin kapattın | Program nötr yapılmadı → sabah uzaktan çalışmaz |
| Kapıyı kapatmadan silahlandın | Prosedür yarım → uzaktan çalışmaz |
| Silahlandıktan sonra kapıyı tekrar açtın | Program nötr iptal → A prosedürünü baştan yap |
| El freni çekili değil | Uzaktan çalıştırma veya silahlanma reddedilir |

---

## B) SABAHA / UZAKTAN ÇALIŞTIRMA (evden, telefondan)

```
1. StarLine uygulamasını aç (GSM/LTE — menzil sınırı yok)
2. "Çalıştır" (Start)
3. Motor çalışır (benzinle — Prins böyle başlar)
4. Klima son bıraktığın ayarda devreye girer (AUTO + sıcaklık)
5. Dörtlüler yanıp söner (çalışıyor göstergesi)
6. 10–15 dakika sonra araca git (üst sınır: 15–20 dk — yağ seyreltmesi riski)
```

**Kapalı garajda asla çalıştırma.**

---

## C) ARACA BİNME (uzaktan çalıştırılmış araç)

```
1. Telefon veya StarLine kumandası ile kilidi AÇ
2. Kapıyı aç — motor çalışıyor (rölantide)
3. Bin (smart key cebinde)
4. FRENE bas
5. START/STOP'a BİR KEZ bas (devralma — motor çalışmaya devam eder)
6. Debriyaja bas → vitese al → sür
```

Frene basmadan vitese alma. START/STOP'a basmak burada **devralma** — motoru kapatmıyor, kontrolü sana veriyor.

---

## D) NORMAL PARK (uzaktan çalıştırma istemiyorsan)

```
Yere park → Vites boş → El freni → START/STOP → motor KAPANIR → İn
```

Bu gecede uzaktan çalıştırma **yok** — bilinçli tercih. Ertesi sabah uzaktan çalıştırmak istersen o gün A prosedürünü uygula.

---

## E) Walk-away otomatik kilit (ayrı özellik)

Walk-away, uzaktan çalıştırma prosedüründen **bağımsız** bir özelliktir:

```
Normal inersin (START/STOP ile kapatırsın)
Anahtar cebinde ~1,5 m uzaklaşırsın → kapılar kilitlenir (modül kuruluysa)
Geri gelirsin → kapılar açılır
```

**Uzaktan çalıştırma günü** yine Bölüm A prosedürünü yaparsın; walk-away o akışı değiştirmez.

Walk-away için ayrı modül veya StarLine SLAVE + proximity ayarı gerekir — ayrı proje dosyasına bak: [uzaklasinca-otomatik-kilit.md](uzaklasinca-otomatik-kilit.md).

---

## F) Özet döngü (telefon-only)

```
[Sürüş]
  → [Park: boş vites + el freni, motor AÇIK]
  → [İn, kapı kapat]
  → [Telefon: Güvenlik kur]
  → [Motor durur, N hazır]
      → [Evden telefon: Çalıştır]
      → [Bin, frene bas, START/STOP devral, sür]
```

---

## G) Sık karışan noktalar

| Soru | Cevap |
|------|-------|
| İnerken START/STOP'a basar mıyım? | **Hayır** — telefondan silahlan |
| Aftermarket kumanda START gerekir mi? | **Hayır** — evden kontrol telefon |
| Motor çalışırken iner miyim? | **Evet** — kısa süre; silahlanınca durur |
| Anahtar cebimdeyken araç ötüyor? | Normal; kapı kapanınca ve silahlanınca düzen oturur |
| Binerken START/STOP? | **Evet** — frene bastıktan sonra bir kez (devralma) |
| Her gün aynı mı? | Uzaktan çalıştırma istediğin her parkta **evet** — A prosedürü |

---

*Son güncelleme: 2026-07-09*
