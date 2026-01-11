# Imbalanced Classification Analysis on Heart Disease Dataset
# Analisis Klasifikasi Data Imbalanced pada Dataset Penyakit Jantung

>>>

## Overview (English)
This project is an applied statistical analysis of classification problems initially assumed to be imbalanced data, using the UCI Heart Disease dataset. It compares Binary Logistic Regression and Random Forest models with various imbalanced data handling techniques to evaluate their impact on model performance, particularly in detecting medical risks.

The analysis focuses on the recall and F1-score metrics due to the importance of minimizing false negatives in clinical decision-making.

## Gambaran Umum (Bahasa Indonesia)
Proyek ini merupakan analisis statistika terapan pada permasalahan klasifikasi yang awalnya diasumsikan sebagai data imbalanced, menggunakan dataset penyakit jantung dari UCI Heart Disease. ini membandingkan model Regresi Logistik Biner dan Random Forest dengan berbagai teknik penanganan data imbalanced untuk mengevaluasi pengaruhnya terhadap kinerja model, khususnya dalam mendeteksi risiko medis.

Analisis difokuskan pada metrik recall dan F1-score karena pentingnya meminimalkan kesalahan negatif palsu dalam pengambilan keputusan klinis.

>>>
## Dataset Source

**English**  
The dataset used in this project is publicly available on Kaggle and can
be accessed via the following link:
[https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data]

Please note that the dataset is not included in this repository in
accordance with Kaggle’s data usage policy.

**Bahasa Indonesia**  
Dataset yang digunakan dalam proyek ini tersedia secara publik di Kaggle
dan dapat diakses melalui tautan berikut:
[https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data]

Dataset tidak disertakan langsung dalam repository ini sesuai dengan
kebijakan penggunaan data Kaggle.

>>>
## Dataset

**English**
- Source: UCI Heart Disease Dataset (Cleveland subset, Kaggle mirror)
- Total observations: 920 records
- Target variable:
  - `num` (0 = no heart disease, 1 = heart disease)
- Selected features:
  - `sex`, `cp`, `trestbps`, `fbs`
- Variables with excessive missing values were excluded to maintain data
  reliability.

**Bahasa Indonesia**
- Sumber: Dataset Penyakit Jantung UCI (subset Cleveland)
- Jumlah observasi: 920 data
- Variabel target:
  - `num` (0 = tidak ada penyakit jantung, 1 = terdapat penyakit jantung)
- Fitur yang digunakan:
  - `sex`, `cp`, `trestbps`, `fbs`
- Variabel dengan nilai hilang berlebih dieliminasi untuk menjaga keakuratan data.

>>>

## Methodology | Metodologi

1. **Data Preprocessing / Pra-pemrosesan Data**
   - Binarisasi variabel target
   - Imputasi data hilang (median, KNN, dan modus)
   - Standardisasi data numerik
   - One-Hot Encoding untuk variabel kategorikal
   - Outlier dipertahankan karena relevansi klinis

2. **Train-Test Split**
   - 80% data latih, 20% data uji
   - Stratified split

3. **Handling Class Imbalance / Penanganan Data Imbalanced**
   - Oversampling
   - Undersampling
   - SMOTE
   - SMOTEENN (diterapkan hanya pada data latih untuk menghindari data leakage)

4. **Modeling / Pemodelan**
   - Binary Logistic Regression
   - Random Forest

5. **Evaluation Metrics / Metrik Evaluasi**
   - Accuracy
   - Precision
   - Recall
   - F1-score
   - Confusion Matrix
   - ROC Curve & AUC

>>>

## Results | Hasil Analisis

**English**
- Logistic Regression showed more stable performance compared to Random Forest given the limited feature set.
- Resampling techniques significantly affected recall and F1-score.
- SMOTE and SMOTEENN improved minority class detection.
- Logistic Regression with SMOTEENN provided the most balanced performance (ROC-AUC ≈ 0.87).

**Bahasa Indonesia**
- Regresi Logistik menunjukkan performa yang lebih stabil dibandingkan Random Forest dengan jumlah fitur yang terbatas.
- Teknik resampling berpengaruh signifikan terhadap nilai recall dan F1-score.
- SMOTE dan SMOTEENN meningkatkan kemampuan model dalam mendeteksi kelas minoritas.
- Kombinasi Regresi Logistik dan SMOTEENN memberikan performa paling seimbang (ROC-AUC ≈ 0.87).

>>>

## Key Takeaways | Kesimpulan Utama
- Accuracy tidak cukup untuk mengevaluasi data imbalanced
- Recall merupakan metrik paling krusial dalam prediksi penyakit
- Data yang tidak terlalu imbalanced tetap perlu dianalisis secara kritis
- Model sederhana dapat unggul jika dipadukan dengan analisis yang tepat

>>>

## Tools & Libraries
- Python
- Pandas, NumPy
- Scikit-learn
- imbalanced-learn
- Matplotlib, Seaborn

>>>

## Author
Kadek Savita Dyutianaya  
Applied Data Science Student  
Politeknik Elektronika Negeri Surabaya

