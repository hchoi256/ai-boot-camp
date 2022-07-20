# PCA
![image](https://user-images.githubusercontent.com/39285147/179999103-280543fd-a85b-4c43-ba31-36416aa6e783.png)

[code](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/machine-learning/unsupervised-learning/pca/principal_component_analysis.ipynb)

## Two Types of PCA
- **변수 선택(Feature Selection)** : 있는 변수 중 결과값을 잘 표현할 수 있는 변수를 (있는 변수들 중에서) 단순히 고르는 것

- **변수 추출(Feature Extraction)** : 변수들을 조합해 새로운 변수를 만들어 결과값을 잘 표현하는 방법

## Goal
값을 예측하는 선형회귀와 다르게 PCA는 X와 Y값 사이의 관계를 학습하는 것을 시도하고 주축 목록을 찾아낸다.

Reduce the dimensions of a d-dimensional dataset by projecting it onto a (k)-dimensional subspace (where k<d)
- Identify patterns in data
- Detect the correlation between variables

## Process
- Standardize the data
- Obtain the Eignevectors and Eigenvalues from the covariance matrix or correlation matrix, or perform Singular Vector Decomposition
- Sort eigenvalues in descending order and choose the k eigenvectors that correspond to the k largest eigenvalues where k is the number of dimensions of the new feature subspace (k<=d)
- Construct the projection matrix W from the selected k eigenvectors
- Transform the original dataset X via W to obtain a k-dimensional feature subspace Y

## 장단점
장점
- PCA를 사용하면 다중공선성 문제, 차원의 저주 문제를 해결할 수 있고, 차원을 축소해주기때문에 사람이 쉽게 관찰하고 이해할 수 있는 2차원으로 데이터들을 보여줄 수 있다.

단점
- 아웃라이어에 굉장히 영향을 많이 받는다.

## Application
- Noise filtering
- Visualization
- Feature Extraction
- Stock market perdictions
- Gene data analysis
