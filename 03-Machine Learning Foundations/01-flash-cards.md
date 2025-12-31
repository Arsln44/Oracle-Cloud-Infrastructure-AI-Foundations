# 🎴 FLASHCARDS - Introduction to Machine Learning

## TEMEL TANIMLAR

### Kart 1
**Ön Yüz:** Machine Learning (ML) nedir? AI ile ilişkisi?
**Arka Yüz:** 
**Tanım:** AI'ın bir alt kümesi. Bilgisayar sistemlerinin açıkça programlanmadan örneklerden öğrenerek tahmin yapması.

**AI ile ilişki:** ML ⊂ AI (ML, AI'ın alt kümesidir)

---

### Kart 2
**Ön Yüz:** "Without being explicitly programmed" ne demek?
**Arka Yüz:** 
Kurallar manuel yazılmaz, sistem otomatik öğrenir.

**Örnek:**
❌ Elle yazılmış kural: "if email contains 'lottery' then spam"
✅ ML: Spam pattern'lerini otomatik öğrenir

---

### Kart 3
**Ön Yüz:** ML'de "Features" nedir?
**Arka Yüz:** 
**Features (Özellikler):** Input data (Girdi verisi)
**Sembol:** X
**Örnek:** Kedi/köpek ayırt etmede: body color, texture, eye color

---

### Kart 4
**Ön Yüz:** ML'de "Labels" nedir?
**Arka Yüz:** 
**Labels (Etiketler):** Output/Çıktı
**Sembol:** Y
**Örnek:** Kedi/köpek ayırt etmede: "Cat" veya "Dog"
**Not:** Sadece Supervised Learning'de vardır!

---

### Kart 5
**Ön Yüz:** Training (Eğitim) ne demek?
**Arka Yüz:** 
ML modelinin **features ve labels arasındaki ilişkiyi** öğrenme süreci.

**Input:** Training Data (Features + Labels)
**Output:** Trained Model

---

### Kart 6
**Ön Yüz:** Inference (Çıkarım) ne demek?
**Arka Yüz:** 
Eğitilmiş modele **yeni bir veri noktası** vererek **tahmin** alma süreci.

**Başka adı:** Prediction (Tahmin)

**Örnek:**
Input: Yeni hayvan özellikleri → Model → Output: "Cat" veya "Dog"

---

### Kart 7
**Ön Yüz:** Trained Model (Eğitilmiş Model) nedir?
**Arka Yüz:** 
Training tamamlandıktan sonra **kullanıma hazır** olan model.

Features-Labels ilişkisini öğrenmiş, artık tahmin yapabilir.

---

## ML SÜRECİ

### Kart 8
**Ön Yüz:** ML sürecinin 4 adımını sırala.
**Arka Yüz:** 
1. **Data Collection:** Features + Labels topla
2. **Training:** Model ilişkiyi öğrenir
3. **Trained Model:** Model hazır
4. **Inference:** Yeni veri → Tahmin

---

### Kart 9
**Ön Yüz:** Training vs Inference farkı?
**Arka Yüz:** 
**Training:**
- Model öğrenme aşaması
- Geçmiş veri kullanılır
- Tek sefer (veya güncelleme için tekrar)

**Inference:**
- Model kullanım aşaması
- Yeni veri gelir, tahmin yapılır
- Sürekli

---

## GÜNLÜK HAYAT ÖRNEKLERİ

### Kart 10
**Ön Yüz:** Günlük hayattan 4 ML örneği ver.
**Arka Yüz:** 
1. **Online Shopping:** Ürün önerileri (tercihler + alışveriş geçmişi)
2. **Netflix:** Film/dizi önerileri (izleme geçmişi)
3. **Email:** Spam filtresi (içerik analizi)
4. **Self-Driving Cars:** Otonom sürüş

---

## ML TÜRLERİ - GENEL

### Kart 11
**Ön Yüz:** 3 ana ML türünü say.
**Arka Yüz:** 
1. Supervised Learning (Denetimli Öğrenme)
2. Unsupervised Learning (Denetimsiz Öğrenme)
3. Reinforcement Learning (Pekiştirmeli Öğrenme)

---

### Kart 12
**Ön Yüz:** ML türlerini ayırt eden ana faktör nedir?
**Arka Yüz:** 
**"Labeled output var mı?"** sorusuna göre:
- Var → Supervised
- Yok → Unsupervised
- Outcomes/Feedback var → Reinforcement

---

## SUPERVISED LEARNING

### Kart 13
**Ön Yüz:** Supervised Learning nedir ve nasıl çalışır?
**Arka Yüz:** 
**Tanım:** Labeled data kullanılır

**Nasıl:**
- Model, features ve labels arasındaki ilişkiyi öğrenir
- Eğitim sonrası tahmin yapar

**Veri:** Features (X) + Labels (Y)

---

### Kart 14
**Ön Yüz:** Supervised Learning'in 5 popüler uygulamasını say.
**Arka Yüz:** 
1. **Disease Detection** (Hastalık tespiti)
2. **Weather Forecasting** (Hava tahmini)
3. **Stock Price Prediction** (Borsa tahmini)
4. **Spam Detection** (Spam tespiti)
5. **Credit Scoring** (Kredi skorlama)

---

### Kart 15
**Ön Yüz:** Disease Detection örneği ile Supervised Learning'i açıkla.
**Arka Yüz:** 
**Input:** Hasta verisi (yaş, semptomlar, test sonuçları)
**Model:** Features-Labels ilişkisini öğrenir
**Output:** Hasta mı / Sağlıklı mı (Label)

---

## UNSUPERVISED LEARNING

### Kart 16
**Ön Yüz:** Unsupervised Learning nedir ve nasıl çalışır?
**Arka Yüz:** 
**Tanım:** Labels kullanılmaz veya mevcut değildir

**Nasıl:**
- Veri setindeki ilişkileri anlar
- Pattern'leri keşfeder

**Veri:** Sadece Features (X)

---

### Kart 17
**Ön Yüz:** Unsupervised Learning'in 4 "real-time" uygulamasını say.
**Arka Yüz:** 
1. **Fraudulent Transactions** (Dolandırıcılık tespiti)
2. **Customer Segmentation** (Müşteri kümeleme)
3. **Outlier Detection** (Aykırı değer tespiti)
4. **Targeted Marketing** (Hedefli pazarlama)

---

### Kart 18
**Ön Yüz:** Fraudulent Transactions örneği ile Unsupervised Learning'i açıkla.
**Arka Yüz:** 
**Input:** İşlem verisi (tutar, saat, lokasyon)
**Model:** Pattern keşfi (label YOK!)
**Output:** Normal/Dolandırıcılık pattern'i

Model kendi başına şüpheli pattern'leri bulur.

---

### Kart 19
**Ön Yüz:** Unsupervised Learning'de "real-time" vurgusu neden?
**Arka Yüz:** 
- Gerçek zamanlı pattern keşfi
- Dinamik veri akışında çalışma
- Örnek: Dolandırıcılık tespiti işlem anında

---

## REINFORCEMENT LEARNING

### Kart 20
**Ön Yüz:** Reinforcement Learning nedir ve nasıl çalışır?
**Arka Yüz:** 
**Tanım:** Algoritmalar outcomes (sonuçlardan) öğrenir

**Nasıl:**
Action → Outcome (Reward/Punishment) → Learning

**Amaç:** En iyi strateji/politikayı bulmak

---

### Kart 21
**Ön Yüz:** Reinforcement Learning'in 3 popüler uygulamasını say.
**Arka Yüz:** 
1. **Automated Robots** (Otonom robotlar)
2. **Autonomous Driving Cars** (Otonom araçlar)
3. **Playing Games** (Oyun oynama - AlphaGo)

---

### Kart 22
**Ön Yüz:** Autonomous Driving örneği ile Reinforcement Learning'i açıkla.
**Arka Yüz:** 
**Durum:** Trafik ışığı kırmızı
**Action:** Dur (doğru) veya Geç (yanlış)
**Outcome:** Reward (doğru) / Punishment (yanlış)
**Learning:** Kırmızı ışıkta dur

Deneme-yanılma ile öğrenme!

---

## KARŞILAŞTIRMA KARTLARI

### Kart 23
**Ön Yüz:** Supervised vs Unsupervised - Temel fark?
**Arka Yüz:** 
**Supervised:**
- Labeled data VAR
- Features → Labels ilişkisi öğrenir
- Tahmin yapar

**Unsupervised:**
- Labeled data YOK
- Pattern keşfeder
- Kümeleme/gruplandırma yapar

---

### Kart 24
**Ön Yüz:** 3 ML türünü veri, öğrenme ve amaç açısından karşılaştır.
**Arka Yüz:** 
| Tür | Veri | Öğrenme | Amaç |
|-----|------|---------|------|
| **Supervised** | Labeled | Features→Labels | Tahmin |
| **Unsupervised** | Unlabeled | Pattern keşfi | Kümeleme |
| **Reinforcement** | Feedback | Outcomes | Karar |

---

### Kart 25
**Ön Yüz:** Her ML türüne birer örnek ver.
**Arka Yüz:** 
- **Supervised:** Spam detection
- **Unsupervised:** Customer segmentation
- **Reinforcement:** Self-driving car

---

## ÖZEL KAVRAMLAR

### Kart 26
**Ön Yüz:** "Pattern Discovery" nedir ve hangi ML türünde?
**Arka Yüz:** 
**Tanım:** Verideki pattern'leri/yapıları keşfetme

**ML Türü:** Unsupervised Learning

**Örnek:** Müşteri verilerinde doğal grupları bulma

---

### Kart 27
**Ön Yüz:** "Clustering" nedir ve hangi ML türünde?
**Arka Yüz:** 
**Tanım:** Benzer verileri gruplara ayırma (kümeleme)

**ML Türü:** Unsupervised Learning

**Örnek:** Customer segmentation

---

### Kart 28
**Ön Yüz:** "Outlier Detection" nedir?
**Arka Yüz:** 
**Tanım:** Aykırı değerleri tespit etme

**ML Türü:** Unsupervised Learning

**Kullanım:** Anormal davranış/veri tespiti

---

### Kart 29
**Ön Yüz:** Features ve Labels arasındaki ilişki nedir?
**Arka Yüz:** 
**Supervised Learning'de:**
- Features (X) → Input
- Labels (Y) → Output
- Model, X→Y ilişkisini öğrenir
- Yeni X gelince Y tahmin edilir

**Unsupervised'da:**
- Sadece Features var
- Labels YOK!

---

### Kart 30
**Ön Yüz:** "Outcomes" nedir ve hangi ML türünde kullanılır?
**Arka Yüz:** 
**Tanım:** Bir action'ın sonuçları (Reward veya Punishment)

**ML Türü:** Reinforcement Learning

**Örnek:** Robot bir hareketi dener → Sonuç iyi/kötü → Öğrenir

---

## UYGULAMA ÖRNEKLERİ

### Kart 31
**Ön Yüz:** Spam Detection hangi ML türüdür ve nasıl çalışır?
**Arka Yüz:** 
**Tür:** Supervised Learning

**Nasıl:**
- Features: Email içeriği, kelimeler, gönderen
- Label: Spam / Normal
- Model eğitilir
- Yeni email gelince tahmin yapar

---

### Kart 32
**Ön Yüz:** Customer Segmentation hangi ML türüdür ve nasıl çalışır?
**Arka Yüz:** 
**Tür:** Unsupervised Learning

**Nasıl:**
- Features: Müşteri özellikleri (yaş, gelir, davranış)
- Label YOK!
- Model benzer müşterileri gruplar
- Doğal kümeler bulur

---

### Kart 33
**Ön Yüz:** Netflix film önerisi hangi ML türü ve nasıl çalışır?
**Arka Yüz:** 
**Tür:** Genellikle Supervised + Unsupervised kombinasyonu

**Nasıl:**
- İzleme geçmişiniz
- Benzer kullanıcıların tercihleri
- Pattern discovery + Prediction

---

## SÜREÇLERİ BİL

### Kart 34
**Ön Yüz:** Kedi/Köpek ayırt etme probleminde Training süreci nasıl işler?
**Arka Yüz:** 
1. **Features topla:** Body color, texture, eye color
2. **Labels ekle:** "Cat" veya "Dog"
3. **Training Data oluştur:** Features + Labels
4. **Model eğit:** İlişkiyi öğrenir
5. **Trained Model:** Kullanıma hazır

---

### Kart 35
**Ön Yüz:** Kedi/Köpek ayırt etme probleminde Inference nasıl işler?
**Arka Yüz:** 
1. **Yeni hayvan gelir**
2. **Features çıkar:** Color, texture vb
3. **Trained Model'e ver**
4. **Model tahmin yapar:** "Cat" veya "Dog"

---

## ÖNEMLİ NOTLAR

### Kart 36
**Ön Yüz:** ML'de "açıkça programlanmadan" öğrenme örneği ver.
**Arka Yüz:** 
**Geleneksel Programlama:**
```
if (email.contains("free") && email.contains("money"))
    return SPAM;
```

**Machine Learning:**
Model, binlerce spam/normal email'den pattern öğrenir.
Yeni kurallar manuel yazılmaz!

---

### Kart 37
**Ön Yüz:** ML'de algoritmaların rolü nedir?
**Arka Yüz:** 
Algoritmalar, makinelere **zeka kazandırır**:
- Örnekler setinden otomatik öğrenme
- Pattern çıkarma
- İlişkileri bulma

Genellikle veri olarak sağlanır.

---

### Kart 38
**Ön Yüz:** Supervised Learning'de neden "labeled" data gerekir?
**Arka Yüz:** 
Çünkü model **Features→Labels ilişkisini** öğrenmeli!

**Analoji:** Öğretmen-öğrenci
- Öğretmen (Labels): Doğru cevapları gösterir
- Öğrenci (Model): Bu cevaplardan öğrenir

Label olmadan model neyin doğru olduğunu bilemez.

---

### Kart 39
**Ön Yüz:** Unsupervised Learning'de model neyi öğrenir?
**Arka Yüz:** 
Label olmadan **verideki doğal yapıları/pattern'leri** öğrenir:

- Hangi veriler benzer? (Clustering)
- Normal nedir, anormal nedir? (Outlier)
- Veriyi nasıl gruplandırmalı? (Segmentation)

---

### Kart 40
**Ön Yüz:** Reinforcement Learning'de "trial and error" nasıl işler?
**Arka Yüz:** 
1. Agent bir action dener
2. Environment feedback verir (good/bad)
3. Good → Reward → Tekrar yap
4. Bad → Punishment → Yapma
5. Zamanla en iyi stratejyi öğrenir

**Örnek:** Bebek yürümeyi öğrenir (düşme=punishment, adım=reward)

---

## 📝 Çalışma Stratejisi

**Öncelik Sırası:**
⭐⭐⭐ Yüksek: Kart 1-9, 11-15, 16-18, 20-22, 23-25
⭐⭐ Orta: Kart 26-33, 38-40
⭐ Düşük: Kart 34-37

**Tekrar Planı:**
- Gün 1: Tanımlar + ML Türleri (1-25)
- Gün 2: Örnekler + Karşılaştırmalar (26-40)
- Gün 3: Hızlı genel tekrar (Tümü)

**İpucu:** 3 ML türünün farkını çok iyi bilin!