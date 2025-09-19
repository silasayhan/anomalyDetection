# Anomaly Detection on Equipment Sensor Data  

Bu proje, **equipment_anomaly_data.csv** veri seti kullanılarak endüstriyel ekipmanlarda arıza olasılığının tespit edilmesini amaçlamaktadır. Çalışmada makine öğrenmesi yöntemleriyle **anomali tespiti** ve **binary classification** (arızalı / arızasız) problemleri ele alınmıştır.  

---

## Proje Yapısı
```
anomalyDetection/
│── binaryClassification.ipynb # İlk Model Denemesi (Random Forest Classifier)
│── binaryClassification_V2.ipynb # Recall Odaklı Geliştirme (SMOTE + Hyperparameter Tuning)
│── equipment_anomaly_data.csv # Veri Seti
│── README.md # Proje Açıklamaları
```

---

## Çalışmanın Adımları  

1. **Veri Analizi (EDA):**  
   - Sıcaklık, basınç, titreşim, nem gibi sensör verileri incelenmiştir.  
   - Eksik veriler ve dağılımlar analiz edilmiştir.  

2. **Modelleme (binaryClassification.jpyn):**  
   - Random Forest Classifier uygulanmıştır.  

3. **Model İyileştirme (binaryClassification_V2.ipynb):**  
   - **Recall Değerini Artırmak** için sınıf dengesizliği problemi ele alınmıştır.  
   - **SMOTE (Synthetic Minority Oversampling Technique)** uygulanmıştır.  
   - **Hiperparametre Optimizasyonu** ile model performansı artırılmıştır.  

---

## Kullanılan Veri Seti  

**equipment_anomaly_data.csv** dosyası şu sensör özelliklerini içermektedir:  
- `temperature` → Sıcaklık Ölçümü  
- `pressure` → Basınç Ölçümü  
- `vibration` → Titreşim Verisi  
- `humidity` → Nem Oranı  
- `equipment` → Ekipman Türü
- `location` → Ölçümün Yapıldığı Lokasyon  
- `faulty` → Hedef Değişken (0: Normal, 1: Arızalı)  

---

## Kullanılan Teknolojiler  

- **Python 3**  
- **Pandas, Numpy** → Veri İşleme  
- **Scikit-learn** → Modelleme ve SMOTE  
- **Matplotlib, Seaborn** → Görselleştirme  

---

## Sonuçlar

İlk modelde Random Forest ile temel doğruluk sağlanmıştır.

İkinci versiyonda, Recall metriği geliştirilmiş ve dengesiz veri seti üzerinde daha başarılı bir sınıflandırma elde edilmiştir.


