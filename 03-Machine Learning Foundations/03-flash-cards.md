# 🎴 FLASHCARDS - Supervised Learning: Classification

## TEMEL KAVRAMLAR

### Kart 1
**Ön Yüz:** Classification nedir?
**Arka Yüz:** 
**Tanım:** Supervised learning problemi. Veri noktalarını önceden tanımlanmış sınıflara (predefined classes) kategorize etmek.

**Amaç:** Sonuca bir **category (kategori)** veya **label (etiket)** atamak.

---

### Kart 2
**Ön Yüz:** Classification ile Regression arasındaki temel fark nedir?
**Arka Yüz:** 
**Classification:**
- Output: **Categorical** (Kategori)
- Örnek: Spam/Not Spam

**Regression:**
- Output: **Continuous** (Sürekli sayı)
- Örnek: Price ($250,000)

**Hatırlama:** Kategori mi sayı mı?

---

## CLASSIFICATION TÜRLERİ

### Kart 3
**Ön Yüz:** Binary Classification nedir? Örnek ver.
**Arka Yüz:** 
**Tanım:** Output **2 sınıfa** ayrılır

**Örnekler:**
- **Spam Detection:** Spam / Not Spam
- **Pass/Fail:** Pass / Fail
- **Disease:** Healthy / Sick
- **Credit:** Approve / Reject

**Hatırlama:** Binary = 2 seçenek

---

### Kart 4
**Ön Yüz:** Multi-class Classification nedir? Örnek ver.
**Arka Yüz:** 
**Tanım:** Output **3 veya daha fazla sınıfa** ayrılır

**Örnekler:**
- **Sentiment:** Positive / Negative / Neutral (3)
- **Iris Flower:** Setosa / Versicolor / Virginica (3)
- **Digit Recognition:** 0, 1, 2, ..., 9 (10)

**Hatırlama:** Multi-class = 3+ seçenek

---

### Kart 5
**Ön Yüz:** Aşağıdakilerden hangileri binary, hangileri multi-class? Spam detection, Sentiment analysis, Pass/Fail, Iris flowers
**Arka Yüz:** 
**Binary (2 sınıf):**
- Spam detection (Spam/Not Spam)
- Pass/Fail

**Multi-class (3+ sınıf):**
- Sentiment analysis (Pos/Neg/Neu - 3)
- Iris flowers (Setosa/Versicolor/Virginica - 3)

---

## LOGISTIC REGRESSION

### Kart 6
**Ön Yüz:** Logistic Regression nedir ve ne yapar?
**Arka Yüz:** 
**Tanım:** Classification için kullanılan basit ML algoritması

**Ne Yapar:** Bir şeyin **true veya false** olduğunu tahmin eder

**Önemli:** İsmi "regression" olsa da **classification** yapar!

---

### Kart 7
**Ön Yüz:** Linear Regression vs Logistic Regression farkı?
**Arka Yüz:** 
| Özellik | Linear | Logistic |
|---------|--------|----------|
| **Kullanım** | Regression | **Classification** |
| **Output** | Continuous | **Categorical** |
| **Fonksiyon** | Straight line | **S-shaped (Sigmoid)** |
| **Örnek** | House price | Spam detection |

---

### Kart 8
**Ön Yüz:** Logistic Regression neden "regression" isminde ama classification yapar?
**Arka Yüz:** 
**Sebep:** Sigmoid function matematiksel olarak regression ailesinden gelir

**Ama:** Output categorical olduğu için classification yapar

**Sonuç:** İsim yanıltıcı, aslında classifier!

---

## SIGMOID FUNCTION

### Kart 9
**Ön Yüz:** Sigmoid Function nedir ve özellikleri?
**Arka Yüz:** 
**Tanım:** S-shaped (S-şeklinde) curve, logistic regression'da kullanılır

**Özellikler:**
1. **Input:** Herhangi bir gerçek sayı (-∞, +∞)
2. **Output:** 0 ile 1 arası (squash/sıkıştırır)
3. **Yorum:** Output probability olarak yorumlanır

---

### Kart 10
**Ön Yüz:** Sigmoid function'ın 3 ana avantajı nedir?
**Arka Yüz:** 
1. **Probability yorumlama:** Output [0,1] → Direk olasılık
2. **Smooth (Pürüzsüz):** Her yerde türevlenebilir → Optimize edilebilir
3. **Non-linear:** Karmaşık decision boundary'ler öğrenir

---

### Kart 11
**Ön Yüz:** Sigmoid function'da "squash" ne demek?
**Arka Yüz:** 
**Squash (Sıkıştırma):** Herhangi bir gerçek sayıyı 0 ile 1 arasına sıkıştırmak

**Örnek:**
- Input: -5 → Output: ~0.007
- Input: 0 → Output: 0.5
- Input: 5 → Output: ~0.993

---

## PASS/FAIL ÖRNEĞİ

### Kart 12
**Ön Yüz:** Pass/Fail classification probleminde input ve output nedir?
**Arka Yüz:** 
**Input:** Hours of study (Çalışma saati)
- Independent variable (Bağımsız değişken)

**Output:** Pass or Fail (Geçti/Kaldı)
- Binary classification
- 2 class: Pass class, Fail class

---

### Kart 13
**Ön Yüz:** Pass/Fail probleminde sigmoid function nasıl kullanılır?
**Arka Yüz:** 
**Süreç:**
1. Input: Hours of study
2. Sigmoid Function işleme
3. Output: Probability of passing (0-1)

**Örnek:**
- 6 saat çalışan → Probability = 0.80 (80% geçme olasılığı)
- 4 saat çalışan → Probability = 0.20 (20% geçme olasılığı)

---

### Kart 14
**Ön Yüz:** Threshold (Eşik değeri) ne işe yarar? Pass/Fail örneğinde nasıl kullanılır?
**Arka Yüz:** 
**Tanım:** Probability'yi class'a çevirmek için kullanılan değer

**Genellikle:** 0.5

**Karar Kuralı:**
```
If Probability > 0.5 → PASS
If Probability ≤ 0.5 → FAIL
```

**Örnek:**
- 0.80 > 0.5 → PASS ✓
- 0.20 < 0.5 → FAIL ✗

---

### Kart 15
**Ön Yüz:** 6 saat çalışan öğrencinin geçme olasılığı %80. Threshold 0.5. Karar?
**Arka Yüz:** 
**Verilen:**
- Hours of study: 6
- Probability: 0.80 (80%)
- Threshold: 0.5

**Karşılaştırma:**
0.80 > 0.5 ✓

**Karar:** **PASS** (Geçti)

---

### Kart 16
**Ön Yüz:** Threshold 0.5 yerine 0.7 seçersek ne değişir?
**Arka Yüz:** 
**Daha Sıkı Kriter:**
- Probability > 0.7 → Pass
- Daha az öğrenci geçer

**Örnek:**
- Prob = 0.65 → 0.5'te PASS, 0.7'de FAIL

**Trade-off:** Daha dikkatli ama daha az geçiren

---

## IRIS FLOWER ÖRNEĞİ

### Kart 17
**Ön Yüz:** Iris Data Set'in 5 özelliğini say.
**Arka Yüz:** 
1. **150 instances** (örnekler)
2. **3 classes** (Setosa, Versicolor, Virginica)
3. **4 features** (Sepal length, Sepal width, Petal length, Petal width)
4. **Standard** ML veri seti
5. **Multi-class classification** problemi

---

### Kart 18
**Ön Yüz:** Iris Data Set'te 3 sınıf (class) nelerdir?
**Arka Yüz:** 
1. **Iris-setosa**
2. **Iris-versicolor**
3. **Iris-virginica**

**Not:** 3 farklı iris çiçeği türü

---

### Kart 19
**Ön Yüz:** Iris Data Set'te 4 özellik (feature/attribute) nelerdir?
**Arka Yüz:** 
1. **Sepal Length** (Çanak yaprak uzunluğu)
2. **Sepal Width** (Çanak yaprak genişliği)
3. **Petal Length** (Taç yaprak uzunluğu)
4. **Petal Width** (Taç yaprak genişliği)

**Hepsi:** Continuous değerler (cm)

---

### Kart 20
**Ön Yüz:** Iris classification binary mi multi-class mi? Neden?
**Arka Yüz:** 
**Cevap:** **Multi-class**

**Neden:** 3 sınıf var (Setosa, Versicolor, Virginica)

**Kural:** 3+ sınıf = Multi-class

---

### Kart 21
**Ön Yüz:** Iris classification'da input ve output nedir?
**Arka Yüz:** 
**Input:** 4 features
- Sepal length, Sepal width
- Petal length, Petal width

**Output:** 1 label (sınıf)
- Setosa / Versicolor / Virginica

**Algoritma:** Logistic Regression (multi-class için genişletilmiş)

---

### Kart 22
**Ön Yüz:** Iris Data Set neden "standard" ML veri seti?
**Arka Yüz:** 
**Nedenler:**
1. Küçük (150 örnek) → Hızlı
2. Basit (4 feature) → Anlaşılır
3. İyi ayrılmış sınıflar → Öğrenme kolay
4. Eğitim için ideal

**Kullanım:** ML algoritmalarını test etmek

---

## VERİ TERİMLERİ

### Kart 23
**Ön Yüz:** Independent variable (Bağımsız değişken) nedir? Örnek ver.
**Arka Yüz:** 
**Tanım:** Diğer değişkenlere bağlı olmayan, **input** olan değişken

**Pass/Fail örneği:** Hours of study

**Iris örneği:** Sepal length, petal width vb.

---

### Kart 24
**Ön Yüz:** Dependent variable (Bağımlı değişken) nedir? Örnek ver.
**Arka Yüz:** 
**Tanım:** Diğer değişkenlere **bağlı** olan, **output** olan değişken

**Pass/Fail örneği:** Pass/Fail (çalışma saatine bağlı)

**Iris örneği:** Flower species (özelliklere bağlı)

---

### Kart 25
**Ön Yüz:** Classifier nedir?
**Arka Yüz:** 
**Tanım:** Classification yapan model

**Örnekler:**
- Logistic Regression
- Decision Tree
- Neural Network

**Görev:** Veri noktalarını sınıflara atamak

---

### Kart 26
**Ön Yüz:** "Predefined classes" ne demek?
**Arka Yüz:** 
**Tanım:** Önceden tanımlanmış sınıflar

**Anlamı:** Sınıflar model eğitiminden önce bellidir

**Örnekler:**
- Pass/Fail → 2 predefined class
- Setosa/Versicolor/Virginica → 3 predefined class

---

## CLASSIFICATION SÜRECİ

### Kart 27
**Ön Yüz:** Classification sürecinin 4 adımını sırala.
**Arka Yüz:** 
1. **Data Collection:** Features + Labels (classes)
2. **Training:** Classifier learns features→class
3. **Trained Classifier:** Model ready
4. **Prediction:** New features → Class label

---

### Kart 28
**Ön Yüz:** Binary classification sürecini Pass/Fail örneği ile açıkla.
**Arka Yüz:** 
1. **Input:** Hours of study
2. **Sigmoid Function:** İşleme
3. **Probability:** 0-1 arası değer
4. **Compare:** Threshold (0.5) ile karşılaştır
5. **Decision:** Pass or Fail

---

### Kart 29
**Ön Yüz:** Multi-class classification sürecini Iris örneği ile açıkla.
**Arka Yüz:** 
1. **Input:** 4 features (sepal, petal)
2. **Logistic Regression:** Multi-class
3. **Probabilities:** Her sınıf için ayrı
   - Setosa: 0.1, Versicolor: 0.7, Virginica: 0.2
4. **Choose:** En yüksek probability
5. **Output:** Versicolor (0.7)

---

## KARŞILAŞTIRMALAR

### Kart 30
**Ön Yüz:** Regression vs Classification - Output türü, örnek, algoritma?
**Arka Yüz:** 
**Regression:**
- Output: Continuous
- Örnek: House price ($250,000)
- Algoritma: Linear Regression

**Classification:**
- Output: Categorical
- Örnek: Spam (Yes/No)
- Algoritma: Logistic Regression

---

### Kart 31
**Ön Yüz:** Binary vs Multi-class - Sınıf sayısı, örnekler?
**Arka Yüz:** 
**Binary:**
- Sınıf: 2
- Örnekler: Pass/Fail, Spam/Ham

**Multi-class:**
- Sınıf: 3+
- Örnekler: Sentiment (3), Iris (3), Digits (10)

---

### Kart 32
**Ön Yüz:** Linear Regression vs Logistic Regression - Fonksiyon ve görsel?
**Arka Yüz:** 
**Linear Regression:**
- Fonksiyon: Straight line (Düz çizgi)
- y = w×x + b

**Logistic Regression:**
- Fonksiyon: S-shaped curve (Sigmoid)
- 0-1 arası output

---

## ÖZEL DURUMLAR

### Kart 33
**Ön Yüz:** Logistic Regression hem binary hem multi-class'ta kullanılabilir mi?
**Arka Yüz:** 
**EVET!**

**Binary:** Tek sigmoid (Pass/Fail)

**Multi-class:** Her sınıf için ayrı sigmoid veya softmax
- One-vs-Rest (OvR) approach
- Iris örneği: 3 sınıf için genişletilmiş

---

### Kart 34
**Ön Yüz:** Probability 0.5 ise (threshold da 0.5), karar ne olur?
**Arka Yüz:** 
**Genellikle:** 

```
If Probability > 0.5 → Pass
If Probability ≤ 0.5 → Fail
```

**Yani:** 0.5 = FAIL (eşitlik durumunda negatif sınıf)

**Ama:** Uygulamaya göre değişebilir

---

### Kart 35
**Ön Yüz:** Sepal ve Petal nedir? (Iris data set)
**Arka Yüz:** 
**Sepal (Çanak yaprak):**
- Çiçeğin dış koruyucu yaprakları
- Genellikle yeşil

**Petal (Taç yaprak):**
- Çiçeğin renkli iç yaprakları
- Görsel çekicilik sağlar

**Iris'te:** Her ikisinin de length ve width ölçülür

---

## PRATIK UYGULAMALAR

### Kart 36
**Ön Yüz:** Spam detection binary mi multi-class mi? Input ve output?
**Arka Yüz:** 
**Tür:** **Binary Classification**

**Input:** Email içeriği (kelimeler, gönderen vb.)
**Output:** Spam / Not Spam (2 sınıf)

**Algoritma:** Logistic Regression

---

### Kart 37
**Ön Yüz:** Sentiment analysis binary mi multi-class mi? Sınıflar?
**Arka Yüz:** 
**Tür:** **Multi-class Classification**

**Sınıflar:** 
- Positive (Pozitif)
- Negative (Negatif)
- Neutral (Nötr)

**Toplam:** 3 sınıf

---

### Kart 38
**Ön Yüz:** Digit recognition (0-9) binary mi multi-class mi?
**Arka Yüz:** 
**Tür:** **Multi-class Classification**

**Sınıflar:** 0, 1, 2, 3, 4, 5, 6, 7, 8, 9

**Toplam:** 10 sınıf

**Input:** El yazısı rakam görüntüsü

---

## SINAV SORULARI

### Kart 39
**Ön Yüz:** Output "Cat", "Dog", "Bird" ise hangi classification türü ve kaç sınıf?
**Arka Yüz:** 
**Tür:** **Multi-class Classification**

**Sınıf Sayısı:** 3 (Cat, Dog, Bird)

**Kural:** 3+ sınıf → Multi-class

---

### Kart 40
**Ön Yüz:** Bir öğrenci 5 saat çalışmış, geçme olasılığı 0.55. Threshold 0.5. Geçer mi?
**Arka Yüz:** 
**Verilen:**
- Hours: 5
- Probability: 0.55
- Threshold: 0.5

**Karşılaştırma:**
0.55 > 0.5 ✓

**Karar:** **PASS** (Geçer)

---

## 📝 Çalışma Stratejisi

**Öncelik Sırası:**
⭐⭐⭐ Yüksek: Kart 1-8, 12-16, 17-22, 27-32, 39-40
⭐⭐ Orta: Kart 9-11, 23-26, 33-38
⭐ Düşük: İleri seviye detaylar

**Günlük Plan:**
- Gün 1: Temel kavramlar + Logistic Regression (1-16)
- Gün 2: Iris örneği + Süreç (17-29)
- Gün 3: Karşılaştırmalar + Pratik (30-40)

**İpucu:** Binary vs Multi-class farkını ÇOK İYİ bilin!