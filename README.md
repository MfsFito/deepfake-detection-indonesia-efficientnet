# deepfake-detection-indonesia-efficientnet
Evaluasi generalisasi EfficientNet-B4 dari dataset global DFDC ke video deepfake politik Indonesia — GEMASTIK XIX 2026

# Deteksi Deepfake Video Tokoh Politik Indonesia Menggunakan EfficientNet

Repository ini berisi kode eksperimen untuk penelitian **"Deteksi Deepfake Video 
Tokoh Politik Indonesia Menggunakan EfficientNet: Evaluasi Generalisasi dari 
Dataset Global ke Konteks Lokal"** — GEMASTIK XIX 2026, Cabang Karya Tulis Ilmiah.

## Ringkasan
Penelitian ini mengevaluasi apakah model EfficientNet-B4 yang dilatih pada 
dataset global (DFDC) tetap akurat ketika diuji pada video deepfake tokoh 
politik Indonesia.

## Struktur Repository
- `01_training_dfdc.ipynb` — Training EfficientNet-B4 pada dataset DFDC
- `02_evaluasi_lokal_indonesia.ipynb` — Evaluasi generalisasi pada dataset uji 
  lokal Indonesia

## Dataset
- **Training:** Wajah hasil ekstraksi dari *train sample* DFDC, bersumber dari 
  dataset publik [dfdc-faces-of-the-train-sample](https://www.kaggle.com/datasets/itamargr/dfdc-faces-of-the-train-sample) 
  oleh Itamar Gilad di Kaggle — merupakan mirror dari data resmi 
  [DeepFake Detection Challenge](https://www.kaggle.com/c/deepfake-detection-challenge), 
  diekstraksi menggunakan MTCNN (`facenet-pytorch`) dengan metodologi yang identik 
  dengan yang digunakan pada penelitian ini.
- **Uji lokal:** Dikurasi mandiri dari kasus deepfake politik Indonesia 
  terverifikasi oleh Mafindo dan cekfakta.com.

## Requirements
torch, torchvision, timm, facenet-pytorch, opencv-python,
scikit-learn, matplotlib, seaborn

## Hasil Utama
| Skenario                       | Akurasi | F1-Score |
| Intra-dataset (DFDC)           | 86,57%  | 91,37%   |
| Generalisasi (Lokal Indonesia) | 37,56%  | 53,91%   |


