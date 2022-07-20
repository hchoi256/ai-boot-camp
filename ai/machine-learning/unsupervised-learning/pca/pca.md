# PCA

[code](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/machine-learning/unsupervised-learning/pca/principal_component_analysis.ipynb)

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

## 단점
아웃라이어에 굉장히 영향을 많이 받는다.

## Application
- Noise filtering
- Visualization
- Feature Extraction
- Stock market perdictions
- Gene data analysis
