# 🎴 FLASHCARDS - Reinforcement Learning (ÖZET)

## TEMEL KAVRAMLAR

### Kart 1
**Ön Yüz:** Reinforcement Learning tanımı? Köpek analojisi?
**Arka Yüz:** 
**Tanım:** Agent environment ile etkileşerek feedback (reward/penalty) alarak öğrenir
**Köpek:** Doğru → Ödül, Yanlış → Ceza → Zamanla öğrenir
**Önemli:** Labeled data YOK, feedback VAR!

### Kart 2
**Ön Yüz:** 7 temel RL terimini say.
**Arka Yüz:** 
1. **Agent** (Öğrenen)
2. **Environment** (Çevre)
3. **State** (Durum)
4. **Action** (Hareket)
5. **Policy** (Strateji)
6. **Reward** (Ödül)
7. **Penalty** (Ceza)

### Kart 3
**Ön Yüz:** Agent nedir? Örnekler?
**Arka Yüz:** 
**Tanım:** Öğrenen/karar veren varlık
**Özellikleri:** Environment ile etkileşir, actions yapar, feedback'den öğrenir
**Örnekler:** Self-driving car, Dog, Robotic arm, Game AI

### Kart 4
**Ön Yüz:** Environment nedir? Örnekler?
**Arka Yüz:** 
**Tanım:** Agent'ın etkileştiği dış sistem, "dünya"
**Örnekler:** Road (car için), Eğitim alanı (dog için), Warehouse (robot için)

### Kart 5
**Ön Yüz:** State nedir? Örnekler?
**Arka Yüz:** 
**Tanım:** Environment'ın o andaki durumu
**Self-driving:** Kameranın gördüğü
**Robot arm:** Kolun pozisyonu, eşyanın yeri
**Anlam:** "Şu anda ne oluyor?"

### Kart 6
**Ön Yüz:** Action nedir? Örnekler?
**Arka Yüz:** 
**Tanım:** Agent'ın yapabileceği hareketler
**Self-driving:** Left, Right, Straight
**Dog:** Sit, Roll, Pick ball
**Robot:** Pick, Move, Place

### Kart 7
**Ön Yüz:** Policy nedir? "Brain of the agent" neden?
**Arka Yüz:** 
**Tanım:** State→Action mapping stratejisi
**"Brain":** Agent'ın nasıl karar vereceğini belirler
**Örnek:** "Kırmızı ışık → Dur" stratejisi

### Kart 8
**Ön Yüz:** Reward vs Penalty farkı ve örnekler?
**Arka Yüz:** 
**Reward:** Pozitif feedback, doğru hareket
- Car: Güvenli sürüş, Dog: Treat

**Penalty:** Negatif feedback, yanlış hareket
- Car: Kaza, Dog: Kızmak

### Kart 9
**Ön Yüz:** Optimal Policy nedir ve nasıl bulunur?
**Arka Yüz:** 
**Tanım:** En çok reward kazandıran strateji
**Nasıl:** Q-Learning, Deep Q-Learning algoritmaları
**Süreç:** Random → Training → Learning → Optimal

## ÖRNEKLER

### Kart 10
**Ön Yüz:** Self-driving car örneğinde tüm RL terimlerini eşleştir.
**Arka Yüz:** 
- **Agent:** Car + zekaası
- **Environment:** Road, çevre
- **State:** Kameranın gördüğü
- **Actions:** Left, Right, Straight
- **Policy:** "Bu görünce şunu yap"
- **Reward:** Güvenli sürüş
- **Penalty:** Kaza

### Kart 11
**Ön Yüz:** Robotic arm training 6 adımı?
**Arka Yüz:** 
1. **Set Environment:** Robot, warehouse, goods
2. **Define State:** Pozisyon, oryantasyon
3. **Define Actions:** Pick, move, place
4. **Decide Reward/Penalty:** Doğru yere koy (+), düşür (-)
5. **Training:** Exploration → Exploitation
6. **Multiple Iterations:** Optimal strategy

### Kart 12
**Ön Yüz:** RL'nin 4 günlük hayat kullanım alanı?
**Arka Yüz:** 
1. **Autonomous Vehicles** (Tesla)
2. **Smart Home** (Alexa, Siri)
3. **Industrial Automation** (Factory robots)
4. **Gaming** (Video game AI)

## KARŞILAŞTIRMALAR

### Kart 13
**Ön Yüz:** RL vs Supervised vs Unsupervised - Veri ve öğrenme?
**Arka Yüz:** 
**Supervised:** Labeled data, examples'tan
**Unsupervised:** Unlabeled data, pattern'lerden
**RL:** Feedback (reward/penalty), trial-error'dan

### Kart 14
**Ön Yüz:** Exploration vs Exploitation farkı?
**Arka Yüz:** 
**Exploration:** Yeni action'lar dene, keşfet (ilk aşama)
**Exploitation:** Öğrenilen iyi action'ları kullan (sonraki aşama)

### Kart 15
**Ön Yüz:** RL'de labeled data var mı? Feedback var mı?
**Arka Yüz:** 
**Labeled Data:** YOK! (Supervised'dan farkı)
**Feedback:** VAR! (Reward/Penalty şeklinde)
**Bu yüzden:** Trial-error ile öğrenir

---

## 📝 Hızlı Hatırlatıcılar

**KÖPEK ANALOJİSİ:** Doğru→Ödül, Yanlış→Ceza, Zamanla öğrenir
**7 TERİM:** Agent, Environment, State, Action, Policy, Reward, Penalty
**POLICY = BRAIN:** State→Action stratejisi
**OPTIMAL POLICY:** Q-Learning ile bulunur
**GÜNLÜK:** Tesla, Alexa, Gaming, Robots
**FARK:** Labeled YOK ama Feedback VAR!