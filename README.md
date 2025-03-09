![image](https://github.com/user-attachments/assets/2d55a29c-e0d4-4294-a8ef-d7bad1ee2135)

# DistilBERT Nedir?

DistilBERT, BERT modelinin daha küçük, daha hızlı ve hafif bir versiyonudur. Hugging Face tarafından geliştirilen bu model, **Knowledge Distillation (Bilgi Damıtma)** yöntemiyle eğitilmiştir. Bu sayede:

- BERT’in %40 daha az parametresine sahiptir.
- %60 daha hızlı çalışır.
- Ancak BERT’in doğruluğunun %97’sini korur (çok az performans kaybı yaşanır).

DistilBERT, çift yönlü (bidirectional) transformer mimarisini kullanır, yani metnin hem solunu hem de sağını okuyarak anlam çıkarır.

---

## Neden DistilBERT Kullanılır?

DistilBERT, hesaplama maliyetini düşürmek ve daha hızlı NLP modelleri oluşturmak için kullanılır:

- **Daha Hafif:** Daha az RAM ve depolama alanı kullanır.
- **Daha Hızlı:** BERT’e göre 2 kat daha hızlı çalışır.
- **Düşük Güç Tüketimi:** Mobil ve edge cihazlarda çalıştırmak için idealdir.
- **Yüksek Performans:** BERT’e çok yakın doğruluk sunar.

Özetle, BERT kadar güçlü bir model çalıştırmak için yeterli donanımınız yoksa veya hız kritikse, DistilBERT mükemmel bir alternatiftir.

---

## DistilBERT Kullanım Alanları

1. **Metin Sınıflandırma**
   - Spam tespiti
   - Haber, e-posta veya müşteri yorumlarını kategorize etme

2. **Duygu Analizi (Sentiment Analysis)**
   - Sosyal medya yorumlarının duygu durumunu belirleme
   - Müşteri geri bildirimlerini olumlu/olumsuz/nötr olarak analiz etme

3. **Adlandırılmış Varlık Tanıma (NER)**
   - Metinde kişi, yer, organizasyon gibi özel isimleri belirleme
   - Hukuki veya finansal belgelerde kritik bilgileri ayıklama

4. **Soru-Cevap Sistemleri (Question Answering)**
   - Belirli bir metinden sorulara cevap verme
   - Chatbot ve sanal asistan geliştirme

5. **Metin Özetleme**
   - Haber makalelerini veya uzun belgeleri kısaltma
   - Akademik ve hukuki dokümanlardan önemli bilgileri çıkarma

6. **Makine Çevirisi**
   - Düşük hesaplama gücü gerektiren çeviri sistemleri geliştirme
   - Çok dilli uygulamalarda metinleri çevirmek

7. **Arama Motorları ve Bilgi Getirme**
   - Kullanıcı sorgularına daha doğru yanıt veren arama sistemleri oluşturma
   - Dokümanlar içinde belirli bilgileri bulma (örneğin, hukuk veya sağlık alanında)

DistilBERT, BERT'e göre daha hızlı ve hafif olduğu için mobil cihazlar, düşük güçlü donanımlar ve gerçek zamanlı uygulamalar için idealdir.

---

## Transformers Nedir?

Transformers, doğal dil işleme (NLP) ve diğer sekans tabanlı görevlerde kullanılan, **kendine dikkat (self-attention)** mekanizmasına dayalı bir yapay sinir ağı mimarisidir. 2017’de Google’ın "Attention is All You Need" makalesiyle tanıtılmıştır.

Transformers, geleneksel RNN ve LSTM gibi ardışık işleyen modellere kıyasla paralel işlem yaparak çok daha hızlı ve etkili çalışır.

---

## Transformer Mimarisinin Genel Yapısı

![image](https://github.com/user-attachments/assets/5807ac12-22ad-45cc-a9a3-01ea36f99b81)

Transformer modeli, **kodlayıcı (encoder)** ve **kod çözücü (decoder)** olmak üzere iki ana bileşenden oluşur:

1. **Kodlayıcı (Encoder)**
   - Girdi metnini işler ve daha anlamlı bir vektör temsiline dönüştürür.
   - BERT gibi modeller yalnızca kodlayıcı kısmını kullanır.

2. **Kod Çözücü (Decoder)**
   - Kodlayıcıdan gelen bilgiyi kullanarak çıkış metnini üretir.
   - GPT ve T5 gibi modeller, kod çözücü tabanlıdır.

### Öne Çıkan Bileşenler:
- **Kendine Dikkat (Self-Attention):** Kelimelerin ilişkisini anlamaya yarar.
- **Çoklu Kafa Dikkati (Multi-Head Attention):** Farklı anlam bağlantılarını öğrenir.
- **Beslemeli İleri Ağ (Feedforward Neural Network):** Daha derin temsiller oluşturur.
- **Pozisyon Kodlaması (Positional Encoding):** Kelimelerin sırasını model tarafından anlaşılır hale getirir.

---

## Neden Popüler?

Transformerlar şu nedenlerle popülerdir:
- Paralel İşleme Yeteneği
- Uzun Bağlamları Anlayabilme
- Farklı NLP Görevlerine Uygunluk
- Transfer Öğrenmeye Uygunluk

Bu avantajlar sayesinde transformer modelleri yaygın şekilde kullanılır.

---

## BERT Nedir?

![image](https://github.com/user-attachments/assets/8b8b21c2-73fc-405f-9557-c293564855ed)

BERT (Bidirectional Encoder Representations from Transformers), Google tarafından geliştirilen çift yönlü transformer tabanlı bir NLP modelidir. BERT'in en büyük yeniliği, kelimeleri çift yönlü (bidirectional) işlemesi ve dilin bağlamını daha iyi kavramasıdır.

### Masked Language Model (MLM) ve Next Sentence Prediction (NSP)
BERT’in eğitimi için iki temel teknik kullanılır:

- **Masked Language Model (MLM):** Maskelenmiş kelimeleri tahmin eder.
- **Next Sentence Prediction (NSP):** İki cümlenin bağını tahmin eder.
  
---

## DistilBERT Nasıl Çalışır?

![The-DistilBERT-model-architecture-and-components (1)](https://github.com/user-attachments/assets/2226d4bd-fead-47d6-ba55-8de38b4dd105)

DistilBERT, BERT’in bilgi yoğunluğunu koruyarak parametrelerini azaltır. Bu süreç Knowledge Distillation ile gerçekleştirilir.

- Katman sayısı yarıya düşürülmüştür.
- NSP görevi kaldırılmıştır.
- Soft Label Loss, MLM Loss ve Cosine Embedding Loss kullanılarak eğitilmiştir.

DistilBERT, BERT’e kıyasla %40 daha az parametreye sahiptir, %60 daha hızlı çalışır ve %97 doğruluk korur.
