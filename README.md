# Mühendislik Fakültesi Öğrenci Veri Seti: Keşifsel Veri Analizi (EDA) ve Özellik Hazırlama

## 📝 Proje Tanımı
Bu proje, bir mühendislik fakültesi öğrenci veri seti üzerinde temel Keşifsel Veri Analizi (EDA) adımlarını uygulamak, eksik verileri yönetmek ve makine öğrenmesi modellemesine hazırlık için veri ön işleme (Data Preprocessing) süreçlerini standart bir iş akışında gerçekleştirmek amacıyla hazırlanmıştır.

##Ödevin Amacı 
* Keşifsel Veri Analizi (EDA) ile veri dağılımlarını ve Bölüm/Lise/İkamet etkilerini anlamak.
* Eksik veri analizi yapmak ve uygun imputasyon stratejilerini belirlemek.
* Kategorik ve sayısal verileri makine öğrenmesi için kullanılabilir, düzenli bir özellik matrisi haline getirmek.
* Örnek modelleme öncesi veri temizleme ve dönüşüm adımlarını standart bir iş akışında uygulamak.

## 🛠 Kullanılan Teknolojiler

* **Dil:** Python
* **Kütüphaneler:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn (Imputer, MinMaxScaler, OneHotEncoder)
* **Ortam:** Jupyter Notebook (Anaconda)

## 📌 Yapılan İşlemler ve Adımlar

Proje, standart bir veri bilim süreci takip edilerek aşağıdaki beş ana başlık altında tamamlanmıştır:

### 1. Veri Yükleme ve İlk İnceleme
* `muhendislik_ogrenci_veriseti.csv` dosyası, karakter problemi çözülerek (`encoding="utf-8-sig"`) Pandas DataFrame'e aktarıldı.
* Sütun tipleri, temel özet istatistikleri ve ilk satırlar kontrol edilerek veri setinin ilk yapısı anlaşıldı.

### 2. Eksik Veri Analizi
* Sütun bazında eksik değer sayıları ve oranları çıkarıldı.
* Eksikliklerin desenleri (rastgele, belirli bir kategoriye bağlı vb.) değerlendirilerek yorumlandı.

### 3. Betimsel İstatistikler ve Şekil Ölçüleri
* Sayısal sütunlar için merkezi eğilim ölçüleri (Ortalama, Medyan, Mod) hesaplandı.
* Yayılım ölçüleri (Varyans, Standart Sapma, Çeyrekler Arası Açıklık (IQR)) belirlendi.
* Veri dağılımlarının şekli için çarpıklık (skewness) değerleri hesaplandı.

### 4. Veri Dönüşümleri ve Özellik Hazırlama
**Veri Temizleme:** Boş string değerler `NaN` olarak dönüştürüldü.
**İmputasyon:** Eksik veriler dolduruldu:
    * Sayısal verilerde: Medyan (aykırı değerlere dayanıklı olması nedeniyle) kullanıldı.
    * Kategorik verilerde: Mod (en sık görülen değer) kullanıldı.
* **Özellik Mühendisliği:**
    * Kategorik veriler makine öğrenmesi için **One-Hot Encoding** ile dönüştürüldü.
    * Sayısal veriler, farklı ölçeklerin etkisini dengelemek amacıyla **MinMaxScaler** kullanılarak ölçeklendi.

### 5. Görselleştirmeler
*`YGS_Puani` ve `Mezuniyet_Notu` dağılımlarını incelemek için **Histogramlar** oluşturuldu.
* Bölümler arası farklılıkları gözlemlemek amacıyla Bölümlere göre `YGS_Puani` ve `Mezuniyet_Notu` **Boxplot**'ları çizildi.
* `YGS_Puani` ve `Mezuniyet_Notu` arasındaki ilişkinin Bölüme göre ayrışmasını göstermek için **Serpilme Diyagramı** (`Bolume` göre renklendirilmiş) oluşturuldu.
* Her bir grafik detaylıca değerlendirildi.

## 🚀 Proje Dosyaları

* `mlodev.ipynb`: Projenin tüm kodlarını, çıktılarını ve her adıma ait yorumları (açıklamaları) içeren ana Jupyter Notebook dosyasıdır.
* `muhendislik_ogrenci_veriseti.csv`: Kullanılan orijinal veri seti.

---
