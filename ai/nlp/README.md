# Natural Language Processing
Natural Language Processing (or NLP) is applying Machine Learning models to text and language.

[code](https://github.com/EricChoii/ai-boot-camp/blob/main/ai/nlp/natural_language_processing.ipynb)

## Overview
- [**Part 1**: Types of NLP](https://github.com/EricChoii/ai-boot-camp/blob/main/ai/nlp/types-of-nlp.md)
- [**Part 2**: Classical vs. Deep Learning Models](https://github.com/EricChoii/ai-boot-camp/blob/main/ai/nlp/classical-vs-dl.md)
- [**Part 3**: Bag-Of-Words](https://github.com/EricChoii/ai-boot-camp/blob/main/ai/nlp/bag-of-words.md)

> *does not talk about Seq2Sqe or Chatbots*

## Implementation
![image](https://user-images.githubusercontent.com/39285147/179495322-a40ef4e9-7f79-4331-9cf9-3060a4fbc4b0.png)

- **courpus**: 최종 후기
- **nltk**: 제외어 (i.e., a, the, etc.)
  - *stopwords*: 제외어 라이브러리 (i.e., stopwords.words('english'))
- **PorterStemmer**: 어간 추출로, 동사를 현재형으로 취합한다 (i.e., 좋았어요/좋았다 --> 좋다)
- **re.sub('[^a-zA-z]', ' ', dataset['Review'][i])**: 구두점 없애기
- **review.lower()**: 소문자로 통일하기
- **review.split()**: 단어별로 분류

> 희소행렬
>> 행렬 안의 많은 항들이 0으로 되어있는 행렬
