# 운전자 보험 약관 RAG 챗봇


## ✅ 프로젝트 배경 및 목적

- **운전자 보험 약관은 너무 복잡하여 고객이 원하는 정보를 직접 찾아내기 어려움**
- **따라서 방대한 약관 속에서 핵심 정보를 추출하여 사용자가 궁금한 내용을 신뢰성 있게 확인할 수 있는 RAG 챗봇 모델 설계**
  
<br/>

## 👤 대상 사용자

- **운전자보험 약관을 손쉽게 확인하고 싶은 일반 가입자**
- **보험 상품 가입을 고려하는 사용자**
  
<br/>


## 💡 전체 플로우
<img width="954" height="600" alt="image" src="https://github.com/user-attachments/assets/6a6701d0-231a-446a-981f-ad62b133ab0c" />

* **데이터 전처리**
  * PDF -> PyPDFLoader로 로드 -> RecursiveCharacterTextSplitter 문서 청크
* **임베딩 및 저장**
  * OpenAIEmbeddings를 사용하여 벡터로 변환 -> postgreSQL에 저장
* **다중 검색**
  * EnsembleRetriever를 활용하여 동시에 문서를 검색 -> 가장 관련성 높은 문서
* **질의응답**
  * LLM의 컨텍스트로 전달 -> 답변 생성 및 출처 제공


<br/>

## ❤️ 기대효과

* **가입자 만족도 및 신뢰도 향상**
  *  필요한 정보를 쉽고 빠르게 얻을 수 있음
  *  정확한 출처 제공으로 답변의 신뢰도가 향상됨 
* **콜센터 업무 효율 증대**
  *  다양한 상황에 대한 응대를 챗봇이 대신함으로써 직원들이 더 복잡하고 전문적인 상담에 집중할 수 있게 되어 업무 효율이 증대됨
* **정보 비대칭성 완화**
  *  보험사는 방대한 정보를 제공하지만, 사용자는 이를 모두 파악하기 어려움
* **확장성 및 유지보수 용이**
  *  새로운 보험 상품이 출시되거나 약관이 개정될 경우, 해당 문서만 추가하면 즉시 반영되어 유지보수가 편리함

<br/>

## 🛠️ 기술 스택

| 항목    | 내용     |
| ---------- | ---------- |
| Language    | <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white">  <img src="https://img.shields.io/badge/sql-4479A1?style=for-the-badge&logo=sql&logoColor=white"> |
| Development    |<img src="https://img.shields.io/badge/streamlit-7952B3?style=for-the-badge&logo=streamlit&logoColor=white"> <img src="https://img.shields.io/badge/Visual Studio Code-61DAFB?style=for-the-badge&logo=VisualStudioCode&logoColor=white"> <img src="https://img.shields.io/badge/langchain-1C3C3C?style=for-the-badge&logo=openai&logoColor=white"> <img src="https://img.shields.io/badge/RAG-FFCA28?style=for-the-badge&logo=rag&logoColor=white">|
| Embedding    | <img src="https://img.shields.io/badge/OpenAIEmbedding-181717?style=for-the-badge&logo=openai&logoColor=white">     |
| LLM Model    | <img src="https://img.shields.io/badge/chatgpt_4.1-3776AB?style=for-the-badge&logo=openai&logoColor=white">      |
| Collaboration Tool    | <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white"> <img src="https://img.shields.io/badge/Discord-02569B?style=for-the-badge&logo=Discord&logoColor=white">     |
| Vector DB    |<img src="https://img.shields.io/badge/pgvector-00599C?style=for-the-badge&logo=pgvector&logoColor=white"> <img src="https://img.shields.io/badge/psycopg2-3776AB?style=for-the-badge&logo=psycopg2&logoColor=white"> <img src="https://img.shields.io/badge/PostgreSQL-0769AD?style=for-the-badge&logo=postgresql&logoColor=white">    |
| API    | <img src="https://img.shields.io/badge/OpenAI API-181717?style=for-the-badge&logo=openai&logoColor=white">    |

<br/>


## 👉 수행결과

### ➤  Vector DB
| Collection    | Embedding     |
| ---------- | ---------- |
| <img width="600" height="300" alt="Image" src="https://github.com/user-attachments/assets/b77924a7-8c06-46e1-897d-e2baa56e0c69" /> | <img width="600" height="300" alt="Image" src="https://github.com/user-attachments/assets/6dc37fde-1434-450c-847e-9f1b7b1146cb" />  |


### ➤  최종 Prompt
<img width="1051" height="586" alt="image" src="https://github.com/user-attachments/assets/eca515c7-8a6a-46ad-a202-18802e0c89a8" />



### ➤  성능 평가
<img width="1948" height="1082" alt="image" src="https://github.com/user-attachments/assets/68f4e85a-ec23-496a-bf18-d5dabe4473d2" />





<br/>

## 👁️‍🗨️ Streamlit 
<img width="1904" height="862" alt="image" src="https://github.com/user-attachments/assets/bd301631-a6d8-4e7f-be65-0e5536850647" />



### ✧ 연령별 추천

| 30대 | 40대 | 특정 나이|
|-----|-----|-----|
| <img width="1100" height="751" alt="Image" src="https://github.com/user-attachments/assets/6eb04024-738b-477f-8560-3dbe02202ddb" />| <img width="1071" height="754" alt="Image" src="https://github.com/user-attachments/assets/e6fc8763-70fb-48e5-b9bd-517e85a40c45" /> | <img width="1440" height="685" alt="image" src="https://github.com/user-attachments/assets/ae4ee676-574a-4c32-8931-929ef851a7ce" /> |


### ✧ 상황별 (횡단보도에서 무단횡단 보행자 사고 났을때)

| | | |
|-----|-----|-----|
| <img width="1094" height="803" alt="Image" src="https://github.com/user-attachments/assets/b91b9abb-6565-4110-8153-c555f8e3aaaf" />| <img width="1029" height="694" alt="Image" src="https://github.com/user-attachments/assets/4ec8e3d9-7886-46f4-b395-9343a9d57860" /> |<img width="1071" height="871" alt="Image" src="https://github.com/user-attachments/assets/4e50635f-1a7c-4cb6-9067-5db611d23ab3" /> |



<br/>

## 🔖 프로젝트 확장성

* 다양한 보험 상품으로의 적용 가능
* 판례 데이터 반영
  * 파인 튜닝(Fine-Tuning)을 통한 판례 기반의 추론 강화
  * 법적 기반을 통한 방향성 확보
  * 챗봇이 더욱 풍부한 역할 가능
