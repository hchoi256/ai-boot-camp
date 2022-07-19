****
### Terms
- Eclat

[code](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/machine-learning/unsupervised-learning/association-rule/codes/eclat.ipynb)

# Eclat
이걸 산 사람은 저걸 산다는 추측 방법. Eclat 모델은 모든 조합을 검토하고 어떤 것에 집중해야 하는지 알려주는 역할을 한다.

Eclat 모델에는 지지도 밖에 없어서 하나의 아이템 자체를 보는 것은 의미가 없다. 최소 두 개 이상의 아이템을 포함하는 세트의 빈도수를 통하여 판단한다. 가령, 모든 영화 감상 목록에서 인터스텔라와 엑스 마키나 영화를 동시에 감상하는 세트의 빈도수. 

## Support(지지도)
![image](https://user-images.githubusercontent.com/39285147/178717475-5b89ee51-26da-4d6a-96e8-40cdda800b7c.png)

## Eclat Algorithm
- **STEP 1**: Set a minimum support (*최소 지지도 수준 이하는 신경쓰지 않기 위함*)
- **STEP 2**: Take all the subsets in transactions having higher support than minimum support
- **STEP 3**: Sort these subsets by decreasing support
