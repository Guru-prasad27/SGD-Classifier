# SGD-Classifier
## AIM:
To write a program to predict the type of species of the Iris flower using the SGD Classifier.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1. Load & preprocess data
Import Iris dataset, extract features (X) and labels (y), then normalize using StandardScaler.

2. Split dataset
Divide into training and testing sets with train_test_split (80% train, 20% test).

3. Initialize classifier
Create SGDClassifier with max_iter=1000 and fixed random_state.

4. Train & predict
Fit model on training data, then predict outcomes on test data.

5. Evaluate performance
Compute accuracy and generate classification report (precision, recall, F1‑score).
```

## Program:
```
/*
Program to implement the prediction of iris species using SGD Classifier.
Developed by:Guru Prasad DR 
RegisterNumber:  212225040104

from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.linear_model import SGDClassifier
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import accuracy_score, classification_report

iris = load_iris()
X = iris.data
y = iris.target

scaler = StandardScaler()
X = scaler.fit_transform(X)

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

model = SGDClassifier(max_iter=1000, random_state=42)

model.fit(X_train, y_train)

y_pred = model.predict(X_test)

print("Accuracy:", accuracy_score(y_test, y_pred))

print("\nClassification Report:\n", classification_report(y_test, y_pred))

*/
```

## Output:
<img width="661" height="275" alt="image" src="https://github.com/user-attachments/assets/a7efc9b9-14f6-411c-a5ff-ee4882adc161" />



## Result:
Thus, the program to implement the prediction of the Iris species using SGD Classifier is written and verified using Python programming.
