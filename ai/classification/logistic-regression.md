****
### Terms
- Logistic regression intuition

[code](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/classification/codes/logistic_regression.ipynb)

# Logistic Regression Intuition
![image](https://user-images.githubusercontent.com/39285147/178243846-cc55ba03-7e5a-4d35-a749-892fdaeacc87.png)

선형 회귀는 *이상치*를 분류하지 못한다. 따라서, 이 회귀선을 변형하여(i.e., sigmoid) 데이터가 어떤 범주에 속할 확률을 0에서 1 사이의 값으로 예측하고 그 확률에 따라 가능성이 더 높은 **범주**에 속하는 것으로 분류해주는 SL 알고리즘이다.
- 결과가 **범주형**일 때 사용

**이상치*: [0, 1] 범위 밖)

## Find probability
![image](https://user-images.githubusercontent.com/39285147/178244899-b471eaee-f5cf-48eb-8782-6f718cf832e1.png)

## Make prediction
![image](https://user-images.githubusercontent.com/39285147/178245232-13193093-4276-47d4-9256-f7fc57ac1d79.png)

# Confusion Matrix
범주화 유형 측정법
