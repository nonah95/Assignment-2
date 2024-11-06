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


![P3](https://github.com/user-attachments/assets/7ff23415-d450-4355-99c7-2eba543a4327)


## Part 2: AI for Data Visualization Techniques in Computational Biology

#Part 1: MNIST dataset 

![MNIST](https://github.com/user-attachments/assets/851add21-43c9-4528-8ef7-640566385f97)

#Part 2: Yolo Model for my Picture 

![Nona Pic](https://github.com/user-attachments/assets/699d4ecf-8648-4ba5-808a-879e759c5ab1)


