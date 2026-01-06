# OCI AI Portfolio - Sınav Hazırlık Rehberi
## Oracle Cloud Infrastructure AI Foundations Sertifikası
**Hazırlayan:** Claude | **Tarih:** 6 Ocak 2026

---

## 📋 İçindekiler

1. OCI AI Services
2. OCI ML Services (Data Science)
3. GPU & AI Infrastructure
4. RDMA & Supercluster
5. Responsible AI
6. Sınav Stratejisi

---

## 1. OCI AI SERVICES

### 1.1 OCI AI Services (Genel)
* **Basit Tanım:** Oracle'ın hazır yapay zeka oyuncakları - kodlama bilmeden resim, metin ve ses işleyebilirsin.
* **Teknik Tanım:** Prebuilt machine learning modelleri içeren, custom training desteği sunan, infrastructure yönetimi gerektirmeyen, API tabanlı cloud servisleri.

**Ne Zaman Kullan:**
* Data science ekibin yok ama ML/AI yetenekleri lazım
* Hızlı prototipleme gerekiyor
* Infrastructure yönetimi istemiyorsun

**Örnek:** E-ticaret şirketi müşteri yorumlarını analiz etmek istiyor ama ML ekibi yok. OCI Language Service kullanarak sentiment analysis yapabilir.
> **Sınav İpucu:** "prebuilt models", "no infrastructure management", "API-based"

### 1.2 OCI Language Service
* **Basit Tanım:** Metinleri okuyan ve anlam çıkaran akıllı okuyucu - mutlu mu üzgün mü, hangi dilde, önemli kelimeler neler anlıyor.
* **Teknik Tanım:** NLP servisi. Sentiment analysis, named entity recognition, PII detection, text translation.

**Özellikler:**
* **Pretrained Models:** Language detection, sentiment analysis, key phrase extraction, text classification, NER, PII detection
* **Custom Models:** Domain-specific NER ve text classification
* **Translation:** Neural machine translation

**Ne Zaman Kullan:**
* Müşteri yorumları sentiment analizi
* Çok dilli dökümanlarda dil tespiti
* PII verilerini otomatik tespit
* Otomatik çeviri

**Ne Zaman Kullanma:**
* Real-time konuşma çevirisi (Speech kullan)
* Görüntüdeki metni okuma (Vision OCR kullan)

**Örnek:** Banka KVKK uyumluluğu için binlerce müşteri mailinde TC kimlik numarası, telefon gibi PII verilerini otomatik tespit edip maskeliyor.
> **Sınav İpucu:** "sentiment analysis", "text analysis", "PII detection", "named entity recognition"

### 1.3 OCI Vision Service
* **Basit Tanım:** Resimlere bakıp "bu bir kedi, şurada araba var" diyen gözlük. Resimlerdeki yazıları da okuyabiliyor.
* **Teknik Tanım:** Computer vision servisi. Object detection, image classification, OCR yetenekli. Bounding box koordinatları sağlar.

**Özellikler:**
* **Pretrained Models:** Object detection, image classification, OCR
* **Custom Models:** Custom object detection, custom image classification

**Ne Zaman Kullan:**
* Resimlerdeki objeleri detect/classify
* Görüntülerdeki metni extract (OCR)
* Custom object detection (fabrikada hatalı ürün tespiti)

**Ne Zaman Kullanma:**
* Strukturlu dökümanlar (fatura, form) → **Document Understanding kullan**
* Sadece metin işleme → **Language kullan**

**Örnek:** Retail mağazası güvenlik kameralarından "mağazada kaç müşteri var, hangi raflarda yoğunluk var" tespit etmek için custom object detection kullanıyor.
> **Sınav İpucu:** "image classification", "object detection", "OCR on images", "bounding box"

### 1.4 OCI Speech Service
* **Basit Tanım:** Konuşmaları dinleyip yazıya döken sekreter. Ses dosyası verirsin, metin olarak alırsın.
* **Teknik Tanım:** Speech-to-text servisi. Audio/media dosyalarını highly accurate text transcription'a dönüştürür. JSON ve SRT formatında output.

**Ne Zaman Kullan:**
* Podcast, webinar, toplantı kayıtlarını metne çevirme
* Call center kayıtlarını analiz
* Video altyazısı oluşturma

**Ne Zaman Kullanma:**
* Metin zaten var, analiz edeceksin (Language kullan)
* Görüntü/video var ama ses yok (Vision kullan)

**Örnek:** Hukuk firması mahkeme duruşma kayıtlarını Speech Service ile metne çeviriyor, sonra Language Service ile önemli entity'leri çıkarıyor.
> **Sınav İpucu:** "speech-to-text", "media files", "transcription", "audio to text"

### 1.5 OCI Document Understanding
* **Basit Tanım:** Fatura, pasaport gibi dökümanları okuyan akıllı tarayıcı. Hem metni hem tabloları hem de hangi tip dökuman olduğunu anlıyor.
* **Teknik Tanım:** OCR ve AI tabanlı document processing. Text extraction, key-value extraction, table extraction, document classification. Word/line level bounding box.

**Özellikler:**
* **Text Extraction:** Word ve line level text + coordinates
* **Key-Value Extraction:** Fatura, makbuz, pasaport, ehliyet için predefined pairs
* **Table Extraction:** Row-column ilişkisi korunarak tabular format
* **Document Classification:** Dökuman tipini otomatik classify

**Ne Zaman Kullan:**
* Fatura, makbuz, pasaport, ehliyet işleme
* Tablo formatındaki dataları extract
* Dökuman tipini otomatik classify
* Batch processing (çok sayıda belge)

**Ne Zaman Kullanma:**
* Sadece sade metin analizi (Language kullan)
* Resimde genel obje tespiti (Vision kullan)

**Örnek:** Muhasebe firması günde yüzlerce fatura alıyor. Document Understanding ile belge tipini classify ediyor, key-value extraction ile "Fatura No, Tarih, Toplam Tutar" çıkarıp ERP'ye aktarıyor.
> **Sınav İpucu:** "key-value extraction", "table extraction", "document classification", "invoice/receipt"

### 1.6 Oracle Digital Assistant
* **Basit Tanım:** Seninle konuşabilen akıllı asistan. "Siparişimi nerede?" diye sorarsın, o anlar ve doğru yere yönlendirir.
* **Teknik Tanım:** Natural language conversation ile kullanıcı isteklerini anlayan, route eden, skills arasında orchestration yapan chatbot platformu.

**Özellikler:**
* Skills routing
* Intent recognition
* Dialogue management
* Interruption handling
* Disambiguation

**Ne Zaman Kullan:**
* Müşteri hizmetleri chatbot
* Multiple skills/domain arasında yönlendirme
* Natural language interface
* Conversational AI ile self-service

**Örnek:** E-ticaret sitesi müşterilerin "siparişim nerede?", "ürün iade nasıl?", "indirim kodu" gibi farklı skill gerektiren soruları Digital Assistant ile yönetiyor.
> **Sınav İpucu:** "chatbot", "natural language conversation", "skills routing", "conversational AI"

#### 🎯 AI Services Hızlı Karar Tablosu

| Soruda Bu Var | Bu Servisi Seç |
| :--- | :--- |
| sentiment, text analysis, PII | **Language** |
| image, object detection, OCR on photo | **Vision** |
| audio, speech, transcription | **Speech** |
| invoice, receipt, table extraction | **Document Understanding** |
| chatbot, conversation, skills | **Digital Assistant** |

**Kritik Ayrım:**
* **Vision OCR** = Resimlerdeki metin (fotoğraf, billboard)
* **Document Understanding OCR** = Yapılandırılmış belgeler (fatura, form)

---

## 2. OCI ML SERVICES (DATA SCIENCE)

### 2.1 OCI Data Science Service
* **Basit Tanım:** Data scientist'ler için hazır oyun alanı - kod yazarsın, modeli eğitirsin, yayınlarsın; server kurulum derdin yok.
* **Teknik Tanım:** Full ML lifecycle platformu. Python ve open-source destekli, managed infrastructure, JupyterLab interface.

**Üç Temel İlke:**
1.  **Accelerated:** Individual data scientist productivity
2.  **Collaborative:** Team sharing, reduce duplicate work
3.  **Enterprise Grade:** OCI security integration, fully managed

**Ne Zaman Kullan:**
* Custom ML modelleri geliştirme
* Data science ekibi collaborative çalışacak
* Python/open-source kullanım
* End-to-end ML lifecycle

**Ne Zaman Kullanma:**
* Hazır AI servisleri yeterli
* Data science yetkinliği yok

**Örnek:** Telekom şirketi churn prediction için custom model geliştiriyor. JupyterLab'de geliştirip Model Catalog'da paylaşıyor, HTTP endpoint olarak deploy ediyor.
> **Sınav İpucu:** "JupyterLab", "full ML lifecycle", "custom model", "collaborative", "Python"

### 2.2 Projects
* **Basit Tanım:** Ana klasör - tüm notebook'ların, modellerin, job'ların toplandığı organizasyon kutusu.
* **Teknik Tanım:** Data science assets'leri organize eden container. Notebook sessions, jobs, pipelines, models, deployments içerir.

**Ne Zaman Kullan:**
* Ekip halinde çalışma
* Farklı ML projelerini izole tutma
* Asset management

**Örnek:** "Fraud Detection", "Credit Scoring", "Customer Segmentation" için ayrı projeler.
> **Sınav İpucu:** "project", "container", "workspace", "organize"

### 2.3 Notebook Sessions
* **Basit Tanım:** Data scientist'in kod yazdığı defter - içinde Python kütüphaneleri hazır, istediğin bilgisayar gücünü seçersin.
* **Teknik Tanım:** JupyterLab environment. CPU/GPU compute shape seçimi, AMD/Intel/Other, managed infrastructure, no manual provisioning.

**Configuration Seçenekleri:**
* Compute shape (CPU/GPU)
* Shape series (AMD/Intel)
* Number of CPUs
* Memory amount
* Block storage
* Networking
* Endpoint type

**Ne Zaman Kullan:**
* Interactive ML development
* Data exploration
* Model training & experimentation

**Ne Zaman Kullanma:**
* Production deployment (Model Deployment kullan)
* Scheduled tasks (Jobs kullan)

**Örnek:** Data scientist Intel shape ile data exploration başlayıp GPU shape'e switch ederek training yapıyor.
> **Sınav İpucu:** "JupyterLab", "interactive", "CPU/GPU selection", "managed infrastructure"

### 2.4 Conda Environments
* **Basit Tanım:** Hazır kütüphane paketi - "ML için gerekli 50 kütüphane" gibi, tek komutla yüklersin.
* **Teknik Tanım:** Prepackaged environment with use-case specific libraries. Environment Explorer'da görünür, Terminal'de install edilir, kernel olarak seçilir.

**Workflow:**
1.  Environment Explorer → Browse
2.  Copy install command
3.  Terminal → Paste & run
4.  Refresh
5.  Select kernel

**Ne Zaman Kullan:**
* Specific ML framework gerekiyor
* Use-case specific packages (NLP, CV)
* Dependency management

**Örnek:** NLP projesi için "NLP" conda environment install ediliyor, NLTK, spaCy, transformers hazır geliyor.
> **Sınav İpucu:** "Conda environment", "prepackaged", "Environment Explorer", "kernel"

### 2.5 ADS SDK (Accelerated Data Science)
* **Basit Tanım:** Oracle'ın data scientist'lere verdiği hazır araç kutusu - sık yapılan işler için kısa yollar.
* **Teknik Tanım:** Oracle'ın Python library'si. Workflow'u simplify/automate eder: data connection, exploration, AutoML, model explanation.

**Özellikler:**
* AutoML
* Model explanation
* OCI Object Storage interface
* Workflow automation

**ADS Workflow (6 Adım):**
1.  **INITIATE** → Model object oluştur
2.  **PREPARE** → `.prepare()` - Artifacts generate
3.  **VERIFY** → `.verify()` - Test without deploy
4.  **SAVE** → `.save()` - Model Catalog'a kaydet
5.  **DEPLOY** → `.deploy()` - REST endpoint oluştur
6.  **PREDICT** → `.predict()` - Inference al

*Status Tracking:* `.summary_status()` - Her adımın durumunu gösterir

**2.5.1 prepare() Method**
* **Ne Yapar:** Model artifacts'ları otomatik generate eder (`score.py`, `runtime.yaml`, serialized model)
* **Ne Zaman Kullan:** Model deployment hazırlığı
* **Örnek:** `model.prepare()` → Tüm deployment dosyaları otomatik oluşur
* **Sınav İpucu:** "generate artifacts", "automation", "no configuration"

**2.5.2 verify() Method**
* **Ne Yapar:** Deployment'ı simulate eder, gerçek deploy etmeden test eder
* **Ne Zaman Kullan:** Pre-deployment testing, artifact validation
* **Örnek:** `model.verify(test_data)` → Local inference, hata varsa burada yakala
* **Sınav İpucu:** "simulate deployment", "test without deploy", "validate"

**2.5.3 save() Method**
* **Ne Yapar:** Modeli Model Catalog'a kaydeder
* **Ne Zaman Kullan:** Model versioning, team collaboration, artifact preservation
* **Örnek:** `model.save()` → Model Catalog'da görünür, paylaşılabilir
* **Sınav İpucu:** "Model Catalog", "versioning", "sharing", "catalog entry"

**2.5.4 deploy() Method**
* **Ne Yapar:** Modeli REST endpoint olarak deploy eder
* **Ne Zaman Kullan:** Production model serving, real-time inference
* **Örnek:** `model.deploy()` → HTTP endpoint oluşur
* **Sınav İpucu:** "REST endpoint", "HTTP API", "real-time serving", "production"

**2.5.5 predict() Method**
* **Ne Yapar:** Deployed endpoint'ten prediction alır
* **Ne Zaman Kullan:** Testing deployed model, production inference
* **Örnek:** `model.predict(new_data)` → Endpoint'e request, result döner
* **Sınav İpucu:** "invoke endpoint", "generate prediction", "deployed model"

### 2.6 Model Catalog
* **Basit Tanım:** Modellerin kütüphanesi - eğittiğin modelleri raftaki gibi saklar, takımla paylaşırsın.
* **Teknik Tanım:** Centralized managed repository. Model metadata, provenance (Git info, source script), versioning. Cross-team sharing.

**Ne Zaman Kullan:**
* Model versioning & tracking
* Team collaboration
* Auditability & compliance
* Reproducibility

**Örnek:** ML ekibi ayda 20 model versiyonu deniyor. Her version metadata ile saklanıyor, 6 ay sonra "o zamanki en iyi model"i geri yükleyebiliyorlar.
> **Sınav İpucu:** "centralized repository", "versioning", "provenance", "metadata", "sharing"

### 2.7 Model Deployments
* **Basit Tanım:** Eğitilmiş modeli internete açan düğme - model artık web adresi olur, isteklere cevap verir.
* **Teknik Tanım:** Model Catalog'daki modelleri HTTP API endpoints olarak deploy eder. Real-time prediction serving, managed infrastructure.

**Ne Zaman Kullan:**
* Real-time prediction
* Model production'a alma
* HTTP API endpoint
* Scalable inference

**Ne Zaman Kullanma:**
* Batch prediction (Job kullan)
* Offline analysis

**Örnek:** E-ticaret sitesi recommendation model'i HTTP endpoint olarak deploy etmiş, web app her sepet değişiminde request atıyor.
> **Sınav İpucu:** "HTTP endpoint", "API", "real-time prediction", "production deployment"

### 2.8 Jobs
* **Basit Tanım:** Tekrarlayan robot işçi - "her gün şu modeli yeniden eğit" dersen otomatik yapar.
* **Teknik Tanım:** Repeatable ML tasks'ı fully managed infrastructure'da define ve run eder. Scheduled/on-demand execution.

**Ne Zaman Kullan:**
* Scheduled model retraining
* Batch inference
* Automated data pipelines
* Production-grade scheduled tasks

**Ne Zaman Kullanma:**
* Interactive development (Notebook kullan)
* Real-time serving (Model Deployment kullan)

**Örnek:** Retail şirketi her Pazar gecesi sales data ile demand forecasting modelini retrain ediyor.
> **Sınav İpucu:** "repeatable tasks", "scheduled execution", "batch processing", "automated"

#### 🎯 Data Science Hızlı Karar Tablosu

| Soruda Bu Var | Bu Component'i Seç |
| :--- | :--- |
| JupyterLab, interactive, kod yazma | **Notebook Sessions** |
| organize, team workspace | **Projects** |
| model saklama, versioning | **Model Catalog** |
| HTTP endpoint, real-time prediction | **Model Deployments** |
| scheduled, repeatable, batch | **Jobs** |
| package management, environment | **Conda** |
| AutoML, Oracle library, simplify | **ADS SDK** |

**Kritik Ayrımlar:**
* **Notebook Sessions** = Interactive development
* **Jobs** = Automated, scheduled tasks
* **Model Catalog** = Storage & versioning
* **Model Deployment** = Production serving

---

## 3. GPU & AI INFRASTRUCTURE

### 3.1 GPU (Graphics Processing Unit)
* **Basit Tanım:** Aynı anda binlerce hesap yapabilen süper hızlı hesap makinesi - CPU tek kişi gibi, GPU binlerce kişi gibi paralel çalışır.
* **Teknik Tanım:** Thousands of lightweight cores ile parallel computing. Deep learning frameworks (TensorFlow, PyTorch) ile entegre. High throughput.

**Neden GPU:**
* Parallel computing (thousands of cores)
* Deep learning optimization
* Batch processing
* Simultaneous requests serving
* High throughput

**Ne Zaman Kullan:**
* Model training (deep learning)
* Large-scale inference
* Transformer models, LLM
* High throughput kritik

**Ne Zaman Kullanma:**
* Simple tabular ML (CPU yeterli)
* Low-volume inference
* Budget constraint

**Örnek:** LLM fine-tuning CPU ile günler sürerken GPU cluster ile saatlere iniyor.
> **Sınav İpucu:** "parallel computing", "thousands of cores", "deep learning", "high throughput"

### 3.2 GPU Architecture Timeline

| Year | Architecture | GPU | Key Feature |
| :--- | :--- | :--- | :--- |
| 2020 | Ampere | **A100** | Tensor cores |
| 2022 | Hopper | **H100** | Transformer engine |
| 2024 | Hopper | **H200** | More memory |
| 2025 | Blackwell | **B200** | Large-scale AI |
| 2025 | Grace Blackwell | **GB200** | Superchip (2x CPU + GPU) |

### 3.3 NVIDIA A100 (Ampere)
* **Basit Tanım:** 2020 model güçlü GPU - "tensor core" denen özel hesap birimleri var.
* **Teknik Tanım:** Ampere architecture, 2020. Tensor cores ile fused multiply-accumulate operations single clock cycle'da.

**Ne Zaman Kullan:**
* Standard deep learning training
* Mid-scale AI workloads
* Cost-performance balance
> **Sınav İpucu:** "A100", "Ampere", "2020", "tensor cores"

### 3.4 NVIDIA H100 (Hopper)
* **Basit Tanım:** 2022 model süper GPU - özellikle transformer modelleri için özel motor var.
* **Teknik Tanım:** Hopper architecture, 2022. Dedicated transformer engine. A100'den daha gelişmiş.

**Ne Zaman Kullan:**
* Transformer models (BERT, GPT, T5)
* LLM training & inference
* State-of-the-art deep learning
> **Sınav İpucu:** "H100", "Hopper", "2022", "transformer engine", "LLM"

### 3.5 NVIDIA H200
* **Basit Tanım:** H100'ün abisi - aynı ama daha çok hafızası var, büyük modeller için ideal.
* **Teknik Tanım:** 2024, H100 benzeri ama more memory. Memory-intensive LLM için optimize.

**Ne Zaman Kullan:**
* Very large LLM (billions of parameters)
* Memory-intensive workloads
* H100'de memory bottleneck
> **Sınav İpucu:** "H200", "2024", "more memory", "large LLM"

### 3.6 NVIDIA B200 (Blackwell)
* **Basit Tanım:** 2025 model en yeni nesil - özellikle dev AI modelleri için tasarlanmış.
* **Teknik Tanım:** Blackwell architecture, 2025. Large-scale AI models için. H100'e göre significant performance improvement.

**Ne Zaman Kullan:**
* Cutting-edge LLM projects
* Maximum performance
* State-of-the-art AI research
> **Sınav İpucu:** "B200", "Blackwell", "2025", "large-scale AI"

### 3.7 NVIDIA GB200 (Grace Blackwell Superchip)
* **Basit Tanım:** Süper güçlü combo - 2 özel CPU + Blackwell GPU birleşmiş, AI datacenterleri için.
* **Teknik Tanım:** 2x NVIDIA Grace CPU + Blackwell GPU unified system. HPC ve AI datacenter için breakthrough processor.

**Ne Zaman Kullan:**
* Superclusters
* Extreme-scale AI workloads
* HPC + AI combined
* Datacenter-level infrastructure
> **Sınav İpucu:** "GB200", "Grace Blackwell", "superchip", "2x CPU", "unified"

### 3.8 NVIDIA L40 / L4
* **Basit Tanım:** Orta sınıf GPU - çok güçlü olmasa da maliyetli değil, küçük-orta işler için yeterli.
* **Teknik Tanım:** Small to medium use cases için cost-effective GPU. Generally available.

**Ne Zaman Kullan:**
* Small to medium workloads
* Cost-optimization
* Inference workloads
* Dev/test environments
> **Sınav İpucu:** "L40", "L4", "cost-effective", "small/medium"

### 3.9 Performance Karşılaştırması
* **H200** → 4X performance of H100 superclusters
* **B200/GB200** → Peak performance of H100 for AI workloads

### 3.10 OCI Data Science AI Quick Actions
* **Basit Tanım:** Hazır LLM'leri tek tuşla GPU'ya deploy eden kolaylık - fine-tune etmek de mümkün.
* **Teknik Tanım:** Popular LLM'leri GPU-powered instances'a deploy eder. Base models fine-tune edip custom deploy. vLLM, text-embedding inference destekler.

**Ne Zaman Kullan:**
* LLM'leri quickly deploy
* LLM fine-tuning
* GPU instances model serving

**Supported Containers:**
* vLLM
* Next generation inference
* Text-embedding inference

**Örnek:** E-ticaret Llama-2'yi product data ile fine-tune edip H100 instance'da deploy ediyor.
> **Sınav İpucu:** "AI Quick Actions", "deploy LLM", "fine-tune", "vLLM", "GPU instances"

#### 🎯 GPU Hızlı Karar Tablosu

| Soruda Bu Var | Bu GPU'yu Seç |
| :--- | :--- |
| Transformer, LLM, dedicated engine | **H100 (Hopper)** |
| More memory, large LLM, 2024 | **H200** |
| Latest, Blackwell, 2025 | **B200** |
| Superchip, unified CPU-GPU, HPC | **GB200** |
| Cost-effective, small/medium | **L40/L4** |
| Tensor cores, 2020 | **A100** |

---

## 4. RDMA & SUPERCLUSTER

### 4.1 RDMA (Remote Direct Memory Access)
* **Basit Tanım:** CPU'yu aradan çıkarıp iki bilgisayarın direkt konuşmasını sağlayan süper hızlı yol.
* **Teknik Tanım:** CPU bypass ederek machine-to-machine data transfer. Extremely low latency, high bandwidth, low CPU overhead.

**Kullanım Alanları:**
* GPU cluster communication
* Database services (ExaCS, Autonomous)
* HPC workloads

**Ne Zaman Kullan:**
* GPU distributed training
* Low latency kritik
* High bandwidth gerekiyor
* Database clusters

**Örnek:** 1000 GPU distributed training yapıyor. RDMA ile GPU'lar microsecond latency'de konuşuyor, CPU overhead olmadan.
> **Sınav İpucu:** "bypass CPU", "low latency", "high bandwidth", "GPU communication"

### 4.2 RoCE (RDMA over Converged Ethernet)
* **Basit Tanım:** RDMA'yı normal Ethernet kabloları üzerinden çalıştıran teknoloji.
* **Teknik Tanım:** RDMA'yı Ethernet fabric üzerinde enable eden protocol. OCI'ın strategic bet. HPC, GPU, database workloads aynı fabric'te.

**Ne Zaman Kullan:**
* Ethernet infrastructure var, RDMA benefits istiyorsun
* Multiple workload types aynı fabric
* Converged network

**Örnek:** OCI datacenter'da aynı Ethernet fabric üzerinde GPU clusters, Oracle Database ve HPC workloads çalışıyor.
> **Sınav İpucu:** "RoCE", "converged ethernet", "strategic bet", "shared fabric"

### 4.3 OCI RDMA Supercluster
* **Basit Tanım:** On binlerce GPU'nun tek bir network içinde konuşabildiği dev cluster.
* **Teknik Tanım:** Three-tier Clos network ile tens of thousands (100,000+) GPU'yu single RDMA network içinde destekleyen lossless networking infrastructure.

**Architecture:**
* Three-tier Clos network
* Block-based (her block = two-tier Clos)
* Non-blocking fabric (any-to-any communication)
* QoS-enabled, buffering optimized

**Bandwidth:**
* 200 Gbps per GPU
* 1.6 Tbps per 8-GPU node

**Ne Zaman Kullan:**
* Very large-scale AI training (10K+ GPUs)
* Distributed LLM training
* Massive parallel computing

**Ne Zaman Kullanma:**
* Small workloads (1-8 GPU)
* Ultra-low latency absolute priority, scale değil

**Örnek:** 50,000 GPU ile GPT-6 benzeri model geliştiriliyor. Tüm GPU'lar single network içinde iletişim kuruyor.
> **Sınav İpucu:** "Supercluster", "tens of thousands GPUs", "100K scale", "three-tier Clos", "lossless"

### 4.4 Latency Değerleri (ÖNEMLI!)

| Scope | Latency (Round Trip) | Use Case |
| :--- | :--- | :--- |
| Intra-rack | < 6.5 μs | Best performance |
| Intra-block | ~6.5 μs | HPC, DB, small GPU |
| Inter-block | ~20 μs | Large GPU workloads |
| Cloud (typical) | 200-400 μs | 10-20x daha kötü! |

**Not:** 20 μs hala typical cloud'dan 10-20x daha iyi!

### 4.5 Block (Architecture)
* **Basit Tanım:** Supercluster içindeki mahalleler - her block kendi içinde daha hızlı.
* **Teknik Tanım:** Organizational unit. Her block kendi two-tier Clos fabric'e sahip. Intra-block 6.5μs, inter-block 20μs.

**Ne Zaman Single Block:**
* Latency-sensitive workloads
* HPC clusters
* Database clusters
* Small to medium GPU workloads

**Örnek:** Oracle Database cluster deploy ediliyor. Control plane single block'a yerleştiriyor, 6.5 μs latency alıyor.
> **Sınav İpucu:** "block", "intra-block 6.5μs", "inter-block 20μs", "single block placement"

### 4.6 Three-Tier Clos Network
* **Basit Tanım:** Üç katlı trafik sistemi - herkes herkesle konuşabilir ama bazen daha fazla kavşaktan geçersin.
* **Teknik Tanım:** Non-blocking network design, 3 hierarchy. 100,000+ GPUs destekler. QoS-enabled, buffering optimized for lossless.

**Ne Zaman Kullan:**
* Massive scale (10K+ GPUs)
* Non-blocking fabric
* Scalability priority

> **Sınav İpucu:** "three-tier Clos", "non-blocking", "200 Gbps per GPU", "1.6 Tbps per node"

### 4.7 Lossless Networking
* **Basit Tanım:** Hiç paket kaybetmeyen network - switch'ler paketi düşürmez.
* **Teknik Tanım:** Switches don't drop packets. Intelligent congestion notification. Higher buffers, QoS-enabled. RDMA requirement.

**Ne Zaman Kullan:**
* RDMA workloads (mandatory)
* GPU distributed training
* Packet loss tolere edilemez

**Örnek:** Distributed training sırasında gradient updates paylaşılıyor. Tek paket kaybı iteration'ı bozar. Lossless networking ile hiçbir paket kaybolmuyor.
> **Sınav İpucu:** "lossless", "no packet drop", "congestion notification", "RDMA requirement"

### 4.8 Network Locality Hints
* **Basit Tanım:** "Bu GPU'lar yan yana, bunlar uzak" bilgisini veren harita - traffic'in çoğu yakında kalır.
* **Teknik Tanım:** Control plane'den gelen topology information. GPU topology optimize edilir. Intra-rack/intra-block traffic maximization.

**Benefit:**
* 85% traffic intra-block
* 50% traffic intra-rack
* Average latency düşer
* Flow collision azalır
* Throughput artar

**Ne Zaman Kullan:**
* Multi-block workloads
* Latency optimization
* Throughput maximization

**Örnek:** 64-GPU workload 2 block'a yayılmış. Locality hints ile %85 traffic intra-block kalıyor, average latency 7-8μs (20μs yerine).
> **Sınav İpucu:** "locality hints", "placement hints", "intra-block traffic", "flow collision reduction"

### 4.9 NVLink
* **Basit Tanım:** NVIDIA GPU'ların kendi aralarında konuştuğu özel kanal - 8 GPU tek node içinde NVLink ile bağlı.
* **Teknik Tanım:** NVIDIA proprietary GPU-to-GPU interconnect within single node. 8x GPU per node.

**Kullanım:**
* Intra-node GPU communication
* Single-node multi-GPU training

**Not:** Cross-node communication için RDMA kullanılır.
> **Sınav İpucu:** "NVLink", "intra-node", "8 GPUs per node", "single node"

### 4.10 Üç Ana Optimizasyon
1.  **Buffer Tuning:**
    * QoS-enabled switches
    * Worst-case latency için buffers
    * Lossless operation garanti

2.  **Placement Control:**
    * HPC/DB → single block (6.5μs)
    * Small GPU → single block
    * Large GPU → multi-block optimized

3.  **Locality Hints:**
    * Network topology transparency
    * 85% intra-block, 50% intra-rack
    * Flow collision azaltma
    * Higher throughput

#### 🎯 RDMA Hızlı Karar Tablosu

| Soruda Bu Var | Bu Kavramı Seç |
| :--- | :--- |
| Bypass CPU, low latency | **RDMA** |
| Ethernet, converged | **RoCE** |
| Tens of thousands GPUs | **Supercluster** |
| 6.5 microseconds | **Intra-block** |
| 20 microseconds | **Inter-block** |
| No packet drop | **Lossless** |
| Topology optimization | **Locality hints** |
| 8 GPUs single node | **NVLink** |

---

## 5. RESPONSIBLE AI

### 5.1 Trustworthy AI - Üç Temel İlke
1.  **LAWFUL (Yasal)**
    * Tüm yasa ve düzenlemelere uyumlu
    * Domain-specific rules (tıbbi cihaz düzenlemeleri)
    * Hakları korur (azınlıklar, çevre)

2.  **ETHICAL (Etik)**
    * Human dignity (insan onuru)
    * Freedom & privacy (özgürlük & gizlilik)
    * Democracy & equality (demokrasi & eşitlik)
    * No unfair bias (ayrımcılık yok)

3.  **ROBUST (Sağlam)**
    * Teknik açıdan sağlam
    * Sosyal açıdan sağlam
    * Unintentional harm önleme

### 5.2 AI Ethics - Üç Ana İlke
1.  **Help Humans & Allow Oversight**
    * Human-in-the-loop
    * Meaningful choice
    * Human oversight
    * Augment not replace

2.  **Never Cause Harm**
    * Physical harm önleme
    * Social harm önleme
    * Safety & security
    * Technical robustness

3.  **Transparent & Fair**
    * Explainable decisions
    * Fair (no bias)
    * Transparent reasoning

### 5.3 Human-Centric Design
* **Basit Tanım:** AI insanın hizmetkarı olmalı, patronu değil - insan her zaman kontrolde.
* **Teknik Tanım:** AI follows principles leaving meaningful opportunity for human choice. Human oversight guaranteed.

**Ne Zaman Kullan:**
* Critical decision systems (medical, legal)
* High-impact automation
* Safety-critical applications

**Örnek:** Doktor AI'dan röntgen analizi istiyor. AI öneri sunuyor ama final teşhisi doktor koyuyor.
> **Sınav İpucu:** "human-centric", "human oversight", "meaningful choice", "human-in-the-loop"

### 5.4 AI Fairness & Bias Prevention
* **Basit Tanım:** AI herkese adil davanmalı - bir ırka, cinsiyete, gruba ayrımcılık yapmamalı.
* **Teknik Tanım:** Equal and just distribution of benefits/costs. Free from unfair bias and discrimination. Consistent performance across demographics.

**Ne Zaman Kullan:**
* Healthcare AI
* Hiring/recruitment systems
* Loan approval systems
* Any decision affecting people

**Örnek:** AI işe alım sistemi çoğunlukla erkek data ile train edilmiş. Kadın adayları unfairly skorluyor. Bias detect edilip data balanced ediliyor.
> **Sınav İpucu:** "fairness", "bias", "discrimination", "equal distribution", "demographic parity"

### 5.5 AI Explainability
* **Basit Tanım:** AI'ın kararını açıklayabilmesi - "neden bu sonuca vardın?" sorusuna cevap vermeli.
* **Teknik Tanım:** Decisions should be explainable to affected parties. Humans must understand reasoning. Transparency in decision-making.

**Ne Zaman Kullan:**
* Healthcare decisions
* Credit/loan rejections
* Legal decisions
* Regulatory compliance (GDPR)

**Örnek:** Kredi reddediliyor. AI: "Debt-to-income %60 (limit %40), 3 ödeme gecikmesi, kredi skoru 580 (minimum 620)".
> **Sınav İpucu:** "explainability", "transparency", "interpretability", "reasoning", "trust"

### 5.6 AI Safety & Security
* **Basit Tanım:** AI güvenli ve sağlam olmalı - hack'lenemez, kötüye kullanılamaz.
* **Teknik Tanım:** Systems must be safe and secure. Technically robust, not open to malicious use. Adversarial attack resistant.

**Ne Zaman Kullan:**
* Critical infrastructure AI
* Healthcare systems
* Financial systems
* Autonomous vehicles

**Örnek:** Otonom araç vision sistemi adversarial attack'e karşı test ediliyor, robust hale getiriliyor.
> **Sınav İpucu:** "safety", "security", "robust", "malicious use prevention", "adversarial resistance"

### 5.7 Responsible AI Implementation
**Üç Adım:**
1.  **GOVERNANCE**
    * Yönetim yapısı kurulumu
    * ↓
2.  **POLICIES & PROCEDURES**
    * Kurallar ve prosedürler
    * ↓
3.  **MONITORING & EVALUATION**
    * Düzenli izleme ve değerlendirme

**Roller:**
* **Developers:** AI system geliştirme
* **Deployers:** Deploy ve operasyon
* **End Users:** Sistemi kullanma

**Örnek:** Şirket AI governance board kuruyor, AI usage policies yazıyor, her quarter audit yapıyor.
> **Sınav İpucu:** "governance", "policies", "procedures", "monitoring", "compliance"

### 5.8 Healthcare AI Challenges
**Challenge 1: Fairness & Bias**
* **Problem:** Biased training data (single demographic)
* **Etki:** Poor performance on underrepresented groups
* **Çözüm:** Diverse, representative datasets

**Challenge 2: Transparency & Trust**
* **Problem:** Complex algorithms, black box
* **Etki:** Difficulty trusting AI
* **Çözüm:** Explainability, regular evaluation

**Örnek:** Deri kanseri AI'ı açık tenli hastalarda eğitilmiş, koyu tenli hastalarda %40 accuracy düşüyor. Data augment ediliyor, model retrain ediliyor.
> **Sınav İpucu:** "healthcare AI", "fairness challenge", "bias in medical data", "diverse datasets"

#### 🎯 Responsible AI Hızlı Karar Tablosu

| Soruda Bu Var | Bu Kavramı Seç |
| :--- | :--- |
| Lawful, ethical, robust | **Trustworthy AI (3 pillars)** |
| Help humans, no harm, transparent | **AI Ethics (3 principles)** |
| Human oversight, meaningful choice | **Human-centric design** |
| Equal treatment, no discrimination | **Fairness & Bias** |
| Why this decision?, reasoning | **Explainability** |
| Adversarial attack, security | **Safety & Security** |
| Governance, policies, monitoring | **Implementation process** |
| Healthcare, one demographic | **Fairness challenge** |

---

## 6. SINAV STRATEJİSİ

### 6.1 Genel Yaklaşım
1.  **Anahtar Kelimeleri Tanı**
    * Soruda geçen critical keywords'leri işaretle
    * Hangi service/component'i işaret ediyor?
2.  **Use-Case'e Bak**
    * "Ne zaman kullan" senaryolarını hatırla
    * Anti-pattern'leri elemele
3.  **Kritik Ayrımları Bil**
    * Benzer kavramları karıştırma
    * Her birinin unique özelliğini bil

### 6.2 Kritik Ayrımlar
* **AI Services vs Data Science:**
    * AI Services = Prebuilt, no data science expertise
    * Data Science = Custom models, Python coding required
* **Vision OCR vs Document Understanding:**
    * Vision = Resimlerdeki metin (foto, billboard)
    * Document Understanding = Strukturlu belgeler (fatura, form)
* **Notebook vs Jobs:**
    * Notebook = Interactive, development
    * Jobs = Automated, scheduled, production
* **Model Catalog vs Model Deployment:**
    * Catalog = Storage, versioning, sharing
    * Deployment = Serving, HTTP endpoint, production
* **RDMA vs RoCE:**
    * RDMA = Technology (CPU bypass)
    * RoCE = Protocol (RDMA over Ethernet)
* **Intra-block vs Inter-block:**
    * Intra-block = 6.5 μs (same block)
    * Inter-block = 20 μs (different blocks)
* **H100 vs H200:**
    * Aynı architecture (Hopper)
    * H200 = H100 + more memory
* **Fairness vs Explainability:**
    * Fairness = Equal outcomes across groups
    * Explainability = Understanding why decision made

### 6.3 Hızlı Referans Tablosu

| Kategori | Anahtar Kelime / Use Case | Servis / Kavram |
| :--- | :--- | :--- |
| **AI Services** | Text analysis, sentiment, PII | Language |
| | Image, object detection, OCR | Vision |
| | Audio, speech-to-text | Speech |
| | Invoice, table extraction | Document Understanding |
| | Chatbot, conversation | Digital Assistant |
| **Data Science** | JupyterLab, interactive | Notebook Sessions |
| | Organize, workspace | Projects |
| | Model storage, versioning | Model Catalog |
| | HTTP endpoint, real-time | Model Deployments |
| | Scheduled, repeatable | Jobs |
| | Package management | Conda |
| | AutoML, simplify | ADS SDK |
| **GPU** | Transformer, LLM, 2022 | H100 |
| | More memory, 2024 | H200 |
| | Latest, Blackwell, 2025 | B200 |
| | Superchip, CPU+GPU | GB200 |
| | Cost-effective, small | L40/L4 |
| **RDMA** | Bypass CPU, low latency | RDMA |
| | Converged ethernet | RoCE |
| | Tens of thousands GPUs | Supercluster |
| | 6.5 microseconds | Intra-block |
| | 20 microseconds | Inter-block |
| | No packet drop | Lossless |
| | Topology optimization | Locality hints |
| **Responsible AI** | Lawful, ethical, robust | Trustworthy AI |
| | Help humans, no harm, transparent | AI Ethics |
| | Human oversight | Human-centric |
| | No discrimination | Fairness |
| | Why this decision | Explainability |
| | Security, adversarial | Safety & Security |

### 6.4 Sınav İpuçları
✅ **Dikkat Et:**
* Anahtar kelimeleri vurgula
* "Ne zaman kullan" senaryolarını hatırla
* Sayıları bil (6.5μs, 20μs, 200 Gbps, etc.)
* Timeline'ı bil (2020→A100, 2022→H100, 2024→H200, 2025→B200)

❌ **Tuzaklara Düşme:**
* Benzer isimleri karıştırma (H100 vs H200)
* Use-case'i yanlış eşleştirme
* Anti-pattern'leri seçme

🎯 **Strateji:**
1.  Soruyu iki kez oku
2.  Anahtar kelimeleri işaretle
3.  Hangi kategori (AI Service, Data Science, GPU, RDMA, Responsible)?
4.  İlgili hızlı referans tablosuna bak
5.  Cevabı işaretle

### 6.5 Örnek Sorular ve Çözüm Yaklaşımı

**Soru Tipi 1: "Which service for..."**
* *"Which OCI AI service for sentiment analysis?"*
* Anahtar: "sentiment analysis"
* Tablo: AI Services → sentiment → **Language** ✅

**Soru Tipi 2: "What is the advantage..."**
* *"What is advantage of Supercluster?"*
* Anahtar: "Supercluster", "advantage"
* Hatırla: Tens of thousands GPUs, massive scale
* Cevap: **Exceptional performance & scalability** ✅

**Soru Tipi 3: "Which feature allows..."**
* *"Which feature allows catalogued models as HTTP endpoints?"*
* Anahtar: "catalogued models", "HTTP endpoints"
* Tablo: Data Science → HTTP endpoint → **Model Deployments** ✅

**Soru Tipi 4: "What latency..."**
* *"What is intra-block latency?"*
* Ezber: Intra-block = **6.5 μs** ✅

---

## 🎯 SON KONTROL LİSTESİ

**Sınava girmeden önce:**

* **AI Services:**
    * [ ] Her servisin ne yaptığını biliyorum
    * [ ] Vision OCR vs Document Understanding ayrımını biliyorum
    * [ ] Use-case'leri biliyorum
* **Data Science:**
    * [ ] ADS SDK workflow'unu biliyorum (6 adım)
    * [ ] Notebook vs Jobs ayrımını biliyorum
    * [ ] Model Catalog vs Deployment ayrımını biliyorum
* **GPU:**
    * [ ] GPU timeline'ı biliyorum (2020→2025)
    * [ ] Her GPU'nun key feature'ını biliyorum
    * [ ] Performance karşılaştırmalarını biliyorum
* **RDMA:**
    * [ ] Latency değerlerini biliyorum (6.5μs, 20μs)
    * [ ] Three-tier Clos architecture'ı biliyorum
    * [ ] Locality hints'i biliyorum
* **Responsible AI:**
    * [ ] 3 pillars biliyorum (Lawful, Ethical, Robust)
    * [ ] 3 principles biliyorum (Help, No harm, Transparent)
    * [ ] Implementation process biliyorum (3 steps)

---

## 📚 Kaynaklar
Bu özet, Oracle Cloud Infrastructure AI Foundations eğitim transkriptlerinden hazırlanmıştır:
* OCI AI Services Overview
* OCI ML Services Overview
* GPU & AI Infrastructure
* RDMA & Supercluster
* Responsible AI
* OCI Data Science Demo