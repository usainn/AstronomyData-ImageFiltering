# AstronomyData-ImageFiltering
Python kullanarak FITS formatındaki astronomi verilerinin görselleştirilmesi, piksel ölçeklendirme ve gelişmiş görüntü işleme (filtreleme, gürültü azaltma) tekniklerinin uygulandığı kapsamlı bir analiz projem.


# Astroenformatik ve Bilimsel Veri Pipeline Modülü 

Bu proje, modern gözlemevlerinin (TUG, DAG vb.) ham veri işleme ihtiyaçlarına yönelik geliştirilmiş; Python ekosistemi üzerinden FITS veri analizi, sinyal iyileştirme ve otonom özellik tespiti süreçlerini otomatize eden teknik bir framework çalışmasıdır.


<img width="425" height="413" alt="indir (4)" src="https://github.com/user-attachments/assets/556e04c7-ab93-4396-8d5b-a9cb756cf0e9" />


##  Gözlemevleri İçin Stratejik Önemi ve Kullanım Alanları

Bu modül, bir gözlemevinin veri işleme hattında (Data Pipeline) şu kritik aşamalarda doğrudan fayda sağlar:

1. **Otonom Veri Kalibrasyonu:** Ham dedektör verilerinin (Raw FITS) bilimsel analize hazır hale getirilmesi için gereken ölçeklendirme (Scaling) süreçlerini standartlaştırır.
2. **Sinyal-Gürültü Oranı (SNR) Optimizasyonu:** Zayıf ışıklı objelerin gözlemlerinde, bilimsel veriyi bozmadan gürültü azaltma (Denoising) yaparak veri kalitesini artırır.
3. **Morfolojik Analiz Otomasyonu:** Galaksilerin sarmal yapılarının, toz bulutlarının ve filamenter yapıların Sato/Meijering filtreleriyle otonom olarak sınıflandırılmasını sağlar.
4. **Hassas Astrometri:** Corner Foerstner algoritmaları sayesinde yıldız merkezlerinin sub-pixel hassasiyetinde tespit edilmesini sağlayarak fotometrik hesaplamalara temel oluşturur.
   
<img width="657" height="342" alt="indir (3)" src="https://github.com/user-attachments/assets/e4c5bdbe-3142-42a7-84f6-00b755f9d898" />

---

##  Teknik Modüller ve Derinlemesine Analiz

###  1. Bilimsel FITS İşleme Ünitesi
* **Astroquery & SkyView:** Proje, sanal gözlemevi protokollerini kullanarak heterojen veri kaynaklarından eşzamanlı veri çekme kabiliyetine sahiptir.
* **Header & WCS Analizi:** Teleskop odak uzaklığı, poz süresi ve koordinat sistemi gibi kritik metadata bilgilerinin manipülasyonu.
* **Gelişmiş Normalizasyon:** * `Z-Scaling`: Gözlem sırasındaki ekstrem parlaklık farklarını normalize ederek objenin en doğal formunu ortaya çıkarır.
    * `Log/Sqrt Transformation`: Derin uzay nesnelerinin (nebula, uzak galaksi) sönük dış yapılarını görünür kılar.

###  2. İleri Seviye Görüntü İşleme Hattı
* **Konvolüsyonel Filtreleme:** SciPy tabanlı 2D konvolüsyon matrisleri ile gözlem gürültülerinin (noise) elimine edilmesi.
* **Lineer Özellik Çıkarımı:** Astronomik görüntülerdeki çizgisel yapıları (gaz akışları, jetler) vurgulayan özel filtreleme algoritmaları.
* **Hassas Obje Lokalizasyonu:** Bilgisayarlı görü teknikleriyle yıldızların ve dairesel kaynakların koordinat tabanlı tespiti.

<img width="959" height="698" alt="indir (2)" src="https://github.com/user-attachments/assets/f45c48d7-a413-4492-9a8d-cba72efaaa32" />

  

---

##  Teknoloji Yığını (Science-Stack)

* **Çekirdek Dil:** Python 3.8+
* **Astro-Kütüphaneler:** `Astropy` (FITS & WCS), `Astroquery` (Veri Madenciliği)
* **Algoritma Geliştirme:** `Scikit-Image` (Feature Engineering), `SciPy` (Signal Processing)
* **Veri Mimarisi:** `NumPy` (N-Dimensional Arrays), `Matplotlib` (Scientific Visualization)

---

##  Entegrasyon ve Dağıtım

Modül, gözlemevi sunucularında veya kişisel araştırma istasyonlarında hızlıca kurulabilir:

```bash
pip install astropy astroquery scikit-image scipy matplotlib numpy
