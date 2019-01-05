# 텍스트 문서 전처리

- tokenizing (토큰화→ 쪼개기?)
    - sentence tokenizing : 여러 개의 문장으로 구성된 문서를 문장 단위로 쪼개기
    - word tokenizing: 문서 혹은 문장을 넣어 단어 수준으로 쪼개기
- stemming (어간추출)
- lemmatizing (원형복원)


## 1. tokenizing

tokenizing은 단어/문장 등으로 이뤄진 (일종의 덩어리 형태의) 텍스트 데이터를 분할하는 과정입니다. 문서를 문장단위로 tokenizing 할 수 있으며, 문서/문장을 단어단위로 tokenizing 할 수 있습니다. nltk.tokenize 모듈을 활용해서 문장으로 쪼갤 경우 sent_tokenize(), 단어단위로 쪼갤 경우 word_tokenize()를 사용합니다. 

```python
from nltk.tokenize import sent_tokenize
text = 'Hi, my name is hyejin. Nice to meet you. This is an example of sentence tokenizing.'
sent_tokenize(text)
```
>Out[10]: 
['Hi, my name is hyejin.',
 'Nice to meet you.',
 'This is an example of sentence tokenizing.']
