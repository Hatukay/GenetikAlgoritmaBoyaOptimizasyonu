#  Genetik Algoritma ile Endüstriyel Boya Karışımı Optimizasyonu

Bu proje, bir endüstriyel boya karışım problemini **Genetik Algoritma (GA)** kullanarak optimize etmek amacıyla geliştirilmiştir. Belirli kısıtlar altında en yüksek renk kalitesi puanını veren pigment oranları hesaplanmıştır.

##  Proje Senaryosu
Bir fabrika, iki tür pigment karışımıyla ideal renk yoğunluğunu yakalamak istemektedir.

* **Amaç Fonksiyonu:** `y = 5x₁ + 2x₂ - x₁x₂` (Maksimizasyon)
* **Değişkenler:**
    * `x₁`: Pigment A oranı (%)
    * `x₂`: Pigment B oranı (%)
* **Kısıtlar:**
    1.  `x₁ + x₂ = 100` (Karışım toplamı %100 olmalı)
    2.  `x₁ ≥ 30` (Pigment A en az %30 kullanılmalı)

##  Kurulum ve Çalıştırma

Bu projeyi çalıştırmak için bilgisayarınızda Python yüklü olmalıdır. Alternatif olarak `.ipynb` dosyasını Google Colab üzerinde de çalıştırabilirsiniz.

1.  Gerekli kütüphaneleri yükleyin:
    ```bash
    pip install numpy matplotlib pandas
    ```
2.  Proje dosyasını (`.ipynb`) Jupyter Notebook veya VS Code ile açıp hücreleri sırasıyla çalıştırın.

##  Algoritma Detayları
Projede kullanılan Genetik Algoritma parametreleri ve yöntemleri:

* **Kodlama:** Reel sayı kodlaması (Real-value encoding).
* **Seçilim:** Turnuva Seçimi (Tournament Selection).
* **Çaprazlama:** Aritmetik Çaprazlama (Arithmetic Crossover).
* **Mutasyon:** Rastgele değer ekleme (Gaussian perturbation).
* **Kısıt Yönetimi:** Onarım (Repair) metodu kullanılarak `x₁ + x₂ = 100` eşitliği her adımda korunmuştur.

##  Sonuçlar
Algoritma 100 jenerasyon sonunda optimum karışıma başarıyla yakınsamıştır.

* **Bulunan En İyi x₁:** %100
* **Bulunan En İyi x₂:** %0
* **Maksimum Skor:** 500

Grafik analizine göre algoritma ilk jenerasyonlarda hızlı bir öğrenme süreci geçirmiş ve global maksimum noktasına ulaşmıştır.

---
**Hazırlayan:**
Ad Soyad: Hatukay Duran Alabay
Öğrenci No: 2112721062
