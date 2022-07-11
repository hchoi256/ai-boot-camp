****
### Terms
- Kernel SVM
- Mapping to Higher Dimension
- Kernel Trick
- Non-linear SVR

[code](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/classification/codes/kernel_svm.ipynb)

# Kernel SVM Intuition
![image](https://user-images.githubusercontent.com/39285147/178288744-b1ec6e6e-89fe-4ca9-8297-000a2bb442e2.png)

# How to Interpret Non-linear Data
## ① Mapping to a Higher Dimension (*Not the best*)
### Case 1: 1D to 2D space
#### STEP 1: 1 dimension
![image](https://user-images.githubusercontent.com/39285147/178288958-bf0662c3-ba9d-4c98-96eb-b7ba1a45bc4c.png)

#### STEP 2: *f=x-5*
![image](https://user-images.githubusercontent.com/39285147/178289077-50af8e19-d23c-4349-8335-2accfc6bf3a0.png)

#### STEP 3: 2 dimension - *(x-5)^2*
![image](https://user-images.githubusercontent.com/39285147/178289183-b4ebce5d-c7fb-4334-8d91-209a8214a54f.png)

### Case 2: 2D to 3D space
![image](https://user-images.githubusercontent.com/39285147/178289680-ccf80ab1-2e93-411a-aaa2-3d0a7c79c815.png)
![image](https://user-images.githubusercontent.com/39285147/178290026-b50fc406-a883-47b6-8093-71cc91cd1887.png)

### ①의 한계
- 고차원으로 매핑하는 과정에 계산이 많이 들어가서 데이터 집합이 클수록 높은 프로세승 능력을 요구한다.
- 프로세스(저차원 > 고차원 > 저차원)의 효율성 ↓, 지연 多

## ② Kernel Trick
**가우스 커널(= RBF 함수 커널)*
![image](https://user-images.githubusercontent.com/39285147/178292028-2d1d4600-2870-41fe-877b-0e6938a7bbc1.png)

고차원으로 가야한다는 ①의 한계를 극복하여 비선형 처리를 수행한다.
- 랜드마크에서 멀리 떨어져 있을수록 우항값(= 높이)이 0에 수렴한다; 반대로, 가까울수록 우항이 1에 가까워진다.
  - *랜드마크*: 점 <0, 0, 0>

### Kernel Trick Intuition
![image](https://user-images.githubusercontent.com/39285147/178293188-f551385a-9e82-4640-ac95-71dd26ad4a8e.png)
![image](https://user-images.githubusercontent.com/39285147/178293266-26f8f072-57a2-4a3b-8c51-0b2dcc1727b7.png)

> *가우스 커널* - 알맞게 시그마를 조절하여(= **결정 경계 조절**) 방사형 **비선형** 데이터를 적절히 분류하는 방법

### 응용
![image](https://user-images.githubusercontent.com/39285147/178294134-aec0b2fd-0b7b-46a5-8aeb-afa667e8ab97.png)

# Types of Kernel Functions
![image](https://user-images.githubusercontent.com/39285147/178294709-b0b1b563-ab91-49de-aac2-75fde935a787.png)

# Non-linear SVR
![image](https://user-images.githubusercontent.com/39285147/178297257-0f389649-5fa5-41a0-b06d-7496f092f531.png)

상기처럼 Linear SVR의 어떤 형태로도 적절하게 표현할 수 없는 데이터셋에 대해 Non-linear SVR을 사용한다.

## 3차원 상에서 RBF 커널에 2차원 데이터 투영한 모습
![image](https://user-images.githubusercontent.com/39285147/178297352-474cee20-2000-4358-8674-f1dc9b75ba43.png)

## 3차원 상에서 Support Vectors 구현하여 2차원에 투영한 모습
![image](https://user-images.githubusercontent.com/39285147/178297096-0adb709c-a01b-43e6-9792-af8589ae1161.png)



