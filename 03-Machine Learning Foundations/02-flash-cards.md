# 🎴 FLASHCARDS - Supervised Learning: Regression

## TEMEL KAVRAMLAR

### Kart 1
**Ön Yüz:** Supervised Learning output türüne göre 2 yönteme ayrılır. Bunlar nelerdir?
**Arka Yüz:** 
1. **Regression:** Output continuous (sürekli) olduğunda
2. **Classification:** Output categorical (kategorik) olduğunda

---

### Kart 2
**Ön Yüz:** Regression ne zaman kullanılır? Örnek ver.
**Arka Yüz:** 
**Ne zaman:** Output **continuous (sürekli sayısal)** olduğunda

**Örnekler:**
- House price: $250,000
- Temperature: 25.5°C
- Age: 30 years
- Stock price: $150.75

---

### Kart 3
**Ön Yüz:** Classification ne zaman kullanılır? Örnek ver.
**Arka Yüz:** 
**Ne zaman:** Output **categorical (kategori/sınıf)** olduğunda

**Örnekler:**
- Spam: Yes/No
- Cancer: Malignant/Benign
- Sentiment: Positive/Negative/Neutral
- Animal: Cat/Dog

---

## LINEAR REGRESSION

### Kart 4
**Ön Yüz:** Linear Regression denklemi nedir? Terimleri açıkla.
**Arka Yüz:** 
```
f(x) = w × x + b
```

- **f(x) veya y:** Output/Prediction (Tahmin)
- **x:** Input (Girdi)
- **w:** Weight/Slope (Ağırlık/Eğim)
- **b:** Bias/Y-intercept (Sapma/Y-kesişim)

---

### Kart 5
**Ön Yüz:** Linear Regression'da w (weight) ne işe yarar?
**Arka Yüz:** 
**w = Slope (Eğim)**

**Anlamı:** Output'un input'a göre değişim oranı

**House price örneği:**
w = 200 → Her 1 sq ft artışta $200 artış

**Etkisi:**
- w ↑ → Çizgi daha dik ↗
- w ↓ → Çizgi daha yatık →

---

### Kart 6
**Ön Yüz:** Linear Regression'da b (bias) ne işe yarar?
**Arka Yüz:** 
**b = Y-intercept (Y-kesişim noktası)**

**Anlamı:** Input = 0 olduğunda output değeri

**Etkisi:**
- b ↑ → Çizgi yukarı kayar ↑
- b ↓ → Çizgi aşağı kayar ↓

---

### Kart 7
**Ön Yüz:** Linear Regression'da optimal w ve b nasıl bulunur?
**Arka Yüz:** 
**Iteratively (Tekrarlı) ayarlama:**

1. İlk w ve b değerleri ile başla
2. Tahmin yap: ŷ = w×x + b
3. Loss hesapla: (ŷ - y)²
4. w ve b'yi ayarla (loss azalacak şekilde)
5. Loss minimum olana kadar tekrar et

---

## VERİ TERİMLERİ

### Kart 8
**Ön Yüz:** Independent Feature (Bağımsız Özellik) nedir?
**Arka Yüz:** 
**Tanım:** Diğer özelliklere bağlı olmayan, **input** olan özellik

**Başka adları:** Input feature, X

**House price örneği:** House Size (Ev büyüklüğü)

**Hatırlama:** Independent = SEBEP = INPUT

---

### Kart 9
**Ön Yüz:** Dependent Feature (Bağımlı Özellik) nedir?
**Arka Yüz:** 
**Tanım:** Diğer özelliklere **bağlı** olan, **output** olan özellik

**Başka adları:** Output label, Y

**House price örneği:** Price (Fiyat) - Size'a BAĞLI

**Hatırlama:** Dependent = SONUÇ = OUTPUT

---

### Kart 10
**Ön Yüz:** Training Example (Eğitim Örneği) / Tuple nedir?
**Arka Yüz:** 
**Tanım:** Tek bir satır veri (Input + Output)

**House price örneği:**
(1000 sq ft, $200,000) ← Bu bir training example/tuple

---

### Kart 11
**Ön Yüz:** Training Data Set nedir?
**Arka Yüz:** 
**Tanım:** Tüm training example'ların (tuple'ların) toplamı

**Kullanım:** Model oluşturmak için kullanılan veri seti

---

### Kart 12
**Ön Yüz:** Scatter Plot neden kullanılır?
**Arka Yüz:** 
**Amaç:** Input ve output arasındaki ilişkiyi görselleştirmek

**Faydası:**
- Pattern'i görmek
- İlişkiyi anlamak
- Çizgi uydurma için

**Örnek:** House Size vs Price scatter plot → Pozitif korelasyon görülür

---

## HATA VE KAYIP

### Kart 13
**Ön Yüz:** Error (Hata) nasıl hesaplanır?
**Arka Yüz:** 
```
Error = Predicted Value - Actual Value
Error = ŷ - y
```

**Örnek:**
- Actual Price (y): $250,000
- Predicted Price (ŷ): $230,000
- Error: -$20,000

---

### Kart 14
**Ön Yüz:** Loss (Kayıp) nedir?
**Arka Yüz:** 
**Tanım:** Kötü tahmin için ceza (penalty)

**Kurallar:**
- Perfect prediction → Loss = 0
- Bad prediction → Loss yüksek

**Amaç:** Loss'u minimize etmek

---

### Kart 15
**Ön Yüz:** Squared Loss nasıl hesaplanır ve neden kullanılır?
**Arka Yüz:** 
**Hesaplama:**
```
Squared Loss = (Predicted - Actual)²
Squared Loss = (ŷ - y)²
```

**Neden kare alınır:**
1. Negatif değerleri pozitif yapar
2. Büyük hataları daha fazla cezalandırır
3. Matematiksel olarak optimize edilmesi kolay

---

### Kart 16
**Ön Yüz:** Loss = 0 ne zaman olur?
**Arka Yüz:** 
**Koşul:** Predicted = Actual olduğunda

```
If ŷ = y
Then Loss = (ŷ - y)² = 0² = 0
```

**Gerçekte:** Perfect prediction nadirdir, goal loss'u minimize etmektir.

---

## SUPERVISED LEARNING UYGULAMALARI

### Kart 17
**Ön Yüz:** House Price Prediction'da input ve output nedir? Hangi tür?
**Arka Yüz:** 
**Input:** House size (square feet)
**Output:** Price (dolar)
**Tür:** **Regression** (çünkü output continuous)

---

### Kart 18
**Ön Yüz:** Cancer Detection'da input ve output nedir? Hangi tür?
**Arka Yüz:** 
**Input:** Medical details (Tıbbi detaylar)
**Output:** Malignant or not (Kötü huylu mu değil mi)
**Tür:** **Classification** (çünkü output categorical)

---

### Kart 19
**Ön Yüz:** Sentiment Analysis'te input ve output nedir? Hangi tür?
**Arka Yüz:** 
**Input:** Customer reviews (Müşteri yorumları)
**Output:** Positive, Negative, or Neutral
**Tür:** **Classification** (çünkü output categorical)

---

### Kart 20
**Ön Yüz:** Stock Price Prediction'da input ve output nedir? Hangi tür?
**Arka Yüz:** 
**Input:** Opening price, closing price, volume traded
**Output:** Stock price
**Tür:** **Regression** (çünkü output continuous)

---

## ÖĞRETMEN-ÖĞRENCİ ANALOJİSİ

### Kart 21
**Ön Yüz:** Supervised Learning'i öğretmen-öğrenci analojisi ile açıkla.
**Arka Yüz:** 
**Teacher (Öğretmen):** Past outcomes = Labels
**Student (Öğrenci):** Model
**Learning (Öğrenme):** Input-output ilişkisini öğrenme

Model, geçmiş sonuçlardan (labeled data) öğrenir, tıpkı öğretmenin öğrenciye öğretmesi gibi.

---

## LINEAR REGRESSION SÜRECİ

### Kart 22
**Ön Yüz:** Linear Regression training sürecinin 6 adımını sırala.
**Arka Yüz:** 
1. **Data Collection:** Input + Output topla
2. **Visualization:** Scatter plot ile pattern gör
3. **Model Definition:** f(x) = w×x + b
4. **Training:** w ve b'yi iteratif ayarla
5. **Trained Model:** Optimal w ve b bulundu
6. **Prediction:** Yeni input → Tahmin

---

### Kart 23
**Ön Yüz:** Model training'de iterasyon (iteration) ne demek?
**Arka Yüz:** 
**Tanım:** Tekrarlı, döngüsel süreç

**Süreç:**
1. Predict (Tahmin yap)
2. Calculate Loss (Kayıp hesapla)
3. Adjust w and b (Ağırlık ve bias'ı ayarla)
4. Repeat (Tekrarla)

**Ne zaman durur:** Loss minimum olduğunda

---

## KARŞILAŞTIRMALAR

### Kart 24
**Ön Yüz:** Regression vs Classification - Temel fark?
**Arka Yüz:** 
**Regression:**
- Output: Continuous (Sayısal)
- Örnek: Price ($250,000)

**Classification:**
- Output: Categorical (Kategori)
- Örnek: Spam (Yes/No)

**Hatırlama:** Regression = Numbers, Classification = Categories

---

### Kart 25
**Ön Yüz:** Independent vs Dependent feature farkı? House price örneği.
**Arka Yüz:** 
**Independent (Bağımsız):**
- Sebep, Input, X
- Örnek: House Size

**Dependent (Bağımlı):**
- Sonuç, Output, Y
- Örnek: Price (size'a bağlı!)

**İlişki:** Price DEPENDS ON Size

---

### Kart 26
**Ön Yüz:** Error vs Loss farkı?
**Arka Yüz:** 
**Error:**
- Fark: ŷ - y
- Pozitif veya negatif olabilir

**Loss:**
- Hata için ceza
- Her zaman pozitif: (ŷ - y)²
- Minimize edilmeli

---

## MATEMATİKSEL İLİŞKİLER

### Kart 27
**Ön Yüz:** w artarsa çizgi nasıl değişir? b artarsa?
**Arka Yüz:** 
**w (slope) artar:**
- Çizgi daha **dik** olur ↗
- Daha büyük eğim

**b (bias) artar:**
- Çizgi **yukarı** kayar ↑
- Paralel hareket

---

### Kart 28
**Ön Yüz:** House price prediction'da w = 200 ne anlama gelir?
**Arka Yüz:** 
**Anlamı:** Her 1 square foot artışta, price $200 artar

**Matematiksel:**
- Slope (eğim) = Değişim oranı
- w = ΔPrice / ΔSize = 200

---

## ÖRNEKLER

### Kart 29
**Ön Yüz:** House size 1,100 sq ft ise ve çizgi denklemimiz f(x) = 200x + 50,000 ise, price tahmini nedir?
**Arka Yüz:** 
```
f(1100) = 200 × 1100 + 50,000
f(1100) = 220,000 + 50,000
f(1100) = $270,000
```

**Predicted Price: $270,000**

---

### Kart 30
**Ön Yüz:** Actual price $250,000, predicted price $230,000. Error, squared loss ve interpretation?
**Arka Yüz:** 
**Error:** 
ŷ - y = $230,000 - $250,000 = -$20,000

**Squared Loss:**
(-20,000)² = 400,000,000

**Interpretation:** Model $20,000 düşük tahmin yaptı (underestimated)

---

## ÖZEL DURUMLAR

### Kart 31
**Ön Yüz:** Linear Regression'da "best fitting line" nasıl bulunur?
**Arka Yüz:** 
**Yöntem:** w ve b'yi iteratif ayarlayarak squared loss'u minimize etme

**Süreç:**
- Birçok w ve b kombinasyonu denenmiş gibi
- Her kombinasyon için loss hesaplanır
- En düşük loss veren = Best fitting line

---

### Kart 32
**Ön Yüz:** Supervised Learning'de "mapping" ne demek?
**Arka Yüz:** 
**Mapping:** Input ve output arasındaki ilişki/fonksiyon

**Matematiksel:** f: X → Y

**House price:** 
- X (size) → Y (price) mapping'i öğrenilir
- f(size) = price

---

### Kart 33
**Ön Yüz:** Linear Regression hangi supervised learning alt türüdür?
**Arka Yüz:** 
**Alt Tür:** **Regression**

**Çünkü:**
- Output continuous
- Doğrusal (linear) bir ilişki varsayar
- f(x) = w×x + b denklemi kullanır

---

### Kart 34
**Ön Yüz:** Bir modelin "trained" olması ne demek?
**Arka Yüz:** 
**Anlamı:** Optimal w ve b değerleri bulundu

**Süreç tamamlandı:**
- Training data kullanıldı
- Loss minimize edildi
- Model kullanıma hazır

**Artık:** Yeni input → Prediction yapabilir

---

## PRATIK UYGULAMALAR

### Kart 35
**Ön Yüz:** Hangi problemler regression, hangileri classification? Listeden ayır: House price, Email spam, Stock price, Sentiment, Age prediction
**Arka Yüz:** 
**Regression (Continuous):**
- House price → Sayısal
- Stock price → Sayısal
- Age prediction → Sayısal

**Classification (Categorical):**
- Email spam → Yes/No
- Sentiment → Pos/Neg/Neu

---

### Kart 36
**Ön Yüz:** Training data set'iniz: [(1000, 200K), (1500, 300K), (2000, 400K)]. Independent ve dependent feature'lar?
**Arka Yüz:** 
**Format:** (House Size, Price)

**Independent Feature (X):** 
- House Size: 1000, 1500, 2000

**Dependent Feature (Y):**
- Price: 200K, 300K, 400K

**Training Examples:** 3 tane

---

## İLERİ SEVIYE

### Kart 37
**Ön Yüz:** Loss function olarak başka ne kullanılabilir? Squared loss'un avantajı?
**Arka Yüz:** 
**Alternatifler:**
- Absolute loss: |ŷ - y|
- Huber loss: Kombinasyon

**Squared Loss Avantajları:**
1. Her yerde türevlenebilir (differentiable)
2. Büyük hataları cezalandırır
3. Tek global minimum var
4. Matematiksel olarak kolay

---

### Kart 38
**Ön Yüz:** Linear Regression'ın limitasyonu nedir?
**Arka Yüz:** 
**Ana Limitasyon:** Sadece **linear (doğrusal)** ilişkileri modelleyebilir

**Sorun:** Gerçek dünyada birçok ilişki non-linear

**Çözüm:** Polynomial regression, neural networks vb.

---

### Kart 39
**Ön Yüz:** Multiple features olursa linear regression denklemi nasıl olur?
**Arka Yüz:** 
**Tek feature:**
f(x) = w × x + b

**Multiple features:**
f(x) = w₁×x₁ + w₂×x₂ + ... + wₙ×xₙ + b

**House price örneği:**
- x₁ = Size
- x₂ = Bedrooms
- x₃ = Age
→ f(x) = w₁×size + w₂×bedrooms + w₃×age + b

---

### Kart 40
**Ön Yüz:** Supervised Learning'de "labeled data" neden kritik?
**Arka Yüz:** 
**Neden kritik:**
- Model, features→labels ilişkisini öğrenir
- Labels olmadan supervised learning yapılamaz
- Labels = "doğru cevaplar" = öğretmen

**Analoji:** Sınavda cevap anahtarı olmadan nasıl öğrenilir?

---

## 📝 Çalışma Stratejisi

**Öncelik Sırası:**
⭐⭐⭐ Yüksek: Kart 1-7, 13-16, 22, 24-25, 29-30
⭐⭐ Orta: Kart 8-12, 17-21, 23, 26-28, 31-36
⭐ Düşük: Kart 37-40 (ileri seviye)

**Günlük Plan:**
- Gün 1: Temel kavramlar (1-16)
- Gün 2: Uygulamalar + Süreç (17-28)
- Gün 3: Örnekler + İleri (29-40)

**İpucu:** Regression vs Classification farkını çok iyi bilin!