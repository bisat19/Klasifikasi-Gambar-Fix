# Tomato Leaf Disease Classification Project

## Penjelasan Projek
Proyek ini merupakan proyek untuk membuat sebuah model yang dapat melakukan klasifikasi gambar. Diberikan kebebasan untuk memilih dataset yang ingin digunakan.

### 🗃️ Dataset

Dataset diambil dari Kaggle dengan topik Tomato Diseases Dataset (CSV+Images) oleh Ammar Alhaj Ali (2021) : https://www.kaggle.com/datasets/ammarnassanalhajali/tomato-diseases-dataset-csvimages yang terdiri 18160 images dari 10 kategori dengan distribusi sebagai berikut:

| Disease Class                          | Number of Images | Percentage  |
|----------------------------------------|-----------------:|------------:|
| Tomato_Yellow_Leaf_Curl_Virus          |            5,357 |      31.21% |
| Bacterial_spot                         |            2,127 |      12.39% |
| Late_blight                            |            1,909 |      11.12% |
| Septoria_leaf_spot                     |            1,771 |      10.32% |
| Spider_mites_Two-spotted_spider_mite   |            1,676 |       9.77% |
| healthy                                |            1,591 |       9.27% |
| Target_Spot                            |            1,404 |       8.18% |
| Early_blight                           |            1,000 |       5.83% |
| Leaf_Mold                              |              952 |       5.55% |
| Tomato_mosaic_virus                    |              373 |       2.17% |
| **Total**                              |        **18,160**|    **100%** |

### 🖼️ Preview Image 

Berikut merupakan contoh dari data-data gambar yang digunakan
![Preview Gambar](https://github.com/bisat19/Klasifikasi-Gambar-Fix/blob/main/images/download.png)

### 🤖 Model

Secara garis besar model dibentuk dari Deep Convolutional Neural Network dengan 4 blok konvolusi dan 2 lapisan fully connected untuk klasifikasi 10 penyakit daun tomat:

### 🧠 Model Architecture Summary

| Layer (Type)               | Output Shape      | Parameters  |
|----------------------------|-------------------|-------------|
| **Input**                  | (256, 256, 3)     | 0           |
| **Conv2D (32 filters)**    | (254, 254, 32)    | 896         |
| **BatchNormalization**     | (254, 254, 32)    | 128         |
| **MaxPooling2D**           | (127, 127, 32)    | 0           |
| **Dropout (20%)**          | (127, 127, 32)    | 0           |
| **Conv2D (64 filters)**    | (125, 125, 64)    | 18,496      |
| **...**                    | ...               | ...         |
| **Output (10 units)**      | (10)              | 5,130       |

**Total Parameters**: 26,088,138  
**Trainable**: 26,086,154  
**Non-trainable**: 1,984  

### 📊 Evaluasi Model

Berikut merupakan evaluasi model yang dibentuk
![Hasil Evaluasi](https://github.com/bisat19/Klasifikasi-Gambar-Fix/blob/main/images/download%20(1).png)

### Prediksi

Berikut merupakan hasil prediksi dengan menggunakan model yang dibentuk
![Hasil Prediksi](https://github.com/bisat19/Klasifikasi-Gambar-Fix/blob/main/images/download%20(2).png)
