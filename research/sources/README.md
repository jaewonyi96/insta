# 뉴스 소스 맵 & 소싱 루틴

- 작성일: 2026-09-30 (편집장 정리본)
- 목적: @ai_freaks.kr(AI 뉴스·재미), @romaan.mag(AI 해설), @bizucafe(비즈니스 기사 + 코멘트), @ekke.now(돈·경제·라이프스타일) 같은 한국형 매거진 큐레이션 인스타 계정을 운영할 때 **매일 무엇을 보고, 어떻게 한국어 게시물로 바꾸는지** 한 장에 정리합니다.
- 근거: 같은 폴더의 검증 파일 5개(`x_ai.md`, `source-tracing.md`, `communities.md`, `newsletters_media.md`, `econ_lifestyle.md`)와 `../best-practices.md`(인스타 정책·저작권)
- **검증 한계**
  - 초판을 쓸 때는 새 웹 검색이 0회였습니다. 1회 시도했지만 워크플로 공유 한도(200회)가 소진돼 거부됐습니다. 그래서 소스의 존재·활동 여부는 위 파일들이 검색으로 확인한 결과를 따랐습니다.
  - **2026-09-30에 재검증을 한 번 더 돌렸습니다.** 세 갈래로 나눠 WebSearch를 썼고(README 사실 점검 59회·46개 항목, `communities.md` 54회·45개 항목, `econ_lifestyle.md` 40회·34개 항목), 검색 스니펫만 보고 페이지를 직접 열지는 않았습니다. 이 README에 반영한 것:
    - **휴면 의심 해제**: Import AI(474호, 2026-09-28), AINews(2026-09-09호), Latent Space, @_akhaliq, @MistralAI, 튜링포스트 코리아, 더밀크, 롱블랙, @rowancheung(2026-04)
    - **주소·이름 수정**: Arena 변경 로그 주소, X @lmarena_ai → @arena, 네이버 섹션별 '많이 본 뉴스' 폐지(→ 경제 섹션 + 언론사별 랭킹), 보조금24 → 혜택알리미는 단순 개명이 아닌 개편, 네이버 증권 → 네이버페이 증권, GeekNews RSS 주소 추가
    - **사실 수정**: Cursor 인수는 2026-06-16 발표·2026-08-14 완료, 디스콰이엇은 2025-10 인수 보도와 2025-12 폐업 표기
    - **[미검증] 해제**: hnrss 파라미터, Reddit `.rss`의 2026년 작동, Techmeme·Product Hunt 피드, r/MachineLearning, 아카라이브 채널 5개, 아프니까 사장이다·리멤버 주소, @business·@FT 등
    - **추가**: 디시 AI 활용 갤러리(`communities.md`에서 복원), Reddit 구독자 수 출처 GummySearch의 종료 예정 경고
    - 제거된 소스는 없습니다. 재검증에서도 확인하지 못한 것(@AIatMeta·@metaai 중 현재 계정, @runwayml·@suno·@TheRundownAI의 X 게시일, AI Explained, 커리어리 활동량, 세븐일레븐 인스타, WSJ·Reuters 등 매체 X 핸들, Artificial Analysis·HF 트렌딩 Spaces·Futurepedia)은 `[미검증]`으로 남겼습니다.
  - 파일에 없던 셋업 팁(구글 알리미, 네이버 키워드 알림, 자동화 도구의 모듈 이름 등)은 **미검증**으로 표기했습니다. 쓰기 전에 직접 확인하세요.
- 표기: `[확인 2026-MM]` 그 달 활동 확인 · `[이전 조사]` 같은 세션 다른 파일에 근거 · `[미검증]` 이번 조사에서 확인 못 함 · `[휴면 의심]` 최근 활동이 오래됨 · `[개명]` 이름·주소 변경 · `[개편]` 서비스 구조 변경 · `[종료 의심]` 폐업·종료 정황이 있음

---

## 1. 핵심 요약

1. **4개 계정의 원본은 대부분 1차 자료입니다.**
   - BZCF는 해외 1차 발표물(창업자 서한, CEO 에세이, 공동 보도자료, a16z 보고서)과 Bloomberg·FT·TechCrunch·CNBC를 씁니다.
   - 에크케는 DART 감사보고서·잠정실적과 모회사(SBS) 방송 현장을 씁니다.
   - 뉴스레터, 애그리게이터, 커뮤니티는 **소재를 찾는 레이더**로만 쓰고, 출처로는 1차 자료를 적습니다.
2. **매일 볼 곳은 15개(Tier 1)로 줄였습니다.** 4개 검증 파일에 든 항목은 225개(파일 간 중복 포함, `communities.md` 재검증으로 1행 복원)입니다. 니치별로 T1 2~4개를 두고, 나머지는 주 2~3회(T2) 또는 주간·필요 시(T3)로 돌립니다(§3).
3. **처음 한 번만 셋업하면 됩니다.**
   - X 비공개 리스트 9개와 알림 6개
   - RSS 리더 폴더 9개
   - 뉴스레터 전용 Gmail과 라벨 4개
   - 커뮤니티 북마크 폴더와 로그인 브라우저 프로필 (§4)
4. **하루 55분 루틴을 권합니다. 최소판은 30분입니다(§5).**
   - 미국 서부 오전 발표는 한국 새벽 2~3시에 도착합니다. 그래서 **아침 20분이 속보를 잡는 시간**입니다.
   - 밤 15분에는 미국 일간 뉴스레터와 Techmeme을 보고 다음 날 소재를 정합니다.
5. **소재는 5개 기준으로 10점 만점 채점해 고릅니다.** 기준은 한국 관련성, 신선도, 시각화, 저장·공유, 검증 가능성입니다. 7점 이상이면 제작합니다.
   - 팩트체크는 **1차 원문 확인 + 독립 소스 2개 + 루머·유출 라벨**이 기본입니다(§6).
6. **캡처와 재업로드는 하지 않습니다.**
   - 인스타는 2026-04-30부터 남의 게시물을 주로 올리는 계정을 사진·캐러셀 추천에서도 뺍니다. 출처를 적어도 스크린샷은 오리지널이 아닙니다.
   - 방식은 **사실 추출 → 내 문장 → 내 해설 → 직접 디자인**입니다. 크리에이터 작품은 허락을 받고 태그합니다(§7).
7. **같은 소재를 여러 계정이 동시에 다룹니다.** 예를 들어 메타코미디 실적은 두 계정이 하루 차이로 올렸습니다.
   - 차별화 수단: **한국 각도**, **직접 써 보기**, **원자료를 직접 가공한 데이터 카드**, **자체 인터뷰**
8. **지금 반영할 변경과 시즌 소재**
   - 개명·폐쇄: xAI→SpaceXAI, LMArena→Arena(X @lmarena_ai→@arena), 통계청→국가데이터처, 기획재정부 분리, Papers with Code 종료, Sora 종료, 네이버 섹션별 랭킹 폐지(2020-11) (§3-7)
   - 시즌 소재: OpenAI DevDay(2026-09-29), 『트렌드 코리아 2027』 출간(2026-09-30, 오늘)

---

## 2. 4개 계정은 어디서 소재를 가져오나

상세 근거는 `source-tracing.md`에 있습니다. 인스타 게시물은 검색 색인이 거의 없어서, 같은 운영자의 Threads·텔레그램·블로그로 추적했습니다.

### 2-1. 추적 요약

| 계정 | 규모 (기준) | 주 소스 유형 | 대표 추적 사례 (원본 → 게시, 시차) | 가공 방식 | 추적 수준 |
|---|---|---|---|---|---|
| **BZCF 비즈까페** (@bizucafe) | IG 약 8만(사용자 스냅샷), 약 7만(검색 스니펫) | ① 해외 1차 발표물(창업자 서한·CEO 에세이·공동 보도자료·주주서한·a16z 보고서) ② 해외 경제지 단독·속보(Bloomberg, FT, TechCrunch, CNBC) ③ 영어 인터뷰·연설 영상 ④ 자체 인터뷰 | Bloomberg Lovable 단독(2025-07-17) → 07-18, 약 1일 · OpenAI×AMD 공동 보도자료(2025-10-06) → 10-07, 1일 미만 · a16z Big Ideas 2026 → 12-20, 약 10일(전문은 네이버 블로그) · 아모데이 에세이(2026-09-12) → bzcf.io 전문 번역 09-13 | 발췌 번역, 번호 매긴 3~5개 교훈, 1인칭 코멘트. 전문은 블로그로 보냄 | 14건, 대부분 신뢰도 높음 |
| **에크케** (@ekke.now) | IG 40.4만(사용자 스냅샷), 39.1만(검색 스니펫). SBS 계열 스튜디오161 제작 | ① DART 감사보고서·잠정실적과 그 보도("OOO는 이렇게 벌고 씁니다") ② SBS 방송·행사 현장과 K팝·소비 트렌드 ③ 자체 인터뷰 ④ 해외 이색 경제 기사를 시즌에 맞춰 재가공 ⑤ 브랜디드 | 한미반도체 2025 실적 공시 → 2026-03-27, 약 7주 · 메타코미디 감사보고서 보도(04-03) → 05-20. **하루 전 다른 계정이 같은 소재** · 2025 SBS 가요대전 → 당일 · 산타 순자산(TheStreet 2023-12) → 2024-12-25 | 공시 수치 카드에 밈 소제목과 원화 환산. 화제성 타이밍(야구 시즌, 연말)에 맞춰 게시 | 9건, 중간~높음 |
| **AI Freaks** (@ai_freaks.kr) | 6.5만+, 월 조회 약 1,000만(채용공고) | (운영 구조로 추론) 글로벌 AI 기업의 출시 발표와 협찬 브리프(Liner, Kimi, Hailuo, Higgsfield 등 20곳 이상과 협업), 바이럴 AI 영상, 툴 직접 테스트 | 개별 게시물이 색인되지 않음. 'AI 호러 계정 모음'(2026-07)은 **계정 귀속 미확인**. 같은 시기 에펨코리아·뉴스1에 같은 소재가 있었음 | 컴필레이션, 툴 소개, 현상 해설(추정) | 낮음 |
| **로만** (@romaan.mag) | 팔로워 6,089, 게시물 25개(사용자 스냅샷) | **추적 불가.** 프로필과 게시물 모두 검색 색인에 없음 | - | - | 없음. 사용자가 앱에서 직접 확인해야 함 |

### 2-2. 패턴

1. **원본은 1차 자료이고, 요약본은 아닙니다.** BZCF의 원본은 발표문, 서한, 보도자료, 단독 기사입니다. 에크케의 원본은 공시 원문과 현장입니다. 추적 사례 중 뉴스레터 요약을 옮긴 것은 없었습니다.
2. **두 가지 속도로 운영합니다.** 속보형은 0~2일 안에 올리고(BZCF의 OpenAI×AMD, 스타인버거 OpenAI 합류), 해설·에버그린형은 1주에서 수년 뒤에 올립니다(a16z 보고서, 베이조스 주주서한).
3. **타이밍은 화제성으로 정합니다.** 에크케는 공시 뒤 수주~2개월을 기다려 야구 시즌, 연말, 시상식 같은 대중 관심 시점에 맞춥니다.
4. **같은 소재를 동시에 다룹니다.**
   - 네이트 뉴스 기획(2026-09-05)은 인스타 매거진들이 같은 이슈를 동시에 다뤄 차별성이 흐려진다고 지적했습니다.
   - 차별화는 두 가지입니다. (a) 전문 번역이나 원문을 블로그로 연결하는 BZCF 방식, (b) 자체 인터뷰와 현장
5. **경쟁 큐레이터의 피드는 벤치마크로만 봅니다.** BZCF 텔레그램(`t.me/s/bzcftel`)은 로그인 없이 볼 수 있는 일일 픽 로그입니다. 무엇을 고르는지는 참고하되, 번역문과 코멘트는 가져오지 않고 같은 원문으로 거슬러 올라가 다른 관점으로 씁니다.

### 2-3. 출처 표기 관행

| 계정 | 캡션의 출처 | 링크 | 인물·크리에이터 태그 | 광고 표기 |
|---|---|---|---|---|
| BZCF | 매체명("FT 기사 내용 중 일부")과 원저자("그의 서한")를 자주 적음 | 원 기사 URL은 대체로 없음. 전문 번역은 **자사 블로그 링크**로 | 인터뷰이 실명 소개 | 브랜드 글은 본문에 경위를 적음("내돈내산", 협업 경품 안내) |
| 에크케 | **기준 연도와 법인명**("*2025년 연결 기준", "법인명: 메타코미디") | 없음 | 인터뷰 출연자 계정 태그(@zzan.boo) | **"#광고"를 캡션 맨 앞에** |
| AI Freaks | 게시물 단위로 확인 못 함 | 바이오에 제휴 할인 링크(Napkin AI) | 불명 | 협업사 20곳 이상. 게시물별 표기는 미확인 |
| 로만 | 데이터 없음 | - | - | - |

- **우리 기준(권장):** 최소 "매체명 또는 원저자 + 날짜"를 적습니다. 원문 링크는 스토리 링크, 바이오 링크 페이지, 블로그로 연결합니다. 광고는 "#광고"를 이미지 안과 캡션 첫 줄에 둡니다(§7).
- 참고: 캐러셀 마지막 장 이미지 속 출처는 검색으로 볼 수 없었습니다. 그래서 위 관행은 **실제보다 과소평가됐을 수 있습니다.**

---

## 3. 니치별 Tier 1/2/3 소스 표

- **Tier 1**: 매일 확인합니다. 니치별 최대 5개, 전체 15개입니다(아래 집계).
- **Tier 2**: 주 2~3회 봅니다. 알림이 켜진 계정은 푸시로 들어오므로 따로 확인하지 않아도 됩니다.
- **Tier 3**: 주 1회 이하, 또는 그 주제를 쓸 때만 봅니다. 주간 루틴(§5-3)에서 몰아 봅니다.
- 한 소스는 가장 많이 쓰는 니치 한 곳에만 배치했습니다. 세부 설명과 근거 URL은 원 파일 표를 보세요.

**Tier 1 집계 (15개)**

| 니치 | T1 개수 | T1 소스 |
|---|---|---|
| AI 뉴스 | 2 | 빅랩 공식 발표 묶음, The Rundown AI |
| AI 괴짜·바이럴 | 2 | X `05_바이럴·크리에이티브`, r/ChatGPT + r/aivideo |
| AI 이해·해설 | 2 | Hacker News(hnrss), Hugging Face Papers Daily |
| 비즈니스 | 2 | Techmeme, X `07_비즈니스` + `09_글로벌경제` |
| 경제·돈·라이프스타일 | 4 | 연합뉴스 경제 RSS, 네이버 경제 섹션 + 언론사별 랭킹, 정책브리핑 보도자료 RSS, 뽐뿌 재테크포럼 + 알구몬 |
| 한국 특화 | 3 | GeekNews, 디시 특이점이 온다 갤러리, 에펨코리아 포텐 + 더쿠 HOT |

> **계정 컨셉에 따라 바꾸세요.** 위 15개는 네 니치를 모두 다루는 종합형 기준입니다.
> - **AI 전문 계정**이면 경제 T1 4개를 T2로 내리고, 대신 AI타임스, r/LocalLLaMA, The Decoder, Axios AI+를 T1로 올립니다.
> - **경제 전문 계정**이면 AI 괴짜·해설 T1을 내리고, 대신 DART(시즌), 정부24+ 혜택알리미, 네이버 데이터랩을 올립니다.

### 3-1. AI 뉴스 (ai_freaks형 속보)

| 티어 | 소스 | 보는 곳 (URL·핸들·RSS) | 쓰는 이유 | 상태·주의 |
|---|---|---|---|---|
| **T1** | **빅랩 공식 발표 묶음** | X 리스트 `01_공식발표` + 알림 6개(§4-1) · RSS `https://openai.com/news/rss.xml` · anthropic.com/news · blog.google/technology/ai/ · deepmind.google · ChatGPT 릴리스 노트(help.openai.com) | 모든 AI 뉴스의 1차 원문입니다. 요약본에서 본 소재도 반드시 여기서 확인합니다 | OpenAI RSS [확인](옛 blog/rss.xml은 이 주소로 리디렉트). Anthropic 공식 RSS는 확인 못 함 → X 알림으로 대신. **[개명] @xai → @SpaceXAI(2026-07-06, X 핸들 포함) [확인 2026-07].** @AIatMeta와 @metaai 중 현재 계정은 [미검증](검색에서 둘 다 'AI at Meta'로 나옴) → 직접 확인 |
| **T1** | **The Rundown AI** | therundown.ai 이메일 → 라벨 `AI-NL` | 200만 명 넘게 받는 AI 일간 요약입니다. **빠짐없음 체크리스트**로 씁니다. 한국에는 저녁~밤에 도착합니다 | [확인 2026](therundown.ai에 200만+ 표기 재확인). 요약본이라 원문으로 재확인. 창업자 **@rowancheung [확인 2026-04]**: 2026-04-27 X 게시물에서 '활성 독자 300만에 가까워진다'고 씀(네트워크 전체 기준일 수 있음, [근거](https://x.com/rowancheung/status/2048767013472833869)). 뉴스레터가 주 채널 |
| T2 | X `03_리크·벤치마크` | @testingcatalog(알림), @btibor91, @scaling01, @ArtificialAnlys, @chetaslua, @arena(구 @lmarena_ai) | 출시 전 리크, 신모델 성적표를 가장 빨리 봅니다 | 리크에는 **[루머]** 라벨. 실례: 'o'로 예고된 상시 에이전트가 실제로는 'dots'로 발표됨. @chetaslua는 단독 게시 금지. **[개명] @lmarena_ai → @arena [확인 2026-06]**(2026-01-28 'LMArena is now Arena' 게시, 2026-06-10 게시물, [근거](https://x.com/arena/status/2016577708831232140)) |
| T2 | X `06_중국·오픈모델` | @deepseek_ai(알림), @Alibaba_Qwen, @Kimi_Moonshot, @Zai_org, @MiniMax_AI, @huggingface, @op7418 | 중국 모델은 예고 없이 나옵니다 | 공식 계정은 @deepseek_ai 하나뿐(사칭 주의). 중국 3사는 인증 배지를 직접 확인 |
| T2 | r/LocalLLaMA (+ r/OpenAI, r/singularity) | `https://www.reddit.com/r/LocalLLaMA/top/.rss?t=day` | 오픈 모델 출시·유출에 대한 1차 반응, 직접 돌려 본 후기 | 약 80만~83만(3자 트래커, 2026-08~09) [확인 2026-09]. Reddit `.rss`는 2026년에도 작동(3자 가이드 기준, 공식 문서는 아님, [근거](https://www.wprssaggregator.com/reddit-rss-feed/)). 유출은 [루머] 표기 |
| T2 | The Decoder | the-decoder.com (리더에 사이트 주소 입력) | 모델 출시, 벤치마크, AI 지출 추세 | [확인 2026-09] |
| T2 | Axios AI+ | axios.com/signup/ai-plus | 평일 일간. Smart Brevity 구조가 카드 한 장의 문법과 거의 같음 | [확인 2026]. 구조만 참고하고 문장은 복제하지 않음 |
| T2 | TLDR AI | tldr.tech/ai | 평일 링크 모음으로 오픈소스·논문·툴을 빠르게 훑음 | [확인 2026], 약 110만 구독. 스폰서 링크가 섞임 |
| T3 | 보조 뉴스레터·매체 | The Neuron(theneuron.ai), Ben's Bites(`bensbites.com/feed`, 주 2회 화·목), AINews(news.smol.ai), Last Week in AI(lastweekin.ai, 주간 누락 점검), The Verge AI, CNBC Tech, @WesRoth(2차 속보), @MistralAI | 주간 누락 점검, 톤 참고 | The Neuron은 **[개명]** 주소가 theneuron.ai이고 2025-01 TechnologyAdvice에 인수됨(옛 주소 theneurondaily.com). **AINews [확인 2026-09]**(2026-09-09호. 지금은 Latent Space의 한 섹션으로 일간 발행, [근거](https://news.smol.ai/issues/26-09-09-not-much/)). **@MistralAI [확인 2026-09]**(2026-09-04 X 게시물, [근거](https://x.com/MistralAI/status/2095951508978209153)) |

### 3-2. AI 괴짜·바이럴 (ai_freaks형 재미)

| 티어 | 소스 | 보는 곳 | 쓰는 이유 | 상태·주의 |
|---|---|---|---|---|
| **T1** | **X `05_바이럴·크리에이티브`** | 핵심 @kimmonismus(Chubby), @minchoi. 리스트 전체는 §4-1 | 신기한 AI 영상과 뉴스 분석(Chubby), 신모델이 나오면 '10 wild examples' 모음(Min Choi) | Chubby [확인 2026-09-29], Min Choi [확인 2026-04]. **예시마다 원작자가 따로 있으니** 개별 크레딧과 허락 필요 |
| **T1** | **r/ChatGPT + r/aivideo (+ r/aiArt)** | `https://www.reddit.com/r/ChatGPT/top/.rss?t=day` · `.../r/aivideo/top/.rss?t=day` | 웃긴 결과물, 프롬프트 유행, AI 영상 쇼케이스. '이게 AI라고?' 릴스의 본진 | 조작된 '챗GPT 답변' 캡처가 흔함. 영상 재업로드 금지 → 원작자의 인스타·유튜브를 찾아 허락과 태그 |
| T2 | @venturetwins (Justine Moore, a16z) | x.com/venturetwins | 화제가 된 AI 영상(일본 AI 영상, AI 결혼식)에 투자자 시각 코멘트 | [확인 2026-07]. 영상 원작자를 추적해 크레딧 |
| T2 | 크리에이티브 툴 공식 | @midjourney(+updates.midjourney.com), @Kling_ai, @ElevenLabs, @pika_labs, @Hailuo_AI, @LumaLabsAI, @bfl_ml | '새로 나온 이상한 기능 따라 해보기' | Midjourney [확인 2026-07], Kling [확인 2026-09-27], ElevenLabs [확인 2026-09-28]. **@runwayml(최근 확인 2025-12), @suno(2025-09)의 2026년 X 게시물은 [미검증]**. 회사는 활동 중(Runway 2026-07-23 모델 라우터 출시, Suno 2026-03-26 v5.5 출시) → 공식 블로그와 suno.com/release-notes 우선 |
| T2 | r/StableDiffusion | `.../r/StableDiffusion/top/.rss?t=day` | 오픈 이미지·영상 모델과 ComfyUI 기법이 가장 먼저 공유됨 | 약 100만(2026-08-31 998,663명, 하루 글 약 64개, prowlo) [확인 2026-09]. NSFW와 실존 인물 LoRA는 제외 |
| T2 | 404 Media | 404media.co/tag/ai-slop/ | 근거가 탄탄한 '이상한 AI' 탐사 보도 | [확인 2026]. 일부 회원 전용 |
| T2 | Product Hunt + HF 트렌딩 Spaces | producthunt.com (Atom `producthunt.com/feed`, 3자 가이드로 확인. 실시간 순위라 다음 날 아침 전날 일간 리더보드를 봄) · huggingface.co/spaces | '써봤다' 툴 카드. 직접 테스트는 오리지널 콘텐츠로 인정받는 데 유리함 | 업보트는 홍보성일 수 있음. 모델 라이선스 확인. 카테고리 피드 슬러그는 [미검증]. HF 트렌딩 Spaces는 재검증에서 검색하지 않음 [미검증](존재는 확실) |
| T3 | 저신호·보조 | @EHuanglu, @AngryTomtweets, @AISafetyMemes, @bilawalsidhu(인스타·Threads @bilawal.ai), Two Minute Papers(유튜브), AI 툴 디렉터리(futuretools.io, theresanaiforthat.com, futurepedia.io), @dreamingtulpa(보류 후보) | 소재가 부족한 날 | @EHuanglu는 툴 홍보가 잦음(Higgsfield X 계정은 2026-02 정지). @AngryTomtweets 본인 게시물은 2025-07까지만 확인. @AISafetyMemes는 공포 조장 주의. @bilawalsidhu의 2026년 X 활동은 [미검증]. 툴 디렉터리는 Future Tools 뉴스 [확인 2026-09], TAAFT·Future Tools의 등록 수는 자체 주장, Futurepedia는 [미검증] |

### 3-3. AI 이해·해설 (로만형)

| 티어 | 소스 | 보는 곳 | 쓰는 이유 | 상태·주의 |
|---|---|---|---|---|
| **T1** | **Hacker News** | `https://hnrss.org/newest?points=100` · `https://hnrss.org/frontpage` · 키워드 `https://hnrss.org/newest?q=OpenAI` | 테크·스타트업 사건에 업계인 댓글이 붙음 → '과장 걷어내기' 해설 재료 | hnrss는 제3자 서비스. 파라미터 `q=`, `points=`, `comments=`, `count=`(최대 100)와 `&` 조합은 hnrss.org 문서로 확인 [확인 2026-09]([근거](https://hnrss.org/)). 댓글은 'Hacker News 댓글'로 한정해 인용 |
| **T1** | **Hugging Face Papers Daily** | huggingface.co/papers (Trending은 /papers/trending) · X @HuggingPapers | 연구 소재. 논문에 연결된 Spaces 데모를 직접 돌려 해설 근거로 씀 | **Papers with Code는 2025-07-24 종료**(도메인은 HF Trending Papers로 리디렉트) [확인 2026-09]. 프리프린트는 '입증됐다' 대신 '논문에 따르면' |
| T2 | X `02_핵심인물` + `04_큐레이터·해설` | @emollick, @karpathy, @simonw, @vitrupo, @rohanpaul_ai, @OfficialLoganK, @demishassabis 등(§4-1) | '왜 중요한가' 관점. 인용 카드 소재 | **직함 변경:** Hassabis는 2026-08-05 DeepMind 의장 겸 Alphabet 수석과학자, Karpathy는 2026-05-19 Anthropic 사전학습 팀 합류. **@_akhaliq [확인 2026-09]**(2026-05·06·09 X 게시물, [근거](https://x.com/_akhaliq/status/2097726716861186348)). 논문 피드는 @HuggingPapers와 같이 봄 |
| T2 | One Useful Thing (Ethan Mollick) | `oneusefulthing.org/feed` | 비개발자 눈높이 해설. 한국어 카드로 옮기기 가장 쉬움 | [확인 2026-08]. 에세이 전문 번역은 허락 필요 |
| T2 | Simon Willison's Weblog | simonwillison.net | 신모델을 직접 써 본 기록, 가격 대비 성능 | [확인 2026-09]. 개발자 관점이라 풀어 쓸 것 |
| T2 | Interconnects (Nathan Lambert) | `interconnects.ai/feed` | 오픈 모델과 중국 모델이 왜 중요한가 | [확인 2026]. **필자가 2026-06 Ai2를 떠남** → 'Ai2 연구자'로 소개하면 틀림 |
| T2 | 순위판: Arena, Artificial Analysis, OpenRouter | arena.ai/blog/leaderboard-changelog · artificialanalysis.ai · openrouter.ai/rankings | '벤치마크 1위와 실사용 1위는 다르다' 해설, '이번 주 AI 순위' 카드 | **[개명] LMArena → Arena(2026-01-28, 옛 lmarena.ai는 arena.ai로 리디렉트).** 변경 로그 주소는 /company/가 아니라 /blog/ 아래([근거](https://arena.ai/blog/leaderboard-changelog)), 2026-07 모델 추가까지 확인 [확인 2026-07]. 지수 버전·조회일 표기. OpenRouter는 토큰 기준 주간 순위와 텍스트 요청 점유율이 따로 있으니 어느 지표·어느 주인지 적음([근거](https://openrouter.ai/rankings)). Artificial Analysis는 재검증에서 검색하지 않음 [미검증](존재는 확실) |
| T2 | MIT Technology Review (The Algorithm, 월요일) | technologyreview.com | 깊이 있는 해설 기사 | [확인 2026-09]. 일부 유료 |
| T2 | r/MachineLearning | `.../r/MachineLearning/top/.rss?t=week` | 과장된 논문·벤치마크에 대한 연구자 반론 | 310만(GummySearch, 2026-08-27 갱신) [확인 2026-08] |
| T3 | 장문·연간 | Import AI(jack-clark.net), The Batch(deeplearning.ai/the-batch), Latent Space(`latent.space/feed`), Dwarkesh Podcast(`dwarkesh.com/feed`), AI Explained(youtube.com/@aiexplained-official), Epoch AI(epoch.ai/data-insights), Stanford AI Index 2026 | 인터뷰 발언 3가지, 연례 '숫자로 보는 AI' | **Import AI [확인 2026-09]**(473호 2026-09-21, 474호 2026-09-28, [근거](https://jack-clark.net/2026/09/28/import-ai-474-platonic-mindspace-tpus-in-space-zhipu-starts-an-outer-rsi-loop/)). The Batch [확인 2026-09], Dwarkesh [확인 2026-09]. **Latent Space [확인 2026]**(2026년 글 latent.space/p/2026, AINews를 섹션으로 흡수, [근거](https://www.latent.space/p/2026)). AI Explained는 2026년 개별 영상 [미검증] |

### 3-4. 비즈니스 (bizucafe형)

| 티어 | 소스 | 보는 곳 | 쓰는 이유 | 상태·주의 |
|---|---|---|---|---|
| **T1** | **Techmeme** | techmeme.com · 시간순 techmeme.com/river · RSS `techmeme.com/feed.xml`(피드 디렉터리 등록으로 확인, 검색 요약 기준) | BZCF가 쓰는 원천(Bloomberg, TechCrunch, CNBC, FT)이 대부분 여기에 먼저 걸림. 클러스터에 붙은 기사 수로 뉴스 크기를 판단 | [이전 조사]. X @Techmeme 게시물에는 링크가 없음 → 원 기사까지 확인 |
| **T1** | **X `07_비즈니스` + `09_글로벌경제`** | @a16z, @nvidianewsroom, @cursor_ai + @business, @FT, @WSJ, @Reuters 등(§4-1) | 창업자 서한, CEO 발표, VC 보고서 같은 BZCF 원본 유형 ①과 해외 경제지 속보 | `09` 리스트 매체 핸들 중 @business·@FT는 [확인 2026-09](`econ_lifestyle.md` 재검증), 나머지(@WSJ, @Reuters 등)는 [미검증](존재는 확실). **Cursor는 2026-06-16 SpaceX 인수 발표, 2026-08-14 인수 완료**([근거](https://techcrunch.com/2026/08/15/spacex-officially-closes-its-cursor-acquisition/)) |
| T2 | TechCrunch | RSS `techcrunch.com/feed/`[미검증] | 투자·출시 속보. BZCF가 실제로 인용한 원천(Cursor 밸류에이션, 스타인버거) | 투자 수치는 회사 공식 발표와 대조 |
| T2 | Bloomberg Technology, The Information, FT (무료 헤드라인) | 무료 헤드라인 뉴스레터 → 라벨 `BIZ-NL` | 단독 포착. BZCF의 Lovable(Bloomberg)과 K자형 경제(FT) 사례 | **유료 기사는 매체명 + 날짜 + 요지만.** 전문 번역·캡처 금지 |
| T2 | a16z | a16z.com/newsletter | 'VC가 투자하겠다는 분야 N개'. BZCF가 Big Ideas 2026을 약 10일 뒤 번역 | 포트폴리오 홍보 성격을 감안 |
| T2 | Stratechery, Platformer | stratechery.com · platformer.news | 해석 관점. Platformer는 인스타·메타 정책 레이더도 겸함 | [미검증]. 유료 부분은 요지만 |
| T2 | GitHub Trending | 비공식 RSS mshibanami.github.io/GitHubTrendingRSS/ | 바이럴 오픈소스가 비즈니스 뉴스로 번지는 초기 신호(OpenClaw → 개발자의 OpenAI 합류, 2026-02) | 제3자 RSS라 끊길 수 있음(일간·주간·월간·언어별 피드 확인, 2026년 갱신일은 [미검증]). 스타 조작 레포 주의 |
| T2 | 블라인드 토픽 베스트 | teamblind.com/kr/topics/토픽-베스트 (로그인) | 연봉, 성과급, 구조조정, 사내 AI 도입 분위기가 기사보다 먼저 드러남 | [확인 2026-06]. **명예훼손 위험이 큼.** 캡처 금지, 기사나 공식 입장으로 교차 확인 |
| T2 | 국내 스타트업·창업 영상 | 아웃스탠딩(outstanding.kr) · 플래텀(platum.kr) · EO Korea(유튜브 채널 ID `UCQ2DWm5Md16Dc3xRwwhVE7Q`) · youtube.com/@ycombinator | 한국 회사 이야기, 창업자 발언 인용 카드. BZCF 유튜브의 원천 유형(해외 인터뷰 영상) | 아웃스탠딩 [확인 2026]. 영상 번역·재편집 게시는 허락 필요 |
| T3 | 해외 보조 | CNBC, WSJ, Reuters, The Economist, Business Insider, Morning Brew, CB Insights, Visual Capitalist, Lenny's Newsletter, Sequoia(Training Data) | '해외에선 이렇다' 비교 각도 | Morning Brew·Visual Capitalist·CB Insights는 [확인 2026](`econ_lifestyle.md` 재검증). WSJ·Reuters·The Economist·Business Insider 등 나머지는 [미검증](존재는 확실). 차트 이미지 재사용 금지, 원 데이터 출처를 인용(Visual Capitalist는 별도 라이선스 사이트가 있음) |
| T3 | 국내 보조 | 더밀크(themiilk.com), 티타임즈(유튜브 @TTimesTV), 아이보스(i-boss.co.kr), 리멤버 커뮤니티, 디스콰이엇(disquiet.io), r/Entrepreneur | 해외 비즈니스의 한국어 해설, 마케팅 실무, 인디 창업 | **더밀크 [확인 2026]**(CES 2026 특집, [근거](https://themiilk.com/collections/351)). **디스콰이엇은 [종료 의심]**: THE VC 검색 요약에 2025-10-30 픽셀릭(릴레잇 운영사) 인수 보도와 2025-12 폐업 표기가 있음([근거](https://thevc.kr/disquiet)) → 최근 글 날짜를 확인하기 전에는 아카이브로만 참고. 리멤버는 community.rememberapp.co.kr 주소 확인(2026 활동량은 [미검증]). 아이보스 [확인 2026] |

### 3-5. 경제·돈·라이프스타일 (ekke형)

| 티어 | 소스 | 보는 곳 | 쓰는 이유 | 상태·주의 |
|---|---|---|---|---|
| **T1** | **연합뉴스 경제** | RSS `https://www.yna.co.kr/rss/economy.xml` | 가장 빠르고 건조한 팩트 요약. 모든 게시물의 사실 기준점 | RSS 주소는 제3자 문서·코드(GitHub 스니펫)에서만 확인했고 연합뉴스 공식 RSS 안내 페이지는 [미검증] → 리더에 등록하기 전에 피드가 열리는지 확인. 사진·그래픽은 유료 라이선스라 쓰지 않음 |
| **T1** | **네이버 뉴스 경제 섹션 + 언론사별 랭킹** | news.naver.com/section/101 · 네이버 뉴스 '랭킹' 메뉴(언론사별 많이 본 뉴스. 한경·매경 등 경제지 위주) | 한국 대중이 지금 실제로 읽는 경제 이슈. news.naver.com은 Similarweb 기준 2026-03 국내 뉴스·미디어 사이트 방문 1위 | **전체·섹션별 '많이 본 뉴스'는 2020-11에 폐지**돼 '경제 랭킹' 메뉴는 없음. 언론사별 랭킹만 남음([근거](https://www.newspim.com/news/view/20201023000042)). 포털은 원문이 아님. 언론사 원문과 원자료로 확인 |
| **T1** | **대한민국 정책브리핑 보도자료** | RSS `https://www.korea.kr/rss/pressrelease.xml` (RSS 안내 korea.kr/etc/rss.do) | 전 부처 발표가 한곳에 있음. '이번 달부터 바뀌는 것'은 저장·공유가 많은 포맷 | [확인 2026-09](korea.kr/etc/rss.do에 보도자료 RSS로 나옴). 공공누리 유형(출처표시, 변경금지 등) 확인 |
| **T1** | **뽐뿌 재테크포럼 + 알구몬** | ppomppu.co.kr/zboard/zboard.php?id=money · algumon.com (키워드 알림) | 특판 적금, 카드 혜택, 금리 변경, 앱테크가 금융사 발표 직후 올라옴. 알구몬은 여러 커뮤니티의 핫딜을 한 화면에 모음 | 뽐뿌 재테크포럼(id=money) [확인 2026-09], 알구몬(웹 algumon.com/n/deal, 앱 2026-09-01 업데이트) [확인 2026-09]. 뽐뿌 공식 RSS는 [미검증]. 금융사 공식 공지로 확인하고 게시 시점을 적음. 알구몬은 에펨코리아 핫딜을 수집하지 않는 것으로 알려짐 |
| T2 (**1~4월은 T1**) | DART 전자공시 | dart.fss.or.kr (관심 기업 공시 알림) · opendart.fss.or.kr | 에크케 'OOO는 이렇게 벌고 씁니다'의 **확인된 원천**. 공시 원문이라 저작권 부담이 적음 | [확인 2026-09]. 연결·별도, 기준 연도 명시. 매체마다 증감률이 달라 원문 대조 |
| T2 | 한국은행·ECOS + 국가데이터처·KOSIS | bok.or.kr · ecos.bok.or.kr · **mods.go.kr** · kosis.kr | 금리, 물가, 고용, 가계동향. 공표 일정이 고정돼 캘린더로 미리 계획 가능 | **[개명] 통계청 → 국가데이터처(2025-10-01, 기재부 외청에서 국무총리 소속으로 승격).** 이전 자료는 '통계청 발표'로 표기. 한국은행·ECOS [확인 2026-09](2026-09 「금융안정 상황」 게시), 한은 RSS 제공 여부는 [미검증] |
| T2 | 금융위원회 + 금감원 파인 | fsc.go.kr · fss.or.kr · fine.fss.or.kr | 청년 금융상품, 소비자경보, 이번 달 금리 비교 | [확인 2026]. 2025-09-25 발표된 금융위 해체·금감원 분리 개편안은 철회돼 두 기관 모두 현 체제 유지. 파인은 계좌 통합조회·숨은 금융자산·금융상품 비교 메뉴를 봄. '예정'과 '확정'을 구분. 특정 상품 추천은 광고로 오인될 수 있음 |
| T2 | 정부24+ 혜택알리미 + 온통청년 | plus.gov.kr/portal/benefitV2/ · youthcenter.go.kr · bokjiro.go.kr | '놓치면 손해 혜택 모음'. 2030 타깃에서 저장률이 높은 소재 | **[개편] 단순 개명이 아님.** 보조금24(맞춤형 혜택 조회, gov.kr/portal/rcvfvrSvc/main)는 남아 있고, 2025-12-10부터 정부24+ 혜택알리미가 받을 수 있는 혜택을 먼저 알려 줌(민간 앱으로도 가입 가능, [근거](https://www.mois.go.kr/frt/bbs/type010/commonSelectBoardArticle.do?bbsId=BBSMSTR_000000000008&nttId=115068)). 온통청년은 청년정책 약 3,000개를 모음 [확인 2026-09]. 지역·소득 조건과 마감일 명시 |
| T2 | 경제지 원문 | 한국경제 RSS 목록 `https://www.hankyung.com/feed` · 매일경제(mk.co.kr) · 이데일리 | 재테크, 세금, 소비·유통 원문. 비즈까페형 '기사 + 코멘트'의 한국판 | 한경 프리미엄 등 유료 기사는 요약 공유 주의 |
| T2 | 증권사 리포트 | **markets.hankyung.com/consensus** · 네이버페이 증권 리서치(finance.naver.com/research) | 업계 판도 해설 카드의 근거 | **[개명] 한경 컨센서스 주소가 바뀜**(옛 hkconsensus.hankyung.com도 검색에 남아 있음). **[개명] 네이버 증권 → 네이버페이 증권**(도메인은 그대로, /research 경로는 [미검증], [근거](https://namu.wiki/w/%EB%84%A4%EC%9D%B4%EB%B2%84%ED%8E%98%EC%9D%B4%20%EC%A6%9D%EA%B6%8C)). 차트 캡처와 PDF 재배포 금지, 투자 권유처럼 보이지 않게 |
| T2 | 검색량 검증 도구 | datalab.naver.com · trends.google.com/trending?geo=KR | 커뮤니티에서만 뜨거운지, 대중도 찾는지 판단. 검색량 그래프를 직접 그리면 오리지널 카드가 됨 | 데이터랩·구글 트렌드 모두 [확인 2026-09]. 데이터랩은 조회 기간 최댓값을 100으로 둔 상대지수이고 절대 검색량은 웹·API 어디에도 없음. 기간·기기·연령 조건을 적음 |
| T2 | 딜·부동산·자영업 커뮤니티 | fmkorea.com/hotdeal · clien.net/service/board/jirum · 네이버 카페 부동산스터디(cafe.naver.com/jaegebal) · 아프니까 사장이다(cafe.naver.com/jihosoccer123) | 딜, 대출 규제·청약 체감, 자영업 경기 체감 | 회원 전용 글은 캡처·인용 금지. 클리앙 알뜰구매 [확인 2026-09]. **아프니까 사장이다 주소 [확인 2026-09]**([근거](https://www.make2t.kr/2026/09/apeunikka-sajangida-naver-cafe.html)). 두 카페 모두 회원 수가 출처마다 엇갈림(부동산스터디 약 104만~163만, 아프니까 사장이다 78만~195만+) → 인용하려면 카페 첫 화면에서 확인 |
| T3 | 정부·공공 (시즌·수시) | 재정경제부(mofe.go.kr), 국토교통부, 한국부동산원·청약홈(applyhome.co.kr), 국세청, KDI, 한국소비자원·참가격(price.go.kr), KOTRA 해외시장뉴스 | 세법 개정, 청약 캘린더, 연말정산(1월)·종합소득세(5월), 가격 비교, 'K제품 해외 반응' | **[개명] 기획재정부 → 재정경제부 + 기획예산처(2026-01-02)** [확인 2026-09]. 그린북은 재정경제부 경제정책국이 계속 발간(9월호 2026-09-11). mofe.go.kr 도메인은 `econ_lifestyle.md` 1차 검증 근거. K-패스는 2026년 정액형 '모두의 카드'가 추가됐고, 10월 이후 환급 기준은 국토부 원문으로 확인 [미검증] |
| T3 | 트렌드 리포트 (월 1회) | 대학내일20대연구소(20slab.org), 캐릿(careet.net), 오픈서베이(blog.opensurvey.co.kr/trendreport/), 트렌드모니터, KB금융 경영연구소·하나금융연구소, 썸트렌드(some.co.kr) | '요즘 20대는', '직장인 OO%' 데이터형 카드 | 조사 시기와 표본 명시. 썸트렌드는 2026-03-18 Claude용 MCP 출시(이후 ChatGPT Apps 승인, 2026-07 유료화) [확인 2026-07] |
| T3 | 『트렌드 코리아 2027』 | 도서(2026-09-30 출간 [확인 2026-09]). 전시 10/13~11/8(영풍문고 여의도 IFC몰점), 강연 10/26(CGV 여의도) | **지금 쓸 시즌 소재:** 10월 첫 주 '2027 키워드 10개' | 도서 내용의 과도한 요약·전재 금지 |
| T3 | 유통 현장 | 다이소몰 신상(daisomall.co.kr/ds/prir), 편의점 IG @cu_official·@gs25_official, 올리브영 랭킹(IG @oliveyoung_official) | '이번 주 편의점 신상', '재입고 요청 TOP3' | 제품 사진은 직접 촬영. 올리브영 IG @oliveyoung_official [확인 2026-09](글로벌·매거진 계정과 헷갈리지 말 것). **세븐일레븐 인스타 핸들은 [미검증]**(X @711korea, 페이스북 7elevenkorea만 확인) |
| T3 | 톤·주제 참고 (경쟁) | 어피티 머니레터(uppity.co.kr, IG @uppity.official), 뉴닉(newneek.co), 토스피드(toss.im/tossfeed), 슈카월드(@syukaworld), 삼프로TV(@3protv) | 이번 주 대중이 관심 갖는 돈 주제 가늠 | **경쟁 매체입니다.** 문장·구성 모방 금지. 영상 캡처·요약 재게시 금지 |
| T3 | 생활 커뮤니티 | 월급쟁이부자들(cafe.naver.com/wecando7 · weolbu.com/community), 월재연(cafe.naver.com/onepieceholicplus), 네이트판(pann.nate.com/talk/ranking), MLB파크 불펜, 디시 미국 주식 갤러리(?id=stockus, 보조 ?id=tenbagger), 맘스홀릭, r/personalfinance | 세대·성별별 돈 체감 온도 | 회원 전용 글 인용 금지. 사연 진위 불명. '여론'으로 일반화하지 않음. 월부 회원 35만은 2022년 수치. MLB파크 불펜 URL 형식은 [미검증] |

### 3-6. 한국 특화

| 티어 | 소스 | 보는 곳 | 쓰는 이유 | 상태·주의 |
|---|---|---|---|---|
| **T1** | **GeekNews (긱뉴스)** | news.hada.io · RSS `news.hada.io/rss/news`(설정 안내 hada.io/blog/geeknews-feed-rss) · 월요일 위클리 news.hada.io/weekly(구독 1.8만+) · X @GeekNewsHada | 한국 테크 종사자의 필터를 한 번 거친 '한국에서 반응할 해외 소식' | [확인](위클리 구독 수·X 핸들 재확인). RSS 주소는 재검증에서 추가([근거](https://hada.io/blog/geeknews-feed-rss/)). 요약문은 작성자 저작물 → 복사 금지, 원문으로 다시 씀 |
| **T1** | **디시 특이점이 온다 갤러리** | gall.dcinside.com/mgallery/board/lists/?id=thesingularity ('개념글' 탭) | 해외 AI 발표가 **한국어로 가장 빨리** 번역되고, 한국 헤비유저의 반응 온도를 봄 | [확인 2026-09]. 나무위키에 따르면 2026년 코딩 글을 분리한 뒤 AI 코딩·도구 글은 AI 활용 갤러리로 옮겨 감(단일 출처) → 아래 T2 행과 같이 봄. 닉네임·IP 가림, 번역 이미지 캡처 금지. 과장과 조롱이 많음 |
| **T1** | **에펨코리아 포텐 + 더쿠 HOT** | fmkorea.com/best(최신순) · fmkorea.com/best2(화제순) · theqoo.net/hot | 한국 대중에게 **실제로 먹히는** AI·돈·소비 소재 레이더. 'AI 호러'와 '두쫀쿠'가 여기서 먼저 뜸 | 에펨 포텐 [확인 2026-09](/best·/best2 구분은 페이지 제목으로 확인, [근거](https://www.fmkorea.com/best2)), 더쿠 HOT [확인 2026-07]. 퍼 온 글은 원출처까지 추적. 성별·정치·팬덤 갈등 소재는 피함. 캡처 금지 |
| T2 | AI타임스 | aitimes.com (네이버 뉴스 언론사 구독) | 한국 AI 기업·정책 뉴스가 가장 많음. 해외 뉴스에 한국 맥락을 붙일 때 씀 | **aitimes.kr(인공지능신문)과 다른 매체.** RSS 주소는 미확인 |
| T2 | X `08_한국` | @hunkims, @upstageai, @LG_AI_Research, @kchonyc 등(§4-1) | Solar Pro 4, K-EXAONE처럼 세계 순위와 연결되는 한국 모델 소식 | 자사 홍보 성격. **@NAVER__Cloud는 게시물 미확인** → 네이버 뉴스룸 우선 |
| T2 | 국내 IT 매체 | ZDNet Korea(zdnet.co.kr), 전자신문(etnews.com), 블로터(bloter.net) — 네이버 언론사 구독 | 국내 AI 산업, 반도체, 정부 AI 정책 | 보도자료를 받아 쓴 기사는 구분 |
| T2 | 디시 AI 활용 마이너 갤러리 **[복원]** | gall.dcinside.com/mgallery/board/lists/?id=ai_utilize ('개념글' 탭) | 특갤이 코딩 글을 막은 뒤 옮겨 온 헤비유저의 AI 코딩·도구 실사용 반응. 특갤과 같이 봄 | [확인 2026-09]. 1차 검증에서 '추정 주소'로 뺐으나 실제로 있어 `communities.md`에서 되살림([근거](https://m.dcinside.com/board/ai_utilize)). 활동량 순위는 [미검증]. 닉네임·IP 가림, 탈옥·NSFW 글 제외 |
| T2 | 아카라이브 ai101·alpaca | arca.live/b/ai101 · arca.live/b/alpaca (참고: aiart, characterai, aivideo) | ai101은 언어모델 뉴스·팁, alpaca는 r/LocalLLaMA의 한국판 | 채널 5개(ai101, alpaca, aiart, characterai, aivideo) 주소 모두 확인. aivideo는 구독 1,961명으로 작음. aiart·characterai는 브랜드 안전상 참고만. 2026년 활동량은 [미검증] |
| T2 | 클리앙 새로운소식 | clien.net/service/board/news | IT에 밝은 3040 직장인의 국내외 기사 공유와 실무자 댓글 | **공식 RSS 없음**(이용자가 만든 feedburner 피드는 [미검증], [근거](https://www.clien.net/service/board/lecture/11373731)) → 북마크로 봄. 2026년 글은 [미검증]. 정치 댓글이 많음 |
| T2 | 지피터스 + 조코딩 | gpters.org · youtube.com/@jocoding | 한국인의 AI 실전 활용 사례와 인터뷰 섭외 풀, 한국 대중이 반응하는 AI 뉴스 | 지피터스 [확인 2026-09](AI 스터디 24기 모집, 유튜브 @gpters 있음. '국내 최대'는 자체 주장). 사례 인용은 작성자 허락. 조코딩은 협업 영상이 섞임 |
| T3 | 해설·연구(한국어) | 튜링포스트 코리아(turingpost.co.kr), PyTorchKR 주간 논문(`discuss.pytorch.kr/c/news/14.rss`[미검증]), SPRi AI 브리프(spri.kr/posts?code=AI-Brief, 월간), 바이라인네트워크, 요즘IT, 디지털데일리 | 로만형 한국어 해설의 배경 지식, 정책 통계 | **튜링포스트 코리아 [확인 2026-04]**(FOD#133 CES 2026, FOD#144 GTC 2026, 2026-04-15 글, [근거](https://turingpost.co.kr/p/nvidia-gtc-2026)). PyTorchKR 주간 논문은 2026-07-13~19호까지 확인 [확인 2026-07], 8~9월 호와 RSS 주소는 [미검증] |
| T3 | 커뮤니티 보조 | 디시 챗지피티 갤러리(?id=chatgpt), 클리앙 AI당(clien.net/service/board/cm_ai), 커리어리(careerly.co.kr), 다음 카페 여성시대(역방향 확산 신호) | 한국인의 AI 놀이, 직장인 AI 활용 후기 | 챗지피티 갤러리 [확인](게시글·나무위키 문서로 재확인. 관련 갤러리 chatgptpro·4o·chatgptmini도 있음). 클리앙 AI당은 게시판만 확인, 최근 활동은 [미검증]. **커리어리는 [휴면 의심]**(사이트는 운영 중이고 2026 채용 글이 있으나 커뮤니티 활동량은 [미검증]). 여성시대(회원 약 72만, 2026-03 검색 요약)는 캡처·인용 금지, 탐색용으로만 |

**벤치마크 (뉴스 소스 아님, 주 1회 형식 분석만)**
- BZCF 텔레그램 `t.me/s/bzcftel`과 bzcf.io
- CHOI(threads.com/@choi.openai)
- AI TREND KOREA(IG·Threads @ai.trend.kr)
- 롱블랙, 폴인(유료라 소스로 쓸 수 없음)

### 3-7. 휴면·개명·변경 플래그 (2026-09-30 기준)

| 대상 | 상태 | 조치 |
|---|---|---|
| xAI | **2026-07-06 SpaceXAI로 개명**(X 핸들 포함) | @xai로 만든 리스트를 @SpaceXAI로 갱신 |
| LMArena | **2026-01-28 Arena(arena.ai)로 개명.** X 핸들도 @lmarena_ai → **@arena**로 바뀌었고 활동 중 [확인 2026-06] | 변경 로그는 arena.ai/blog/leaderboard-changelog. `03` 리스트의 @lmarena_ai를 @arena로 교체 |
| Papers with Code | **2025-07-24 종료** | HF Papers(Trending)로 대체 |
| Sora (@soraofficialapp) | 종료. 앱 2026-04-26, API 2026-09-24 | 리스트에서 제외 |
| @NVIDIAAIDev | 보관 처리됨 | @NVIDIAAI |
| @legit_api | 최근 확인 2025-06, 근거 없는 리크 서술 | 제거함 |
| Higgsfield (@higgsfield_ai) | 2026-02-09 X 계정 정지 | 현재 핸들 미확인 |
| @TheRundownAI | 2026년 X 게시물 [미검증](@rowancheung은 2026-04-27 게시물 확인) | 뉴스레터를 주 채널로 |
| @runwayml(2025-12), @suno(2025-09), @AngryTomtweets 본인(2025-07), @bilawalsidhu | 2026년 X 게시물 [미검증]. Runway·Suno 회사는 2026년에도 출시 활동 중 | 공식 블로그, 릴리스 노트, 다른 플랫폼 우선 |
| AI Explained, 커리어리 | 최근 발행·활동이 확인되지 않음 [미검증] | 구독·팔로우 전에 최근 발행일 확인 |
| 디스콰이엇 | **[종료 의심]** 2025-10-30 픽셀릭 인수 보도, THE VC에 2025-12 폐업 표기(검색 요약) | 최근 글 날짜를 확인하기 전에는 아카이브로만 참고 |
| 휴면 의심 해제(2026-09-30 재검증) | Import AI(474호, 2026-09-28), AINews(2026-09-09호, Latent Space 섹션), Latent Space, @_akhaliq(2026-09), @MistralAI(2026-09-04), 튜링포스트 코리아(2026-04), 더밀크(CES 2026), 롱블랙(2026 새 기능) | 플래그 해제. 월 1회 휴면 점검 대상에서 뺌 |
| GummySearch (Reddit 구독자 수 출처) | 2025-11-30 서비스를 닫았고 2026-12-01 완전 종료 예정(제3자 글) | 구독자 수는 prowlo·subredditstats나 서브레딧 페이지에서 기준일과 함께 확인 |
| 네이버 뉴스 '많이 본 뉴스' | 전체·섹션별 랭킹 2020-11 폐지. 언론사별 랭킹만 남음 | '경제 섹션 + 언론사별 랭킹'으로 봄 |
| 네이버 증권 | **네이버페이 증권**으로 서비스명 변경(도메인 finance.naver.com 그대로) | 출처 표기 이름만 바꿈 |
| 통계청 | **2025-10-01 국가데이터처로 승격**(mods.go.kr) | 기관명 표기 변경 |
| 기획재정부 | **2026-01-02 재정경제부(mofe.go.kr)와 기획예산처로 분리** | 세제·경제정책은 재정경제부, 예산은 기획예산처 |
| 보조금24 | **[개편]** 보조금24(맞춤형 혜택 조회)는 남아 있고, 2025-12-10부터 **정부24+ 혜택알리미**가 받을 수 있는 혜택을 먼저 알려 줌 | 혜택알리미 plus.gov.kr/portal/benefitV2/ 를 주로 보고, 조회는 보조금24도 가능 |
| 한경 컨센서스 | markets.hankyung.com/consensus로 이동 | 북마크 교체 |
| The Neuron | 주소 theneuron.ai, 2025-01 TechnologyAdvice에 인수 | 광고·제휴 콘텐츠 구분 |
| 인물 직함 | Hassabis(2026-08-05 DeepMind 의장 겸 Alphabet 수석과학자), Karpathy(2026-05-19 Anthropic 합류), Nathan Lambert(2026-06 Ai2 떠남), 조경현(2026-01-16 Genentech 떠나 NYU 복귀), Cursor(2026-06-16 SpaceX 인수 발표, 2026-08-14 인수 완료) | 인용 카드의 직함을 최신화 |

---

## 4. 모니터링 셋업 가이드

처음 한 번 2~3시간이면 끝납니다. 이후에는 §5 루틴만 돌립니다.

### 4-1. X 리스트 구성안

- 리스트는 **비공개**로 만듭니다. 비공개 리스트는 추가해도 상대에게 알림이 가지 않습니다.
- 01~08은 `x_ai.md` §3을 그대로 옮긴 것이고, 09는 이번에 추가했습니다.

| 리스트 | 계정 | 볼 때 |
|---|---|---|
| `01_공식발표` | OpenAI, OpenAIDevs, ChatGPTapp, AnthropicAI, claudeai, ClaudeDevs, GoogleDeepMind, GeminiApp, Google, AIatMeta, SpaceXAI, grok, perplexity_ai | 아침·밤 |
| `02_핵심인물` | sama, OfficialLoganK, koraykv, demishassabis, karpathy, bcherny, AravSrinivas, emollick, ClementDelangue | 밤 |
| `03_리크·벤치마크` | testingcatalog, btibor91, chetaslua, scaling01, ArtificialAnlys, arena(구 lmarena_ai) | 아침 |
| `04_큐레이터·해설` | kimmonismus, rohanpaul_ai, HuggingPapers, _akhaliq, vitrupo, rowancheung, TheRundownAI, simonw, WesRoth | 주 2~3회 |
| `05_바이럴·크리에이티브` | minchoi, venturetwins, EHuanglu, AngryTomtweets, AISafetyMemes, bilawalsidhu, midjourney, runwayml, Kling_ai, pika_labs, Hailuo_AI, LumaLabsAI, bfl_ml, suno, ElevenLabs | 밤 |
| `06_중국·오픈모델` | deepseek_ai, Alibaba_Qwen, Kimi_Moonshot, Zai_org, MiniMax_AI, MistralAI, huggingface, op7418 | 주 2~3회 |
| `07_비즈니스` | a16z, Techmeme, NVIDIAAI, nvidianewsroom, cursor_ai | 밤 |
| `08_한국` | hunkims, upstageai, LG_AI_Research, NAVER__Cloud, kchonyc, GeekNewsHada, AITimes_News, yozm_it | 주 2~3회 |
| `09_글로벌경제` **[추가]** | business, technology, FT, WSJ, Reuters, TheEconomist, BusinessInsider, MorningBrew, VisualCap, CBinsights, TechCrunch | 밤 |

- **알림은 6개만 켭니다:** @OpenAI, @sama, @AnthropicAI, @GoogleDeepMind(또는 @OfficialLoganK), @deepseek_ai, @testingcatalog
- **팔로우 전에 확인할 것**
  - @AIatMeta와 @metaai 중 어느 쪽이 현재 계정인지 [미검증](재검증 검색에서 둘 다 'AI at Meta'로 나옴)
  - @Kimi_Moonshot, @Zai_org, @MiniMax_AI의 인증 배지
  - `09` 리스트 매체 핸들 가운데 @WSJ, @Reuters, @TheEconomist, @BusinessInsider 등 [미검증](존재는 확실). @business와 @FT는 `econ_lifestyle.md` 재검증에서 확인(@business와 별도로 @Bloomberg 계정도 있음)
  - (해결) @lmarena_ai는 @arena로 개명 확인 → `03` 리스트에 반영함
- **리스트를 콘텐츠로 묶는 순서:** 01·03(무슨 일이 일어났나) → 02·04(왜 중요한가) → 05(사람들이 뭘 만들었나) → 07·08·09(돈과 한국에는 어떤 의미인가). 이 네 단계를 한 이슈에 적용하면 캐러셀 한 편이 됩니다.

### 4-2. RSS 리더 (Feedly 또는 Inoreader) 폴더 구조

- 사이트 주소만 넣어도 리더가 피드를 자동으로 찾는 경우가 많습니다. 아래 `[미검증]` 주소가 안 되면 사이트 주소를 넣으세요.
- 키워드 필터·규칙 같은 자동 분류 기능은 도구와 요금제마다 이름과 범위가 다릅니다 **[미검증]**.

| 폴더 | 피드 (RSS 주소 또는 입력할 사이트) | 볼 때 |
|---|---|---|
| `01_AI-공식` | `https://openai.com/news/rss.xml` · blog.google/technology/ai/ · deepmind.google | 아침 |
| `02_AI-뉴스` | the-decoder.com · `techcrunch.com/feed/`[미검증] · theverge.com/ai-artificial-intelligence | 아침·밤 |
| `03_AI-해설` | `oneusefulthing.org/feed` · simonwillison.net · `interconnects.ai/feed` · jack-clark.net · `latent.space/feed` · `dwarkesh.com/feed` · `lennysnewsletter.com/feed` · `bensbites.com/feed` | 주 2~3회 |
| `04_글로벌-커뮤니티` | `https://hnrss.org/newest?points=100` · `https://hnrss.org/frontpage` · Reddit 피드(§4-4) · `producthunt.com/feed`(Atom, 3자 가이드로 확인) · GitHub Trending(mshibanami.github.io/GitHubTrendingRSS/에서 일간 피드 선택) · HF Papers 비공식 `papers.takara.ai/api/feed`[미검증](takara-ai/papers-api는 있으나 2026년 작동은 미확인) | 아침·밤 |
| `05_비즈니스` | techmeme.com(`techmeme.com/feed.xml`, 피드 디렉터리 등록으로 확인) · platum.kr · 404media.co | 밤 |
| `06_한국-AI·테크` | GeekNews `news.hada.io/rss/news`(설정 안내 hada.io/blog/geeknews-feed-rss) · `discuss.pytorch.kr/c/news/14.rss`[미검증] · bloter.net | 아침 |
| `07_경제·돈` | `https://www.yna.co.kr/rss/economy.xml`(제3자 문서로만 확인, 등록 전 작동 확인) · `https://www.korea.kr/rss/pressrelease.xml` · 한국경제 섹션 피드(`https://www.hankyung.com/feed`에서 선택) · 매일경제(사이트 RSS 페이지에서 선택) | 아침 |
| `08_유튜브` | 형식 `https://www.youtube.com/feeds/videos.xml?channel_id=채널ID` · 확인된 ID: Two Minute Papers `UCbfYPyITQ-7l4upoX8nvctg`, Last Week in AI `UCKARTq-t5SPMzwtft8FWwnA`, AI타임스 `UCxKaTFMQcCg4kA_oHLGbNxQ`, 조코딩 `UCQNE2JmbasNYbjGAcuBiRRg`, EO Korea `UCQ2DWm5Md16Dc3xRwwhVE7Q` | 주 2~3회 |
| `09_알림` | 구글 알리미 RSS(§4-6) | 아침 |

### 4-3. 뉴스레터 전용 메일함

- 뉴스레터만 받는 **별도 Gmail**을 만들고, 발신 주소 기준 필터로 "받은편지함 건너뛰기 + 라벨"을 겁니다.

| 라벨 | 넣을 뉴스레터 | 여는 시간 |
|---|---|---|
| `AI-NL` | The Rundown AI, TLDR AI, Axios AI+, The Neuron, Ben's Bites, AINews, Import AI, Last Week in AI, The Batch, MIT TR(The Algorithm, The Download), 404 Media, Epoch Brief | 밤(한국 저녁~밤 도착) |
| `BIZ-NL` | Bloomberg·FT·The Information 무료 헤드라인, Stratechery 무료 글, Platformer, a16z, Lenny's, Morning Brew, CB Insights, 아웃스탠딩, 플래텀 | 밤 |
| `KR-AI` **[추가]** | GeekNews 위클리(월요일 아침, 구독 1.8만+), 튜링포스트 코리아, 요즘IT, 바이라인네트워크 | 월요일 아침, 주 2~3회 |
| `KR-ECON` | 어피티 머니레터, 뉴닉, 캐릿 트렌드레터, 정책브리핑 뉴스레터(korea.kr/newsletter/) | 아침 |

- **요약 뉴스레터는 소재 찾기에만 씁니다.** 사실은 공식 발표나 원 기사로 다시 확인합니다.
- 한국 매체는 메일 대신 **네이버 뉴스 언론사 구독**으로 받습니다: AI타임스, ZDNet Korea, 전자신문, 블로터, 디지털데일리, 조선비즈, 머니투데이, 이데일리.

### 4-4. Reddit·Hacker News 필터

- **Reddit**
  - 형식은 `https://www.reddit.com/r/<서브레딧>/top/.rss?t=day`입니다. 주간은 `t=week`입니다. 공개 `.rss` 엔드포인트는 2023년 API 유료화 뒤에도 남아 **2026년에도 작동**한다는 3자 가이드가 있습니다(서브레딧·사용자·검색 URL, top 정렬과 `t=` 필터 지원. 공식 문서는 아님, [근거](https://www.wprssaggregator.com/reddit-rss-feed/)).
  - 일간(`t=day`): LocalLLaMA, singularity, ChatGPT, aivideo, OpenAI, ClaudeAI, GeminiAI, StableDiffusion
  - 주간(`t=week`): MachineLearning, aiArt, artificial, Entrepreneur, personalfinance
  - r/LocalLLaMA는 'New Model' 같은 플레어 위주로 봅니다.
  - 리더에서 막히면 Reddit 앱 알림이나 AINews 요약으로 대신합니다.
  - **구독자 수 출처 주의:** 그동안 쓰던 GummySearch는 Reddit API 상업 라이선스를 받지 못해 2025-11-30에 문을 닫았고, 제3자 글에 따르면 2026-12-01에 완전히 종료됩니다([근거](https://gummysearch.com/docs/gummysearch-is-now-closed-6533h)). 앞으로는 prowlo, subredditstats 같은 대안이나 서브레딧 페이지에서 **기준일과 함께** 확인합니다. r/artificial처럼 사이트마다 수치가 크게 엇갈리는 곳(130만 vs 43만)도 있습니다.
- **Hacker News (hnrss)**
  - `points=100`으로 잡음을 거릅니다. 키워드 피드는 `q=`를 씁니다(예: `https://hnrss.org/newest?q=OpenAI`).
  - hnrss.org 문서로 확인한 파라미터: `q=`, `points=`, `comments=`, `count=`(기본 20, 최대 100). `&`로 조합합니다(예: `https://hnrss.org/newest?q=AI&points=100&comments=20`). 주소 끝에 `.atom`·`.jsonfeed`를 붙이면 다른 형식으로 받습니다([근거](https://hnrss.org/)).
  - 한국 기업 키워드(예: Samsung, Naver)를 따로 걸어 두면 '한국 각도' 소재가 걸립니다.
- **인용 원칙:** 'r/LocalLLaMA에서는 ~라는 반응이 많았다'처럼 **장소를 한정**합니다. u/아이디는 허락을 받았을 때만 적습니다.

### 4-5. 커뮤니티 알림·북마크

| 도구 | 넣을 것 |
|---|---|
| **북마크 폴더 `KR-커뮤니티`** | 에펨코리아 포텐(fmkorea.com/best 최신순, /best2 화제순), 더쿠 HOT(theqoo.net/hot), 특이점 갤러리·AI 활용 갤러리 개념글, 뽐뿌 재테크포럼, 클리앙 새로운소식(공식 RSS 없음), 에펨코리아 핫딜 |
| **로그인 브라우저 프로필 하나** | 블라인드, 네이버 카페(부동산스터디, 월부, 아프니까 사장이다), 다음 카페 여성시대, 아카라이브 |
| **알구몬 키워드 알림** | 딜·앱테크 키워드(예: 특판, 적금, 앱테크) |
| **네이버 카페 앱 키워드 알림 [미검증]** | 가입한 카페의 게시판 키워드. 기능 이름과 범위는 앱에서 확인 |
| **DART 관심 기업 공시 알림** | 대중이 아는 브랜드, 구단, 엔터·코미디 레이블, AI 반도체 기업 |
| **정부24+ 혜택알리미 맞춤 알림** | 청년, 1인가구 등 타깃 조건 |

### 4-6. 구글 알리미 · 네이버 키워드 알림

- **구글 알리미** (google.com/alerts) **[미검증]**
  - 키워드별 알림을 이메일이나 RSS로 받는 기능으로 알려져 있습니다. 이번 조사에서는 확인하지 못했습니다.
  - RSS 전달이 되면 `09_알림` 폴더에 넣습니다.
  - 추천 키워드
    - 한국 적용 여부 확인용: "ChatGPT 한국", "Gemini 한국 출시"
    - 비즈니스: 관심 기업명 + "투자 유치", "감사보고서" + 관심 브랜드
    - 돈: "청년 적금", "금통위", "달라지는 제도"
    - 시즌: "트렌드 코리아 2027"
- **네이버**
  - 한국 매체는 **언론사 구독**으로 받습니다(§4-3).
  - 키워드 뉴스 알림 기능은 **[미검증]**입니다. 앱에서 기능이 있는지 확인하세요.
  - `econ_lifestyle.md`는 편의점 신상용으로 네이버 뉴스 "CU 신상", "GS25 출시" 키워드 알림을 제안했습니다.
  - 기능이 없으면 네이버 뉴스 검색 결과를 최신순으로 북마크해 두고 아침에 한 번 엽니다.

### 4-7. 텔레그램

- **이번 조사에서 확인된 채널은 2개뿐입니다.**
  - GeekNews 텔레그램: 구독 방법은 hada.io/blog/geeknews-subscribe 안내를 따릅니다.
  - BZCF 텔레그램 `t.me/s/bzcftel`: 웹에서 로그인 없이 볼 수 있습니다. **벤치마크 전용**입니다.
- 한국 AI·경제 텔레그램 채널은 이번에 검증하지 못했습니다. 새로 찾으면 T3로 넣고 한 달간 적중률을 본 뒤 올립니다.
- **활용 팁:** 나만 보는 비공개 채널을 하나 만들어 자동화(§4-9) 결과와 휴대폰에서 찾은 링크를 모으는 **수신함**으로 씁니다.

### 4-8. AI로 요약·중복 제거

- 하루치 헤드라인(리더에서 복사, 뉴스레터 목차, X 리스트 메모)을 Claude나 ChatGPT에 붙여 넣고 **묶기 → 1차 출처 표시 → 채점**만 시킵니다.
- **AI 출력은 후보 목록이지 사실이 아닙니다.** 게시 전에는 반드시 원문을 엽니다.

```
너는 한국어 인스타 매거진의 뉴스 데스크다. 아래는 지난 24시간 동안 모은 헤드라인과 링크다.
1) 같은 사건을 다룬 항목끼리 묶고, 묶음마다 1차 출처(공식 발표·공시·논문·원 게시물)에 가장 가까운 링크를 표시해라.
   목록에 1차 출처가 없으면 "1차 출처 미확인"이라고 써라. 링크를 추측해서 만들지 마라.
2) 묶음마다 5개 기준(한국 독자 관련성, 신선도, 시각화 가능성, 저장·공유 유발, 검증 가능성)을 0~2점으로 채점하고 이유를 한 줄로 써라.
3) 리크·루머·커뮤니티 단일 출처는 [루머]로 표시해라.
4) 합계 상위 5개를 표로 정리하고, 각각 "한국 독자에게 한 줄로 왜 중요한가"를 써라.
[여기에 목록 붙여넣기]
```

- **쓰지 말 것**
  - AI 요약을 다시 요약해 게시하는 **'요약의 요약'**을 하지 않습니다. AINews도 AI 생성 요약입니다.
  - 유료 기사 전문을 붙여 넣어 번역문을 만든 뒤 게시하지 않습니다.
- **보조 도구:** 썸트렌드는 2026-03 Claude용 MCP를 출시해 AI 도구 안에서 언급량을 바로 조회할 수 있습니다(`econ_lifestyle.md`).

### 4-9. 선택: 자동화 (n8n / Make / Zapier)

손으로 하는 루틴이 2주 이상 안정되면 붙입니다. **자동 게시는 하지 않습니다.**

```
[RSS 여러 개] → [합치기] → [중복 제거] → [키워드 필터] → (선택) [LLM 분류·요약]
              → [Notion DB '소재 인박스'에 행 추가] → [Slack 또는 텔레그램 비공개 채널에 T1 키워드만 알림]
```

- **도구별 시작 모듈 [미검증, 이름은 버전마다 다를 수 있음]:** n8n의 RSS 피드 트리거 노드, Make의 RSS 'Watch RSS feed items' 모듈, Zapier의 'RSS by Zapier'
- **중복 제거**
  - URL에서 추적 파라미터(`utm_` 등)를 떼고 비교합니다.
  - 이미 본 URL을 저장해 두고 걸러냅니다.
  - 제목이 비슷한 항목은 LLM 단계에서 묶습니다.
- **Notion '소재 인박스' 필드:** 제목 · 원문 URL · 1차 출처 URL · 소스명 · 티어 · 니치 · 발견 시각 · 점수(0~10) · 라벨(공식/보도/루머/의견) · 상태(인박스/검증 중/제작/보류/게시) · 게시 URL
- **주의**
  - X 게시물은 API 비용 때문에 자동 수집이 어렵습니다. Techmeme의 X 게시물에 링크가 빠진 이유도 X API 비용입니다. X는 손으로 리스트를 봅니다.
  - LLM 요약을 **다른 사람에게 서비스로 제공**하면 「인공지능기본법」(2026-01-22 시행)상 이용사업자에 해당할 수 있습니다. 자기 작업용으로만 씁니다(`../best-practices.md` 5-4).

---

## 5. 하루·주간 소싱 루틴

### 5-1. 시차 감각

- 미국 서부 오전 10시 발표는 한국 **새벽 2시**(서머타임 기간) 또는 **새벽 3시**(서머타임 종료 후)에 도착합니다. 그래서 한국 아침에는 밤사이 미국 발표가 쌓여 있습니다.
- 미국 아침에 발송되는 일간 뉴스레터(The Rundown AI 등)는 한국 저녁~밤에 옵니다.
- 한국 정부 보도자료, 공시, 통계는 한국 시간 기준으로 나옵니다. 통계 공표와 금통위는 일정이 미리 고정돼 있어 캘린더에 넣어 둘 수 있습니다(`econ_lifestyle.md`).

### 5-2. 하루 루틴 (KST, 표준 55분 / 최소 30분)

| 시간 | 분 | 할 일 | 소스 (T1 중심) | 산출물 |
|---|---|---|---|---|
| 07:30 | 20 | **밤사이 미국 + 오늘 한국 스캔** | X 알림 6개와 `01`·`03` 리스트, 리더 `01_AI-공식`, hnrss points=100, Reddit 일간(ChatGPT, aivideo), HF Papers Daily → GeekNews, 특갤 개념글 → 연합뉴스 경제 RSS, 정책브리핑 RSS, 네이버 경제 섹션 + 언론사별 랭킹 | 소재 후보 5~8개를 인박스에 |
| 07:50 | 5 | **1차 채점** | §6 체크리스트 | 오늘 제작 1~2개, 내일 후보 2~3개 |
| 12:30 | 10 | **한국 대중 반응** | 에펨코리아 포텐, 더쿠 HOT, 뽐뿌 재테크포럼 + 알구몬 | 후보의 '한국 각도' 메모, 새 소비·딜 소재 |
| 15:00 | 5 | **검증** | 네이버 데이터랩·구글 트렌드로 관심 확인 → 원자료(DART, KOSIS, 공식 블로그, 보도자료 원문) → 독립 소스 2개 | 체크리스트의 '검증 가능성' 확정, [루머] 여부 결정 |
| 21:00 | 15 | **미국 아침 + 다음 날 준비** | The Rundown AI(누락 점검), Techmeme, X `02`·`05`·`07`·`09` 리스트 | 내일 아침 게시물 확정, 인박스 정리 |

- **최소판 30분:** 07:30 스캔 15분(알림, `01` 리스트, GeekNews, 연합뉴스 경제, 네이버 경제 섹션·언론사별 랭킹) + 21:00 15분(The Rundown AI, Techmeme, 에펨·더쿠 훑기)
- **속보가 터진 날**(대형 모델 출시, 금통위, 대형 공시)은 T2·T3를 건너뛰고 해당 이슈의 '예고 → 발표 → 정리' 3연속 게시에 집중합니다.

### 5-3. 주간 루틴

| 요일 | 할 일 |
|---|---|
| 월 | GeekNews 위클리, MIT TR The Algorithm. 이번 주 캘린더 확인(금통위, 통계 공표, 실적, 빅테크 행사). 벤치마크 계정 형식 분석 15분(BZCF 텔레그램, @ai.trend.kr, CHOI) |
| 수 | **T2 몰아 보기 1차:** 해설(One Useful Thing, Simon Willison, Interconnects, `02`·`04` 리스트), 한국(AI타임스, 아카라이브, 클리앙, 지피터스), 경제(한은·국가데이터처 발표, 금융위·파인, 증권사 리포트) |
| 금 | **T2 몰아 보기 2차 + 숫자 카드:** Arena 변경 로그, Artificial Analysis, OpenRouter → '이번 주 AI 순위'. a16z, Stratechery, GitHub Trending, 블라인드, 혜택알리미·온통청년 신규 |
| 토 또는 일 | **T3와 회고:** 트렌드 리포트(20대연구소, 오픈서베이, 트렌드모니터, KB·하나), 다이소·편의점 신상, 청약 캘린더, Last Week in AI로 주간 누락 점검. **이번 주 저장·공유 상위 3개 게시물의 소스를 기록**하고, 한 달 누적으로 소스 티어를 조정 |
| 월 1회 | SPRi AI 브리프, KDI 경제동향. **휴면 점검:** §3-7 플래그 소스의 최근 게시일을 보고 삭제하거나 교체 |

**연간 캘린더(고정 소재)**
- 1월: 연말정산, 잠정실적(DART)
- 3~4월: 감사보고서·사업보고서 시즌(DART가 T1으로 승격)
- 5월: 종합소득세
- 6·12월: '하반기·새해부터 달라지는 것'(정책브리핑)
- 9~10월: 『트렌드 코리아』 출간(2027년판은 2026-09-30 출간, 전시 10/13~11/8, 강연 10/26)
- 연 1회: Stanford AI Index
- 빅테크 행사: 예) OpenAI DevDay 2026-09-29

---

## 6. 소재 선정 체크리스트와 팩트체크 절차

### 6-1. 선정 체크리스트 (각 0~2점, 10점 만점)

| 기준 | 2점 | 1점 | 0점 |
|---|---|---|---|
| **한국 독자 관련성** | 한국에서 바로 쓰거나(한국 출시), 한국 기업·돈·제도에 직접 영향 | 해외 이야기지만 한국 비교 각도가 있음(한국 모델 순위, 한국 기업 연결) | 한국과 연결점이 없음 |
| **신선도** | 24시간 이내이거나, 한국어로 아직 제대로 다뤄지지 않음 | 1주 이내이거나, 이미 다뤄졌지만 새 해석·데이터를 더할 수 있음 | 여러 계정이 이미 같은 각도로 다룸 |
| **시각화 가능성** | 숫자·비교·순서가 있어 표, 차트, 단계, 체크리스트로 직접 만들 수 있음 | 인용 카드나 텍스트 카드는 가능 | 캡처 말고는 보여 줄 게 없음 → 오리지널 인정이 어려움 |
| **저장·공유 유발** | 신청법, 비교표, 체크리스트, '친구에게 보낼' 정보 | 흥미롭지만 한 번 보고 끝남 | 반응을 기대하기 어려움 |
| **검증 가능성** | 1차 출처와 독립 소스 2개 이상 | 1차 출처만 있거나, 보도 2개만 있음 | 커뮤니티 단일 출처, 익명 주장 |

- **7점 이상:** 제작합니다.
- **5~6점:** 해설 각도(왜 중요한가, 한국엔 어떤 의미인가)를 찾으면 제작하고, 못 찾으면 주간 라운드업에 한 줄로 넣습니다.
- **4점 이하:** 보류합니다.
- **점수와 무관하게 제외하는 경우**
  - 검증이 0점인데 [루머] 라벨로도 쓸 가치가 없는 경우
  - 개인을 식별할 수 있거나 명예훼손 위험이 있는 경우(블라인드, 네이트판 사연)
  - 실존 인물 합성·딥페이크
  - 특정 종목·상품 추천으로 읽히는 경우
  - 타 플랫폼 워터마크가 있는 영상

### 6-2. 팩트체크 절차

1. **원문까지 거슬러 올라갑니다.** 뉴스레터 → 기사 → 공식 발표·공시·논문·원 게시물 순서로 갑니다. 커뮤니티는 레이더일 뿐이고, 출처로 적는 것은 원문입니다.
2. **독립 소스 2개 이상으로 확인합니다.** 여러 매체가 같은 단독 기사를 재인용했다면 소스 1개로 셉니다. 예: 'The Information에 따르면'으로 시작하는 기사가 10개여도 소스는 1개입니다.
3. **수치는 원문과 대조합니다.**
   - 에크케의 메타코미디 건처럼 매체마다 증감률이 다르게 나올 수 있습니다(영업익 35%와 96%).
   - 공시는 연결·별도 기준과 기준 연도를 적습니다.
   - 벤치마크는 지수 버전과 조회일을, 통계는 발표 기관과 발표일을 적습니다.
4. **한국 적용 여부를 확인합니다.** 미국에 먼저 나오는 기능이 많습니다. 릴리스 노트나 공식 공지 기준으로 '한국 출시 여부'를 적습니다.
5. **루머·유출은 표시합니다.**
   - 표지와 캡션에 **[루머]** 또는 **[리크]** 라벨을 붙입니다.
   - '코드에서 발견됨', '보도에 따르면'처럼 근거 수준을 그대로 적습니다.
   - 실례: TestingCatalog가 'o'로 예고한 상시 에이전트가 실제로는 'dots'로 발표됐습니다. 이름과 세부는 틀릴 수 있습니다.
6. **인물·조직의 현재 상태를 확인합니다.** 직함, 소속, 개명(§3-7)을 보고, 사칭 계정인지 확인합니다(DeepSeek 공식 계정은 @deepseek_ai 하나).
7. **연구 데모와 제품을 구분합니다.** 연구 데모는 '연구 단계', 프리프린트는 '논문에 따르면', 공식 데모는 '잘 나온 결과만 골랐을 수 있음'으로 적습니다.
8. **의견은 사람 이름으로 인용합니다.** Mollick, Karpathy, CEO의 발언은 그 사람의 견해로 적고 사실처럼 단정하지 않습니다.
9. **정정 절차를 미리 정합니다.** 틀리면 캡션을 수정하고, 정정 문구를 첫 줄에 쓰고, 스토리로 공지합니다. 캐러셀 이미지는 게시 후 순서 변경·삭제가 가능하다는 설명이 있습니다(3자 자료, `../best-practices.md`).

---

## 7. 출처 표기·저작권 가이드

### 7-1. 먼저 알아야 할 인스타 정책

- **2026-04-30부터** 자기가 만들지 않은 콘텐츠를 반복해서 올리거나, 남의 작업을 주로 사진·캐러셀로 올리는 계정은 앱 전반의 **추천(비팔로워 노출)에서 제외**됩니다(TechCrunch·Tubefilter 2026-04-30, [확인 2026-09]).
  - 릴스에 있던 보호 장치를 사진·캐러셀로 넓힌 것입니다. 적용 범위는 메인 피드와 탐색 탭의 추천이고, 기존 팔로워에게 보이는 방식은 바뀌지 않습니다.
  - 라이선스 계약이 있거나 원작자의 명시적 허락을 받은 퍼블리셔는 적용에서 빠집니다([근거](https://techcrunch.com/2026/04/30/instagram-restricts-reach-of-content-aggregators-in-new-crackdown/)).
- **오리지널로 인정되지 않는 것**
  - 테두리·워터마크 추가, 같은 언어 자막, 보이는 내용을 설명만 하는 캡션
  - **출처를 적어도 남의 게시물 스크린샷을 올리는 것**
  - 실용 테스트: "내 기여를 빼도 콘텐츠가 거의 그대로면 오리지널이 아니다"
- **오리지널로 인정되는 것:** 직접 만들었거나 실질적으로 변형한 콘텐츠, 직접 디자인한 가이드·스토리텔링형 시각 콘텐츠
- **복구 조건:** 최근 30일(롤링) 동안 올린 사진·캐러셀·릴스의 대부분이 오리지널이면 다시 추천 대상이 됩니다. **설정 > 계정 상태**에서 확인하고 이의를 제기할 수 있습니다.
- **남의 콘텐츠를 소개할 때** 인스타가 권장하는 방법은 두 가지입니다.
  - **네이티브 리포스트 버튼**(2025-08-06 출시, 원작자 자동 크레딧)
  - **콜라보(공동 작업자) 태그**(최대 5개 계정 초대. 초대는 14일 안에 수락하지 않으면 만료되고, 원작성자를 5명에 포함하는지는 출처마다 다름)
- 근거: `../best-practices.md` §1-2, 5-2. 공식 가이드는 creators.instagram.com/original-content-guidelines입니다.

**원칙 한 줄: 사실 추출 → 내 문장으로 재작성 → 내 해설 추가 → 직접 디자인 → 출처 표기.** 이 방식이 저작권 리스크와 추천 제외 리스크를 동시에 줄입니다.

### 7-2. 유형별 규칙

| 유형 | 하지 않는 것 | 하는 것 |
|---|---|---|
| **X 게시물** | 트윗 스크린샷 게시 | 핵심 문장 1~2개를 번역해 **직접 만든 인용 카드**로 재구성합니다. 표기는 "— 샘 올트먼, X(@sama), 2026-09-28" 형식입니다. 영상은 재업로드하지 않고 원문 링크로 안내합니다 |
| **Reddit·커뮤니티 글** | 캡처, 닉네임·IP 노출, 회원 전용 글 인용 | '레딧 r/LocalLLaMA에서 화제'처럼 장소만 적습니다. 작성자 창작물(이미지, 영상, 번역문)은 허락을 받고 u/아이디나 크리에이터 계정을 태그합니다 |
| **뉴스 기사 이미지** | 기사 사진, 그래픽, 방송 캡처 사용 (텍스트와 별도로 사진 저작권 침해) | 직접 만든 도표·일러스트, 이용 조건을 확인한 공식 보도자료 이미지, 직접 촬영한 사진, AI 생성 이미지(표기) |
| **기사 텍스트** | 문장·구성 번역 전재, 유료 기사 요지를 넘는 번역 | 사실(수치, 발표 내용)은 자유롭게 씁니다(저작권법 제7조 5호: 사실 전달에 불과한 시사보도는 보호 대상이 아님). 기자의 표현과 분석은 보호되므로 내 문장으로 씁니다. 유료 매체는 **매체명 + 날짜 + 요지**만 씁니다. 제목 + 원문 링크 공유는 침해가 아니라는 안내가 있습니다 |
| **번역 인용 범위** | 에세이·인터뷰·보고서 **전문 번역** 게시(허락 없이) | 저작권법 제28조의 인용 요건을 지킵니다: 보도·비평 목적, 정당한 범위, 출처 명시, **내 콘텐츠가 주(主)이고 인용이 종(從)**. 실무에서는 핵심 발언 몇 문장만 직접 인용하고 나머지는 내 요약과 해설로 채웁니다. 캐러셀 한 장 안에서도 인용문보다 내 해설이 많게 합니다. 전문 번역이 필요하면 원저자 허락을 받습니다 |
| **공시·통계·보도자료** | 표 캡처 | 수치를 옮겨 직접 도표화합니다. 공공누리 유형을 확인합니다(변경금지 유형이면 재가공 제한) |
| **크리에이터 작품 (AI 영상·이미지)** | 무단 재업로드, 워터마크 지우기, 모음 게시물 통째로 가져오기 | 허락 + 콜라보 태그 또는 계정 태그. 허락이 없으면 **스틸 1장 + 링크**로 제한하거나 뺍니다. 직접 같은 툴로 만들어 보는 것이 가장 안전한 오리지널입니다 |
| **인물 사진** | 연예인·CEO 사진 무단 사용 (사진 저작권 + 초상권 + 퍼블리시티권) | 공식 보도자료 사진(이용 조건 확인) 또는 일러스트 |
| **광고·협찬** | '더보기' 안에 숨긴 광고 표기 | **이미지 안 + 캡션 첫 줄에 "#광고"**, 유료 파트너십 레이블. 제휴 링크도 똑같이 표시 |
| **AI 생성물** | 사실적인 AI 영상·음성을 표시 없이 게시 | 메타의 AI 공개 도구로 표시하고, 캡션에 "이미지: AI 생성(툴명)"을 적음 |

### 7-3. 출처 표기 형식 (통일안)

- 캐러셀 **마지막 장을 '출처' 슬라이드**로 하고, 캡션 하단에도 적습니다. 인스타 캡션 링크는 눌리지 않으므로 원문 링크는 스토리 링크, 바이오 링크 페이지, 블로그로 연결합니다.
- 예시
  - 공식 발표: `출처: OpenAI 공식 발표(2026-09-29) · CNBC, 9to5Mac 보도`
  - 유료 기사: `블룸버그(2025-07-17) 보도에 따르면`
  - 공시: `한미반도체 2025년 감사보고서(연결 기준), DART`
  - 통계: `국가데이터처 ○○조사(발표일)` / 2025-10 이전 자료는 `통계청`
  - 커뮤니티: `레딧 r/aivideo 화제작 · 원작자 @handle (허락 받음)`
  - 리크: `[리크] TestingCatalog 보도, 공식 확인 전`

### 7-4. 허락 요청 메시지 템플릿

**한국어 (인스타 DM·이메일)**

```
안녕하세요, [계정명] 에디터 [이름]입니다.
[플랫폼]에 올리신 [작품/글 제목 또는 링크]를 보고 연락드려요.
저희 인스타 매거진(@[우리 핸들], 팔로워 약 [N]명)에서
"[게시물 주제]" 캐러셀(또는 릴스)에 이 작품을 소개하고 싶습니다.

- 사용 방식: [영상 전체 / 스틸 1장 / 일부 구간 N초], 수정 없이 사용
- 크레딧: 이미지 안과 캡션에 @[원작자 핸들] 표기, 원하시면 콜라보(공동 작업자)로 초대
- 게시물 성격: [광고·협찬이 없는 일반 게시물 / 협찬이 포함된 게시물]
- 게시 예정일: [날짜]

괜찮으시면 "사용 동의합니다"라고 답장 주세요.
원치 않으시면 사용하지 않고, 게시 후에도 요청하시면 바로 내리겠습니다.
감사합니다.
```

**English (Reddit·X·해외 크리에이터)**

```
Hi [name], I'm [your name], editor at [@our_handle], a Korean-language Instagram magazine about AI.
We'd love to feature your [video/image/post: link] in a post about "[topic]".

- How: [full video / one still / N-second clip], unedited
- Credit: your handle @[handle] on the image and in the caption; happy to add you as a collaborator
- Type of post: [non-sponsored / includes a sponsor]
- Planned date: [date]

If that's OK, could you reply "Yes, you can use it"? If not, no problem, and we'll take it down any time you ask.
Thank you!
```

- 답장은 날짜와 함께 보관합니다. 이 캡처는 게시하지 않고 내부 기록용으로만 둡니다.
- 답이 없으면 '허락 없음'으로 보고 스틸 1장 + 링크로 제한하거나 뺍니다.

---

## 8. 소스 → 인스타 게시물 변환 예시

### 예시 1. X 발표 → 카드뉴스 (AI 뉴스)

- **소스 흐름** (`x_ai.md`)
  - 2026-09-28: @sama가 DevDay 전날 예고
  - 2026-09-29: OpenAI DevDay. CNBC·9to5Mac 보도에 따르면 상시 에이전트 'dots', GPT-6.1 Sol 등 20여 건을 발표 [확인 2026-09](CNBC·9to5Mac·Axios)
  - 사전에 TestingCatalog가 같은 에이전트를 'o'라는 이름으로 예고했음
- **확인**
  - openai.com/news RSS의 공식 글, @OpenAI 원 게시물, 릴리스 노트로 기능별 사실과 **한국 적용 여부**를 확인합니다.
  - CNBC와 9to5Mac으로 교차 확인합니다.
- **각도**
  - ai_freaks형: "20개 중 한국 사용자에게 오늘 달라지는 것 3가지"
  - 로만형 후속: "상시 에이전트가 뭐고 왜 중요한가"
- **캐러셀 (7장)**
  1. 커버: "OpenAI가 어제 20개를 발표했다. 한국 사용자가 알아야 할 건 3개"
  2. 한 줄 요약과 발표 일시
  3~5. 변화 1~3: 각 장에 무엇이 바뀌나 / 누가 쓸 수 있나(요금제) / 한국 출시 여부(확인일). 내용은 **공식 글 기준**으로 채우고 모르는 칸은 비워 둡니다.
  6. 박스 "리크 vs 실제": 'o'로 알려졌던 에이전트가 실제로는 'dots'. 루머 라벨이 왜 필요한지 보여 줍니다.
  7. 출처와 기준일
- **디자인:** 발표 영상 캡처 대신 직접 만든 아이콘과 UI 도식을 씁니다. 공식 이미지를 쓰려면 이용 조건을 확인합니다.
- **캡션:** 첫 줄 훅 → 3줄 요약 → "출처: OpenAI 공식 발표(2026-09-29), CNBC·9to5Mac 보도. 한국 출시 여부는 OpenAI 공지 기준(확인일)".
- **확장:** '예고(전날, [리크] 라벨) → 발표(당일) → 정리(다음 날)'의 3연속 게시가 가능합니다.

### 예시 2. Reddit 바이럴 → 괴짜 콘텐츠 (AI 괴짜·바이럴)

- **소스 흐름** (`source-tracing.md`, `communities.md`)
  - 2026년 여름 'AI 호러' 유행: r/aivideo 주간 상위에 AI 호러 영상이 여러 편
  - 에펨코리아 포텐에 "인스타에서 수집한 AI 기괴호러 영상" 글(2026-07)
  - 뉴스1 "납량특집 대신 'AI호러'로 피서" 보도
- **확인**
  - 네이버 데이터랩으로 'AI 호러' 검색 추이를 봅니다. 대중도 찾는지 확인하는 단계입니다.
  - 영상마다 **원 게시자**를 추적해 인스타·유튜브 계정을 찾습니다. 재공유 계정이 아니라 원작자를 찾아야 합니다.
- **허락:** §7-4 템플릿으로 DM을 보냅니다.
  - 허락 O: 영상 사용 + 콜라보 태그
  - 허락 X: 스틸 1장 + 계정 태그 + 링크로 제한하거나 뺍니다.
- **오리지널 요소 (필수)**
  - 에디터가 같은 유형의 툴로 **직접 만든 짧은 AI 호러 클립**("직접 만들어 봤다"). 원작자가 툴을 밝힌 경우에만 툴 이름을 적습니다.
  - 해설 슬라이드 "AI 괴담 영상, 왜 계속 보게 될까": 익숙한 장소를 쓰는 공통점 같은 **관찰**만 적습니다. 심리학적 주장은 출처가 있을 때만 인용합니다.
- **형식:** 릴스 또는 캐러셀 "요즘 뜨는 AI 호러 크리에이터 5". 각 장은 스틸 + @원작자 + 한 줄 코멘트 + (밝힌 경우) 사용 툴로 구성합니다.
- **제외 조건:** 실존 인물 합성, 타 플랫폼 워터마크 영상, 레딧·커뮤니티 캡처, 미성년자로 보이는 인물
- **캡션:** "영상: 각 크리에이터 제공(허락 받음) · 에디터 제작분은 AI 생성(툴명)". 사실적인 AI 영상이면 AI 공개 도구로 표시합니다.

### 예시 3. 경제 보도자료 → 돈 정보 카드뉴스 (경제·돈)

- **소스 흐름:** 정책브리핑 보도자료 RSS에 금융위원회의 청년 금융상품 보도자료(예: 청년미래적금 같은 제도)가 올라옵니다. 이 카드의 구체 조건은 모두 **보도자료 원문으로 채울 자리**입니다. `econ_lifestyle.md` 재검증은 청년미래적금이 2026-06-22 출시됐다는 것(만 19~34세, 3년 만기, 월 최대 50만 원)까지만 은행 블로그 기준으로 확인했습니다. 게시 전에 금융위 원문으로 다시 확인합니다.
- **확인**
  - 보도자료 원문(PDF)과 금융위 사이트에서 대상, 금액, 기간, 신청처를 확인합니다.
  - 연합뉴스 경제 보도로 교차 확인합니다.
  - **'예정'인지 '확정'인지** 구분합니다(시행일, 법 개정 필요 여부).
  - 공공누리 유형을 확인합니다(보도자료 표 재가공 가능 여부).
- **반응:** 뽐뿌 재테크포럼과 월재연에서 사람들이 헷갈려하는 질문 **유형**만 모읍니다. 캡처와 인용은 하지 않습니다. 이것으로 FAQ 장을 만듭니다.
- **각도:** 에크케형 '벌기·모으기·쓰기' 톤. "누가, 얼마, 언제, 어디서" + "내 경우 계산해 보면"
- **캐러셀 (9장)**
  1. 커버: "[대상]이면 놓치면 손해: [제도명] 3분 정리"
  2. 한 줄 요약
  3. 대상 체크리스트: 나이, 소득, 거주 조건
  4. 금액 표: 납입 한도, 지원 금액. 보도자료 수치를 직접 도표화
  5. 계산 예시: "월 [N]만 원 넣으면 만기 때 [계산값]". 보도자료 조건으로 직접 계산하고 가정을 적음
  6. 신청 방법·기간·신청처
  7. FAQ 3개: 커뮤니티 질문 유형 기반, 답은 원문 근거
  8. 주의: 조건이 바뀔 수 있음, 예정 사항 표시, "거주지·소득 조건 확인 필수"
  9. 출처: 금융위원회 보도자료(발표일), 정책브리핑
- **캡션:** "신청 기간 전에 저장해 두세요" 저장 유도, "특정 금융상품 가입 권유가 아닙니다". 협찬이면 첫 줄에 #광고.
- **응용:** 같은 틀로 DART 공시 → "○○는 이렇게 벌고 씁니다"(연결·별도, 기준 연도 명시)와 한국은행 금통위 → "금리가 내 대출·예금에 미치는 영향"을 만들 수 있습니다.

---

## 9. 파일 안내

| 파일 | 내용 | 언제 보나 |
|---|---|---|
| `README.md` (이 파일) | 소스 맵, Tier 표, 셋업, 루틴, 체크리스트, 저작권, 변환 예시 | 처음 셋업할 때, 주간 회고 때 |
| [`x_ai.md`](x_ai.md) | X 계정 55개 검증본. 최근 활동 날짜, 비공개 리스트 8개 구성, 알림 전략, Top 10, 제거·보류 계정 | X 리스트를 만들고 갱신할 때 |
| [`source-tracing.md`](source-tracing.md) | 4개 계정 게시물의 원본 역추적(BZCF 14건, 에크케 9건), 시차, 가공 방식, 출처 표기 관행 | 경쟁 계정의 소싱 방식을 참고할 때 |
| [`communities.md`](communities.md) | 커뮤니티·애그리게이터 46행(HN, Reddit, HF, GeekNews, 디시, 에펨, 더쿠, 뽐뿌, 블라인드 등). RSS 형식, 인용 원칙. 6장에 2026-09-30 재검증(디시 AI 활용 갤러리 복원, GummySearch 종료 경고) | 커뮤니티 모니터링과 인용 원칙 |
| [`newsletters_media.md`](newsletters_media.md) | 뉴스레터·매체·공식 발표·유튜브 67개. 구독 방법, 유료 매체 처리, 벤치마크 부록 | 메일함과 RSS 리더 셋업 |
| [`econ_lifestyle.md`](econ_lifestyle.md) | 경제·돈·라이프스타일 57개. 정부 조직 개편 반영(국가데이터처, 재정경제부, 정부24+), 트렌드 리포트, 유통 현장. 6장에 2026-09-30 재검증(네이버 랭킹 폐지, 네이버페이 증권, 연합뉴스 RSS 부분 검증으로 하향) | 에크케형 경제 카드 제작 |
| [`../best-practices.md`](../best-practices.md) | 인스타 알고리즘, 독창성 정책(2026-04-30), 광고 표기, 저작권·초상권, AI 생성물 표기, 세무 | 게시 전 법·정책 점검 |
| [`../landscape.md`](../landscape.md) | 한국 AI·비즈니스·경제 매거진 계정 지형 | 포지셔닝 검토 |
| `../accounts/` (`ai_freaks_kr.md`, `bizucafe.md`, `ekke_now.md`, `romaan_mag.md`) | 4개 벤치마크 계정 프로필 상세 | 계정별 벤치마크 |

**남은 확인 과제 (사용자가 직접 하면 좋은 것)**
1. X에서 확인할 것: @AIatMeta와 @metaai 중 현재 계정, 중국 3사 인증 배지, `09_글로벌경제` 매체 핸들(@business·@FT 외), @TheRundownAI·@runwayml·@suno·@bilawalsidhu의 최근 게시일
2. 리더에 넣어 실제 작동 확인: Reddit `.rss`, `techmeme.com/feed.xml`, `producthunt.com/feed`, hnrss 파라미터는 재검증에서 문서·3자 가이드로 확인됐으니 작동만 보면 됩니다. 연합뉴스 경제 RSS(공식 안내 페이지 미확인), HF Papers 비공식 피드, PyTorchKR RSS, `techcrunch.com/feed/`는 아직 [미검증]
3. 구글 알리미의 RSS 전달, 네이버 뉴스·카페 키워드 알림 기능이 있는지 확인
4. 세븐일레븐 인스타 핸들, MLB파크 불펜 URL 형식, 뽐뿌 공식 RSS, 한국은행 RSS, 커리어리·AI Explained의 최근 활동, 디스콰이엇 서비스 지속 여부, K-패스 10월 이후 환급 기준. (해결: 아프니까 사장이다·리멤버 커뮤니티·아카라이브 채널 주소는 2026-09-30 재검증에서 확인)
5. @romaan.mag을 인스타 앱에서 직접 열어 최근 게시물 5~10개의 소재 원본을 기록 → `source-tracing.md` 보강
6. 한국 AI·경제 텔레그램 채널을 새로 찾아 T3로 한 달 시험
