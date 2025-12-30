# 📚 GÜN 1: AI vs ML vs DL - Detaylı Çalışma Notu

## 🎯 Modül Özeti
Bu modül AI, ML ve Deep Learning arasındaki farkları, makine öğrenme türlerini ve temel kavramları örneklerle açıklıyor.

---

## 🤖 AI vs ML vs DL - Hiyerarşi ve Tanımlar

### Yapı (En Genelden En Özele):
```
┌─────────────────────────────────────────┐
│   ARTIFICIAL INTELLIGENCE (AI)          │ ← En geniş kavram
│   ┌─────────────────────────────────┐   │
│   │   MACHINE LEARNING (ML)         │   │ ← AI'ın alt kümesi
│   │   ┌─────────────────────────┐   │   │
│   │   │   DEEP LEARNING (DL)    │   │   │ ← ML'nin alt kümesi
│   │   │                         │   │   │
│   │   └─────────────────────────┘   │   │
│   └─────────────────────────────────┘   │
└─────────────────────────────────────────┘
```

---

## 🤖 1. ARTIFICIAL INTELLIGENCE (AI)

### Tanım
**AI:** Normalde insan zekası gerektiren görevleri yapabilen makineler veya sistemler yaratma konsepti

### Örnek: Self-Driving Car (Otonom Araç)
**İnsan gibi kararlar alır:**
- Trafikte navigasyon
- Yayaları tespit etme
- Güvenli şerit değiştirme

**💡 Anahtar:** AI, "insan gibi düşünme" yeteneğidir

---

## 🔧 2. MACHINE LEARNING (ML)

### Tanım
**ML:** AI'ın bir alt kümesi. Makinelerin **veriden öğrenerek** tahmin veya karar vermesini sağlayan algoritmaların geliştirilmesi

### Örnek: Spam Email Filter
**Nasıl çalışır:**
- Kullanıcı etkileşimlerini gözlemler
- Email içeriğini analiz eder
- Spam'i öğrenir ve spam klasörüne taşır

### Algorithm (Algoritma) Nedir?
**ML bağlamında algoritma:**
- Belirli kurallar seti
- Matematiksel denklemler
- ML modelinin veriden öğrenmek için takip ettiği prosedürler

**💡 Anahtar:** ML, "veriden öğrenme" yeteneğidir

---

## 🧠 3. DEEP LEARNING (DL)

### Tanım
**DL:** ML'nin bir alt alanı. Karmaşık veri paternlerini öğrenmek için **çok katmanlı neural networks** (derin sinir ağları) kullanır

### Örnek: Image Recognition Software
**Görevi:**
- Resimlerdeki belirli nesneleri tanıma
- Örnek: İnternetteki fotoğraflarda kedileri tanıma

### Özellikler
- **Deep Neural Networks** (Derin sinir ağları)
- Çok katmanlı yapı
- Karmaşık patternleri anlama

**💡 Anahtar:** DL, "karmaşık paternleri otomatik öğrenme" yeteneğidir

---

## 📊 AI vs ML vs DL - Karşılaştırma Tablosu

| Özellik | AI | ML | DL |
|---------|----|----|-----|
| **Kapsam** | En geniş | AI'ın alt kümesi | ML'nin alt kümesi |
| **Tanım** | İnsan gibi düşünen sistemler | Veriden öğrenen sistemler | Çok katmanlı neural networks |
| **Örnek** | Self-driving car | Spam filter | Image recognition |
| **Yöntem** | Genel kavram | Algoritmalar | Deep neural networks |
| **Veri İhtiyacı** | Değişken | Orta | Çok yüksek |
| **Karmaşıklık** | Değişken | Orta | Yüksek |

---

## 🎓 MACHINE LEARNING TÜRLERİ

### 3 Ana Tür:
1. **Supervised Learning** (Denetimli Öğrenme)
2. **Unsupervised Learning** (Denetimsiz Öğrenme)
3. **Reinforcement Learning** (Pekiştirmeli Öğrenme)

---

## 📝 1. SUPERVISED LEARNING (Denetimli Öğrenme)

### Tanım
Algoritma **labeled data (etiketli veri)** den öğrenir ve tahmin/sınıflandırma yapar

### Temel Kavram
**"Learning from labeled data"** - Etiketli veriden öğrenme

---

### Detaylı Örnek: Kredi Kartı Onayı

#### Geleneksel Yöntem (Manuel/Rules Engine):
**Süreç:**
1. Başvuru ve belgeler gönderilir
2. Doğrulama yapılır
3. Kredi skoru kontrolü
4. 10-15 gün onay süreci

**Rules Engine ile:**
- Kurallar yazılır (if-then mantığı)
- Yeni veri gelir
- Karar verilir

**Dezavantajlar:**
- ❌ Yavaş
- ❌ Kuralları yazacak yetenekli insan gerekir
- ❌ Kurallar sürekli değişir

**Avantajlar:**
- ✅ Kararların nasıl verildiği şeffaf

---

#### ML Yöntemi:

**Soru:** Geçmiş veriye bakarak kurallar oluşturabilir miyiz?

**Cevap:** Evet! **Supervised Learning** ile

**Süreç:**

**1. Past Data (Geçmiş Veri):**
- Geçmiş kredi kartı onay verileri
- Bu veriler "examples" (örnekler) setidir
- Her örneğin **label'ı** var: Onaylandı ✓ / Reddedildi ✗

**2. Training (Eğitim):**
- Model, geçmiş örneklerden öğrenir
- Algoritma, örnekleri tek tek inceler
- Model **incrementally (artırımlı olarak)** güncellenir

**3. Model Building:**
- Belirli bir görevi yapacak **özel zeka** (specific intelligence) oluşur
- Model artık kullanıma hazır

**4. Prediction (Tahmin):**
- **Yeni veri** gelir (yeni başvuru)
- Model tahminde bulunur: Onayla / Reddet

**💡 İşte bu Supervised Learning'dir!**

---

### Supervised Learning Özellikleri

✅ **Labeled data** gerekir (etiketli veri)
✅ **Training** süreci var
✅ **Model** oluşturulur
✅ **Prediction** yapılır
✅ Geçmiş örneklerden öğrenme

**Kullanım Alanları:**
- Kredi kartı onayı
- Email spam tespiti
- Hastalık teşhisi
- Hisse senedi fiyat tahmini

---

## 🔍 2. UNSUPERVISED LEARNING (Denetimsiz Öğrenme)

### Tanım
Veri **label'ı olmayan** (unlabeled) yapıda. Algoritma verideki pattern'leri ve yapıları keşfeder.

### Temel Kavram
**"Exploring patterns and grouping similar data"** - Pattern keşfi ve benzer verileri gruplama

### Amaç
- Trendleri keşfetme
- Potansiyel içgörüler (insights)
- **Clustering (Kümeleme)**
- **Dimensionality Reduction (Boyut azaltma)**

---

### Örnek 1: Retail Marketing (Perakende Pazarlama)

**Toplanan Veri:**
- Household size (Hane büyüklüğü)
- Income (Gelir)
- Location (Lokasyon)
- Occupation (Meslek)

**Clustering Sonucu:**
- "Small family" (Küçük aile) kümesi
- "High spender" (Yüksek harcama yapan) kümesi
- Diğer kümeler...

**Kullanım:** Pazarlama ve satış stratejileri

---

### Örnek 2: Streaming Services (Yayın Hizmetleri)

**Toplanan Veri:**
- Viewing sessions (İzleme seansları)
- Minutes per session (Seans başına dakika)
- Number of unique shows watched (İzlenen benzersiz program sayısı)

**Kullanım:** Streaming servislerini düzenleme

---

### Örnek 3: Fruit & Vegetable Clustering

**Soru:** Hangi meyve ve sebzeler besinsel olarak benzer?

**Veri:** Meyve ve sebzelerin besin değerleri

**Sonuç:** 
- Benzer besin değerlerine sahip olanlar gruplandı
- İçgörü: Besinsel olarak farklı meyve/sebzeleri diyetimize ekleyebiliriz

**💡 Unsupervised Learning Use Case:** Pattern keşfi, benzer verileri gruplama

---

### Unsupervised Learning Özellikleri

✅ **Unlabeled data** (etiketsiz veri)
✅ **Pattern discovery** (pattern keşfi)
✅ **Clustering** (kümeleme)
✅ **No training labels needed** (eğitim etiketi gerekmez)

**Kullanım Alanları:**
- Müşteri segmentasyonu
- Anomaly detection (kısmen)
- Öneri sistemleri
- Veri ön işleme

---

## 🎮 3. REINFORCEMENT LEARNING (Pekiştirmeli Öğrenme)

### Tanım
Bilgisayar programı, farklı aksiyonlar deneyerek ve **feedback (geri bildirim)** alarak karar vermeyi öğrenir

### Nasıl Öğreniyoruz?

**Örnek: Satranç Öğrenme**
1. **Move/Decision:** Bir hamle yap
2. **Feedback:** Doğru hamle mi? Kontrol et
3. **Memory/Learning:** Sonuçları hafızada tut, bir dahaki sefere kullan

**💡 Trial and Error** (Deneme-Yanılma) ile öğrenme

---

### Reinforcement Learning Özellikleri

**Terimler:**
- **Agent:** Öğrenen varlık (robot, program)
- **Environment:** Çevre
- **Actions:** Yapılan hareketler
- **Rewards:** Ödüller (doğru hareket)
- **Punishments:** Cezalar (yanlış hareket)

**Süreç:**
1. Agent bir action yapar
2. Environment feedback verir (reward/punishment)
3. Agent öğrenir
4. Döngü devam eder

---

### Kullanım Alanları

✅ **Autonomous car driving** (Otonom araç sürüşü)
✅ **Robots** (Robotlar)
✅ **Game playing AI** (Oyun oynayan AI - AlphaGo)
✅ **Resource management**

**💡 Anahtar:** Trial and error ile en iyi stratejiyi bulma

---

## 🧠 DEEP LEARNING DETAYLARI

### Temel Soru
**"Can we identify if an image is a cat or a dog by looking at just one pixel?"**
**Cevap:** HAYIR!

**"Can we write rules to identify a cat or a dog in an image?"**
**Cevap:** ÇOK ZOR!

**Çözüm:** Deep Learning!

---

### Deep Learning'in Gücü

**Amaç:** Ham veriden (örn: pikseller) **features (özellikler) ve rules (kurallar)** otomatik çıkarma

**Nasıl:**
- Çok katmanlı **neural networks** (sinir ağları)
- Otomatik özellik çıkarma
- Kendiliğinden öğrenme

**Örnek:** Kedi/köpek tanıma
- Piksellerden başlar
- İlk katmanlar: Kenarlar, çizgiler
- Orta katmanlar: Şekiller, dokular
- Son katmanlar: Kedi/köpek özellikleri

---

## 🧠 NEURAL NETWORKS (Sinir Ağları)

### Tanım
**Neural Networks:** Birbirine bağlı beyin hücrelerinin (neurons) katmanlar halinde dizilmesi

### Görevi
**Functional Approximation (Fonksiyonel Yaklaşıklama):**
- Gizli bir fonksiyonu tahmin etme
- Geçmiş veya mevcut veriye bakarak
- Örneklerden pattern çıkarma

### Yapı
**Layers (Katmanlar):**
- Input layer (Giriş katmanı)
- Hidden layers (Gizli katmanlar) - Çok katman = Deep
- Output layer (Çıkış katmanı)

**💡 "Deep" kelimesi:** Çok sayıda hidden layer'dan gelir

---

### Neural Networks Özellikleri

✅ Supervised learning algoritmasıdır
✅ Katmanlar halinde neuronlar
✅ Karmaşık patternleri öğrenebilir
✅ **Functional approximation** için en iyi

**Kullanım:**
- Image recognition
- Speech recognition
- Natural language processing

---

## 🎨 GENERATIVE AI

### Tanım
**Generative AI:** Machine learning'in bir alt kümesi. Yeni içerik oluşturur.

### Ne Üretir?
- Text (Metin)
- Audio (Ses)
- Images (Görüntüler)
- Video
- Code

---

### Nasıl Çalışır?

**1. Pattern Learning:**
- Mevcut veriden patternleri öğrenir
- Neural networks kullanır (genellikle)

**2. Content Creation:**
- Öğrendiği patternlerden yeni içerik üretir
- **Fresh and creative output**

---

### Örnek: ChatGPT

**Nasıl Çalışır:**
- Eğitim verisindeki **text patternlerini** öğrenir
- Bu patternleri anlayarak yeni **text-based responses** üretir

**Generative AI'ın Rolü:**
- İçerik oluşturma gereken AI görevlerinde
- İnovasyon gerektiren alanlarda

---

## 🎯 ÖZETLEYİCİ TABLO - ML TÜRLERİ

| Tür | Veri Tipi | Nasıl Öğrenir | Kullanım | Örnek |
|-----|-----------|---------------|----------|-------|
| **Supervised** | Labeled | Etiketli örneklerden | Tahmin, sınıflandırma | Kredi kartı onayı |
| **Unsupervised** | Unlabeled | Pattern keşfi | Clustering | Müşteri segmentasyonu |
| **Reinforcement** | Feedback | Trial-error, rewards | Karar verme | Otonom araç |

---

## 🔑 Sınav İçin Kritik Kavramlar

### Tanımlar:
- ✅ **AI** = İnsan gibi düşünen sistemler
- ✅ **ML** = Veriden öğrenen sistemler (AI'ın alt kümesi)
- ✅ **DL** = Çok katmanlı neural networks (ML'nin alt kümesi)

### ML Türleri:
- ✅ **Supervised** = Labeled data, training, prediction
- ✅ **Unsupervised** = Unlabeled data, clustering, pattern discovery
- ✅ **Reinforcement** = Trial-error, rewards/punishments, agents

### Deep Learning:
- ✅ **Neural Networks** = Katmanlı neuronlar
- ✅ **Deep** = Çok katmanlı
- ✅ **Feature extraction** = Otomatik özellik çıkarma
- ✅ **Functional approximation**

### Generative AI:
- ✅ ML'nin alt kümesi
- ✅ Yeni içerik oluşturur
- ✅ Pattern learning → Creative output
- ✅ ChatGPT örneği

---

## 💡 Önemli Notlar

1. **Hiyerarşi:** AI ⊃ ML ⊃ DL
2. **Supervised Learning:** Etiketli veri + Training = Model
3. **Unsupervised Learning:** Etiketsiz veri → Pattern keşfi
4. **Reinforcement Learning:** Trial-error + Feedback = Öğrenme
5. **Deep Learning:** Çok katmanlı neural networks
6. **Generative AI:** Yeni içerik üretme

---

## ✏️ Kendi Notlarınız İçin Boş Alan

_______________________________________________
_______________________________________________
_______________________________________________
_______________________________________________