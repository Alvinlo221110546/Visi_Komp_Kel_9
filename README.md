# Computer Vision Pipeline

![OpenCV](https://img.shields.io/badge/OpenCV-4.8.0-blue)
![Python](https://img.shields.io/badge/Python-3.8+-yellow)

## 📝 Deskripsi Proyek

Pipeline ini mengimplementasikan alur lengkap pemrosesan gambar computer vision dari awal hingga ekstraksi fitur. Kode ini cocok untuk pembelajaran pengolahan gambar digital dan computer vision dasar.

## 🏗️ Alur Pemrosesan

### 1. Preprocessing (pra-pemrosesan)
```python
# Histogram equalization untuk meningkatkan kontras
image_eq = cv2.equalizeHist(image)
Mengunduh dataset COCO val2014

Konversi ke grayscale

Equalisasi histogram untuk perbaikan kontras

Penyimpanan hasil di folder /val2014_processed

2. Deteksi Tepi
python
# Deteksi tepi dengan Canny
tepi_cv = cv2.Canny(gambar, lower, upper)
Implementasi deteksi tepi menggunakan:

Canny edge detection (OpenCV)

Operator Sobel (manual)

Visualisasi perbandingan hasil

Penyimpanan di folder /val_edge

3. Deteksi Pojok Harris
python
# Deteksi pojok Harris
harris = cv2.cornerHarris(gray_img, blockSize, ksize, k)
Deteksi feature point menggunakan Harris Corner

Implementasi manual untuk matriks 15x15

Visualisasi response heatmap

Penyimpanan di folder /val_harris

4. Filter Median
python
# Filter median 3x3
median = cv2.medianBlur(img, 3)
Reduksi noise dengan filter median

Perhitungan manual untuk neighborhood 3x3

Penyimpanan di folder /val_median

5. Operator Prewitt
python
# Prewitt edge detection
prewitt_x = cv2.filter2D(img, -1, prewitt_x_kernel)
Deteksi tepi menggunakan operator Prewitt

Perhitungan gradien manual

Penyimpanan di folder /val_prewitt

6. Operasi Morfologi
python
# Erosi dan dilasi
eroded = cv2.erode(img, kernel)
dilated = cv2.dilate(img, kernel)
Implementasi:

Erosi

Dilasi

Skeletonisasi

Penjelasan langkah demi langkah

Penyimpanan di folder /val_morphology

7. Ekstraksi Fitur ORB
python
# Deteksi fitur ORB
orb = cv2.ORB_create()
kp, des = orb.detectAndCompute(img, None)
Deteksi dan deskripsi fitur

Pencocokan fitur dengan Brute-Force Matcher

Visualisasi keypoints

Penyimpanan di folder /val_features

🛠️ Instalasi
Clone repository

bash
git clone https://github.com/username/project.git
Install dependencies

bash
pip install opencv-python numpy matplotlib