# Assignment-2
Nano706
This is assignment #2

## Part 1: AI for Modeling Molecular Reactions, Biological Systems, Mechanisms, its Regulation, Cell Growth

#Part 1: Visualizing the data 

I visualize a wine quality dataset using a scatter plot to show the relationship between two variables, "Alcohol" and "Malic Acid," and their association with wine quality. 

- **Figure Setup**: `plt.figure(figsize=(10, 6))` specifies the plot size.
- **Scatter Plot**: `plt.scatter(...)` plots "Alcohol" on the x-axis and "Malic Acid" on the y-axis, with colors representing wine quality.
- **Title and Labels**: `plt.title`, `plt.xlabel`, and `plt.ylabel` set the title and axis labels.
- **Color Bar**: `plt.colorbar(...)` adds a color bar to indicate the quality scale.
- **Display Plot**: `plt.show()` renders the plot.
  
- In the next section of this part: 
- **Standardize Features**: Use `StandardScaler()` from `sklearn` to standardize the dataset, ensuring each feature has a mean of 0 and standard deviation of 1.
- **Fit and Transform**: `scaler.fit_transform(X)` standardizes the features in `X`, outputting a scaled version stored in `X2`.

![P1](https://github.com/user-attachments/assets/be3947d1-3e06-4cd7-be0d-b722a552a444)

#Part 2: Split the Data 

Here’s a description of the data-splitting code:

- **Split the Data**: Use `train_test_split` to divide the dataset into training and testing sets, enabling model evaluation.
- **Training and Testing Sets**: 
  - `X_train`, `X_test`: Feature subsets for training and testing.
  - `y_train`, `y_test`: Target subsets for training and testing.
- **Parameters**:
  - **`test_size=0.3`**: Allocates 30% of the data for testing.
  - **`random_state=42`**: Ensures reproducibility by setting a fixed random seed.
  
![P2](https://github.com/user-attachments/assets/0b96ac8d-6174-4a38-977e-e25c1353324d)


#Part 3: Decision Tree & Logistic Regression Model - SVM

![P3](https://github.com/user-attachments/assets/7ff23415-d450-4355-99c7-2eba543a4327)

The description of each model's training, prediction, and evaluation process:

### SVM Model
- **Train the SVM Model**: Instantiate `SVC` with a linear kernel, and train it on the training data.
  ```python
  svm = SVC(kernel='linear')
  svm.fit(X_train, y_train)
  ```
- **Make Predictions**: Use the trained SVM model to predict the test set labels.
  ```python
  y_pred = svm.predict(X_test)
  ```
- **Evaluate the Model**: Calculate the accuracy of the SVM model on the test set.
  ```python
  accuracy_svm = accuracy_score(y_test, y_pred)
  print(f"Accuracy of the SVM model: {accuracy_svm:.2f}")
  ```

### Decision Tree Model
- **Train the Decision Tree Model**: Instantiate `DecisionTreeClassifier` and fit it to the training data.
  ```python
  tree = DecisionTreeClassifier()
  tree.fit(X_train, y_train)
  ```
- **Make Predictions**: Use the trained Decision Tree model to predict the test set labels.
  ```python
  y_pred_tree = tree.predict(X_test)
  ```
- **Evaluate the Model**: Calculate the accuracy of the Decision Tree model on the test set.
  ```python
  accuracy_tree = accuracy_score(y_test, y_pred_tree)
  print(f"Accuracy of the Decision Tree model: {accuracy_tree:.2f}")
  ```

### Logistic Regression Model
- **Train the Logistic Regression Model**: Instantiate `LogisticRegression` with a specified maximum iteration count and train it on the data.
  ```python
  log_reg = LogisticRegression(max_iter=1000)
  log_reg.fit(X_train, y_train)
  ```
- **Make Predictions**: Use the trained Logistic Regression model to predict the test set labels.
  ```python
  y_pred_log_reg = log_reg.predict(X_test)
  ```
- **Evaluate the Model**: Calculate the accuracy of the Logistic Regression model on the test set.
  ```python
  accuracy_log_reg = accuracy_score(y_test, y_pred_log_reg)
  print(f"Accuracy of the Logistic Regression model: {accuracy_log_reg:.2f}")
  ```


## Part 2: AI for Data Visualization Techniques in Computational Biology

#Part 1: MNIST dataset 

![MNIST](https://github.com/user-attachments/assets/851add21-43c9-4528-8ef7-640566385f97)

Here’s a structured explanation of training and evaluating these classifiers:

### Random Forest Classifier
- **Train the Random Forest Classifier**: Instantiate `RandomForestClassifier` with 100 trees and a random seed, then train it on the training data.
  ```python
  rf_classifier = RandomForestClassifier(n_estimators=100, random_state=42)
  rf_classifier.fit(X_train, y_train)
  ```
- **Make Predictions**: Use the trained Random Forest model to predict the test set labels.
  ```python
  y_pred_rf = rf_classifier.predict(X_test)
  ```
- **Evaluate the Model**: Calculate and print the accuracy of the Random Forest model on the test set.
  ```python
  accuracy_rf = accuracy_score(y_test, y_pred_rf)
  print(f"Random Forest Accuracy: {accuracy_rf * 100:.2f}%")
  ```

### Logistic Regression Classifier
- **Train the Logistic Regression Classifier**: Initialize `LogisticRegression` with a maximum iteration of 1000 and a fixed random seed, then fit it to the training data.
  ```python
  logistic_classifier = LogisticRegression(max_iter=1000, random_state=42)
  logistic_classifier.fit(X_train_scaled, y_train)
  ```
- **Make Predictions**: Use the trained Logistic Regression model to predict the test set labels.
  ```python
  y_pred_logistic = logistic_classifier.predict(X_test_scaled)
  ```
- **Evaluate the Model**: Calculate and print the accuracy of the Logistic Regression model on the test set.
  ```python
  accuracy_logistic = accuracy_score(y_test, y_pred_logistic)
  print(f"Logistic Regression Accuracy: {accuracy_logistic * 100:.2f}%")
  ```

### MLP (Neural Network) Classifier
- **Train the MLP Classifier**: Initialize `MLPClassifier` with 100 hidden units, a maximum iteration of 500, and a fixed random seed, then fit it to the training data.
  ```python
  mlp = MLPClassifier(hidden_layer_sizes=(100,), max_iter=500, random_state=42)
  mlp.fit(X_train_scaled, y_train)
  ```
- **Make Predictions**: Use the trained MLP model to predict the test set labels.
  ```python
  y_pred_mlp = mlp.predict(X_test_scaled)
  ```
- **Evaluate the Model**: Calculate and print the accuracy of the MLP model on the test set.
  ```python
  accuracy_mlp = accuracy_score(y_test, y_pred_mlp)
  print(f"MLP Accuracy: {accuracy_mlp * 100:.2f}%")
  ```

### Summary of Accuracy Results
- Print the accuracy results for each model for easy comparison.
  ```python
  print(f"Logistic Regression Accuracy: {accuracy_logistic * 100:.2f}%")
  print(f"Random Forest Accuracy: {accuracy_rf * 100:.2f}%")
  print(f"MLP Accuracy: {accuracy_mlp * 100:.2f}%")
  ```

#Part 2: Yolo Model for my Picture 

![Nona Pic](https://github.com/user-attachments/assets/699d4ecf-8648-4ba5-808a-879e759c5ab1)

Here's a step-by-step description to guide you in uploading, resizing, and detecting faces using the YOLO model in a Jupyter Notebook:

### Step 1: Upload and Open the Image
1. Define the image path.
2. Open the image using PIL (Python Imaging Library).

   ```python
   from PIL import Image
   import numpy as np
   import matplotlib.pyplot as plt

   # Path to your image
   img_path = '/content/Nona.jpg'
   image = Image.open(img_path)
   ```

### Step 2: Resize the Image
1. Resize the image to specified dimensions (e.g., 888x688).
   
   ```python
   # Resize the image
   resized_image = image.resize((888, 688))
   ```

### Step 3: Convert Image to Array
1. Convert the resized image to a NumPy array for processing with YOLO.

   ```python
   # Convert resized image to array
   img_array = np.array(resized_image)
   ```

### Step 4: Perform Face Detection with YOLO
1. Pass the image array through the YOLO model to detect faces.
   
   ```python
   # Perform inference
   results = model(img_array)
   ```

### Step 5: Display Results with Detections
1. Use the model’s `show()` function to display the detections on the image.

   ```python
   # Show results with detections
   results.show()
   ```

### Step 6: Optional - Display the Resized Image without Detections
1. Display the resized image without detections for comparison.

   ```python
   # Display the resized image
   plt.imshow(resized_image)
   plt.axis('off')
   plt.title('Resized Image')
   plt.show()
   ```

These steps will allow you to upload, resize, and detect faces in your photo using the YOLO model. Make sure the YOLO model is correctly loaded as `model` before running these steps.


