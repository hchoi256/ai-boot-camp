# Convolutional Neural Network
![image](https://user-images.githubusercontent.com/39285147/179902542-86d89abf-4428-465f-8560-a1a083ab5d7c.png)

# 강의 목차
### [What are CNN?](#CNN)
### [Step 1 - Convolution Operation](#Convolution-Operation)
### [Step 1(b) - ReLU Layer](#ReLU-Layer)
### [Step 2 - Pooling](#Pooling)
### [Step 3 - Flattening](#Flattening)
### [Step 4 - Full Connection](#Full-Connection)
### [Step 5 - CNN Performance](#CNN-Performance)

[code](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/deep-learning/convolutional_neural_network.ipynb) - [contact me if you need dataset](https://hchoi256.github.io/)

> ANN vs. CNN
>> ANN은 특징이 정리된 입력값들을 가지고 학습을 해야했지만, CNN은 인간처럼 스스로 특징을 찾아서 입력값을 도출해낸다.

## CNN
![image](https://user-images.githubusercontent.com/39285147/179897796-f3a44156-97da-4728-9824-869f7f31ba94.png)

이미지에서 feature를 뽑기위해 사용하는 합성곱 연산 과정을 수반한다.

특징 탐지기를 사용해 이미지에서 특징을 찾고, 그것들을 특징 맵에 넣고, 픽셀 사이의 *공간적 관계*를 보전한다.

신경망 학습에서 특징 스케일링은 필수적이다.

> Convolution -> Max Pooling -> Flattening -> Full Connection

## Convolution Operation
![image](https://user-images.githubusercontent.com/39285147/179901651-4550a375-2050-46ea-aa3e-17ea90ecabbe.png)

각 feature map들은 각기 다른 커널을 통해 생성되며 그 특징이 이미지 어느 부분에 나타나있는지 표시한다. 또한, 그 feature map 집합을 Convolutional Layer라 지칭한다.

### Convolution
![image](https://user-images.githubusercontent.com/39285147/179900743-d9fd4bf7-9788-4941-a6c7-8f8e5e268aa8.png)

두 개의 함수의 결합으로, 한 함수가 다른 것의 모양을 어떻게 바꾸는지 보여준다.

> Feature detector(= kernel, filter)
>> 우리가 무언가를 보는/인식하는 방식으로, Convolution Operation 이후 Feature Map에서 특정 수치가 높다면 그것은 해당 커널(어떤 특징)과 밀접한 관련이 있다.

> Stride
>> 필터 적용시 이동 간격으로, Stride가 클수록 이미지가 더 작아지고 정보를 더 많이 잃는다.

<details markdown="1">
<summary>Types of Kernel</summary>

[*Sharpen*]

![image](https://user-images.githubusercontent.com/39285147/179902014-7329c0f1-92f0-4db3-9649-5629654dda30.png)

[*Blur*]

![image](https://user-images.githubusercontent.com/39285147/179902072-88b3621d-a314-4269-8435-b37cdb500985.png)

[*Edge Enhance*]

![image](https://user-images.githubusercontent.com/39285147/179902147-857c1a66-29e6-42ff-8d35-5fc440460b46.png)
![image](https://user-images.githubusercontent.com/39285147/179902241-0709f89b-ea5d-4f28-b720-174720a4af3e.png)

[*Edge Detect*]

![image](https://user-images.githubusercontent.com/39285147/179902177-3c902d7a-32ba-4123-ba84-719a777554ae.png)
![image](https://user-images.githubusercontent.com/39285147/179902160-da736e49-fc2c-4400-82a3-98e089bfbdfa.png)

가운데 픽셀(-4) 강도가 낮아지고, 주변(1) 강도를 올려준다.

[*Emboss*]

![image](https://user-images.githubusercontent.com/39285147/179902349-44be9355-efb5-4300-a81f-c812bdfb4db1.png)
![image](https://user-images.githubusercontent.com/39285147/179902379-284a44dd-58d8-4a58-9f9a-ef574b5a4788.png)

입체감 선사

</details>

## ReLU Layer
![image](https://user-images.githubusercontent.com/39285147/179902905-9e100976-2ff1-4aa7-9f84-817d73fa8a43.png)

정류기 함수(i.e., ReLU)로 이미지에 선형성을 깨뜨리고 비선형성을 도입하고 싶어서 사용한다.

![image](https://user-images.githubusercontent.com/39285147/180514256-9cca684d-5f1e-44a0-a902-a9274b169942.png)

ReLU 함수를 통하여 값이 증가하여도 기울기가 줄어드는 (= 학습 속도가 줄어드는) 단점이 개선되어, 주로 은닉층에서 활용된다.

## Pooling
![image](https://user-images.githubusercontent.com/39285147/179903718-0b4fd665-8a1b-4a61-8a86-0b404a44bfd8.png)

Pooling을 통하여 특징을 보존할 수 있고, 더 나아가 그들의 공간적, 조직상 또는 다른 종류의 왜곡까지 고려 가능하다 (모델 일반화 ↑, 과적합 ↓).

가령, 각기 다른 방향을 바라보고 있는 같은 치타의 사진으로부터 특징을 찾아내기 위해 Pooling이 사용된다.

#### Max Pooling
![image](https://user-images.githubusercontent.com/39285147/179903816-5e9995b4-e328-4f37-97bb-c745dd9bbd7b.png)
![image](https://user-images.githubusercontent.com/39285147/179904632-0bb7d474-dab2-4240-b323-2c3164e5bf58.png)

### 장점
- 불필요한 데이터가 차지하는 75%만큼 사이즈를 절감하여 처리속도가 증가한다.
- CNN의 최종 계층에 들어갈 피라미터 개수를 줄여서 **과적합**을 방지한다.

## Flattening
![image](https://user-images.githubusercontent.com/39285147/179905388-d0b0cc96-04f0-4ed8-a5c2-ba33599c546e.png)

인공 신경망에 1차원 배열로써 입력하기 위해서 Flattening한다.

## Full Connection
![image](https://user-images.githubusercontent.com/39285147/179907316-73091b20-abf1-4c9f-a38b-099449234249.png)

컨볼루션 신경망(CNN)에 인공 신경망(ANN)을 추가한다.

### Backpropagation
- 비용함수를 최소화하도록 ANN의 가중치를 업데이트한다.
- 특징 탐지기(커널)을 업데이트한다 (특징 자체를 잘못 찾았을 수도)

## CNN Performance
1. **특성 검출 개수를 증가시킨다** (i.e., 커널 32개 보다 64가 CNN 성능 개선에 도움이 되었다).
2. **Dropout**: 신경망 내 뉴런 탈락 (피라미터 수 ↓, 일반화 ↑, 모델 성능 ↑)
- 과적합 개선 및 뉴런 간의 다중공신성 문제 해결

# Reference
> Softmax
>> ![image](https://user-images.githubusercontent.com/39285147/179908795-76677ab7-84ca-44d9-84a4-fc09f8290fe2.png)
>>
>> 출력값은 서로 연관되지 않아야 하는데 왜 두 합이 1로 수렴될까? 그 이유는 softmax 함수가 모든 값들의 합이 1이 되도록 정규화를 수행하기 때문이다.

[Cross-Entropy](https://github.com/hchoi256/ai-terms/blob/main/entropy.md)
