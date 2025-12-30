# 📚 GÜN 1: AI - Tasks and Data - Detaylı Çalışma Notu

## 🎯 Modül Özeti
Bu modül, farklı AI görevlerinin (Language, Speech, Vision, Anomaly Detection, Recommendations, Forecasting) hangi veri türleri ve model mimarileri kullandığını detaylandırıyor.

---

## 🗣️ LANGUAGE AI - Dil İşleme

### Kullanılan Deep Learning Mimarileri

#### 1. **RNN (Recurrent Neural Networks)**
**Özellikler:**
- Veriyi **sıralı** (sequential) işler
- **Hidden states** (gizli durumlar) saklar
- Her adımda önceki bilgiyi kullanır

**Kullanım:** Metin sıralaması, dil çevirisi temel görevleri

---

#### 2. **LSTM (Long Short-Term Memory)**
**Özellikler:**
- Veriyi **sıralı** işler
- **Gates (kapılar)** kullanarak context'i (bağlamı) daha iyi tutar
- RNN'den daha gelişmiş hafıza mekanizması

**Avantaj:** Uzun metinlerde bağlamı kaybetmez

**Kullanım:** Uzun metin analizi, sentiment analizi

---

#### 3. **Transformers** ⭐
**Özellikler:**
- Veriyi **paralel** işler (RNN/LSTM gibi sıralı değil)
- **Self-attention** konsepti kullanır
- Context'i (bağlamı) çok daha iyi anlar

**Neden Önemli:** Modern LLM'lerin (GPT, BERT) temel mimarisi!

**Kullanım:** ChatGPT, Google Translate, modern NLP görevleri

---

### 📊 Language AI Mimarileri Karşılaştırma

| Mimari | İşleme Türü | Hafıza | Hız | Örnek |
|--------|-------------|--------|-----|-------|
| RNN | Sıralı (Sequential) | Hidden states | Yavaş | Basit dil modelleri |
| LSTM | Sıralı (Sequential) | Gates ile gelişmiş | Yavaş | Sentiment analizi |
| Transformer | Paralel | Self-attention | Hızlı | GPT, BERT |

---

## 🎤 SPEECH AI - Konuşma İşleme

### İki Ana Kategori

#### 1. **Audio-Related (Ses İşleme)**
**Input:** Ses/Audio
**Output:** Değişken (göreve göre)

**Örnekler:**
- Speech-to-Text (Konuşmadan metine)
- Speaker Recognition (Konuşmacı tanıma)
- Voice Conversion (Ses dönüştürme)

---

#### 2. **Generative AI (Üretken AI)**
**Input:** Değişken
**Output:** Ses/Audio (model tarafından üretilir)

**Örnekler:**
- Music Composition (Müzik bestesi)
- Speech Synthesis (Konuşma sentezi - Text-to-Speech)

---

### 🎵 Ses Verisi Nasıl Dijitalleştirilir?

#### **Sample Rate (Örnekleme Oranı)**
**Tanım:** Bir saniyede kaç kez ses örneği alındığı

**Standart:** 44.1 kHz = 44,100 sample/saniye
- Ses CD'leri bu örnekleme oranını kullanır
- Kayıt: Saniyede 44,100 kez örneklenir
- Oynatma: Donanım saniyede 44,100 kez sesi yeniden oluşturur

---

#### **Bit Depth (Bit Derinliği)**
**Tanım:** Her örnekteki bit sayısı (bilgi zenginliği)

**Analoji:** Her 44,100 parçanın ne kadar detaylı olduğu

**💡 Önemli:** Tek bir ses örneğine bakarak bir şey anlaşılamaz! Birden fazla örnek korelasyona ihtiyaç vardır. (Bir şarkının saniyenin küçücük bir parçasını dinleyerek ne olduğunu anlayamazsınız)

---

### Kullanılan Deep Learning Mimarileri (Speech AI)

1. **RNN** - Sıralı işleme
2. **LSTM** - Gelişmiş hafıza
3. **Transformers** - Paralel işleme
4. **Variational Autoencoders (VAE)** - Ses üretimi
5. **Waveform Models** - Dalga formu modelleme
6. **Siamese Networks** - Benzerlik karşılaştırma

**💡 Ortak Özellik:** Tüm modeller sesin **sıralı doğasını** (sequential nature) dikkate alır

---

## 👁️ VISION AI - Görüntü İşleme

### İki Ana Kategori

#### 1. **Image-Related (Görüntü İşleme)**
**Input:** Görüntü (Image)
**Output:** Değişken (göreve göre)

**Örnekler:**
- Image Classification (Görüntü sınıflandırma)
- Object Detection (Nesne tespiti)
- **Facial Recognition (Yüz tanıma)** ⭐ En popüler!

**Facial Recognition Kullanım Alanları:**
- Güvenlik (Security)
- Biyometri (Biometrics)
- Kolluk kuvvetleri (Law Enforcement)
- Sosyal medya (Social Media)
- Real-time izleme ve takip

---

#### 2. **Generative AI (Üretken AI)**
**Input:** Değişken
**Output:** Görüntü/Video (model tarafından üretilir)

**Örnekler:**
- Text-to-Image (Metinden görüntü: DALL-E)
- Belirli stil veya yüksek çözünürlükte görüntü üretme
- **3D model oluşturma:**
  - Nesneler
  - Makine parçaları
  - Binalar
  - İlaçlar
  - İnsanlar
- Son derece gerçekçi yeni görüntü ve videolar

---

### 🖼️ Görüntü Verisi (Images as Data)

**Piksel (Pixel) Türleri:**
- Grayscale (Gri tonlama)
- Color (Renkli)

**💡 Önemli:** Tek bir piksele bakarak görüntünün ne olduğunu anlayamazsınız!

**Yapılacak görev** → **Gereken input ve output türünü** belirler

---

### Kullanılan Deep Learning Mimarileri (Vision AI)

#### 1. **CNN (Convolutional Neural Networks)** ⭐
**Özellikler:**
- Görüntülerdeki **pattern'leri** (kalıpları) tespit eder
- **Hiyerarşik görsek özellikleri** öğrenir
- Her katman daha karmaşık özellikler öğrenir

**Kullanım:** Image classification, feature extraction

---

#### 2. **YOLO (You Only Look Once)** ⭐
**Özellikler:**
- Görüntüyü işler ve içindeki nesneleri tespit eder
- **Tek geçişte** (one pass) nesne tespiti
- Çok hızlı!

**Kullanım:** Real-time object detection

---

#### 3. **GAN (Generative Adversarial Networks)** ⭐
**Özellikler:**
- **Gerçekçi görüntüler** üretir
- İki ağdan oluşur:
  - Generator (Üreten)
  - Discriminator (Ayırt eden)

**Kullanım:** Yeni görüntü üretme, stil transferi

---

## 📊 DİĞER AI GÖREVLERİ

### 1. **Anomaly Detection (Anormallik Tespiti)**

**Veri Türü:** Time Series Data (Zaman serisi verisi)

**Veri Formatı:**
- Single variate (Tek değişkenli)
- Multivariate (Çok değişkenli)

**Kullanım Alanları:**
- Fraud Detection (Dolandırıcılık tespiti)
- Machine Failure (Makine arızası tahmini)
- Kalite kontrol

---

### 2. **Recommendations (Öneri Sistemleri)**

**Gereken Veri:**
- Benzer ürünlerin verisi
- Benzer kullanıcıların verisi

**Nasıl Çalışır:** 
- Ürün benzerliği analizi
- Kullanıcı davranışı analizi

**Örnekler:**
- Netflix film önerileri
- Amazon ürün önerileri
- Spotify müzik önerileri

---

### 3. **Forecasting (Tahminleme)**

**Veri Türü:** Time Series Data (Zaman serisi verisi)

**Kullanım Alanları:**
- Weather Forecasting (Hava durumu tahmini)
- Stock Price Prediction (Borsa tahmini)
- Talep tahmini
- Satış tahmini

---

## 🎯 VERİ TÜRLERİ ÖZET TABLOSU

| AI Görevi | Ana Veri Türü | Özellikler | Model Örnekleri |
|-----------|---------------|------------|-----------------|
| **Language** | Metin (Sequential) | Sıralı, bağlam önemli | RNN, LSTM, Transformer |
| **Speech** | Ses (Sequential) | 44.1kHz sample, bit depth | RNN, LSTM, VAE, Waveform |
| **Vision** | Görüntü (Pixel) | Grayscale/Color, spatial | CNN, YOLO, GAN |
| **Anomaly Detection** | Time Series | Tek/Çok değişkenli | LSTM, Autoencoder |
| **Recommendations** | User/Product Data | Benzerlik matrisleri | Collaborative Filtering |
| **Forecasting** | Time Series | Geçmiş veriden gelecek | ARIMA, LSTM, Prophet |

---

## 🔑 Sınav İçin Kritik Kavramlar

### Language AI:
- ✅ RNN → Sequential, hidden states
- ✅ LSTM → Sequential, gates, better context
- ✅ Transformer → Parallel, self-attention

### Speech AI:
- ✅ 44.1 kHz = 44,100 sample/second
- ✅ Bit depth = bilgi zenginliği
- ✅ Sequential nature önemli

### Vision AI:
- ✅ CNN → Pattern detection, hierarchical
- ✅ YOLO → Object detection, one pass
- ✅ GAN → Generates realistic images
- ✅ Facial recognition → Çok popüler, security

### Diğer:
- ✅ Anomaly Detection → Time series
- ✅ Recommendations → Similar products/users data
- ✅ Forecasting → Time series

---

## 💭 Önemli Notlar

1. **Sequential vs Parallel:**
   - RNN/LSTM → Sequential (yavaş ama context tutar)
   - Transformer → Parallel (hızlı ve daha iyi context)

2. **Veri Doğası:**
   - Language: Sequential (kelime sırası önemli)
   - Speech: Sequential (zaman boyutlu)
   - Vision: Spatial (mekansal, pikseller)

3. **Generative AI:**
   - Speech → Music, TTS
   - Vision → Images, 3D models
   - Language → Text generation (GPT)

4. **Time Series:**
   - Anomaly Detection ✓
   - Forecasting ✓
   - Speech (zaman boyutlu) ✓

---

## ✏️ Kendi Notlarınız İçin Boş Alan

_______________________________________________
_______________________________________________
_______________________________________________
_______________________________________________