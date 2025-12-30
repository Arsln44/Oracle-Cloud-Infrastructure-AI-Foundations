# 🎴 FLASHCARDS - AI vs ML vs DL

## TEMEL TANIMLAR

### Kart 1
**Ön Yüz:** AI, ML ve DL arasındaki hiyerarşik ilişki nedir?
**Arka Yüz:** 
AI ⊃ ML ⊃ DL
- AI en geniş kavram
- ML, AI'ın alt kümesi
- DL, ML'nin alt kümesi

---

### Kart 2
**Ön Yüz:** Artificial Intelligence (AI) nedir? Örnek ver.
**Arka Yüz:** 
**Tanım:** Normalde insan zekası gerektiren görevleri yapabilen makineler/sistemler yaratma
**Örnek:** Self-driving car (otonom araç)
- Trafikte navigasyon
- Yayaları tespit
- Güvenli şerit değiştirme

---

### Kart 3
**Ön Yüz:** Machine Learning (ML) nedir? Örnek ver.
**Arka Yüz:** 
**Tanım:** AI'ın alt kümesi. Makinelerin veriden öğrenerek tahmin/karar vermesini sağlayan algoritmalar
**Örnek:** Spam email filter
- Kullanıcı etkileşimlerinden öğrenir
- Email içeriğini analiz eder
- Spam'i otomatik tanır

---

### Kart 4
**Ön Yüz:** Deep Learning (DL) nedir? Örnek ver.
**Arka Yüz:** 
**Tanım:** ML'nin alt alanı. Çok katmanlı neural networks kullanarak karmaşık patternleri öğrenir
**Örnek:** Image recognition
- Resimlerde kedi/köpek tanıma
- Derin sinir ağları kullanır

---

### Kart 5
**Ön Yüz:** ML bağlamında "algoritma" nedir?
**Arka Yüz:** 
- Belirli kurallar seti
- Matematiksel denklemler
- ML modelinin veriden öğrenmek için takip ettiği prosedürler

---

## MACHINE LEARNING TÜRLERİ

### Kart 6
**Ön Yüz:** 3 ana Machine Learning türünü say.
**Arka Yüz:** 
1. Supervised Learning (Denetimli Öğrenme)
2. Unsupervised Learning (Denetimsiz Öğrenme)
3. Reinforcement Learning (Pekiştirmeli Öğrenme)

---

## SUPERVISED LEARNING

### Kart 7
**Ön Yüz:** Supervised Learning nedir ve temel kavramı?
**Arka Yüz:** 
**Tanım:** Algoritma labeled data (etiketli veri) den öğrenir
**Temel Kavram:** "Learning from labeled data"
**Süreç:** Training → Model → Prediction

---

### Kart 8
**Ön Yüz:** Supervised Learning örneği: Kredi kartı onayı nasıl çalışır?
**Arka Yüz:** 
1. **Past Data:** Geçmiş onay verileri (labeled: Onay/Red)
2. **Training:** Model örneklerden öğrenir
3. **Model:** Specific intelligence oluşur
4. **Prediction:** Yeni başvuru → Karar

---

### Kart 9
**Ön Yüz:** Rules Engine vs ML yöntemi - Avantaj/Dezavantajlar?
**Arka Yüz:** 
**Rules Engine:**
✅ Şeffaf kararlar
❌ Yavaş, yetenekli insan gerekir, kurallar değişir

**ML:**
✅ Hızlı, otomatik öğrenme, ölçeklenebilir
❌ "Black box" olabilir

---

### Kart 10
**Ön Yüz:** Supervised Learning özellikleri nelerdir?
**Arka Yüz:** 
- Labeled data gerekir
- Training süreci var
- Model oluşturulur
- Prediction yapılır
- Geçmiş örneklerden öğrenme

---

### Kart 11
**Ön Yüz:** Supervised Learning kullanım alanlarına 4 örnek ver.
**Arka Yüz:** 
1. Kredi kartı onayı
2. Email spam tespiti
3. Hastalık teşhisi
4. Hisse senedi fiyat tahmini

---

## UNSUPERVISED LEARNING

### Kart 12
**Ön Yüz:** Unsupervised Learning nedir ve temel kavramı?
**Arka Yüz:** 
**Tanım:** Unlabeled (etiketsiz) verideki pattern'leri ve yapıları keşfeder
**Temel Kavram:** "Exploring patterns and grouping similar data"
**Yöntemler:** Clustering, Dimensionality Reduction

---

### Kart 13
**Ön Yüz:** Unsupervised Learning amaçları nelerdir?
**Arka Yüz:** 
- Trendleri keşfetme
- Potansiyel insights
- Clustering (Kümeleme)
- Dimensionality Reduction (Boyut azaltma)

---

### Kart 14
**Ön Yüz:** Unsupervised Learning örneği: Retail Marketing nasıl kullanır?
**Arka Yüz:** 
**Veri:** Household size, Income, Location, Occupation
**Clustering:** 
- "Small family" kümesi
- "High spender" kümesi
**Kullanım:** Pazarlama ve satış stratejileri

---

### Kart 15
**Ön Yüz:** Unsupervised Learning örneği: Fruit & Vegetable Clustering amacı?
**Arka Yüz:** 
**Veri:** Besin değerleri
**Sonuç:** Besinsel olarak benzer meyve/sebzeleri gruplar
**İçgörü:** Besinsel olarak farklı meyve/sebzeleri diyete ekleyebiliriz

---

### Kart 16
**Ön Yüz:** Unsupervised Learning özellikleri nelerdir?
**Arka Yüz:** 
- Unlabeled data (etiketsiz)
- Pattern discovery
- Clustering
- No training labels needed

---

### Kart 17
**Ön Yüz:** Unsupervised Learning kullanım alanlarına 4 örnek ver.
**Arka Yüz:** 
1. Müşteri segmentasyonu
2. Anomaly detection (kısmen)
3. Öneri sistemleri
4. Veri ön işleme

---

## REINFORCEMENT LEARNING

### Kart 18
**Ön Yüz:** Reinforcement Learning nedir ve temel kavramı?
**Arka Yüz:** 
**Tanım:** Farklı aksiyonlar deneyerek ve feedback alarak karar vermeyi öğrenir
**Temel Kavram:** "Trial and Error" (Deneme-Yanılma)
**Yöntem:** Actions → Feedback (Rewards/Punishments) → Learning

---

### Kart 19
**Ön Yüz:** Satranç öğrenme örneği ile Reinforcement Learning'i açıkla.
**Arka Yüz:** 
1. **Move/Decision:** Bir hamle yap
2. **Feedback:** Doğru hamle mi? Kontrol et
3. **Memory/Learning:** Sonuçları hafızada tut
4. **Loop:** Bir sonraki hamle için kullan

---

### Kart 20
**Ön Yüz:** Reinforcement Learning'de terimler: Agent, Environment, Actions, Rewards, Punishments
**Arka Yüz:** 
- **Agent:** Öğrenen varlık (robot, program)
- **Environment:** Çevre
- **Actions:** Yapılan hareketler
- **Rewards:** Ödüller (doğru hareket)
- **Punishments:** Cezalar (yanlış hareket)

---

### Kart 21
**Ön Yüz:** Reinforcement Learning süreci nasıl işler?
**Arka Yüz:** 
1. Agent bir action yapar
2. Environment feedback verir (reward/punishment)
3. Agent öğrenir
4. Döngü devam eder
→ En iyi strateji bulunur

---

### Kart 22
**Ön Yüz:** Reinforcement Learning kullanım alanlarına 4 örnek ver.
**Arka Yüz:** 
1. Autonomous car driving
2. Robots
3. Game playing AI (AlphaGo)
4. Resource management

---

## DEEP LEARNING

### Kart 23
**Ön Yüz:** Deep Learning'in temel sorusu ve cevabı?
**Arka Yüz:** 
**Soru:** "Tek bir piksele bakarak kedi/köpek ayırt edilebilir mi?"
**Cevap:** HAYIR!

**Soru:** "Kedi/köpek tanımak için kurallar yazılabilir mi?"
**Cevap:** ÇOK ZOR!

**Çözüm:** Deep Learning!

---

### Kart 24
**Ön Yüz:** Deep Learning'in gücü nedir?
**Arka Yüz:** 
Ham veriden (örn: pikseller) **features (özellikler) ve rules (kurallar)** otomatik çıkarma

**Nasıl:**
- Çok katmanlı neural networks
- Otomatik özellik çıkarma
- Kendiliğinden öğrenme

---

### Kart 25
**Ön Yüz:** Kedi/köpek tanımada Deep Learning katmanları nasıl çalışır?
**Arka Yüz:** 
**Piksellerden başlar:**
- **İlk katmanlar:** Kenarlar, çizgiler
- **Orta katmanlar:** Şekiller, dokular
- **Son katmanlar:** Kedi/köpek özellikleri

→ Otomatik feature extraction!

---

## NEURAL NETWORKS

### Kart 26
**Ön Yüz:** Neural Networks nedir?
**Arka Yüz:** 
**Tanım:** Birbirine bağlı beyin hücrelerinin (neurons) katmanlar halinde dizilmesi

**Yapı:**
- Input layer (Giriş)
- Hidden layers (Gizli) - Çok katman = "Deep"
- Output layer (Çıkış)

---

### Kart 27
**Ön Yüz:** Neural Networks'ün görevi nedir?
**Arka Yüz:** 
**Functional Approximation (Fonksiyonel Yaklaşıklama):**
- Gizli bir fonksiyonu tahmin etme
- Geçmiş/mevcut veriye bakarak
- Örneklerden pattern çıkarma

---

### Kart 28
**Ön Yüz:** Neural Networks özellikleri nelerdir?
**Arka Yüz:** 
- Supervised learning algoritmasıdır
- Katmanlar halinde neuronlar
- Karmaşık patternleri öğrenebilir
- Functional approximation için en iyi

---

### Kart 29
**Ön Yüz:** "Deep" kelimesi nereden gelir?
**Arka Yüz:** 
Çok sayıda **hidden layer** (gizli katman) dan gelir.
Ne kadar çok katman → O kadar "deep"

---

## GENERATIVE AI

### Kart 30
**Ön Yüz:** Generative AI nedir ve ne üretir?
**Arka Yüz:** 
**Tanım:** Machine learning'in alt kümesi. Yeni içerik oluşturur.

**Üretebilecekleri:**
- Text (Metin)
- Audio (Ses)
- Images (Görüntüler)
- Video
- Code

---

### Kart 31
**Ön Yüz:** Generative AI nasıl çalışır?
**Arka Yüz:** 
1. **Pattern Learning:** Mevcut veriden patternleri öğrenir (neural networks ile)
2. **Content Creation:** Öğrendiği patternlerden yeni içerik üretir

→ Fresh and creative output!

---

### Kart 32
**Ön Yüz:** ChatGPT örneği ile Generative AI'yı açıkla.
**Arka Yüz:** 
**ChatGPT:**
- Eğitim verisindeki text patternlerini öğrenir
- Bu patternleri anlayarak yeni text-based responses üretir

**Generative AI'ın Rolü:**
- İçerik oluşturma
- İnovasyon

---

## KARŞILAŞTIRMA KARTLARI

### Kart 33
**Ön Yüz:** Supervised vs Unsupervised Learning - Temel farklar?
**Arka Yüz:** 
**Supervised:**
- Labeled data
- Training → Model → Prediction
- Örnek: Kredi onayı

**Unsupervised:**
- Unlabeled data
- Pattern discovery → Clustering
- Örnek: Müşteri segmentasyonu

---

### Kart 34
**Ön Yüz:** 3 ML türünü veri tipi, öğrenme yöntemi ve kullanım açısından karşılaştır.
**Arka Yüz:** 
| Tür | Veri | Öğrenme | Kullanım |
|-----|------|---------|----------|
| **Supervised** | Labeled | Etiketli örnekler | Tahmin |
| **Unsupervised** | Unlabeled | Pattern keşfi | Clustering |
| **Reinforcement** | Feedback | Trial-error | Karar verme |

---

### Kart 35
**Ön Yüz:** AI, ML ve DL'yi kapsam, tanım ve örnek açısından karşılaştır.
**Arka Yüz:** 
**AI:**
- Kapsam: En geniş
- Tanım: İnsan gibi düşünme
- Örnek: Self-driving car

**ML:**
- Kapsam: AI'ın alt kümesi
- Tanım: Veriden öğrenme
- Örnek: Spam filter

**DL:**
- Kapsam: ML'nin alt kümesi
- Tanım: Çok katmanlı neural networks
- Örnek: Image recognition

---

## ÖZEL DURUMLAR

### Kart 36
**Ön Yüz:** "Incrementally updates the model" ne demek?
**Arka Yüz:** 
Model, veriyi tek tek inceleyerek **artırımlı olarak** güncellenir.
Her örnekten bir şeyler öğrenir ve modeli geliştirir.

---

### Kart 37
**Ön Yüz:** "Specific intelligence to do a specific task" ne demek?
**Arka Yüz:** 
Model, belirli bir görevi yapmak için **özel zeka** kazanır.
Örnek: Kredi kartı onaylama modelinin sadece o işe özel zekası vardır.

---

### Kart 38
**Ön Yüz:** Clustering nedir ve hangi ML türünde kullanılır?
**Arka Yüz:** 
**Clustering:** Benzer verileri gruplara ayırma
**Kullanım:** Unsupervised Learning
**Örnekler:** Müşteri segmentasyonu, ürün gruplandırma

---

### Kart 39
**Ön Yüz:** Dimensionality Reduction nedir?
**Arka Yüz:** 
Yüksek boyutlu veriyi daha az boyuta indirme (Unsupervised Learning tekniği)
**Amaç:** Veri karmaşıklığını azaltma, görselleştirme

---

### Kart 40
**Ön Yüz:** Generative AI ML'nin neresinde durur?
**Arka Yüz:** 
Generative AI, **Machine Learning'in bir alt kümesidir**.
Genellikle neural networks (özellikle deep learning) kullanır.

---

## 📝 Çalışma Stratejisi

**Öncelik Sırası:**
⭐⭐⭐ Yüksek: Kart 1-6, 7, 12, 18, 23, 26, 30, 33
⭐⭐ Orta: Kart 8-11, 13-17, 19-22, 24-29, 31-32
⭐ Düşük: Kart 34-40 (detay kartlar)

**Günlük Plan:**
- Sabah: Tanımlar (1-6)
- Öğle: ML Türleri (7-22)
- Akşam: Deep Learning & Gen AI (23-32)
- Gece: Tekrar (33-40)

**İpucu:** Hiyerarşiyi unutmayın: AI ⊃ ML ⊃ DL