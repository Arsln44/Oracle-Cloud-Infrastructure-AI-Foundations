# 📚 GÜN 2: INTRODUCTION TO MACHINE LEARNING - Detaylı Çalışma Notu

## 🎯 Modül Özeti
Bu modül Machine Learning'in ne olduğunu, nasıl çalıştığını ve günlük hayattan örneklerini açıklıyor.

---

## 🤖 MACHINE LEARNING NEDİR?

### Tanım
**Machine Learning (ML):** Artificial Intelligence'ın bir alt kümesidir. Bilgisayar sistemlerinin **açıkça programlanmadan** örneklerden öğrenerek tahmin yapabilmesini sağlar.

### Temel Kavramlar

**"Without being explicitly programmed"** - Açıkça programlanmadan
- Kurallar elle yazılmaz
- Sistem örneklerden öğrenir
- Otomatik öğrenme

**Powered by Algorithms:**
- Algoritmalar makinelere zeka kazandırır
- Örnekler setinden (genellikle veri olarak) otomatik öğrenme

---

## 💼 GÜNLÜK HAYATTAN MACHINE LEARNING ÖRNEKLERİ

### 1. Online Shopping (E-ticaret)
**Ne Yapar:** Ürün önerileri
**Nasıl:** 
- Tercihlerimize göre
- Alışveriş geçmişimize göre
**Teknoloji:** Machine Learning

---

### 2. Netflix
**Ne Yapar:** Film/dizi önerileri
**Nasıl:**
- İzleme geçmişimize göre
- Benzer izleyicilerin tercihlerine göre
**Teknoloji:** Machine Learning

---

### 3. Email (Spam Filtresi)
**Ne Yapar:** Spam uyarısı
**Nasıl:**
- Email içeriğine göre
- Spam/Normal sınıflandırması
**Teknoloji:** Machine Learning

---

### 4. Self-Driving Cars (Otonom Araçlar)
**Ne Yapar:** Aracı hedefe götürür
**Nasıl:**
- Otomatik sürüş
- Karar verme
**Teknoloji:** Machine Learning

---

## 🔧 MACHINE LEARNING NASIL ÇALIŞIR?

### Problem: Kedi ve Köpeği Ayırt Etme

#### Adım 1: Features (Özellikler) Tanımlama

**Input Data (Girdi Verisi):**
- Body color (Vücut rengi)
- Texture (Doku)
- Eye color (Göz rengi)
- Diğer ayırt edici özellikler

**💡 Bu özelliklere toplu olarak "Input Data" denir**

---

#### Adım 2: Labels (Etiketler) Ekleme

**Output/Label (Çıktı/Etiket):**
- "Cat" (Kedi)
- "Dog" (Köpek)

**💡 Her feature set'ine karşılık gelen çıktı/etiket**

---

#### Adım 3: Training (Eğitim)

**Training Data Set (Eğitim Veri Seti):**
```
Features + Labels → Training Data
```

**Ne Olur:**
- ML model, **features** ve **labels** arasındaki **ilişkiyi öğrenir**
- Veriden pattern'ler çıkarır

**Sonuç:** **Trained Model (Eğitilmiş Model)**

---

#### Adım 4: Inference (Çıkarım/Tahmin)

**Inference Nedir:**
- Eğitilmiş modele **yeni bir veri noktası** vermek
- Model **tahmin** yapar

**Örnek:**
```
Input: Yeni bir hayvanın özellikleri
↓
Trained Model
↓
Output: "Cat" veya "Dog"
```

**💡 Inference = Prediction (Tahmin) süreci**

---

## 📊 MACHINE LEARNING SÜRECİ - ÖZET

```
┌─────────────────────────────────────────────────────┐
│                  1. DATA COLLECTION                  │
│              Features + Labels topla                 │
└────────────────────┬────────────────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────────────────┐
│                   2. TRAINING                        │
│        Model, features-labels ilişkisini öğrenir     │
└────────────────────┬────────────────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────────────────┐
│                3. TRAINED MODEL                      │
│            Model artık kullanıma hazır               │
└────────────────────┬────────────────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────────────────┐
│              4. INFERENCE (PREDICTION)               │
│         Yeni veri → Model → Tahmin                   │
└─────────────────────────────────────────────────────┘
```

---

## 🎓 MACHINE LEARNING TÜRLERİ (3 ANA TÜR)

### Ayırt Edici Faktör
**"Labeled output var mı?"** sorusuna göre ML türü belirlenir

---

### 1. SUPERVISED LEARNING (Denetimli Öğrenme)

**Özellik:** **Labeled data** kullanılır

**Ne Yapar:**
- Model, **features ve labels arasındaki ilişkiyi** öğrenir
- Eğitim sonrası tahmin yapar

**Veri Yapısı:**
```
Features (X) + Labels (Y) → Training
```

**Amaç:** Yeni veri geldiğinde doğru label'ı tahmin etmek

---

#### Supervised Learning Uygulamaları (POPÜLER!)

| Uygulama | Input | Output | Açıklama |
|----------|-------|--------|----------|
| **Disease Detection** | Hasta verisi | Hastalık var/yok | Hastalık tespiti |
| **Weather Forecasting** | Geçmiş hava verileri | Hava durumu tahmini | Hava tahmini |
| **Stock Price Prediction** | Geçmiş borsa verileri | Fiyat tahmini | Borsa tahmini |
| **Spam Detection** | Email içeriği | Spam/Normal | Spam tespiti |
| **Credit Scoring** | Müşteri verisi | Kredi skoru | Kredi değerlendirmesi |

**💡 Örnek - Disease Detection:**
```
Input: Hasta verisi (yaş, semptomlar, test sonuçları)
↓
ML Model
↓
Output: Hasta mı / Sağlıklı mı
```

---

### 2. UNSUPERVISED LEARNING (Denetimsiz Öğrenme)

**Özellik:** **Labels kullanılmaz veya mevcut değildir**

**Ne Yapar:**
- Veri setindeki **ilişkileri** anlamak için kullanılır
- Pattern'leri keşfeder

**Veri Yapısı:**
```
Features (X) only → Pattern Discovery
```

**Amaç:** Verideki yapıları/grupları bulmak

---

#### Unsupervised Learning Uygulamaları (REAL-TIME!)

| Uygulama | Veri | Ne Bulur | Açıklama |
|----------|------|----------|----------|
| **Fraudulent Transactions** | İşlem verisi | Dolandırıcılık pattern'leri | Sahte işlem tespiti |
| **Customer Segmentation** | Müşteri verisi | Müşteri grupları | Müşteri kümeleme |
| **Outlier Detection** | Herhangi bir veri | Aykırı değerler | Anormal veri tespiti |
| **Targeted Marketing** | Müşteri davranışı | Hedef kitleler | Pazarlama kampanyaları |

**💡 Örnek - Fraudulent Transactions:**
```
Input: İşlem verisi (tutar, saat, lokasyon vb.)
↓
ML Model (Pattern Discovery)
↓
Output: Normal/Dolandırıcılık pattern'i
```

**Not:** Label yok! Model kendi başına pattern bulur.

---

### 3. REINFORCEMENT LEARNING (Pekiştirmeli Öğrenme)

**Özellik:** Algoritmalar **outcomes (sonuçlardan)** öğrenir

**Ne Yapar:**
- Kararlar veya seçimler yapmayı öğrenir
- Deneme-yanılma yoluyla

**Nasıl Çalışır:**
```
Action → Outcome (Reward/Punishment) → Learning
```

**Amaç:** En iyi stratejiyi/politikayı bulmak

---

#### Reinforcement Learning Uygulamaları (POPÜLER!)

| Uygulama | Açıklama | Nasıl Öğrenir |
|----------|----------|---------------|
| **Automated Robots** | Otonom robotlar | Task'leri deneme-yanılma ile öğrenir |
| **Autonomous Driving Cars** | Otonom araçlar | Sürüş deneyimlerinden öğrenir |
| **Playing Games** | Oyun oynama (AlphaGo) | Oyunu oynayarak strateji öğrenir |

**💡 Örnek - Autonomous Driving:**
```
Durum: Trafik ışığı kırmızı
↓
Action: Dur (veya geç - yanlış!)
↓
Outcome: Reward (doğru) / Punishment (yanlış)
↓
Learning: Kırmızı ışıkta dur
```

---

## 📊 ML TÜRLERİ KARŞILAŞTIRMA

| Özellik | Supervised | Unsupervised | Reinforcement |
|---------|------------|--------------|---------------|
| **Veri** | Labeled | Unlabeled | Feedback/Outcomes |
| **Ne Öğrenir** | Features→Labels ilişkisi | Pattern'ler, yapı | En iyi strateji |
| **Amaç** | Tahmin | Keşif, kümeleme | Karar verme |
| **Örnek** | Spam detection | Customer segmentation | Self-driving car |
| **Output** | Label/Tahmin | Clusters/Groups | Action/Decision |

---

## 🔑 ANAHTAR KELİMELER VE KAVRAMLAR

### Temel Terimler
- ✅ **Features (Özellikler):** Input data, X
- ✅ **Labels (Etiketler):** Output, Y (Supervised'da var)
- ✅ **Training (Eğitim):** Model öğrenme süreci
- ✅ **Trained Model:** Eğitilmiş, kullanıma hazır model
- ✅ **Inference (Çıkarım):** Tahmin yapma süreci
- ✅ **Prediction (Tahmin):** Model çıktısı
- ✅ **Data Point:** Tek bir veri örneği

### ML Türlerine Özel
- ✅ **Labeled Data:** Etiketli veri (Supervised)
- ✅ **Unlabeled Data:** Etiketsiz veri (Unsupervised)
- ✅ **Pattern Discovery:** Pattern keşfi (Unsupervised)
- ✅ **Outcomes:** Sonuçlar (Reinforcement)
- ✅ **Reward/Punishment:** Ödül/Ceza (Reinforcement)
- ✅ **Clustering:** Kümeleme (Unsupervised)
- ✅ **Segmentation:** Segmentasyon (Unsupervised)
- ✅ **Outlier:** Aykırı değer (Unsupervised)

### Uygulamalara Özel
- ✅ **Disease Detection:** Hastalık tespiti
- ✅ **Weather Forecasting:** Hava tahmini
- ✅ **Stock Price Prediction:** Borsa tahmini
- ✅ **Spam Detection:** Spam tespiti
- ✅ **Credit Scoring:** Kredi skorlama
- ✅ **Fraudulent Transactions:** Dolandırıcılık işlemler
- ✅ **Customer Segmentation:** Müşteri kümeleme
- ✅ **Outlier Detection:** Aykırı değer tespiti
- ✅ **Targeted Marketing:** Hedefli pazarlama
- ✅ **Automated Robots:** Otonom robotlar
- ✅ **Autonomous Driving:** Otonom sürüş

---

## 💡 ÖNEMLİ NOTLAR

### 1. "Without being explicitly programmed"
**Anlamı:** Kurallar manuel yazılmaz, sistem otomatik öğrenir
**Örnek:** 
- ❌ "if email contains 'lottery' then spam" (Elle yazılmış kural)
- ✅ ML modeli spam pattern'lerini otomatik öğrenir

### 2. Features ve Labels İlişkisi
**Supervised Learning:**
- Features + Labels birlikte verilir
- Model aralarındaki ilişkiyi öğrenir
- Yeni feature gelince label tahmin edilir

**Unsupervised Learning:**
- Sadece Features verilir
- Labels yok!
- Model kendi başına pattern bulur

### 3. Training vs Inference
**Training (Eğitim):**
- Model öğrenme aşaması
- Geçmiş veri kullanılır
- Tek sefer yapılır (veya güncelleme için tekrar)

**Inference (Çıkarım):**
- Model kullanım aşaması
- Yeni veri gelir
- Tahmin yapılır
- Sürekli yapılır

### 4. Real-Time Applications
**Unsupervised için "real-time" vurgusu:**
- Gerçek zamanlı pattern keşfi
- Dinamik veri akışında çalışma
- Örnek: Dolandırıcılık tespiti (işlem anında)

---

## 🎯 SINAV İÇİN KRİTİK NOKTALAR

### Ezberlenecekler:
1. **ML Tanımı:** AI'ın alt kümesi, açıkça programlanmadan öğrenme
2. **3 ML Türü:** Supervised (labeled), Unsupervised (unlabeled), Reinforcement (outcomes)
3. **ML Süreci:** Data → Training → Trained Model → Inference
4. **Features:** Input/X
5. **Labels:** Output/Y (Supervised'da var)
6. **Inference = Prediction**

### Örnekleri Bilin:
- **Supervised:** Disease detection, spam, credit scoring
- **Unsupervised:** Fraud detection, customer segmentation
- **Reinforcement:** Robots, autonomous cars, games

### Karşılaştırmalar:
- Supervised **≠** Unsupervised (labeled vs unlabeled)
- Training **≠** Inference (öğrenme vs tahmin)
- Features **≠** Labels (input vs output)

---

## 🎓 ÖĞRENME KONTROL LİSTESİ

Kendinize sorun:
- [ ] ML nedir, AI ile ilişkisi?
- [ ] Features ve Labels nedir?
- [ ] Training ne demek?
- [ ] Inference ne demek?
- [ ] 3 ML türünü ayırt edebiliyor muyum?
- [ ] Supervised'da ne var, Unsupervised'da ne yok?
- [ ] Reinforcement nasıl öğrenir?
- [ ] Her ML türüne 2 örnek verebiliyor muyum?
- [ ] "Without explicitly programmed" ne demek?
- [ ] Real-time unsupervised uygulamalar?

**Hepsine EVET demeniz gerekiyor!**

---

## ✏️ Kendi Notlarınız İçin Boş Alan

_______________________________________________
_______________________________________________
_______________________________________________
_______________________________________________