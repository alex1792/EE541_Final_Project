# 1. Model Details
We trained and evaluated four different models: ResNet18, ResNet34, ResNet50, MobileNetV2 in this project to compare their performance.
## Model date
December 2024
## Model type
CNN model
## Model version
1. ResNet18: 11,191,389 Total Parameters
2. ResNet34: 21,299,549 Total Parameters
3. ResNet50: 23,567,453 Total Parameters
4. MobileNetV2: 2,261,021 Total Parameters

# 2. Model Use
Currently, we developed the full training and evaluation process. In the future, we plan to develop real-time model interpretation api. By now, if you want to execute the training and evaluation, please follow the following steps.

## Environment
1. Execute the .ipynb code on Google Colab
2. Ensure GPU runtime is enabled for optimal performance

## Data Preparation
1. Download the required dataset from Kaggle
2. Compress the dataset into a file named ‘dataset.zip’

## Data Storage
1. Upload ‘dataset.zip’ to your Google Drive
2. Place the file into the directory ‘/EE541_Final_Project/’

## Execution
1. Open the .ipynb file in Google Colab
2. Run the code cell sequentially

# 3. Data, Performance, Limitations
## Data
The model is trained on the ASL Alphabet dataset, which consists of:
1. 29 classes: 26 alphabets (A to Z), 'delete', 'space', and 'nothing'
2. 87,000 images in total (3,000 images per class)
3. Image dimensions: 200 x 200 pixels

## Dataset Characteristic
Includes images with varying brightness, angles, and scales
All training images are based on right-handed signers
Minimal preprocessing required due to inherent diversity in the dataset
## Performance
1. ResNet18: 99.92% accuracy, average runtime 423.69 ms
2. ResNet34: 100% accuracy, average runtime 691.03 ms
3. ResNet50: 100% accuracy, average runtime 1556.85 ms
4. MobileNetV2: 99.85% accuracy, average runtime 671.41 ms
## Limitations
1. Static Image Constraints:
The current model has only been tested and validated on static input images.
Comprehensive evaluation in real-time, dynamic environments has not yet been conducted.
2. Dataset Diversity:
The original dataset lacked left-handed gesture images, potentially leading to bias in recognition for left-handed individuals.
While data augmentation partially addressed this issue, the full diversity of real-world scenarios may not be completely covered.
3. Limited Impact of Grayscale Processing:
Experiments showed that grayscale processing of images had limited effect on improving model performance.
This may be due to the model already achieving high accuracy, leaving little room for further improvement.
4. Real-time Application Challenges:
Although ResNet18 performs excellently in execution time, additional challenges may arise in real-world real-time applications.
Further validation is needed for the model's performance in continuous gesture recognition and real-time video stream processing.
5. Ongoing Improvement in Generalization Ability:
Despite enhanced generalization through data augmentation, further optimization may be necessary for a wider range of practical application scenarios.
Particularly, recognition capabilities under non-standard gestures, different backgrounds, and lighting conditions may need improvement.
6. ASL-Specific Limitations:
The model is specifically trained for American Sign Language (ASL) and may not be applicable to other sign language systems.
Its application in cross-cultural or multilingual environments may be limited.

# 4. References
[1] [Real-time Object Detection and Classification for ASL alphabet](https://cs231n.stanford.edu/reports/2022/pdfs/147.pdf)

[2] [Sign Language Recognition Based on Computer Vision](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9844497)

[3] [ASL Alphabet dataset](https://www.kaggle.com/datasets/grassknoted/asl-alphabet/data?select=asl_alphabet_train)

[4] [Handedness prevalence in the deaf: Meta-Analysis](https://www.sciencedirect.com/science/article/pii/S0149763415302189)
