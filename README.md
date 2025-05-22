# 🧠 Local PPT Analyzer with LLM

회사 내부 보안 문서를 외부 서버(GPT API 등)에 업로드하지 않고도 분석할 수 있도록, 로컬 환경에서 실행 가능한 LLM 기반 PPT 분석 파이프라인입니다. PowerPoint(.pptx) 문서를 불러와 텍스트를 추출하고, 로컬에서 실행 중인 언어 모델을 통해 요약, 질의응답 등 다양한 자연어 처리를 수행합니다.

## 🔍 주요 기능

- PPT(.pptx) 파일에서 텍스트, 표, 이미지 등의 정보를 파싱
- 각 슬라이드에 대한 요약 및 핵심 정보 추출
- 사용자 질문에 대한 슬라이드 기반 답변 생성 (질의응답 시스템)
- 외부 API 호출 없이, 로컬에서 GPT 계열 언어모델 사용

## 💡 사용 예시

- 회사 내부 전략 문서, 사업계획서 등의 자동 요약
- 전사 회의자료 분석 및 질의응답 시스템 구축
- 보안상 외부 업로드가 불가능한 문서의 분석 자동화

## 🛠️ 사용 방법

1. 필요한 패키지 설치
    ```bash
    pip install -r requirements.txt
    ```

2. 로컬 LLM 실행 (예: `llama.cpp`, `ollama`, `lm-studio` 등)

3. Jupyter Notebook 실행
    ```bash
    jupyter notebook main.ipynb
    ```

4. PPT 파일 업로드 및 분석 실행

## 📁 폴더 구조

.
├── main.ipynb # 분석 메인 노트북
├── models/ # 로컬 LLM 파일 위치
├── slides/ # 분석 대상 PPT 파일 저장 폴더
├── outputs/ # 요약 및 응답 결과 저장
└── README.md # 프로젝트 설명 파일

markdown
복사
편집

## 🔐 보안 및 개인정보 보호

- 본 프로젝트는 회사 내부 자료 분석을 위한 **로컬 실행용**으로 제작되었습니다.
- 모든 데이터는 사용자의 로컬 머신에서만 처리되며, 외부 서버로 전송되지 않습니다.
- 언어모델 역시 로컬에 저장된 사전 학습된 모델을 사용합니다.

## 📦 요구사항

- Python 3.8 이상
- 주요 라이브러리: `python-pptx`, `langchain`, `openai` 또는 로컬 LLM wrapper (`ollama`, `llama-cpp`, etc.)

## 🧩 참고

- LangChain 또는 LCEL 기반으로 구성되어 있으며, 최신 버전 호환 확인 요망
- PPT 외에 PDF 등 다양한 문서 포맷 확장 가능

---
