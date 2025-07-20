# 📈 Microsoft Hisse Senedi Fiyat Tahmini / Microsoft Stock Price Prediction

Bu projede, **Microsoft (MSFT)** hisse senedi verileri kullanılarak çeşitli makine öğrenmesi algoritmaları ile kapanış fiyatlarının tahmini yapılmıştır.  
In this project, **Microsoft (MSFT)** stock data is used to predict closing prices using various machine learning algorithms.

---

## 📊 Veri Seti / Dataset

- **Kaynak / Source:** Kaggle - [Microsoft Stock Price History](https://www.kaggle.com/datasets)
- **Zaman Aralığı / Date Range:** 1986 - 2023
- **Sütunlar / Columns:** Date, Open, High, Low, Close, Volume

---

## ⚙️ Özellik Mühendisliği / Feature Engineering

- Tarih verisinden çıkarılanlar / Extracted from `Date`:
  - `Year`, `Month`, `Day`, `DayOfWeek`
- Teknik göstergeler / Technical indicators:
  - 20-günlük ve 50-günlük hareketli ortalama / 20-day and 50-day moving averages: `MA20`, `MA50`
  - Günlük getiriler / Daily returns: `Daily_Return`
  - 10-günlük volatilite / 10-day volatility: `Volatility_10`

---

## 🤖 Kullanılan Modeller / Models Used

Aşağıdaki makine öğrenmesi algoritmaları uygulanmıştır:  
The following machine learning models were used:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Support Vector Regressor (SVR)
- K-Nearest Neighbors (KNN)

---

## 📈 Performans Sonuçları / Performance Results

| Model                    | R² Skoru / R² Score | MSE (Hata) / MSE (Error) |
|--------------------------|----------------------|---------------------------|
| Linear Regression        | 0.9999               | 0.55                      |
| Decision Tree Regressor | 0.9998               | 2.28                      |
| Random Forest Regressor | 0.9999               | 1.07                      |
| SVR                      | 0.9077               | 1099.40                   |
| KNN                      | 0.9969               | 37.03                     |

> 📌 **Not / Note:** Linear Regression ve Random Forest modelleri yüksek başarı göstermiştir.  
> Linear Regression and Random Forest models have shown high accuracy.

---

## 📊 Görselleştirme / Visualization

Her modelin tahmin ve gerçek kapanış fiyatları çizdirilmiştir.  
Each model's predicted vs actual closing prices are plotted for comparison.

![Model Prediction Graph](C:\Users\cam2\Desktop\Veri Datalaro\Microsoft Stock Price Prediction Using Machine Learning\DecisionTree.png)
![Model Prediction Graph](C:\Users\cam2\Desktop\Veri Datalaro\Microsoft Stock Price Prediction Using Machine Learning\KNN.png)
![Model Prediction Graph](images/knn_vs_actual.png)
![Model Prediction Graph](images/knn_vs_actual.png)
![Model Prediction Graph](images/knn_vs_actual.png)
---

## 🚀 Nasıl Çalıştırılır? / How to Run?

Gerekli kütüphaneleri yükleyin / Install required libraries:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
