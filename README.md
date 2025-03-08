# Rupiah-Banknote-Authenticity-Detector

<p align="center">
  <img src="real_fake_rupiah/assets/images/Mockup%20Start%20App.png" alt="Screenshot 1" width="150"/>
  <img src="real_fake_rupiah/assets/images/Mockup%20Asli.png" alt="Screenshot 2" width="150"/>
  <img src="real_fake_rupiah/assets/images/Mockup%20Palsu.png" alt="Screenshot 3" width="150"/>
</p>
<br>
Rupiah Banknote Authenticity Detector is a project that integrates machine learning with a mobile application to verify the authenticity of Rupiah banknotes. This project utilizes a Deep Learning-based image detection model, trained through fine-tuning on a pre-trained model, to determine whether a banknote is genuine or counterfeit. The model is developed and trained using the High-API Framework TensorFlow Keras, while the user interface is built using the cross-platform Flutter framework.

### 📱 Application Demo:
https://youtu.be/4KxXdnXJpFA

## 💻 Development Environment Specifications

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
- **System RAM**: 62.8 GB
- **GPU RAM**: 16,384 MiB
- **Storage Capacity**: 201.2 GB

### 3. Flutter Dependencies
This project uses several Flutter dependencies to handle camera functionality, TensorFlow Lite models, audio, and logging:
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
```

## 🎯 Business Understanding
<p align="center">
  <img height="300" alt="image" src="https://github.com/user-attachments/assets/e269a576-cff0-43af-bf52-ec2d46a563dd"/>
</p>

According to the 2020 population census data released by Badan Pusat Statistik, Indonesia had a population of over 270 million people (BPS, 2020). By 2024, Indonesia's population increased by 11 million, making it the fourth most populous country in the world (BPS, 2024). Among this population, approximately 22.97 million people, or about 8.51% of the total population in 2020, were classified as persons with disabilities (Kemensos, 2022). Within this category, individuals with visual impairments were the largest group, totaling approximately 3,474,035 people (Brebahama et al., 2020).

<p align="center">
  <img height="300" alt="image" src="https://github.com/user-attachments/assets/f29d698f-d792-4be7-a686-e38d518ba816"/>
  <strong>The number of counterfeit Rupiah banknotes in circulation in Indonesia from 2016 to 2022.
Source: Bank Indonesia (2022), in Sadya (2022).</strong>
</p>

Data from Bank Indonesia (2022), as cited in Sadya (2022), indicates that the circulation of counterfeit currency in Indonesia reached 575,327 banknotes in 2022 (recorded from January to October 2022), as shown in Figure I.2. This number represents a 154.38% increase compared to the previous year, which recorded 260,394 counterfeit banknotes in 2021 (Bank Indonesia, 2022, as cited in Sadya, 2022). This issue requires serious attention as it may lead to future problems, particularly in ensuring transaction security for the Indonesian public. Moreover, the high circulation of counterfeit Rupiah banknotes can undermine public trust in the Rupiah currency and the national financial system.

<p align="center">
  <img height="300" alt="image" src="https://github.com/user-attachments/assets/494b1d79-d99c-4f4c-832e-b33393a6b39a"/>
  <br>
  <strong>Testing the existing system using genuine Rupiah banknotes from the 2016 and 2022 emissions</strong>
</p>
<p align="center">
  <img height="300" alt="image" src="https://github.com/user-attachments/assets/4e70363f-480b-45d7-affa-445ff12adb83" />
  <br>
  <strong>Testing the existing system using genuine Rupiah banknotes from the 2016 and 2022 emissions</strong>
</p>

The developer conducted several experiments on the existing Rupiah banknote identification system mentioned earlier. The developer used samples of Rp50,000 and Rp100,000 banknotes from different emission years, namely 2016 and 2022. The experiments on the existing Rupiah banknote identification system were carried out using the Cash Reader application.

Based on the experiments conducted, several features were found in the application, including:

* Displays the banknote's denomination as text
* Provides the banknote's denomination as audio output
* Identifies the denomination on both sides (front and back)
* Supports the detection of Rupiah banknotes from the 2016 and 2022 emissions

From the experiments conducted by the developer, it was found that the application does not yet support the detection or identification of Rupiah banknote authenticity, either in text or audio form. Referring to these experiments, the results can be used as the basis for a gap analysis. The results of the gap analysis are presented in the following table:

<strong>Gap Analysis</strong>
| **Current State** | **Desired State** | **Action Plan** |
|------------------|------------------|----------------|
| SThe existing system does not have a feature to identify the authenticity of Rupiah banknotes with output in text and/or audio format | SiThe system can identify the authenticity of Rupiah banknotes with output in text and/or audio format, making it easier to understand for visually impaired individuals | MThe system can identify the authenticity of Rupiah banknotes with output in text and/or audio format, making it easier to understand for visually impaired individuals |
| SThe existing system does not provide confidence probability in the detection process | The system can present confidence probability that measures the uncertainty of prediction results, both in text and audio format, providing more information for visually impaired individuals in using Rupiah banknotes | MDevelop a system that can display confidence probability in the identification process of Rupiah banknotes in text and/or audio format |

## 🏗 Data Preparation

## 📝 Evaluation & Analysis
