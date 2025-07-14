📌 농업 종사자를 위한 챗봇
한국 농업 기술센터의 「가뭄 대비 농작물 관리 요령」 문서를 기반으로, 농업 종사자에게 맞춤형 상담을 제공하는 챗봇 애플리케이션입니다.

LangChain과 벡터 검색을 활용해, PDF의 세부 내용을 검색해 답변할 수 있도록 설계되었습니다.

🌾 주요 기능
✅ PDF 문서 벡터화 및 검색
✅ LLM을 통한 문맥 기반 질문 응답
✅ Streamlit UI로 실시간 채팅
✅ 대화 이력 관리 (세션별 Memory)
✅ 농업 전문가의 어조로 응답

📂 폴더 및 파일 구조
css
복사
편집
.
├── README.md         ← 이 문서
├── main.py           ← LangChain 체인 생성, 벡터스토어 관리
├── app.py            ← Streamlit 웹앱 UI
├── farm/             ← 벡터스토어 디렉토리 (Chroma DB)
├── parent_docstore/  ← ParentDocumentRetriever의 저장소
├── sqlite_cache/     ← LLM 응답 캐시 (선택)
└── 가뭄 대비 농작물 관리 요령.pdf ← 참고 자료
🛠️ 기술 스택
Python 3.10+

LangChain (OpenAI / Chroma / Memory)

Streamlit

OpenAI GPT-4.1, GPT-4.1-nano

Dotenv (환경 변수 관리)

⚙️ 설치 및 실행
1️⃣ 의존성 설치
bash
복사
편집
pip install -r requirements.txt
예: langchain, streamlit, langchain-openai, chromadb, python-dotenv

2️⃣ .env 파일 생성
ini
복사
편집
OPENAI_API_KEY=your_openai_key_here
3️⃣ PDF를 벡터 DB로 임베딩
(main.py 내 load_vector_store 함수로 자동화 지원 예정)

4️⃣ 앱 실행
bash
복사
편집
streamlit run app.py
🧭 사용 방법
웹 UI에서 질문 입력

PDF 문서 내용 기반으로 답변 생성

대화 이력 관리로 연속적 질문 가능

📑 참고 자료 – 가뭄 대비 농작물 관리 요령
제주지역 최근 강수량 부족 현황

작목별 피해 및 관리 대책:

감자: 싹 출현기~괴경비대기에 수분 부족시 상품율 저하 → 스프링클러 관수, 비닐피복

노지감귤: 착색 지연 → 정기적 관수, 피복

당근: 파종 후 관수 시설 설치 → 수량 증가

마늘: 파종 후, 구 비대기 관수 필수 → 엽선단 고사 방지

브로콜리: 육묘·정식 후 수분 관리 → 시들음 방지

양배추: 90%가 수분 → 관수 시설 필수

월동무: 발아 불량·열근 방지 → 적정 관수

콜라비: 정식기 뿌리활착 → 수분 관리

관수 시점: 저녁~아침 시간대 증발량 적음

건조 기후 시 해충(총채벌레·응애·노린재) 증가 → 살충제 살포 권장

(📖 출처: 가뭄 대비 농작물 관리 요령.pdf 전체 내용 포함)
