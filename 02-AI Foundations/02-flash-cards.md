# 🎴 FLASHCARDS - AI Tasks and Data

## LANGUAGE AI

### Kart 1
**Ön Yüz:** Language AI için kullanılan 3 ana deep learning mimarisini say.
**Arka Yüz:** 
1. RNN (Recurrent Neural Networks)
2. LSTM (Long Short-Term Memory)
3. Transformers

---

### Kart 2
**Ön Yüz:** RNN'nin temel özellikleri nelerdir?
**Arka Yüz:** 
- Veriyi **sequential (sıralı)** işler
- **Hidden states** (gizli durumlar) saklar
- Her adımda önceki bilgiyi kullanır

---

### Kart 3
**Ön Yüz:** LSTM'yi RNN'den ayıran temel özellik nedir?
**Arka Yüz:** 
**Gates (kapılar)** kullanarak context'i (bağlamı) daha iyi tutar. RNN'den daha gelişmiş hafıza mekanizmasına sahiptir.

---

### Kart 4
**Ön Yüz:** Transformer mimarisinin RNN/LSTM'den farkı nedir?
**Arka Yüz:** 
- Veriyi **parallel (paralel)** işler (sıralı değil)
- **Self-attention** konsepti kullanır
- Context'i çok daha iyi anlar
- Modern LLM'lerin (GPT, BERT) temelidir

---

### Kart 5
**Ön Yüz:** Hangi Language AI mimarisi en hızlıdır ve neden?
**Arka Yüz:** 
**Transformer** - Çünkü veriyi paralel işler. RNN ve LSTM sıralı işlediği için daha yavaştır.

---

## SPEECH AI

### Kart 6
**Ön Yüz:** Speech AI'ın iki ana kategorisi nedir?
**Arka Yüz:** 
1. **Audio-Related:** Ses input → Değişken output (Speech-to-Text, Speaker Recognition)
2. **Generative AI:** Değişken input → Ses output (Music Composition, Speech Synthesis)

---

### Kart 7
**Ön Yüz:** Sample Rate (Örnekleme Oranı) nedir ve standart değeri nedir?
**Arka Yüz:** 
**Tanım:** Bir saniyede kaç kez ses örneği alındığı
**Standart:** 44.1 kHz = 44,100 sample/saniye (CD kalitesi)

---

### Kart 8
**Ön Yüz:** Bit Depth (Bit Derinliği) nedir?
**Arka Yüz:** 
Her ses örneğindeki bit sayısı - yani her örneğin ne kadar bilgi zengin olduğu.

---

### Kart 9
**Ön Yüz:** Speech AI için kullanılan 6 deep learning mimarisini say.
**Arka Yüz:** 
1. RNN
2. LSTM
3. Transformers
4. Variational Autoencoders (VAE)
5. Waveform Models
6. Siamese Networks

**Ortak özellik:** Hepsi sesin sequential (sıralı) doğasını dikkate alır

---

### Kart 10
**Ön Yüz:** Speech-to-Text ve Text-to-Speech arasındaki fark nedir?
**Arka Yüz:** 
- **Speech-to-Text:** Audio-Related (ses input → metin output)
- **Text-to-Speech (Speech Synthesis):** Generative AI (metin input → ses output)

---

## VISION AI

### Kart 11
**Ön Yüz:** Vision AI'ın iki ana kategorisi nedir?
**Arka Yüz:** 
1. **Image-Related:** Görüntü input → Değişken output (Classification, Object Detection)
2. **Generative AI:** Değişken input → Görüntü output (Text-to-Image, 3D models)

---

### Kart 12
**Ön Yüz:** Facial Recognition (Yüz Tanıma) hangi 4 alanda kullanılır?
**Arka Yüz:** 
1. Security (Güvenlik)
2. Biometrics (Biyometri)
3. Law Enforcement (Kolluk kuvvetleri)
4. Social Media (Sosyal medya)

---

### Kart 13
**Ön Yüz:** Vision AI için kullanılan 3 ana deep learning mimarisini say ve özelliklerini belirt.
**Arka Yüz:** 
1. **CNN:** Pattern detection, hierarchical learning
2. **YOLO:** Object detection, tek geçişte
3. **GAN:** Realistic image generation

---

### Kart 14
**Ön Yüz:** CNN (Convolutional Neural Networks) ne yapar?
**Arka Yüz:** 
- Görüntülerdeki **pattern'leri** (kalıpları) tespit eder
- **Hiyerarşik görsel özellikleri** öğrenir
- Her katman daha karmaşık özellikler öğrenir

---

### Kart 15
**Ön Yüz:** YOLO'nun açılımı ve özelliği nedir?
**Arka Yüz:** 
**You Only Look Once**
- Görüntüyü tek geçişte (one pass) işler
- İçindeki nesneleri tespit eder
- Çok hızlı - real-time detection

---

### Kart 16
**Ön Yüz:** GAN (Generative Adversarial Networks) nasıl çalışır?
**Arka Yüz:** 
İki ağdan oluşur:
- **Generator (Üreten):** Görüntü üretir
- **Discriminator (Ayırt eden):** Gerçek/sahte ayırır
Gerçekçi görüntüler üretir

---

### Kart 17
**Ön Yüz:** Görüntü verisi (pixel) için önemli not nedir?
**Arka Yüz:** 
Tek bir piksele bakarak görüntünün ne olduğunu anlayamazsınız! Görüntü spatial (mekansal) bir veridir.

---

## DİĞER AI GÖREVLERİ

### Kart 18
**Ön Yüz:** Anomaly Detection için hangi veri türü gerekir ve ne tür veriler olabilir?
**Arka Yüz:** 
**Veri Türü:** Time Series Data (Zaman serisi)
**Formatlar:**
- Single variate (Tek değişkenli)
- Multivariate (Çok değişkenli)

---

### Kart 19
**Ön Yüz:** Anomaly Detection kullanım alanlarına 3 örnek ver.
**Arka Yüz:** 
1. Fraud Detection (Dolandırıcılık tespiti)
2. Machine Failure (Makine arızası)
3. Kalite kontrol

---

### Kart 20
**Ön Yüz:** Recommendation Systems (Öneri Sistemleri) için hangi veri gerekir?
**Arka Yüz:** 
- Benzer ürünlerin verisi
- Benzer kullanıcıların verisi

---

### Kart 21
**Ön Yüz:** Forecasting (Tahminleme) için hangi veri türü kullanılır? Örnekler ver.
**Arka Yüz:** 
**Veri:** Time Series Data
**Örnekler:**
- Weather forecasting (Hava durumu)
- Stock price prediction (Borsa)
- Talep tahmini

---

## KARŞILAŞTIRMA KARTLARI

### Kart 22
**Ön Yüz:** Sequential (sıralı) işleme yapan mimariler hangileridir?
**Arka Yüz:** 
- RNN (Language, Speech)
- LSTM (Language, Speech)
- Yavaş ama context tutar

---

### Kart 23
**Ön Yüz:** Parallel (paralel) işleme yapan mimari hangisidir?
**Arka Yüz:** 
**Transformer**
- Hızlı
- Self-attention ile daha iyi context
- Modern LLM'lerin temel mimarisi

---

### Kart 24
**Ön Yüz:** Generative AI hangi alanlarda kullanılır? (3 alan)
**Arka Yüz:** 
1. **Speech:** Music composition, Text-to-Speech
2. **Vision:** Text-to-Image, 3D models
3. **Language:** Text generation (GPT)

---

### Kart 25
**Ön Yüz:** Time Series Data hangi AI görevlerinde kullanılır?
**Arka Yüz:** 
1. Anomaly Detection
2. Forecasting
3. Speech AI (zaman boyutlu)

---

### Kart 26
**Ön Yüz:** RNN, LSTM ve Transformer'ı karşılaştır (İşleme türü, hız, kullanım)
**Arka Yüz:** 
| Mimari | İşleme | Hız | Kullanım |
|--------|--------|-----|----------|
| RNN | Sequential | Yavaş | Basit NLP |
| LSTM | Sequential | Yavaş | Sentiment analizi |
| Transformer | Parallel | Hızlı | GPT, BERT |

---

### Kart 27
**Ön Yüz:** Veri doğası açısından Language, Speech ve Vision AI'ı karşılaştır.
**Arka Yüz:** 
- **Language:** Sequential (kelime sırası önemli)
- **Speech:** Sequential (zaman boyutlu, 44.1kHz)
- **Vision:** Spatial (mekansal, pikseller)

---

### Kart 28
**Ön Yüz:** 44.1 kHz sample rate ne anlama gelir?
**Arka Yüz:** 
Ses, saniyede 44,100 kez örneklenir (CD kalitesi). Kayıt ve oynatma bu frekansta yapılır.

---

### Kart 29
**Ön Yüz:** Facial Recognition neden Vision AI'da en popüler task'tır?
**Arka Yüz:** 
Çünkü çok geniş kullanım alanı var:
- Real-time surveillance (izleme)
- Security (güvenlik)
- Social media
- Law enforcement

---

### Kart 30
**Ön Yüz:** Text-to-Image generation hangi Vision AI mimarisi kullanır?
**Arka Yüz:** 
**GAN (Generative Adversarial Networks)** veya **Diffusion Models**
Örnek: DALL-E, Midjourney, Stable Diffusion

---

## 📝 Çalışma Stratejisi

**Prioritization (Önceliklendirme):**
1. ⭐⭐⭐ Yüksek öncelik: RNN/LSTM/Transformer, CNN/YOLO/GAN, 44.1kHz
2. ⭐⭐ Orta öncelik: VAE, Waveform Models, Time Series
3. ⭐ Düşük öncelik: Siamese Networks detayları

**Günlük Tekrar:**
- Sabah: Kart 1-10
- Öğle: Kart 11-20
- Akşam: Kart 21-30

**İpucu:** Mimarileri ve özelliklerini karıştırmayın!