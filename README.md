# 🌽 Klasifikasi Varietas Biji Jagung (Zea mays) menggunakan MobileNetV3-Small

## Anggota Kelompok 
1. Nicholas - 103102400047
2. Devika Widya Vania - 103102400044
3. Zalsabila Rezky Amelia Arep - 103102400043
4. Sofia - 103102400039

Proyek ini dikembangkan untuk membedakan varietas jagung berdasarkan fitur visual biji. Fokus utamanya adalah efisiensi model menggunakan arsitektur **MobileNetV3-Small** dan perbandingan performa antara bobot terbaik (*Best*) serta bobot terakhir (*Last*) selama 30 epoch.

**Tugas utama meliputi:**
- **Preprocessing**: Pembersihan gambar rusak dan augmentasi data.
- **Modeling**: Implementasi Transfer Learning dengan pembekuan backbone.
- **Evaluation**: Analisis performa menggunakan Confusion Matrix, Classification Report, dan Kurva ROC.

---

## Struktur Project
```text
├── Corn_Classification_Code.ipynb  # Notebook utama (Training & Eval)
├── Corn_Image_Dataset/             # Folder dataset (Train, Val, Test)
│   ├── Chulpi Cancha/
│   ├── Indurata/
│   └── Rugosa/
├── Laporan_Corn_Classification 
└── README.md                        # Dokumentasi proyek

```
---
## Dataset Overview
* **Total Data**: 1.050 gambar.
* **Kelas**: 3 Varietas (Chulpi Cancha, Indurata, Rugosa).
* **Pembagian Data**: 
    * 70% Training
    * 15% Validation
    * 15% Testing.
* **Preprocessing**: Pembersihan gambar korup, resize 224x224, dan augmentasi (rotasi & color jitter).

## Detail Model & Pelatihan
* **Arsitektur**: MobileNetV3-Small (Pretrained on ImageNet).
* **Optimizer**: AdamW.
* **Scheduler**: Cosine Annealing Learning Rate.
* **Loss Function**: Cross-Entropy Loss.
* **Epochs**: 30.
* **Teknik**: Mixed Precision Training (GradScaler) untuk efisiensi memori GPU.

## Hasil & Evaluasi
* Grafik Loss dan Akurasi (Training vs Validation).
* **Confusion Matrix** untuk melihat kesalahan prediksi antar kelas.
* **Classification Report** (Precision, Recall, F1-Score).
* **ROC Curve & AUC Score** untuk evaluasi performa probabilitas model.

---
**Cara Menjalankan Program**

**1. Prasyarat**
* **Python 3.8+** sudah terinstal.
* **Environment**: Disarankan menggunakan Google Colab atau perangkat dengan GPU (NVIDIA), namun tetap bisa berjalan di CPU.
* **Library Utama**: `torch`, `torchvision`, `matplotlib`, `scikit-learn`, `tqdm`, `pillow`.

**2. Langkah Instalasi & Run**
* Clone atau download repository ke perangkat lokal:
```bash
git clone https://github.com/ddev-0504/Corn-Classification.git

```

* Instal library yang dibutuhkan:
```bash
pip install torch torchvision matplotlib scikit-learn tqdm pillow

```

* Jalankan program/notebook:
```bash
jupyter notebook 30-epoch-perbandingan-best-dan-last.ipynb

```

*(Atau buka file tersebut melalui VS Code / Google Colab dan pilih **Run All**).*
