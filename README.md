# 🧠 Intel Image Classification with CNN
Bu proje, **Intel Image Classification** veri seti kullanılarak farklı görüntü kategorilerini (binalar, ormanlar, denizler vb.) sınıflandırmak için bir **Evreşimsel Sinir Ağı (CNN)** modeli geliştirmeyi amaçlamaktadır.  

## 📂 Veri Seti
- **Kaynak:** [Intel Image Classification Dataset](https://www.kaggle.com/datasets/puneet6060/intel-image-classification)  
- **Sınıflar (6 kategori):**
  - Binalar (Buildings)  
  - Ormanlar (Forest)  
  - Buzullar (Glacier)  
  - Dağlar (Mountain)  
  - Deniz (Sea)  
  - Caddeler (Street)  

Veri setinde **eğitim (train)**, **doğrulama (validation)** ve **test (test)** klasörleri bulunmaktadır.  

---

## ⚙️ Kullanılan Teknolojiler
- Python  
- TensorFlow / Keras  
- NumPy, Pandas  
- Matplotlib, Seaborn  
- Scikit-learn  

---

## 🚀 Model Eğitimi
- Model, bir **CNN (Convolutional Neural Network)** mimarisi üzerine kurulmuştur.  
- Eğitim sürecinde **veri artırma (data augmentation)** ve **erken durdurma (early stopping)** teknikleri uygulanmıştır.  
- **En yüksek doğruluk oranı:** `82.5%`  

📊 **Accuracy & Loss Grafikleri:**

![Accuracy](images/accuracy.png)  
![Loss](images/loss.png)  

---

## 🔍 Örnek Tahminler
Modelin test veri setinde yaptığı tahminlerden 9 örnek görsel:  

![Sample Predictions](images/sample_predictions.png)  

---

## 📌 Projeyi Çalıştırma

Projeyi kendi bilgisayarınızda çalıştırmak için:  

1. Bu repoyu klonlayın:  
   ```bash
   git clone https://github.com/kullaniciadi/intel-image-classification.git
   cd intel-image-classification
