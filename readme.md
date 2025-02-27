
Overview
This project focuses on predicting the presence or absence of heart disease based on patient data. We use a neural network model to classify the data. The dataset contains multiple features about patients, and the goal is to train a machine learning model to predict whether or not a patient has heart disease.

Dataset
The dataset used in this project is the Cleveland Heart Disease Dataset from the UCI Machine Learning Repository. The dataset contains information on various attributes related to heart disease diagnosis.

Dataset Details
Source: UCI Machine Learning Repository
URL: Heart Disease Dataset
Number of Features: 13
Classes: 5 (0 = no disease, 1 = mild disease, 2 = moderate disease, 3 = severe disease, 4 = very severe disease)
Attributes:
age: Age of the patient (years)
sex: Gender of the patient (1 = male, 0 = female)
cp: Chest pain type (1-4)
trestbps: Resting blood pressure (mm Hg)
chol: Serum cholesterol level (mg/dl)
fbs: Fasting blood sugar > 120 mg/dl (1 = true, 0 = false)
restecg: Resting electrocardiographic results (0-2)
thalach: Maximum heart rate achieved (bpm)
exang: Exercise induced angina (1 = yes, 0 = no)
oldpeak: ST depression induced by exercise relative to rest
slope: Slope of the peak exercise ST segment (1-3)
ca: Number of major vessels colored by fluoroscopy (0-3)
thal: Thalassemia (3 = normal, 6 = fixed defect, 7 = reversible defect)
class: Diagnosis (0 = no disease, 1-4 = disease severity)
Approach
1. Data Preprocessing
Missing Data: We handled missing data, represented by "?", by dropping rows containing these entries.
Feature Scaling: We used standard scaling to normalize numerical inputs to improve model performance.
Categorical Conversion: The target variable (class) was one-hot encoded to convert it into a format suitable for categorical classification tasks.
2. Model Building
We used a neural network to solve the classification problem. The architecture of the model includes:

Input Layer: Accepts the features from the dataset.
Hidden Layers: Two hidden layers with 128 and 64 neurons, using ReLU activation.
Output Layer: A softmax layer for multi-class classification, predicting the class label (heart disease severity).
Optimizer: Adam optimizer with a learning rate of 0.001.
Loss Function: Categorical Cross-Entropy to handle multi-class classification.
3. Model Training
The model was trained using the training dataset (80% of the total data). We used 100 epochs with a batch size of 10 for training. The model was evaluated based on accuracy during training.

4. Binary Classification Model
To improve the model, we simplified the problem by converting it into a binary classification problem (heart disease or no heart disease). This change made it easier for the model to learn patterns and improved accuracy.

5. Evaluation
The model was evaluated using both:

Categorical Model: Using the multi-class classification approach (0 to 4 classes).
Binary Model: Using the simplified binary classification approach (heart disease or no heart disease).
We calculated metrics such as:

Accuracy
Precision
Recall
F1-Score
Results were evaluated using the test set (20% of the total data).

Results
Categorical Model:
The accuracy for the categorical model (predicting all classes) was XX%.

Classification Report for Categorical Model:
Precision: XX%
Recall: XX%
F1-Score: XX%
Binary Model:
The accuracy for the binary model (predicting heart disease or no disease) was YY%.

Classification Report for Binary Model:
Precision: YY%
Recall: YY%
F1-Score: YY%
Key Observations:
The binary classification approach provided better results, as distinguishing between the presence or absence of heart disease is a simpler problem compared to differentiating between various severity levels.
The model showed strong performance with both models, though the binary classification approach outperformed the multi-class model.#   A t h e n a - E d u c a t i o n - A s s e s s m e n t  
 