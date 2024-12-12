# EE541_Final_Project - CV for American Sign Language - Interpretation of Sign Language


Members: Yu-Hsin Wu (USC ID: 3434391900), Yu-Hung Kung (USC ID: 3431428440)


Dataset: [ASL_Alphabet](https://www.kaggle.com/datasets/grassknoted/asl-alphabet)


Execution Environment: Google Colab, with Nvidia L4 GPU

GitHub Link: https://github.com/alex1792/EE541_Final_Project

## Introduction
This project aims to train and evaluate models for interpreting the American Sign Language (ASL) alphabet using the ASL Alphabet dataset. We trained and compared four different convolutional neural network models: ResNet18, ResNet34, ResNet50, and MobileNetV2. The dataset comprises 87,000 images across 29 classes, with 3,000 images per class.

## Dataset Description
The ASL Alphabet dataset contains high-quality images of hand gestures representing the 26 letters of the English alphabet, plus three additional classes (likely "space", "delete", and "nothing"). Each image is a color photograph of a hand forming a specific ASL letter sign against various backgrounds.

## Methodology
We selected four popular CNN architectures for this image classification task:
ResNet18, ResNet34, ResNet50: These Residual Networks of varying depths are known for their ability to train very deep networks effectively.
MobileNetV2: A lightweight model designed for mobile and embedded vision applications, offering a good balance between accuracy and computational efficiency.
We trained each model on the dataset and compared their performance in terms of accuracy and computational requirements.

## How to Run the Code
1. Open the .ipynb file using Google Colab.
2. Download the dataset from Kaggle and compress it into a file named 'dataset.zip'.
3. Upload 'dataset.zip' to your Google Drive under the path '/EE541_Final_Project/'.
4. Ensure you are using a GPU runtime in Google Colab.
5. Execute the .ipynb code in Google Colab.

## Results and Discussion
Our analysis of the four CNN models for ASL alphabet recognition yielded impressive results, with all models achieving over 99% accuracy. However, significant differences were observed in their execution times, primarily due to variations in network architecture and the number of parameters:

1. ResNet18: This model demonstrated the fastest execution time while maintaining high accuracy. Its relatively shallow architecture allows for quick training and inference without compromising performance.
2. ResNet34: Performed similarly to ResNet18 in terms of accuracy but with a slightly longer execution time due to its deeper structure.
3. MobileNetV2: Despite being designed for mobile applications, this model achieved comparable accuracy to the ResNet variants. Its execution time fell between ResNet18 and ResNet34, showcasing its efficiency.
4. ResNet50: While achieving high accuracy, this model had the longest execution time among the four. Its deep architecture, while powerful, comes at the cost of increased computational requirements.

The high accuracy across all models suggests that the ASL alphabet recognition task can be effectively solved with various CNN architectures. However, the trade-off between accuracy and execution time becomes apparent, especially when considering deployment scenarios.
ResNet18 emerges as the most balanced option, offering the best combination of high accuracy and low execution time. This makes it particularly suitable for real-time applications or scenarios with limited computational resources.

As for space complexity, we have preserved 4 trained models, the following are sizes of different models:
1. ResNet18: 42.8MB
2. ResNet34: 81.4MB
3. ResNet50: 90.2MB
4. MobileNetV2: 8.9MB

For a more comprehensive analysis, including detailed performance metrics, confusion matrices, and further insights, please refer to the EE_541_Final_Report.pdf.

## Future Work
We expect that future systems will be able to capture gestures via a real-time camera, recognize them immediately, and display the results on the screen. This application allows people who do not understand ASL to quickly understand the meaning of ASL gestures and reduce communication barriers between the two parties.


## References
[1] [Real-time Object Detection and Classification for ASL alphabet](https://cs231n.stanford.edu/reports/2022/pdfs/147.pdf)

[2] [Sign Language Recognition Based on Computer Vision](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9844497)

[3] [Handedness prevalence in the deaf: Meta-Analysis](https://www.sciencedirect.com/science/article/pii/S0149763415302189)

[4] [ASL Alphabet dataset](https://www.kaggle.com/datasets/grassknoted/asl-alphabet/data?select=asl_alphabet_train)


