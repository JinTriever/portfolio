# Neubreze Workspace

개발 중 발생하는 화면 수정 내역, 시험 기록, 사진, 일정과 주간 보고서를 한곳에서 관리하려고 만든 개인용 macOS 작업공간입니다.

## 주요 기능

- 프로젝트별 화면과 변경 내역 관리
- 작업 메모와 주간 보고서 작성
- 일정·반복 업무와 자유 페이지 관리
- 시험 사진·관찰·설문 자료 보관과 조회
- 문서 편집과 프로젝트 화이트보드
- 로컬 자료 검색, 음성 변환과 AI 초안 생성
- 로컬 저장과 암호화 백업·복원

## 구현 방식

Python 표준 라이브러리로 로컬 HTTP 서버를 만들고 SQLite에 기록을 저장했습니다. JavaScript·HTML·CSS로 화면을 구성하고 Swift·AppKit·WKWebView로 macOS 창과 메뉴, 알림·인쇄 기능을 연결했습니다.

Quill로 문서 편집을, Excalidraw로 화이트보드를 구성했습니다. 프로젝트별 메모와 변경 내역을 연결해 보고서 작성과 자료 검색에 사용할 수 있도록 만들었습니다.

Ollama와 whisper.cpp·ffmpeg를 연결해 로컬 자료 질의와 녹음 변환을 처리했습니다. AI 응답은 사용자가 검토하는 초안으로 제공했습니다. 백업은 CryptoKit·CommonCrypto·Keychain을 사용해 암호화하고, 복원 전 데이터 형식과 파일 경로를 검사하도록 구성했습니다.

## 사용 기술

Python, SQLite, JavaScript, HTML, CSS, Swift, AppKit, WKWebView, Quill, Excalidraw, Ollama, whisper.cpp, CryptoKit
