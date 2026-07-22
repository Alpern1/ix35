# Projeler

> Her proje **kendi klasöründe**. Yeni fikir = yeni klasör. Eski klasörlere dokunulmaz.

## Durum

| Durum | Anlamı |
|-------|--------|
| 💡 Fikir | Henüz sadece konuşuldu |
| 📋 Planlama | Araştırma / plan |
| 🔧 Devam ediyor | Uygulama |
| ✅ Tamamlandı | Bitti → `araba/yapilanlar.md` |
| ❄️ Donduruldu | Ertelendi |
| ❌ İptal | Yapılmayacak |

## Aktif projeler

| Klasör | Proje | Durum | Öncelik |
|--------|-------|-------|---------|
| [uzaktan-calisma-klima/](uzaktan-calisma-klima/) | Uzaktan çalıştırma & klima (StarLine GSM ECO) | 📋 Planlama | Yüksek |
| [uzaklasinca-kilit/](uzaklasinca-kilit/) | Uzaklaşınca otomatik kilit (walk-away) | 📋 Planlama | Orta |
| [yazilim-kodlama/](yazilim-kodlama/) | Yazılım / BCM kodlama / chip — ne yapılabilir? | 💡 Fikir | Orta |
| [koltuk-sogutma/](koltuk-sogutma/) | Koltuk soğutma / havalandırma (OEM görünüm) | 💡 Fikir | Orta |

Her klasörde **`README.md`** = ana proje dosyası. Diğer `.md` dosyaları o projeye özel destek dokümanlarıdır.

## Yeni proje

```bash
cp -r projeler/_sablon projeler/<yeni-isim>
# projeler/<yeni-isim>/README.md doldur
# Bu tabloya satır ekle
# degisiklikler.md not düş
```

Şablon: [_sablon/README.md](_sablon/README.md)

---

*Son güncelleme: 2026-07-22*
