# AstronomyData-ImageFiltering
Python kullanarak FITS formatındaki astronomi verilerinin görselleştirilmesi, piksel ölçeklendirme ve gelişmiş görüntü işleme (filtreleme, gürültü azaltma) tekniklerinin uygulandığı kapsamlı bir analiz projesi.



# AstroImage-Processor: FITS Veri Analizi ve Gelişmiş Görüntü İşleme 🔭

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Astropy](https://img.shields.io/badge/Powered%20by-Astropy-orange.svg)](https://www.astropy.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Bu proje, uzay gözlemlerinden elde edilen ham **FITS (Flexible Image Transport System)** verilerinin işlenmesi, görselleştirilmesi ve gelişmiş görüntü işleme algoritmaları kullanılarak analiz edilmesini içerir. Tek bir Google Colab notebooku üzerinden, astronomik verilerin bilimsel standartlarda nasıl manipüle edileceği ve bilgisayarlı görü (computer vision) tekniklerinin bu verilere nasıl uygulanacağı uygulamalı olarak gösterilmektedir.

---

## 📑 İçerik Tablosu
1. [Proje Hakkında](#proje-hakkında)
2. [Temel Özellikler](#temel-özellikler)
3. [Kullanılan Veri Setleri](#kullanılan-veri-setleri)
4. [Teknik Detaylar](#teknik-detaylar)
5. [Kurulum ve Kullanım](#kurulum-ve-kullanım)
6. [Görsel Sonuçlar](#görsel-sonuçlar)

---

## 🧐 Proje Hakkında

Astronomi araştırmalarında görüntüler genellikle standart JPEG veya PNG formatında değil, her pikselin bilimsel bir değer (foton sayısı, yoğunluk vb.) taşıdığı **FITS** formatında saklanır. Bu proje, ham FITS verisini alıp:
- İnsan gözünün görebileceği bir forma dönüştürmeyi (Scaling),
- Gürültüden arındırmayı (Denoising),
- Ve derin yapısal özelliklerini (Feature Extraction) ortaya çıkarmayı amaçlar.

---

## ✨ Temel Özellikler

### 🌌 Astronomik Veri Analizi
* **Astroquery Entegrasyonu:** NASA SkyView servisleri üzerinden M31 (Andromeda Galaksisi) verilerinin otomatik olarak çekilmesi.
* **FITS Manipülasyonu:** Dosya başlık (header) bilgilerinin incelenmesi ve Python ile özel FITS dosyalarının oluşturulması.
* **Gelişmiş Ölçeklendirme Teknikleri:** * `Min-Max Scaling` (Yoğunluk Normalizasyonu)
    * `Z-Scaling` (İstatistiksel Görselleştirme)
    * `Logaritmik & Karekök Normalizasyon` (Düşük ışıklı detayların ve galaktik kolların vurgulanması)
    * `ZScaleInterval` ile profesyonel kontrast ayarı.

### 🖼️ Görüntü İşleme ve Filtreleme
* **Gürültü Temizleme (Denoising):** Gaussian Kernel konvolüsyonu kullanılarak ham verideki sinyal gürültüsünün azaltılması.
* **Kenar ve Yapı Tespiti:** * `Sato` ve `Meijering` filtreleri kullanılarak galaksi içindeki toz bulutlarının ve doğrusal yapıların belirginleştirilmesi.
    * `Corner Foerstner` algoritması ile yıldız merkezlerinin ve dairesel objelerin hassas tespiti.
* **Multiscale Analysis:** Yerel özelliklerin (local features) farklı ölçeklerde analiz edilerek veri setinden çıkarılması.

---

## 🛠 Teknik Detaylar

Projede kullanılan temel kütüphaneler ve görevleri:

| Kütüphane | Kullanım Amacı |
| :--- | :--- |
| **Astropy** | FITS okuma/yazma, görselleştirme ve birim sistemleri. |
| **Astroquery** | Çevrimiçi astronomik veri arşivlerine erişim. |
| **Scikit-Image** | Gelişmiş filtreleme (Sato, Meijering) ve özellik tespiti. |
| **SciPy** | 2D Konvolüsyon ve sinyal işleme algoritmaları. |
| **Matplotlib** | Bilimsel görselleştirme ve histogram analizleri. |
| **NumPy** | Matris işlemleri ve veri normalizasyonu. |

---

## 🚀 Kurulum ve Kullanım

1. **Depoyu Klonlayın:**
   ```bash
   git clone [https://github.com/kullaniciadi/AstroImage-Processor.git](https://github.com/kullaniciadi/AstroImage-Processor.git)
   cd AstroImage-Processor
