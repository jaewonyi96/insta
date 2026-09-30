# X·AI 뉴스 소스 검증본 (x_ai)

- 작성일: 2026-09-30
- 대상: 한국형 AI·비즈니스 큐레이션 인스타 계정(@ai_freaks.kr, @romaan.mag, @bizucafe 스타일)을 운영하기 위해 매일 볼 **X(트위터) 중심의 AI 뉴스 소스**
- 결과: 초안 50개 항목을 검증함 → **50개 유지(그중 12개 수정)**, **1개 제거**(@legit_api), **5개 추가** → 최종 55개

---

## 1. 개요

### 1-1. 검증 방법 (먼저 읽어 주세요)

- **이번 검증 단계에서는 새 웹 검색을 한 번도 하지 못했습니다.**
  - 이 세션의 WebSearch 한도(200회)가 이미 소진된 상태였습니다.
  - x.com·instagram.com 직접 접속도 이 실행 환경의 네트워크 정책으로 막혀 있습니다.
- 대신 **초안을 만든 에이전트가 같은 세션에서 실제로 받은 WebSearch 원본 결과 98건**을 모두 다시 읽었습니다(검색어, 결과 제목, URL, 요약).
  - 초안의 주장을 하나씩 이 원본과 대조했습니다.
  - 원본에 근거가 없는 주장은 지우거나 '미확인'으로 바꿨습니다.
- **'최근 확인' 날짜**: 검색 결과에 잡힌 X 게시물 URL의 status ID를 날짜로 바꿨습니다(X 스노플레이크 ID: `(ID >> 22) + 1288834974657` ms → UTC).
  - 이 날짜는 **검색에 잡힌 가장 최근 게시물**일 뿐이고, 실제 마지막 게시일은 더 최근일 수 있습니다.
  - '날짜 미확인'은 프로필 페이지만 검색됐다는 뜻입니다.
- 팔로워 수는 검색 스니펫에 나온 시점의 값입니다.
- 교차 확인용으로 같은 폴더의 `source-tracing.md`(4개 계정의 원본 역추적)와 `../accounts/ai_freaks_kr.md`도 참고했습니다.

### 1-2. 브라우저로 직접 확인하는 법 (10분)

이 실행 환경에서는 X·인스타가 막혀 있지만, **사용자 본인 브라우저에서는 바로 열립니다.** 아래 순서로 최종 확인하면 됩니다.

1. 주소창에 `x.com/핸들`을 입력해 계정이 존재하는지 봅니다.
2. 기관 인증 배지나 소속(affiliation) 배지가 있는지 봅니다.
3. **고정 게시물이 아닌** 가장 최근 게시물의 날짜를 봅니다.
4. 바이오에 걸린 링크가 해당 회사의 공식 도메인인지 봅니다.

**우선 확인할 계정** (검증에서 의문이 남은 것):
- @AIatMeta와 @metaai 중 어느 쪽이 현재 계정인지
- @lmarena_ai의 핸들이 Arena로 바뀌었는지
- @Kimi_Moonshot, @Zai_org, @MiniMax_AI의 인증 여부
- 2026년 게시물을 검색으로 확인하지 못한 계정: @_akhaliq, @rowancheung, @MistralAI, @suno, @bilawalsidhu, @koraykv, @NAVER__Cloud, @Techmeme, @AITimes_News

### 1-3. 초안 대비 주요 수정 사항

| 항목 | 초안 | 수정 | 근거 |
|---|---|---|---|
| AK / DailyPapers | @_akhaliq를 대표 핸들로 둠. "가장 빨리 소개하는 계정(1.7만 건 이상 트윗)" | **@HuggingPapers를 대표로 바꿈** | 1.7만 건은 2023년 5월 수치입니다. 그때 AK는 논문 소개를 HF Daily Papers로 옮긴다고 밝혔습니다. @_akhaliq의 최근 확인 게시물은 2024-09이고, @HuggingPapers는 2026-03 활동이 확인됩니다. |
| Legit / Chetaslua | "Gemini 4 Pro 리크를 가장 먼저 포착" | **해당 문구 삭제**, @legit_api 제거, @chetaslua만 유지 | Gemini 4 Pro 리크는 TestingCatalog·BigGo 등이 보도했고, 이 두 계정의 것이라는 근거가 없습니다. @legit_api의 최근 확인 게시물은 2025-06입니다. |
| Legit 주의 문구 | "요청하신 'legit_rumors'" | "이전 단계 후보 목록에 있던 'legit_rumors'" | 사용자가 요청한 핸들이 아니라 앞 단계 작업 목록에서 나온 이름입니다. |
| SpaceXAI | 근거 URL이 제3자(@mark_k) 트윗 | Yahoo Finance 보도로 교체 | 개명(2026-07-06)은 보도로 확인됩니다. |
| AI at Meta | "@metaai는 예전 핸들이니 @AIatMeta로" | "둘 다 표시명이 'AI at Meta'. 팔로우 전에 현재 계정 확인" | 검색 요약은 @AIatMeta로 옮겼다고 했지만, @metaai 페이지에도 같은 표시명이 붙어 있어 어느 쪽이 현재인지 단정할 수 없습니다. |
| LMArena | "핸들이 바뀔 수 있으니 확인" | 최근 확인 게시물이 **2025-09**라는 사실을 추가. arena.ai 리더보드 변경 로그를 대체 모니터링 대상으로 둠 | 2026년 게시물이 검색되지 않았습니다. |
| Rowan Cheung | 알림·리스트 중심 | 2026년 X 게시물 미확인(최근 2025-07, @TheRundownAI 기준). **뉴스레터를 주 채널로** | 검색 결과의 날짜 기준 |
| Angry Tom | 근거 URL이 2024-06 게시물 | 2025-07 본인 게시물과 2026-09 타 계정 보도로 교체. 해당 영상은 특정 툴(Sherpa) 사용 사례라는 점 추가 | 검색 결과 |
| Bilawal Sidhu | 활동 확인으로 표기 | X 계정 자체의 2026년 게시물은 미확인으로 표기(프로젝트, 인스타, Threads는 활동 확인) | 검색 결과 |
| NAVER Cloud | LG와 같이 '1차 출처' | @NAVER__Cloud는 프로필만 확인. 네이버 뉴스룸을 우선하도록 변경 | 게시물이 검색되지 않았습니다. |
| 리스트 번호 | '07_한국'과 '07_비즈니스·인프라'가 겹치고, '05_크리에이티브툴'과 '05_괴짜·바이럴'이 따로 나옴 | 리스트 8개로 다시 정리(§3) | 초안 내부 불일치 |
| CHOI, AI TREND KOREA | channel=community | Threads 경쟁 벤치마크로 따로 분리 | 뉴스 소스가 아니라 경쟁 계정 |
| TestingCatalog | — | 리크가 틀릴 수 있다는 실례 추가: DevDay 전에 'o'로 예고된 상시 에이전트가 실제로는 'dots'라는 이름으로 발표됨 | TestingCatalog 기사, 9to5Mac의 DevDay 보도 |

---

## 2. 추천 소스 표

표기: **최근 확인** = 검색에 잡힌 가장 최근 게시물의 날짜(UTC). 리스트 이름은 §3의 X 비공개 리스트입니다.

### 2-1. 공식 발표 (AI 랩·빅테크·툴 회사)

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 |
|---|---|---|---|---|---|---|---|---|
| OpenAI (+ @OpenAIDevs, @ChatGPTapp) | [x.com/OpenAI](https://x.com/OpenAI)<br>최근 확인 2026-06-23(@OpenAIDevs) | ai_news | 영어 | 1차(공식 발표와 동시) | 높음 | 01_공식발표. @OpenAI는 알림 켜기. 라이브 이벤트 때는 @OpenAIDevs도 봄 | 새 모델, 요금제, 기능 공지. 2026-09-29 DevDay에서 상시 에이전트 'dots', GPT-6.1 Sol 등 20여 건을 발표했다(CNBC·9to5Mac 보도). '오늘 ChatGPT에 생긴 변화 3가지' 카드로 바로 만들 수 있음 | 영상·이미지 저작권은 OpenAI에 있음. 재업로드하지 말고 짧게 인용. 한국 적용 여부는 따로 확인. @ChatGPT라는 별도 계정도 있음. 팔로워 약 470만(스니펫) |
| Anthropic / Claude (@AnthropicAI, @claudeai, @ClaudeDevs) | [x.com/AnthropicAI](https://x.com/AnthropicAI)<br>최근 확인 2026-04-17(@claudeai), 2026-07-06(@bcherny) | ai_news | 영어 | 1차 | 높음 | 01_공식발표에 3개 계정. Claude Code 제작자 @bcherny는 02_핵심인물 | 모델 출시, 안전·해석가능성 연구, 'Claude 헌법'(2026-01-21) 같은 정책. @claudeai는 Claude Design(2026-04-17)과 Cowork 같은 제품 소식. @ClaudeDevs는 2026-04-16에 개설됨. 연구 발표는 로만형 해설 소재 | 실험 환경의 결과를 '실제 AI가 그랬다'로 과장하지 말 것. 원문 링크 필수 |
| Google DeepMind | [x.com/GoogleDeepMind](https://x.com/GoogleDeepMind)<br>최근 확인 2026-07-07 | ai_research | 영어 | 1차 | 높음 | 01_공식발표. 알림 켜기(Gemini 4 대기) | Genie 3(월드모델), AlphaGenome Atlas, WeatherNext 3, Gemini 3.8 Live. Gemini 4는 2026-09 기준 사후학습 단계이고 조기 출시를 노린다는 보도가 있음 → 출시 발표가 여기 먼저 뜰 가능성이 큼 | 연구 데모는 제품이 아닌 경우가 많으니 '연구 단계'라고 표기 |
| Google Gemini 앱 (+ @Google) | [x.com/GeminiApp](https://x.com/GeminiApp)<br>최근 확인 2026-07-16 | ai_tools | 영어 | 1차 | 높음 | 01_공식발표. 큰 발표는 @Google도 동시에 공지 | Nano Banana 2(2026-02-26), 아바타 이미지(2026-07-16)처럼 일반인이 바로 따라 할 수 있는 기능. Nano Banana는 피규어 셀카 유행을 만든 전례가 있음 → '따라 해보기' 캐러셀 | 미국에 먼저 나오는 기능이 많음. 한국 적용 여부를 표기 |
| AI at Meta | [x.com/AIatMeta](https://x.com/AIatMeta)<br>날짜 미확인(프로필만 검색됨) | ai_news | 영어 | 1차 | 높음 | 01_공식발표 | Muse Spark(2026-04-08, Meta Superintelligence Labs의 첫 모델), Muse Spark 1.3, 개인 에이전트 muse.ai. 인스타·왓츠앱과 연결된 AI 기능이라 한국 인스타 독자가 체감하기 쉬움 | @metaai 페이지에도 'AI at Meta'라는 같은 표시명이 붙어 있음. 팔로우 전에 인증 배지와 최근 게시일로 현재 계정을 확인 |
| SpaceXAI (구 xAI) + @grok | [x.com/SpaceXAI](https://x.com/SpaceXAI)<br>2026-07-06 개명 | ai_news | 영어 | 1차 | 중간 | 01_공식발표. 주요 발표는 @elonmusk가 먼저 예고하는 경우가 많음 | Grok 모델, Grok Imagine 1.0(2026-02-02, 10초·720p 영상), Grok Build. SpaceX의 xAI 인수(2026-02)와 Cursor 인수(2026-06) 같은 머스크 관련 뉴스는 비즈니스와 괴짜 양쪽 소재 | **[이름 변경]** 2026-07-06 xAI가 SpaceXAI로 이름과 X 핸들을 바꿈. 옛 @xai로 만든 리스트는 갱신. 머스크 발언은 확인된 사실과 분리해서 표기 |
| Mistral AI | [x.com/MistralAI](https://x.com/MistralAI)<br>보조: @MistralDevs<br>최근 확인 2025-06-10 | ai_news | 영어/프랑스어 | 1차 | 높음 | 06_중국·오픈모델 | 유럽 대표 랩의 오픈웨이트·추론 모델(Magistral 등). '미국·중국 말고 유럽은?' 비교 콘텐츠 | **[2026 활동 미확인]** 검색에 잡힌 가장 최근 게시물이 2025-06임. 한국 관심도가 낮아 단독보다 비교·요약 게시물에 넣기 |
| DeepSeek | [x.com/deepseek_ai](https://x.com/deepseek_ai)<br>최근 확인 2026-04-24 | ai_news | 영어/중국어 | 1차(예고 없이 발표하는 경우가 많음) | 높음 | 06_중국·오픈모델. 알림 켜기 | DeepSeek-V4 Preview(2026-04-24, 오픈소스, 1M 컨텍스트, Pro 1.6T·Flash 284B) 같은 '저비용 고성능' 발표 → 가격 비교 인포그래픽 | DeepSeek가 '@deepseek_ai가 유일한 공식 계정'이라고 공지함. @deepseekai, @deepseekcto 같은 사칭 계정을 인용하지 말 것 |
| Qwen (Alibaba) | [x.com/Alibaba_Qwen](https://x.com/Alibaba_Qwen)<br>최근 확인 2026-07-19 | ai_news | 영어/중국어 | 1차 | 높음 | 06_중국·오픈모델 | Qwen3.8-Max(2.4T, 2026-08 보도), Qwen3.8-Flash-Next. 2026-09-22 Apsara 행사에서 Qwen 4 라인업 4종을 공개(출시일·가격·가중치 미정) → '중국 AI 어디까지 왔나' | 발표일과 오픈웨이트 공개일이 다른 경우가 많음. '공개 예정'과 '공개됨'을 구분 |
| 중국 AI 3사: Moonshot Kimi / Z.ai / MiniMax | [x.com/Kimi_Moonshot](https://x.com/Kimi_Moonshot)<br>보조: @Zai_org, @MiniMax_AI<br>핸들은 타 계정의 태그로 확인(2025-08, 2026-02) | ai_news | 영어/중국어 | 1차 | 높음 | 06_중국·오픈모델에 3개 모두 | Kimi K3(2026-07-16 공개, 2.7T 오픈웨이트, 07-26 가중치 공개). Z.ai와 MiniMax는 2026-01 홍콩 상장, Moonshot은 상장 준비 보도 → 모델 출시와 상장·투자 뉴스를 함께. Kimi와 Hailuo(MiniMax)는 AI Freaks의 협업사이기도 함 | 세 핸들 모두 다른 계정의 태그로만 확인함. X에서 인증 배지를 직접 확인 |
| NVIDIA AI (+ @nvidia, @nvidianewsroom) | [x.com/NVIDIAAI](https://x.com/NVIDIAAI)<br>최근 확인 2026-03(@nvidia, @NVIDIAAIDev) | ai_news | 영어 | 1차 | 중간 | 07_비즈니스 | GPU·인프라, Open Agent Safety Platform, 오픈모델. 젠슨 황과 AI 반도체 이야기는 삼성·SK하이닉스와 연결되는 비즈니스 소재 | @NVIDIAAIDev는 보관 처리되고 @NVIDIAAI로 안내됨(검색 요약 기준). 젠슨 황이 X를 시작했다는 보도는 있지만 핸들은 확인하지 못함 |
| Hugging Face (+ CEO @ClementDelangue) | [x.com/huggingface](https://x.com/huggingface)<br>최근 확인 2025-08-05(@ClementDelangue) | ai_tools | 영어 | 수시간 이내 | 중간 | 06_중국·오픈모델. huggingface.co/models?sort=trending도 함께 | 오픈소스 모델 트렌딩과 새 데모. 'gpt-oss가 HF 트렌딩 1위'처럼 생태계 흐름을 숫자로 → '이번 주 뜬 무료 AI' | 모델마다 라이선스가 달라서 '무료'라고 쓰기 전에 상업 이용 가능 여부 확인. 팔로워 약 80.6만(스니펫) |
| Midjourney | [x.com/midjourney](https://x.com/midjourney)<br>최근 확인 2026-07-24 | ai_tools | 영어 | 1차 | 높음 | 05_바이럴·크리에이티브. updates.midjourney.com도 함께 | V8, V8.1, V8.2(2026-07-24 기본 모델) → '같은 프롬프트, 버전별 비교' 캐러셀 | 남의 결과물은 크레딧 필수. 직접 생성해서 비교하는 방식 권장 |
| Runway | [x.com/runwayml](https://x.com/runwayml)<br>최근 확인 2025-12-17 | ai_tools | 영어 | 1차 | 높음 | 05_바이럴·크리에이티브 | Gen-4.5(2025-12), '월드 시뮬레이터' 비전. 영화 같은 공식 데모 → 릴스 '이게 AI라고?' | 공식 데모는 잘 나온 결과만 고른 것일 수 있다고 캡션에 밝히기. 2026년 게시물은 검색으로 확인하지 못함 |
| Kling AI | [x.com/Kling_ai](https://x.com/Kling_ai)<br>최근 확인 2026-09-27 | ai_tools | 영어 | 1차 | 중간 | 05_바이럴·크리에이티브 | 콰이쇼우의 영상 AI. Kling 3.0('Everyone a Director', 15초 클립, 네이티브 오디오). 2026-09-27 'CLING ON! We've got news'로 새 발표 예고 | 이벤트·프로모션 게시물이 많으니 기능 발표만 골라낼 것 |
| 영상·이미지 AI 2군: Pika / Hailuo(MiniMax) / Luma / Black Forest Labs | [x.com/pika_labs](https://x.com/pika_labs)<br>보조: @Hailuo_AI, @LumaLabsAI, @bfl_ml<br>최근 확인 2026-04-02(Pika) | ai_tools | 영어 | 1차 | 중간 | 05_바이럴·크리에이티브에 4개 모두 | Pika(실시간 영상 채팅 PikaStream 1.0, AI 전용 소셜 영상 앱), Hailuo(MiniMax H3), Luma(Ray3.2, 2026-06-09), BFL(FLUX 3: 이미지·영상·오디오와 로봇 동작 예측, 2026-07) → '새로 나온 이상한 AI 기능' 소재 | Luma, BFL, Hailuo는 X 게시물 날짜를 확인하지 못함. 공식 블로그(lumalabs.ai/news, bfl.ai/blog, hailuoai.video)와 교차 확인 |
| Suno | [x.com/suno](https://x.com/suno)<br>보조: @SunoMusic<br>최근 확인 2025-09-23 | ai_tools | 영어 | 1차 | 높음 | 05_바이럴·크리에이티브. suno.com/release-notes도 함께 | v5, Personas → 'AI가 만든 노래' 문화 뉴스와 따라 하기 튜토리얼 | 핸들이 섞여 있음(v5 발표는 @suno, @SunoMusic에는 2024년 게시물). 2026년 게시물은 미확인이라 릴리스 노트를 우선. AI 음악 저작권 분쟁을 함께 언급 |
| ElevenLabs | [x.com/ElevenLabs](https://x.com/ElevenLabs)<br>최근 확인 2026-09-28 | ai_tools | 영어 | 1차 | 높음 | 05_바이럴·크리에이티브 | Eleven v4·v4 Turbo(2026-09-28, Artificial Analysis TTS 1위), 유니버설뮤직그룹과 파트너십(2026-09-10) → '내 목소리를 복제하면?' 체험형 콘텐츠 | 예전 핸들 @elevenlabsio도 남아 있음. 목소리 복제 콘텐츠는 딥페이크 윤리 문제를 함께 다룰 것 |
| Perplexity (+ CEO @AravSrinivas) | [x.com/AravSrinivas](https://x.com/AravSrinivas)<br>보조: @perplexity_ai<br>최근 확인 2026-06-04 | ai_tools | 영어 | 1차 | 중간 | @AravSrinivas는 02_핵심인물, @perplexity_ai는 01_공식발표 | Perplexity Computer(2026-02-25), Personal Computer(2026-06), 매출 1억→5억 달러 같은 경영 지표 → 비즈까페형 AI 스타트업 콘텐츠 | CEO 발언에는 홍보 성격이 섞여 있음. 수치는 언론 보도와 교차 확인. @perplexity_ai의 2026년 게시물은 확인하지 못함 |
| Cursor | [x.com/cursor_ai](https://x.com/cursor_ai)<br>최근 확인 2026-06-16 | ai_tools | 영어 | 1차 | 높음 | 07_비즈니스. cursor.com/changelog도 함께 | 바이브코딩 대표 툴. Projects(2026-09), /visualize. 2026-06 SpaceX가 인수(CNBC 보도, 약 600억 달러)하고 SpaceXAI 팀에 합류 → AI 인수합병 뉴스의 중심 | 개발자 대상 정보가 많으니 일반 독자용으로 풀어 쓸 것. 소유 구조가 바뀐 점을 표기 |

### 2-2. 핵심 인물

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 |
|---|---|---|---|---|---|---|---|---|
| Sam Altman | [x.com/sama](https://x.com/sama)<br>최근 확인 2026-09-28 | ai_news | 영어 | 1차(공식 발표보다 먼저 예고) | 높음 | 02_핵심인물. 알림 켜기 | "Here is our current plan for OpenAI"(2026-06-08), DevDay 전날 예고(2026-09-28) → '샘 알트먼이 오늘 한 말' 인용 카드 | 짧은 예고성 트윗을 확정 사실처럼 쓰지 말 것 |
| Logan Kilpatrick | [x.com/OfficialLoganK](https://x.com/OfficialLoganK)<br>최근 확인 2026-09-23 | ai_news | 영어 | 1차 | 높음 | 02_핵심인물. 알림 켜기 | Google AI Studio·Gemini API 담당. Gemini 3.1 Pro, Gemini 4 사전학습 시작(2026-07-21), 3.8 Flash TTS(2026-09-23)를 가장 먼저 올림 | 개인 계정이라 농담도 섞여 있음. 제품명과 날짜는 공식 블로그로 확인. 팔로워 약 27.5만(스니펫) |
| Demis Hassabis | [x.com/demishassabis](https://x.com/demishassabis)<br>최근 확인 2026-08-05 | ai_research | 영어 | 1차 | 높음 | 02_핵심인물 | 노벨상 수상자. Gemma 4(1.5억 다운로드 이상), 과학 AI 비전 → 해설형 콘텐츠에 무게감 | **[역할 변경]** 2026-08-05 Google DeepMind 의장 겸 Alphabet 수석과학자로 옮김. 직함 표기 주의 |
| Andrej Karpathy | [x.com/karpathy](https://x.com/karpathy)<br>최근 확인 2026-05-19 | ai_research | 영어 | 수시간(해설 중심) | 높음 | 02_핵심인물 | '바이브코딩'이라는 말을 만든 인물. 'slopacolypse'(2026-01), autoresearch 저장소, Sequoia Ascent 대담 → 로만형 해설 소재 | **[소속 변경]** 2026-05-19 Anthropic 합류(본인 트윗, Axios). 긴 글은 요약하다 뜻이 바뀌기 쉬우니 원문 인용 |

### 2-3. 리크·벤치마크

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 |
|---|---|---|---|---|---|---|---|---|
| TestingCatalog (Alexey Shabanov) | [x.com/testingcatalog](https://x.com/testingcatalog)<br>+ testingcatalog.com<br>최근 확인 2026-08-02 | ai_news | 영어 | 1차(출시 전 리크) | 중간 | 03_리크·벤치마크. 알림 켜기. 사이트 RSS도 함께 | 출시 전 기능을 앱·웹 코드에서 찾아내는 대표 리크 계정(베를린, 팔로워 약 7.8만). Google I/O 리크, OpenAI 상시 에이전트 예고 | 리크는 게시물에 '루머/리크' 표시 필수. 실례: DevDay 전에 'o'로 예고된 상시 에이전트가 실제로는 'dots'라는 이름으로 발표됨. 이름과 세부는 틀릴 수 있음 |
| Tibor Blaho | [x.com/btibor91](https://x.com/btibor91)<br>+ Threads @btibor91<br>최근 확인 2025-12-28 | ai_news | 영어 | 1차(출시 전 리크) | 높음 | 03_리크·벤치마크 | ChatGPT 웹앱 코드에서 Pro Lite, 월 500달러 Pro Max, 광고 도입 흔적 등을 찾아냄. Decrypt, Yahoo Tech, Vice가 인용 보도 → '곧 바뀌는 ChatGPT 요금제' | 코드에 흔적이 있다고 출시가 확정된 것은 아님. '코드에서 발견됨'이라고 정확히 쓸 것 |
| Chetaslua | [x.com/chetaslua](https://x.com/chetaslua)<br>최근 확인 2026-01-28 | ai_news | 영어 | 1차(출시 전 리크) | 낮음 | 03_리크·벤치마크에만 넣고 단독 게시 금지 | 미공개 Gemini 체크포인트를 직접 테스트한 결과를 공유(예: 'Snow Bunny'가 Gemini 3 Pro GA라는 추정). 'legit' 리크 커뮤니티 소속 | **[수정]** 초안의 'Gemini 4 Pro 리크를 가장 먼저 포착'은 근거가 없어 삭제. 리크끼리 모순이 잦으니 TestingCatalog나 공식 발표와 교차 확인 |
| Lisan al Gaib | [x.com/scaling01](https://x.com/scaling01)<br>최근 확인 2026-09-29 | ai_research | 영어 | 수시간 이내(출시 직후) | 중간 | 03_리크·벤치마크 | 새 모델이 나오면 시스템카드 벤치마크를 가장 빨리 표로 정리(Opus 5.5 벤치마크, 2026-09-22). 자체 벤치마크 LisanBench → '신모델 성적표' 원자료 | 밈과 과격한 표현이 섞여 있음. 숫자는 시스템카드나 Artificial Analysis로 재확인 |
| Artificial Analysis | [x.com/ArtificialAnlys](https://x.com/ArtificialAnlys)<br>+ artificialanalysis.ai<br>최근 확인 2026-09-28 | ai_research | 영어 | 수시간 이내(출시 1~2일 안에 평가) | 높음 | 03_리크·벤치마크. 리더보드는 주 1회 확인 | LLM·이미지·음성 독립 벤치마크. Intelligence Index, TTS 1위 교체(Eleven v4), Terminal-Bench-Science. 업스테이지 Solar Pro 4(42점) 같은 한국 모델도 평가 → '이번 달 AI 순위' 정기 콘텐츠 | 차트 캡처 시 출처 표기 필수. 벤치마크 점수가 실사용 체감과 같지 않다고 캡션에 적기 |
| LMArena (Arena) | [x.com/lmarena_ai](https://x.com/lmarena_ai)<br>+ [arena.ai 리더보드 변경 로그](https://arena.ai/company/leaderboard-changelog)<br>최근 확인 2025-09-16 | ai_research | 영어 | 수시간 이내 | 높음 | 03_리크·벤치마크. 당분간 변경 로그를 함께 봄 | 사용자 투표 기반 순위표. 'Leaderboard Disrupted' 같은 순위 변동 공지. 익명 신모델이 먼저 등장하는 곳이라 리크의 원천도 됨 | **[핸들 주의]** 서비스 이름이 Arena(arena.ai)로 바뀌었고 X 표시 이름도 'Arena.ai'였음. 2026년 게시물은 검색되지 않음 → 핸들이 바뀌었는지 X에서 직접 확인 |

### 2-4. 큐레이터·해설

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 |
|---|---|---|---|---|---|---|---|---|
| Rowan Cheung / The Rundown AI | [x.com/rowancheung](https://x.com/rowancheung)<br>보조: @TheRundownAI<br>최근 확인 2025-07-29(@TheRundownAI) | ai_news | 영어 | 수시간(뉴스레터는 매일) | 중간 | 04_큐레이터·해설. **뉴스레터를 이메일로 구독해 주 채널로** | 구독자 200만 명 이상인 AI 뉴스레터 The Rundown 창업자. X 약 59.1만, 인스타 약 44.1만 → 한국 AI 계정들이 무엇을 다룰지 미리 보는 벤치마크 | **[2026 X 활동 미확인]** 그대로 번역하면 표절. 1차 출처를 찾아가 자기 시각으로 다시 쓸 것 |
| Chubby (Kim Isenberg) | [x.com/kimmonismus](https://x.com/kimmonismus)<br>최근 확인 2026-09-29 | ai_news | 영어 | 수시간 이내 | 중간 | 04_큐레이터·해설 | 독일의 AI 분석가. 'AI gone wild'류 신기한 영상과 뉴스 분석을 섞어 올림 → 괴짜 소재와 해설 소재를 한 번에. Superintelligence 뉴스레터(22.5만 명 이상) | 남의 영상을 재공유하는 경우가 많으니 원작자를 추적해 크레딧. 팔로워 약 11.7만~13.9만(스니펫) |
| Rohan Paul | [x.com/rohanpaul_ai](https://x.com/rohanpaul_ai)<br>최근 확인 2026-05-24 | ai_research | 영어 | 수시간 이내 | 중간 | 04_큐레이터·해설. 게시량이 많으니 알림은 끄기 | 'Compiling in real-time, the race towards AGI'. 하루 수십 건의 뉴스·논문·인터뷰 클립 → 놓친 뉴스를 찾는 안전망 | 양이 많아서 중요도는 직접 판단. 원출처 링크로 확인. 팔로워 약 15.8만(스니펫) |
| DailyPapers (@HuggingPapers) + AK (@_akhaliq) | [x.com/HuggingPapers](https://x.com/HuggingPapers)<br>+ huggingface.co/papers<br>최근 확인 2026-03-29(@HuggingPapers), 2024-09-12(@_akhaliq) | ai_research | 영어 | 1차(논문 공개 당일) | 중간 | 04_큐레이터·해설. huggingface.co/papers 매일 확인 | HF Daily Papers 트렌딩 논문 → '기묘한 AI 논문' 코너(괴짜)와 '논문 쉽게 읽기'(해설) | **[대표 핸들 수정]** AK는 2023-05 약 1.7만 건 트윗 뒤 논문 소개를 HF Daily Papers로 옮긴다고 밝힘. @_akhaliq의 2026년 게시물은 확인하지 못함. 논문 그림은 저자 크레딧 필수. @HuggingPapers 팔로워 약 2.2만 |
| 歸藏 (guizang.ai) | [x.com/op7418](https://x.com/op7418)<br>최근 확인 2026-08-31 | ai_tools | 중국어 | 수시간 이내 | 중간 | 06_중국·오픈모델. X 번역 기능 활용 | 베이징의 제품 디자이너. 중국 AI 이미지·영상 툴과 디자인 워크플로를 서구 계정보다 빨리 소개 → 한국에 덜 알려진 소재 | 번역 오류 주의. 툴 이름과 수치는 공식 페이지로 확인. X 팔로워 수는 확인 불가(GitHub 약 4,900) |
| Ethan Mollick | [x.com/emollick](https://x.com/emollick)<br>최근 확인 2026-09-18 | ai_research | 영어 | 수시간(해설 중심) | 높음 | 02_핵심인물. 뉴스레터 One Useful Thing도 구독 | 와튼스쿨 교수. 'The Overhang'(2026-09-18, Forbes가 소개), AI로 인한 탈숙련 → 로만형 논점 출처 | 의견은 반드시 그의 견해로 인용하고 사실처럼 단정하지 말 것 |
| vitrupo | [x.com/vitrupo](https://x.com/vitrupo)<br>+ Threads @vitrupo<br>최근 확인 2026-01-24 | ai_research | 영어 | 수시간~하루 | 높음 | 04_큐레이터·해설 | AI 리더 인터뷰의 핵심 발언 클립(Amanda Askell, Sam Altman, Kyle Fish) → '이번 주 AI 명언' 인용 카드 | 클립은 잘라낸 것이니 맥락을 확인하고 원본 영상 링크 표기. 영상 재업로드 금지 |

### 2-5. 괴짜·바이럴

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 |
|---|---|---|---|---|---|---|---|---|
| Min Choi | [x.com/minchoi](https://x.com/minchoi)<br>최근 확인 2026-04-21 | ai_fun_viral | 영어 | 수시간 이내(출시 당일~다음 날) | 중간 | 05_바이럴·크리에이티브 | 새 모델이 나오면 '10 wild examples' 형식으로 놀라운 결과물을 모음(ChatGPT Images 2.0, Veo 3의 '실제로 없었던 길거리 인터뷰') → ai_freaks.kr형 '이게 AI라고?' 캐러셀 구조 참고 | 예시마다 원작자가 따로 있음. 개별 크레딧을 붙이거나 허락받기. 모음 게시물을 통째로 가져가지 말 것 |
| Justine Moore (a16z) | [x.com/venturetwins](https://x.com/venturetwins)<br>최근 확인 2026-07-18 | ai_fun_viral | 영어 | 하루 이내 | 높음 | 05_바이럴·크리에이티브 | a16z 파트너. 일본 AI 영상(2026-05), AI 결혼식 영상(2026-07)처럼 화제가 된 AI 영상을 골라 투자자 시각의 코멘트를 붙임 | 영상 원작자(인스타·레딧 크리에이터)를 추적해 크레딧. 재업로드 전에 허락 |
| el.cine | [x.com/EHuanglu](https://x.com/EHuanglu)<br>최근 확인 2026-08-11 | ai_fun_viral | 영어 | 수시간 이내 | 중간 | 05_바이럴·크리에이티브 | AI 영화감독 겸 컨설턴트. 'AI video is now undetectable'(2026-08-11) 같은 충격 데모와 단계별 튜토리얼 → 릴스용 'AI로 영화 만들기' | Higgsfield 등 특정 툴 홍보가 잦음. Higgsfield는 2026-02 미공개 유료 홍보 논란 뒤 X 계정이 정지됨 → 광고인지 판단하기 어려우니 추천 툴 소개 시 주의 |
| Angry Tom | [x.com/AngryTomtweets](https://x.com/AngryTomtweets)<br>최근 확인 2025-07-12(본인), 2026-09-26(타 계정 보도) | ai_fun_viral | 영어 | 수시간 이내 | 낮음 | 05_바이럴·크리에이티브 | '밈이 영상이 됐다: 웃긴 예시 10개' 같은 AI 영상 모음. 'Pixar가 2년 걸릴 걸 AI로 2시간에'(2026-09 화제) → 괴짜 소재 | 과장 캡션과 툴 홍보가 섞여 있음(위 영상은 Pocket FM의 Sherpa 툴 사용 사례로 보도됨). '약 220만'은 보도 수치이고 X 단독인지 불명 |
| AI Notkilleveryoneism Memes | [x.com/AISafetyMemes](https://x.com/AISafetyMemes)<br>최근 확인 2026-01-27 | ai_fun_viral | 영어 | 수시간 이내 | 낮음 | 05_바이럴·크리에이티브 | AI가 이상하게 행동한 사례(탈출 시도, 자원 축적 같은 실험 보고)와 AI 위험론 밈 → 'AI가 수상하다' 코너 소재 탐색 | AI 위험을 강조하는 성향이 뚜렷함. 원 연구나 기사를 확인해 공포 조장 없이 사실 위주로 다시 쓸 것 |
| Bilawal Sidhu | [x.com/bilawalsidhu](https://x.com/bilawalsidhu)<br>+ 인스타·Threads @bilawal.ai<br>X 게시물은 2026년 미확인, 프로젝트는 2026-08 | ai_fun_viral | 영어 | 하루 이내 | 높음 | 05_바이럴·크리에이티브. 인스타와 Substack도 있음 | 전 구글 3D Maps 출신. 실시간 항공기·위성·CCTV를 3D 지구본에 얹은 'God's Eye View'(2026-08 GitHub 트렌딩 1위, 소셜 합산 2,500만 뷰 이상) 같은 공간 AI 데모 | **[X 활동 미확인]** 인스타·Threads를 우선. 작품 영상은 본인 저작물이니 크레딧 필수. '160만 명 이상'은 여러 플랫폼 합산 |

### 2-6. 한국

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 |
|---|---|---|---|---|---|---|---|---|
| Sung Kim (업스테이지 대표) + Upstage | [x.com/hunkims](https://x.com/hunkims)<br>보조: @upstageai<br>최근 확인 2026-07-22 | korea_ai | 영어/한국어 | 1차 | 높음 | 08_한국에 두 계정 | Solar Pro 4(Artificial Analysis 42점), Solar Open 2 같은 한국 LLM 소식을 X에 먼저 올림 → '한국 AI가 세계에서 몇 등인가' | 자사 홍보 성격. 벤치마크 수치는 Artificial Analysis 게시물과 교차 확인 |
| LG AI Research / NAVER Cloud | [x.com/LG_AI_Research](https://x.com/LG_AI_Research)<br>보조: @NAVER__Cloud<br>최근 확인 2026-01-12(LG) | korea_ai | 영어/한국어 | 1차 | 높음(LG) | 08_한국. 국내 보도자료는 LG·네이버 뉴스룸에서 | K-EXAONE(2026-01), K-EXAONE 2.0 750B, EXAONE Deep → '소버린 AI', '국가대표 AI 모델' 같은 정책·비즈니스 뉴스와 연결 | **[NAVER Cloud 활동 미확인]** 프로필만 검색됨 → 네이버 뉴스룸(navercorp.com)을 우선. 영문 게시물은 국내 발표와 시차가 있을 수 있음 |
| 조경현 (Kyunghyun Cho) | [x.com/kchonyc](https://x.com/kchonyc)<br>최근 확인 2026-01-22 | korea_ai | 영어 | 하루 이내 | 높음 | 08_한국 | 뉴욕대 교수이자 세계적인 한국인 AI 연구자. 연구·책 추천, 업스테이지 Solar Open 100B 기술보고서 소개(2026-01-05) → 해설형 콘텐츠의 신뢰도 | 학술 표현이 많으니 인용할 때 뜻이 바뀌지 않게. 2026-01 Genentech을 떠남. 팔로워 약 8.5만 이상(스니펫) |
| GeekNews (하다) | [x.com/GeekNewsHada](https://x.com/GeekNewsHada)<br>날짜 미확인 | korea_ai | 한국어 | 수시간 이내 | 높음 | 08_한국. 뉴스레터·슬랙봇·텔레그램으로도 구독 가능 | 해커뉴스 등 해외 기술 뉴스를 한국어로 요약하는 커뮤니티. 새 글이 X로 자동 발행 → 한국 개발자들이 지금 주목하는 AI 툴과 이슈 | 요약문을 그대로 쓰지 말고 원문 기사로 확인. 공지는 @GeekNewsBot에서 따로 올라옴 |
| 한국 IT 미디어: AI타임스 / 요즘IT | [x.com/AITimes_News](https://x.com/AITimes_News)<br>보조: @yozm_it<br>날짜 미확인 | korea_ai | 한국어 | 하루 이내 | 중간 | 08_한국. aitimes.com 사이트를 함께 | AI타임스는 국내외 AI 기사를 한국어로 보도. 요즘IT는 봇 없이 직접 IT·AI 실무 콘텐츠를 올림 → 국내 기업 도입 사례 같은 국내 맥락 | 기사 본문을 옮기면 저작권 침해. 요약하고 링크와 매체명 표기. @AITIMES1은 인공지능신문(다른 매체). X 게시 빈도는 미확인 |

### 2-7. 경쟁 벤치마크 (뉴스 소스가 아니라 형식 참고용, Threads)

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 |
|---|---|---|---|---|---|---|---|---|
| CHOI | [threads.com/@choi.openai](https://www.threads.com/@choi.openai?hl=ko) | korea_ai | 한국어 | 수시간 이내 | 중간 | Threads에서 팔로우. 주 1회 인기 게시물 형식 분석 | '대한민국 최고의 AI 채널'을 내건 Threads 계정(팔로워 약 29.4만, 게시물 1.1만 건, OpenAI Codex Ambassador) → 해외 AI 뉴스가 한국 SNS에서 어떤 톤으로 소비되는지 확인 | 경쟁 계정이니 형식 참고용으로만. X의 @arrakis_ai('CHOI' 표시명, OpenCodex 게시)와 같은 사람인지는 확인하지 못함 |
| AI TREND KOREA ㅣ 에트매거진 | [threads.com/@ai.trend.kr](https://www.threads.com/@ai.trend.kr?hl=ko)<br>+ 인스타 @ai.trend.kr | korea_ai | 한국어 | 하루~주간 요약 | 중간 | 인스타와 Threads 모두 팔로우. 게시 빈도, 커버 디자인, 캡션 구조를 주 1회 분석 | 만들려는 것과 같은 '한국 AI 매거진형' 계정. 주간 AI 뉴스 정리, 실사용 사례 → 직접 경쟁 벤치마크(GitHub의 카드뉴스 자동화 프로젝트가 "ai.trend.kr, ai_freaks.kr, choi.openai를 이겨야 한다"고 적음) | 형식만 참고하고 차별화 포인트를 정할 것. Threads 약 9,400명(스니펫) |

### 2-8. 이번 검증에서 추가한 소스 (5개)

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법 | 활용 포인트 | 주의 |
|---|---|---|---|---|---|---|---|---|
| **[추가]** a16z (Andreessen Horowitz) | [x.com/a16z](https://x.com/a16z)<br>+ a16z.com/newsletter<br>최근 확인 2025-12-10 | startup | 영어 | 하루~주간 | 높음 | 07_비즈니스. 뉴스레터도 구독 | 'Big Ideas 2026' 같은 VC 전망 보고서. **BZCF가 실제로 번역해 쓴 원본**으로 확인됨(`source-tracing.md`) → 비즈까페형 '세계 최고 VC가 투자하겠다는 분야' 콘텐츠 | 보고서 전문은 저작물이니 요지 번역과 링크로. 포트폴리오 홍보 성격을 감안 |
| **[추가]** Techmeme | [x.com/Techmeme](https://x.com/Techmeme)<br>+ techmeme.com<br>날짜 미확인(사이트는 2026년 활동 확인) | business | 영어 | 수시간 이내 | 높음 | 07_비즈니스. 원문은 techmeme.com에서 | 2005년부터 운영한 테크 뉴스 애그리게이터. 사람 에디터와 알고리즘이 주요 보도를 순위로 매김 → '오늘 가장 중요한 비즈니스·AI 뉴스' 필터 | X 게시물에는 링크가 빠져 있음(X API 비용 문제). 헤드라인만 보고 쓰지 말고 원문 기사까지 확인 |
| **[추가]** Simon Willison | [x.com/simonw](https://x.com/simonw)<br>+ simonwillison.net<br>최근 확인 2026-09-21 | ai_tools | 영어 | 수시간~하루 | 높음 | 04_큐레이터·해설. 블로그 RSS | 신모델을 직접 써 보고 가격 대비 성능(Artificial Analysis 파레토 곡선), 사용 메모를 블로그에 정리(DeepSeek-V4-Flash, Claude Sonnet 5.5 등) → 로만형 '직접 써 보니' 해설 | 개발자 관점이라 일반 독자용으로 풀어 쓸 것. 인용 시 블로그 원문 링크 |
| **[추가]** Wes Roth | [x.com/WesRoth](https://x.com/WesRoth)<br>최근 확인 2026-09-02 | ai_news | 영어 | 수시간 이내 | 중간 | 04_큐레이터·해설 | AI 뉴스 유튜버. xAI의 SpaceXAI 개명을 하루 만에 보도(2026-07-07). 빅테크 감원, 중국 로봇 스타트업 같은 뉴스 → 빠른 2차 속보 | 2차 출처라 1차 확인 필수. 유튜브식 과장 표현 주의 |
| **[추가]** Koray Kavukcuoglu | [x.com/koraykv](https://x.com/koraykv)<br>최근 확인 2025-11-18 | ai_news | 영어 | 1차 | 높음 | 02_핵심인물 | Google DeepMind SVP. 2026-09 보도에서 'DeepMind의 새 수장'으로 소개됨. Gemini 3 출시 때 성적표 스레드를 올렸고, 2026-09-23~24 Gemini 4 조기 출시 방침을 밝힘 → Gemini 4 출시일 포착용 | 2026년 X 게시물은 검색으로 확인하지 못함. 직함은 최신 보도로 확인 |

---

## 3. X 리스트 구성과 알림 전략 (정리본)

초안의 번호가 겹쳐서 **비공개 리스트 8개**로 다시 정리했습니다. 비공개 리스트는 추가해도 상대에게 알림이 가지 않습니다. 리스트는 최대 1,000개, 리스트당 5,000명까지 만들 수 있습니다.

| 리스트 | 계정 |
|---|---|
| 01_공식발표 | OpenAI, OpenAIDevs, ChatGPTapp, AnthropicAI, claudeai, ClaudeDevs, GoogleDeepMind, GeminiApp, Google, AIatMeta, SpaceXAI, grok, perplexity_ai |
| 02_핵심인물 | sama, OfficialLoganK, koraykv, demishassabis, karpathy, bcherny, AravSrinivas, emollick, ClementDelangue |
| 03_리크·벤치마크 | testingcatalog, btibor91, chetaslua, scaling01, ArtificialAnlys, lmarena_ai |
| 04_큐레이터·해설 | kimmonismus, rohanpaul_ai, HuggingPapers, _akhaliq, vitrupo, rowancheung, TheRundownAI, simonw, WesRoth |
| 05_바이럴·크리에이티브 | minchoi, venturetwins, EHuanglu, AngryTomtweets, AISafetyMemes, bilawalsidhu, midjourney, runwayml, Kling_ai, pika_labs, Hailuo_AI, LumaLabsAI, bfl_ml, suno, ElevenLabs |
| 06_중국·오픈모델 | deepseek_ai, Alibaba_Qwen, Kimi_Moonshot, Zai_org, MiniMax_AI, MistralAI, huggingface, op7418 |
| 07_비즈니스 | a16z, Techmeme, NVIDIAAI, nvidianewsroom, cursor_ai |
| 08_한국 | hunkims, upstageai, LG_AI_Research, NAVER__Cloud, kchonyc, GeekNewsHada, AITimes_News, yozm_it |

- **알림은 6개만 켭니다**: @OpenAI, @sama, @AnthropicAI, @GoogleDeepMind(또는 @OfficialLoganK), @deepseek_ai, @testingcatalog.
- 나머지는 **하루 두 번(아침·저녁) 리스트를 10분씩** 훑습니다.
- **콘텐츠 파이프라인**
  1. 01·03 리스트에서 '무슨 일이 일어났나'(속보와 리크)
  2. 02·04 리스트에서 '왜 중요한가'(해설, 로만형)
  3. 05 리스트에서 '사람들이 뭘 만들었나'(괴짜·바이럴, ai_freaks형)
  4. 07·08 리스트에서 '돈과 한국에는 어떤 의미인가'(비즈까페형과 국내 맥락)
  - 한 이슈를 이 네 단계로 묶으면 캐러셀 한 편이 됩니다.

---

## 4. 우선순위 Top 10

| 순위 | 소스 | 왜 |
|---|---|---|
| 1 | **OpenAI (@OpenAI + @sama)** | 한국 독자가 가장 많이 쓰는 AI라 반응이 가장 큽니다. 2026-09-29 DevDay처럼 한 번에 20여 건씩 발표가 나오고, 알트먼이 전날 예고하는 패턴이 있어 '예고 → 발표 → 정리' 3연속 게시물을 만들 수 있습니다. |
| 2 | **Google (@GoogleDeepMind + @OfficialLoganK)** | Gemini 4가 사후학습 단계이고 '가능한 한 빨리' 내놓겠다고 밝혀서, 가까운 시일의 최대 이벤트 후보입니다. Nano Banana처럼 따라 하기 좋은 소비자 기능도 여기서 나옵니다. |
| 3 | **Anthropic (@AnthropicAI + @claudeai)** | 모델 출시와 함께 안전·해석가능성 연구가 꾸준히 나와서 로만형 '이해하는 AI' 소재가 가장 풍부합니다. Karpathy 합류처럼 인물 뉴스도 겹칩니다. |
| 4 | **TestingCatalog** | 출시 전 리크를 가장 먼저 잡는 계정입니다(2026-08 활동 확인). 'RUMOR' 라벨을 붙인 '곧 나올 기능' 게시물로 경쟁 계정보다 하루 먼저 다룰 수 있습니다. 다만 이름과 세부는 틀릴 수 있습니다('o' → 실제 'dots'). |
| 5 | **Artificial Analysis** | 순위가 바뀌는 순간이 곧 콘텐츠입니다('이번 달 AI 순위'). 업스테이지 같은 한국 모델도 평가해 한국 각도를 붙이기 쉽습니다. 2026-09-28까지 활동이 확인됩니다. |
| 6 | **Chubby (@kimmonismus)** | 신기한 AI 영상(괴짜)과 뉴스 분석(해설)을 한 계정에서 매일 얻습니다(2026-09-29 활동 확인). 1인 운영자의 시간 대비 효율이 가장 높습니다. |
| 7 | **Min Choi (@minchoi)** | 신모델이 나오면 '10 wild examples'를 다음 날까지 모읍니다. ai_freaks.kr형 캐러셀의 구조를 그대로 참고할 수 있습니다(원작자 크레딧 필수). |
| 8 | **Ethan Mollick (@emollick)** | 'Overhang'과 탈숙련 같은 논점을 매주 던집니다. 뉴스가 적은 날에도 로만형 해설 게시물을 만들 수 있는 '생각거리' 공급원입니다. |
| 9 | **a16z (@a16z)** [추가] | BZCF가 실제로 번역해 쓴 원본으로 확인된 유일한 X 소스입니다. 비즈까페형 '투자자가 보는 다음 트렌드' 콘텐츠의 1차 출처입니다. |
| 10 | **한국 모델: @hunkims(업스테이지) + @LG_AI_Research** | 해외 소식만 번역하는 계정들과 차별화하는 '한국에는 어떤 의미인가' 단계를 담당합니다. Solar Pro 4, K-EXAONE처럼 세계 순위와 연결되는 소식이 나옵니다. |

차순위: @deepseek_ai와 @Alibaba_Qwen(중국 모델 충격 뉴스는 예고 없이 나와서 알림 필수), @Techmeme(비즈니스 속보 필터), @venturetwins(바이럴 영상 큐레이션).

---

## 5. 제거한 항목과 이유

| 항목 | 이유 |
|---|---|
| **Legit (@legit_api)** | (1) 검색에 잡힌 가장 최근 게시물이 2025-06-10입니다. 2026년 활동 근거가 없습니다. (2) 초안의 'Gemini 4 Pro 리크를 가장 먼저 포착'은 근거가 없습니다. 해당 리크는 TestingCatalog, StartupFortune, BigGo가 보도했고, 이 계정의 것이라는 결과가 없었습니다. (3) 신호대잡음이 '낮음'인 리크 계정이라 활동이 확인된 @chetaslua 하나로 충분합니다. |

**초안 단계에서 이미 제외된 항목** (검증 결과 동의):
- **'legit_rumors'**: 이전 단계 후보 목록에 있던 이름입니다. 검색 결과에 이 핸들이 전혀 나오지 않아 존재를 확인할 수 없습니다.
- **Jimmy Apples (@apples_jimmy)**: 계정을 삭제했다가 돌아온 이력이 있고 '트롤'이라는 의혹이 있습니다. 출처로 쓰기에 부적합합니다.
- **AI Leaks and News (@AILeaksAndNews)**: 다른 리크를 재공유하는 2차 계정입니다(약 7,100명). 2026-04 활동은 확인되지만 원출처가 아닙니다.
- **@soraofficialapp**: OpenAI가 2026-03-24 Sora 종료를 공지했습니다. 앱은 2026-04-26, API는 2026-09-24에 종료됐습니다. 휴면 계정입니다.
- **@xai**: 2026-07-06 @SpaceXAI로 바뀌었습니다.
- **@NVIDIAAIDev**: 보관 처리돼 @NVIDIAAI로 안내됩니다.

**추가 후보로 검토했지만 보류한 계정**:

| 계정 | 판단 |
|---|---|
| @heyBarsee | 검색상 최근 게시물이 2025-04이고, 2026년 활동을 확인하지 못했습니다. |
| @ai_for_success | 2026-05 활동이 확인됩니다. AI 뉴스와 밈 계정이지만 이미 있는 큐레이터와 겹칩니다. |
| @dreamingtulpa | 2026-07-25 FLUX 3 실험 게시물이 확인됩니다. AI 아트 실험 계정이라 괴짜 소재가 부족할 때 추가할 만합니다. |
| @theneurondaily | 구독자 약 70만의 뉴스레터입니다. X 활동 빈도는 미확인이라 뉴스레터 목록에서 다루는 편이 맞습니다. |
| @bensbitesdaily | 2024-09부터 주 2회로 바뀌었습니다. 뉴스레터 목록에서 다룹니다. |
| @slow_developer | AGI 논쟁형 코멘트 계정입니다. 신호가 약합니다. |

**찾지 못한 공백** (사용자가 직접 확인):
- ByteDance Seed / Seedance의 공식 X 계정: 공식 사이트, GitHub, Hugging Face만 확인됐습니다.
- Higgsfield: AI Freaks의 협업사입니다. 2026-02-09에 @higgsfield_ai가 정지된 뒤 현재 어떤 핸들이 활동하는지 확인하지 못했습니다.
- Liner: AI Freaks의 협업사입니다. X 계정을 찾지 못했습니다.
- 젠슨 황의 X 핸들: 계정을 만들었다는 보도만 있고 핸들은 확인하지 못했습니다.

---

## 6. 출처

검증에 쓴 근거입니다. 모두 초안 작성 에이전트가 이 세션에서 받은 WebSearch 결과에 실제로 나온 URL입니다.

**공식 발표**
- OpenAI: [x.com/OpenAI/highlights](https://x.com/OpenAI/highlights), [x.com/OpenAIDevs/status/2069484303281779090](https://x.com/OpenAIDevs/status/2069484303281779090), [x.com/chatgptapp](https://x.com/chatgptapp), [9to5Mac DevDay 2026](https://9to5mac.com/2026/09/29/openai-teases-20-announcements-at-devday-watch-live/), [CNBC DevDay 2026](https://www.cnbc.com/2026/09/29/openai-devday-2026-live-updates.html)
- Anthropic: [AnthropicAI 헌법 게시물](https://x.com/AnthropicAI/status/2014005798691877083), [claudeai: ClaudeDevs 개설](https://x.com/claudeai/status/2044779666477646187), [claudeai: Claude Design](https://x.com/claudeai/status/2045156267690213649), [bcherny](https://x.com/bcherny/status/2074247226038063316)
- Google: [GoogleDeepMind Genie 3](https://x.com/GoogleDeepMind/status/1952732150928724043), [Gemini 4 사후학습 보도(Yahoo Finance)](https://finance.yahoo.com/technology/ai/articles/google-gemini-4-enters-post-122454510.html), [GeminiApp Nano Banana 2](https://x.com/GeminiApp/status/2027052041697464629), [GeminiApp 아바타](https://x.com/GeminiApp/status/2077812539480748035)
- Meta: [x.com/aiatmeta](https://x.com/aiatmeta), [x.com/metaai](https://x.com/metaai), [CNBC Muse Spark](https://www.cnbc.com/2026/04/08/meta-debuts-first-major-ai-model-since-14-billion-deal-to-bring-in-alexandr-wang.html)
- SpaceXAI: [Yahoo Finance 개명 보도](https://finance.yahoo.com/technology/ai/articles/xai-makes-rebrand-spacexai-complete-215010760.html), [x.com/SpaceXAI](https://x.com/SpaceXAI), [xAI Grok Imagine 1.0](https://x.com/xai/status/2018164753810764061)
- Mistral: [Magistral 게시물](https://x.com/MistralAI/status/1932441507262259564), [x.com/MistralDevs](https://x.com/MistralDevs)
- DeepSeek: [유일한 공식 계정 공지](https://x.com/deepseek_ai/status/1884103376868368589), [V4 Preview](https://x.com/deepseek_ai/status/2047516922263285776)
- Qwen: [Alibaba_Qwen](https://x.com/Alibaba_Qwen/status/2078759124914098291), [MarkTechPost Qwen3.8-Max](https://www.marktechpost.com/2026/08/03/alibaba-qwen-releases-qwen3-8-max/), [Qwen 4 Apsara](https://pasqualepillitteri.it/en/news/17552/qwen-4-alibaba-apsara-en)
- 중국 3사: [tphuang 태그 게시물](https://x.com/tphuang/status/2023742103562445188), [Fortune Kimi K3](https://fortune.com/2026/07/16/moonshots-kimi-k3-pushes-chinese-ai-into-fable-level-territory/), [lmarena의 Zai_org 태그](https://x.com/lmarena_ai/status/1955669431742587275)
- NVIDIA: [x.com/NVIDIAAI](https://x.com/NVIDIAAI), [x.com/nvidianewsroom](https://x.com/nvidianewsroom), [@nvidia 게시물](https://x.com/nvidia/status/2031311890752704790)
- Hugging Face: [x.com/huggingface](https://x.com/huggingface), [Clem gpt-oss](https://x.com/ClementDelangue/status/1952827283808375168)
- 크리에이티브 툴: [Midjourney V8.2](https://x.com/midjourney/status/2080781271043911807), [Runway Gen-4.5](https://x.com/runwayml/status/2001352437186334875), [Kling CLING ON](https://x.com/Kling_ai/status/2104224551986925580), [Pika PikaStream](https://x.com/pika_labs/status/2039804583862796345), [x.com/hailuo_ai](https://x.com/hailuo_ai), [Luma Ray3.2](https://lumalabs.ai/news/introducing-ray-3-2), [MarkTechPost FLUX 3](https://www.marktechpost.com/2026/07/26/black-forest-labs-releases-flux-3-a-multimodal-flow-model-for-image-video-audio-and-robot-action-prediction/), [Suno v5](https://x.com/suno/status/1970583230807167300), [Eleven v4](https://x.com/ElevenLabs/status/2104572127617994917), [ElevenLabs·UMG](https://x.com/ElevenLabs/status/2098049234465620251)
- Perplexity: [Perplexity Computer](https://x.com/AravSrinivas/status/2026695864039911684), [CNBC 2026-06](https://www.cnbc.com/2026/06/03/perplexity-ceo-ai-valuations-computer-agentic.html)
- Cursor: [SpaceX 합류 게시물](https://x.com/cursor_ai/status/2066875698346954891), [CNBC 인수 보도](https://www.cnbc.com/2026/06/16/spacex-spcx-cursor-acquisition-ipo.html)

**핵심 인물**
- [sama: OpenAI 계획](https://x.com/sama/status/2064088940932641225), [sama 최근 게시물](https://x.com/sama/status/2104661956879913457)
- [Logan: Gemini 4 사전학습](https://x.com/OfficialLoganK/status/2079594867161022817), [Logan: 3.8 Flash TTS](https://x.com/OfficialLoganK/status/2102785495726219305)
- [Demis Hassabis](https://x.com/demishassabis/status/2085034334914769203)
- [Karpathy: Anthropic 합류](https://x.com/karpathy/status/2056753169888334312), [Axios](https://www.axios.com/2026/05/19/anthropic-openai-karpathy-andrej-claude)
- [Koray Kavukcuoglu Gemini 3](https://x.com/koraykv/status/1990814337330786749), [Northeast Times: DeepMind의 새 수장](https://northeasttimes.com/2026/09/24/google-deepmind-s-new-chief-signals-gemini-4-launch-is-close/)

**리크·벤치마크**
- [x.com/testingcatalog](https://x.com/testingcatalog), [TestingCatalog 'o' 예고 기사](https://www.testingcatalog.com/openai-to-announce-o-always-on-agent-during-devday/)
- [Decrypt Pro Max](https://decrypt.co/379359/openai-500-per-month-chatgpt-pro-max-plan), [btibor91](https://x.com/btibor91/status/2005252132954689619)
- [chetaslua Snow Bunny](https://x.com/chetaslua/status/2016623119826636955), [chetaslua·legit 커뮤니티](https://x.com/chetaslua/status/1974149300348391488), [legit_api](https://x.com/legit_api/status/1932297290875891777), [Gemini 4 Pro 리크 보도(TestingCatalog)](https://www.testingcatalog.com/gemini-4-pro-frontend-ui-taste-leak/)
- [scaling01 Opus 5.5](https://x.com/scaling01/status/2102435665061216267)
- [Artificial Analysis Terminal-Bench-Science](https://x.com/ArtificialAnlys/status/2103265956479070260), [AA Solar Pro 4](https://x.com/ArtificialAnlys/status/2087590023742775472)
- [lmarena_ai](https://x.com/lmarena_ai/status/1965115050273976703), [Arena.ai 표시명 게시물](https://x.com/lmarena_ai/status/1919455362106769849), [arena.ai 변경 로그](https://arena.ai/company/leaderboard-changelog)

**큐레이터·바이럴**
- [rowancheung](https://x.com/rowancheung?lang=en), [TheRundownAI](https://x.com/TheRundownAI/status/1950074079685292326)
- [kimmonismus](https://x.com/kimmonismus/status/2104944586439225497), [rohanpaul_ai](https://x.com/rohanpaul_ai/status/2058431034971263062)
- [HuggingPapers](https://x.com/HuggingPapers/status/2038258691192041735), [AK의 HF 이전 공지(2023)](https://x.com/_akhaliq/status/1654284910700396546?lang=en)
- [op7418](https://x.com/op7418/status/2094246671068864573), [emollick The Overhang](https://x.com/emollick/status/2101010622305493013), [Forbes](https://www.forbes.com/sites/johnwerner/2026/09/26/ethan-mollicks-new-overhang/), [vitrupo](https://x.com/vitrupo/status/2015067894154211648)
- [minchoi](https://x.com/minchoi/status/2046710643479265340), [venturetwins 일본 AI 영상](https://x.com/venturetwins/status/2053526412418781677), [venturetwins 결혼식 영상](https://x.com/venturetwins/status/2078544211448897718)
- [EHuanglu](https://x.com/EHuanglu/status/2087129152667480079), [Higgsfield 정지 보도](https://piunikaweb.com/2026/02/11/higgsfield-ai-ceo-speaks-up-after-x-account-suspension-negative-pr/)
- [AngryTomtweets 2025](https://x.com/AngryTomtweets/status/1944160070792884735), [AGTP 2026-09 보도](https://x.com/AGTPinsights/status/2103902996119814187)
- [AISafetyMemes](https://x.com/AISafetyMemes/status/2016160041108177266), [God's Eye View](https://github.com/bilawalsidhu/gods-eye-view)

**한국·경쟁 계정**
- [hunkims](https://x.com/hunkims/status/2079949203615453414), [x.com/upstageai](https://x.com/upstageai), [LG_AI_Research K-EXAONE](https://x.com/LG_AI_Research/status/2010723674190688676/photo/1), [x.com/NAVER__Cloud](https://x.com/NAVER__Cloud)
- [kchonyc](https://x.com/kchonyc/status/2014189177806401908), [kchonyc Solar Open](https://x.com/kchonyc/status/2008191520881639504)
- [GeekNewsHada](https://x.com/GeekNewsHada), [GeekNewsBot](https://x.com/GeekNewsBot?lang=ko), [AITimes_News](https://x.com/AITimes_News), [yozm_it](https://twitter.com/yozm_it)
- [CHOI Threads](https://www.threads.com/@choi.openai?hl=ko), [arrakis_ai](https://x.com/arrakis_ai/status/2079503929902317796), [ai.trend.kr Threads](https://www.threads.com/@ai.trend.kr?hl=ko), [ai.trend.kr 인스타](https://www.instagram.com/ai.trend.kr/)

**추가 소스**
- [a16z Big Ideas 2026 Part 2](https://x.com/a16z/status/1998788800970109250), [a16z Big Ideas Part 1](https://a16z.com/newsletter/big-ideas-2026-part-1/)
- [x.com/Techmeme](https://x.com/Techmeme)
- [simonw 2026-09](https://x.com/simonw/status/2102175146740232238), [simonw 2026-08](https://x.com/simonw/status/2083343395704160359)
- [WesRoth 개명 보도](https://x.com/WesRoth/status/2074554037878304808), [WesRoth 2026-09](https://x.com/WesRoth/status/2095256468362809619)

**제거·보류 근거**
- [Sora 종료 공지](https://x.com/soraofficialapp/status/2036546752535470382?lang=en), [TechCrunch Sora 종료](https://techcrunch.com/2026/03/24/openais-sora-was-the-creepiest-app-on-your-phone-now-its-shutting-down/)
- [Jimmy Apples](https://x.com/apples_jimmy), [AILeaksAndNews](https://x.com/AILeaksAndNews)
- [heyBarsee](https://x.com/heyBarsee), [dreamingtulpa](https://x.com/dreamingtulpa/status/2081008781870198975), [ai_for_success](https://x.com/ai_for_success/status/2058998697711874394)

**참고 목록**
- [pasqualepillitteri.it '36 X AI Accounts to Follow in 2026'](https://pasqualepillitteri.it/en/news/3633/ai-x-twitter-accounts-to-follow-2026) (2026-05-28 검증)
- [Axios 'Who to follow on X to make sense of AI'](https://www.axios.com/2026/09/14/ai-x-twitter-who-to-follow) (2026-09-14)
- [ReDeck 'X에서 팔로우해야 할 최고의 AI 뉴스 계정'](https://getredeck.com/ko/best/ai-news-accounts-on-x/)
- [X 리스트 가이드(Tweet Archivist)](https://www.tweetarchivist.com/twitter-lists-complete-guide)

**로컬 교차 자료**: `/home/user/insta/research/sources/source-tracing.md`(BZCF의 a16z 인용 확인), `/home/user/insta/research/accounts/ai_freaks_kr.md`(AI Freaks 협업사, 경쟁 벤치마크 언급)
