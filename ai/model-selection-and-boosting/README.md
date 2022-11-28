# Model Selection and Boosting
## 강의 목차
### [Model Selection](#Model-Selection-Methods)
### [About XGBoost](#XGBoost)

## Model Selection
ML 모델을 최상의 방법으로 평가하기 위한 **k-fold 교차 검증**과 하이퍼 피라미터의 최고값을 찾는 **피라미터 조정**을 배운다.

### 학습 목표
- How to deal with the bias variance tradeoff when building a model and evaluating its performance?
- How to choose the optimal values for the hyperparameters (the parameters that are not learned)?

### [k-Fold Cross Validation](https://github.com/hchoi256/ai-terms/blob/main/README.md)
![image](https://user-images.githubusercontent.com/39285147/180011204-6c4dc19a-67d9-4e3f-977f-18096de6639a.png)
![image](https://user-images.githubusercontent.com/39285147/180012732-6950390a-bfe1-4ac5-90f8-8be829be29be.png)

[code](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/model-selection-and-boosting/k_fold_cross_validation.ipynb)

특정 숫자의 훈련 테스트 폴드를 생성하는 것으로, 가령 10개의 훈련 테스트 폴드라면 각 훈련 폴드로 훈련을 하고 동시에 테스트 폴드에서 따로 테스트한다. 잔차제곱을 Confusion Matrix를 사용하여 표현한 정확도보다 더 신빙성있는 수치를 배출한다.

### [Grid Search](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/model-selection-and-boosting/grid_search.ipynb)
![image](https://user-images.githubusercontent.com/39285147/180014865-4c77da81-587b-4aee-b1df-6ec3fd9fb9ea.png)

어떤 모델이든 훈련되지 않은 하이퍼 피라미터의 최적값을 찾는 방법으로, 훈련 데이터만을 대상으로 수행한다.

## [XGBoost](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/model-selection-and-boosting/xg_boost.ipynb)
![image](https://user-images.githubusercontent.com/39285147/180016227-f64de04a-f582-49f9-a675-698dd5713359.png)

XGBoost는 회귀와 분류 둘다 적용될 수 있고 [*캐글대회*](https://m.hanbit.co.kr/channel/category/category_view.html?cms_code=CMS7895414616)에서 압도적 승리를 거머줬을 정도로 타모델에 비해 지극히 강력한 성능을 자랑한다.

### Process
- Importing the libraries
- Importing the dataset
- Splitting the dataset into the Training and Test set
- Training XGBoost on the Training set
- Making the confusion matrix
- Applying k-fold Cross-Validation
