# 🎴 FLASHCARDS - Demo: OCI AI Services

## VISION AI SERVICE - GENEL

### Kart 1
**Ön Yüz:** OCI Vision AI Service'in 4 ana özelliği (task) nedir?
**Arka Yüz:** 
1. Image Classification (Görüntü Sınıflandırma)
2. Object Detection (Nesne Tespiti)
3. Text Detection (Metin Tespiti - OCR)
4. Document AI (Belge Analizi)

---

### Kart 2
**Ön Yüz:** Confidence Score nedir?
**Arka Yüz:** 
AI'ın bir tahmininden ne kadar emin olduğunu gösteren yüzde değeri.
Örnek: %99.23 → AI %99.23 oranında emin

---

## IMAGE CLASSIFICATION

### Kart 3
**Ön Yüz:** Image Classification ne yapar ve çıktısı nedir?
**Arka Yüz:** 
**Ne Yapar:** Görüntüdeki nesneleri/kavramları tespit eder
**Çıktı:** Labels (etiketler) + Confidence Scores
**Örnek:** Zebra görüntüsü → Zebra, Animal, Vegetation, Grassland (her biri için skor)

---

### Kart 4
**Ön Yüz:** Tek bir görüntüye kaç label atanabilir?
**Arka Yüz:** 
Birden fazla label atanabilir. Her label'ın kendi confidence score'u vardır.
Örnek: Zebra görüntüsü → 5+ label (Zebra, Animal, Vegetation, Sky, Mammal)

---

## OBJECT DETECTION

### Kart 5
**Ön Yüz:** Object Detection ne yapar ve Image Classification'dan farkı nedir?
**Arka Yüz:** 
**Object Detection:** 
- Nesneleri tespit eder + konumlarını gösterir
- Bounding boxes (sınırlayıcı kutular) kullanır

**Fark:**
- Classification: "Bu görüntüde arabalar var" (genel)
- Detection: "5 araba var, burada, burada, burada" (spesifik konumlar)

---

### Kart 6
**Ön Yüz:** Bounding Box nedir ve hangi Vision AI özelliğinde kullanılır?
**Arka Yüz:** 
**Tanım:** Tespit edilen nesnelerin etrafına çizilen sınırlayıcı kutular
**Kullanım:** Object Detection
Her kutu için: Label + Confidence Score

---

### Kart 7
**Ön Yüz:** Object Detection demo'sunda trafik görüntüsünde neler tespit edildi?
**Arka Yüz:** 
- Çoklu arabalar (multiple cars)
- Taksi (taxi)
- Çoklu insanlar (multiple people)
Her biri bounding box ile işaretlendi

---

## TEXT DETECTION

### Kart 8
**Ön Yüz:** Text Detection (OCR) ne yapar?
**Arka Yüz:** 
Görüntüdeki yazılı metinleri tespit eder ve çıkarır.
**OCR:** Optical Character Recognition
**Örnekler:** Plaka okuma, belge dijitalleştirme, tabela okuma

---

### Kart 9
**Ön Yüz:** Text Detection demo'sunda otobüs görüntüsünde neler tespit edildi?
**Arka Yüz:** 
- Otobüs üzerindeki TÜM yazılar
- Plaka numarası: M32HOD
- Sayılar: 45
- Küçük text blokları bile tespit edildi

---

### Kart 10
**Ön Yüz:** Text Detection farklı fontları tespit edebilir mi?
**Arka Yüz:** 
Evet! Demo'da farklı fontlar (Arial, Arial Black vb.) başarılı şekilde tespit edildi.
Satır satır tarama yapılır.

---

## DOCUMENT AI

### Kart 11
**Ön Yüz:** Document AI'ın yeni adı nedir ve özellikleri değişti mi?
**Arka Yüz:** 
**Yeni Ad:** Document Understanding Service (Ayrı servis)
**Özellikler:** AYNI - Sadece servis ismi değişti
⚠️ Sınavda her iki isimle de karşılaşabilirsiniz!

---

### Kart 12
**Ön Yüz:** Document AI / Document Understanding ne yapar?
**Arka Yüz:** 
Yapılandırılmış belgeleri analiz eder ve veri çıkarır:
1. Raw Text (Ham metin)
2. Key-Value Pairs (Anahtar-değer çiftleri)
3. Table Extraction (Tablo çıkarma)

---

### Kart 13
**Ön Yüz:** Document AI demo'sunda fişten (receipt) çıkarılan Key-Value Pairs nelerdir?
**Arka Yüz:** 
- Transaction Date (İşlem Tarihi)
- Transaction Time (İşlem Zamanı)
- Subtotal (Ara Toplam)
- Tax (Vergi)
- Total (Toplam)
+ Satır satır key-value pair'ler

---

### Kart 14
**Ön Yüz:** Document AI table extraction yapabilir mi? Demo örneği?
**Arka Yüz:** 
Evet! Fiş örneğinde 3 tablo tespit edildi:
1. Ürün detayları tablosu
2. Toplam kısmı tablosu
3. Kart yetkilendirme (Terminal ID, Tutar) tablosu

---

### Kart 15
**Ön Yüz:** Document AI/Understanding'in kullanım alanlarını say.
**Arka Yüz:** 
- Fatura işleme otomasyonu
- Belge dijitalleştirme
- Veri girişi otomasyonu
- Invoice processing
- Form doldurma otomasyonu

---

## LANGUAGE AI SERVICE - GENEL

### Kart 16
**Ön Yüz:** OCI Language AI Service'in 2 ana özelliği nedir?
**Arka Yüz:** 
1. Text Analysis (Metin Analizi)
2. Text Translation (Metin Çevirisi)

---

### Kart 17
**Ön Yüz:** Text Analysis için kaç pretrained model vardır? İsimleri?
**Arka Yüz:** 
6+ Pretrained Model:
1. Language Detection
2. Text Classification
3. Sentiment Analysis
4. Entity Extraction
5. Key Phrase Extraction
6. PII Detection

---

## TEXT ANALYSIS DETAYLARI

### Kart 18
**Ön Yüz:** Language Detection ne yapar?
**Arka Yüz:** 
Metnin hangi dilde yazıldığını tespit eder.
Örnek: İngilizce, Türkçe, Fransızca vb.
Confidence score ile birlikte

---

### Kart 19
**Ön Yüz:** Text Classification ne yapar?
**Arka Yüz:** 
Metni kategorilere ayırır.
Demo Örneği: "Science and Technology" / "Computer-related"
Diğer kategoriler: Sports, Politics, Health vb.

---

### Kart 20
**Ön Yüz:** Entity Extraction ne yapar? Örnek ver.
**Arka Yüz:** 
Metindeki varlıkları (entities) çıkarır ve kategorize eder.

Demo Örnekleri:
- Food → Product
- Computers → Product
- Manual Instruments → Product
- World War II → Event

Her entity için confidence score

---

### Kart 21
**Ön Yüz:** Key Phrase Extraction ne yapar?
**Arka Yüz:** 
Metindeki anahtar kavramları/ifadeleri çıkarır.
Demo Örnekleri:
- "early computers"
- "simple manual instruments"

---

### Kart 22
**Ön Yüz:** Sentiment Analysis'in iki türü nedir?
**Arka Yüz:** 
1. **Aspect-Based Sentiment:** Konu/yön bazlı duygu analizi
   - Örnek: Food → Positive, Service → Negative
2. **Sentence Level Sentiment:** Cümle bazlı duygu
   - Her cümle için ayrı: Positive/Negative/Neutral

---

### Kart 23
**Ön Yüz:** Aspect-Based Sentiment nedir? Örnek ver.
**Arka Yüz:** 
Paragraftaki farklı konular için ayrı sentiment analizi.

Demo Örneği:
- **Aspect:** Food → Sentiment: Positive
- **Aspect:** Service → Sentiment: Negative
- **Aspect:** Early computers → Sentiment: Neutral

Her aspect için score ve Positive/Negative göstergesi

---

### Kart 24
**Ön Yüz:** PII Detection nedir ve neden önemlidir?
**Arka Yüz:** 
**PII:** Personal Identifiable Information (Kişisel Tanımlanabilir Bilgi)

**Ne Yapar:** Hassas bilgileri tespit eder
**Örnekler:** İsimler, tarihler, adresler, telefon

**Neden Önemli:** 
- GDPR compliance
- Veri güvenliği
- Hassas bilgi maskeleme

---

### Kart 25
**Ön Yüz:** PII Detection demo'sunda neler tespit edildi?
**Arka Yüz:** 
- "World War II" → Potansiyel hassas bilgi
- Tarihler → Potansiyel hassas bilgi
Uyarı: Bu bilgiler hassas olabilir

---

## TEXT TRANSLATION

### Kart 26
**Ön Yüz:** Text Translation özelliği nasıl çalışır?
**Arka Yüz:** 
**Source Language:** Kaynak dil seçilir (ör: English)
**Target Language:** Hedef dil seçilir (çoklu seçenek)
**Çeviri:** Saniyeler içinde tamamlanır

Demo: İngilizce → Fransızca, Japonca

---

## CUSTOM MODEL TRAINING

### Kart 27
**Ön Yüz:** OCI AI Services'de Custom Model Training yapılabilir mi?
**Arka Yüz:** 
Evet! Her iki serviste de (Vision & Language)

**Nasıl:**
1. Kendi verilerinizi (custom data) sağlarsınız
2. Kendi modelinizi eğitirsiniz
3. Özel ihtiyaçlarınıza göre sonuç alırsınız

---

## KARŞILAŞTIRMA KARTLARI

### Kart 28
**Ön Yüz:** Vision AI'da Image Classification vs Object Detection farkı?
**Arka Yüz:** 
**Image Classification:**
- "Bu görüntüde ne VAR?"
- Labels + Scores
- Konum bilgisi YOK

**Object Detection:**
- "NEREDE ve KAÇ TANE?"
- Bounding boxes + Labels + Scores
- Konum bilgisi VAR

---

### Kart 29
**Ön Yüz:** Text Detection vs Document AI farkı?
**Arka Yüz:** 
**Text Detection (OCR):**
- Sadece metin çıkarır
- Ham metin

**Document AI:**
- Metin + Yapı analizi
- Key-Value Pairs
- Table Extraction
- Yapılandırılmış veri

---

### Kart 30
**Ön Yüz:** Language AI hangi pratik senaryolarda kullanılır?
**Arka Yüz:** 
1. **Müşteri Hizmetleri:** Sentiment analysis
2. **Çoklu Dil Desteği:** Otomatik çeviri
3. **Compliance:** PII detection (GDPR)
4. **İçerik Yönetimi:** Otomatik sınıflandırma

---

### Kart 31
**Ön Yüz:** Vision AI hangi pratik senaryolarda kullanılır?
**Arka Yüz:** 
1. **E-ticaret:** Ürün kategorilendirme
2. **Güvenlik:** Plaka okuma, yüz tanıma
3. **Muhasebe:** Fiş/fatura otomasyonu
4. **Lojistik:** Paket/envanter takibi

---

## SINAV İPUÇLARI

### Kart 32
**Ön Yüz:** Document AI servis adı değişikliği - Sınavda dikkat!
**Arka Yüz:** 
**Eski:** Document AI (Vision Service içinde)
**Yeni:** Document Understanding Service (Ayrı servis)
**Özellikler:** TAMAMEN AYNI

⚠️ Sınavda her iki isimle de soru gelebilir!

---

### Kart 33
**Ön Yüz:** Vision AI - Hangi özellik hangi çıktıyı verir?
**Arka Yüz:** 
- **Image Classification** → Labels + Scores
- **Object Detection** → Bounding Boxes + Labels + Scores
- **Text Detection** → Ham Metin
- **Document AI** → Metin + Key-Value + Tables

---

### Kart 34
**Ön Yüz:** Language AI - 6 pretrained model'i hızlıca say!
**Arka Yüz:** 
1. Language Detection
2. Text Classification
3. Sentiment Analysis (2 tür!)
4. Entity Extraction
5. Key Phrase Extraction
6. PII Detection

---

## 📝 Çalışma Stratejisi

**Öncelik Sırası:**
⭐⭐⭐ Yüksek: Kart 1, 3, 5, 11, 16, 17, 22, 24
⭐⭐ Orta: Kart 12-15, 18-21, 26
⭐ Düşük: Senaryolar (30-31)

**Tekrar Planı:**
- Gün 1: Tüm kartlar
- Gün 2: Bilmediğiniz kartlar
- Gün 3: Hızlı genel tekrar