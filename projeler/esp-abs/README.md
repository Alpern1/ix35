# ESP + ABS — kısa ışık / bozuk yolda fren hissi

> Kırmızı ışıkta kalkışta metal şıkırtı + sarı ESP yanıp sönmesi; bozuk yolda frende ABS “tutmuyor” hissi.

## Durum

- **Durum:** 📋 Planlama (teşhis)
- **Öncelik:** Orta–yüksek (fren/stabilite; hâlâ yanıp sönmüyorsa acil değil ama bak)
- **Tahmini bütçe:** Teşhis ucuz; sensör/tone ring ~değişken
- **Zorluk:** Orta (göz + tarama; modül işi usta)
- **Oluşturulma:** 2026-09-02
- **Son güncelleme:** 2026-09-02 (dönen metal ses; lamba ≠ motor)

## Araç bilgisi (ortak)

[araba/ozellikler.md](../../araba/ozellikler.md) · [araba/notlar.md](../../araba/notlar.md) · [araba/bakim.md](../../araba/bakim.md)

## Olay (kullanıcı — 2026-09-02)

1. Kırmızı ışık, vites boş → 1’e attı, kalktı. Önünde araç var; çok ani kalkış değil.
2. Altından **metal şıkırtı**; gösterge **sarı ESP** yanıp söndü (~1–2 sn), sonra söndü. Başka bir şey yok.
3. Ayrı gözlem: titrek/bozuk yolda frene basınca ABS **düzgün tutmuyor** gibi (2016 Ibiza’da böyle hissetmemiş).
4. **2026-09-02 netleştirme:** Ses **dönen / çalışan** parçadan; alt sac / egzoz saçı değil (kullanıcı emin). Lamba ilk anda **motor arıza ışığı** sanıldı (“motor düştü / kırıldı”); aslında **sarı ESP** — motor check-engine değil. Ses “saçma” derecede ürkütücüydü.

## Lamba: motor değil

| | Motor (check engine) | ESP (bu olay) |
|--|----------------------|---------------|
| Tipik renk | Genelde turuncu/sarı motor ikonu | **ESP** yazısı / kayma ikonu (sarı) |
| Anlam | Motor/ECU | Teker hız / denge / çekiş |
| Bu olay | Değil | Kısa yanıp söndü |

Motor “kırılmış” senaryosu bu anlatımla **uyuşmuyor**: araç kalktı, lamba söndü, sonra normal devam.

## İki olayın alakası var mı?

**Olabilir — aynı donanım ailesi.** ESP ve ABS aynı **tekerlek hız sensörleri**, ton halkaları (ABS ring) ve genelde aynı **ABS/ESP beyni** üzerinden çalışır.

| Senaryo | ESP kısa + dönen metal ses | Bozuk yolda “ABS garip” | Birlikte mi? |
|---------|----------------------------|-------------------------|--------------|
| **A — ABS ton halkası çatlak / gevşek (bir numaralı şüphe)** | Halka dönerken metal şıkırtı + bozuk hız sinyali → ESP | Tümsekte sinyal daha kötü | **Evet — en iyi tek açıklama** |
| **B — Tekerlek hız sensörü / konnektör** | Ses zayıf; lamba güçlü | ABS hissi bozulur | Evet (ses ayrıysa A+B) |
| **C — Aks / CV (iç–dış mafsallar)** | Kalkışta metal tık/şık | ABS’yi doğrudan açıklamaz | Ses için aday; ESP için daha zayıf |
| **D — Porya / rulman** | Dönünce metal/uğultu | Dolaylı | Mümkün; genelde süreğen |
| **E — ESP/TCS kısa müdahale** | Lamba normal-ish; **sert metal ses açıklamaz** | Ayrı | Ses dönense E yetmez |
| **F — Alt sac / egzoz saçı** | — | — | **Elenmesi** (kullanıcı: dönen parça) |

**Ibiza karşılaştırması:** SUV + farklı ABS → bozuk yolda ABS daha sık keser; tek başına arıza değil. ESP + dönen metal + bu his → **ton halkası / sensör**.

**Acil değil (şimdi):** Lamba kalıcı değil, fren “yok” değil.  
**Acil say:** ESP/ABS sürekli, fren yumuşar, ses her kalkışta / hızlanınca tekrarlar.

## En olası teşhis sırası

1. **ABS ton halkası** (aks/göbek dişli çember) — çatlak, eksik diş, gevşek; dönerken şıkırtı + ESP klasik ikili.
2. **Tekerlek hız sensörü** ucu / fiş (çamur, oksit) — özellikle aynı teker.
3. **Aks / CV** — kalkışta metal; dönüşte de tıkırtı var mı diye dinle.
4. Porya rulmanı (süreğen uğultu/şıkırtı).
5. ABS beyni (en seyrek; önce 1–2).

## Sen nasıl teşhis edersin (DIY)

### 1) Tekrar say — 1 hafta

- ESP **bir daha** yanıyor mu? Hangi durumda (kalkış, tümsek, yağmur, sağ/sol dönüş)?
- Bozuk yolda frende: pedal **titriyor** (ABS kesiyor) mı, yoksa araç **kayar/uzar** mı?
- Metal ses **sadece o bir kalkışta** mı, yoksa her 1’den kalkışta / yavaş sürüşte de mi?
- Ses **ön mü arka mı, sağ mı sol mu?** (pencere açık kısa deneme, güvenli yer).

### 2) Arıza kodu oku (en kritik adım)

Basit “motor” OBD (ELM327 ucuz) **çoğu zaman ABS/ESP kodunu okumaz** — motor ışığı zaten yanmadığı için motor tarafında kod da beklenmez.

- Gerekli: **ABS/ESP okuyan** tarayıcı.
- Bakılacak: tekerlek hız sensörü / `C1xxx` (hangi köşe).
- Kod yok ama ses dönense → yine de **ton halkasını gözle** (aralıklı arıza kod bırakmayabilir).

### 3) Gözle (kriko + sehpalar)

1. Ön (ve gerekirse arka) tekerlerde aks/göbek **dişli ABS halkası**: kırık diş, çatlak, pas parçası, gevşeklik.
2. Aynı teker **hız sensörü** fişi ve uç–halka boşluğu (çok kirli / sürtme izi).
3. Lastik basınçları eşit.
4. ~~Egzoz saçı birincil şüphe değil~~ (dönen ses teyidi).

### 4) Yol testi (güvenli yer)

- Yumuşak 1’den kalkış tekrar: ses/lamba?
- Hafif dönüşlü kalkış: CV tıkırtısı?
- ESP tekrarlarsa taraf not et → tarama.

### 5) Yapma (şimdi)

- Motor açma / “motor kırıldı” paniğiyle parçaya saldırmak.
- ESP fişini çekmek.
- Kod/göz olmadan dört sensör birden.

## Sonraki adım (karar ağacı)

```
Dönen metal ses + kısa ESP (bu olay)
 └─ Öncelik: ABS ton halkası + sensör göz / ABS tarama
      ├─ Halka çatlak/diş eksik → halka (veya aks seti) + kod sil
      ├─ Sensör/fiş kötü → temizle/değiştir
      └─ Temiz + kod yok + bir daha olmaz → 1–2 hafta izle; ABS hissi ayrı not
```

## Açık sorular

- Ses / ESP tekrarlandı mı?
- Ön-arka / sağ-sol taraf netleşti mi?
- ABS tarama yapıldı mı?

## İlerleme

| Tarih | Not |
|-------|-----|
| 2026-09-02 | İlk olay; teşhis notu |
| 2026-09-02 | Ses dönen parça (saç değil); lamba motor sanıldı → ESP teyidi |

---

*Araç sabit bilgisi `araba/` altında; burada tekrarlanmaz.*
