# 🧠 Intel Image Classification with CNN

Bu proje, **Intel Image Classification Dataset** kullanılarak farklı görüntü kategorilerini (binalar, ormanlar, buzullar, dağlar, denizler, caddeler) sınıflandırmak için bir **Evreşimsel Sinir Ağı (CNN)** modeli geliştirmeyi amaçlamaktadır.  

## 📂 Veri Seti
- **Kaynak:** [Intel Image Classification Dataset (Kaggle)](https://www.kaggle.com/datasets/puneet6060/intel-image-classification)  
- Veri seti üç klasörden oluşmaktadır:  
  - `seg_train` → Eğitim verileri  
  - `seg_test` → Test verileri  
  - `seg_pred` → (isteğe bağlı tahmin için kullanılabilir)  

- **Sınıflar (6 kategori):**
  - Buildings (Binalar)  
  - Forest (Orman)  
  - Glacier (Buzul)  
  - Mountain (Dağ)  
  - Sea (Deniz)  
  - Street (Cadde)  

---

## ⚙️ Kullanılan Teknolojiler
- **Python 3.x**  
- **TensorFlow / Keras** (CNN modeli ve eğitim için)  
- **NumPy, Pandas** (veri işlemleri için)  
- **Matplotlib, Seaborn** (grafikler için)  
- **Scikit-learn** (train/validation/test bölme için)  

---

## 🏗️ Model Mimarisi
Model **Keras Sequential API** ile oluşturulmuş olup aşağıdaki katmanlardan oluşmaktadır:  

1. **Conv2D + BatchNorm + MaxPooling** (32 filtre)  
2. **Conv2D + BatchNorm + MaxPooling** (64 filtre)  
3. **Conv2D + BatchNorm + MaxPooling** (128 filtre)  
4. **Conv2D + BatchNorm + MaxPooling** (256 filtre)  
5. **Flatten + Dense(512, ReLU) + Dropout(0.5)**  
6. **Dense(num_classes, Softmax)**  

**Optimizasyon:** Adam (lr=0.0001)  
**Loss fonksiyonu:** Categorical Crossentropy  
**Metric:** Accuracy  

---

## 🚀 Eğitim Süreci
- **Epoch sayısı:** 40  
- **Batch size:** 64  
- **Data Augmentation:**  
  - Döndürme (rotation)  
  - Kaydırma (shift)  
  - Zoom  
  - Yatay çevirme (horizontal flip)  

---

## 🔍 Test Sonuçları
Model test veri setinde şu performansı göstermiştir:  

- **Test Doğruluk (Accuracy):** `82.5%`  
- **Test Loss:** ≈ 0.5  

---

## 🖼️ Örnek Tahminler
Modelin rastgele seçilen test görselleri üzerindeki tahminleri:  

---

## 📌 Kullanım & Kod Görüntüleme

Bu projeyi çalıştırmak için:  
1. Gerekli kütüphaneleri yükle (örn. `pip install -r requirements.txt`)  
2. `notebook.ipynb` dosyasını açıp hücreleri sırayla çalıştır  

Ayrıca, Kaggle üzerinde projenin orijinal notebook versiyonunu inceleyebilirsin:  
[Notebook’u Kaggle’da Görüntüle](https://www.kaggle.com/code/beyzanurakar/notebookbf4c787a91)  

---
