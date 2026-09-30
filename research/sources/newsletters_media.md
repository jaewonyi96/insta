# 뉴스레터·미디어·공식 채널 소스 검증본 (newsletters_media)

- 작성일: 2026-09-30
- 대상: 한국형 매거진 큐레이션 인스타 계정(@ai_freaks.kr의 AI 뉴스·재미, @romaan.mag의 AI 해설, @bizucafe의 비즈니스 기사와 코멘트, @ekke.now의 돈·경제·라이프스타일)을 운영하면서 **매일 보고 한국어 게시물로 바꿀 뉴스레터, 매체, 공식 블로그·데이터, 유튜브**
- 결과: 초안 60개 검증
  - **57개 유지**(그중 20여 개는 URL, 속도, 수치, 소속을 고침)
  - **3개는 표에서 빼서 부록 '벤치마크'로 옮김**(BZCF 텔레그램, 롱블랙, 폴인)
  - 가짜이거나 폐쇄된 소스는 **0개**
  - **10개 추가** → 최종 표 67개
- 같이 볼 파일: `x_ai.md`(X 계정), `source-tracing.md`(4개 계정이 실제로 인용한 원문 역추적)

---

## 1. 개요

### 1-1. 검증 방법

- 이번 단계에서 **WebSearch 38회**를 썼습니다(한도 40회).
  - Tier 1 후보와 휴면·개명 의심 항목을 먼저 확인했습니다.
  - WebFetch, curl, 브라우저는 쓰지 않았습니다. 그래서 모든 근거는 **검색 결과의 제목, URL, 요약**입니다.
- '검증' 칸의 표기는 다음 뜻입니다.

| 표기 | 뜻 |
|---|---|
| **확인 2026-MM** | 이번 검색에서 그 달의 게시물이나 발행이 확인됨 |
| **확인(존재)** | 주소와 운영 주체는 확인됨. 2026년 활동은 검색에 잡히지 않음 |
| **이전 조사 확인** | 같은 세션의 앞선 조사 파일(`source-tracing.md`, `../landscape.md`, `../best-practices.md`)에 검색 근거가 남아 있음 |
| **미검증** | 이번 예산 안에서 확인하지 못함. 존재는 확실한 대형 매체·기관만 이 표기로 남김 |

- 구독자·팔로워 수는 **검색 요약에 나온 값**을 옮긴 것입니다. 기준일이 없으면 '날짜 미상'으로 적었습니다.
- 표 이름 앞의 **[T1]/[T2]/[T3]**는 모니터링 주기입니다.
  - **T1**: 매일 봄
  - **T2**: 주 2~3회 또는 주간
  - **T3**: 월간, 비정기, 필요할 때
- **[추가]**는 초안에 없던 소스입니다.

### 1-2. 모니터링 스택 (권장)

| 도구 | 넣을 것 |
|---|---|
| **별도 Gmail + 라벨** (`AI-NL`, `BIZ-NL`, `KR-ECON`) | 이메일 뉴스레터 전부 |
| **RSS 리더 한 곳** (Feedly, Inoreader 등) | 공식 RSS가 확인된 곳, Substack(`주소/feed`), 매체 사이트(주소를 넣으면 리더가 피드를 자동으로 찾음) |
| **유튜브 RSS** | `https://www.youtube.com/feeds/videos.xml?channel_id=채널ID` (유튜브 표준 형식). 채널 ID는 표에 적음 |
| **네이버 뉴스 언론사 구독** | 한국 매체 |
| **캘린더** | 금통위, 통계 공표 일정, 실적 시즌(1~4월), 빅테크 행사 |

**하루 루틴 (KST)**
1. **아침**: 한국 매체, DART, 정책브리핑, GeekNews를 보고, 밤사이 온 미국 공식 발표를 확인합니다.
2. **저녁~밤**: 미국 일간 뉴스레터(The Rundown, TLDR AI, Axios AI+)와 Techmeme을 봅니다.

### 1-3. 쓰기 원칙

- **요약본은 소재 찾기에만 씁니다.** 뉴스레터, 애그리게이터, 한국 번역 기사에서 소재를 찾으면, 사실은 **공식 발표나 원 기사**로 다시 확인합니다.
- **유료 매체는 '매체명 + 날짜 + 요지'만 씁니다.** 해당 매체: The Information, Bloomberg, FT, Stratechery, 롱블랙, 폴인. 전문을 번역하거나 캡처하면 안 됩니다.
- **원문을 직접 읽고, 내 문장과 해설로 다시 써서, 직접 디자인해야 합니다.**
  - 인스타는 2026-04-30부터 남의 콘텐츠를 주로 재게시하는 계정을 사진·캐러셀 추천에서 뺍니다(`../best-practices.md`, TechCrunch 2026-04-30).
  - 기사 사진, 영상 캡처, 경쟁 큐레이터의 번역문은 가져오지 않습니다.

---

## 2. 추천 소스 표

### A. 글로벌 AI 뉴스레터·블로그

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| **[T1] The Rundown AI** | therundown.ai (X @TheRundownAI, Threads @therundownai) | AI 뉴스 일간 요약 | 영어 | 일간. 미국 아침 발송이라 한국은 저녁~밤 도착 | 높음 | 이메일 → 라벨 `AI-NL` | '오늘의 AI 3줄', 'N월 N주차 AI 소식' 라운드업의 체크리스트. 자매지로 Rundown Tech, Rundown Robotics가 있음 | 요약본이니 공식 원문으로 재확인. 창업자 Rowan Cheung의 X는 2026년 게시물이 확인되지 않음(`x_ai.md`)이라 **뉴스레터를 주 채널로** | **확인 2026**: 플래그십 200만+ 구독, 네트워크 추가 약 80만(2026 리뷰 기사) |
| **[T2] The Neuron** | **theneuron.ai** (구 theneurondaily.com, IG @theneurondaily) | AI 뉴스·툴, 비개발자용 | 영어 | 일간 | 높음 | 이메일, IG | 가볍고 웃긴 AI 소식을 고르는 기준과 톤을 AI Freaks식 '괴짜' 톤에 참고 | **2025-01 TechnologyAdvice에 인수됨**(TechRepublic 등 20여 브랜드를 가진 B2B 테크 퍼블리셔). 광고·제휴 콘텐츠와 구분할 것. 밈 이미지 재사용 금지 | **확인**: 인수 발표(2025-01), 당시 구독 50만+. 초안의 '약 70만'은 근거가 없어 지움. 주소를 theneuron.ai로 고침 |
| **[T1] TLDR AI** | tldr.tech/ai | AI 연구·엔지니어링·툴 | 영어 | 평일 일간 | 높음 | 이메일, 웹 아카이브 | 오픈소스 모델, 논문, 개발 툴 링크를 빠르게 훑기. 깊게 다룰 주제 고르기 | 한 줄 링크 모음이라 원문 필수. 스폰서 링크가 섞임 | **확인 2026**: 약 110만 구독(2026 리뷰 기사) |
| **[T2] Ben's Bites** | bensbites.com (Substack. 구 bensbites.co) | AI 빌더·툴·에이전트 활용 | 영어 | **주 2회(화·목)** | 중간 | 이메일, `bensbites.com/feed`(Substack) | '이렇게 써보세요' 활용법 카드 | 커뮤니티는 유료(연 80달러), 글은 무료와 유료가 섞임. 초안의 '일간~주 수회'는 틀려서 고침 | **확인 2026**: 약 12만 구독(2026-03 기사). 2026년 주제는 '에이전트로 만들기' |
| **[T2] Import AI (Jack Clark)** | **jack-clark.net**(주 아카이브), importai.substack.com | AI 연구·정책 해설 | 영어 | 주간 | 높음 | 이메일. RSS 리더에 jack-clark.net 입력 | 로만식 '이 논문이 의미하는 것' 해설의 재료 | 필자가 앤트로픽 공동창업자라 이해관계를 밝힐 것. 글 끝의 짧은 소설(픽션)을 사실로 옮기지 말 것 | **확인 2026-06**: 459호(2026-06-01)까지 확인. 주간 독자 7만(사이트 표기). 7월 이후 호는 검색에 없음 |
| **[T2] Last Week in AI** | lastweekin.ai (팟캐스트 Apple, Spotify, 유튜브 채널 ID UCKARTq-t5SPMzwtft8FWwnA) | 주간 AI 뉴스 정리 | 영어 | 주간 | 높음 | 이메일, 팟캐스트 앱 | 주간 라운드업에서 빠진 소식이 없는지 점검 | 2차 정리물이니 원문 링크로 확인 | **확인 2026-09**: 257회(2026-09-19 녹화). 진행자 Andrey Kurenkov, Jeremie Harris |
| **[T3] Latent Space** | latent.space (팟캐스트 latent.space/podcast) | AI 엔지니어링, 창업자·연구자 인터뷰 | 영어 | 주간 | 높음 | `latent.space/feed`(Substack), 팟캐스트 | '인터뷰 중 인상 깊은 발언 3가지' 카드 | 전문적이라 대중용으로 풀 때 오역 주의. 인터뷰 전문 번역은 허락 필요 | **확인(존재)**: 자체 표기로 2025년 독자·청취자 1,000만+. 2026년 회차는 검색에 없음 |
| **[T2] AINews (smol.ai)** | news.smol.ai (구독 news.smol.ai/subscribe) | X, Reddit, Discord의 AI 화제 자동 요약 | 영어 | 일간 | 중간 | 이메일, 웹 아카이브(검색 가능) | '오늘 개발자들이 떠든 것'을 한 번에 파악 | AI가 만든 요약이라 원 게시물 확인 필수. 분량이 매우 김. 구 Buttondown 주소는 이전됨 | **확인 2026-02**: 2026-02-20호(서브레딧 12개, X 계정 544개, Discord 24개 점검) |
| **[T2] Interconnects (Nathan Lambert)** | interconnects.ai | 오픈 모델, 강화학습, 후처리 학습, 중국 오픈 모델 | 영어 | 주 1~2회 | 높음 | `interconnects.ai/feed`(Substack) | '딥시크·큐웬이 왜 중요한가' 같은 해설형 카드의 근거 | 관점이 강하니 의견과 사실을 구분. **필자가 2026-06 Ai2를 떠나 새 프로젝트로 옮김**. 'Ai2 연구자'로 소개하면 틀림 | **확인 2026**: 'My bets on open models, mid-2026', 'State of the blog mid-2026' |
| **[T2] The Batch (DeepLearning.AI)** | deeplearning.ai/the-batch (X @DeepLearningAI) | 앤드루 응의 편지 + 주간 AI 뉴스 | 영어 | 주간 | 높음 | 이메일 | '앤드루 응이 말하는 ○○' 인용 카드, 교육형 해설 | 인용할 때 발행일과 편지 원문 명시 | **확인 2026-09**: 370호(2026-09-11), 편지는 2026-09-25까지 |
| **[T1] One Useful Thing (Ethan Mollick)** | oneusefulthing.org | AI 활용, 일의 미래 | 영어 | 월 2~4회 | 높음 | `oneusefulthing.org/feed`(Substack), X | 비개발자용 해설. 'Summer 2026 어떤 AI를 쓸까' 가이드는 툴 비교 카드의 뼈대가 됨 | 에세이 전문 번역은 허락 필요. 요지와 출처만 | **확인 2026-08**: 2026-08-31 'Agency and Agents' 외 |
| **[추가][T2] Simon Willison's Weblog** | simonwillison.net | LLM 실사용, 개발 툴, 프롬프트 인젝션 | 영어 | 거의 매일 | 높음 | RSS 리더에 사이트 주소 입력 | 신모델을 직접 써 본 기록. '2026 in LLMs (so far)'(2026-09-27) 같은 정리 글은 로만식 해설 카드의 뼈대 | 개인 블로그라 의견이 섞임. 발언은 필자 이름으로 인용 | **확인 2026-09** |
| **[추가][T2] MIT Technology Review (The Algorithm, The Download)** | technologyreview.com (The Algorithm 구독 forms.technologyreview.com/newsletters/ai-demystified-the-algorithm/) | AI 해설, 과학·사회 영향 | 영어 | The Algorithm은 주간(월), The Download는 평일 | 높음 | 이메일 | 'AI가 과학적 발견을 했다고 언제 말할 수 있나'(2026-09-28) 같은 해설 기사 → 로만식 깊이 있는 카드 | 일부 기사 유료 | **확인 2026-09** |

### B. 글로벌 미디어·애그리게이터

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| **[T1] Techmeme** | techmeme.com (X @Techmeme) | 테크 업계 1면 애그리게이터 | 영어 | 수분~수시간 | 높음 | RSS(`techmeme.com/feed.xml`로 알려짐. 안 되면 사이트 주소 입력). KST 아침·저녁 2회 | 오늘 가장 큰 테크·AI 비즈니스 뉴스와 여러 매체를 교차 검증 | 링크 집합이라 원 기사 확인. X 게시물에는 링크가 빠짐(`x_ai.md`) | **이전 조사 확인**(사이트 2026 활동). RSS 주소는 미검증 |
| **[T1] Axios AI+** | axios.com/technology (구독 axios.com/signup/ai-plus) | AI 산업, 정책, 투자 흐름 | 영어 | 평일 일간 | 높음 | 이메일 | '왜 중요한가' 중심의 짧은 구조(Smart Brevity)가 카드뉴스 문법과 거의 같음 | 구조만 참고하고 문장은 복제하지 말 것 | **확인 2026**: 일간 AI+를 Ina Fried와 Madison Mills(2026-02 합류)가 공동 집필. 이전 조사에서 2026-09-12 아모데이 기사 확인 |
| **[T1] The Decoder** | the-decoder.com | 모델 출시, 벤치마크, AI 비즈니스 | 영어 | 수시간 | 높음 | RSS 리더에 사이트 주소 입력, 뉴스레터 | '이번 주 신모델', AI 지출·가격 추세 카드(예: Ramp AI Index 기사) | 벤치마크 수치는 원 논문이나 공식 발표로 확인 | **확인 2026-09** |
| **[T2] TechCrunch** | techcrunch.com (RSS techcrunch.com/feed/, X @TechCrunch) | 스타트업 투자, 출시 속보 | 영어 | 수시간 | 중간 | RSS | BZCF가 실제로 인용한 원천(Cursor 밸류에이션, 스타인버거의 OpenAI 합류 등) | 투자 수치는 회사 공식 발표와 대조 | **이전 조사 확인**(2026-02 기사). RSS 주소는 미검증 |
| **[T2] Bloomberg Technology** | bloomberg.com/technology (X @technology) | AI 스타트업 밸류에이션 단독 | 영어 | 1차 단독 | 높음 | 무료 뉴스레터 헤드라인, X | 숫자 중심 비즈니스 카드. BZCF가 Lovable·Anysphere 보도를 카드로 옮김 | 유료. 요지와 출처만 | **이전 조사 확인** |
| **[T2] The Information** | theinformation.com | AI 기업 매출, 인재 이동, 투자 단독 | 영어 | 1차 단독 | 높음 | 무료 헤드라인 이메일, X | 다른 매체가 'The Information에 따르면'으로 재인용하는 단독을 가장 먼저 포착 | 고가 유료. '○○에 따르면' 형식으로 요지만 | 미검증(존재 확실) |
| **[T2] Stratechery (Ben Thompson)** | stratechery.com | 빅테크·AI 비즈니스 전략 | 영어 | 주 수회(무료 글은 주 1회 정도) | 높음 | 무료 글 이메일, 팟캐스트 | '이 발표가 사업적으로 의미하는 것' 같은 해석 관점 | 유료 글 전재·번역 금지. 필자 명시 | 미검증 |
| **[T2] Platformer (Casey Newton)** | platformer.news | 플랫폼 정책, AI 규제, 메타·인스타 정책 | 영어 | 주 수회 | 높음 | 이메일, Hard Fork 팟캐스트 | 콘텐츠 소재이자, 인스타 알고리즘·정책 변화를 빨리 아는 레이더 | 유료 부분은 요지만 | 미검증 |
| **[추가][T2] 404 Media** | 404media.co (AI 태그 404media.co/tag/ai/, AI 슬롭 태그 404media.co/tag/ai-slop/) | 기괴한 AI, AI 슬롭, 탐사 보도 | 영어 | 주 수회 | 높음 | 이메일, 팟캐스트 | AI Freaks식 '이상한 AI' 소재. 근거가 탄탄한 탐사형(예: LinkedIn이 AI 슬롭 신고 기능 도입(2026-07), 도서관 전자책 서비스의 AI 생성 책 정리) | 일부 기사는 회원 전용 | **확인 2026** |
| **[T3] The Verge (AI 섹션)** | theverge.com/ai-artificial-intelligence | 소비자 AI 제품, 리뷰 | 영어 | 수시간 | 중간 | RSS 리더에 섹션 주소 입력 | '새로 나온 ○○ 써보니' 대중형 카드 | 기사 사진 저작권 | 미검증 |
| **[T3] Financial Times** | ft.com (X @FT) | 거시경제, 빅테크 전략 | 영어 | 수시간 | 높음 | 무료 헤드라인 뉴스레터 | 경제·비즈니스 해설(BZCF의 'K자형 경제' 사례) | 유료. 매체명·날짜·요지만 | **이전 조사 확인**(BZCF 인용으로 간접) |
| **[T3] CNBC Tech** | cnbc.com/technology | 빅테크 계약·실적 속보, CEO 방송 인터뷰 | 영어 | 수시간 | 중간 | RSS, 유튜브 CNBC | CEO 발언 인용 카드(BZCF OpenAI×AMD 사례의 원문 중 하나) | 방송 캡처 금지 | **이전 조사 확인**(2025-10 기사) |
| **[T3] Lenny's Newsletter / Podcast** | lennysnewsletter.com | PM, 그로스, AI 제품 리더 인터뷰 | 영어 | 주간 | 높음 | `lennysnewsletter.com/feed`(Substack), 유튜브 | 'OOO 인터뷰 중 좋았던 것 3가지', 커리어 카드 | 발언자와 에피소드 명시 | 미검증 |
| **[T3] a16z** | a16z.com (뉴스레터 a16z.com/newsletter, X @a16z) | VC 리포트(Big Ideas, 소비자 AI 앱 순위) | 영어 | 주간 + 시즌 리포트 | 높음 | 뉴스레터 | 'VC가 투자하겠다는 분야 N개' 리스트 카드. BZCF가 Big Ideas 2026을 약 10일 뒤 번역 | 포트폴리오 홍보 가능성. 차트는 출처 표기 | **이전 조사 확인** |
| **[T3] Sequoia Capital** | sequoiacap.com (Training Data 팟캐스트) | VC 에세이, AI Ascent, 창업자 인터뷰 | 영어 | 비정기 | 높음 | 팟캐스트 앱 | '최상위 VC가 보는 AI 시장' 해설 | 투자사 관점 표기 | 미검증 |

### C. 글로벌 공식 발표·데이터

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| **[T1] OpenAI News / ChatGPT 릴리스 노트** | openai.com/news, 릴리스 노트 help.openai.com, X @OpenAI | 1차 발표(모델, 제품, 파트너십) | 영어 | 1차 | 높음 | **공식 RSS `https://openai.com/news/rss.xml`**, X 알림 | 'ChatGPT 새 기능 사용법' 카드의 근거. BZCF가 OpenAI×AMD 발표를 1일 안에 카드로 만듦 | 마케팅 표현과 사실 구분. 공식 이미지는 이용 조건 확인 | **확인**: 공식 RSS 존재(개발자 커뮤니티, Feeder) |
| **[T1] Anthropic News** | anthropic.com/news, X @AnthropicAI | 1차 발표(Claude, 정책, 연구, CEO 에세이) | 영어 | 1차 | 높음 | X 알림, 페이지 확인. 공식 RSS는 확인 못함(제3자 변환 피드만 보임) | 해석형 매거진의 핵심 원천(bzcf.io가 아모데이 에세이를 전문 번역) | 자사 관점이라 경쟁사 비교에 주의 | 미검증(존재 확실) |
| **[T1] Google Blog (AI) / Google DeepMind** | blog.google/technology/ai/, deepmind.google, X @GoogleDeepMind | 1차 발표(Gemini, 영상·이미지 모델, 연구) | 영어 | 1차 | 높음 | RSS 리더에 블로그 주소 입력, X | 'AI로 이런 것까지' 데모와 신기능 카드 | 데모 영상 재업로드 금지, 공식 링크 사용 | 미검증(존재 확실) |
| **[T1] Hugging Face Papers (Daily, Trending)** | huggingface.co/papers | 논문, 인기 모델·데모 | 영어 | 일간 | 중간 | 하루 1회 페이지 확인. X @HuggingPapers(`x_ai.md`) | 오픈소스 모델 소식과 'AI로 이런 것도' 소재를 가장 빨리 봄 | 동료 심사 전 논문이 많으니 '발표'가 아니라 '연구 공개'로 표현 | **확인**: Papers with Code가 **2025-07-24 종료**되어 HF Trending Papers로 리디렉트됨(초안의 추정이 맞음) |
| **[추가][T2] Arena (구 LMArena)** | arena.ai (리더보드 변경 로그 arena.ai/company/leaderboard-changelog) | 사용자 블라인드 투표 모델 순위(텍스트, 코드, 영상) | 영어 | 수시 | 높음 | 변경 로그 주 1~2회 확인 | '이번 주 1위 모델' 카드 | **2026-01-28 LMArena → Arena로 개명**. lmarena.ai 링크는 대체로 리디렉트됨. 투표 순위라 말투·형식 선호가 반영된다는 비판이 있음. 순위표 캡처 대신 수치를 옮겨 직접 도표화 | **확인 2026** |
| **[추가][T2] Artificial Analysis** | artificialanalysis.ai (Intelligence Index) | 모델 지능·속도·가격 비교 | 영어 | 수시 | 높음 | 사이트 확인(신모델 나올 때) | '가성비 모델 순위', '가격 대비 성능' 카드 | 지수 버전이 자주 바뀜(v4.x) → 버전과 날짜 표기. 제3자 요약 사이트 수치는 쓰지 말 것 | **확인 2026** |
| **[추가][T3] Epoch AI** | epoch.ai/data-insights, 뉴스레터 The Epoch Brief(epochai.substack.com) | AI 컴퓨트·비용·칩 추세 데이터 | 영어 | 월 수회 | 높음 | 이메일, 사이트 | 차트 카드 근거(예: 'AI 칩 연산 능력이 약 7개월마다 2배') | 추정치가 포함되니 '추정'으로 표기하고 날짜 명시 | **확인 2026**(2026-02 Epoch Brief) |
| **[추가][T3] Stanford HAI AI Index** | hai.stanford.edu/ai-index/2026-ai-index-report | 연간 AI 통계 종합 | 영어 | 연 1회 | 높음 | 발간 시기 캘린더 등록 | 연례 대형 캐러셀 시리즈('숫자로 보는 AI 2026') | 보고서 연도와 데이터 연도가 다를 수 있음 | **확인**(2026 보고서 페이지) |
| **[T3] Product Hunt** | producthunt.com | 신규 AI 툴 출시·순위 | 영어 | 일간 | 중간 | 일간·주간 뉴스레터, AI 카테고리 | '이번 주 써볼 만한 AI 툴 5', 광고주 후보 발굴 | 업보트는 홍보성일 수 있음. 직접 써 보고 소개. 협찬이면 #광고 | 미검증 |

### D. 글로벌 유튜브·팟캐스트

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| **[T2] Matt Wolfe / Future Tools** | youtube.com/@mreflow, futuretools.io (뉴스레터 futuretools.io/newsletter) | 주간 AI 뉴스 영상, AI 툴 디렉터리 | 영어 | 영상 주간, 뉴스레터 주 2회 | 중간 | 유튜브 알림, 뉴스레터 | 주간 라운드업 선정 기준 벤치마크, 툴 소개 카드 | 영상 클립 재사용 금지. 원 발표로 사실 확인 | **확인(존재)**: 구독자 92.5만+, 뉴스레터 25만+(제3자 글, 날짜 미상) |
| **[T2] AI Explained** | youtube.com/@aiexplained-official | 신모델을 벤치마크·논문 수준에서 비판적으로 해설 | 영어 | 비정기(주 0~2회) | 높음 | 유튜브 알림. 뉴스레터 'Signal to Noise', 팟캐스트도 있음 | 로만식 '과장 걷어내기' 관점 | 제작자 해석이니 채널명 표기 | **확인(존재)**. 2026년 영상은 검색에 없음 |
| **[T3] Two Minute Papers** | youtube.com/@TwoMinutePapers (채널 ID UCbfYPyITQ-7l4upoX8nvctg) | 그래픽·시뮬레이션·생성 AI 연구 데모 | 영어 | 주 1~2회 | 높음 | 유튜브 RSS | '이게 AI라고?' 릴스 소재 고르기 | 재업로드 금지. 논문 프로젝트 페이지의 공개 데모와 출처 사용 | **확인 2026-09**: 2026-09-24 'Claude Opus 5.5' 영상 |
| **[T3] Dwarkesh Podcast** | dwarkesh.com (유튜브 핸들은 초안의 @DwarkeshPatel. 미검증) | AI 연구자·CEO 장시간 인터뷰 | 영어 | 격주 안팎 | 높음 | `dwarkesh.com/feed`(Substack), 팟캐스트 | '인터뷰 중 인상 깊은 발언 3가지', AGI 전망 해설 | 타임스탬프와 함께 정확히 인용. 번역 전문 게재 금지 | **확인 2026-09**: Noam Brown 편(2026-09-17), 2026년 다리오 아모데이 편 |
| **[T3] Y Combinator / Lightcone** | youtube.com/@ycombinator | 창업 강연, 파트너 대담, AI 스타트업 트렌드 | 영어 | 주 수회 | 높음 | 유튜브 알림 | 해외 창업 영상을 골라 요지를 옮기는 BZCF식 제작의 원천 | 영상 번역·재편집 게시는 허락 필요 | 미검증 |

### E. 한국 AI·IT 매체

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| **[T1] AI타임스** | aitimes.com (X @AITimes_News, IG @aitimes_news, 유튜브 채널 ID UCxKaTFMQcCg4kA_oHLGbNxQ) | 국내외 AI 뉴스(국내 기업·정책 포함) | 한국어 | 수시간 | 중간 | 네이버 뉴스 언론사 구독. RSS는 사이트 메뉴에서 확인(주소 미확인) | 한국 맥락 AI 카드. 인스타 AI 정책 같은 운영 관련 뉴스 | 해외 기사 번역이 많으니 원출처를 찾아 인용. **aitimes.kr은 '인공지능신문'이라는 다른 매체**, X @AITIMES1도 인공지능신문 | **이전 조사 확인**(기사, IG 859). X는 `x_ai.md` 참고 |
| **[T1] GeekNews (긱뉴스)** | news.hada.io (주간 news.hada.io/weekly, 텔레그램 GeekNewsHada, X @GeekNewsHada) | 해외·국내 테크 링크 + 한국어 요약 커뮤니티 | 한국어 | 수시간 | 높음 | RSS 제공(주소와 설정은 hada.io/blog/geeknews-feed-rss 안내 참고), 텔레그램, 월요일 아침 위클리 | 한국 개발자가 반응하는 AI 이슈를 빨리 확인 | 요약문을 복사하지 말고 원문으로 확인 | **확인**: 위클리 구독 1.8만+(날짜 미상) |
| **[T2] ZDNet Korea** | zdnet.co.kr | 국내 IT 산업, AI 정책(독자 AI 파운데이션 모델 등) | 한국어 | 수시간 | 중간 | 네이버 뉴스 언론사 구독 | '한국 AI 지금 어디쯤?' 카드 | 보도자료를 받아 쓴 기사 구분 | **이전 조사 확인**(2026-09-30 칼럼) |
| **[T2] 전자신문** | etnews.com | ICT, 반도체, 정부 R&D | 한국어 | 수시간 | 중간 | 네이버 뉴스 언론사 구독 | AI 반도체, 정부 AI 예산 카드 | 유료·단독은 요지와 출처만 | **확인(존재)**: 2025-09-30 기사 검색됨 |
| **[추가][T2] 블로터** | bloter.net | IT, 산업, 보안, AI 기업 | 한국어 | 수시간 | 중간 | 네이버 뉴스 언론사 구독 | 국내 AI 산업·보안 뉴스, 연간 '아웃룩' 기획 | '보도자료' 섹션 기사는 기업 발표 그대로라 구분 | **확인 2026**(2026 기사 다수) |
| **[T2] 바이라인네트워크** | byline.network | 기업 IT, 클라우드, AI 해설 | 한국어 | 일간 | 높음 | 사이트 뉴스레터, 유튜브 | 로만식 해석형 한국어 톤 참고, 국내 사례 인용원 | 해설 기사 논지는 출처 명시 | 미검증(도메인은 검색 결과에서 확인) |
| **[T2] 요즘IT (위시켓)** | yozm.wishket.com (X @yozm_it) | 실무자 기고, AI 툴 활용기 | 한국어 | 일간 | 중간 | 뉴스레터 | 직무별 AI 활용 카드 | 저작권이 기고자에게 있음. 필자 명시 | 미검증 |
| **[T3] 디지털데일리** | ddaily.co.kr | IT, 보안, 통신, 금융IT | 한국어 | 수시간 | 중간 | 네이버 뉴스 언론사 구독 | 네이버·카카오·통신3사 AI 전략 | 보도자료성 기사 구분 | 미검증 |
| **[추가][T2] 튜링포스트 코리아** | turingpost.co.kr | AI 해설, 'AI 101', 주간 다이제스트 | 한국어 | 주 2~3회(자체 표기) | 높음 | 이메일 | 로만식 한국어 AI 해설의 문체·구성 참고 | 일부 유료. 영문 Turing Post 기반 | **확인(존재)**. 2026년 글은 검색에 없음 → 구독 전 최근 발행일 확인 |
| **[추가][T2] 조코딩** | youtube.com/@jocoding (jocoding.net, 채널 ID UCQNE2JmbasNYbjGAcuBiRRg) | AI 뉴스, 코딩, 바이브코딩 | 한국어 | 주 수회 | 중간 | 유튜브 알림 | 한국 대중이 반응하는 AI 뉴스가 무엇인지 확인. 한국어 설명 방식 참고 | 크리에이터 해석이고 협업·광고 영상이 섞임 | **확인(존재)**: 2026-09 추천 글에 언급됨 |
| **[T2] SPRi AI 브리프** | spri.kr/posts?code=AI-Brief | 국내외 AI 정책·산업·기술 동향 | 한국어 | 월간 | 높음 | 사이트 게시판 월 1회 확인 | 한국 맥락 해설 카드의 통계·정책 근거 | 정식 이름은 'AI 산업 동향 브리프'. 발행 호수 명시 | **확인 2026**(2026년 2월호) |

### F. 한국 비즈니스·경제 매체·뉴스레터·유튜브

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| **[T2] 아웃스탠딩** | outstanding.kr | 국내 플랫폼·스타트업·IT 비즈니스 해설, 창업자 인터뷰 | 한국어 | 일간 | 높음 | 뉴스레터, 멤버십 | BZCF식 '회사 이야기' 코멘트의 한국 사례 | 유료 비중이 큼. 요지만 인용 | **확인 2026**(2026-02 기사) |
| **[T2] 플래텀** | platum.kr | 국내 스타트업 투자, 창업자 인터뷰 | 한국어 | 일간 | 중간 | RSS 리더에 사이트 주소 입력, 뉴스레터 | '이번 주 투자받은 AI 스타트업' 카드 | 보도자료 기반 기사가 많음 | **이전 조사 확인** |
| **[T3] 더밀크** | themiilk.com | 실리콘밸리·미국 테크 한국어 해설 | 한국어 | 일간 | 중간 | 뉴스레터 | 해외 AI 비즈니스를 한국 맥락으로 옮길 때 참고 | 일부 유료, 비슷한 포지션의 경쟁 매체. 원 해외 출처로 거슬러 올라가 인용 | 미검증 |
| **[T2] 뉴닉 NEWNEEK** | newneek.co (구독 newneek.co/subscribe), IG @newneek.official | 시사·경제 쉬운 해설 | 한국어 | 평일 아침 | 높음 | 뉴스레터, 앱 | 오늘 대중이 알아야 할 이슈 고르기 | 경쟁 큐레이터라 문장·구성 모방 금지. 구독자 수는 출처마다 43만~63만으로 달라 인용하지 말 것 | **확인(존재, 발행 중)**, IG 235K는 이전 조사 |
| **[T2] 어피티 머니레터** | uppity.co.kr (머니레터 uppity.co.kr/newsletter/money-letter/), IG @uppity.official | 2030 직장인 경제·재테크(잘쓸레터 별도) | 한국어 | 평일 아침 | 높음 | 머니레터 구독 | 에크케식 '벌기·모으기·쓰기' 카드 소재와 톤 | 직접 경쟁 매체. 투자 조언처럼 읽히는 표현 주의 | **확인 2026-09**: 사이트 표기 '50만 명이 받아보는 머니레터', 추석 주간(9/21~25) 휴간 공지. 초안의 '45만'은 예전 광고소개서 값 |
| **[T3] 캐릿 Careet (대학내일)** | careet.net, IG @careet.official | MZ 트렌드, 밈, 소비 | 한국어 | 주간 트렌드레터 | 높음 | 트렌드레터, IG | 라이프스타일·AI 밈 트렌드 카드 | 웹 콘텐츠 일부 유료. 조사 데이터 출처 명시 | **이전 조사 확인** |
| **[T2] EO (이오)** | 유튜브 'EO Korea'(youtube.com/channel/UCQ2DWm5Md16Dc3xRwwhVE7Q). 영어 인터뷰는 글로벌 'EO' 채널이 따로 있음. IG @eostudio.kr | 국내외 창업자·AI 스타트업 인터뷰 | 한국어(글로벌 채널은 영어 + 한국어 자막) | 주 수회 | 높음 | 유튜브 RSS(채널 ID) | 창업자 발언 인용 카드 | 영상 캡처는 허락 필요. 채널 @핸들은 확인 못함 | **확인(존재)**: 채널 URL. IG는 이전 조사 |
| **[T2] 티타임즈** | ttimes.co.kr, 유튜브 **@TTimesTV** | 테크·비즈니스 해설 영상 | 한국어 | 일간 | 중간 | 유튜브 알림 | 한국 직장인 눈높이 해설 방식 참고 | 머니투데이 계열 | **확인**: 채널 핸들 @TTimesTV(초안의 '핸들 미확인' 해결) |
| **[T3] 삼프로TV** | youtube.com/**@3protv**(채널 이름 '삼프로TV_경제의신과함께'). 자매 채널 @3promoney | 증시, 거시경제, 산업 전문가 라이브 | 한국어 | 평일 매일 라이브 | 중간 | 유튜브 알림, 출연자 발언 메모 | AI 반도체·빅테크 실적이 한국 투자자에게 어떤 의미인지 | 종목 추천으로 읽히지 않게 조심. 발언자 명시 | **확인**: 핸들 @3protv, 구독자 304만(vidIQ, 날짜 미상) |

### G. 한국 공식 데이터·정부 발표

> 에크케식 경제 카드의 1차 원천입니다. 별도 조사(econ_lifestyle)와 겹칠 수 있습니다.

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| **[T1 시즌] DART 전자공시** | dart.fss.or.kr (OpenDART API) | 사업보고서, 감사보고서, 잠정실적 | 한국어 | 1차 공시. 1~4월에 몰림 | 높음 | 관심 기업 공시 알림, 실적 시즌 캘린더 | 에크케 'OOO는 이렇게 벌고 씁니다' 시리즈의 확인된 원천 | 연결·별도, 기준 연도를 적을 것. 매체마다 증감률 표기가 다르니 원문 대조 | **이전 조사 확인** |
| **[T2] 대한민국 정책브리핑** | korea.kr | 부처 보도자료(과기정통부 AI, 금융위·재정당국 청년 금융) | 한국어 | 1차 발표 | 중간 | 부처별 보도자료 RSS, 키워드 알림 | '이번 달부터 바뀌는 돈 정책' 카드 | 시행일, 대상 요건을 정확히. 공공누리 유형 확인 | **이전 조사 확인** |
| **[T2] 한국은행 / ECOS** | bok.or.kr, ecos.bok.or.kr | 기준금리, 물가, 소비자심리, 가계부채 | 한국어 | 1차(일정 공지) | 높음 | 보도자료, 금통위 일정 캘린더 | '금리가 내 통장에 미치는 영향' 데이터 카드 | 출처와 수치 기준일 필수 | 미검증(공식 기관) |
| **[T2] 국가데이터처(구 통계청) / KOSIS** | kosis.kr | 고용, 물가, 가계동향, 1인가구 통계 | 한국어 | 1차(월간·연간 일정) | 높음 | 통계 공표 일정 캘린더 | '통계로 보는 2030의 돈' 카드 | 기관명을 '국가데이터처'로 쓸 것. 2025-10 이전 자료는 '통계청' 발표로 표기 | **확인**: **2025-10-01 통계청이 국가데이터처로 승격**(국무총리 소속). KOSIS 주소는 미검증 |
| **[T3] KDI 한국개발연구원** | kdi.re.kr | 월간 'KDI 경제동향', 경제 전망 | 한국어 | 월간 | 높음 | 보도자료, 뉴스레터 | 경기 판단 한 줄 인용 카드 | 전망치는 발표일 표기 | 미검증(공식 기관) |

---

## 3. 우선순위 Top 10

| 순위 | 소스 | 왜 |
|---|---|---|
| 1 | **The Rundown AI** | 200만+가 받는 가장 큰 AI 일간 요약입니다. 매일 저녁 'AI 3줄'과 주간 라운드업의 **빠짐없음 체크리스트**로 쓰기 가장 효율적입니다. AI Freaks식 계정의 기본 레이더입니다. |
| 2 | **OpenAI / Anthropic / Google·DeepMind 공식 뉴스룸** (한 묶음) | 모든 AI 뉴스의 **1차 원문**입니다. OpenAI는 공식 RSS(`openai.com/news/rss.xml`)가 확인됐습니다. 요약본에서 찾은 소재를 여기서 확인해야 틀리지 않습니다. |
| 3 | **Techmeme** | 영어권 테크 매체 헤드라인을 한 화면에서 교차 검증할 수 있습니다. BZCF가 쓰는 원천(Bloomberg, TechCrunch, CNBC, FT)이 대부분 여기 먼저 걸립니다. 비즈니스 코멘트형(@bizucafe) 소재의 입구입니다. |
| 4 | **AI타임스** | 한국 AI 기업·정책 뉴스가 가장 많이 나옵니다. 해외 뉴스의 **한국 맥락**을 붙이는 데 필요합니다. aitimes.kr(인공지능신문)과 혼동하지 마세요. |
| 5 | **GeekNews** | 한국 개발자들이 실제로 반응하는 해외 AI 이슈를 한국어 요약으로 빨리 봅니다. RSS, 텔레그램, 위클리 채널이 모두 확인됐습니다. |
| 6 | **The Decoder** | 모델 출시, 벤치마크, AI 지출 추세를 짧고 빠르게 씁니다. 2026-09에도 활발합니다. '이번 주 신모델' 카드에 바로 쓸 수 있습니다. |
| 7 | **Axios AI+** | 평일 일간이고, Smart Brevity 구조가 **카드뉴스 한 장의 문법과 거의 같습니다.** AI 정책과 투자 흐름을 매일 잡습니다. |
| 8 | **Hugging Face Papers (Trending)** | Papers with Code 종료(2025-07) 뒤 연구·오픈모델 트렌드를 보는 표준 창구가 됐습니다. '이게 AI라고?' 같은 괴짜 소재도 여기서 먼저 나옵니다. |
| 9 | **One Useful Thing** (+ 주간 해설 묶음: Import AI, Interconnects, Simon Willison) | 로만식 '이해시키는' 해설의 관점을 줍니다. Mollick은 비개발자 눈높이라 한국어 카드로 옮기기 가장 쉽습니다. 2026-08까지 활동이 확인됐습니다. |
| 10 | **DART 전자공시** (+ 한국은행, 국가데이터처) | 에크케식 '이 회사는 이렇게 벌고 씁니다' 카드의 **확인된 원천**입니다. 공시 원문이라 저작권 부담이 없고, 다른 AI·비즈니스 큐레이터와 겹치지 않는 차별 소재입니다. |

**Top 10 다음으로 볼 것**
- **숫자·순위 카드용**: Arena(개명 확인), Artificial Analysis, Epoch AI, Stanford AI Index
- **재미·괴짜 소재용**: 404 Media, Two Minute Papers

---

## 4. 제거·이동한 항목과 이유

### 4-1. 완전 삭제: 0건

- 초안 60개 가운데 **가짜이거나 폐쇄된 소스는 없었습니다.**
- 검색으로 확인한 항목은 모두 2025~2026년에도 운영 중입니다.
- 다만 Import AI(최근 확인 2026-06), AINews(2026-02), 튜링포스트 코리아(2026년 글 미확인)는 **최근 발행일을 다시 확인**하세요.

### 4-2. 표에서 빼서 부록으로 옮긴 것: 3건

| 항목 | 이유 |
|---|---|
| **BZCF 텔레그램 / bzcf.io** (t.me/s/bzcftel, bzcf.io, substack.com/@bzcf) | 원천 뉴스가 아니라 **경쟁 큐레이터의 결과물**입니다. 번역문과 코멘트를 가져오면 안 되고, 원천은 이미 이 표(Bloomberg, TechCrunch, a16z, 공식 뉴스룸)에 있습니다. 벤치마크용으로는 `source-tracing.md`에 자세히 정리돼 있습니다. |
| **롱블랙** (longblack.co, IG @longblack.co) | 유료 노트를 전재하거나 요약해 올릴 수 없어서 **뉴스 소스로 쓸 수 없습니다.** 'AI판 롱블랙' 포지셔닝과 스토리텔링의 벤치마크로만 의미가 있습니다. |
| **폴인** (folin.co, IG @folin_co) | 롱블랙과 같은 이유입니다(유료 구독 콘텐츠). 커리어 콘텐츠 포맷을 참고하는 용도로만 씁니다. |

### 4-3. 틀렸거나 근거가 없어 고친 서술

| 항목 | 초안 | 수정 | 근거 |
|---|---|---|---|
| The Neuron | 주소 theneurondaily.com, 구독 '약 70만' | 주 주소 **theneuron.ai**. 구독은 **인수 당시 50만+**. TechnologyAdvice 인수(2025-01) 명시 | TechnologyAdvice 보도자료, The Neuron 공지 |
| Ben's Bites | '일간~주 수회' | **주 2회(화·목)**, 약 12만 구독, 커뮤니티 유료 | bensbites.com/about, 2026-03 기사 |
| Import AI | importai.substack.com이 주소 | **jack-clark.net이 주 아카이브**. 최근 확인 459호(2026-06-01) | jack-clark.net |
| Interconnects | 소속 언급 없음 | 필자가 **2026-06 Ai2를 떠남**. 소속 표기 주의 | 검색 요약 |
| TLDR AI | 구독 '미확인' | 약 110만(2026 리뷰 기사) | readless |
| Last Week in AI | 활동 미확인 | 257회(2026-09-19) 확인 | 팟캐스트 목록 |
| OpenAI News | 'RSS 제공 여부 확인' | 공식 RSS `openai.com/news/rss.xml` 확인 | 개발자 커뮤니티, Feeder |
| Hugging Face | 'Papers with Code 2025년 종료(확인 필요)' | **2025-07-24 종료, HF Trending Papers로 리디렉트** 확인 | Coursera, HyperAI |
| 국가데이터처 | '2025년 10월 개편으로 앎' | **2025-10-01 출범, 국무총리 소속** 확인 | 아시아경제, 전자신문, 위키백과 |
| AI타임스 | RSS 모니터링 권장 | RSS 주소는 확인 못함. **aitimes.kr은 인공지능신문(다른 매체)**이라는 혼동 경고 추가 | 검색 결과 |
| 삼프로TV | '@3protv로 알고 있으나 미검증' | **@3protv 확인**, 구독자 304만(날짜 미상), 자매 채널 @3promoney | vidIQ, 유튜브 |
| 티타임즈 | '핸들 미확인' | **@TTimesTV** 확인 | 유튜브 |
| EO | '유튜브 핸들 미확인' | EO Korea **채널 ID** 확인(핸들은 여전히 미확인). 글로벌 EO 채널이 따로 있음 | 유튜브, 나무위키 요약 |
| 어피티 | 머니레터 45만(광고소개서) | 사이트 표기 **50만**. 2026-09 발행 확인 | uppity.co.kr |
| SPRi | '간행물 명칭·주기 확인 필요' | 월간 **'AI 산업 동향 브리프'** 확인(2026년 2월호) | spri.kr, Scribd |
| Matt Wolfe | 규모 미확인 | 구독자 92.5만+, Future Tools 뉴스레터 주 2회 25만+(제3자 글, 날짜 미상) | 검색 요약 |
| AI Explained | 활동 전제 | 2026년 영상은 검색에 없음을 명시. 뉴스레터 'Signal to Noise'가 있음 | 검색 요약 |

---

## 5. 출처

**이번 검증에서 쓴 검색 결과**

- The Neuron 인수: https://solutions.technologyadvice.com/press/technologyadvice-acquires-the-neuron/ , https://www.theneuron.ai/newsletter/the-neuron-acquired/ , https://www.beehiiv.com/case-studies/the-neuron
- Ben's Bites: https://www.bensbites.com/about , https://aiforautomation.io/news/2026-03-30-bens-bites-120k-ai-newsletter-founder-a16z
- AINews: https://news.smol.ai/issues/2026-02-20-not-much , https://buttondown.com/ainews
- Import AI: https://jack-clark.net/2026/05/26/import-ai-458-reckoning-with-the-future-and-a-singularity-story/ , https://jack-clark.net/about/
- TLDR AI: https://tldr.tech/ai , https://www.readless.app/newsletters/tldr-ai
- Interconnects: https://www.interconnects.ai/p/my-bets-on-open-models-mid-2026 , https://www.interconnects.ai/p/state-of-the-blog-mid-2026
- Last Week in AI: https://podcasts.apple.com/us/podcast/last-week-in-ai/id1502782720 , https://lastweekin.ai/s/podcast
- One Useful Thing: https://www.oneusefulthing.org/p/agency-and-agents , https://www.oneusefulthing.org/archive
- The Batch: https://www.deeplearning.ai/the-batch , https://x.com/DeepLearningAI/status/2098766076347568451
- OpenAI RSS: https://feeder.co/discover/feb0ad8f6b/openai-com-news , https://community.openai.com/t/openai-website-rss-feed-inquiry/733747
- Papers with Code 종료: https://www.coursera.org/articles/papers-with-code , https://hyper.ai/en/news/42900
- The Decoder: https://the-decoder.com/top-ai-spenders-cut-per-employee-costs-by-nearly-10-percent-in-august/
- 국가데이터처: https://www.asiae.co.kr/article/economic-general/2025093013434468167 , https://www.etnews.com/20250930000292
- 삼프로TV: https://www.youtube.com/@3protv , https://vidiq.com/youtube-stats/channel/@3protv/
- EO Korea: https://www.youtube.com/channel/UCQ2DWm5Md16Dc3xRwwhVE7Q , https://namu.wiki/w/EO
- 티타임즈TV: https://www.youtube.com/@TTimesTV/videos , https://www.ttimes.co.kr/
- 아웃스탠딩: https://outstanding.kr/top20260213
- SPRi AI 브리프: https://spri.kr/posts?code=AI-Brief , https://www.scribd.com/document/1033784889/Ai-%EC%82%B0%EC%97%85-%EB%8F%99%ED%96%A5-%EB%B8%8C%EB%A6%AC%ED%94%84-2026%EB%85%84-2%EC%9B%94%ED%98%B8-Spri-Ai-Brief-2026-Feb
- Two Minute Papers: https://ai-tldr.dev/releases/two-minute-papers-claude-opus-5-5-sep24/ , https://www.youtube.com/channel/UCbfYPyITQ-7l4upoX8nvctg
- AI Explained: https://www.youtube.com/@aiexplained-official , https://www.atakinteractive.com/blog/17-ai-youtubers-were-actually-watching-right-now
- Axios AI+: https://www.axios.com/signup/ai-plus , https://talkingbiznews.com/media-news/mills-to-cover-ai-for-axios/ , https://x.com/MadisonMills22/status/2020978909471441119
- GeekNews: https://hada.io/blog/geeknews-subscribe/ , https://hada.io/blog/geeknews-feed-rss/ , https://x.com/GeekNewsHada
- AI타임스: https://www.aitimes.com/ , https://x.com/AITimes_News , http://www.aitimes.kr/rss/ (인공지능신문, 다른 매체)
- Arena(구 LMArena): https://arena.ai/blog/lmarena-is-now-arena , https://arena.ai/company/leaderboard-changelog , https://en.wikipedia.org/wiki/Arena_(AI_platform)
- The Rundown AI: https://www.therundown.ai/ , https://www.readless.app/blog/the-rundown-ai-newsletter-review-2026
- Simon Willison: https://simonwillison.net/2026/Sep/27/2026-in-llms-so-far/
- Artificial Analysis: https://artificialanalysis.ai/evaluations/artificial-analysis-intelligence-index
- Stanford AI Index 2026: https://hai.stanford.edu/ai-index/2026-ai-index-report
- 404 Media: https://www.404media.co/tag/ai-slop/ , https://www.404media.co/
- Epoch AI: https://epoch.ai/data-insights , https://epochai.substack.com/p/the-epoch-brief-february-2026
- 튜링포스트 코리아: https://turingpost.co.kr/
- 조코딩: https://www.youtube.com/@jocoding , https://jocoding.net/about/ , https://aisolutions.kr/2026/09/11/free_ai_study_youtube_channels_top3_recommended_by_choigpt/
- Latent Space: https://www.latent.space/podcast , https://www.latent.space/about
- Matt Wolfe: https://www.youtube.com/@mreflow , https://futuretools.io/newsletter , https://airisingtrends.com/matt-wolfe-ai/
- 블로터: https://bloter.net/news/articleView.html?idxno=664736
- MIT Technology Review: https://www.technologyreview.com/2026/09/28/1145230/when-can-we-say-ai-made-a-scientific-discovery/ , https://forms.technologyreview.com/newsletters/ai-demystified-the-algorithm/
- 뉴닉: https://newneek.co/subscribe , http://www.businessreport.kr/news/articleView.html?idxno=52928
- 어피티: https://uppity.co.kr/newsletter/money-letter/ , https://uppity.co.kr/category/newsletter/moneyletter/
- Dwarkesh Podcast: https://www.dwarkesh.com/ , https://www.lesswrong.com/posts/jWCy6owAmqLv5BB8q/on-dwarkesh-patel-s-2026-podcast-with-dario-amodei

**앞선 조사에서 가져온 근거** (같은 세션 파일)

- `source-tracing.md`: BZCF와 에크케의 원천 역추적. TechCrunch, Bloomberg, CNBC, FT, a16z, OpenAI, DART, 정책브리핑, 플래텀, Axios 근거 URL
- `../landscape.md`: AI타임스, EO, 뉴닉, 롱블랙, 폴인, 어피티, 캐릿의 IG 수치와 URL
- `../best-practices.md`: 인스타 애그리게이터 제재(TechCrunch 2026-04-30)
- `x_ai.md`: Techmeme, AI타임스, GeekNews, 요즘IT의 X 핸들, Rowan Cheung의 X 활동 날짜

---

## 부록. 벤치마크(뉴스 원천은 아님)

| 이름 | 주소 | 볼 것 | 검증 |
|---|---|---|---|
| BZCF 텔레그램 / bzcf.io | t.me/s/bzcftel , bzcf.io , substack.com/@bzcf | 매일 무엇을 골라 어떻게 코멘트하는지. 같은 원문으로 거슬러 올라가 **다른 관점**으로 쓰기 | 이전 조사 확인(텔레그램 9,940, 날짜 미상) |
| 롱블랙 | longblack.co , IG @longblack.co | 1일 1노트 유료 구조, 브랜드 스토리텔링 | 이전 조사 확인(IG 181K) |
| 폴인 | folin.co , IG @folin_co | 전문가 인터뷰형 커리어 콘텐츠 포맷 | 이전 조사 확인(IG 108K) |
