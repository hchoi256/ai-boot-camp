****
### Terms
- UCB

[code](https://github.com/EricChoii/ai-boot-camp/blob/main/ai/machine-learning/reinforcement-learning/codes/upper_confidence_bound.ipynb)

# Upper Confidence Bound (UCB)
![image](https://user-images.githubusercontent.com/39285147/179367150-4d5bd124-8058-4194-b3b4-a729064780c3.png)

Exploration/Exploitation에 시간과 돈을 소모해야하는 AB Test보더 다 정교한 '결정론적' 방법으로, 그 동안의 관측 결과에서부터 time t에서 arm i의 expected reward의 confidence (확률이 높은) upper bound를 선택하는 방식으로 **더 빠른** '탐색'을 수행한다.
- 예측 횟수 ↑, 신뢰 구간 ↓, U(a) ↓, exploration ↓ --> 더 안정적인 결과를 보여주는 action을 선택 --> (exploitation) 효과적으로 action을 선택하게 끔 하는 효과가 생깁니다.

## Visualization
[*5000 rounds*]

![image](https://user-images.githubusercontent.com/39285147/179471716-f6a3459f-bce2-4234-871f-f98679fcd013.png)

UCB는 예측 라운드가 늘어날 수록 더 정확한 분류를 해낸다.

## 한계점
500 라운드처럼 적은 횟수의 라운드에서는 정확한 식별이 어렵다. 하지만, 톰슨 샘플링은 가능하다.

# Reference
[UCB](https://jyoondev.tistory.com/137)
