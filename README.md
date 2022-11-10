# Group9_MachineLearningHC

## Model Ensemble

### Introduction

model ensemble is a method to get a better result from the voting of a group of model, therefore we must ensure the models are using the same training and testing set.

### Step
1. Ensure the code in the branch is the latest version (we had updated the code and dataset)

2. run the "HCTech.ipynb" code until completing the following block
```
X_train.to_csv('train_binary_x.csv', index=False)
y_train.to_csv('train_binary_y.csv', index=False)
X_test.to_csv('test_binary_x.csv', index=False)
y_test.to_csv('test_binary_y.csv', index=False)
```
*This block save the data to the current directory, you can change its path.

3. Use 'train_binary_x.csv' and 'train_binary_y.csv' to train the model (decision tree, random forest, MLP, perceptron, DNN or anything)
*You can adjust the thing used to change (ex: using SMOTE) but ensure to start with these specific file.

4. Use 'test_binary_x.csv' to test the model, DO NOT use 'test_binary_y.csv' to evaluate it.

5. Output the answer as the following format.
*Do not change the order of the 'test_binary_x.csv'
```
index, score
0, 1.8863079276343342e-06
1, 1.0374536032031756e-05
2, 5.440356289909687e-06
3, 0.7755006551742554
4, 1.4836804439255502e-05
5, 1.5318420992116444e-05
6, 3.7484101085283328e-06
7, 2.6681723284127656e-06
8, 6.323603156488389e-05
9, 3.993187874584692e-06
10, 3.346433231854462e-06
11, 3.931617357011419e-06
```
The first line should be written as 'index, score\n'
The first column should be the index of the testing data.
The seconf column should be ==the probility of having a birth (predict 1)==

6. Save the answer as the format of "result-{method}-{accuracy_of_training_data}.txt"
ex: result-RandomForest-0.954321.txt, result-DNN_SMOTE-0.954321.txt
*accuracy_of_training_data should be with at least six decimal places

