# CoreNLP 설치하기

# CoreNLP 다운로드!

아래 링크에서 다운 받습니다. <br>
https://stanfordnlp.github.io/CoreNLP/#about <br>

저는 3.9.2 버전을 다운로드 받았습니다! <br>
stanford-corenlp-full-2018-10-05.zip 형태로 받아진 파일을 압축풀기를 합니다. <br>

corenlp는 java 기반으로 돌아가기 때문에 java를 설치하셔야 해요! <br>

cmd창을 키고, 압축이 풀어진 폴더의 경로로 변경시켜줘요 <br>
저는 D드라이브 ㄴㅌ폴더의 하위 폴더로 저장되어 있습니다. <br>
(cmd 에서는 기본경로가 C드라이브를 되어 있어서 D드라이브로 먼저 바꿔서 진행했습니다.) <br>
그리고, coreNLP 서버를 실행시켜 줍니다. 서버실행은 하단 url 에서 참고했어요. <br>
https://stanfordnlp.github.io/CoreNLP/corenlp-server.html <br>

cmd 창 입력내용  <br>
> C:\Users\USER>cd /d D:\
> cd D:\ㄴㅌ\stanford-corenlp-full-2018-10-05\stanford-corenlp-3.9.2-models
> java -mx4g -cp "*" edu.stanford.nlp.pipeline.StanfordCoreNLPServer -port 9000 -timeout 15000


그럼 이제 끄읕! <br>
파이썬에서도 잘 돌아가는지 확인해보겠습니다.  <br>


```python
from nltk.parse.corenlp import CoreNLPDependencyParser
dep_parser = CoreNLPDependencyParser(url='http://localhost:9000')
parse, = dep_parser.raw_parse('The quick brown fox jumps over the lazy dog.')
print(parse.to_conll(4))
```

결과도 잘 나오네요. <br>

```python
The	DT	4	det
quick	JJ	4	amod
brown	JJ	4	amod
fox	NN	5	nsubj
jumps	VBZ	0	ROOT
over	IN	9	case
the	DT	9	det
lazy	JJ	9	amod
dog	NN	5	nmod
.	.	5	punct
```

여러가지 분석들은 다음에 해보겠습니다. <br>
감사합니다.
