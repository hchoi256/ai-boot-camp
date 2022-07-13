****
### Terms
- Apriori

[code](https://github.com/EricChoii/ai-boot-camp/blob/main/ai/unsupervised-learning/association-rule/codes/apriori.ipynb)

# Apriori
## Support(지지도)
![image](https://user-images.githubusercontent.com/39285147/178700555-cea5698d-3ba6-412f-b0ce-0140de9b3046.png)
![image](https://user-images.githubusercontent.com/39285147/178702321-d8f60dfc-e81a-4bc7-b3bf-ae864e404b28.png)

특정 아이템이 데이터에서 발생하는 빈도

## Confidence(신뢰도)
![image](https://user-images.githubusercontent.com/39285147/178700676-9e95ec4f-6526-486e-8d84-8b6d3b8d240f.png)
![image](https://user-images.githubusercontent.com/39285147/178702266-dd738680-86ae-4edb-a075-a4f0a38bb695.png)

두 아이템의 연관규칙이 유용한 규칙일 가능성의 척도(= 아이템 집합 간의 연관성 강도를 측정하는 데 쓰는 신뢰도)
  
## Lift(향상도)
![image](https://user-images.githubusercontent.com/39285147/178700818-870a09b8-cac6-4d21-8bb9-5c2bf814cf9b.png)
![image](https://user-images.githubusercontent.com/39285147/178702300-dcb813fa-cbe2-450a-b276-b4b1bab6b03e.png)

두 아이템의 연관규칙이 우연인지 아닌지를 나타내는 척도(= 생성된 규칙이 실제 효용가치가 있는지를 판별하는 데 사용되는 향상도)

## Apriori Algorithm
- **STEP 1**: Set a minimum support and confidence
- **STEP 2**: Take all the subsets in transactions having higher support than minimum support
- **STEP 3**: Take all the rules of these subsets having higher confidence than minimum confidence
- **STEP 4**: Sort the rules by decreasing lift

## Applications
- Reference Systems by Amazon
- 신용카드 사기를 당했을 때 주로 결제되는 내역 패턴
- B2C에서 구매자의 구매 상품과 비슷한 상품 추천
