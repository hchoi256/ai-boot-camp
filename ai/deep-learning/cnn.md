# Convolutional Neural Network
![image](https://user-images.githubusercontent.com/39285147/179902542-86d89abf-4428-465f-8560-a1a083ab5d7c.png)

# 강의 목차
### [What are CNN?](#What-are-CNN?)
### [Step 1 - Convolution Operation](#Convolution-Operation)
### [Step 1(b) - ReLU Layer](#ReLU-Layer)
### [Step 2 - Pooling](#Pooling)
### [Step 3 - Flattening](#Flattening)
### [Step 4 - Full Connection](#Full-Connection)
### [Reference](#Reference)

[code](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/deep-learning/convolutional_neural_network.ipynb)

## What are CNN?
![image](https://user-images.githubusercontent.com/39285147/179897796-f3a44156-97da-4728-9824-869f7f31ba94.png)

이미지에서 feature를 뽑기위해 사용하는 합성곱 연산 과정을 수반한다.

특징 탐지기를 사용해 이미지에서 특징을 찾고, 그것들을 특징 맵에 넣고, 픽셀 사이의 *공간적 관계*를 보전한다.

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
## Pooling
## Flattening
## Full Connection

# Reference
> Softmax
>>

[Cross-Entropy](https://github.com/hchoi256/ai-terms/blob/main/entropy.md)
