# Natural Language Processing
Natural Language Processing (or NLP) is applying Machine Learning models to text and language.

[code](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/nlp/natural_language_processing.ipynb)

## Overview
- [**Part 1**: Types of NLP](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/nlp/types-of-nlp.md)
- [**Part 2**: Classical vs. Deep Learning Models](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/nlp/classical-vs-dl.md)
- [**Part 3**: Bag-Of-Words](https://github.com/hchoi256/ai-boot-camp/blob/main/ai/nlp/bag-of-words.md)

> *does not talk about Seq2Sqe or Chatbots*

## Implementation - 감성 분석

### Process
1. Importing libraries
2. Importing datasets
3. Cleaning text
4. Creating the Bag of Words model
5. Splitting the data into Training and Test sets
6. Training thee Naive Bayes model on the Training set
7. Predicting the Test set results
8. Making the confusion matrix
9. Predicting if a single review is positive or negative

### Note
![image](https://user-images.githubusercontent.com/39285147/179498392-39d35dca-6727-4289-bf88-4122801fb1d5.png)

- **courpus**: 최종 후기
- **nltk**: 제외어 (i.e., a, the, etc.)
  - *stopwords*: 제외어 라이브러리 (i.e., stopwords.words('english'))
- **PorterStemmer**: 어간 추출로, 동사를 현재형으로 취합한다 (i.e., 좋았어요/좋았다 --> 좋다)
- **re.sub('[^a-zA-z]', ' ', dataset['Review'][i])**: 구두점 없애기
- **review.lower()**: 소문자로 통일하기
- **review.split()**: 단어별로 분류

> NLTK
>> Tokenization
>> Part of Speech Tagging
>> Named Entity Recognition
>> Sentiment analysis(감성 분석)

> 희소행렬
>> 행렬 안의 많은 항들이 0으로 되어있는 행렬

### Tokenization
주어진 코퍼스(corpus)에서 토큰(token)이라 불리는 단위로 나누는 작업이다 ('단어'가 토근의 기준일 수 있다).
- **CounterVectorizer()**: 주어진 후기로부터 모든 단어 집합을 가져온다.
  - *max_features* = 1500: 가장 빈번하게 사용되는 1500개의 단어를 가져온다 (rick처럼 한 번만 나오는 연관성 없는 단어는 제외)
  
#### Types of Tokenization
- **Word tokenization**: 대량의 텍스트를 단어로 분할하는 과정에서 각 단어를 인식하고 특정 감정에 대한 분류 및 계산과 같은 추가 분석을 거쳐야 하는 NLP 작업
- **Sentence tokenization**: 문장을 기준으로 토큰화
- **Regex tokenization**: Regex를 기준으로 토큰화
- **Blank line tokenization**: 빈 줄을 기준으로 토큰화
  
## How to Improve Performance
1. 여러 다른 모델 사용
2. 텍스트 정리
3. 제외어 범주 다듬기 (i.e., not 뿐만 아니라 isn't 포함하기)
