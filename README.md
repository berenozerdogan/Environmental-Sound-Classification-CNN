# CNN Tabanlı Derin Öğrenme ile Çevresel Ses Sınıflandırması

Bu proje, UrbanSound8K veri setini kullanarak 10 farklı çevresel ses sınıfını (siren, matkap, köpek havlaması vb.) derin öğrenme yöntemleriyle sınıflandırmayı amaçlar.

## Proje Özeti
Ses verileri doğrudan sayısal sinyaller yerine, zaman-frekans düzleminde temsil edilen **Mel-Spektrogram** görüntülerine dönüştürülmüştür. Bu görüntüler, bir Evrişimli Sinir Ağı (CNN) modeline girdi olarak verilmiş ve yüksek doğrulukla sınıflandırma yapılmıştır.

## Veri Seti
Projelerde kullanılan **UrbanSound8K** veri seti, 8732 adet etiketli ses klibi içermektedir.
[Veri Seti Kaynağı](https://www.kaggle.com/datasets/chrisfilo/urbansound8k)

## Teknik Detaylar
* **Özellik Çıkarma:** Librosa kütüphanesi kullanılarak Mel-Spektrogram dönüşümü yapılmıştır.
* **Model Mimarisi:** * Convolutional Layers (Evrişimli Katmanlar)
    * MaxPooling & Dropout (Aşırı öğrenmeyi önleme)
    * Dense Layers (Tam bağlantılı katmanlar)
* **Başarım:** Test setinde **%88.13 doğruluk (accuracy)** elde edilmiştir.

## Sonuçlar
* **Doğruluk:** %88.13
* **Kayıp (Loss):** 0.67
* Model, özellikle belirgin frekans aralıklarına sahip olan seslerde (siren vb.) oldukça yüksek başarı göstermiştir.

## Kullanılan Araçlar
* Python (Keras, TensorFlow, Librosa, Scikit-learn)
* Google Colab (Eğitim için GPU desteği)
