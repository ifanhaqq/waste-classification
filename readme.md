# Waste Classification System

Sistem klasifikasi gambar sampah untuk membedakan sampah **Organik** dan **Anorganik** menggunakan metode **Histogram of Oriented Gradients (HOG)** dan **Support Vector Machine (SVM)**.

## Requirements

Pastikan Python dan Jupyter Notebook sudah terinstall.

Library yang digunakan:

- numpy
- pandas
- matplotlib
- scikit-learn
- opencv-python
- scikit-image
- joblib
- jupyter

## Clone Repository

Clone repository ke komputer lokal:

```bash
git clone https://github.com/ifanhaqq/waste-classification
cd waste-classification
```

## Install Dependencies

Install seluruh library yang dibutuhkan:

```bash
pip install numpy pandas matplotlib scikit-learn opencv-python scikit-image joblib jupyter
```

## Menyiapkan Dataset

Letakkan dataset pada folder `dataset` dengan struktur sebagai berikut:

```text
dataset/
├── organic/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
│
└── inorganic/
    ├── image1.jpg
    ├── image2.jpg
    └── ...
```

Pastikan:

- Folder `organic` hanya berisi gambar sampah organik.
- Folder `inorganic` hanya berisi gambar sampah anorganik.
- Format gambar yang digunakan adalah JPG, JPEG, atau PNG.

## Menjalankan Jupyter Notebook

Buka terminal pada folder project kemudian jalankan:

```bash
jupyter notebook
```

atau

```bash
jupyter lab
```

Setelah browser terbuka, buka file:

```text
waste_classification.ipynb
```

## Training Model

Jalankan seluruh cell notebook secara berurutan.

Tahapan yang dilakukan notebook:

1. Memuat dataset.
2. Melakukan preprocessing gambar.
3. Melakukan ekstraksi fitur menggunakan HOG.
4. Membagi dataset menjadi data training dan testing.
5. Melatih model SVM.
6. Melakukan evaluasi model.
7. Menyimpan model hasil training.

## Evaluasi Model

Notebook akan menampilkan beberapa metrik evaluasi:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

Contoh output:

```text
Accuracy : 85.00%
Precision: 84.00%
Recall   : 86.00%
F1 Score : 85.00%
```

## Menjalankan Prediksi

Pada bagian akhir notebook tersedia cell untuk melakukan prediksi gambar baru.

Ubah path gambar pada variabel berikut:

```python
image_path = "test_images/sample.jpg"
```

Kemudian jalankan cell prediksi.

Contoh output:

```text
Prediction : Organic
```
