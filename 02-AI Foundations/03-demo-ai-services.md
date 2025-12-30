# 📚 GÜN 1: Demo - OCI AI Services - Detaylı Çalışma Notu

## 🎯 Modül Özeti
Bu demo, Oracle Cloud Infrastructure (OCI) AI servislerinin pratik kullanımını gösteriyor. İki ana servis: **Vision AI** ve **Language AI**

---

## 👁️ OCI VISION AI SERVICE

### 4 Ana Özellik (Task)

#### 1. **Image Classification (Görüntü Sınıflandırma)**

**Ne Yapar:** Görüntüdeki nesneleri/kavramları tespit eder ve etiketler (labels)

**Demo Örnekleri:**

**Örnek 1: Doğa Görüntüsü**
- **Label:** Vegetation (Bitki örtüsü)
- **Confidence Score:** 99.23%
- **Anlam:** AI %99.23 oranında bu görüntüde bitki örtüsü olduğundan emin

**Örnek 2: Zebra Görüntüsü**
- **Labels:** Zebra, Vegetation, Grassland, Plant, Animal
- Her biri için confidence score (güven skoru) verilir

**Örnek 3: İki Zebra**
- **Labels:** Zebra, Animal, Vegetation, Sky, Mammal

**💡 Önemli:** Tek bir görüntüye birden fazla label atanabilir. Her label'ın confidence score'u vardır.

---

#### 2. **Object Detection (Nesne Tespiti)**

**Ne Yapar:** Görüntüdeki nesneleri tespit eder ve **bounding boxes (sınırlayıcı kutular)** ile işaretler

**Demo Örnekleri:**

**Örnek 1: Trafik Görüntüsü**
- **Tespit Edilenler:**
  - Çoklu arabalar (multiple cars)
  - Taksi (taxi)
  - Çoklu insanlar (multiple people)
- Her nesne için:
  - Bounding box (kutu)
  - Label (etiket)
  - Confidence score

**Örnek 2: Meyve Sepeti**
- **Tespit Edilenler:**
  - Orange (Portakal)
  - Banana (Muz)
  - Apple (Elma)
  - Bowl (Kase)

**💡 Fark:** Image Classification vs Object Detection
- **Classification:** "Bu görüntüde arabalar var" (genel)
- **Detection:** "Bu görüntüde 5 araba var, burada, burada ve burada" (spesifik konumlar)

---

#### 3. **Text Detection (Metin Tespiti - OCR)**

**Ne Yapar:** Görüntüdeki yazılı metinleri tespit eder ve çıkarır (OCR - Optical Character Recognition)

**Demo Örnekleri:**

**Örnek 1: Otobüs Görüntüsü**
- **Tespit Edilenler:**
  - Otobüs üzerindeki tüm yazılar
  - Plaka numarası: **M32HOD**
  - Sayılar: **45**
  - Küçük text blokları bile tespit edildi

**Örnek 2: Farklı Font'lar**
- **Test:** Farklı fontlarda yazılmış metinler
- **Sonuç:** 
  - Arial font tespit edildi
  - Arial Black tespit edildi
  - Satır satır tarama yapıldı

**💡 Kullanım Alanları:**
- Plaka okuma
- Belge dijitalleştirme
- Tabela okuma

---

#### 4. **Document AI (Belge Analizi)**

**⚠️ Önemli Not:** Document AI artık ayrı bir servise taşındı: **Document Understanding Service**
- Özellikler aynı kaldı
- Sadece servis ismi değişti

**Ne Yapar:** Belgeleri (özellikle yapılandırılmış belgeler) analiz eder ve veri çıkarır

**Demo Örneği: Fatura (Receipt) Analizi**

**1. Raw Text (Ham Metin) Çıkarma:**
- Fiş üzerindeki TÜM metinler okundu
- "Receipt" kelimesinden "Thank you"ya kadar her şey

**2. Key-Value Pairs (Anahtar-Değer Çiftleri) Çıkarma:**
- **Transaction Date** (İşlem Tarihi)
- **Transaction Time** (İşlem Zamanı)
- **Subtotal** (Ara Toplam)
- **Tax** (Vergi)
- **Total** (Toplam)
- Satır satır key-value pair'ler çıkarıldı

**3. Table Extraction (Tablo Çıkarma):**
- **3 tablo tespit edildi:**
  - Tablo 1: Ürün detayları
  - Tablo 2: Toplam kısmı
  - Tablo 3: Kart yetkilendirme kodu, Terminal ID, Tutar

**💡 Kullanım Alanları:**
- Fatura işleme otomasyonu
- Belge dijitalleştirme
- Veri girişi otomasyonu
- Invoice processing

---

## 🗣️ OCI LANGUAGE AI SERVICE

### 2 Ana Özellik

#### 1. **Text Analysis (Metin Analizi)**

**Pretrained Models (Önceden Eğitilmiş Modeller):**
1. Language Detection (Dil Tespiti)
2. Text Classification (Metin Sınıflandırma)
3. Sentiment Analysis (Duygu Analizi)
4. Entity Extraction (Varlık Çıkarma)
5. Key Phrase Extraction (Anahtar İfade Çıkarma)
6. PII Detection (Kişisel Bilgi Tespiti)

---

**Demo Örneği: Teknoloji Metni Analizi**

**1. Language Detection:**
- **Tespit Edilen Dil:** English
- **Confidence Score:** Yüksek

---

**2. Text Classification:**
- **Kategori:** Science and Technology / Computer-related
- Metin teknoloji ve bilgisayar ile ilgili olarak sınıflandırıldı

---

**3. Entity Extraction (Varlık Çıkarma):**
- **Tespit Edilen Entities:**
  - Food (Yiyecek)
  - Computers (Bilgisayarlar)
  - Manual Instruments (Manuel Aletler)
- **Tags (Etiketler):**
  - Product (Ürün)
  - Event (Olay)
  - Diğer kategoriler
- Her entity için **confidence score**

---

**4. Key Phrase Extraction:**
- **Çıkarılan Anahtar İfadeler:**
  - "early computers"
  - "simple manual instruments"
  - Metindeki önemli kavramlar

---

**5. Sentiment Analysis (Duygu Analizi)**

**a) Aspect-Based Sentiment (Yön Bazlı Duygu):**
- **Aspect:** Paragraftaki bir konu/özne
- **Örnekler:**
  - Food → Sentiment (Pozitif/Negatif/Nötr)
  - Service → Sentiment
  - Early computers → Sentiment
- Her aspect için:
  - Score (Skor)
  - Positive/Negative (Pozitif/Negatif)

**b) Sentence Level Sentiment (Cümle Seviyesi Duygu):**
- Her cümle için ayrı sentiment
- **Demo'da:** Negative veya Neutral

---

**6. PII Detection (Personal Identifiable Information - Kişisel Bilgi Tespiti):**
- **Tespit Edilenler:**
  - "World War II" → Potansiyel hassas bilgi
  - Tarihler → Potansiyel hassas bilgi
- **Uyarı:** Bu bilgiler hassas olabilir

**💡 Kullanım Alanları:**
- GDPR compliance
- Veri güvenliği
- Hassas bilgi maskeleme

---

#### 2. **Text Translation (Metin Çevirisi)**

**Özellikler:**
- **Source Language:** Kaynak dil (örn: English)
- **Target Language:** Hedef dil (çoklu seçenek)
- Saniyeler içinde çeviri

**Demo Örneği:**

**Kaynak:** İngilizce metin

**Hedef 1: French (Fransızca)**
- Birkaç saniyede çevrildi

**Hedef 2: Japanese (Japonca)**
- Başarılı şekilde çevrildi

**💡 Desteklenen Diller:** Çoklu dil seçeneği var

---

### Custom Model Training (Özel Model Eğitimi)

**Özellik:** Kendi verilerinizle özel model eğitebilirsiniz

**Nasıl Çalışır:**
- Custom data (özel veri) sağlarsınız
- Kendi modelinizi eğitirsiniz
- Özel ihtiyaçlarınıza özel sonuçlar

**Nerede Kullanılır:** Her iki serviste de (Vision & Language)

---

## 🎯 ÖZET TABLO - OCI AI SERVİSLERİ

### Vision AI Service

| Özellik | Ne Yapar | Çıktı | Örnek Kullanım |
|---------|----------|-------|----------------|
| **Image Classification** | Görüntü etiketleme | Labels + Confidence | Görüntü kategorilendirme |
| **Object Detection** | Nesne tespiti | Bounding boxes + Labels | Trafik analizi, envanter |
| **Text Detection** | OCR | Metinler | Plaka okuma, belge dijitalleştirme |
| **Document AI** | Belge analizi | Text + Key-Value + Tables | Fatura işleme, form doldurmayı otomatikleştirme |

---

### Language AI Service

| Özellik | Ne Yapar | Örnek |
|---------|----------|-------|
| **Language Detection** | Dil tespiti | English, Turkish vb |
| **Text Classification** | Metin kategorilendirme | Technology, Sports vb |
| **Sentiment Analysis** | Duygu analizi | Positive/Negative/Neutral |
| **Entity Extraction** | Varlık çıkarma | Person, Location, Organization |
| **Key Phrase Extraction** | Anahtar kelime | "early computers" |
| **PII Detection** | Hassas bilgi tespiti | İsim, tarih, adres |
| **Text Translation** | Dil çevirisi | EN → FR, JA vb |

---

## 🔑 Sınav İçin Kritik Kavramlar

### Vision AI:
- ✅ 4 özellik: Classification, Detection, Text Detection, Document AI
- ✅ **Confidence Score:** Her sonuç için güven skoru
- ✅ **Bounding Box:** Object Detection'da kullanılır
- ✅ **Document Understanding:** Document AI'ın yeni adı
- ✅ **Key-Value Pairs:** Belgelerden yapılandırılmış veri çıkarma
- ✅ **Table Extraction:** Tablolar otomatik çıkarılır

### Language AI:
- ✅ 6+ pretrained model
- ✅ **Aspect-Based Sentiment:** Konu bazlı duygu analizi
- ✅ **PII Detection:** GDPR için kritik
- ✅ **Custom Model Training:** Her iki serviste de mevcut
- ✅ **Çoklu dil desteği:** Translation için

---

## 💡 Servis Adı Değişikliği (ÖNEMLİ!)

**Eski:** Document AI (Vision Service içinde)
**Yeni:** Document Understanding Service (Ayrı servis)
**Özellikler:** Tamamen aynı

⚠️ **Sınavda:** Her iki isimle de karşılaşabilirsiniz!

---

## 🎓 Pratik Kullanım Senaryoları

### Vision AI:
1. **E-ticaret:** Ürün görsellerini otomatik kategorize etme
2. **Güvenlik:** Plaka okuma, yüz tanıma
3. **Muhasebe:** Fiş/fatura otomasyonu
4. **Lojistik:** Paket/envanter takibi

### Language AI:
1. **Müşteri Hizmetleri:** Sentiment analysis ile müşteri memnuniyeti
2. **Çoklu dil desteği:** Otomatik çeviri
3. **Compliance:** PII detection ile GDPR
4. **İçerik Yönetimi:** Otomatik metin sınıflandırma

---

## ✏️ Kendi Notlarınız İçin Boş Alan

_______________________________________________
_______________________________________________
_______________________________________________
_______________________________________________