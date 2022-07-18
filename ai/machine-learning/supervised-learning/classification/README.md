# ML Classification models
## 강의 목차
### [Logistic Regression](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/supervised-learning/classification/logistic-regression.md)
### [K-Nearest Neighbors (K-NN)](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/supervised-learning/classification/knn.md)
### [Support Vector Machine (SVM)](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/supervised-learning/classification/svm.md)
### [Kernel SVM](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/supervised-learning/classification/kernel-svm.md)
### [Naive Bayes](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/supervised-learning/classification/naive-bayes.md)
### [Decision Tree Classification](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/supervised-learning/classification/decision-tree.md)
### [Random Forest Classification](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/supervised-learning/classification/random-forest.md)
### [분류 모델 성능 평가](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/supervised-learning/classification/performance-of-classifiers.md)
### [Pros and Cons of Classification](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/supervised-learning/classification/Classification_Pros_Cons.pdf)

## Performance: Classifiers
**모든 모형 다 테스트 후 최적 모델 선정하여야 하나**, ~~일반적으로는 아래 성능을 따른다 (overfitting 등 여러 변수 제외).~~

~~- Logistic < Naive Beyas = SVM(선형) < Decision Tree = Random Forest < KNN = Kernel SVM(비선형)~~

## Linear vs. Non-linear
![image](https://user-images.githubusercontent.com/39285147/178288426-588c6cdd-2a2f-45f3-86db-00f4dcc71b7f.png)

### 선형 (해석)
선형결합에서 가중치가 선형 관계인 경우
- 분류 결과의 decision boundary가 비선형 일수도 있다.
#### 분류기
- Linear regression
- Logistic regression
- SVM (선형)

### 비선형 (예측)
데이터를 어떻게 변형하더라도 파라미터를 선형 결합식으로 표현할 수 없는 모델
#### 분류기
- KNN
- kernel SVM (비선형)
  - RBF
  - Polynomial Kernel
  - Sigmoid Kernel
- Naive Beyas
- Decision tree
- Random forest
