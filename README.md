# ix35 — Araba Projeleri

Bu repo, **2012 Hyundai ix35** için kalıcı araba bilgisi ve **birbirinden ayrı proje planları** tutar. Sohbetler kaybolur; dosyalar kalır.

## Nasıl çalışıyoruz?

Detaylı akış: **[NASIL-CALISIRIZ.md](NASIL-CALISIRIZ.md)**

```
araba/     → Arabanın hafızası (özellikler, notlar, yapılanlar)
projeler/  → Her proje ayrı dosya; yeni fikir = yeni dosya
```

**Yeni bir şey aklına gelince:** *"Aklımda yeni bir şey var: …"* de — eski projelere karışmadan yeni proje dosyası açılır, araba bilgileri `araba/` klasöründen okunur.

## Klasör yapısı

| Dosya / Klasör | Ne için? |
|----------------|----------|
| [NASIL-CALISIRIZ.md](NASIL-CALISIRIZ.md) | Repo sözleşmesi — sen + asistan nasıl ilerler |
| [araba/](araba/) | Arabanın sabit bilgileri, kısıtlar, yapılan işler |
| [projeler/README.md](projeler/README.md) | Tüm projelerin listesi |
| [projeler/_sablon.md](projeler/_sablon.md) | Yeni proje şablonu |
| [degisiklikler.md](degisiklikler.md) | Önemli değişiklik günlüğü |

## Aktif projeler (özet)

| # | Proje | Dosya |
|---|-------|-------|
| 1 | Uzaktan çalıştırma & klima (StarLine) | [projeler/uzaktan-calisma-ve-klima.md](projeler/uzaktan-calisma-ve-klima.md) |
| 2 | Uzaklaşınca otomatik kilit | [projeler/uzaklasinca-otomatik-kilit.md](projeler/uzaklasinca-otomatik-kilit.md) |

## Yeni proje eklemek

1. `projeler/_sablon.md` → `projeler/<proje-adi>.md`
2. `projeler/README.md` listesine ekle
3. `degisiklikler.md` kısa not
