# Canlı Kurulum Anlatımı — Kutu Geldi, Araç Başındayız

> **Sistem:** StarLine A93 v2 2CAN+2LIN GSM ECO  
> **Araç:** 2012 Hyundai ix35 · 1.6 GDI · Smart Key · **Manuel** · Prins LPG  
> **Kim:** Sen + bu rehber (montajcı yok)  
> **Süre:** 3 gün — Cuma hazırlık · Cumartesi kablo · Pazar yazılım + test  

Bu dosyayı **yanında açık tut**. Her adımı sırayla yap; atlama. Kutunun yanında, arabada, laptop başında okuyacaksın.

---

## Bu rehberin kullanımı

```
□ Bir adımı bitir → kutudaki kutuyu işaretle
□ "BAŞARILI SAY" maddesini görmeden sonraki adıma geçme
□ Her bağlantıdan sonra FOTO çek (telefon albümü: "ix35 StarLine")
□ Şüphede multimetre — renge güvenme
□ Sarı airbag kablosuna DOKUNMA
```

**Altın kural:** `can.starline.ru` şeması ile bu rehber çelişirse **şemayı dinle**.

---

# BÖLÜM 0 — KUTU KAPIDA / SALONDA (Gün 0)

*Saat: Kargo geldi. Henüz araca dokunmuyoruz.*

## Adım 0.1 — Kutuyu aç

**Elinde:** Bıçak veya makas, temiz zemin (masa).

1. Kutuyu yatay koy, bantları kes.
2. Üstteki straforu çıkar.
3. İçeriği **tek tek** masaya koy — karıştırma.

**Başarılı say:** Aşağıdaki tablodaki her satır masada.

## Adım 0.2 — Envanter (eksikse kurma)

| # | Parça | Nasıl tanırsın | Kutuda? |
|---|-------|----------------|---------|
| 1 | Ana ünite | Siyah dikdörtgen kutu, ~10×8 cm, çok kablo çıkışı | □ |
| 2 | 2CAN+2LIN modülü | Daha küçük kutu, üzerinde micro-USB | □ |
| 3 | Ana kablo demeti | Kalın siyah kablo, uçlarda X1/X2/X3… konnektörler | □ |
| 4 | GSM anteni | İnce koaksiyel kablo + küçük siyah çubuk | □ |
| 5 | LCD bröle (ana kumanda) | Ekranlı, StarLine yazılı | □ |
| 6 | İkinci bröle | Yedek / basit | □ |
| 7 | Siren | Küçük hoparlör, 2 kablo | □ |
| 8 | Servis (vale) düğmesi | Küçük push buton, 2 kablo | □ |
| 9 | Sıcaklık sensörü | İnce kablo + metal prob | □ |
| 10 | Kaput switch (hood pin) | Uzun pimli, 2 kablo | □ |
| 11 | Montaj vidası / cırt / pabuç | Zıp | □ |
| 12 | Kısa kullanım kılavuzu | Kağıt | □ |
| 13 | SIM yuvası bilgisi | GSM ECO’da nano-SIM gerekir | □ |

**Eksik varsa:** Foto çek → satıcıya yaz → **kuruluma başlama.**

## Adım 0.3 — Salon masasında “tanışma” (30 dk)

**Elinde:** Ana ünite, CAN modülü, laptop (henüz güç yok).

1. Ana ünitenin üzerindeki etiketi oku: **A93 v2 2CAN+2LIN** yazmalı.
2. CAN modülünü eline al — micro-USB girişini bul.
3. Ana kablo demetindeki büyük konnektörü ana üniteye **tak-çıkar** alıştırması yap (akü bağlı değil, zararsız).
4. Bröleyi eline al — pil var mı kontrol et (kapağı açma, sallama yeter).

**Başarılı say:** Parçaların ne olduğunu adıyla söyleyebiliyorsun.

## Adım 0.4 — Laptop hazırlığı (akşam, 1 saat)

**Neredesin:** Ev, masa, internet var.

1. Tarayıcıda aç: https://help.starline.ru/slm  
2. **StarLine Master** indir → kur (Windows).
3. Tarayıcıda aç: https://can.starline.ru  
4. Yol: **Hyundai** → **ix35** → **2010–2013** veya **2012** → **Start-Stop** (кнопка).
5. Çıkan sayfada:
   - Bağlantı şemasını **PDF indir**
   - Firmware listesinde **Ready** (yeşil/hazır) sürümü not et
   - Sayfa numarasını veya kodunu yaz (ör. forumda 2012 için `7382` geçiyor — sende farklı olabilir, **sitedeki güncel Ready’yi seç**)
6. PDF’i telefona at (WhatsApp kendine).
7. Telefona **StarLine 2** uygulamasını kur.
8. nano-SIM al (henüz takma) — PIN kodunu **kapat**.

**Başarılı say:** Laptop’ta StarLine Master açılıyor; telefonda PDF şema var.

---

# BÖLÜM 1 — CUMA AKŞAMI (Gün 1): Arabayı tanı, henüz kesme yok

*Saat: ~2 saat. Araç park halinde. Akü takılı.*

## Adım 1.1 — Alet çantası

**Çantaya koy:**

- Multimetre (+ pil dolu)
- Plastik trim sökme takımı
- Tornavida seti (PH1, PH2, düz)
- Kıskaç seti
- İzolasyon bandı, zip tie, etiket bandı / kalem
- LED fener veya telefon flaş
- Powerbank + laptop şarj
- Bu PDF + telefon şema

## Adım 1.2 — Sigorta kutusu (ilk temas)

**Neredesin:** Sürücü koltuğu, kapı açık.

1. Otur, sol ayağını pedale koy.
2. Direksiyonun **sol altına** bak — plastik dikdörtgen kapak görürsün.
3. Üst kenardan parmağınla çek — **tık** sesi normal.
4. Kapağı çıkar, **iç yüzündeki şemayı fotoğrafla**.
5. Sigortaları sayma — sadece şu etiketleri bul:
   - SMART KEY (26)
   - MODULE 5 (18)
   - CLUSTER (6)
6. Kapağı **geri tak**.

**Başarılı say:** Sigorta kutusunu 30 saniyede açıp kapatabiliyorsun.

## Adım 1.3 — OBD bul

**Neredesin:** Sürücü koltuğu, başını direksiyon altına eğ.

1. Sol tarafta **trapez siyah 16 pinli** soket ara.
2. Bulunca foto çek.
3. Dokunma — sadece yerini öğren.

## Adım 1.4 — Sol alt trim alıştırması

**Neredesin:** Sürücü kapı eşiği.

1. Plastik sökme aleti ile sol alt panelin alt kenarına gir.
2. Nazikçe kaldır — 2–3 klips çıkar.
3. **Kablo kesme yok** — sadece sök-tak.
4. İçeride kablo demetleri görürsün — foto.
5. Paneli geri tak.

**Başarılı say:** Trim kırılmadan sökülüp takıldı.

## Adım 1.5 — Fren pedalı switch

**Neredesin:** Sürücü ayağı fren pedalında.

1. Pedalın **üstüne** elini sok (motor soğukken).
2. Küçük **beyaz 4 pinli** konnektör ara — fren linkine gider.
3. Foto çek — yarın buraya dokunacaksın.

## Adım 1.6 — Cuma bitiş

Arabaya **hiçbir StarLine parçası takma**. Sadece keşif.

```
□ Sigorta foto
□ OBD foto
□ Trim içi foto
□ Fren switch foto
□ Yorgunsan iyi — yarın asıl iş
```

---

# BÖLÜM 2 — CUMARTESİ SABAH (Gün 2): Güvenlik ve masaüstü firmware

*Saat 08:00. Garaj veya düz zemin. Hava açık.*

## Adım 2.1 — Akü eksiyi sök

**Elinde:** 10 mm anahtar veya lokma.

1. Kaputu aç.
2. Akünün **eksi (-)** kutup başını bul (genelde siyah kablo).
3. Somunu gevşet → kabloyu **çıkar**.
4. Eksi kabloyu yan tarafa koy — **metal temas etmesin**.
5. Kaputu kapat (yağmur yoksa açık bırakılabilir).

**Başarılı say:** Eksi kablo tamamen sökük. İç lambalar yanmıyor.

> **Neden:** Kısa devre ve yanlışlıkla marş riskini sıfırlar.

## Adım 2.2 — Parçaları araca taşı

Kutudaki her şeyi arka koltuya veya temiz bez üstüne koy. Bröle cebinde kalsın.

## Adım 2.3 — Laptop: CAN modülü firmware (akü hâlâ sökük)

**Neredesin:** Ön yolcu koltuğu veya arka koltuk, laptop açık.

1. **2CAN modülünü** eline al.
2. micro-USB ile laptop’a bağla.
3. **StarLine Master** aç.
4. Menüden CAN modül / firmware güncelleme bölümünü bul.
5. `can.starline.ru`’da not ettiğin **ix35 Start-Stop Ready** firmware’i seç → yükle.
6. “Başarılı” yazana kadar bekle — kabloyu çekme.
7. USB’yi çıkar.

**Başarılı say:** StarLine Master firmware yüklemeyi onayladı.

**Takılırsan:** Farklı USB kablo dene; Windows sürücü izni ver.

## Adım 2.4 — Ana üniteyi geçici yerleştir

**Neredesin:** Sürücü ayak boşluğu, trim sökülmeden.

1. Ana üniteyi **henüz vida delme** — cırt veya zip ile geçici sabitle (direksiyon altı görünür yer, geçici).
2. CAN modülünü ana üniteye montaj klipsi ile tak (kılavuzdaki gibi).
3. Ana kablo demetini ana üniteye tak.

**Başarılı say:** Ana ünite + CAN modülü birlikte, gevşek ama bağlı.

---

# BÖLÜM 3 — CUMARTESİ: Gösterge ve CAN (en kritik bölüm)

*Saat 09:30. Eksi hâlâ sökük.*

## Adım 3.1 — Gösterge çerçevesini sök

**Elinde:** Plastik sökme aleti.

1. Direksiyonu **aşağı indir** (kolon kilidi).
2. Gösterge çerçevesinin üst/alt kenarından plastik aleti sok.
3. Yavaşça çevreleyerek klipsleri çöz — **anında çekme**, sırayla.
4. Çerçeveyi çıkar, cam yüzeyi çizme.
5. Arkada kablo demetleri ve konnektörler görünür.

**Başarılı say:** Gösterge camı yerinde, çerçeve çıkmış, airbag kapağına dokunmadın.

**DİKKAT:** **Sarı** veya **turuncu** kablo demetleri = airbag. Uzaktan dur.

## Adım 3.2 — CAN şemasını aç

**Elinde:** Telefon (PDF şema), multimetre.

1. Şemada **“подключение CAN”** / CAN bağlantı bölümünü bul.
2. Hangi konnektör yazıyorsa not et (ix35’te çoğu kurulumda **sol gösterge / kombinasyon** demeti).
3. Şemadaki pin numarası + kablo rengi not et — **örnek:** “pin 6 CAN-H, pin 14 CAN-L” (sende farklı olabilir).

## Adım 3.3 — CAN pinlerini multimetre ile doğrula

**Akü eksisi hâlâ sökük** — CAN ölçümü için bazen kontak gerekir; önce şemayı oku.

1. Kontak gerekiyorsa: **geçici olarak** eksi kabloyu 5 dk tak → ölç → tekrar sök.  
   VEYA push-start’ta fren basılı + START’a bir kez bas (ACC) — **motor çalıştırma**.
2. Multimetre **DC 20V**.
3. Şemadaki CAN-H ve CAN-L pinlerine prob dokundur — referans: şasi toprak.
4. CAN hatlarında idle voltaj genelde **2–3 V** civarı oynar (araç uyanıkken).
5. **Yanlış pin** = sigorta patlar veya garip değer — o zaman dur, şemaya dön.

**Başarılı say:** İki pin (H ve L) şemayla eşleşti, ölçüm mantıklı.

## Adım 3.4 — CAN kablolarını bağla

**Elinde:** StarLine CAN modülünden çıkan CAN-H, CAN-L (veya tek 4'lü demet).

1. Şemada **ekleme yöntemi** yazar: konnektör arkasına pin ekleme veya hazır T-harness.
2. **Orijinal pini çıkarma** — StarLine genelde konnektörün arkasına ek pin sokar.
3. CAN-H → bulduğun H pinine
4. CAN-L → bulduğun L pinine
5. Her bağlantıyı tırnakla sık, hafif çek testi.
6. Etiket yapıştır: “CAN-H”, “CAN-L”.
7. **Foto.**

**Başarılı say:** CAN bağlı, gevşek yok, airbag hattına değmedi.

## Adım 3.5 — Çerçeveyi geri tak (geçici)

CAN testi pazar günü. Şimdilik çerçeveyi yerine oturt — tam klipsleme yapılabilir.

---

# BÖLÜM 4 — CUMARTESİ ÖĞLE: Güç ve toprak

*Saat 12:00.*

## Adım 4.1 — Sürekli +12V (Kırmızı / kılavuzdaki renk)

**Şemada:** “+30”, “постоянный плюс”, “constant +12V”.

1. Sigorta kutusunu aç (Adım 1.2).
2. Multimetre ile sigorta çıkışlarını ölç — **kontak kapalıyken de 12V** olan hat = sürekli +12V adayı.
3. Şemada hangi sigorta yazıyorsa onu kullan veya uygun add-a-fuse / sigorta tap.
4. StarLine ana demetindeki **sürekli +12V** kablosunu bağla.
5. **Sigorta tap kullanıyorsan:** Orijinal sigorta amperine uygun — genelde 10–15A.

**Başarılı say:** Kontak kapalıyken bile StarLine sürekli hat kablosunda 12V ölçüyorsun (eksi takılıyken ölçemezsin — bağlantıyı görsel kontrol).

## Adım 4.2 — Kontak +12V (ACC)

**Şemada:** “+15”, “при включенном зажигании”.

1. **Geçici eksi tak** (ölçüm için) veya yardımcı.
2. Kontak kapalı → 0V; ACC açık (START’a bir basış) → 12V olan hat bul.
3. StarLine **kontak +12V** kablosunu bağla.
4. Foto + etiket.

**Başarılı say:** ACC açılınca 12V, kapanınca 0V.

## Adım 4.3 — Toprak (şasi)

1. Temiz metal gövde noktası bul (fabrika toprak cıvatası — sürücü kick paneli civarı).
2. Cıvata altını hafif zımpara — boya kalksın.
3. Siyah toprak kablosunu sıkı bağla — sallanınca oynamasın.

**Başarılı say:** Toprak kablosu sıkı, metal temas iyi.

---

# BÖLÜM 5 — CUMARTESİ ÖĞLEDEN SONRA: Analog sinyaller

*Saat 14:00.*

## Adım 5.1 — Fren pedalı

**Neden:** ix35’te fren sinyali CAN’da yok — uzaktan marş için şart.

1. Fren switch konnektörünü bul (Cuma foto).
2. Şemada hangi pin **fren basılında +12V** veya ground pulse — oku.
3. Multimetre: fren basılı / basılı değil farkını gör.
4. StarLine’ın **fren** giriş kablosunu bağla (genelde mavi veya şemada “тормоз”).
5. **Kes-yapıştır yerine** konnektör arkasına pin tercih et.

**Başarılı say:** Fren basınca multimetre değişiyor; bağlantı sabit.

## Adım 5.2 — Debriyaj (manuel)

1. Debriyaj pedalı switch’ini bul (fren gibi küçük konnektör).
2. Şemada “сцепление” / clutch varsa bağla.
3. Yoksa StarLine Master’da manuel ayarda debriyaj bypass seçeneğini not et — pazar günü yazılımda aç.

## Adım 5.3 — El freni

1. El freni çekili/bırakıldı switch (konsol veya BCM’de).
2. Şema istiyorsa bağla — manuel güvenlik için önemli.

## Adım 5.4 — Kaput switch (hood pin)

1. Kaput kenarında montaj noktası seç — kapak kapanınca pin basılir.
2. Delik aç veya mevcut klips — **kısa devre yapma**.
3. İki kablo: biri toprak, biri StarLine hood girişi.
4. Kaput açık → devre açık; kapalı → kapalı.

**Test:** Eli ile pimi sık — multimetre bip.

**Başarılı say:** Kaput kapanınca switch kapanıyor.

## Adım 5.5 — Servis (vale) düğmesi

1. Sürücü altında gizli ama erişilir yere monte et (trim arkası).
2. İki kablo ana üniteye “VALET” girişine.
3. Gizli tut — hırsız kolay bulmasın.

**Başarılı say:** Düğmeye basınca ileride programlama moduna girebileceksin (pazar).

## Adım 5.6 — Siren

1. Motor bölmesinde su almayan nokta — ön panel arkası.
2. Siren ağzı aşağı veya yan (su birikmez).
3. İki kablo şemaya göre.

---

# BÖLÜM 6 — CUMARTESİ AKŞAM: Güç hatları (push-start immo)

*Saat 17:00. En dikkatli bölüm.*

## Adım 6.1 — Kick panel aç

1. Sol alt trimi tamamen sök.
2. BCM’ye giden **kalın beyaz konnektörleri** gör.
3. Şemadaki **“подключение по силе”** / güç bağlantı sayfasını aç.

## Adım 6.2 — ACC, IGN1, IGN2, START bul

**Yöntem (forum önerisi):**

1. Şemada **anahtarlı** aynı araç BCM pinout’una bak.
2. Kendi arabanda aynı pin numaralarını multimetre ile bul:
   - ACC: kontak açık, motor kapalı → 12V
   - IGN: kontak açık → 12V
   - START: START düğmesine basılı tut → 12V (kısa süre)
3. **Renk uyuşmazlığı normal** — pin numarası önemli.

## Adım 6.3 — StarLine güç çıkışlarını bağla

StarLine’ın röleli güç modülü / mavi-sarı çıkışları şemaya göre:

- ACC çıkışı → ACC hattı
- IGN çıkışları → IGN hatları  
- START → START hattı

**Her bağlantıdan sonra etiket + foto.**

**Başarılı say:** Tüm güç hatları şemadaki gibi — henüz akü takılı değil.

## Adım 6.4 — Sıcaklık sensörü

1. Motor bölmesinde enjektör borusu veya şemadaki noktaya prob sık.
2. Kablo güvenli şekilde içeri geçir (conta delme mümkünse kullan).

## Adım 6.5 — GSM anteni

1. Anteni **henüz gizleme** — geçici cam üstü / torpido test.
2. Kablo ana ünite GSM girişine.

## Adım 6.6 — Cumartesi kapanış

```
□ Tüm kablolar zip tie ile toparlandı
□ Trim parçaları yerinde (gevşek olabilir)
□ Not defteri: "CAN pin X, sürekli +12V sigorta Y, fren pin Z"
□ Akü EKSİ hâlâ sökük — gece böyle bırak OK
□ Foto galerisi 20+ kare
```

**Bugün marş deneme — HAYIR.**

---

# BÖLÜM 7 — PAZAR SABAH: Akü, iKey, yazılım

*Saat 09:00.*

## Adım 7.1 — Akü eksiyi tak

1. Eksi kabloyu kutbaşa oturt.
2. Somunu sık — el gücü + biraz daha, aşırı değil.

**Başarılı say:** İç lamba yanar, kumanda çalışır.

## Adım 7.2 — StarLine Master — araç profili

**Laptop ön koltukta, USB ile ana üniteye bağlan** (kılavuzdaki programlama kablosu veya Bluetooth adaptör varsa ona göre).

1. StarLine Master → cihazı bul.
2. Araç: **Hyundai ix35**
3. Yıl: **2012**
4. Tip: **Start-Stop (кнопка)**
5. Vites: **МКПП / Manuel**
6. Ayarları kaydet.

## Adım 7.3 — iKey öğrenme (ix35 — CopyKey YOK)

**Resmi forum prosedürü:**

1. Motor kapalı, vites boş, el freni çekili.
2. **Servis (vale) düğmesine 14 kez** hızlıca bas (1–2 sn aralık).
3. Fren pedalına bas (push-start prosedürü).
4. **START/STOP’a bir kez bas** — kontak açılsın, **motoru çalıştırma**.
5. İki kısa siren/bip = **iKey öğrenildi**.
6. Olmazsa: 14 vale tekrar, internet bağlantısı kontrol (bazı modüllerde gerekir).

**Başarılı say:** İki kısa onay sesi / Master’da iKey OK.

## Adım 7.4 — Manuel vites güvenlik ayarları

StarLine Master → Tablo 2 / otomotiv ayarları:

```
□ Vites tipi: МКПП (Manuel)
□ Programlı nötr: AÇIK
□ El freni kontrolü: AÇIK
□ Debriyaj kontrolü: şemana göre
□ Uzaktan marş süresi: 15 dk (900 sn)
□ Kapı açılınca motor dursun: AÇIK
□ Kaput açıkken marş yok: AÇIK
```

Kaydet → modüle gönder.

---

# BÖLÜM 8 — PAZAR: İlk marş (bröle ile)

*Saat 11:00. Açık alan. Komşu rahatsız olmasın.*

## Adım 8.1 — Güvenlik kontrolü

```
□ Kaput kapalı ve hood pin OK
□ Vites N (boş) — kolu sallayarak hisset
□ El freni çekili
□ Debriyaj bırakılmış
□ Anahtar cebinde (smart key)
□ Kimse önde kaputta değil
```

## Adım 8.2 — Programlı nötr / rezervasyon

Manuel vites StarLine’da tipik akış:

1. Motor çalışıyorken veya prosedüre göre: vites N, el freni.
2. Brölede **programlı nötr** kombinasyonu (kılavuz: genelde uzun basış veya ⏱ tuşu 3 sn).
3. Motor stop olur, sistem silahlanır.
4. **Kapı kapanınca** motor kapalı kalır — güvenli mod.

*Tam tuş kombinasyonu bröle modeline göre kılavuzda — StarLine A93 kılavuz Tablo 1.*

## Adım 8.3 — Bröleden ilk marş

1. Bröle ekranında motor simgesi / START.
2. **2 sn bas** — motor kalkmalı.
3. Dörtlü veya park lambası yanıp sönebilir — normal.
4. **Durdur** — bröleden stop.

**5 kez tekrarla.**

**Başarılı say:** 5/5 marş ve stop.

**Olmazsa:**

| Belirti | Bak |
|---------|-----|
| Tık yok | START/IGN güç hatları |
| Tık var, çalışmıyor | iKey tekrar |
| Çalışıp ölüyor | Fren/debriyaj sinyali |

---

# BÖLÜM 9 — PAZAR ÖĞLE: GSM ve telefon

*Saat 13:00.*

## Adım 9.1 — SIM kart

1. Ana ünite kapağını aç (kılavuzdaki yuva).
2. **nano-SIM** tak — çip aşağı, kesik köşe hizalı.
3. SIM PIN telefonda **kapalı** olmalı.

## Adım 9.2 — APN (gerekirse)

StarLine Master → GSM → APN:

| Operatör | APN |
|----------|-----|
| Turkcell | internet |
| Vodafone | internet |
| Türk Telekom | internet |

Kaydet. Modül yeniden başlasın (1–2 dk).

## Adım 9.3 — StarLine 2 uygulama

1. Uygulamayı aç → hesap oluştur / giriş.
2. **Cihaz ekle** — QR veya seri no (kutu/kart).
3. Bağlantı için **GSM** seç (sadece Bluetooth değil).
4. Durum ekranı gelene kadar bekle (2–5 dk).

**Başarılı say:** Uygulamada araç görünüyor, “bağlı” veya son durum zamanı güncel.

## Adım 9.4 — Evden kilitle testi

1. Telefonu **WiFi kapat**, mobil veri aç.
2. Evden veya aracın 100 m uzağından:
   - Uygulamada **kilitle (silahlan)** → kapılar kilit sesi duyulmalı (yakınsan)
   - **Kilidi aç** → dene
3. Durum ekranında güvenlik modu değişimini gör.

**Başarılı say:** Uzaktan kilitle/aç çalışıyor.

---

# BÖLÜM 10 — PAZAR ÖĞLEDEN SONRA: Uzaktan marş testi

*Saat 15:00. Açık alan.*

## Adım 10.1 — Klima hazırlığı

1. Motor çalışırken klima **AUTO**, 24°C ayarla.
2. Normal prosedürle kapat / programlı nötr ile silahla.
3. Uygulamadan **uzaktan marş** bas.
4. 2–3 dk bekle — fan üflemesi veya motor sesi.

## Adım 10.2 — 10’lu test

| # | Uzaktan START | Uzaktan STOP | Kapı açılınca stop? |
|---|---------------|--------------|---------------------|
| 1 | □ | □ | □ |
| 2 | □ | □ | □ |
| … | | | |
| 10 | □ | □ | □ |

**Hedef:** 10/10 marş.

## Adım 10.3 — Güvenlik testleri

```
□ Kaput açıkken marş BAŞLAMAMALI
□ Vites 1. vitesteyken (kontrollü) uzaktan marş DENEME — başlamamalı
□ 15 dk sonra motor kendini durduruyor mu
```

---

# BÖLÜM 11 — PAZAR AKŞAM: Toparlama

*Saat 17:00.*

## Adım 11.1 — Kalıcı montaj

1. Ana üniteyi kalıcı gizli noktaya sabitle (cırt + vida).
2. Tüm trim klipsleri oturana kadar bastır.
3. Gösterge çerçevesi tam otursun.
4. Gevşek kablo kalmasın.

## Adım 11.2 — Bröle öğren

1. StarLine Master → bröle kayıt.
2. İkinci bröleyi de kaydet (yedek).

## Adım 11.3 — Son foto + not

```
Kurulum tarihi: __________
Firmware kodu: __________
Başarılı uzaktan marş: __ / 10
Sorunlar: __________
```

---

# GÜNLÜK KULLANIM — Her parktan sonra

```
1. Vites N
2. El freni çek
3. Programlı nötr / rezervasyon (bröle)
4. Çık → StarLine 2 ile kilitle VEYA bröle
5. Ertesi gün evden marş / kilitle
```

**Unutursan:** Marş çalışmaz — arıza değil, güvenlik.

---

# ACİL GERİ ALMA

Her şey ters giderse:

1. Akü eksiyi sök.
2. StarLine kablolarını sök (foto sırasına göre ters).
3. Orijinal konnektörler boş kaldı — araç fabrika haline döner.
4. Foruma foto + firmware kodu ile yaz.

---

# KAYNAKLAR (yanında açık tut)

| Ne | Link |
|----|------|
| CAN şema + firmware | https://can.starline.ru |
| StarLine Master | https://help.starline.ru/slm |
| ix35 2012 DIY forum | https://support.starline.ru/communities/10/topics/62980-hyundai-ix35-2012-knopka-start-stop |
| ix35 2014 DIY (benzer) | https://support.starline.ru/communities/10/topics/41978-starline-a93-2can2lin-na-hyundai-tucson-ix35-2014-start-stop |
| Güç bağlantı 2012 | https://support.starline.ru/communities/10/topics/24327-ix35-2012g-podklyuchenie-po-sile |
| StarLine 2 uygulama | App Store / Play |

---

# HIZLI GÜN ÖZETİ

| Gün | Nerede | Ne |
|-----|--------|-----|
| **0** | Salon | Kutu envanter, laptop yazılım |
| **1 Cuma** | Araba (kesme yok) | Sigorta, OBD, trim keşif |
| **2 Cumartesi** | Araba | Akü eksiyi sök → CAN → güç → fren → kaput → BCM güç |
| **3 Pazar** | Araba + laptop | Akü tak → iKey → marş test → GSM → uzaktan test → gizle |

---

*Son güncelleme: 2026-07-09 — StarLine A93 GSM ECO · ix35 2012 manuel push-start*
