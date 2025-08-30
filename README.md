# Bank Term Deposit Prediction (Kaggle Playground S5E8)

Bu proje, **Kaggle Playground Series - Season 5, Episode 8** yarışması için hazırlanmıştır.  
Amaç: Bir müşterinin banka vadeli mevduatına abone olup olmayacağını tahmin etmek.  
Modelleme sürecinde **LightGBM** kullanılarak **%97.58 AUC** başarı elde edilmiştir. 🚀  


## 🚀 Sonuçlar
- Model: **LightGBM**
- Cross-Validation AUC: **0.9758**
- Kaggle Yarışma Linki: [Playground Series S5E8](https://www.kaggle.com/competitions/playground-series-s5e8/overview)

## 🔧 Kullanılan Kütüphaneler
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `lightgbm`

## 📊 Özellikler ve İşlemler
- Eksik/rare kategorilerin gruplandırılması (`job`, `month`, `education`, `contact`)  
- Negatif bakiyelerin düzeltilmesi ve log dönüşümü (`balance`, `duration`)  
- Aykırı değerlerin IQR yöntemi ile sınırlandırılması (`campaign`, `duration`)  
- Özellik mühendisliği:  
  - `balance_log1p`, `duration_log1p`, `campaign_log1p` gibi log dönüşümler  
  - `pdays_is_minus1` flag’i  
  - `is_long_duration` flag’i  

## 📌 Notlar
- Stratified K-Fold (8 fold) kullanıldı.  
- Erken durdurma (early stopping) ile aşırı öğrenme engellendi.  
- Final model %97.58 AUC ile yüksek doğruluk sağlamıştır.  

---

