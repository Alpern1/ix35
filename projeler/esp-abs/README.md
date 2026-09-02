# ESP + ABS — kısa ışık / bozuk yolda fren hissi

> Kırmızı ışıkta kalkışta metal şıkırtı + sarı ESP yanıp sönmesi; bozuk yolda frende ABS “tutmuyor” hissi.

## Durum

- **Durum:** 📋 Planlama (teşhis)
- **Öncelik:** Orta–yüksek (fren/stabilite; hâlâ yanıp sönmüyorsa acil değil ama bak)
- **Tahmini bütçe:** Teşhis ucuz; sensör/tone ring ~değişken
- **Zorluk:** Orta (göz + tarama; modül işi usta)
- **Oluşturulma:** 2026-09-02
- **Son güncelleme:** 2026-09-02

## Araç bilgisi (ortak)

[araba/ozellikler.md](../../araba/ozellikler.md) · [araba/notlar.md](../../araba/notlar.md) · [araba/bakim.md](../../araba/bakim.md)

## Olay (kullanıcı — 2026-09-02)

1. Kırmızı ışık, vites boş → 1’e attı, kalktı. Önünde araç var; çok ani kalkış değil.
2. Altından **metal şıkırtı**; gösterge **sarı ESP** yanıp söndü (~1–2 sn), sonra söndü. Başka bir şey yok.
3. Ayrı gözlem: titrek/bozuk yolda frene basınca ABS **düzgün tutmuyor** gibi (2016 Ibiza’da böyle hissetmemiş).

## İki olayın alakası var mı?

**Olabilir — aynı donanım ailesi.** ESP ve ABS aynı **tekerlek hız sensörleri**, ton halkaları (ABS ring) ve genelde aynı **ABS/ESP beyni** üzerinden çalışır.

| Senaryo | ESP kısa yanma + şıkırtı | Bozuk yolda “ABS garip” | Birlikte mi? |
|---------|--------------------------|-------------------------|--------------|
| **A — Sensör / ton halkası kir-çatlak (en mantıklı ilk şüphe)** | Yanlış hız sinyali → ESP kısa müdahale + lamba | Tümsekte teker kalkınca sinyal daha kötü → ABS fazla/az keser | **Evet** |
| **B — ESP/TCS kısa müdahale (normal-ish)** | Kalkışta bir teker kaydı sandı → lamba 1–2 sn | Ayrı konu | Kısmen |
| **C — Metal ses ayrı (egzoz saçı / muhafaza / CV)** | Ses saçı; lamba sensör | ABS hissi ayrı veya aynı | Ses ≠ ESP olabilir |
| **D — Fren hidroliği / disk-balata** | Tek başına ESP kısa ışığı açıklamaz | Pedal hissi + titreşim | Dolaylı |

**Ibiza karşılaştırması:** SUV (ix35) + farklı ABS kalibrasyonu + süspansiyon → bozuk yolda ABS **daha sık devreye girer**; bu tek başına arıza demek değil. Ama ESP olayı + bu his **birlikte** → sensör/ton halkasına bak.

**Acil değil (şimdi):** Lamba kalıcı yanmıyor, fren “yok” demiyor, sürekli ESP yok.  
**Acil say:** ESP/ABS **sürekli** yanıyor, fren yumuşuyor, bir teker kilitleniyor/kayma hissi artıyor.

## En olası teşhis sırası

1. **Tekerlek hız sensörü veya ABS ton halkası** (kir, oksit konnektör, çatlak diş) — özellikle bir ön teker.
2. Gevşek **egzoz ısı kalkanı** / alt muhafaza (şıkırtı için; ESP’siz de olur).
3. Aks / CV (kalkışta metal; genelde dönüşte de tıkırtı).
4. ABS beyni / hidrolik ünite (daha seyrek; önce 1).

## Sen nasıl teşhis edersin (DIY)

### 1) Tekrar say — 1 hafta

- ESP **bir daha** yanıyor mu? Hangi durumda (kalkış, tümsek, yağmur, sağ/sol dönüş)?
- Bozuk yolda frende: pedal **titriyor** (ABS kesiyor) mı, yoksa araç **kayar/uzar** mı?
- Metal ses **sadece kalkışta** mı, yoksa yavaşlarken/boşta da mı?

### 2) Arıza kodu oku (en kritik adım)

Basit “motor” OBD (ELM327 ucuz) **çoğu zaman ABS/ESP kodunu okumaz**.

- Gerekli: **ABS/ESP okuyan** tarayıcı (Launch, Thinkcar, Carman, usta cihazı, bazı Foxwell vb.).
- Bakılacak: `C1xxx` / tekerlek hız sensörü kodları (ör. sağ ön, sol ön…).
- Kod **yok** ama semptom var → yine de halka/sensör gözle; aralıklı arıza kod bırakmayabilir.

Kayseri: Usta / elektrikçi 5 dk ABS tarama yeterli; parça değiştirmeden önce kod.

### 3) Gözle (sehpa / kriko + sehpalar)

Araç güvenli kaldırılmışken (sehpa şart):

1. Her tekerlekte **ABS sensör konnektörü** — yeşil/oksit, gevşek, su izi.
2. Sensör ucu / ton halkası (disk arkası veya aks üzerindeki dişli halka): **kırık diş, pas topağı, çamur**.
3. Altına bak: egzoz **ısı kalkanı** el ile sallanıyor mu → şıkırtı adayı.
4. Lastik basınçları **eşit** mi (ESP yanlış kayma sanır).

### 4) Yol testi (güvenli yer)

- Düz asfalt, ılık motor: yumuşak 1’den kalkış → ses/lamba?
- Bilinçli hafif tümsekli yol: frende pedal titreşimi **beklenen ABS** olabilir.
- ESP bir daha yanarsa: **hemen** hangi teker tarafı (sağ/sol his) not et; tarama yaptır.

### 5) Yapma (şimdi)

- ESP’yi fişten kesme / lamba söndürme “çözümü”.
- Kod okumadan dört sensör birden değiştirme.
- “Ibiza gibi değil” diye ABS’yi arızalı sayıp beyni söktürme.

## Sonraki adım (karar ağacı)

```
ESP bir daha yandı veya ABS “fren yok” gibi uzuyor mu?
 ├─ EVET → ABS tarama (kod) + ton halkası/sensör göz
 └─ HAYIR (tek seferlik) → 1–2 hafta izle; yine de basınç + alt muhafaza bak
        └─ Bozuk yolda sadece pedal titreşimi → çoğu zaman normal ABS
```

## Açık sorular

- ESP tekrarlandı mı?
- Metal ses hangi taraftan (ön/arka, sağ/sol)?
- Elde ABS okuyan cihaz / usta var mı?

## İlerleme

| Tarih | Not |
|-------|-----|
| 2026-09-02 | İlk olay anlatıldı; teşhis notu açıldı |

---

*Araç sabit bilgisi `araba/` altında; burada tekrarlanmaz.*
