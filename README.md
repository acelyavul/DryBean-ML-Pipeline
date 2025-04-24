# Dry Bean Dataset – Machine Learning Pipeline

Bu proje, UCI Dry Bean veri kümesi üzerinde uçtan uca bir makine öğrenmesi süreci uygulamaktadır. Veri ön işleme, özellik çıkarımı (PCA ve LDA), çoklu sınıflandırma modelleri ve nested cross-validation gibi önemli adımlar içermektedir.

---

## İçerik

- **Veri Seti:** [Dry Bean Dataset (UCI)](https://archive.ics.uci.edu/ml/datasets/Dry+Bean+Dataset)
- **Aşamalar:**
  - Eksik veri ekleme ve temizleme
  - Aykırı değer analizi (IQR yöntemi)
  - Özellik ölçekleme (StandardScaler)
  - Kategorik verilerin kodlanması (LabelEncoder)
  - PCA ve LDA ile boyut indirgeme
  - Nested Cross-Validation (inner: 3-fold, outer: 5-fold)
  - 5 farklı sınıflandırma modeli
  - ROC analizleri ve metrik karşılaştırmaları

---

## Kullanılan Modeller

- Logistic Regression  
- Decision Tree  
- Random Forest  
- XGBoost  
- Naive Bayes  

---

## Performans Metrikleri

Her model için aşağıdaki metrikler hesaplandı:

- Accuracy  
- Precision (macro average)  
- Recall (macro average)  
- F1 Score (macro average)  
- ROC-AUC (her sınıf için, OVA yöntemiyle)

---

## Veri Temsilleri

| Veri Kümesi     | Açıklama                                   |
|------------------|---------------------------------------------|
| `processed_df`   | Preprocessing sonrası ham veri             |
| `pca_df`         | PCA ile boyut indirgenmiş veri             |
| `lda_df`         | LDA ile sınıf ayrımı maksimize edilmiş veri |

---

## Gereksinimler

```bash
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
```

📝 Tüm işlemler `DryBean_ML_Pipeline.ipynb` notebook dosyasında açıklamalı şekilde sunulmuştur.
