
# Regression

## [Simple Linear Regression](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/regression/simple_linear_regression.ipynb)

![image](https://user-images.githubusercontent.com/39285147/177331908-96267c1b-82d3-4b76-929d-fa9ca6c6e7d1.png)

### Libraries
- *from sklearn.linear_model import LinearRegression*

## [Multiple Linear Regression](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/regression/multiple_linear_regression.ipynb)
![image](https://user-images.githubusercontent.com/39285147/177505039-04e82862-8af1-4dab-b4b7-0e20887b1d37.png)

### 5 Methods of Building Models
- All-in
- Backward Elimination
- Forward Selection
- Bidirectional Elimination
- Score Comparison


## [Polynomial Linear Regression](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/regression/polynomial_regression.ipynb)
![image](https://user-images.githubusercontent.com/39285147/177683114-a22d28b0-6b99-4c34-b4e8-f56f25fabaf3.png)
![image](https://user-images.githubusercontent.com/39285147/177683119-265fc600-7486-43b6-bdaa-50109a305ae8.png)


## [SVR](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/regression/support_vector_regression.ipynb)
![image](https://user-images.githubusercontent.com/39285147/177983301-baaa9147-5d0f-4c06-ac85-dd31f8715ec8.png)

SVR은 데이터에 노이즈가 있다고 가정하며, 적정 범위(2ϵ) 내에서는 실제값과 예측값의 차이를 허용한다
- Feature scaling O
- 회귀선: [하한선, 상한선]
  - 튜브 내에 실제 값이 있다면, 예측값과 차이가 있더라도 용인해주기 위해 penalty를 0
  - 튜브 밖에 실제 값이 있다면, penalty를 부여하게 됩니다.


## [Decision Tree Regression](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/regression/decision_tree_regression.ipynb)
- No need for feature scaling
![image](https://user-images.githubusercontent.com/39285147/177811894-12312896-240c-45a1-aa4a-9f9a0c101285.png)
![image](https://user-images.githubusercontent.com/39285147/177811933-8e0ecf5a-6830-464a-ac64-dffcf16ab5bb.png)


## [Random Forest Regression](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/regression/random_forest_regression.ipynb)
- No need for feature scaling
- Multiple combinations of DMTs

### 랜덤 포레스트의 장점
- Classification(분류) 및 Regression(회귀) 문제에 모두 사용 가능
- Missing value(결측치)를 다루기 쉬움
- 대용량 데이터 처리에 효과적
- 모델의 노이즈를 심화시키는 Overfitting(오버피팅) 문제를 회피하여, 모델 정확도를 향상시킴
- Classification 모델에서 상대적으로 중요한 변수를 선정 및 Ranking 가능

## Note

### [Regression Models: Pros and Cons](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/regression/Regression_Pros_Cons.pdf)

### Implemenetation
-	Importing the librarires
-	Importing the dataset
-	Splitting the dataset into the Training set and Test set
-	Training the Simple Linear Regression model on the Training set
-	Predicting the Test set results
-	Visualising the Training set results
-	Visualising the Test set results

### Encoder
- **OneHotEncoder**
  - Categorical data w/o order
- **LabelEncoder**
  - Categorical data w/ order
  - 
![image](https://user-images.githubusercontent.com/39285147/177999210-181b42ea-927c-4968-a36f-145902eaeefa.png)
- 트리 모델은 스케일링 필요 없다.
