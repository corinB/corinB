Phase 1 – Source 분석 및 요구 정리
- [x] 현재 README.md에서 사용할 수 있는 문장, 이모지, 배지를 목록화
- [x] 섹션별(소개, 기술 스택, 경험)로 재배치 가능한 콘텐츠를 태그 지정
- [x] 추가 정보 금지 규칙과 placeholder 요구사항 정리

#### Phase 1 결과
- 소개 문장(원문 유지):
  - 🎓 대구대학교 컴퓨터공학과 재학
  - 💻 웹 개발과 AI/컴퓨터 비전 분야에 관심이 많습니다
  - 🤖 임베디드 시스템(Jetson Nano, Raspberry Pi, Arduino)을 활용한 프로젝트 경험
  - 🔍 YOLOv5, SSD-MobileNet-v2 등을 이용한 객체 탐지 및 컴퓨터 비전 프로젝트 수행
  - 🌐 Spring Boot와 React를 활용한 풀스택 개발 경험
  - 🤝 오픈소스 프로젝트 협업 및 Hugging Face 생태계 활용 경험
  - 💬 Python, Java, JavaScript, Computer Vision 등에 대해 언제든 물어보세요
  - 📊 데이터 분석(R, MongoDB, MySQL)부터 웹 개발까지 다양한 기술 스택 활용
- 사용 이모지: 🚀, 🎓, 💻, 🤖, 🔍, 🌐, 🤝, 💬, 📊
- 뱃지 목록:
  - 프로그래밍 언어: C, Python, Java, JavaScript, R
  - 웹 기술: HTML5, CSS3, React
  - 백엔드 & 프레임워크: Spring Boot, Flask
  - AI & 컴퓨터 비전: OpenCV, YOLOv5, Hugging Face, Le Robot, SSD-MobileNet-v2, SmoVLM
  - 데이터베이스: MySQL, MongoDB
  - 하드웨어: Jetson Nano, Raspberry Pi, Arduino
  - 운영체제 & 도구: Linux, Raspbian, JetPack, Git, GitHub
- 재배치 태그:
  - 학력·관심: 🎓, 💻
  - 임베디드·컴퓨터 비전: 🤖, 🔍
  - 풀스택·협업: 🌐, 🤝
  - 상담/문의: 💬
  - 데이터·기술 범위: 📊
- 제약 요약: README 외 신규 정보 금지, placeholder 필수, JS/CSS 사용 금지, 이미지 ALT 필수, 500KB 이하 권장, 120자 줄바꿈 유지

Phase 2 – 섹션 아키텍처 설계
- [x] Hero부터 Footer까지 7개 섹션의 순서와 핵심 메시지 결정
- [x] 각 섹션에 배치될 Bullet/문장 길이, 줄바꿈 가이드 정의
- [x] 카드형 표현을 위한 Markdown/제한적 HTML 패턴 시나리오 수립

#### Phase 2 결과
- 섹션 순서 및 핵심 메시지:
  - Hero: 한 줄 요약(학력·관심) + {HERO_GIF_URL}, {TYPING_SVG_URL}
  - About: 4–5줄 bullet로 학력, 관심, 프로젝트 범위, 협업 강조
  - Tech Stack: 카테고리별 배지 묶음, 가로 구분선과 소제목 유지
  - Projects: 임베디드, 객체 탐지, 풀스택 경험을 카드 3개로 요약
  - Stats: 기여도·활동 지표 2개 카드와 짧은 설명
  - Contact: 문의 문장과 {BADGE_CONTACT}, {CONTACT_LINK_*}
  - Footer: {FOOTER_NOTE} 문구와 업데이트 안내
- 줄바꿈·문장 가이드:
  - Hero CTA는 2~3줄 내, 120자 이하, 이모지 최소화
  - About bullet은 항목당 1줄, 필요 시 쉼표 구분
  - 카드 형식 문장은 제목 + 한 줄 설명 + 배지/placeholder 조합
  - Stats/Projects는 빈 줄로 카드 구분, HTML `<br>` 최소화
- 카드 표현 패턴:
  - `> 💡` 스타일 인용구나 굵은 제목으로 카드 헤더 연출
  - 수평선(`---`)으로 카드 그룹 분리
  - 이미지 placeholder는 `<img>` 태그 사용, 텍스트와 줄 바꿈으로 간격 확보

Phase 3 – 애니메이션 감각 및 시각 요소 계획
- [x] {HERO_GIF_URL}, {TYPING_SVG_URL} 배치 위치와 ALT 문구 초안 작성
- [x] Shields.io 뱃지 재배열 로직과 색 대비 체크리스트 마련
- [x] Projects/Stats 카드에 사용할 {PROJECT_*}, {STATS_*} placeholder 구성안 작성

#### Phase 3 결과
- Hero 시각 요소:
  - {HERO_GIF_URL}를 상단 좌측에 `<img>` 배치, ALT "히어로 애니메이션" 문구 예상
  - {TYPING_SVG_URL}를 이름 아래에 `<img>`로 배치, ALT "타이핑 효과 소개" 계획
  - 두 이미지 모두 `<!-- replace here: ... -->` 주석 포함
- 뱃지 재배열 로직:
  - for-the-badge 스타일 유지, 카테고리별 3~6개로 묶어 가독성 확보
  - 다크 테마 대비 문제되는 배지(예: JavaScript 노란색)에는 인라인 텍스트 설명 추가 고려
  - 섹션 단위로 뱃지 묶음 사이 공백 줄 1개 유지, 렌더링 시 줄바꿈 자연스럽게 유도
- Projects/Stats placeholder 구성:
  - Projects: {PROJECT_1_IMG} (임베디드), {PROJECT_2_IMG} (객체 탐지), {PROJECT_3_IMG} (풀스택)
  - 각 카드에 `<img>` + 간단 설명 + 관련 배지 조합
  - Stats: {STATS_1_URL} (활동 요약), {STATS_2_URL} (연속 기여) 이미지, ALT 문구 각각 "GitHub 활동 그래프", "기여 스트릭"
  - 이미지 용량 500KB 이하 확인 메모
- 추가 시각 규칙:
  - Hero와 Projects 사이에 구분선을 사용해 섹션 전환감 부여
  - Stats 섹션에 shields.io dynamic badge {BADGE_STATS} 배치로 변동성 강조

Phase 4 – 접근성·성능 가드레일 수립
- [x] ALT 텍스트, 120자 줄바꿈, 이모지 절제 등 규칙 명문화
- [x] 다크/라이트 테마 대비와 이미지 용량(≤500KB) 확인 절차 기록
- [x] 외부 링크 placeholder 주석 작성 규칙 정리

#### Phase 4 결과
- 접근성 규칙:
  - 모든 이미지에 의미 있는 ALT 문구 작성, 언어는 한글 유지
  - 줄당 120자 이하 유지, 긴 나열은 쉼표 또는 세미콜론으로 분리
  - 이모지는 제목과 핵심 포인트에서만 사용, 같은 이모지 반복 최소화
  - 링크 텍스트는 명확한 목적을 드러내도록 작성(예: "프로젝트 보기")
- 성능 규칙:
  - Placeholder용 이미지도 500KB 이하 파일 사용, 교체 전 확인 메모 포함
  - GIF/SVG는 지연 없이 로드되도록 외부 호스팅 품질 확인 권장
  - 중복 뱃지 호출 최소화, 동일한 shields.io URL 반복 사용 지양
- Placeholder 주석 규칙:
  - `<img src="{...}">` 바로 다음 줄에 `<!-- replace here: ... -->` 주석 삽입
  - 링크 placeholder는 `[텍스트]({CONTACT_LINK_*}) <!-- replace here: contact link -->` 형식 채택
  - 통계/프로젝트 이미지 동일한 주석 패턴 유지

Phase 5 – 검증 및 인계 체크리스트 작성
- [x] markdownlint, link-check, 렌더링 미리보기 절차 정리
- [x] Placeholder 교체 시점과 주석 유지 조건 정의
- [x] 최종 README.md 산출물 출력 방식 및 계약(단일 코드 블록) 명시

#### Phase 5 결과
- 검증 절차:
  - `npm run lint:md` 또는 `npx markdownlint "**/*.md"` 실행
  - `npx markdown-link-check README.md`로 링크 상태 확인(placeholder 제외 주석으로 명시)
  - GitHub 미리보기 사용해 다크/라이트 테마 렌더링 확인
- Placeholder 교체 가이드:
  - 실 URL 삽입 시 주석 `<!-- replace here: ... -->` 유지, 교체 완료 메모 추가 가능
  - 이미지 교체 후 ALT 텍스트 확인 및 필요 시 용량 재확인
  - 뱃지 변경 시 shields.io 파라미터 검토(스타일, 색상)
- 출력 계약:
  - 구현 단계에서 README 전체를 하나의 ```markdown 코드블록으로 제공
  - 헤더, 리스트 등 Markdown 표준만 사용, JS/CSS 삽입 금지
  - 완료 후 lint/링크 체크 실행 안내 포함
