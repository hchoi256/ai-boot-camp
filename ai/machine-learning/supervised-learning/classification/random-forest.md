****
### Terms
- Random Forest
- Ensemble learning

[code](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/machine-learning/supervised-learning/classification/codes/random_forest_classification.ipynb)

# Random Forest Intuition
![image](https://user-images.githubusercontent.com/39285147/178423838-f07bda91-6a04-40cb-b7e3-3b295cbdc8c8.png)
 
 **Bagging* 방식의 Ensemble 모델로 여러 여러 의사결정나무 방법들을 합치는 방법이다.
 
*다수의 힘*: 모든 나무들의 소리를 확인하고 다수결의 결정을 가져와서 그 결과에 기반해 범주화를 수행하여 불확실성을 최소화한다.

## Ensemble learning
모델을 학습시켜 결합하는 방식으로 문제를 해결하는 방식이다

### Ensemble Types
- **Bagging**: 같은 유형의 알고리즘들을 조합하되 각각 학습하는 데이터를 다르게 한다.
- **Voting**: 서로 다른 종류의 알고리즘들을 결합한다.

## Process
![image](https://user-images.githubusercontent.com/39285147/178426777-8171d3c1-0738-4def-b7e2-a0a5491d7da6.png)

- **STEP 1**: Pick at random K data points from the training set
- **STEP 2**: Build the decision tree associated to these K data points
- **STEP 3**: Choose the number Ntree of trees you want to build and repeat STEPS 1 & 2; each decision tree is **different**
- **STEP 4**: For a new data point, make each one of your Ntree trees predict the category to which the data points belongs, and assign the new data point to the category that wins the majority vote.

## Applications
[*Microsoft's kinect*](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/BodyPartRecognition.pdf) - *Real-Time Human Pose Recognition in Parts from Single Depth Images*

![image](https://user-images.githubusercontent.com/39285147/178424037-459a5de0-91dc-49e1-ac10-5a8f3e46e252.png)

랜덤 포레스트를 사용하여 몸의 일부가 어디 있는지 이해하고 거기에 기반해서 기기가 컴퓨터  게임에서 뭘 해야 할지 알아낸다.
- 더 빠른 속도의 프로세싱을 의사결정 포레스트로 얻어서 이 도구에 필요한 하드웨어 가격을 줄였다.
