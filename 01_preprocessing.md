# 텍스트 문서 전처리

- tokenizing (토큰화→ 쪼개기?)
    - sentence tokenizing : 여러 개의 문장으로 구성된 문서를 문장 단위로 쪼개기
    - word tokenizing: 문서 혹은 문장을 넣어 단어 수준으로 쪼개기
- stemming (어간추출)
- lemmatizing (원형복원)


## 1. tokenizing
```python
from nltk.tokenize import sent_tokenize
text = 'Hi, my name is hyejin. Nice to meet you. This is an example of sentence tokenizing.'
sent_tokenize(text)
```
>Out[10]: 
['Hi, my name is hyejin.',
 'Nice to meet you.',
 'This is an example of sentence tokenizing.']
