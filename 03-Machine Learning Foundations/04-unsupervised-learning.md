# 📚 GÜN 2: UNSUPERVISED LEARNING - Detaylı Çalışma Notu

## 🎯 Modül Özeti
Bu modül Unsupervised Learning'i, clustering algoritmasını, similarity (benzerlik) kavramını ve clustering sürecini açıklıyor.

---

## 📖 UNSUPERVISED LEARNING NEDİR? (HATIRLATMA)

### Tanım
**Unsupervised Learning:** **Unlabeled (etiketsiz)** veri ile çalışan machine learning türü

**Amaç:** Verideki **pattern'leri** ve **yapıları** keşfetmek

**Ana Yöntem:** **CLUSTERING** (Kümeleme)

---

## 💼 UNSUPERVISED LEARNING KULLANIM ALANLARI

### 1. Customer Segmentation (Müşteri Segmentasyonu)
**Ne Yapar:** Müşterileri benzer gruplara ayırır

**Kullanım:**
- Hedefli pazarlama
- Kişiselleştirilmiş hizmetler
- Müşteri analizi

---

### 2. Anomaly Detection (Anormallik Tespiti)
**Ne Yapar:** Normal olmayan pattern'leri bulur

**Kullanım:**
- Fraud detection (Dolandırıcılık)
- Network intrusion (Ağ saldırısı)
- Manufacturing defects (Üretim hataları)

---

### 3. Recommendation Systems (Öneri Sistemleri) ⭐

#### Örnek: Netflix Movie Recommendations

**Input:** Users' movie viewing history (Kullanıcıların izleme geçmişi)

**Clustering:**
- Kullanıcılar **izledikleri film türlerine** veya **verdikleri puanlara** göre gruplandırılır
- Benzer kullanıcılar aynı cluster'da

**Output:** Kişiselleştirilmiş film önerileri

**Süreç:**
```
User A → Horror, Thriller izlemiş → Cluster 1
User B → Horror, Thriller izlemiş → Cluster 1
User C → Romance, Comedy izlemiş → Cluster 2

User A'ya → Cluster 1'deki diğer kullanıcıların beğendiği filmler önerilir
```

**💡 Aynı mantık müzik önerileri için de geçerli (Spotify, Apple Music)**

---

## 🎯 SİMİLARİTY (BENZERLİK) KAVRAMI

### Tanım
**Similarity:** İki veri noktasının birbirine ne kadar yakın olduğu

### Özellikler

**1. Değer Aralığı:**
```
Similarity ∈ [0, 1]

0 = Hiç benzer değil
1 = Tamamen benzer
```

**2. Önemi:**
- Hangi cluster'a düşeceğini belirler
- Clustering için **kritik** kavram

---

### Örnek: Meyve Sepeti

**Senaryo:** Bir meyve sepetinden benzer meyveleri tanımla

**Özellik:** Renk (Color)

**Karşılaştırma:**
- **Apple (Elma):** Kırmızı
- **Cherry (Kiraz):** Kırmızı
- **Banana (Muz):** Sarı

**Similarity:**
```
Apple ↔ Cherry (İkisi de kırmızı)
Similarity ≈ 0.9 (Çok benzer, 1'e yakın)

Apple ↔ Banana (Biri kırmızı, diğeri sarı)
Similarity ≈ 0.2 (Az benzer, 0'a yakın)
```

**Kural:** Similarity yüksek → Aynı cluster'a düşme ihtimali yüksek

---

## 📊 SİMİLARİTY MEASURES (BENZERLİK ÖLÇÜLERİ)

### 1. Euclidean Distance (Öklid Uzaklığı) ⭐

**Tanım:** İki nokta arasındaki düz çizgi mesafesi

**Formül:**
```
d = √[(x₂-x₁)² + (y₂-y₁)²]
```

**2D Örnek:**
```
Point A: (1, 2)
Point B: (4, 6)

Distance = √[(4-1)² + (6-2)²]
         = √[9 + 16]
         = √25 = 5
```

**Kullanım:** En yaygın, genel amaçlı

**Özellik:** Küçük distance → Yüksek similarity

---

### 2. Manhattan Distance (Manhattan Uzaklığı)

**Tanım:** İki nokta arası "şehir blokları" mesafesi (sadece yatay ve dikey)

**Formül:**
```
d = |x₂-x₁| + |y₂-y₁|
```

**2D Örnek:**
```
Point A: (1, 2)
Point B: (4, 6)

Distance = |4-1| + |6-2|
         = 3 + 4 = 7
```

**Kullanım:** Grid-based veriler, şehir haritaları

---

### 3. Cosine Similarity (Kosinüs Benzerliği)

**Tanım:** İki vektör arasındaki açının kosinüsü

**Değer:**
```
Cosine Similarity ∈ [-1, 1]

1 = Aynı yön
0 = Dik açı
-1 = Ters yön
```

**Kullanım:** Text mining, document similarity

**Avantaj:** Büyüklük (magnitude) önemli değil, sadece yön

---

### 4. Jaccard Similarity (Jaccard Benzerliği)

**Tanım:** İki kümenin kesişiminin birleşime oranı

**Formül:**
```
Jaccard = |A ∩ B| / |A ∪ B|
```

**Örnek:**
```
Set A = {1, 2, 3, 4}
Set B = {3, 4, 5, 6}

A ∩ B = {3, 4} → 2 eleman
A ∪ B = {1, 2, 3, 4, 5, 6} → 6 eleman

Jaccard = 2/6 = 0.33
```

**Kullanım:** Set veriler, presence/absence data

---

## 🔄 UNSUPERVISED LEARNING WORKFLOW (5 ADIM)

### Adım 1: PREPARE THE DATA (Veri Hazırlama)

**Preprocessing Adımları:**

#### a) Removing Missing Values (Eksik Değerleri Kaldırma)
- Null/NA değerleri temizle
- Eksik veriyi doldur (imputation) veya sil

#### b) Normalizing the Data (Veriyi Normalize Etme)
- Farklı ölçekleri aynı range'e getir
- Örnek: [0, 1] veya [-1, 1] aralığına

**Neden gerekli?**
```
Feature 1: Age (18-80) → Küçük range
Feature 2: Income ($20K-$200K) → Büyük range

Normalize olmadan → Income feature baskın olur!
```

#### c) Feature Scaling (Özellik Ölçeklendirme)
- Standardization (Standartlaştırma): Mean=0, Std=1
- Min-Max Scaling: [0, 1] aralığına

**💡 Preprocessing çok önemli! "Garbage in, garbage out"**

---

### Adım 2: CREATE SIMILARITY MATRIX (Benzerlik Matrisi Oluşturma)

**Similarity Matrix Nedir?**
- Her veri noktası çifti arasındaki benzerlik değerleri
- n veri → n×n matris

**Örnek: 4 Meyve**

|       | Apple | Cherry | Banana | Orange |
|-------|-------|--------|--------|--------|
| **Apple**  | 1.0   | 0.9    | 0.2    | 0.6    |
| **Cherry** | 0.9   | 1.0    | 0.1    | 0.5    |
| **Banana** | 0.2   | 0.1    | 1.0    | 0.7    |
| **Orange** | 0.6   | 0.5    | 0.7    | 1.0    |

**Gözlem:**
- Apple ↔ Cherry: 0.9 (Yüksek benzerlik)
- Banana ↔ Orange: 0.7 (Orta benzerlik)
- Apple ↔ Banana: 0.2 (Düşük benzerlik)

**Hangi Similarity Metric?**
- **Veri doğasına** (nature of data) bağlı
- **Clustering algoritmasına** bağlı

---

### Adım 3: RUN CLUSTERING ALGORITHM (Clustering Algoritması Çalıştırma)

**Süreç:**
1. Similarity matrix'i kullan
2. Benzer veri noktalarını grupla
3. Cluster'lar oluştur

---

#### Clustering Algoritması Türleri (4 Ana Tür)

**1. Partition-Based (Bölümleme Tabanlı)**
- **Örnekler:** K-Means, K-Medoids
- **Mantık:** Veriyi K adet cluster'a böl
- **Kullanım:** En yaygın, hızlı

**2. Hierarchical-Based (Hiyerarşik Tabanlı)**
- **Örnekler:** Agglomerative, Divisive
- **Mantık:** Ağaç yapısı (dendrogram) oluştur
- **Kullanım:** Hiyerarşik ilişkiler

**3. Density-Based (Yoğunluk Tabanlı)**
- **Örnekler:** DBSCAN, OPTICS
- **Mantık:** Yoğun bölgeleri cluster yap
- **Kullanım:** Gürültülü veri, irregular şekiller

**4. Distribution-Based (Dağılım Tabanlı)**
- **Örnekler:** Gaussian Mixture Models (GMM)
- **Mantık:** Verinin istatistiksel dağılımı
- **Kullanım:** Probabilistic clustering

---

### Adım 4: INTERPRET THE RESULTS (Sonuçları Yorumlama)

**Ne Yapılır:**
- Cluster'ları incele
- Her cluster'ın özelliklerini anla
- Mantıklı mı kontrol et

**Örnek: Customer Segmentation**
```
Cluster 1: Yüksek gelirli, genç müşteriler
Cluster 2: Orta gelirli, aileli müşteriler
Cluster 3: Düşük gelirli, öğrenci müşteriler
```

---

### Adım 5: ADJUST CLUSTERING (Clustering'i Ayarla)

**Neden Gerekli?**
- İlk denemede mükemmel sonuç gelmeyebilir
- **Iterative (yinelemeli)** ve **exploratory (keşfedici)** süreç

**Sorun: "Ground Truth" Yok!**
- Labeled output olmadığı için sonucu doğrulamak zor
- **Ground truth:** Doğru cevaplar (Supervised'da var, Unsupervised'da YOK!)

**Verification (Doğrulama):**
1. **Cluster level:** Cluster'lar mantıklı mı?
2. **Example level:** Bireysel örnekler doğru cluster'da mı?
3. **Expectations:** Beklentilerimizle uyuşuyor mu?

**İyileştirme:**
- Önceki adımları tekrarla
- Farklı preprocessing dene
- Farklı similarity metric dene
- Farklı clustering algoritması dene
- Cluster sayısını değiştir

**💡 Deneme-yanılma (trial and error) süreci!**

---

## 🔑 ANAHTAR KELİMELER VE KAVRAMLAR

### Temel Terimler
- ✅ **Unsupervised Learning:** Unlabeled data ile öğrenme
- ✅ **Clustering:** Benzer veri noktalarını gruplama
- ✅ **Cluster:** Benzer verilerin grubu
- ✅ **Similarity:** Benzerlik (0-1 arası)
- ✅ **Similarity Matrix:** Benzerlik matrisi (n×n)
- ✅ **Pattern Discovery:** Pattern keşfi

### Similarity Measures
- ✅ **Euclidean Distance:** Düz çizgi mesafesi (en yaygın)
- ✅ **Manhattan Distance:** Şehir blokları mesafesi
- ✅ **Cosine Similarity:** Açı benzerliği (text için)
- ✅ **Jaccard Similarity:** Küme benzerliği

### Preprocessing Terimleri
- ✅ **Missing Values:** Eksik değerler
- ✅ **Normalizing:** Normalize etme (aynı range'e getirme)
- ✅ **Feature Scaling:** Özellik ölçeklendirme
- ✅ **Standardization:** Standartlaştırma (mean=0, std=1)

### Clustering Algoritması Türleri
- ✅ **Partition-Based:** K-Means vb.
- ✅ **Hierarchical-Based:** Dendrogram, ağaç yapısı
- ✅ **Density-Based:** DBSCAN, yoğunluk tabanlı
- ✅ **Distribution-Based:** GMM, dağılım tabanlı

### Süreç Terimleri
- ✅ **Workflow:** İş akışı, adımlar
- ✅ **Iterative:** Yinelemeli, tekrarlı
- ✅ **Exploratory:** Keşfedici
- ✅ **Ground Truth:** Doğru cevaplar (Unsupervised'da YOK!)
- ✅ **Verification:** Doğrulama
- ✅ **Interpretation:** Yorumlama

### Uygulama Terimleri
- ✅ **Customer Segmentation:** Müşteri segmentasyonu
- ✅ **Anomaly Detection:** Anormallik tespiti
- ✅ **Recommendation Systems:** Öneri sistemleri
- ✅ **Movie/Music Recommendations:** Film/müzik önerileri

---

## 💡 ÖNEMLİ NOTLAR

### 1. Unsupervised vs Supervised
**En Büyük Fark:** **Ground truth (labeled output) YOK!**

**Supervised:**
- Labels var → Doğru cevapları biliyoruz
- Model accuracy hesaplanabilir
- Sonuç doğrulanabilir

**Unsupervised:**
- Labels YOK → Doğru cevapları bilmiyoruz
- Sonuç "mantıklı mı?" diye kontrol edilir
- Subjective (öznel) değerlendirme

---

### 2. Similarity Yüksek = Aynı Cluster
**Temel Prensip:**
```
High Similarity → Same Cluster
Low Similarity → Different Clusters
```

**Örnek:**
- Apple & Cherry (similarity = 0.9) → Aynı cluster
- Apple & Banana (similarity = 0.2) → Farklı cluster'lar

---

### 3. Similarity Matrix Seçimi
**Neye Göre?**

**a) Veri Doğası (Nature of Data):**
- Numerical data → Euclidean/Manhattan
- Text data → Cosine
- Binary/Set data → Jaccard

**b) Clustering Algoritması:**
- K-Means → Euclidean (genellikle)
- Hierarchical → Euclidean, Manhattan, Cosine
- DBSCAN → Euclidean

---

### 4. Preprocessing Neden Kritik?
**Senaryo: Normalize Etmeden**
```
Feature 1 (Age): 25, 30, 35 → Range: 10
Feature 2 (Income): $30K, $50K, $80K → Range: 50K

Income feature baskın → Age effect kaybolur!
```

**Çözüm:** Feature scaling ile her feature eşit ağırlık

---

### 5. Iterative Süreç
**Unsupervised Learning = Deneme-Yanılma**

```
1. İlk clustering yap
2. Sonuçları incele
3. Tatmin edici değil mi?
   → Preprocessing'i değiştir
   → Similarity metric değiştir
   → Algoritma değiştir
   → Cluster sayısını değiştir
4. Tekrar dene
5. Tatmin edici olana kadar devam
```

**💡 Tek seferde mükemmel sonuç beklemeyin!**

---

### 6. Recommendation Systems
**Netflix Örneği Detayı:**

**Adım 1: Data Collection**
- User A: Horror (8/10), Thriller (9/10), Comedy (4/10)
- User B: Horror (9/10), Thriller (8/10), Comedy (3/10)
- User C: Comedy (9/10), Romance (8/10), Horror (2/10)

**Adım 2: Clustering**
- User A & B → Cluster 1 (Horror/Thriller severler)
- User C → Cluster 2 (Comedy/Romance severler)

**Adım 3: Recommendation**
- User A'ya → Cluster 1'deki User B'nin izlediği filmler önerilir
- User C'ye → Cluster 2'deki diğer kullanıcıların filmleri önerilir

**💡 "Benzer insanlar benzer şeyleri sever" mantığı**

---

## 🎯 SINAV İÇİN KRİTİK NOKTALAR

### Mutlaka Bilin:
1. **Unsupervised = Unlabeled data** ✓
2. **Ana Yöntem: Clustering** ✓
3. **Similarity: 0-1 arası** ✓
4. **4 Similarity Measure:** Euclidean, Manhattan, Cosine, Jaccard ✓
5. **5 Adımlı Workflow** ✓
6. **4 Clustering Türü:** Partition, Hierarchical, Density, Distribution ✓
7. **Ground Truth YOK → Verification zor** ✓

### Örnekleri Bilin:
- **Recommendation Systems:** Netflix, Spotify
- **Customer Segmentation:** Pazarlama
- **Anomaly Detection:** Fraud

### Süreç Adımları:
1. Prepare Data (Preprocessing)
2. Create Similarity Matrix
3. Run Clustering Algorithm
4. Interpret Results
5. Adjust Clustering

---

## 📊 KARŞILAŞTIRMA TABLOLARI

### Supervised vs Unsupervised

| Özellik | Supervised | Unsupervised |
|---------|------------|--------------|
| **Veri** | Labeled | Unlabeled |
| **Amaç** | Tahmin | Pattern keşfi |
| **Örnek** | Classification, Regression | Clustering |
| **Ground Truth** | Var | **YOK** |
| **Verification** | Kolay (accuracy) | **Zor (subjective)** |

---

### Similarity Measures Karşılaştırma

| Measure | Formül Tipi | Kullanım | Özellik |
|---------|-------------|----------|---------|
| **Euclidean** | Düz çizgi | Genel amaçlı | En yaygın |
| **Manhattan** | Grid/Blok | Şehir haritaları | Yatay+Dikey |
| **Cosine** | Açı | Text mining | Büyüklük önemsiz |
| **Jaccard** | Küme kesişimi | Set data | Binary/presence data |

---

## 📋 ÖĞRENME KONTROL LİSTESİ

Kendinize sorun:
- [ ] Unsupervised Learning nedir?
- [ ] Clustering ne demek?
- [ ] Similarity 0-1 arası mı?
- [ ] 4 similarity measure'ı sayabiliyor muyum?
- [ ] 5 adımlı workflow nedir?
- [ ] 4 clustering türü nedir?
- [ ] Preprocessing neden önemli?
- [ ] Ground truth neden yok?
- [ ] Netflix recommendation nasıl çalışır?
- [ ] Iterative süreç ne demek?

**Hepsine EVET cevabı vermelisiniz!**

---

## ✏️ Kendi Notlarınız İçin Boş Alan

_______________________________________________
_______________________________________________
_______________________________________________
_______________________________________________