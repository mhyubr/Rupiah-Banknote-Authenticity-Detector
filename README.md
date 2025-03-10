# Rupiah-Banknote-Authenticity-Detector

<p align="center">
  <img src="real_fake_rupiah/assets/images/Mockup%20Start%20App.png" alt="Screenshot 1" width="150"/>
  <img src="real_fake_rupiah/assets/images/Mockup%20Asli.png" alt="Screenshot 2" width="150"/>
  <img src="real_fake_rupiah/assets/images/Mockup%20Palsu.png" alt="Screenshot 3" width="150"/>
</p>
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
  <br>
  <strong>Percentage of persons with disabilities by type</strong>
  <strong>Source: Susenas (2020), in Bappenas (2021)</strong>
</p>

According to the 2020 population census data released by Badan Pusat Statistik, Indonesia had a population of over 270 million people (BPS, 2020). By 2024, Indonesia's population increased by 11 million, making it the fourth most populous country in the world (BPS, 2024). Among this population, approximately 22.97 million people, or about 8.51% of the total population in 2020, were classified as persons with disabilities (Kemensos, 2022). Within this category, individuals with visual impairments were the largest group, totaling approximately 3,474,035 people (Brebahama et al., 2020).

<p align="center">
  <img height="300" alt="image" src="https://github.com/user-attachments/assets/f29d698f-d792-4be7-a686-e38d518ba816"/>
  <br>
  <strong>The number of counterfeit Rupiah banknotes in circulation in Indonesia from 2016 to 2022</strong>
  <strong>Bank Indonesia (2022), in Sadya (2022)</strong>
</p>

Data from Bank Indonesia (2022), as cited in Sadya (2022), indicates that the circulation of counterfeit currency in Indonesia reached 575,327 banknotes in 2022 (recorded from January to October 2022), as shown in Figure I.2. This number represents a 154.38% increase compared to the previous year, which recorded 260,394 counterfeit banknotes in 2021 (Bank Indonesia, 2022, as cited in Sadya, 2022). This issue requires serious attention as it may lead to future problems, particularly in ensuring transaction security for the Indonesian public. Moreover, the high circulation of counterfeit Rupiah banknotes can undermine public trust in the Rupiah currency and the national financial system.

<p align="center">
  <img height="300" alt="image" src="https://github.com/user-attachments/assets/494b1d79-d99c-4f4c-832e-b33393a6b39a"/>
  <br>
  <strong>Testing the existing system using counterfeit Rupiah banknotes from the 2016 and 2022 emissions</strong>
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
<p align="center">
  <strong>Gap Analysis</strong>
</p>

| **Current State** | **Desired State** | **Action Plan** |
|------------------|------------------|----------------|
| The existing system does not have a feature to identify the authenticity of Rupiah banknotes with output in text and/or audio format | SiThe system can identify the authenticity of Rupiah banknotes with output in text and/or audio format, making it easier to understand for visually impaired individuals | MThe system can identify the authenticity of Rupiah banknotes with output in text and/or audio format, making it easier to understand for visually impaired individuals |
| SThe existing system does not provide confidence probability in the detection process | The system can present confidence probability that measures the uncertainty of prediction results, both in text and audio format, providing more information for visually impaired individuals in using Rupiah banknotes | MDevelop a system that can display confidence probability in the identification process of Rupiah banknotes in text and/or audio format |

## 🏗 Data Preparation

### Data collection

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/8ce94436-b929-4e92-861f-d1c5eee724a3" />
  <br>
  <strong>Authentic Rupiah banknotes issued in 2016 and 2022</strong>
</p>
<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/9db4c5ce-faea-4db2-bb3f-4b330105abfd" />
  <br>
  <strong>Counterfeit Rupiah banknotes issued in 2016 and 2022</strong>
</p>

The data used in this study consists of unstructured data in the form of images of Rupiah banknotes issued in 2016 and 2022, with denominations of Rp10,000, Rp20,000, Rp50,000, and Rp100,000. The collected images were obtained from various sources and reflect real-world conditions during image acquisition. These conditions include banknotes in normal condition, crumpled, with scribbles, different background variations, and varying lighting intensities.

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/5f62c9d4-7a8a-424d-9d6b-130b2b44c9c5" />
  <br>
  <strong>Comparison of Dataset Collection</strong>
</p>

The collection of authentic and counterfeit Rupiah banknote images with various denominations was conducted through direct image acquisition and sourcing from relevant external sources. The image data obtained from the developer’s photography consists of 1,002 images, comprising 793 authentic banknote images and 209 counterfeit banknote images. Additionally, the dataset collected from external sources contains 86 images, including 80 authentic banknote images and 6 counterfeit banknote images. Therefore, the total dataset used in this study consists of 1,088 Rupiah banknote images.

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/20c0ddbb-124f-4a3c-bd72-5eb1d3ac3f79" />
  <br>
  <strong>Rupiah banknotes in various conditions</strong>
</p>

The developer also incorporated various real-world conditions beyond image augmentation that visually impaired individuals might encounter when detecting the authenticity of Rupiah banknotes. These conditions could pose challenges for visually impaired users in the identification process. Such conditions include crumpled banknotes, marked or scribbled notes, and certain factors that may go unnoticed by visually impaired individuals, such as tilted or 180° rotated banknotes.

### Data Labeling

<p align="center">
  <img width="284" alt="image" src="https://github.com/user-attachments/assets/433fa5e3-5233-4327-96ee-ea01656dd495" />
  <br>
  <strong>Image data labeling</strong>
</p>
In image data processing, data labeling is the process of assigning labels or categories to each image in the dataset before using it to train a model. In this study, the chosen image labeling method is folder-based labeling, selected for its ease of implementation and compatibility with widely used training libraries such as TensorFlow and PyTorch. The labeling process involves dividing the dataset into two main parts: train and test. Each part contains two subfolders: asli (genuine), which holds images of authentic banknotes, and palsu (fake), which contains images of counterfeit banknotes.

### Data Splitting

<p align="center">
  <img width="267" alt="image" src="https://github.com/user-attachments/assets/a2bce6cf-de6f-4f1e-a730-eb4c65d2a091" />
  <br>
  <strong>Single train-test split with an external testing set</strong>
  <strong>Source (Mathai et al., 2020)</strong>
</p>

This development adopts the data splitting technique with a single train-test split scheme complemented by an external testing set. This scheme is applied to separate the evaluation conducted during model development (internal evaluation) from the final evaluation when the model is ready for deployment (external evaluation).

The primary reason for choosing this scheme is that internal validation, in this case using validation data, is insufficient to determine the predictive performance of the model under development. Therefore, external evaluation is required using testing data, which is independent and not involved during the model development process (Baumann, D & Baumann, K, 2014, as cited in Mathai et al., 2020).

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/51a31eea-2243-4dd1-a96e-e7031d98470b" />
  <br>
  <strong>Data splitting</strong>
</p>

In this development, the data split ratio between the training dataset and the testing dataset is 80:20. A total of 80% of the data is allocated for training and validation, which is further divided using a 80:20 or 70:30 ratio, with the selection determined through a hyperparameter tuning process.

From the total dataset, 80% accounts for 870 images, while the remaining 20% is used for model testing, consisting of 218 images.

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/617887cc-4a0c-4f1b-9b0c-a664828c03cd" />
  <br>
  <strong>Data splitting is performed based on class labels</strong>
</p>

Based on the data split results, 708 images of genuine banknotes and 162 images of counterfeit banknotes are used for model training and validation. Meanwhile, 165 images of genuine banknotes and 53 images of counterfeit banknotes are used for model testing.

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/3e9b822c-acf6-4fcb-bebd-ef3a1bdf2a02" />
  <br>
  <strong>Train Dataset</strong>
</p>

The training dataset comes from the train directory, which is then split into training and validation data with a ratio of 70:30 or 80:20, used for model testing simulations with hyperparameter tuning. The training dataset consists of images that have undergone the cropping process, making up 70% or 80% of the train directory.

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/73e425a6-50cd-41cf-9dc0-1cedb44c75ff" />
  <br>
  <strong>Validation Dataset</strong>
</p>

The validation dataset comes from the train directory, which has been split at a 70:30 or 80:20 ratio for training and validation purposes. The validation dataset consists of images that have undergone the cropping process, making up 30% or 20% of the train directory. No image augmentation is applied to the validation dataset to preserve the authenticity of the images, ensuring consistent and accurate validation of the model’s performance on unseen data. Additionally, the validation dataset is used to evaluate the model during training to aid in model selection and hyperparameter tuning.

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/4371194f-76a9-4c48-bba2-11651e956977" />
  <br>
  <strong>Test Dataset</strong>
</p>

The testing dataset comes from the test directory, comprising 20% of the total dataset. The testing dataset does not undergo image cropping or image augmentation to maintain the authenticity of the images, ensuring that it reflects real-world conditions when determining the authenticity of banknotes for visually impaired individuals. The images in the testing dataset are expected to represent actual conditions that visually impaired individuals may encounter when identifying the authenticity of Rupiah banknotes from the 2016 and 2022 emissions.

## Data Preprocessing

After collecting and labeling the Rupiah banknote image data, the developer proceeds with data preprocessing to ensure the images are ready for the modeling stage.

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/17b56e5c-3c20-49c1-88f8-602003859e44" />
  <br>
  <strong>Test Dataset</strong>
</p>


## 📝 Evaluation & Analysis
