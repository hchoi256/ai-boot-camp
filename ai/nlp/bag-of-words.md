# Bag of Words
![image](https://user-images.githubusercontent.com/39285147/179490578-5e5ee6b5-6832-4fdf-b790-6814695b1f90.png)

Bag of Words 기법은 문서(document)를 자동으로 분류하기 위한 방법중 하나로서, 글에 포함된 단어(word)들을 **순서를 무시하는** 벡터로 표현하고, 그 분포를 관찰하여 이 문서가 어떤 종류의 문서인지를 판단하는 기법을 지칭한다.
- i.e., 어떤 문서에서 '환율', '주가', '금리' 등의 단어가 많이 나온다면 이 문서는 경제학에 관련된 문서로 분류하고, '역광', '노출', '구도' 등의 단어가 많다면 사진학에 대한 문서로 분류하는 방식이다.

> Vector 표현
>> 문서1 : 정부가 발표하는 물가상승률과 소비자가 느끼는 물가상승률은 다르다.
>>
>> vocabulary : {'정부': 0, '가': 1, '발표': 2, '하는': 3, '물가상승률': 4, '과': 5, '소비자': 6, '느끼는': 7, '은': 8, '다르다': 9}
>> bag of words vector : [1, 2, 1, 1, 2, 1, 1, 1, 1, 1]

### Applications of BoW
영상처리, 컴퓨터 비전 
- 이미지를 분류(image categorization), 검색(image retrieval), 최근에는 물체나 씬(scene)을 인식하기 용도로도 폭넓게 활용되고 있다.

## 동작 원리
1. Logistic regression (NLP)
2. Neural network (DNLP)

## 한계점
BoW으로는 Yes/No 형식으로 대답할 수 밖에없어서, 다른 모델들과 조합하여 사용해야 한다.
