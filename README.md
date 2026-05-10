# AstronomyData-ImageFiltering
Python kullanarak FITS formatındaki astronomi verilerinin görselleştirilmesi, piksel ölçeklendirme ve gelişmiş görüntü işleme (filtreleme, gürültü azaltma) tekniklerinin uygulandığı kapsamlı bir analiz projesi.


# Astronomik Veri Analizi ve Görüntü İşleme Portfolyosu 

Bu çalışma, **Ulusal Gözlemevleri (TUG, DAG)** bünyesindeki staj ve projelerimde kullanmak üzere geliştirdiğim; ham astronomik verilerin (FITS) bilimsel standartlarda işlenmesi, analiz edilmesi ve modern görüntü işleme teknikleriyle iyileştirilmesini içeren teknik bir portfolyodur.

##  Projenin Amacı ve Kapsamı
Astronomi araştırmalarında kullanılan ham veriler, genellikle standart görsel formatların ötesinde, her pikselin fiziksel bir değer taşıdığı **FITS (Flexible Image Transport System)** formatındadır. Bu projede, bu ham verilerin bilimsel analiz süreçlerine hazırlanması ve bilgisayarlı görü (computer vision) algoritmalarıyla anlamlandırılması üzerine bir iş akışı oluşturulmuştur.

---

##  Teknik Yetkinlikler ve Uygulamalar

###  1. FITS Veri Analizi ve Bilimsel Görselleştirme
* **Veri Madenciliği:** `astroquery` kütüphanesi kullanılarak NASA/SkyView üzerinden M31 (Andromeda) gibi gök cisimlerine ait gerçek gözlem verileri çekilmiştir.
* **Header Analizi:** FITS dosyalarının metadata (başlık) bilgileri üzerinden teleskop ve gözlem parametrelerinin analizi yapılmıştır.
* **Piksel Ölçeklendirme (Scaling):** Ham verideki geniş dinamik aralığı insan gözünün algılayabileceği seviyeye getirmek için şu teknikler uygulanmıştır:
    * **Z-Scaling:** Verideki gürültüyü baskılayıp sinyali ön plana çıkaran istatistiksel ölçeklendirme.
    * **Logaritmik ve Karekök Dönüşümleri:** Galaktik kollar gibi düşük parlaklıktaki detayların belirginleştirilmesi.

###  2. Gelişmiş Görüntü İşleme ve Özellik Çıkarımı
* **Denoising (Gürültü Azaltma):** Gözlem sırasında oluşan termal ve elektronik gürültüleri temizlemek amacıyla Gaussian Blurring ve 2D Konvolüsyon teknikleri uygulanmıştır.
* **Özellik Belirginleştirme:** `skimage` tabanlı **Sato** ve **Meijering** filtreleri ile galaksilerdeki filamenter yapıların ve toz bulutlarının analizi gerçekleştirilmiştir.
* **Nesne Tespiti:** **Corner Foerstner** algoritması kullanılarak yıldız merkezlerinin ve dairesel objelerin yüksek hassasiyetle tespiti sağlanmıştır.

---

##  Teknoloji Yığını

Bu projede kullanılan kütüphaneler, modern astroenformatik çalışmalarının temelini oluşturmaktadır:
* **Astroenformatik:** `Astropy`, `Astroquery`
* **Görüntü İşleme:** `Scikit-Image`, `SciPy`, `OpenCV`
* **Veri Analizi & Görselleştirme:** `NumPy`, `Matplotlib`

---

##  Kurulum ve Kullanım

Proje, Google Colab üzerinde veya yerel bir Jupyter ortamında çalıştırılabilir. Gerekli bağımlılıkları yüklemek için:

```bash
pip install astropy astroquery scikit-image scipy matplotlib numpy
