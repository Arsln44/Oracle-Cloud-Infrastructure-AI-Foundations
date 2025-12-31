# 🎴 FLASHCARDS - Unsupervised Learning (ÖZET)

## TEMEL KAVRAMLAR

### Kart 1
**Ön Yüz:** Unsupervised Learning tanımı ve temel özelliği?
**Arka Yüz:** 
**Tanım:** Unlabeled (etiketsiz) data ile çalışan ML türü
**Temel:** Pattern keşfi, clustering
**Önemli:** Ground truth YOK!

### Kart 2
**Ön Yüz:** Similarity nedir ve değer aralığı?
**Arka Yüz:** 
**Tanım:** İki veri noktasının birbirine ne kadar yakın olduğu
**Aralık:** 0-1
- 0 = Hiç benzer değil
- 1 = Tamamen benzer

### Kart 3
**Ön Yüz:** 4 Similarity Measure'ı say.
**Arka Yüz:** 
1. Euclidean Distance (en yaygın)
2. Manhattan Distance
3. Cosine Similarity (text için)
4. Jaccard Similarity (set için)

## UNSUPERVISED WORKFLOW

### Kart 4
**Ön Yüz:** Unsupervised Learning workflow'un 5 adımı?
**Arka Yüz:** 
1. **Prepare Data:** Preprocessing
2. **Create Similarity Matrix:** Benzerlik hesapla
3. **Run Clustering:** Algoritma çalıştır
4. **Interpret Results:** Sonuçları yorumla
5. **Adjust:** İteratif düzelt

### Kart 5
**Ön Yüz:** Preprocessing'de 3 temel adım?
**Arka Yüz:** 
1. **Remove Missing Values:** Eksik veri temizle
2. **Normalize Data:** Aynı range'e getir
3. **Feature Scaling:** Ölçeklendir (standardize)

### Kart 6
**Ön Yüz:** 4 Clustering algoritma türü?
**Arka Yüz:** 
1. **Partition-Based** (K-Means)
2. **Hierarchical-Based** (Dendrogram)
3. **Density-Based** (DBSCAN)
4. **Distribution-Based** (GMM)

## SIMILARITY MEASURES

### Kart 7
**Ön Yüz:** Euclidean Distance nedir ve formül?
**Arka Yüz:** 
**Tanım:** Düz çizgi mesafesi
**Formül:** d = √[(x₂-x₁)² + (y₂-y₁)²]
**Kullanım:** En yaygın, genel amaçlı

### Kart 8
**Ön Yüz:** Cosine Similarity ne zaman kullanılır?
**Arka Yüz:** 
**Kullanım:** Text mining, document similarity
**Avantaj:** Büyüklük (magnitude) önemli değil, sadece yön
**Değer:** [-1, 1]

## UYGULAMALAR

### Kart 9
**Ön Yüz:** Netflix recommendation nasıl çalışır?
**Arka Yüz:** 
**Input:** İzleme geçmişi
**Clustering:** Benzer film izleyen kullanıcılar gruplandırılır
**Output:** Aynı cluster'daki kullanıcıların beğendiği filmler önerilir

### Kart 10
**Ön Yüz:** Unsupervised Learning 3 ana kullanım alanı?
**Arka Yüz:** 
1. **Customer Segmentation**
2. **Anomaly Detection**
3. **Recommendation Systems**

## SUPERVISED VS UNSUPERVISED

### Kart 11
**Ön Yüz:** Supervised vs Unsupervised - Ground Truth farkı?
**Arka Yüz:** 
**Supervised:** Ground truth VAR (labeled output)
**Unsupervised:** Ground truth YOK!
→ Verification zor, subjective değerlendirme

### Kart 12
**Ön Yüz:** Unsupervised Learning neden "iterative"?
**Arka Yüz:** 
Ground truth olmadığı için:
- İlk denemede mükemmel olmayabilir
- Deneme-yanılma gerekir
- Parametreleri değiştirip tekrar dene

## ÖZEL DURUMLAR

### Kart 13
**Ön Yüz:** Similarity Matrix nedir?
**Arka Yüz:** 
**Tanım:** Her veri çifti arası benzerlik değerleri
**Boyut:** n veri → n×n matris
**Kullanım:** Clustering algoritmaları için

### Kart 14
**Ön Yüz:** Preprocessing neden kritik?
**Arka Yüz:** 
**Sebep:** Farklı ölçekli feature'lar bias yaratır
**Örnek:** Income ($20K-$200K) vs Age (18-80)
→ Normalize etmezsen Income baskın olur!

### Kart 15
**Ön Yüz:** Apple & Cherry similarity 0.9, Apple & Banana 0.2. Ne demek?
**Arka Yüz:** 
**Apple-Cherry:** Yüksek benzerlik → Aynı cluster'a düşer
**Apple-Banana:** Düşük benzerlik → Farklı cluster'lara düşer

---

## 📝 Hızlı Tekrar Notları

**EZBER:**
- Unsupervised = Unlabeled
- Similarity = 0-1
- 4 Measure: Euclidean, Manhattan, Cosine, Jaccard
- 5 Adım: Prepare → Matrix → Cluster → Interpret → Adjust
- 4 Tür: Partition, Hierarchical, Density, Distribution
- Ground Truth YOK!

**SINAV:** Netflix örneği ve workflow adımları çok önemli!