# Nasıl Çalışırız — ix35 Repo Sözleşmesi

> Bu repo **arabanın hafızası** + **ayrı ayrı projeler** için.  
> Yeni fikir geldiğinde eski projelere dokunmadan ilerleriz.

---

## Üç katman

```
┌─────────────────────────────────────────────────────────┐
│  araba/          Arabanın kalıcı bilgisi (ortak hafıza) │
├─────────────────────────────────────────────────────────┤
│  projeler/       Her proje kendi dosyasında / klasöründe│
├─────────────────────────────────────────────────────────┤
│  degisiklikler   Neden değişti? (kısa günlük)           │
└─────────────────────────────────────────────────────────┘
```

### 1. `araba/` — Unutmayacağımız bilgiler

| Dosya | Ne zaman güncellenir |
|-------|----------------------|
| [ozellikler.md](araba/ozellikler.md) | Model, motor, donanım, km — **sabit gerçekler** |
| [notlar.md](araba/notlar.md) | LPG, manuel vites, DIY tercihi, kısıtlar |
| [yapilanlar.md](araba/yapilanlar.md) | Arabada **fiziksel olarak yapılan** her iş |

**Kural:** Proje dosyalarına araba özelliği kopyalamak yerine `araba/` dosyalarına yaz; projeler oraya link versin.

### 2. `projeler/` — Projeler birbirinden ayrı

Her **proje** = bir ana dosya (veya klasör + `README.md`).

| Tür | Örnek | Kural |
|-----|-------|-------|
| **Ana proje** | `uzaktan-calisma-ve-klima.md` | Hedef, durum, kararlar burada |
| **Destek / araştırma** | `telefon-kontrol-arastirma.md` | Sadece o projeye bağlı; listesi ana dosyada |
| **Yeni proje** | `projeler/<yeni-isim>.md` | Eski proje dosyalarına **dokunma** |

Proje listesi: [projeler/README.md](projeler/README.md)

### 3. Yeni fikir geldiğinde (sen + asistan)

```
1. araba/ozellikler.md + araba/notlar.md oku
2. projeler/README.md — aynı proje var mı bak
3. Yoksa: _sablon.md kopyala → yeni proje dosyası
4. projeler/README.md listesine ekle
5. degisiklikler.md kısa not
6. Eski proje dosyalarını değiştirme (sadece yeni dosya)
```

**Senin cümlen:** *"Aklımda yeni bir şey var: …"*  
**Beklenen:** Yeni `projeler/xxx.md` açılır; StarLine / walk-away dosyalarına karışılmaz.

---

## Proje grupları (şu an)

| # | Proje | Ana dosya | Durum |
|---|-------|-----------|-------|
| 1 | Uzaktan çalıştırma & klima (StarLine) | [uzaktan-calisma-ve-klima.md](projeler/uzaktan-calisma-ve-klima.md) | 📋 Planlama |
| 2 | Uzaklaşınca otomatik kilit | [uzaklasinca-otomatik-kilit.md](projeler/uzaklasinca-otomatik-kilit.md) | 📋 Planlama |

Proje 1'in destek dosyaları (kurulum, tedarik, karşılaştırma…) ana dosyada listelenir — ayrı proje sayılmaz.

---

## Tamamlanan iş

Proje bittiğinde:

1. Proje dosyasında durum → ✅ Tamamlandı  
2. Özet + parça/maliyet → `araba/yapilanlar.md`  
3. Arabaya kalıcı etki varsa → `araba/ozellikler.md` veya `notlar.md`

---

## Şablon

Yeni proje: [projeler/_sablon.md](projeler/_sablon.md) kopyala.

Dosya adı: küçük harf, tire — ör. `cam-filmi.md`, `jant-boyama.md`

---

*Son güncelleme: 2026-07-10*
