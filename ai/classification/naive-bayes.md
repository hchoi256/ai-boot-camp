****
### Terms
- Naive Bayes

[code](https://github.com/EricChoii/ai-boot-camp-ablearn/blob/main/ai/classification/codes/naive_bayes.ipynb)

# Bayes
![image](https://user-images.githubusercontent.com/39285147/178406887-84424b6b-2469-414c-9433-1c3f5565aa42.png)

# Naive Bayes Intuition
![image](https://user-images.githubusercontent.com/39285147/178408112-e5b39a5b-98e5-46e0-b04c-df0749e67c91.png)
![image](https://user-images.githubusercontent.com/39285147/178408167-355fa96a-eb74-41ae-ab78-f5acf821d634.png)

Beyas와 다르게 데이터셋의 모든 데이터들이 동등하고 **독립적**이라고 가정 (independent assumptions)
- ML에서 요소가 독립적이지 않으면 베이즈 이론 적용 불가능한 한계를 개선했다.

## Goal
![image](https://user-images.githubusercontent.com/39285147/178408141-16c9bd7d-0725-4245-aff8-a78e09a7622d.png)

## Process
![image](https://user-images.githubusercontent.com/39285147/178408577-14d7c57f-81ea-40ae-b0e6-79e75baf73e1.png)
![image](https://user-images.githubusercontent.com/39285147/178408872-5311a2a7-6cd1-433c-ba57-4f7a49c4ad44.png)

요소가 두 개일 경우 하나만 구하고 나머지는 1에서 뺀 나머지로 쉽게 계산해볼 수 있다.
- 하지만, 요소가 세 개라면 두 번의 계산을 거쳐야 한다.

<details markdown="1">
<summary>Find P(X)(접기/펼치기)</summary> 

![image](https://user-images.githubusercontent.com/39285147/178408431-0e56e190-084a-459c-93d6-e6f9d15f7300.png)
![image](https://user-images.githubusercontent.com/39285147/178408478-6b3ee1d3-f96f-4872-afe8-02a8fe823bcb.png)

새로운 데이터가 X와 유사한 요소를 보일 가능도

</details>

## Conclusion
![image](https://user-images.githubusercontent.com/39285147/178408907-09ca4cc3-0d06-48d4-a857-cf3aafea5098.png)
![image](https://user-images.githubusercontent.com/39285147/178411506-54e54b51-c568-4d39-816e-fb86ae243ffe.png)

