# Kullanım Senaryoları — İnme & Binme

> Manuel vites + Smart Key + START/STOP + StarLine A93 v2 2CAN+2LIN
> **Akşam:** telefon yok — kapı kapanınca program nötr biter (Fonksiyon 15)
> **Sabah:** telefon veya Siri ile çalıştır

---

## Temel kural

| Durum | Ne yaparsın |
|-------|-------------|
| **Uzaktan çalıştırma istediğin park** | Program nötr prosedürü (A) |
| **İstemiyorsan** | Normal in: START/STOP ile kapat (B) |
| **Sabah evden** | Telefon / Siri / uygulama kısayolu |

Detay: [telefon-otomasyon.md](telefon-otomasyon.md)

---

## A) ARAÇTAN İNME — uzaktan çalıştırmaya hazırlık

### Sistem yokken (şu an)

```
Park → vites boş → el freni → START/STOP → motor KAPANIR → in
```

### Sistem kurulduktan sonra (önerilen akış)

Kurulumda **Fonksiyon 15 = kapı kapanınca** (veya kapı + 20 sn gecikme) ayarlı:

```
1. Yere park et
2. Vitesi BOŞA al, el frenini ÇEK
3. Debriyaj ve frenden ayağını çek
4. START/STOP'a BİR KEZ bas (pedallara basmadan)
   → Motor ÇALIŞIR KALMALI; durursa kurulum hatası
5. İn — smart key cebinde (kısa uyarı normal)
6. Kapıyı KAPAT
7. Motor KENDİ KAPANIR → program nötr tamam → uzaktan çalıştırmaya hazır
```

**Telefondan "güvenlik kur" yok.** Kapı kapanması yeterli.

### Alternatif bitiş yolları (kurulumda seçilir)

| Yol | Ne yaparsın |
|-----|-------------|
| **Kapı kapanınca** (önerilen) | Sadece kapıyı kapat |
| Fabrika KİLİT tuşu (SLAVE) | Kapat → smart key'den kilitle |
| Telefon / Siri | İstemezsen kurma — yedek |

---

## B) NORMAL PARK (uzaktan çalıştırma yok)

```
Park → vites boş → el freni → START/STOP (motor kapanır) → in
```

---

## C) SABAHA — evden çalıştırma

```
1. StarLine uygulaması → "Çalıştır" (veya Siri: kayıtlı cümle)
2. Motor benzinle çalışır (Prins)
3. Klima son ayarda devreye girer
4. 10–15 dk bekle → araca git
```

Kapalı garajda asla.

---

## D) ARACA BİNME

```
1. Kilidi aç (telefon, kumanda veya smart key)
2. Bin — motor rölantide
3. FRENE bas
4. START/STOP bir kez (devralma)
5. Debriyaj → vites → sür
```

---

## E) Walk-away (ayrı proje, sonra)

Uzaktan çalıştırma akışından bağımsız. Bkz. [uzaklasinca-otomatik-kilit.md](uzaklasinca-otomatik-kilit.md).

---

## F) Özet döngü

```
[Sürüş] → [Park: N + el freni]
       → [START/STOP bir kez, pedalsız]
       → [İn, kapı kapat, motor durur]
           → [Sabah: telefon/Siri çalıştır]
           → [Bin, fren, START/STOP devral, sür]
```

---

## G) Sık sorular

| Soru | Cevap |
|------|-------|
| Her akşam telefonla güvenlik kur? | **Hayır** — kapı kapanınca biter |
| START/STOP bir kez basmak zorunda mıyım? | Push-start'ta evet — kontak simülasyonu; motor açık kalmalı |
| Sabah telefon şart mı? | Evden çalıştırma için evet (veya Siri) |
| Kumanda START 2.5 sn? | Bu sistemde yok |

---

*Son güncelleme: 2026-07-09*
