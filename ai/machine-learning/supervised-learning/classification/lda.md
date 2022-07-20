# LDA
![image](https://user-images.githubusercontent.com/39285147/180001194-581be4f5-1d12-4cf1-b6ec-cc5632f23a6a.png)
![image](https://user-images.githubusercontent.com/39285147/180001832-3ac79934-d360-4de1-a837-80a7068e096e.png)

데이터들을 하나의 직선(1차원 공간)에 projection시킨 후 그 projection된 data들이 잘 구분이 되는가를 판단하는 방법이다.
- Projection 후 두 데이터들의 중심(평균)이 서로 멀수록, 그 분산이 작을수록 구분이 잘 되었다고 얘기할 수 있다. 

PCA처럼 주로 차원 축소 기술로 사용된다. 하지만, 주축을 찾는 PCA의 목적과 더불어 다중 클래스 사이의 분할을 **최대화** 하는 축에 관심이 있다는 점에서 차이가 있다.
- PCA: 축을 주성분을 차원축소한다.
- LDA: 데이터 안 클래스들의 분리를 찾는다.

종속변수와의 연관성 때문에 지도학습 알고리즘으로 분류되었다.

[code](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/machine-learning/supervised-learning/classification/codes/linear_discriminant_analysis.ipynb)

## Goal
- 클래스 판별 정보를 유지하는 와중에 미래 공간을 작은 부분 공간에 투영한다.

## Process
![image](https://user-images.githubusercontent.com/39285147/180001410-5c95a6a9-f289-4873-b9e4-375e2c729a59.png)


