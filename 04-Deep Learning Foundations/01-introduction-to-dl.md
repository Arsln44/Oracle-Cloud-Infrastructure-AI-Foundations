# 📚 GÜN 3: DEEP LEARNING - INTRODUCTION - Detaylı Çalışma Notu

## 🎯 Modül Özeti
Bu modül Deep Learning'in tanımını, ANN (Artificial Neural Network) yapısını, tarihçesini ve temel kavramları açıklıyor.

---

## 🧠 DEEP LEARNING NEDİR?

### Tanım
**Deep Learning (DL):** Machine learning'in bir alt kümesi. **Artificial Neural Networks (ANN)** eğiterek görevleri çözer.

**Hiyerarşi:**
```
AI ⊃ ML ⊃ DL
```

### Örnek Görev
**Image Classification** (Görüntü sınıflandırma)

---

## 🔑 ANN'NİN ÖNEMLİ ÖZELLİĞİ

**Raw Data İşleyebilme:**
- **Pixels** (pikseller) gibi ham veriyi işler
- Bu veriden **patterns (desenler)** çıkarır
- Pattern'ler **features (özellikler)** olarak kullanılır
- Bu özelliklerle **outcome (sonuç)** tahmin eder

**💡 En Önemli Fark: Otomatik feature extraction!**

---

## ✍️ HANDWRITTEN DIGIT RECOGNITION ÖRNEĞİ

### Problem
**Görev:** 0-9 arası el yazısı rakamları tanıma

**Zorluk:** Herkes rakamları farklı yazar

### ANN Çözümü

**1. Input:** Image pixels (28×28 = 784 piksel)

**2. Pattern Extraction:**
- Edges (kenarlar)
- Curves (eğriler)
- Diğer desenler

**3. Correlation:** Pattern'leri ilişkilendirir

**4. Prediction:** Hangi rakam? (0-9)

**Özet:** Bir sürü pikselden → ANN → Internal representation → Prediction

---

## 🆚 ML vs DEEP LEARNING FARKI

### Machine Learning
**Feature Engineering:**
- Features **manuel** belirtilir
- İnsan özellikleri tanımlar
- Zaman alıcı

### Deep Learning
**Automatic Feature Extraction:**
- Features **otomatik** çıkarılır
- Veriden öğrenir
- Internal representation oluşturur
- Manuel olarak mümkün olmayan kombinasyonlar

**💡 DL'nin Gücü: Otomatik feature learning!**

---

## ⚡ DEEP LEARNING AVANTAJLARI

### 1. Parallel Computation (Paralel Hesaplama)
**Nasıl:**
- Data küçük **batches** (gruplara) bölünür
- Paralel işlenir

**Sonuç:**
- ✅ Büyük veri kısa sürede işlenir
- ✅ **Scalability** (ölçeklenebilirlik)
- ✅ **Performance** (performans)

### 2. Kompleks Veri İşleme
**Ne Zaman DL Kullan:**
- Karmaşık veri
- Features kolayca tanımlanamıyor
- ML algoritmaları yetersiz

**💡 DL complements (tamamlar) ML'yi karmaşık veri için**

---

## 📜 DEEP LEARNING TARİHÇESİ

### 1950s - İlk Kavramlar
- Artificial Neuron
- Perceptron
- Multi-layer Perceptron

### 1980s - Backpropagation
**En önemli konsept:** Backpropagation algoritması training için

### 1990s - CNN
**Convolutional Neural Networks** image analysis için tanıtıldı

### 2000 - GPU'lar
**GPU (Graphics Processing Unit)** tanıtıldı

### 2010+ - GPU Yaygınlaşması
- GPU ucuzladı, yaygınlaştı
- **DL patlaması başladı!**

**Kullanım Alanları:**
- Computer Vision
- Natural Language Processing (NLP)
- Speech Recognition
- Text Translation

### 2012 - Büyük Ağlar
- **AlexNet**
- **Deep Q-Network**

### 2016+ - Generative Use Cases
Generative AI kullanım alanları başladı

### Bugün
- **Large Language Models (LLM)**
- Çeşitli generative modeller
- Geniş kullanım alanları

**💡 GPU = DL'nin yükselişindeki anahtar faktör**

---

## 🎯 DL UYGULAMALARI (VERİ TİPLERİNE GÖRE)

### 1. Images (Görüntüler)

| Uygulama | Açıklama |
|----------|----------|
| **Image Classification** | Görüntüyü sınıflandırma |
| **Object Detection** | Nesneleri tespit etme |
| **Image Segmentation** | Piksel seviyesinde ayırma |
| **Facial Recognition** | Yüz tanıma |

**Önerilen Mimari: CNN**

---

### 2. Videos (Videolar)

| Uygulama | Açıklama |
|----------|----------|
| **Action Recognition** | Hareket tanıma |
| **Video Classification** | Video sınıflandırma |

**Önerilen Mimari: CNN + RNN**

---

### 3. Text (Metin)

| Uygulama | Açıklama |
|----------|----------|
| **Text Translation** | Metin çevirisi |
| **Sentiment Detection** | Duygu analizi |
| **Text Summarization** | Metin özetleme |
| **Question Answering** | Soru cevaplama |

**Önerilen Mimari:**
- **Transformers** (en yeni, en iyi)
- LSTM
- RNN

---

### 4. Audio (Ses)

| Uygulama | Açıklama |
|----------|----------|
| **Music Generation** | Müzik üretimi |
| **Speech-to-Text** | Konuşmadan metine |
| **Text-to-Speech** | Metinden konuşmaya |

**Önerilen Mimari: RNN, LSTM, Transformers**

---

### 5. Generative Tasks (Üretken Görevler)

| Uygulama | Açıklama | Mimari |
|----------|----------|--------|
| **Text-to-Image** | Metinden görüntü | Transformers, GANs, Diffusion |
| **Image Generation** | Görüntü üretimi | GANs, Diffusion |

---

## 🧠 ARTIFICIAL NEURAL NETWORK (ANN)

### İlham Kaynağı
**Human Brain (İnsan Beyni)**

### Yapı
**Interconnected Nodes:** Birbirine bağlı düğümler

**Node = Neuron**

---

## 🔧 ANN NASIL ÇALIŞIR?

### Basit Açıklama

**1. Weights (Ağırlıklar):**
- Neuronlar arası bağlantılara atanır
- Connection strength (bağlantı gücü)

**2. Weighted Sum:**
- Weighted inputs toplanır

**3. Threshold:**
- Toplam belirli bir eşiği geçerse → Neuron fires (ateşlenir)

**4. Layer to Layer:**
- Bir katmanın outputu → Diğer katmanın inputu

---

## 🏗️ ANN BUILDING BLOCKS (5 Bileşen)

### 1. LAYERS (Katmanlar)

**a) Input Layer (Giriş Katmanı):**
- **Mandatory (Zorunlu)**
- Ham veriyi alır
- Örnek: 28×28 = 784 piksel

**b) Hidden Layers (Gizli Katmanlar):**
- **Optional (İsteğe bağlı)**
- Birden fazla olabilir
- Internal representation öğrenir
- Ne kadar çok → "Deep" learning

**c) Output Layer (Çıkış Katmanı):**
- **Mandatory (Zorunlu)**
- Final prediction
- Örnek: 10 neuron (0-9 rakamlar için)

---

### 2. NEURONS (Nöronlar)

**Tanım:** Computational units (Hesaplama birimleri)

**Görev:**
- Input kabul eder
- Output üretir

---

### 3. WEIGHTS (Ağırlıklar)

**Tanım:** Connection strength (Bağlantı gücü)

**Nerede:**
- Input → Neuron arası
- Neuron → Neuron arası

**Değişir:** Training sırasında ayarlanır

---

### 4. ACTIVATION FUNCTIONS (Aktivasyon Fonksiyonları)

**Görev:**
- Weighted sum üzerinde çalışır
- Output üretir
- Non-linearity ekler

**Örnekler:**
- ReLU
- Sigmoid
- Tanh

---

### 5. BIAS

**Tanım:** Neuron'a ek input

**Amaç:** Flexibility (Esneklik) sağlar

---

## ✍️ HANDWRITTEN DIGIT RECOGNITION - DETAYLI ÖRNEK

### Veri Toplama
**Large number of digit images** topla

### ANN Yapısı

**Input Layer:**
- 28×28 piksel = **784 input neurons**

**Hidden Layers:**
- 2 hidden layer (örnek)
- Her biri **16 neurons**

**Output Layer:**
- **10 neurons** (0-9 rakamlar için)

### Görevler

**Hidden Layers:**
- **Internal representation** öğrenir
- Raw image data'dan pattern çıkarır

**Output Layer:**
- **Desired outcome** üretir
- Hangi rakam? (0-9)

---

## 🔄 TRAINING SÜRECİ: BACKPROPAGATION

### Örnek Senaryo

**1. Image Göster:**
- Digit "2" görüntüsü

**2. Beklenen:**
- Output neuron for digit 2 fires

**3. Gerçekleşen:**
- Output neuron for digit 6 fires

**4. Hata (Error):**
- Yanlış tahmin!

---

### Backpropagation Algorithm

**Amaç:** Error'ı düzeltmek

**Nasıl:**
1. **Error hesapla**
2. **Weights'i ayarla** (calculation ile)
3. **Backward (geriye)** doğru güncelle

**İterasyon:**
- Binlerce image göster
- Her defasında weights ayarla
- **Iteratively (yinelemeli)**

**Sonuç:**
- ANN çoğu input image için doğru tahmin yapar

**💡 Bu sürece "Model Training" denir**

---

## 🔑 ANAHTAR KELİMELER

### Temel Terimler
- ✅ **Deep Learning:** ML'nin alt kümesi, ANN kullanır
- ✅ **ANN:** Artificial Neural Network
- ✅ **Neuron:** Hesaplama birimi
- ✅ **Layer:** Katman (Input, Hidden, Output)
- ✅ **Weights:** Bağlantı gücü
- ✅ **Bias:** Esneklik için ek input
- ✅ **Activation Function:** Non-linearity ekler

### Özellikler
- ✅ **Raw Data Processing:** Ham veri işleme
- ✅ **Pattern Extraction:** Desen çıkarma
- ✅ **Automatic Feature Extraction:** Otomatik özellik çıkarma
- ✅ **Internal Representation:** İç temsil
- ✅ **Parallel Computation:** Paralel hesaplama
- ✅ **Batches:** Küçük gruplar

### Training
- ✅ **Backpropagation:** Geriye yayılım algoritması
- ✅ **Model Training:** Model eğitimi
- ✅ **Iteratively:** Yinelemeli
- ✅ **Adjust Weights:** Ağırlıkları ayarlama

### Mimariler
- ✅ **CNN:** Convolutional Neural Network
- ✅ **RNN:** Recurrent Neural Network
- ✅ **LSTM:** Long Short-Term Memory
- ✅ **Transformers:** En yeni mimari
- ✅ **GANs:** Generative Adversarial Networks

### Tarihçe
- ✅ **GPU:** Graphics Processing Unit
- ✅ **AlexNet:** 2012'de önemli ağ
- ✅ **LLM:** Large Language Models

---

## 🎯 SINAV İÇİN KRİTİK

### Mutlaka Bilin:
1. **DL = ML'nin alt kümesi** ✓
2. **ANN = Artificial Neural Network** ✓
3. **Otomatik feature extraction** ✓
4. **3 Layer: Input, Hidden, Output** ✓
5. **Backpropagation = Training algoritması** ✓
6. **GPU = DL'nin yükselişi** ✓
7. **CNN → Images** ✓
8. **Transformers → Text (en yeni)** ✓

### Karşılaştırmalar:
- ML → Manuel features
- DL → **Otomatik features**
- Traditional NN → Sequential
- DL → **Parallel computation**

### Mimariler:
- **Images:** CNN
- **Text:** Transformers > LSTM > RNN
- **Audio:** RNN, LSTM, Transformers
- **Generative:** GANs, Diffusion, Transformers

---

## 📋 KONTROL LİSTESİ

- [ ] DL nedir, ML ile farkı?
- [ ] ANN nedir?
- [ ] 3 layer türü?
- [ ] Neuron, Weight, Bias, Activation function?
- [ ] Otomatik feature extraction?
- [ ] Backpropagation ne işe yarar?
- [ ] GPU neden önemli?
- [ ] Hangi veri tipi için hangi mimari?
- [ ] Digit recognition örneği?

**Hepsine EVET!**