# Analisis Perbandingan CNN from Scratch dan Transfer Learning Menggunakan MobileNetV2 untuk Klasifikasi Citra

**Proyek Individu - Tugas Pembelajaran Mesin 2**

**Nama Mahasiswa :** Bulgatine Agnia
**NIM              :** *(452024618080)*
**Mata Kuliah      :** Pembelajaran Mesin 2
**Dosen Pengampu   :** Assoc. Prof. Dr. Ir. Oddy Virgantara Putra, S.Kom., M.T., IPP.
**Universitas      :** Universitas Darussalam Gontor

---

# 1. Deskripsi Proyek

Proyek ini bertujuan untuk membandingkan performa dua pendekatan **Deep Learning** dalam menyelesaikan tugas klasifikasi citra, yaitu **CNN from Scratch** dan **Transfer Learning**. Kedua metode diimplementasikan menggunakan TensorFlow dan Keras, kemudian dievaluasi berdasarkan nilai accuracy, loss, serta kemampuan model dalam melakukan klasifikasi citra.

Eksperimen yang dilakukan terdiri atas:

* **Eksperimen 1 (CNN from Scratch)**
  Membangun model Convolutional Neural Network (CNN) dari awal tanpa menggunakan pretrained model. Dataset yang digunakan adalah **CIFAR-10** dengan dua kelas yang dipilih untuk proses klasifikasi citra.

* **Eksperimen 2 (Transfer Learning)**
  Mengimplementasikan metode Transfer Learning menggunakan **MobileNetV2** sebagai pretrained model. Strategi yang digunakan adalah **Feature Extraction**, yaitu membekukan seluruh layer pada model dasar dan hanya melatih classifier baru.

---

# 2. Tujuan Proyek

Tujuan dari proyek ini adalah:

* Mengimplementasikan CNN from Scratch untuk klasifikasi citra.
* Mengimplementasikan Transfer Learning menggunakan MobileNetV2.
* Membandingkan performa kedua model berdasarkan hasil eksperimen.
* Menganalisis kelebihan dan kekurangan masing-masing pendekatan.
* Menentukan metode yang lebih sesuai berdasarkan ukuran dataset, kebutuhan komputasi, dan tingkat akurasi.

---

# 3. Dataset

### CNN from Scratch

* Dataset : **CIFAR-10**
* Jumlah kelas : 2
* Resolusi gambar : **32 × 32 piksel**
* Format warna : RGB

### Transfer Learning

* Pretrained Model : **MobileNetV2**
* Framework : TensorFlow / Keras
* Strategi : Feature Extraction

---

# 4. Arsitektur Model

## CNN from Scratch

Model CNN terdiri atas beberapa layer utama, yaitu:

* Convolution Layer
* Batch Normalization
* Max Pooling Layer
* Flatten Layer
* Dense Layer
* Dropout Layer
* Output Layer

Optimizer yang digunakan adalah **Adam** dengan fungsi loss yang disesuaikan untuk proses klasifikasi.

## Transfer Learning

Model Transfer Learning menggunakan:

* MobileNetV2 (Pretrained ImageNet)
* Global Average Pooling
* Dense Layer
* Dropout
* Output Layer

Seluruh layer MobileNetV2 dibekukan (freeze), kemudian hanya classifier yang dilatih selama proses training.

---

# 5. Hasil Eksperimen

| Metrik              | CNN from Scratch | Transfer Learning |
| ------------------- | ---------------: | ----------------: |
| Training Accuracy   |       **84.66%** |        **54.55%** |
| Validation Accuracy |       **76.30%** |        **55.10%** |
| Training Loss       |       **0.3488** |        **0.6835** |
| Validation Loss     |       **0.4899** |        **0.6814** |

Berdasarkan hasil eksperimen, model **CNN from Scratch** memberikan performa yang lebih baik dibandingkan Transfer Learning pada konfigurasi yang digunakan dalam penelitian ini.

---

# 6. Struktur Repository GitHub

```text
project-cnn-vs-transfer-learning/
├── dataset/
│   └── link_dataset.txt
├── notebook/
│   └── cnn_vs_transfer_learning.ipynb
├── report/
│   └── laporan.pdf
├── README.md
└── requirements.txt
```

---

# 7. Software dan Library

Proyek ini dikembangkan menggunakan:

* Python 3.x
* Google Colab
* TensorFlow
* Keras
* NumPy
* Matplotlib
* Scikit-learn

---

# 8. Cara Menjalankan Project

1. Clone repository GitHub.
2. Install seluruh library yang terdapat pada `requirements.txt`.
3. Buka file `cnn_vs_transfer_learning.ipynb` menggunakan Google Colab atau Jupyter Notebook.
4. Jalankan seluruh sel secara berurutan.
5. Model akan melakukan proses training dan menghasilkan grafik accuracy, loss, serta evaluasi model.

---

# 9. Kesimpulan

Hasil penelitian menunjukkan bahwa pada eksperimen yang dilakukan, **CNN from Scratch** memperoleh performa yang lebih baik dibandingkan Transfer Learning. CNN menghasilkan nilai training accuracy sebesar **84.66%** dan validation accuracy sebesar **76.30%**, sedangkan Transfer Learning memperoleh training accuracy sebesar **54.55%** dan validation accuracy sebesar **55.10%**.

Pemilihan metode deep learning sebaiknya disesuaikan dengan karakteristik dataset, kebutuhan komputasi, waktu pelatihan, serta tujuan implementasi pada aplikasi nyata.

---

# 10. Referensi

1. Goodfellow, I., Bengio, Y., & Courville, A. (2016). *Deep Learning*. MIT Press.
2. Chollet, F. (2021). *Deep Learning with Python*. Manning Publications.
3. TensorFlow Documentation. https://www.tensorflow.org/
4. Keras Documentation. https://keras.io/
5. CIFAR-10 Dataset. https://www.cs.toronto.edu/~kriz/cifar.html
6. MobileNetV2 Paper. https://arxiv.org/abs/1801.04381

