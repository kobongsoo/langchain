# 랭체인(LangChain)
출처 : 위키독스 [랭체인](https://wikidocs.net/233341) ebook <br>

LangChain은 LLM 모델, 임베딩 모델을 활용해 RAG, Q&A, 요약등 다양한 애플리케이션을 개발할 수 있는 프레임워크.<br>

### 설치<br>
```
# pip
pip install langchain

# conda
conda install langchain -c conda-forge
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
