# 📚 GÜN 2: SUPERVISED LEARNING - REGRESSION - Detaylı Çalışma Notu

## 🎯 Modül Özeti
Bu modül Supervised Learning'i ve Linear Regression'ı detaylı olarak ele alıyor. House price prediction örneği ile pratik uygulama gösteriliyor.

---

## 📖 SUPERVISED LEARNING TANIMI (TEKRAR)

**Supervised Learning:** Labeled data'dan öğrenen machine learning modeli

**Temel Prensip:** Model, **input ve output arasındaki mapping (eşleme)** öğrenir

---

## 💼 SUPERVISED LEARNING UYGULAMALARI

### 1. House Price Predictor (Ev Fiyat Tahmini)
- **Input:** House size (Ev büyüklüğü - square feet)
- **Output:** Price (Fiyat - dolar)

### 2. Cancer Detection (Kanser Tespiti)
- **Input:** Medical details (Tıbbi detaylar)
- **Output:** Malignant or not (Tümör kötü huylu mu değil mi)

### 3. Sentiment Analysis (Duygu Analizi)
- **Input:** Customer reviews (Müşteri yorumları)
- **Output:** Positive, Negative, or Neutral (Pozitif, Negatif veya Nötr)

### 4. Stock Price Prediction (Borsa Tahmini)
- **Input:** Opening price, closing price, volume traded (Açılış, kapanış, hacim)
- **Output:** Stock price (Hisse fiyatı)

---

## 🎓 SUPERVISED LEARNING = ÖĞRETMEN-ÖĞRENCİ ANALOJİSİ

**Benzetme:**
- **Teacher (Öğretmen):** Past outcomes (Geçmiş sonuçlar = Labels)
- **Student (Öğrenci):** Model
- **Learning (Öğrenme):** Input-output ilişkisini öğrenme

**Süreç:**
```
Past Data (Input + Output) → Model Training → Learned Relationship
```

---

## 📊 SUPERVISED LEARNING: REGRESSION vs CLASSIFICATION

### Output Türüne Göre Ayrım

| Output Türü | Yöntem | Örnek |
|-------------|--------|-------|
| **Continuous (Sürekli)** | **Regression** | House price: $250,000 |
| **Categorical (Kategorik)** | **Classification** | Spam: Yes/No |

### Regression
- **Output:** Continuous (Sürekli sayısal değer)
- **Örnekler:** Fiyat, sıcaklık, yaş, maaş
- **Algoritma:** Linear Regression, Polynomial Regression vb.

### Classification
- **Output:** Categorical (Kategori/sınıf)
- **Örnekler:** Spam/Ham, Cat/Dog, Positive/Negative/Neutral
- **Algoritma:** Logistic Regression, Decision Trees vb.

**💡 Bu derste odak: REGRESSION (Linear Regression)**

---

## 🏠 LINEAR REGRESSION ÖRNEK: HOUSE PRICE PREDICTION

### Problem Tanımı
**Amaç:** Ev fiyatını, ev büyüklüğüne göre tahmin etmek

**Tek Feature (Özellik):** House size (square feet)

---

### Veri Seti Yapısı

**Training Data Set:**

| House Size (sq ft) | Price ($) |
|-------------------|-----------|
| 1000 | 200,000 |
| 1200 | 240,000 |
| 1500 | 300,000 |
| 1800 | 360,000 |
| ... | ... |

---

### Terimler

#### Independent Feature (Bağımsız Özellik)
- **Tanım:** Diğer özelliklere bağlı olmayan, girdi olan özellik
- **Başka adı:** Input feature, X
- **Örnekte:** House size (Ev büyüklüğü)

#### Dependent Feature (Bağımlı Özellik)
- **Tanım:** Diğer özelliklere bağlı olan, çıktı olan özellik
- **Başka adı:** Output label, Y
- **Örnekte:** Price (Fiyat)
- **Neden bağımlı:** Fiyat, ev büyüklüğüne BAĞLI

#### Training Example (Eğitim Örneği)
- **Tanım:** Tek bir satır (Input + Output)
- **Başka adı:** Tuple (Demet)
- **Örnek:** (1000 sq ft, $200,000)

#### Training Data Set (Eğitim Veri Seti)
- **Tanım:** Tüm training example'ların toplamı
- **Kullanım:** Model oluşturmak için

---

### Görselleştirme: Scatter Plot

**Neden Scatter Plot?**
- Input ve output arasındaki ilişkiyi görmek için
- Pattern'i anlamak için

**Gözlem:**
```
House Size ↑ → Price ↑ (Doğru orantı)
```

**Çizgi (Line) Uydurma:**
- Bu noktalardan geçen bir düz çizgi çizilir
- Bu çizgi tahmin için kullanılır

**Örnek Tahmin:**
```
House Size = 1,100 sq ft
↓
Çizgiyi kullan
↓
Price ≈ $220,000 (tahmini)
```

---

## 📐 LINEAR REGRESSION MATEMATIĞI

### Çizgi Denklemi

**Genel Form:**
```
f(x) = w × x + b
```

veya

```
y = w × x + b
```

**Terimler:**

#### w (Weight/Slope - Ağırlık/Eğim)
- **Tanım:** Çizginin eğimi (slope)
- **Anlamı:** House price'ın house size'a göre değişim oranı
- **Örnek:** w = 200 → Her 1 sq ft artışta $200 artış

#### b (Bias/Y-intercept - Sapma/Y-kesişim noktası)
- **Tanım:** Y eksenini kestiği nokta
- **Anlamı:** House size = 0 olduğunda fiyat
- **Kullanım:** Çizgiyi yukarı-aşağı kaydırır

#### x (Input)
- **Örnekte:** House size

#### f(x) veya y (Output/Prediction)
- **Örnekte:** Predicted price

---

### Çizgiyi Ayarlama

**Bias (b) değiştirme:**
- Çizgi **yukarı-aşağı** hareket eder
- Slope değişmez

**Slope (w) değiştirme:**
- Çizgi **yukarı veya aşağı doğru eğilir**
- Daha dik veya daha yatık olur

**Amaç:** En iyi uyum sağlayan çizgiyi bulmak
- w ve b'yi **iteratively (iteratif/tekrarlı)** ayarlayarak

---

## 🎯 MODEL EĞİTİMİ: NASIL ÇALIŞIR?

### Süreç

**1. İlk Tahmin:**
- Rastgele w ve b değerleri ile başla
- Tahmin yap: ŷ = w × x + b

**2. Hata Hesaplama:**

**Error (Hata):**
```
Error = Predicted Value - Actual Value
Error = ŷ - y
```

**Örnek:**
- Actual Price (y): $250,000
- Predicted Price (ŷ): $230,000
- Error: $230,000 - $250,000 = -$20,000

---

**3. Loss (Kayıp) Hesaplama:**

**Loss Nedir?**
- **Tanım:** Kötü tahmin için ceza (penalty)
- Perfect prediction → Loss = 0
- Bad prediction → Loss yüksek

**Loss Hesaplama Yöntemi (Squared Loss):**
```
Loss = (Predicted - Actual)²
Loss = (ŷ - y)²
```

**Neden Kare Alınır?**
- Negatif değerleri pozitif yapar
- Büyük hataları daha fazla cezalandırır

**Örnek:**
```
Error = -$20,000
Squared Loss = (-20,000)² = 400,000,000
```

---

**4. Weight ve Bias Güncelleme:**

**Algoritma (Linear Regression):**
- w ve b değerlerini **iteratively (iteratif)** ayarlar
- **Amaç:** Squared loss'u **minimize** etmek

**Süreç:**
```
1. Tahmin yap
2. Loss hesapla
3. w ve b'yi ayarla (loss azalacak şekilde)
4. Tekrar et
```

---

**5. Optimal Değerlere Ulaşma:**

**Ne zaman durur?**
- Loss minimum seviyeye geldiğinde
- Daha fazla iyileştirme olmadığında

**Sonuç:**
- **Optimal w ve b** bulundu
- **Trained Model** hazır!

---

### Model Kullanımı (Prediction)

**Trained Model:**
```
f(x) = w_optimal × x + b_optimal
```

**Yeni Tahmin:**
```
Input: House Size = 1,500 sq ft
↓
f(1500) = w_optimal × 1500 + b_optimal
↓
Output: Predicted Price
```

---

## 🔄 LINEAR REGRESSION SÜRECİ ÖZET

```
┌─────────────────────────────────────────────┐
│   1. DATA COLLECTION                        │
│   Input (House Size) + Output (Price)       │
└──────────────────┬──────────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────────┐
│   2. VISUALIZATION                          │
│   Scatter Plot → Pattern görme              │
└──────────────────┬──────────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────────┐
│   3. MODEL DEFINITION                       │
│   f(x) = w × x + b                          │
└──────────────────┬──────────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────────┐
│   4. TRAINING (ITERATIVE)                   │
│   • Predict: ŷ = w × x + b                  │
│   • Calculate Loss: (ŷ - y)²                │
│   • Adjust w and b                          │
│   • Repeat until loss minimized             │
└──────────────────┬──────────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────────┐
│   5. TRAINED MODEL                          │
│   f(x) = w_optimal × x + b_optimal          │
└──────────────────┬──────────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────────┐
│   6. PREDICTION                             │
│   New House Size → f(x) → Predicted Price   │
└─────────────────────────────────────────────┘
```

---

## 🔑 ANAHTAR KELİMELER VE KAVRAMLAR

### Temel Terimler
- ✅ **Regression:** Output continuous olduğunda kullanılan yöntem
- ✅ **Classification:** Output categorical olduğunda kullanılan yöntem
- ✅ **Linear Regression:** Çizgi ile tahmin (f(x) = w×x + b)
- ✅ **Mapping:** Input-output ilişkisi
- ✅ **Continuous Output:** Sürekli sayısal değer
- ✅ **Categorical Output:** Kategori/sınıf

### Veri Terimleri
- ✅ **Independent Feature:** Input, X, bağımsız özellik
- ✅ **Dependent Feature:** Output, Y, bağımlı özellik
- ✅ **Training Example:** Tek satır (input + output)
- ✅ **Tuple:** Training example'ın başka adı
- ✅ **Training Data Set:** Tüm training example'lar
- ✅ **Scatter Plot:** Input-output grafiği

### Matematik Terimleri
- ✅ **w (Weight):** Eğim, slope
- ✅ **b (Bias):** Y-intercept, kesişim
- ✅ **Slope:** Çizginin eğimi, değişim oranı
- ✅ **Y-intercept:** Y eksenini kestiği nokta
- ✅ **f(x) = w×x + b:** Linear regression denklemi

### Eğitim Terimleri
- ✅ **Error:** Predicted - Actual
- ✅ **Loss:** Hata için ceza (penalty)
- ✅ **Squared Loss:** (ŷ - y)²
- ✅ **Minimize:** Loss'u en aza indirme
- ✅ **Iteratively:** Tekrarlı, döngüsel
- ✅ **Optimal:** En iyi, minimum loss veren
- ✅ **Trained Model:** Eğitilmiş, kullanıma hazır model
- ✅ **Prediction:** Tahmin yapma

### Uygulama Terimleri
- ✅ **House Price Prediction:** Ev fiyat tahmini
- ✅ **Cancer Detection:** Kanser tespiti
- ✅ **Sentiment Analysis:** Duygu analizi
- ✅ **Stock Price Prediction:** Borsa tahmini
- ✅ **Malignant:** Kötü huylu (tümör için)

---

## 💡 ÖNEMLİ NOTLAR

### 1. Regression vs Classification
**Ne zaman hangisi?**
- Output **sayısal** (fiyat, sıcaklık, yaş) → **REGRESSION**
- Output **kategori** (Yes/No, Cat/Dog, colors) → **CLASSIFICATION**

### 2. Independent vs Dependent
**Kolay hatırlama:**
- **Independent (Bağımsız):** Sebep → Input → X → House Size
- **Dependent (Bağımlı):** Sonuç → Output → Y → Price

**Price DEPENDS ON Size** → Price is DEPENDENT

### 3. w ve b Ayarlama
**Görsel Etki:**
- **b artırır:** Çizgi yukarı kayar ↑
- **b azaltır:** Çizgi aşağı kayar ↓
- **w artırır:** Çizgi daha dik olur ↗
- **w azaltır:** Çizgi daha yatık olur →

### 4. Loss Neden Squared?
**Avantajları:**
- Negatif değerleri pozitif yapar
- Büyük hataları daha çok cezalandırır
- Matematiksel olarak optimize edilmesi kolay

**Örnek:**
- Error = -10 → Squared = 100
- Error = -20 → Squared = 400 (4 kat daha fazla ceza!)

### 5. Iterative Training
**Neden iterative?**
- Tek seferde optimal w ve b bulunmaz
- Adım adım iyileştirme gerekir
- Her iterasyonda loss azalır
- Minimum'a ulaşana kadar devam

### 6. Perfect Prediction
**Loss = 0 ne zaman?**
```
If ŷ = y (Predicted = Actual)
Then Loss = (ŷ - y)² = 0² = 0
```

**Gerçekte:**
- Perfect prediction nadirdir
- Goal: Loss'u minimize etmek (sıfır değil!)

---

## 🎯 SINAV İÇİN KRİTİK NOKTALAR

### Mutlaka Bilin:
1. **Regression = Continuous output** ✓
2. **Classification = Categorical output** ✓
3. **Linear Regression denklemi: f(x) = w×x + b** ✓
4. **w = slope (eğim)** ✓
5. **b = y-intercept (kesişim)** ✓
6. **Loss = (ŷ - y)²** (Squared loss) ✓
7. **Independent feature = Input = X** ✓
8. **Dependent feature = Output = Y** ✓
9. **Training example = Tuple = Tek satır** ✓
10. **Supervised Learning = Labeled data** ✓

### Örnekleri Bilin:
- **Regression:** House price, stock price, temperature
- **Classification:** Spam detection, cancer detection, sentiment
- **House Price:** Size → Price (regression örneği)

### Matematiksel İlişkiler:
- **Error = ŷ - y**
- **Squared Loss = (ŷ - y)²**
- **Loss = 0 ↔ Perfect prediction**
- **Loss ↑ ↔ Bad prediction**

---

## 📋 ÖĞRENME KONTROL LİSTESİ

Kendinize sorun:
- [ ] Regression ve Classification farkını biliyor muyum?
- [ ] Linear Regression denklemi nedir?
- [ ] w ve b ne işe yarar?
- [ ] Independent vs Dependent feature farkı?
- [ ] Training example = Tuple mı?
- [ ] Loss nasıl hesaplanır?
- [ ] Neden squared loss kullanılır?
- [ ] Iterative training ne demek?
- [ ] Optimal w ve b nasıl bulunur?
- [ ] Supervised Learning = Labeled data?
- [ ] House price prediction'da input/output ne?

**Hepsine EVET cevabı vermelisiniz!**

---

## ✏️ Kendi Notlarınız İçin Boş Alan

_______________________________________________
_______________________________________________
_______________________________________________
_______________________________________________