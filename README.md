# Thermal Bridge Detection Using Drone-Based RGB and Thermal Imagery

Bu repository, bina çatıları üzerindeki **ısı köprülerinin (thermal bridges)** tespitine yönelik olarak geliştirilen bir analiz / makine öğrenmesi çalışmasını içermektedir. Projede, literatürde yer alan ve açık erişimli olarak sunulan **TBBR (Thermal Bridges on Building Rooftops)** veri seti kullanılmıştır.


---

## Projenin Amacı

Bu projenin temel hedefleri:

- Drone tabanlı **RGB ve termal görüntülerin** birlikte kullanımını incelemek
- Çatı üzerindeki ısı köprülerinin otomatik tespiti için:
  - veri ön işleme,
  - anotasyonların modele uygun hale getirilmesi,
  - analiz / modelleme adımlarını gerçekleştirmek
- Enerji verimliliği, bina denetimi ve kentsel analiz alanlarına katkı sağlayacak bir yaklaşım geliştirmektir

Bu çalışma, mevcut bir veri setinin **yeniden kullanımı ve etkin değerlendirilmesine** odaklanmaktadır.

---

## Kullanılan Veri Seti

**Thermal Bridges on Building Rooftops (TBBR) Dataset**  
🔗 https://zenodo.org/records/4767772

Veri seti, bina çatıları üzerindeki ısı köprülerini içeren **RGB ve termal drone görüntülerinden** oluşmaktadır. Tüm veri seti ve anotasyonlar özgün çalışmanın yazarları tarafından hazırlanmıştır.

### Veri Setinin Genel Özellikleri

- **Toplam görüntü:** 917
- **Toplam anotasyon:** 6895
- **Görüntü türleri:**
  - RGB görüntüler
  - Termal (FLIR-XT2) görüntüler
  - Yükseklik haritası (height map)
- **Görüntü boyutları:**
  - Orijinal: 3000x4000 piksel
  - İşlenmiş: 2400x3400 piksel
- **Anotasyon türü:**  
  - Polygon tabanlı ısı köprüsü anotasyonları

### Görüntülerin Toplanma Koşulları (Özet)

- **Drone:** DJI M600  
- **Lokasyon:** Karlsruhe, Almanya  
- **Tarih:** 19 Mart 2019 (07:00 – 08:00)
- **Çevresel koşullar:**  
  - Sıcaklık: 3.78 °C – 4.97 °C  
  - Nem: %80 – %98  
  - Doğrudan güneş ışığı yok

Bu bilgiler, veri setinin bağlamını açıklamak amacıyla özetlenmiştir. Detaylı teknik bilgiler için veri setinin resmi sayfasına başvurulmalıdır.

---

## Bu Projede Yapılan Çalışmalar

Bu repository kapsamında:

- Veri seti yapısının incelenmesi
- RGB ve termal görüntüler için:
  - ön işleme (normalizasyon, yeniden boyutlandırma vb.)
  - anotasyon formatlarının dönüştürülmesi
- Model eğitimi / analiz süreci
- Sonuçların değerlendirilmesi ve yorumlanması

gerçekleştirilmiştir.


---

## Repository Yapısı

```text
.
├── data/               # Veri setine ait yerel referanslar (repo içinde yer almaz)
├── preprocessing/      # Veri ön işleme adımları
├── notebooks/          # Deneyler ve analizler
├── models/             # Eğitilmiş modeller / konfigürasyonlar
├── results/            # Çıktılar ve değerlendirme sonuçları
└── README.md
