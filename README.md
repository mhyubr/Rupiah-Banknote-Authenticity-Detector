# Rupiah-Banknote-Authenticity-Detector

<p align="center">
  <img src="real_fake_rupiah/assets/images/Mockup%20Start%20App.png" alt="Screenshot 1" width="150"/>
  <img src="real_fake_rupiah/assets/images/Mockup%20Asli.png" alt="Screenshot 2" width="150"/>
  <img src="real_fake_rupiah/assets/images/Mockup%20Palsu.png" alt="Screenshot 3" width="150"/>
</p>

Rupiah Banknote Authenticity Detector is a project that integrates machine learning with a mobile application to verify the authenticity of Rupiah banknotes. This project utilizes a Deep Learning-based image detection model, trained through fine-tuning on a pre-trained model, to determine whether a banknote is genuine or counterfeit. The model is developed and trained using the High-API Framework TensorFlow Keras, while the user interface is built using the cross-platform Flutter framework.

### Application Demo:
https://youtu.be/4KxXdnXJpFA

## Development Environment Specifications

### 1. Modeling Environment
- **Python Version**: 3.10.13
- **Numpy**: 1.26.4
- **Pandas**: 2.2.2
- **TensorFlow**: 2.15.0
- **Matplotlib**: 3.7.5
- **Seaborn**: 0.12.2
- **Scikit-learn**: 1.2.2
- **Optuna**: 3.6.1

### 2. Computing Specifications
- **Accelerator Name**: Tesla P100-PCIE-16GB
- **Versi CUDA**: 12.2
- **Power Capacity**: 250 W
- **RAM Sistem**: 62.8 GB
- **RAM GPU**: 16,384 MiB
- **Kapasitas Penyimpanan**: 201.2 GB

## Aplikasi Mobile (Flutter)

### Deskripsi Proyek
Aplikasi Flutter ini berfungsi sebagai antarmuka untuk mendeteksi keaslian uang Rupiah menggunakan model TensorFlow yang telah dilatih. Dengan memanfaatkan kamera perangkat, aplikasi dapat mengambil gambar uang Rupiah dan memberikan hasil deteksi mengenai keasliannya.

### Struktur Proyek Flutter
- **Nama Proyek**: `real_fake_rupiah`

### Flutter Dependencies
Proyek ini menggunakan beberapa dependencies Flutter untuk menangani fungsionalitas kamera, model TensorFlow Lite, serta audio dan logging:

```yaml
dependencies:
  flutter:
    sdk: flutter
  camera: ^0.11.0
  tflite_v2: ^1.0.0
  audioplayers: ^6.0.0
  logger: ^2.3.0
  cupertino_icons: ^1.0.6

dev_dependencies:
  flutter_test:
    sdk: flutter
  flutter_lints: ^3.0.0
