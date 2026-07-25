# Nasıl Çalışırız

> Bu dosya repo yapısını tanımlar. **Hatırlatmana gerek yok** — klasör yapısı kendini anlatır.

## Klasör ağacı

```
ix35/
├── README.md                 ← Giriş
├── NASIL-CALISIRIZ.md        ← Bu dosya (yapı sözleşmesi)
├── degisiklikler.md          ← Önemli değişiklik günlüğü
│
├── araba/                    ← ORTAK HAFIZA (tüm projeler buradan beslenir)
│   ├── README.md
│   ├── ozellikler.md         ← Sabit araç bilgisi
│   ├── notlar.md             ← Kısıtlar, tercihler, hatırlatmalar
│   └── yapilanlar.md         ← Fiziksel olarak yapılan işler
│
└── projeler/                 ← PROJELER (birbirinden izole)
    ├── README.md             ← Proje listesi
    ├── _sablon/              ← Yeni proje şablonu
    │   └── README.md
    ├── uzaktan-calisma-klima/    ← Proje 1
    │   ├── README.md             ← Ana proje dosyası
    │   ├── master-plan.md
    │   ├── kurulum-canli-anlatim.md
    │   └── … (sadece bu projeye ait)
    └── uzaklasinca-kilit/        ← Proje 2
        └── README.md
```

## Kurallar

### Araba bilgisi → `araba/`

| Ne | Nereye |
|----|--------|
| Model, motor, donanım, km | `araba/ozellikler.md` |
| LPG, manuel, DIY, bütçe, kısıtlar | `araba/notlar.md` |
| Yapılan mod / bakım | `araba/yapilanlar.md` |

Proje dosyalarında araç bilgisini kopyalama — `../../araba/` linki ver.

### Her proje → `projeler/<isim>/`

- Klasör adı: küçük harf, tire (`cam-filmi`, `multimedya`)
- **`README.md`** = ana proje (hedef, durum, kararlar)
- Diğer `.md` = o projeye özel araştırma / kurulum / plan
- **Başka proje klasörüne yazma**

### Yeni fikir geldiğinde

1. `araba/` oku
2. `projeler/README.md` — aynı proje var mı?
3. Yoksa: `_sablon/` kopyala → `projeler/<yeni-isim>/`
4. `projeler/README.md` + `degisiklikler.md` güncelle

### Proje bittiğinde

1. `README.md` durum → ✅
2. Özet → `araba/yapilanlar.md`

---

*Son güncelleme: 2026-07-10*
