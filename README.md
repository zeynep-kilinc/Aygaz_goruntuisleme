# Aygaz_goruntuisleme
Hayvan Sınıflandırma Projesi - CNN ile Görüntü İşleme

# PROJE TANITIMI

Bu proje, görüntü işleme teknikleri ve evrişimsel sinir ağları (CNN) kullanarak 10 farklı hayvan sınıfını sınıflandırmayı amaçlamaktadır. Kaggle platformu üzerinde geliştirilmiş olan bu projede, derin öğrenme modelleri eğitilmiş ve manipüle edilmiş test setleri ile model performansı analiz edilmiştir.

# VERİ SETİ BİLGİLERİ

Veri seti: Animals with Attributes 2 (AwA2)

Toplam Görsel Sayısı: 37,322

Sınıf Sayısı: 50 (Bu projede 10 sınıf kullanıldı.)

Boyutlar: 64x64 piksellik renklendirilmiş RGB formatında görseller

Veri Kökeni: Farklı hayvan türlerine ait resimlerden oluşmaktadır.

Bu projede veri seti, başlangıçta 10 sınıfa indirgenmiş ve eğitim, doğrulama ve test setlerine bölünmüştür.

# KULLANILAN ARAÇ VE KÜTÜPHANELER

Python 3

TensorFlow ve Keras

OpenCV

NumPy

Matplotlib ve Seaborn

# PROJE AŞAMALARI

1. Veri Hazırlama

Veri seti indirildi ve yeniden boyutlandırıldı.

Eğitim, doğrulama ve test setlerine ayrıldı.

Veri artırma teknikleri uygulandı (döndürme, yansıtma, parlaklık değişiklikleri).

2. Model Tasarımı ve Eğitim

CNN modeli oluşturuldu (4 evrişim katmanı ve 2 yoğun bağlantı katmanı).

Model, erken durdurma ve model kaydetme mekanizmaları ile optimize edildi.

Eğitim sırasında eğitim/doğrulama kayıpları ve başarı oranları izlenerek model geliştirildi.

3. Performans Değerlendirmesi

Test seti üzerinde model performansı analiz edildi.

Karışıklık matrisi ve sınıflandırma raporları çıkarıldı.

4. Manipüle Edilmiş Test Setleri ve Analizler

Manipüle Edilmiş Test Setleri:

Parlaklık artışı ve azalma manipülasyonları uygulandı.

Renk sabitliği algoritması (Gray World) uygulandı.

Her manipülasyon sonrası model performansı test edildi.

# SONUÇLAR

# 1. Orijinal Test Seti
Doğruluk (Accuracy): %67.00
# 2. Manipüle Edilmiş Test Setleri
# Bright Manipülasyonu:
Doğruluk (Accuracy): %64.31
Renk Sabitliği Sonrası Doğruluk: %57.03
# Dark Manipülasyonu:
Doğruluk (Accuracy): %67.28
Renk Sabitliği Sonrası Doğruluk: %61.54
Genel Değerlendirme:
Manipülasyon Sonuçları:

Bright manipülasyonu, modelin performansında hafif bir düşüşe neden olmuştur.
Dark manipülasyonu ise modelin performansını orijinal test setine kıyasla korumuş, hatta biraz artırmıştır.
Renk Sabitliği Algoritması Sonuçları:

Her iki manipülasyon türünde de renk sabitliği algoritması doğruluk oranını düşürmüştür.
Bu durum, algoritmanın model üzerinde iyileştirme sağlamadığını ve bazı renk bilgilerini bozarak performansı olumsuz etkilediğini göstermektedir.
Sonuç Önerisi:

Modelin manipülasyonlara daha dayanıklı hale getirilmesi için daha kapsamlı veri artırma ve model iyileştirme yöntemleri uygulanabilir.
Alternatif renk sabitliği algoritmaları (örneğin Retinex) test edilmelidir.
# Genel Sonuç Yorumu:
Manipüle edilmiş test setleri üzerinde doğruluk oranlarında düşüşler gözlemlenmiştir. Bu durum, modelin manipüle edilmiş ve renksel farklılıklar içeren görsellerde daha zayıf performans gösterdiğini ortaya koymaktadır. Renk sabitliği algoritması uygulanması, manipüle edilmiş setlerde bazı iyileşmeler sunsa da beklenen düzeyde bir artış sağlamamıştır. Modelin özellikle parlaklık manipülasyonlarına daha duyarlı olduğu gözlemlenmiştir.
# KAGGLE LİNKİ: 
https://www.kaggle.com/code/zeyyser/notebook18665f70c4
