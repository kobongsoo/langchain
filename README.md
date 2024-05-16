# 랭체인(LangChain)
출처 : 위키독스 [랭체인](https://wikidocs.net/233341) ebook <br>

LangChain은 LLM 모델, 임베딩 모델을 활용해 RAG, Q&A, 요약등 다양한 애플리케이션을 개발할 수 있는 프레임워크.<br>

### 설치<br>
```
# langchain 만 설치
# pip
pip install langchain

# conda
conda install langchain -c conda-forge

# 필요한 모든 패키지 한꺼번에 설치
pip install -U langchain langchain-community langchain-experimental langchain-core langchain-openai langsmith langchainhub python-dotenv unstructured chromadb faiss-cpu rank_bm25 python-docx sqlalchemy

```
### 설정
#### 1) API 키 발급
- [**OpenAI API 키 발급**](https://teddylee777.github.io/openai/openai-api-key/)
- [허깅페이스 API 키 발급](https://sunshower99.tistory.com/30)
- [구글 API 키 발급](https://okayoon.tistory.com/entry/%EA%B5%AC%EA%B8%80-API-KEY%EC%83%9D%EC%84%B1%ED%95%98%EB%8A%94-%EB%B2%95)
- [랭체인 API 키 발급](https://bcho.tistory.com/1427)
  <br>(**OpenAI API 키/허깅페이스 API키 필수, 다른키는 선택 사항**)
  
 #### 2).env 파일 설정
- 프로젝트 루트 디렉토리에 .env 파일을 생성.
- 파일에 API 키를 다음 형식으로 저장: OPENAI_API_KEY 에 발급받은 API KEY 를 입력.
- .env 파일 저장.
```
OPENAI_API_KEY='sk-XXXXXXXXXX'
HUGGINGFACEHUB_API_TOKEN='hf_XXXXXXXXX'
GOOGLE_API_KEY = 'AIXXXXXXXXXXX'
LANGCHAIN_API_KEY = 'lsv2_XXXXXXXXXX'
```
- 코드 작성 후 확인
```
# API KEY를 환경변수로 관리하기 위한 설정 파일
# 설치: pip install python-dotenv
import os
from dotenv import load_dotenv

# API KEY 정보로드
load_dotenv()

# API_KEY 확인
print(f"[API KEY]\n{os.environ['OPENAI_API_KEY']}")
```

### 소스 설명
|명칭|설명|참고|
|:----------------|:---------------------------------------------------------|--------|
|[02.Prompt](https://github.com/kobongsoo/langchain/tree/master/02.Prompt)|프롬프트 관련 예제|
|[03.OutputParsers](https://github.com/kobongsoo/langchain/tree/master/02.OutputParsers)|다양한 출력 파서||
|[04.Model](https://github.com/kobongsoo/langchain/tree/master/04.Model)|다양한 LLM 모델 연동|OpenAI, 허깅페이스, 올라마|
|[05.Memory](https://github.com/kobongsoo/langchain/tree/master/05.Memory)|댜양한 메모리 연동|버퍼,토큰,엔티티,지식그래프,요약,검색 메모리|
|[06.Chain](https://github.com/kobongsoo/langchain/tree/master/06.Chain)|체인|대화형,구조화,문서요약,문서분할-병합 인등|
|[07.DocumentLoader](https://github.com/kobongsoo/langchain/tree/master/07.DocumentLoader)|파일 로딩방법|웹크롤링|
|[08.TextSplitter](https://github.com/kobongsoo/langchain/tree/master/08.TextSplitter)|텍스트 분할 방법들|문자,재귀적문자,토큰,시맨틱,코드,마크다운 분할 방법|
|[09.Embedding](https://github.com/kobongsoo/langchain/tree/master/09.Embedding)|임베딩 방법들|OpenAI,허깅페이스,GPT4ALL|
|[10.VectorStore](https://github.com/kobongsoo/langchain/tree/master/10.VectorStore)|벡터저장소들|Chroma, FAISS|
|[11.Retriever](https://github.com/kobongsoo/langchain/tree/master/11.Retriever)|검색기들|벡터,문맥압축,앙상블,긴문맥재정력,상위문서검색기,다중쿼리검색기등|
|[12.RAG](https://github.com/kobongsoo/langchain/tree/master/12.RAG)|RAG|Q&A,RAG 예시|



