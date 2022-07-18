# Artificial Neural Network
![image](https://user-images.githubusercontent.com/39285147/179502990-456391e2-bc2b-4069-b2f4-8658a2f4e9c5.png)

[code](https://github.com/EricChoii/ai-boot-camp/blob/main/ai/deep-learning/ann.md)

# 강의 목차
- [The Neuron](#The-Neuron)
- [The Activation Function](#The-Activation-Function)
- [How do Neural Networks work? (example)](#How-do-Neural-Networks-work)
- [Gradient Descent](#Gradient-Descent)
- [Stochastic Gradient Descent](#Stochastic-Gradient-Descent)
- [Backpropagation](#Backpropagation)

## The Neuron
![image](https://user-images.githubusercontent.com/39285147/179503630-49a8ef30-2a1c-4de0-8c2a-7910c430cce0.png)

## The Activation Function
![image](https://user-images.githubusercontent.com/39285147/179505263-7a8b8e68-05ac-4093-9128-b670cf0c805e.png)

### Threshhold Function
![image](https://user-images.githubusercontent.com/39285147/179504289-5694a414-7878-412c-b559-fcad0e9fe86a.png)

### Sigmoid Functino
![image](https://user-images.githubusercontent.com/39285147/179504097-d0d51a22-b89b-4c35-b00a-ef512a248ba6.png)

### Rectifier
![image](https://user-images.githubusercontent.com/39285147/179504175-4b72ded3-4456-4691-9356-c5dd9f61a6bd.png)

### Hyperbolic Tangent (Tanh)
![image](https://user-images.githubusercontent.com/39285147/179504234-8b153f1f-c694-4d48-9051-626399c401ea.png)

## How do Neural Networks work
![image](https://user-images.githubusercontent.com/39285147/179506502-b0e176a2-7f7b-48dc-a128-cc71c0153349.png)

### How do NN learn?
![image](https://user-images.githubusercontent.com/39285147/179507564-aa9b81cf-ef7e-463c-bd1c-69d17faa730c.png)
![image](https://user-images.githubusercontent.com/39285147/179507961-8e068c3f-4eea-485a-aef4-a115ee99415a.png)

> 비용 함수
>> 예측값과 실제값의 차이/오류를 알려주는 함수로, 비용함수를 최소화하여 가중치를 업데이트하는 모델 학습 방식에 사용된다.

> 역전파
>> 예측값과 실제값의 차이인 오차를 계산하고, 이것을 다시 역으로 전파하여 가중치를 조정하는 과정을 의미한다. 이때, 역전파 과정에서는 최적화 함수를 이용합니다.

## [Gradient Descent(= Batch Gradient Descent](https://github.com/EricChoii/lg-ai-auto-driving-radar-sensor/blob/main/supervised-learning/gradient-discent.md)
![image](https://user-images.githubusercontent.com/39285147/179517720-510df59a-32ea-422b-90b1-d95e242e6d26.png)

*모든 데이터*를 가지고 신경망에서 학습을 수행하여 가중치 업데이트를 수행한다.

### 한계점 및 해결
![image](https://user-images.githubusercontent.com/39285147/179517820-59c3f071-886b-42f9-8eec-f1fd23833801.png)

**Stochastic Gradient Descent**는 볼록한 형태의 비용함수를 필요로 하지 않으므로, 상기 함수꼴 모양에서도 수행이 가능하다.

## [Stochastic Gradient Descent](https://github.com/EricChoii/lg-ai-auto-driving-radar-sensor/blob/main/supervised-learning/gradient-discent.md)
![image](https://user-images.githubusercontent.com/39285147/179517808-468c6626-3096-4ff2-a97b-842abb56a68c.png)

*랜덤한 하나의 데이터*를 가지고 신경망에서 학습을 수행하여 가중치 업데이트를 수행하고, 또 다른 하나의 확률적 데이터를 가지고 앞서 언급된 작업을 반복한다.

### SGD vs. BGD
![image](https://user-images.githubusercontent.com/39285147/179518561-861ffd82-a689-4794-a667-e46e974ef2e6.png)

SGD의 장점
- Local optima에 빠지는 현상을 상대적으로 피해준다 (더 큰 변동성을 감당할 수 있기 때문이다).
- 한번에 모든 데이터에 접근하지 않아서 수행이 빠르다


> Mini-batch Gradient Descent
>> BGD와 SGD의 확장버전으로, 설정된 횟수 만큼의 데이터 행을 실행한다 (i.e., 5, 10, etc.)

## Backpropagation
![image](https://user-images.githubusercontent.com/39285147/179519600-66e86494-8c48-4121-81da-73c86b568fd8.png)

역전파 알고리즘은 출력값에 대한 입력값의 기울기(미분값)을 출력층 layer에서부터 계산하여 거꾸로 전파시키는 것이다.

역전파 과정에서 이 알고리즘의 구조화된 방식으로 인해 모든 가중치를 **동시에** 조정할 수 있어서, 신경망에서 어떤 가중치가 어떤 오차의 원인이 되는지 파악할 수 있다.

> Forwardpropagation
>> ![image](https://user-images.githubusercontent.com/39285147/179519501-2149e1ea-4b48-4799-8f08-35b6437b2a2b.png)


