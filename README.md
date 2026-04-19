# COVID-19 Hasta Tahmini – Makine Öğrenmesi Projesi

Bu proje, gerçek bir COVID-19 veri seti kullanarak, bir kişinin demografik bilgilerine ve sağlık geçmişine dayanarak hasta olup olmadığını tahmin eden bir makine öğrenmesi modelidir. Proje kapsamında veri analizi, temizleme ve modelleme süreçleri uçtan uca uygulanmıştır.

## 📊 1. Veri Seti Tanıtımı
- **Veri Seti Kaynağı:** [Kaggle - COVID-19 Patient Precondition Dataset](https://www.kaggle.com/datasets/tanmoyx/covid19-patient-precondition-dataset)
- **Açıklama:** Meksika hükümeti tarafından paylaşılan bu veri seti, hastaların temel sağlık bilgilerini ve COVID-19 sonuçlarını içermektedir.

## 🛠️ 2. Veri Ön İşleme (Data Preprocessing) & EDA
- **Eksik Veriler:** Veri setinde "bilinmiyor" anlamına gelen **97, 98 ve 99** değerleri temizlenerek veri setinden çıkarılmıştır.
- **Hedef Değişken (Target):** `CLASIFFICATION_FINAL` sütunu üzerinden hastalar "Pozitif (1)" ve "Negatif (0)" olarak iki sınıfa ayrılmıştır.
- **Veri Temizliği:** Tahmin başarısını etkileyebilecek `id`, `patient_type` ve `covid_res` gibi sızıntı (leakage) yaratabilecek sütunlar kaldırılmıştır.
- **Eğitim ve Test:** Veri seti **%80 eğitim** ve **%20 test** olacak şekilde bölünmüştür.

## 🤖 3. Kullanılan Algoritmalar
Ödev gereksinimleri doğrultusunda iki farklı makine öğrenmesi algoritması kullanılmıştır:
- **Logistic Regression:** Sınıflandırma problemleri için temel bir istatistiksel model.
- **Random Forest:** Karar ağaçları tabanlı, yüksek doğruluk oranına sahip güçlü bir topluluk öğrenme algoritması.

## 📈 4. Model Performans Sonuçları
Elde edilen sonuçlara göre modellerin başarısı şu şekildedir:

| Algoritma | Doğruluk (Accuracy) |
| :--- | :--- |
| Logistic Regression | %91 |
| Random Forest | %94 |

## 🧪 5. Değerlendirme ve Sonuç
- **Random Forest** modeli, verilerdeki karmaşık ilişkileri daha iyi analiz ederek en yüksek başarıyı göstermiştir.
- **Confusion Matrix** sonuçları, modelin her iki sınıfta da dengeli ve güvenilir tahminler yaptığını göstermektedir.
- **Precision ve Recall** değerleri, projenin gerçek dünya verilerinde uygulanabilir olduğunu kanıtlamaktadır.

## 🚀 6. Projeyi Çalıştırma
1. Repodaki `covid19_hasta_tahmini.ipynb` dosyasını indirin.
2. [Google Colab](https://colab.research.google.com/) üzerinde açın ve Kaggle'dan indirilen `covid.csv` dosyasını sisteme yükleyin.
3. Tüm hücreleri sırayla çalıştırarak sonuçları gözlemleyin.
