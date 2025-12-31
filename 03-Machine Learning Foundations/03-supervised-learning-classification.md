# 📚 GÜN 2: SUPERVISED LEARNING - CLASSIFICATION - Detaylı Çalışma Notu

## 🎯 Modül Özeti
Bu modül Classification konusunu, Binary ve Multi-class Classification'ı, Logistic Regression algoritmasını ve Sigmoid function'ı açıklıyor.

---

## 📖 REGRESSION vs CLASSIFICATION (TEKRAR)

### Output Türüne Göre Ayrım

| Output Türü | Yöntem | Örnek |
|-------------|--------|-------|
| **Continuous (Sürekli)** | **REGRESSION** | House price: $250,000 |
| **Categorical (Kategorik)** | **CLASSIFICATION** | Spam: Yes/No |

**💡 Bu derste odak: CLASSIFICATION**

---

## 🎯 CLASSIFICATION NEDİR?

### Tanım
**Classification:** Supervised learning problemi. Amacı, sonuca (outcome) bir **category (kategori)** veya **label (etiket)** atamak.

### Temel Prensip
Veri noktalarını (data points) **önceden tanımlanmış sınıflara** (predefined classes) kategorize etmek veya atamak.

**Temel:** Features/attributes (özellikler)

---

## 📊 CLASSIFICATION TÜRLERİ

### 1. BINARY CLASSIFICATION (İkili Sınıflandırma)

**Tanım:** Output **2 sınıfa** ayrılır

**Örnekler:**

| Uygulama | Input | Output Classes | Açıklama |
|----------|-------|----------------|----------|
| **Spam Detection** | Email içeriği | Spam / Not Spam | Email spam mi değil mi? |
| **Pass/Fail** | Hours of study | Pass / Fail | Öğrenci geçti mi kaldı mı? |
| **Disease Detection** | Medical data | Disease / Healthy | Hasta mı sağlıklı mı? |
| **Credit Approval** | Customer data | Approve / Reject | Kredi onaylan mı onaylanmasın mı? |

**💡 Binary = 2 seçenek = True/False = Yes/No = 0/1**

---

### 2. MULTI-CLASS CLASSIFICATION (Çok Sınıflı Sınıflandırma)

**Tanım:** Output **3 veya daha fazla sınıfa** ayrılır

**Örnekler:**

| Uygulama | Input | Output Classes | Açıklama |
|----------|-------|----------------|----------|
| **Sentiment Analysis** | Customer review | Positive / Negative / Neutral | Duygu analizi (3 sınıf) |
| **Iris Flower Classification** | Petal, sepal özellikleri | Setosa / Versicolor / Virginica | Çiçek türü (3 sınıf) |
| **Digit Recognition** | Hand-written digit image | 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 | Rakam tanıma (10 sınıf) |
| **Animal Classification** | Animal image | Cat / Dog / Bird / Fish / ... | Hayvan türü (çoklu) |

**💡 Multi-class = 3+ seçenek**

---

## 🧠 LOGISTIC REGRESSION

### Tanım
**Logistic Regression:** Classification için kullanılan basit ama güçlü bir ML algoritması

**Ne Yapar:** Bir şeyin **true veya false** olduğunu tahmin eder

**Önemli:** İsmi "regression" olsa da aslında bir **classification** algoritmasıdır!

---

### Linear Regression vs Logistic Regression

| Özellik | Linear Regression | Logistic Regression |
|---------|-------------------|---------------------|
| **Kullanım** | Regression | Classification |
| **Output** | Continuous (sayı) | Categorical (sınıf) |
| **Fonksiyon** | Straight line (Düz çizgi) | S-shaped curve (S eğrisi) |
| **Denklem** | y = w×x + b | Sigmoid function |
| **Örnek** | House price prediction | Spam detection |

---

## 📐 SIGMOID FUNCTION (S-Shaped Curve)

### Tanım
**Sigmoid Function:** Logistic regression'da kullanılan **S-şeklinde** bir fonksiyon

### Özellikler

**1. Input:**
- Herhangi bir gerçek sayı (real-valued number)
- -∞ ile +∞ arasında

**2. Output:**
- **0 ile 1 arasına sıkıştırır** (squashes)
- Bu range **probability (olasılık)** olarak yorumlanır

**3. Görsel:**
```
1.0 |           ___________
    |          /
0.5 |         /
    |        /
0.0 |_______/
    |
    -∞  0  +∞
```

**💡 Sigmoid = "S" şeklinde = 0-1 arası = Probability**

---

### Sigmoid Fonksiyonunun Avantajları

1. **Probability yorumlama:**
   - Output [0, 1] aralığında
   - Direk probability olarak kullanılabilir

2. **Smooth (Pürüzsüz) fonksiyon:**
   - Her yerde türevlenebilir
   - Optimization için ideal

3. **Non-linear:**
   - Karmaşık decision boundary'ler

---

## 📚 PASS/FAIL ÖRNEĞİ (Binary Classification)

### Problem Tanımı
**Amaç:** Öğrencinin çalışma saatine göre sınavı geçip geçmeyeceğini tahmin etmek

---

### Veri Yapısı

**Features:**
- **Independent Variable (Bağımsız Değişken):** Hours of study (Çalışma saati)

**Output:**
- **Binary:** Pass veya Fail (Geçti veya Kaldı)

**Classes:**
- **Pass class:** Sınavı geçenler
- **Fail class:** Sınavı kalanlar

---

### Logistic Regression ile Çözüm

#### 1. Model Tanımı
**Fonksiyon:** Sigmoid function

**Input:** Hours of study
**Output:** Probability of passing (Geçme olasılığı)

```
Hours of study → Sigmoid Function → Probability (0-1)
```

---

#### 2. Probability Hesaplama

**Sigmoid çıktısı:** 0 ile 1 arası bir sayı

**Örnek:**
- 6 saat çalışan öğrenci → Probability = 0.80 (80%)
- 4 saat çalışan öğrenci → Probability = 0.20 (20%)

---

#### 3. Decision Making (Karar Verme)

**Threshold (Eşik Değeri):** Genellikle **0.5**

**Karar Kuralı:**
```
If Probability > 0.5:
    Class = Pass
Else:
    Class = Fail
```

**Örnekler:**

| Hours of Study | Probability | Threshold | Decision |
|---------------|-------------|-----------|----------|
| 6 hours | 0.80 (80%) | 0.5 | **PASS** (0.80 > 0.5) |
| 4 hours | 0.20 (20%) | 0.5 | **FAIL** (0.20 < 0.5) |
| 5 hours | 0.55 (55%) | 0.5 | **PASS** (0.55 > 0.5) |
| 3 hours | 0.10 (10%) | 0.5 | **FAIL** (0.10 < 0.5) |

---

## 🌸 IRIS FLOWER CLASSIFICATION ÖRNEĞİ (Multi-class)

### Iris Data Set

**Tanım:** Machine learning'de **standart** bir veri seti

**Boyut:**
- **150 instances** (örnekler)
- **3 sınıf** (classes)
- **4 özellik** (features)

---

### Sınıflar (Classes)

**3 Iris Türü:**
1. **Iris-setosa**
2. **Iris-versicolor**
3. **Iris-virginica**

**💡 3 sınıf olduğu için: Multi-class Classification**

---

### Özellikler (Features)

**4 Attribute (Özellik):**
1. **Sepal Length** (Çanak yaprak uzunluğu)
2. **Sepal Width** (Çanak yaprak genişliği)
3. **Petal Length** (Taç yaprak uzunluğu)
4. **Petal Width** (Taç yaprak genişliği)

**Hepsi:** Continuous (sürekli) değerler (cm cinsinden)

---

### Problem Tanımı

**Input:** 4 features (sepal length, sepal width, petal length, petal width)

**Output:** 1 label (Setosa / Versicolor / Virginica)

**Yöntem:** Logistic Regression (Multi-class için genişletilmiş)

---

### Veri Yapısı Örneği

| Sepal Length | Sepal Width | Petal Length | Petal Width | **Species (Label)** |
|--------------|-------------|--------------|-------------|---------------------|
| 5.1 cm | 3.5 cm | 1.4 cm | 0.2 cm | **Setosa** |
| 6.2 cm | 2.9 cm | 4.3 cm | 1.3 cm | **Versicolor** |
| 7.3 cm | 2.9 cm | 6.3 cm | 1.8 cm | **Virginica** |

---

## 🎯 CLASSIFICATION SÜRECİ

### Genel Süreç

```
┌─────────────────────────────────────────┐
│   1. DATA COLLECTION                    │
│   Features + Labels (classes)           │
└────────────────┬────────────────────────┘
                 │
                 ▼
┌─────────────────────────────────────────┐
│   2. TRAINING                           │
│   Classifier learns features→class       │
│   (Logistic Regression uses Sigmoid)    │
└────────────────┬────────────────────────┘
                 │
                 ▼
┌─────────────────────────────────────────┐
│   3. TRAINED CLASSIFIER                 │
│   Model ready for classification        │
└────────────────┬────────────────────────┘
                 │
                 ▼
┌─────────────────────────────────────────┐
│   4. PREDICTION                         │
│   New features → Class label            │
└─────────────────────────────────────────┘
```

---

### Binary Classification Süreci (Pass/Fail Örneği)

```
1. Input: Hours of study
   ↓
2. Sigmoid Function
   ↓
3. Probability (0-1)
   ↓
4. Compare with Threshold (0.5)
   ↓
5. Decision: Pass or Fail
```

---

### Multi-class Classification Süreci (Iris Örneği)

```
1. Input: 4 features (sepal, petal dimensions)
   ↓
2. Logistic Regression (multi-class)
   ↓
3. Probabilities for each class
   (Setosa: 0.1, Versicolor: 0.7, Virginica: 0.2)
   ↓
4. Choose highest probability
   ↓
5. Output: Versicolor (0.7 en yüksek)
```

---

## 🔑 ANAHTAR KELİMELER VE KAVRAMLAR

### Temel Terimler
- ✅ **Classification:** Kategorik output için supervised learning
- ✅ **Category/Label:** Sınıf, etiket
- ✅ **Binary Classification:** 2 sınıf
- ✅ **Multi-class Classification:** 3+ sınıf
- ✅ **Classifier:** Classification yapan model
- ✅ **Predefined Classes:** Önceden tanımlı sınıflar

### Logistic Regression Terimleri
- ✅ **Logistic Regression:** Classification algoritması
- ✅ **Sigmoid Function:** S-shaped curve, 0-1 arası
- ✅ **S-shaped Curve:** S eğrisi
- ✅ **Probability:** Olasılık (0-1)
- ✅ **Threshold:** Eşik değeri (genellikle 0.5)
- ✅ **Squash:** Sıkıştırma (herhangi bir sayıyı 0-1'e)

### Veri Terimleri
- ✅ **Independent Variable:** Bağımsız değişken, input
- ✅ **Dependent Variable:** Bağımlı değişken, output (sınıf)
- ✅ **Instance:** Örnek, tek veri noktası
- ✅ **Attribute:** Özellik, feature

### Iris Veri Seti Terimleri
- ✅ **Sepal:** Çanak yaprak
- ✅ **Petal:** Taç yaprak
- ✅ **Iris-setosa, Iris-versicolor, Iris-virginica:** 3 çiçek türü

---

## 💡 ÖNEMLİ NOTLAR

### 1. Classification vs Regression
**Kolay Hatırlama:**
- **Output sayı mı?** → Regression
- **Output kategori mi?** → Classification

**Örnekler:**
- Fiyat ($250,000) → Regression
- Spam (Yes/No) → Classification
- Sıcaklık (25.5°C) → Regression
- Hayvan türü (Cat/Dog) → Classification

---

### 2. Binary vs Multi-class
**Ayırt Etme:**
- **2 sınıf** → Binary
- **3+ sınıf** → Multi-class

**Örnekler:**
- Pass/Fail → Binary (2)
- Positive/Negative/Neutral → Multi-class (3)
- Setosa/Versicolor/Virginica → Multi-class (3)

---

### 3. Logistic Regression İsmi
**Dikkat:** İsmi "regression" olsa da aslında **classification** yapar!

**Neden "regression"?**
- Sigmoid function matematiksel olarak regression ailesinden
- Ama output categorical → Classification

---

### 4. Sigmoid Function Neden Önemli?
**3 Ana Sebep:**
1. **0-1 arası output** → Probability yorumu
2. **Smooth (Pürüzsüz)** → Türevlenebilir, optimize edilebilir
3. **Non-linear** → Karmaşık pattern'leri öğrenir

---

### 5. Threshold Seçimi
**Genellikle 0.5 ama:**
- Farklı threshold'lar seçilebilir
- Örnek: Kanser tespitinde 0.3 (daha hassas)
- Trade-off: False positive vs False negative

**Pass/Fail Örneği:**
- Threshold = 0.5 → Normal
- Threshold = 0.7 → Daha sıkı (daha az öğrenci geçer)
- Threshold = 0.3 → Daha gevşek (daha çok öğrenci geçer)

---

### 6. Iris Data Set Önemi
**Neden Standart?**
- Küçük (150 örnek)
- Basit (4 feature)
- İyi ayrılmış sınıflar
- Eğitim için ideal

**Kullanım:** ML algoritmaları test etmek için

---

## 🎯 SINAV İÇİN KRİTİK NOKTALAR

### Mutlaka Bilin:
1. **Classification = Categorical output** ✓
2. **Binary = 2 sınıf, Multi-class = 3+ sınıf** ✓
3. **Logistic Regression = Classification algoritması** ✓
4. **Sigmoid = S-shaped, output 0-1 (probability)** ✓
5. **Threshold genellikle 0.5** ✓
6. **Iris data set: 150 instance, 3 sınıf, 4 feature** ✓

### Örnekleri Bilin:
- **Binary:** Spam detection, Pass/Fail
- **Multi-class:** Sentiment (3), Iris (3), Digit (10)
- **Logistic Regression:** Pass/Fail, Iris classification

### Karşılaştırmaları Bilin:
- **Classification vs Regression:** Categorical vs Continuous
- **Binary vs Multi-class:** 2 vs 3+ sınıf
- **Linear Regression vs Logistic Regression:** Straight line vs S-curve

---

## 📊 KARŞILAŞTIRMA TABLOLARI

### Supervised Learning Alt Türleri

| Özellik | Regression | Classification |
|---------|------------|----------------|
| **Output Türü** | Continuous (Sürekli) | Categorical (Kategorik) |
| **Örnek Output** | $250,000 | Spam/Not Spam |
| **Algoritma** | Linear Regression | Logistic Regression |
| **Fonksiyon** | Straight line | S-shaped (Sigmoid) |
| **Kullanım** | Fiyat, sıcaklık, yaş | Sınıf, kategori, etiket |

---

### Classification Türleri

| Özellik | Binary Classification | Multi-class Classification |
|---------|----------------------|---------------------------|
| **Sınıf Sayısı** | 2 | 3+ |
| **Örnek** | Pass/Fail | Setosa/Versicolor/Virginica |
| **Output** | 0 or 1 | 0, 1, 2, ... |
| **Threshold** | Tek (0.5) | Her sınıf için ayrı |

---

## 📋 ÖĞRENME KONTROL LİSTESİ

Kendinize sorun:
- [ ] Classification nedir?
- [ ] Binary vs Multi-class farkı?
- [ ] Logistic Regression ne yapar?
- [ ] Sigmoid function özellikleri?
- [ ] Threshold ne işe yarar?
- [ ] Pass/Fail örneğinde 0.6 probability ne demek?
- [ ] Iris data set'te kaç sınıf var?
- [ ] Independent vs dependent variable?
- [ ] Classification vs Regression farkı?
- [ ] Logistic Regression neden "regression" isminde?

**Hepsine EVET cevabı vermelisiniz!**

---

## ✏️ Kendi Notlarınız İçin Boş Alan

_______________________________________________
_______________________________________________
_______________________________________________
_______________________________________________