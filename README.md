# Pengembangan Machine Learning

📂 Sumber Dataset [Kaggle]: Intel Image Classification (puneet6060/intel-image-classification)
Deskripsi: Dataset berisi gambar lingkungan dengan enam kategori berbeda, digunakan untuk klasifikasi gambar berbasis Convolutional Neural Networks (CNN).

Jumlah Kelas:
- Buildings
- Forest
- Glacier
- Mountain
- Sea
- Street

🛠️ Splitting Dataset
Setelah penggabungan dan verifikasi data, dataset dibagi menggunakan rasio:
| Dataset Split | Persentase | Keterangan        |
|---------------|------------|-------------------|
| Training      | 64%        | Data untuk training model |
| Validation    | 16%        | Data untuk validasi saat training |
| Testing       | 20%        | Data untuk evaluasi akhir |

🖥️ Model CNN
| Layer (Type)             | Output Shape         | Param #    |
|--------------------------|----------------------|------------|
| conv2d_4 (Conv2D)        | (None, 128, 128, 64) | 1,792      |
| batch_normalization_4    | (None, 128, 128, 64) | 256        |
| max_pooling2d_4          | (None, 64, 64, 64)   | 0          |
| conv2d_5 (Conv2D)        | (None, 64, 64, 64)   | 36,928     |
| batch_normalization_5    | (None, 64, 64, 64)   | 256        |
| max_pooling2d_5          | (None, 32, 32, 64)   | 0          |
| conv2d_6 (Conv2D)        | (None, 32, 32, 128)  | 131,200    |
| batch_normalization_6    | (None, 32, 32, 128)  | 512        |
| max_pooling2d_6          | (None, 16, 16, 128)  | 0          |
| conv2d_7 (Conv2D)        | (None, 16, 16, 256)  | 1,605,888  |
| batch_normalization_7    | (None, 16, 16, 256)  | 1,024      |
| max_pooling2d_7          | (None, 8, 8, 256)    | 0          |
| flatten_1 (Flatten)      | (None, 16384)        | 0          |
| dense_3 (Dense)          | (None, 128)          | 2,097,280  |
| dropout_2 (Dropout)      | (None, 128)          | 0          |
| dense_4 (Dense)          | (None, 64)           | 8,256      |
| dropout_3 (Dropout)      | (None, 64)           | 0          |
| dense_5 (Dense)          | (None, 6)            | 390        |

🎯 Akurasi
- Training Set: 95.53%
- Test Accuracy: 88.13%
