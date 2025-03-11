# Rupiah-Banknote-Authenticity-Detector

<p align="center">
  <img src="real_fake_rupiah/assets/images/Mockup%20Start%20App.png" alt="Screenshot 1" width="150"/>
  <img src="real_fake_rupiah/assets/images/Mockup%20Asli.png" alt="Screenshot 2" width="150"/>
  <img src="real_fake_rupiah/assets/images/Mockup%20Palsu.png" alt="Screenshot 3" width="150"/>
</p>
Rupiah Banknote Authenticity Detector is a project that integrates machine learning with a mobile application to verify the authenticity of Rupiah banknotes. This project utilizes a Deep Learning-based image detection model, trained through fine-tuning on a pre-trained model, to determine whether a banknote is genuine or counterfeit. The model is developed and trained using the High-API Framework TensorFlow Keras, while the user interface is built using the cross-platform Flutter framework.

### 📄 Publication:
https://ieeexplore.ieee.org/document/10751570

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
  <img height="200" alt="image" src="https://github.com/user-attachments/assets/494b1d79-d99c-4f4c-832e-b33393a6b39a"/>
  <br>
  <strong>Testing the existing system using counterfeit Rupiah banknotes from the 2016 and 2022 emissions</strong>
</p>
<p align="center">
  <img height="200" alt="image" src="https://github.com/user-attachments/assets/4e70363f-480b-45d7-affa-445ff12adb83" />
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
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/8ce94436-b929-4e92-861f-d1c5eee724a3" />
  <br>
  <strong>Authentic Rupiah banknotes issued in 2016 and 2022</strong>
</p>
<p align="center">
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/9db4c5ce-faea-4db2-bb3f-4b330105abfd" />
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
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/51a31eea-2243-4dd1-a96e-e7031d98470b" />
  <br>
  <strong>Data splitting</strong>
</p>

In this development, the data split ratio between the training dataset and the testing dataset is 80:20. A total of 80% of the data is allocated for training and validation, which is further divided using a 80:20 or 70:30 ratio, with the selection determined through a hyperparameter tuning process.

From the total dataset, 80% accounts for 870 images, while the remaining 20% is used for model testing, consisting of 218 images.

<p align="center">
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/617887cc-4a0c-4f1b-9b0c-a664828c03cd" />
  <br>
  <strong>Data splitting is performed based on class labels</strong>
</p>

Based on the data split results, 708 images of genuine banknotes and 162 images of counterfeit banknotes are used for model training and validation. Meanwhile, 165 images of genuine banknotes and 53 images of counterfeit banknotes are used for model testing.

<p align="center">
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/3e9b822c-acf6-4fcb-bebd-ef3a1bdf2a02" />
  <br>
  <strong>Train Dataset</strong>
</p>

The training dataset comes from the train directory, which is then split into training and validation data with a ratio of 70:30 or 80:20, used for model testing simulations with hyperparameter tuning. The training dataset consists of images that have undergone the cropping process, making up 70% or 80% of the train directory.

<p align="center">
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/73e425a6-50cd-41cf-9dc0-1cedb44c75ff" />
  <br>
  <strong>Validation Dataset</strong>
</p>

The validation dataset comes from the train directory, which has been split at a 70:30 or 80:20 ratio for training and validation purposes. The validation dataset consists of images that have undergone the cropping process, making up 30% or 20% of the train directory. No image augmentation is applied to the validation dataset to preserve the authenticity of the images, ensuring consistent and accurate validation of the model’s performance on unseen data. Additionally, the validation dataset is used to evaluate the model during training to aid in model selection and hyperparameter tuning.

<p align="center">
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/4371194f-76a9-4c48-bba2-11651e956977" />
  <br>
  <strong>Test Dataset</strong>
</p>

The testing dataset comes from the test directory, comprising 20% of the total dataset. The testing dataset does not undergo image cropping or image augmentation to maintain the authenticity of the images, ensuring that it reflects real-world conditions when determining the authenticity of banknotes for visually impaired individuals. The images in the testing dataset are expected to represent actual conditions that visually impaired individuals may encounter when identifying the authenticity of Rupiah banknotes from the 2016 and 2022 emissions.

### Data Preprocessing

After collecting and labeling the Rupiah banknote image data, the developer proceeds with data preprocessing to ensure the images are ready for the modeling stage.

#### Image Croping

<p align="center">
  <img width="580" alt="image" src="https://github.com/user-attachments/assets/17b56e5c-3c20-49c1-88f8-602003859e44" />
  <br>
  <strong>Image Croping</strong>
</p>

During the collection of Rupiah banknote images, whether through direct photography by the developer or from other sources, various background conditions and hand images were present in some data. Therefore, to prevent the model from learning these backgrounds and hand images, which could introduce bias in model performance, the developer applied image cropping.

#### Image Resizing

<p align="center">
  <img width="580" alt="image" src="https://github.com/user-attachments/assets/a5996e43-83c4-4be1-b300-dd13fd511dc8" />
  <br>
  <strong>Image Resizing</strong>
</p>

In this development, the image resizing method is applied using sizes recommended by the pre-trained architecture while also considering findings from Lakhani (2020). The study indicates that, in most cases, an image size of 256 × 256 pixels reaches a plateau, where increasing the resolution does not significantly improve model accuracy. Additionally, the same study found that, under certain conditions, larger image sizes, such as 448 × 448 pixels to 512 × 512 pixels, perform better as features become more visible at higher resolutions, enhancing detection accuracy compared to lower resolutions. Therefore, this development utilizes image sizes of 256 × 256 pixels, 448 × 448 pixels, and 512 × 512 pixels, with the best parameter selection conducted through hyperparameter tuning.

#### Image Normalizing

<p align="center">
  <img width="580" alt="image" src="https://github.com/user-attachments/assets/c11a1a92-6f3c-454f-9cfc-52ee7c4b1a83" />
  <br>
  <strong>Image Normalizing</strong>
</p>

In this development, normalization is applied to the training, validation, and testing datasets using an empirical method simplified from the min-max normalization method, which can be mathematically formulated as follows.

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/b527bb84-20a7-4109-b862-055c5eec71fd" />
  <br>
  <strong>Min-Max Normalization</strong>
</p>

Where:
- Xnorm  = normalization result of Xi
- Xi     = data to be normalized
- min(X) = minimum value in dataset X
- max(X) = maximum value in dataset X

The minimum intensity value of the image is 0, and the maximum value is 255. Therefore, the min-max normalization equation can be simplified into the following equation, resulting in an empirical method.

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/53b35c56-a2e1-4f47-ab5f-6b0227504636" />
  <br>
  <strong>Metode Empirical</strong>
</p>

- Xnorm  = normalization result of Xi
- Xi     = data to be normalized

#### One-Hot Encoding

In this development, the one-hot encoding method is used to align with the output activation function, which is softmax. The use of this method also considers research conducted by Lu (2020) in the study titled "Quasi-Orthonormal Encoding for Machine Learning Applications." This research highlights the relationship between one-hot encoding and the softmax activation function in handling categorical variables within classification models.

The study explains that one-hot encoding effectively represents both input and target output in multi-class classification. The softmax function processes the model's output by converting raw values from the final neural network layer into a probability distribution. It then utilizes loss functions such as cross-entropy for model training.

Similarly, during the decoding phase, the one-hot encoding method converts the model's output back into categorical form using the argmax function. The argmax function selects the index with the highest value in the output vector, while the softmax function generates a probability vector to determine the class with the highest probability.

<p align="center">
  <img width="550" alt="image" src="https://github.com/user-attachments/assets/8f209823-95f2-4dde-bba5-e12d615670b1" />
  <br>
  <strong>One-hot Encoding</strong>
</p>

In the table, each class is encoded in a binary vector format, allowing machine learning algorithms to process categorical information in a numerically interpretable manner. The table presents the results of one-hot encoding for both classes or labels: genuine and counterfeit. The genuine class is represented by the binary vector [1., 0.], meaning that for data belonging to the genuine class, the first element in the vector is 1, and the second element is 0. Conversely, the counterfeit class is represented by the binary vector [0., 1.], where the first element is 0, and the second element is 1.

#### Image Augmentation

<p align="center">
  <img width="700" alt="image" src="https://github.com/user-attachments/assets/100448d8-e463-413c-9af1-83b9f5b9cd39" />
  <br>
  <strong>Image Augmentation</strong>
</p>

Image augmentation is a process used to generate new images from existing image data to increase the diversity and quantity of data available for training a model. It is employed to enhance model performance and robustness by introducing variations in the training data. The use of image augmentation also helps the model generalize to new images that have not been seen before or during the training process.

At this stage, the developer applies transformations to each training image to introduce variations and simulate different conditions of Rupiah banknotes during the training process.

Therefore, to ensure the trained dataset can adapt to various conditions of Rupiah banknotes used by visually impaired individuals, five types of transformations are applied in this development, as follows:

1. Randomly adjusting the brightness of the image by up to 25% brighter or darker. In this case, the image can have a brightness level ranging from 75% to 125% of its original brightness. The purpose of this transformation is to make the model more robust against lighting variations that visually impaired individuals may encounter when identifying the authenticity of Rupiah banknotes.

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/297d6d39-201f-4f17-b929-5c8c0a042d5b" />
  <br>
  <strong>Adjust brightness</strong>
</p>

2. Randomly rotating the image within an angle range of 0 to 315° (clockwise) or 0 to -315° (counterclockwise). The purpose of this transformation is to add variation to the training data by changing the image orientation, helping the model learn to recognize objects from different angles. Additionally, this transformation is used to prevent situations where visually impaired individuals are unaware of the angle of the banknote being identified.

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/a27d8fd8-22f2-457c-af65-948e91fb5605" />
  <br>
  <strong>Rotation</strong>
</p>

3. Randomly shifting the image horizontally by up to 20% of the original image width. The purpose of this transformation is to simulate changes in object positioning within the image, which may occur when visually impaired individuals identify the authenticity of Rupiah banknotes.

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/985e8327-3b98-434c-8e74-ab28cda467b5" />
  <br>
  <strong>Width shift</strong>
</p>

4. Randomly shifting the image vertically by up to 20% of the original image height. The purpose of this transformation is to help the model recognize objects that may be slightly shifted up or down in situations where visually impaired individuals identify the authenticity of Rupiah banknotes.

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/a985d31b-d659-44dd-b814-36006c560054" />
  <br>
  <strong>Height shift</strong>
</p>

5. Randomly scaling the image within a range of 0% to 25% of the original size. In this case, the image size will vary between 75% and 125% of its original dimensions. The purpose of this transformation is to help the model recognize objects from different distances, ensuring that the model can accurately identify Rupiah banknotes even when the observation distance varies.

<p align="center">
  <img width="300" alt="image" src="https://github.com/user-attachments/assets/d0687e1f-eb2c-43cc-ae5e-5fb5575d5df8" />
  <br>
  <strong>Height shift</strong>
</p>

## 🛠️ Model Preparation

The models used in this development are custom CNN architectures and pre-trained architectures, namely VGG-19 and EfficientNetV2. For the EfficientNetV2 architecture, the developer selected the EfficientNetV2B2 variant based on the consideration that this development requires a model architecture with higher complexity and accuracy while still accounting for available resource constraints. The selection of the EfficientNetV2-B2 variant also considers the study by Pardede & Purohita (2023), which compares 12 types of pre-trained architectures, including eight (8) variants of EfficientNetV2: EfficientNetV2B0, EfficientNetV2B1, EfficientNetV2B2, EfficientNetV2B3, EfficientNetV2S, EfficientNetV2M, and EfficientNetV2L, ordered from the smallest to the largest variant based on parameter size (model weights). The study results indicate that the EfficientNetV2 architecture, particularly the EfficientNetV2B2 variant, consistently achieves an accuracy and F1-Score above 80%. This model has the fourth fastest training time, following MobileNetV3L, EfficientNetV2B0, and EfficientNetV2B1, with a training time of 29 minutes and 5 seconds at the 100th epoch using the fine-tuning method.

The pre-trained architectures VGG-19 and EfficientNetV2B2 are used with a fully-trainable approach, meaning all layers are retrained to perform fine-tuning.

<p align="center">
  <img width="700" alt="image" src="https://github.com/user-attachments/assets/05f30162-1aae-4cbe-8253-f64c0134df8d" />
  <br>
  <strong>Custom CNN architecture</strong>
</p>

The custom CNN architecture, as shown in Figure, receives input in the form of images with sizes of 256 × 256 pixels, 448 × 448 pixels, or 512 × 512 pixels, which are tested through hyperparameter tuning (the largest input size is used in Figure IV.23) with three channels (red, green, and blue). The neural network structure consists of five main blocks, where each block contains Conv2D and MaxPooling layers.

Block 1 starts the process with a single Conv2D layer containing 32 filters of size 3×3, followed by a MaxPooling layer of size 2×2 to reduce spatial dimensions. In Block 2 and Block 3, the number of filters increases to 64 with a 3×3 kernel, followed by a 2×2 MaxPooling layer. This pattern continues in Block 4 and Block 5, where the number of filters increases to 128.

After passing through these five blocks, the output from the last block is flattened into a one-dimensional vector. This vector is then forwarded to a fully connected (dense) layer with 512 neurons using ReLU activation, followed by a dropout layer with a rate of 0.2 to prevent overfitting by disabling some neurons during training. Finally, the output from the dense layer is passed to an output layer with two neurons, which uses the softmax activation function to determine the probability of two different classes (genuine or counterfeit). All parameters in this network are trainable, meaning every weight is updated during the training process, with a total of 13,124,352 parameters and a memory usage of 50.07 MB.

<p align="center">
  <img width="700" alt="image" src="https://github.com/user-attachments/assets/99bdb0df-1030-4a4a-825b-299d1cc436ec" />
  <br>
  <strong>VGG-19 Architecture</strong>
</p>

In the pre-trained VGG-19 architecture shown in the figure, the input layer receives Rupiah banknotes as images in the form of three channels (red, green, and blue). The VGG-19 structure consists of five convolutional blocks, each containing two Conv2D (convolution) layers followed by a MaxPooling layer. The main characteristic of this architecture is that in each block, the spatial dimensions of the image are reduced, while the number of filters (which indicate features) increases.

In Block 1, the convolutional layer uses filters with a size of 64, followed by MaxPooling to reduce spatial dimensions. In Block 2, the number of filters increases to 128, with a further reduction in image size. In Blocks 3 and 4, the filter size continues to increase to 256 and 512, respectively, along with further reductions in image dimensions. Finally, in Block 5, the filter size remains at 512, but the image dimensions continue to decrease.

After passing through the five convolutional blocks, Global Average Pooling is applied to reduce the dimensions to 512 features in a one-dimensional vector. Once the dimensionality is reduced through pooling, these features pass through a fully connected (dense) layer with 512 neurons using ReLU activation to process the extracted features. In the output layer, the features go through a probability classification process using the softmax activation function, which determines whether the image belongs to the genuine or counterfeit Rupiah banknote class.

In this VGG-19 architecture, dropout regularization is not applied to maintain the authenticity of the performance comparison between the pre-trained VGG-19 model and other architectures during testing. This approach ensures that each model's performance is evaluated fairly and objectively without interference from regularization techniques that could influence the final results. Overall, the VGG-19 architecture has approximately 9,409,520 trainable parameters with a memory size of 77.39 MB.

<p align="center">
  <img width="700" alt="image" src="https://github.com/user-attachments/assets/9da6d431-5a23-4ceb-b105-a59761aab2aa" />
  <br>
  <strong>EfficientNetV2B2 Architecture</strong>
</p>

The image displays the EfficientNetV2B2 architecture used in this development. The architecture processes input images of Indonesian Rupiah banknotes with varying resolutions, which will be tested using hyperparameter tuning. The input images are then converted into a format with three channels (red, green, and blue).

In the first layer of EfficientNetV2B2, there is a stem layer consisting sequentially of an input layer, rescaling, normalization, zero padding, Conv2D, batch normalization, and activation. The subsequent layers consist of seven main blocks, where each block contains a combination of modules (Module 1, Module 2, and Module 3) that perform various convolution operations. These operations aim to reduce model complexity while enhancing processing efficiency. A detailed structure of each module in the EfficientNetV2B2 architecture can be seen in the following table.

<p align="center">
  <img width="538" alt="image" src="https://github.com/user-attachments/assets/52e1af22-ad80-4433-ba25-dc6c13e1e925" />
  <br>
  <strong>Layer arrangement in the EfficientNetV2B2 architecture module</strong>
</p>

Each block concludes with an add operation, which merges information from multiple layers within the block, enabling deeper and more diverse feature learning. After passing through these seven blocks, the output from the last block is processed through a Global Average Pooling layer, reducing the feature dimensions into a one-dimensional vector of length 1408. This vector is then passed to a fully connected (dense) layer with 512 neurons. Finally, the output from the dense layer is fed into the output layer, which utilizes the softmax activation function to classify the image as either an authentic or counterfeit Rupiah banknote.

In this EfficientNetV2B2 architecture, dropout regularization is not applied to maintain the integrity of performance comparisons between the pre-trained EfficientNetV2B2 model and other architectures during testing. This approach ensures that model performance evaluations are conducted fairly and objectively, without any influence from regularization techniques that could alter the final results. Overall, the EfficientNetV2B2 architecture used in this training process consists of 9,409,520 trainable parameters with a memory usage of 35.89 MB.

## 🧠 Modeling

The three neural network architectures prepared beforehand—custom CNN, VGG-19, and EfficientNetV2B2—were then trained using several training schemes. The model training process utilized a dataset that had undergone preprocessing steps, including labeling, splitting, and preprocessing. The images were then converted into numerical arrays with three channels (red, green, and blue) to match the input layer of the model architecture.

The loss function used during training was categorical crossentropy. Categorical crossentropy calculates the loss between the probability distribution predicted by the model and the actual probability distribution (true labels). This loss function is particularly well-suited for multi-class classification tasks when using the softmax activation function in the output layer. Softmax produces probability outputs that serve as input to the categorical crossentropy function. Softmax allows the model to predict class probabilities, while categorical crossentropy measures the prediction error, enabling both functions to work together to improve model accuracy. This loss function updates the model's weights during training to minimize prediction errors.

The primary evaluation metric used was accuracy, which is a common measure of a model's classification performance. Accuracy calculates the proportion of correct predictions out of the total predictions made by the model, providing a clear understanding of how well the model classifies data into the correct categories (authentic or counterfeit). Accuracy offers direct and easily interpretable feedback on the model’s ability to predict the correct labels and is often the key metric for evaluating classification models.

<p align="center">
  <img width="275" alt="image" src="https://github.com/user-attachments/assets/12391dac-288d-406b-8ea0-ebdc3169ca4c" />
  <br>
  <strong>Feedforward and backpropagation process flow</strong>
</p>

After the model is compiled, it is trained using the training and validation datasets. During this stage, the custom CNN, VGG-19, and EfficientNetV2B2 models learn from the data by adjusting the weights and biases in each layer through the feedforward and backpropagation processes.

During the feedforward process, input data—converted into numerical arrays with three channels (red, green, and blue)—is passed through the neural network layers to generate a predicted output. Each layer in the custom CNN, VGG-19, and EfficientNetV2B2 architectures processes the data sequentially through convolution, pooling, and fully connected layers to obtain the final prediction. This prediction is then compared to the actual labels using the categorical cross-entropy (CCE) loss function, which calculates the error or loss. The loss measures the difference between the model’s prediction and the expected outcome for a single sample, while the cost represents the average loss across all samples in a batch.

During backpropagation, this error is used to compute gradients for each weight in the network, which are then updated using the AdamW optimizer. This optimizer incorporates decoupled weight decay to prevent overfitting, allowing the custom CNN, VGG-19, and EfficientNetV2B2 models to learn effectively and achieve high classification accuracy.

The overall training configuration used for model development is summarized in the following table.

<p align="center">
  <img width="598" alt="image" src="https://github.com/user-attachments/assets/1e705808-2bf6-4468-acb1-28af57bc334b" />
  <br>
  <strong>Model training configuration</strong>
</p>

The table above outlines the training configuration applied in this development. The models were trained using the AdamW optimizer with a small learning rate of 1e-05. The chosen loss function was categorical cross-entropy, which is commonly used for multi-class classification tasks in combination with the softmax activation function in the output layer. The evaluation metric used was accuracy to assess model performance. The models were trained for a maximum of 1,000 epochs to ensure adequate convergence. To maintain consistency in data splitting and model training, a fixed seed value of 42 was applied.

### Callbacks

The model training process can leverage the use of callbacks to facilitate the storage of the best-performing model, halt training when necessary, and dynamically adjust the learning rate. In this development, three types of callbacks were utilized: Early Stopping, Model Checkpoint, and ReduceLROnPlateau.

#### Early Stopping

In this development, early stopping was implemented to halt the model training process if no significant improvement was observed in the specified evaluation metric. The primary goal of early stopping is to prevent overfitting and optimize training time. The configuration parameters for the early stopping callback are detailed in the following table.

<p align="center">
  <img width="598" alt="image" src="https://github.com/user-attachments/assets/8fa6e2c4-d69f-49bb-a481-9ace488eb292" />
  <br>
  <strong>Model training configuration</strong>
</p>

The table outlines the configuration of parameters used for the early stopping callback during model training. The monitor parameter specifies the metric to be observed throughout training to determine whether training should be stopped. Validation loss (val_loss) was chosen as the monitored metric, meaning that training would be halted if val_loss, or validation loss, failed to improve. This approach aligns with the study conducted by Li et al. (2024) in their paper, “Keeping Deep Learning Models in Check: A History-Based Approach to Mitigate Overfitting”, which emphasizes the use of validation loss curves to prevent overfitting in model training. Their research experimented with patience values ranging from 5 to 115 epochs and found that validation loss curves typically changed every 10 epochs on average. Based on these findings, the developer set the patience value to 10, allowing the model time to improve validation loss for 10 epochs before stopping the training process.

Additionally, the min_delta parameter was set to 0, ensuring that even minor improvements in validation loss were recognized as progress. This configuration allows the model to escape local minima by considering even small reductions in loss, which can be significant in the long run.

The verbose parameter was set to 1, meaning that detailed log outputs would be generated whenever early stopping occurred. This feature helps developers monitor and analyze the training process more effectively.

#### Model Checkpoint

In this development, Model Checkpoint was implemented to store the best-performing model during training based on specific criteria, in this case, validation loss. The Model Checkpoint mechanism automatically saves a copy of the model at a given epoch whenever an improvement in performance is detected. This ensures that the best model is preserved after training is completed or if training is prematurely stopped by early stopping.

By utilizing Model Checkpoint, developers can ensure that the final model used for evaluation and deployment is the most optimal version obtained throughout the training process. The complete configuration parameters for the Model Checkpoint callback are summarized in the following table.

<p align="center">
  <img width="598" alt="image" src="https://github.com/user-attachments/assets/8fa6e2c4-d69f-49bb-a481-9ace488eb292" />
  <br>
  <strong>Checkpoint model parameter configuration</strong>
</p>

The table outlines the configuration parameters for using the Model Checkpoint callback during model training.

- The filepath parameter specifies the directory or filename where the best-performing model will be saved. The naming convention is adjusted based on the model being trained. By setting a specific filepath that aligns with the model name, developers can ensure that the best-performing model version is stored with a relevant and easily identifiable name for further evaluation or deployment.

- The monitor parameter is set to validation loss, meaning the Model Checkpoint will track validation loss during training. Whenever validation loss improves (i.e., decreases), the newly trained model is saved. This is crucial because validation loss indicates how well the model generalizes to unseen data. Additionally, monitoring validation loss aligns with the early stopping callback, which uses the same monitoring parameter.

- The mode parameter is set to auto, allowing the Model Checkpoint to automatically select the appropriate evaluation mode based on the monitored metric. Since validation loss is being tracked, the mode will automatically switch to min, meaning that if the validation loss is lower than in previous epochs, the checkpoint will save the model for that epoch.

- The save_best_only parameter is set to True, ensuring that only the best-performing model is saved. This prevents unnecessary storage of models from epochs that do not show performance improvements, optimizing storage usage and focusing on models with the highest performance.

- Lastly, the verbose parameter is set to 1, meaning that the checkpoint process will provide real-time updates during training. In other words, developers will receive notifications whenever a new best-performing model is saved, allowing them to monitor progress and assess the effectiveness of the checkpointing strategy.

#### ReduceLROnPlateau

In this development, ReduceLROnPlateau is utilized to dynamically adjust the learning rate during training based on improvements in the evaluation metric. The configuration parameters for the ReduceLROnPlateau callback are detailed in the following table.

<p align="center">
  <img width="597" alt="image" src="https://github.com/user-attachments/assets/f4240458-ee4f-46ef-b123-9a8904bdefb6" />
  <br>
  <strong>ReduceLROnPlateau parameter configuration</strong>
</p>

The table presents the configuration parameters used in the ReduceLROnPlateau callback for dynamically adjusting the learning rate throughout the training process.

- The monitor parameter is set to validation loss, meaning that the learning rate will be reduced if no improvement is observed in validation loss. This choice aligns with the monitoring parameters used in the early stopping and model checkpoint callbacks. Additionally, validation loss is commonly used to regulate learning rates. A study by Mahesh et al. (2024) titled "Transformative Breast Cancer Diagnosis using CNNs with Optimized ReduceLROnPlateau and Early Stopping Enhancements" demonstrated that using validation loss for monitoring within a CNN architecture resulted in a classification model with 95.2% accuracy.

- The factor parameter is set to 0.5, meaning that if validation loss does not improve, the learning rate will be reduced to half of its previous value. This reduction helps prevent overly aggressive training that could cause the model to overshoot the optimal point, leading to instability in performance. The selection of this decay factor is also based on research by Zaheer et al. (2018) in their study "Adaptive Methods for Nonconvex Optimization", where they experimented with different optimizers using ReduceLROnPlateau across various batch sizes. Their findings indicate that a decay factor of 0.5 performs well in most cases, even when the learning rate reduction rate is 5 to 10 times higher.

- The patience parameter is set to 5, meaning that if validation loss does not improve for five consecutive epochs, the learning rate will be reduced based on the decay factor. In general, the choice of patience in ReduceLROnPlateau depends on the dataset size (Zaheer et al., 2018). Moreover, this value is chosen in relation to the early stopping patience value of 10. Using a lower patience value for ReduceLROnPlateau compared to early stopping allows the model to adjust the learning rate more quickly and provides an opportunity for the model to escape potential local minima before training is terminated.

- The min_lr parameter is set to 1e-8, ensuring that the learning rate does not drop below this threshold. This prevents excessively small learning rates, which could cause training to become too slow or stagnate.

- Lastly, the verbose parameter is set to 1, meaning that updates regarding learning rate adjustments will be displayed during training. This provides immediate feedback to developers, helping them analyze how frequently the learning rate changes throughout training and better understand the model's training dynamics.

### Hyperparameter Optimization with Grid Search Method

The model training was conducted using multiple training scenarios designed as part of the hyperparameter tuning process to select the optimal dataset parameters for Rupiah banknote authenticity identification modeling. The hyperparameter tuning process was performed manually, with the selection of the best model based on both identification performance and training time efficiency achieved across different training scenarios.

The optimal parameter selection was carried out using the grid search method. Grid search helps evaluate various hyperparameter combinations to determine the configuration that delivers the best results in terms of identification performance and training efficiency. The training scenarios and parameters used in grid search are detailed in the following table.

<p align="center">
  <img width="528" alt="image" src="https://github.com/user-attachments/assets/dc84e619-4dca-4f9e-a5d6-51ebc2bb9970" />
  <br>
  <strong>ReduceLROnPlateau parameter configuration</strong>
</p>

The table above presents various training scenarios used in the grid search process for model hyperparameter tuning. Each scenario involves a different combination of three key parameters: train-valid split, image size, and batch size.

- The train-valid split determines the proportion of data allocated for training and validation. Scenarios 1 to 6 use a 70:30 split, while scenarios 8 to 12 use an 80:20 split.
- The image size refers to the resolution of images processed during training, with values varying between 256, 448, and 512 pixels:
-- 256 pixels are used in scenarios 1, 7, and 13.
-- 448 pixels are applied in scenarios 3, 9, and 15.
-- 512 pixels are used in scenarios 5, 11, and 17.


## 📝 Evaluation & Analysis
