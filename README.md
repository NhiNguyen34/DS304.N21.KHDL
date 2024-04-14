# DS304.N21.KHDL

# Analysis of the Impact of Preprocessing Techniques on the Performance of Diabetic Retinopathy Image Classification

Diabetic retinopathy, a retinal disorder, affects up to 85% of diabetic patients, making its accurate diagnosis and early treatment crucial. Currently, various classification models yield promising evaluation results. However, the effectiveness of preprocessing techniques in diabetic retinopathy image classification remains unverified. This research addresses a gap in existing knowledge by investigating the impact of preprocessing on classification accuracy, potentially leading to the streamlining of current methods and eliminating unnecessary steps.

## Hypothesis Testing

Hypothesis testing is used to investigate the impact of preprocessing techniques, with both one-way and two-way ANOVA. The effectiveness of various preprocessing methods is assessed using Tukey’s HSD test as a follow-up to one-way ANOVA with repetitions.


## Preprocessing Techniques

In image classification tasks, including computer vision tasks in general, preprocessing plays a crucial role as it helps enhance available images, highlight image details and features, and can also improve model performance. Based on the diabetic retinopathy competition on Kaggle, the group decides to use three specific preprocessing methods:

1. **Without Preprocessing:** No specific preprocessing methods were used to avoid the risk of these techniques leading to worse results than normal. However, all images were resized to a fixed size of 224x224, which was used as the default size for all methods.

2. **Circle Crop:** This method involved removing black regions around the images that had little impact on the conclusions. Specifically, rows and columns that only contained pixel values less than 7 (the highest value to remove black regions) were removed to avoid the model’s conclusions based on black regions in the images.

3. **Ben Graham:** This preprocessing technique involved blending images between the original image and the original image processed with GaussianBlur. The parameters included Image1 (the original image), Image2 (the original image processed with GaussianBlur with a kernel size of (0, 0)), Alpha and beta (custom hyperparameters with values set by the author as 4 and -4, respectively), and Y (another hyperparameter used to bring the data to the desired value range).

## Experimental Models

We conducted experiments using both Deep Learning and Machine Learning models to provide the most objective conclusions:

- **KNN (K-Nearest Neighbors):** A supervised machine learning algorithm used for classification and prediction based on the principle of ’nearest neighbors.’

- **SVC (Support Vector Machine):** A supervised machine learning model used in classification tasks. It creates the best hyperplane to separate two classes of data.

- **Random Forest:** A supervised machine learning algorithm used for classification and prediction. It is an ensemble of multiple decision trees.

- **CNN (Convolutional Neural Network):** A type of neural network used in image processing and analysis. It automatically learns features from images and is commonly used in classification tasks.

- **ResNet-18:** A CNN architecture proposed by Kaiming He, effective for handling classification and image recognition tasks.

- **VGG-16:** A CNN architecture proposed by Karen Simonyan and Andrew Zisserman, known for its excellent performance in image classification tasks.

## Evaluation Metric

For the classification task, the F1-scoremicro was used as the evaluation metric, calculated using True Positive (TP), False Positive (FP), and False Negative (FN).

## Datasets

The datasets used in the experiments are APTOS, collected through the Asian Pacific Tele-Ophthalmology Society (APTOS) Diabetic Retinopathy Detection competition, and Messidor-2. These datasets are popular for diabetic retinopathy detection and contain images with labels ranging from 0 to 4, representing increasing levels of disease severity.

## Results

The classification performance of the models varied unevenly. Deep learning models generally showed increased or unchanged performance when applying preprocessing techniques, while traditional machine learning models showed varying changes, with more instances of performance reduction.

## Contact

For any inquiries or feedback regarding the dataset, you can contact us at [].
Authors:
- Nhi Ngoc-Yen Nguyen: [21521231@gm.uit.edu.vn](mailto:21521231@gm.uit.edu.vn)
- Liu The Hien
- Nguyen Duc Anh


