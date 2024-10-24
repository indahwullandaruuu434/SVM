# Klasifikasi Iris Menggunakan SVM dengan Penyetelan Hyperparameter

Proyek ini menerapkan Support Vector Machine (SVM) untuk mengklasifikasikan dataset bunga Iris, termasuk penyetelan hyperparameter menggunakan GridSearchCV. Model SVM adalah alat yang kuat untuk tugas pembelajaran terawasi seperti klasifikasi, dan notebook ini menunjukkan cara penggunaannya secara efektif pada dataset yang terkenal.

## Dataset

Dataset yang digunakan dalam proyek ini adalah [dataset Iris] yang terdiri dari 150 sampel dari tiga spesies bunga Iris: *Iris setosa*, *Iris versicolor*, dan *Iris virginica*. Empat fitur diukur dari setiap sampel:
- Panjang sepal (cm)
- Lebar sepal (cm)
- Panjang petal (cm)
- Lebar petal (cm)

## Dependensi

Proyek ini menggunakan pustaka Python berikut:
- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`

Pastikan untuk menginstal pustaka yang diperlukan dengan menjalankan:

```bash
pip install -r requirements.txt
```

## Langkah-Langkah

1. **Pra-Pemrosesan Data**:
   - Memuat dataset ke dalam DataFrame Pandas.
   - Mengubah variabel target (spesies) menggunakan `LabelEncoder`.

2. **Pembagian Data**:
   - Membagi data menjadi set pelatihan dan set pengujian (70% latih, 30% uji) menggunakan `train_test_split`.

3. **Pelatihan Model**:
   - Melatih model SVM menggunakan kernel yang berbeda (poly, rbf, sigmoid) dan hyperparameter (`C` dan `gamma`).

4. **Penyetelan Hyperparameter**:
   - Menggunakan `GridSearchCV` untuk mencari hyperparameter optimal untuk model SVM. Pencarian dilakukan pada grid nilai untuk `C`, `gamma`, dan `kernel`.

5. **Evaluasi**:
   - Menampilkan skor terbaik dan hyperparameter yang optimal.
   - Mengevaluasi model menggunakan akurasi.

## Hasil

Setelah penyetelan model, kombinasi hyperparameter terbaik adalah:
- **Kernel**: rbf
- **C**: 10
- **Gamma**: 0.1

Akurasi model setelah penyetelan mencapai sekitar **98.1%**.

## Cara Menjalankan

1. Clone repositori dan navigasikan ke direktori proyek:

   ```bash
   git clone <tautan-repositori>
   cd <direktori-proyek>
   ```

2. Instal pustaka yang diperlukan:

   ```bash
   pip install -r requirements.txt
   ```

3. Jalankan Jupyter notebook:

   ```bash
   jupyter notebook SVM.ipynb
   ```

4. Ikuti langkah-langkah dalam notebook untuk melatih dan mengevaluasi model.

