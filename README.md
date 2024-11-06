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


## Part 2: AI for Data Visualization Techniques in Computational Biology

#Part 1: MNIST dataset 

![MNIST](https://github.com/user-attachments/assets/851add21-43c9-4528-8ef7-640566385f97)

#Part 2: Yolo Model for my Picture 

![Nona Pic](https://github.com/user-attachments/assets/699d4ecf-8648-4ba5-808a-879e759c5ab1)


