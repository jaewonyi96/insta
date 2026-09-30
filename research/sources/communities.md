# 커뮤니티·애그리게이터 소스 검증본 (communities)

- 작성일: 2026-09-30
- 대상: 한국형 매거진 큐레이션 인스타 계정(@ai_freaks.kr의 AI 뉴스·재미, @romaan.mag의 AI 해설, @bizucafe의 비즈니스 기사와 코멘트, @ekke.now의 돈·경제·라이프스타일)을 운영하면서 **매일 보고 소재를 건질 커뮤니티, 링크 애그리게이터, 트렌드 페이지**
- 결과: 초안 44개 검증
  - **40개 유지**. 그중 2개는 다른 항목에 합쳐 표에서는 38행입니다. URL, 이름, 수치, 서술을 16군데 고쳤습니다(4-3).
  - **4개 삭제**(근거 없음, 휴면 의심, 경쟁 계정). 묶음 항목 안의 근거 없는 하위 주소 7개도 뺐습니다.
  - **7개 추가** → 45행
- **재검증(2026-09-30)**: 1차 검증 때 못 한 웹 검색을 54회 해서 표의 거의 모든 행을 다시 확인했습니다. 결과는 **6장**에 있습니다.
  - 주소 1개를 고쳤습니다(Arena 변경 로그).
  - 1차에서 '추정 주소'나 '근거 없음'으로 뺀 디시 갤러리 가운데 **4곳이 실제로 있었습니다**(특이점 미니, AI 활용, Ai 창작, 해외주식). AI 활용 갤러리는 행으로 되살렸고(→ 표 46행), 해외주식 갤러리는 미국 주식 행에 보조 주소로 넣었습니다.
  - Reddit 구독자 수 출처인 **GummySearch가 문을 닫는 중**이라 기준일이 있는 수치로 바꿨습니다.
  - 추가 7개 가운데 6개는 주소를 확인했습니다. MLB파크 불펜만 주소 형식을 확인하지 못했습니다.
  - 새로 발견한 죽은 소스나 가짜 소스는 없습니다.
- 같이 볼 파일: `x_ai.md`(X 계정), `newsletters_media.md`(뉴스레터·매체·공식 데이터), `source-tracing.md`(4개 계정이 실제로 쓴 원문 역추적)

---

## 1. 개요

### 1-1. 검증 방법과 한계 (먼저 읽어 주세요)

- **이번 단계에서는 새 웹 검색을 하지 못했습니다.** 워크플로 전체의 검색 한도(200회)가 이미 소진돼, WebSearch 3회 시도가 모두 거부됐습니다. WebFetch, curl, 브라우저, GitHub 도구는 규칙에 따라 쓰지 않았습니다.
- 대신 다음 세 가지로 **반대 검증**을 했습니다.
  1. **교차 대조**: 같은 세션의 다른 조사 파일(`newsletters_media.md`, `x_ai.md`, `source-tracing.md`, `../landscape.md`, `../best-practices.md`)에 남은 검색 근거와 맞춰 봤습니다. 예를 들어 LMArena 개명과 Papers with Code 종료는 여기서 확인했습니다.
  2. **초안 근거 점검**: 초안이 적은 근거 URL이 독립된 근거인지, 아니면 그 소스 주소를 그대로 적은 것인지 봤습니다. 날짜가 있는지도 확인했습니다.
  3. **내부 일관성 점검**: 수치 단위, 주소 형식, 추정으로 만든 듯한 주소(예: 다른 갤러리 ID를 그대로 붙인 것), 뉴스 원천이 아닌 항목을 찾았습니다.
- 그래서 1차 검증의 '검증' 칸은 **새로 확인한 사실이 아니라 근거의 종류**를 적은 것이었습니다.
- **2026-09-30 재검증**에서는 WebSearch를 54회 썼습니다(WebFetch, curl, 브라우저, GitHub 도구는 쓰지 않음). 검색 결과 스니펫만 봤고 페이지를 직접 열지는 않았습니다. 그래서 '확인'은 **검색 스니펫에서 확인했다**는 뜻입니다. 재검증한 행은 검증 칸 맨 앞에 아래 표기를 붙였습니다.

| 표기 | 뜻 |
|---|---|
| **재검증 확인(09-30)** | 2026-09-30 검색 스니펫으로 존재, 주소, 활동(가능하면 2026년 글·호)을 확인함 |
| **재검증 부분 확인(09-30)** | 존재는 확인했으나 세부 주소, 활동 시기, 수치 가운데 일부는 확인하지 못함 |
| **이전 조사 확인** | 같은 세션의 다른 파일에 검색 근거가 있음(파일명을 적음) |
| **초안 근거(2026-MM)** | 초안을 쓸 때 검색 스니펫으로 그 달의 활동이 확인됨. 이번에 다시 확인하지는 못함 |
| **초안 근거(존재)** | 초안에 독립된 근거 URL이 있으나 날짜가 없음 |
| **미검증(존재 확실)** | 근거가 그 주소 자체뿐이거나 없음. 다만 대형 서비스라 존재는 확실함. 세부 주소와 수치는 쓰기 전에 확인 |
| **미검증** | 존재나 주소를 확신할 수 없음. **쓰기 전에 반드시 확인** |

- 표 이름 앞의 **[T1]/[T2]/[T3]**는 모니터링 주기입니다(`newsletters_media.md`와 같은 기준).
  - **T1**: 매일 봄
  - **T2**: 주 2~3회
  - **T3**: 주 1회 이하, 필요할 때
- **[추가]**는 초안에 없던 소스입니다. 이번에 검색하지 못했기 때문에 **존재가 확실한 곳만** 넣었고, 모두 '미검증'으로 표기했습니다.

### 1-2. 이번 검증에서 바뀐 핵심

> 아래는 1차 검증 내용입니다. **2026-09-30 재검증에서 일부가 뒤집혔습니다**(디시 갤러리 주소, OpenRouter 수치의 단위, Reddit RSS 작동 여부). 6장을 먼저 보세요.

- **LMArena는 2026-01-28에 Arena(arena.ai)로 이름을 바꿨습니다**(`newsletters_media.md`). 초안의 lmarena.ai를 arena.ai로 고쳤습니다.
- **Papers with Code는 2025-07-24에 종료됐습니다.** Hugging Face Trending Papers를 별도 항목으로 두지 않고 HF Papers 항목에 합쳤습니다.
- **디시인사이드 AI 갤러리 묶음 6개 중 5개**는 근거가 없어 뺐습니다. 특히 숫자 ID(235711)나 다른 도메인 형식이 섞인 주소는 추정으로 만든 주소일 가능성이 있습니다. 근거가 있는 챗지피티 갤러리만 남겼습니다.
- 초안의 '특이점 미니 갤러리' 주소는 본 갤러리 ID(`thesingularity`)를 그대로 붙인 형태이고 근거는 나무위키 스니펫 하나뿐이라 뺐습니다.
- **Threads 한국 AI·비즈 서클**(@choi.openai 등)은 뉴스 원천이 아니라 **경쟁 큐레이터**입니다. `x_ai.md`와 같은 판단으로 부록 '벤치마크'로 옮겼습니다. 시드 계정에 벤치마크 대상인 @bizucafe가 들어 있어 순환 참조이기도 했습니다.
- 확인할 수 없는 **구체 수치**(OpenRouter 'DeepSeek 요청 24.4%', 더쿠 HOT 선정 기준 '댓글 56개·조회 2,050', 더쿠 카테고리 번호)는 뺐습니다.
- 한국 **자영업·마케팅·직장인** 커뮤니티와 **검색 트렌드 도구**가 비어 있어서 추가했습니다(@bizucafe, @ekke.now용).

### 1-3. 모니터링 스택

| 도구 | 넣을 것 |
|---|---|
| **RSS 리더** (Feedly, Inoreader 등) | hnrss 피드, Reddit `top/.rss?t=day` 피드, GeekNews, PyTorchKR, GitHub Trending(비공식) |
| **로그인 브라우저 프로필 하나** | 블라인드, 네이버 카페(부동산스터디, 월부, 아프니까 사장이다), 다음 카페 여성시대, 아카라이브 |
| **북마크 폴더 'KR-커뮤니티'** | 에펨코리아 포텐, 더쿠 HOT, 특이점 갤러리 개념글, AI 활용 갤러리 개념글, 뽐뿌 재테크포럼, 클리앙 새로운소식(공식 RSS 없음) |
| **검색 트렌드** | 네이버 데이터랩, Google 트렌드. 커뮤니티에서 뜬 소재가 대중에게도 퍼졌는지 확인 |

- Reddit RSS 형식: `https://www.reddit.com/r/<서브레딧>/top/.rss?t=day` (주간은 `t=week`)
  - 재검증(09-30): 2026년 제3자 안내글(wprssaggregator.com '모든 URL 패턴이 2026년에도 작동')에서 작동한다고 확인했습니다. 다만 Reddit 공식 문서는 아닙니다. 리더가 막히면 Reddit 앱 알림이나 AINews 요약으로 대신합니다.

**하루 루틴 (KST)**
1. **아침(15분)**: r/LocalLLaMA, r/singularity, Hacker News(밤사이 미국 시간대) → GeekNews, 특이점 갤러리(한국 반응)
2. **점심(10분)**: 에펨코리아 포텐, 더쿠 HOT, 뽐뿌 재테크포럼, 블라인드 토픽 베스트
3. **저녁(10분)**: r/ChatGPT, r/aivideo(재미 소재), HF 트렌딩, Product Hunt 전날 순위

### 1-4. 커뮤니티 소재를 쓰는 원칙

- **커뮤니티는 '레이더'이지 '출처'가 아닙니다.** 커뮤니티에서 소재를 찾으면 공식 발표, 원 기사, 원 게시자까지 거슬러 올라가 확인하고 **그것을 출처로** 적습니다.
- **캡처를 올리지 않습니다.** 인스타는 2026-04-30부터 남의 게시물 스크린샷 위주 계정을 사진·캐러셀 추천에서 뺍니다(`../best-practices.md`, TechCrunch 2026-04-30). 커뮤니티 캡처는 복제권·공중송신권 문제도 있습니다.
- **개인을 드러내지 않습니다.** 닉네임, 유동 IP, 사연 속 인물은 가립니다. 회원 전용 카페와 오픈채팅 글은 인용하지 않습니다.
- **창작물은 허락과 크레딧**을 받습니다. AI 영상, 이미지, 번역문이 여기에 해당합니다. 허락이 없으면 링크와 스틸 1장 정도로 제한합니다.
- **소수 댓글을 '여론'으로 일반화하지 않습니다.** "레딧 r/LocalLLaMA에서는 ~라는 반응이 많았다"처럼 **장소를 한정해서** 씁니다.

---

## 2. 추천 소스 표

### A. 글로벌 링크 애그리게이터·트렌드 페이지

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법(RSS) | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| **[T1] Hacker News** | news.ycombinator.com | 테크·스타트업·AI 개발 | 영어 | 매우 빠름(프론트페이지는 등록 후 수 시간 안) | 프론트페이지 높음, newest 낮음 | RSS(제3자 hnrss.org): `hnrss.org/frontpage`, `hnrss.org/newest?points=100`(100점 이상), `hnrss.org/newest?q=OpenAI`(키워드). 파라미터는 `&`로 조합 | 모델 출시, 오픈소스, 스타트업 사건(인수·셧다운·해고)에 업계인 댓글이 붙음 → @romaan.mag식 해설 재료. Show HN은 신기한 툴 소재(@ai_freaks.kr) | 링크 모음이라 원문 저작권은 원저자에게 있음. 댓글은 'Hacker News 댓글'로 표기하고 업계 전체 반응으로 일반화하지 않음. 영어권 개발자 시각 | **재검증 확인(09-30)**: hnrss.org 안내 스니펫에서 `/frontpage`·`/newest`·`/show`·`/ask`, `points=N`, `comments=N`, `q=키워드`, `count=N`(기본 20, 최대 100)을 확인. 주소 끝에 `.atom`·`.jsonfeed`를 붙이면 다른 형식 |
| **[T1] Techmeme** | techmeme.com (시간순 techmeme.com/river, X @Techmeme) | 테크 비즈니스·빅테크·AI 산업 | 영어 | 수십 분~수 시간 | 높음 | RSS `techmeme.com/feed.xml`(검색 요약에서 확인. 안 되면 리더에 사이트 주소 입력). 클러스터에 붙은 기사 수로 뉴스 크기를 판단 | @bizucafe식 '해외 비즈니스 기사 + 코멘트' 소재. 유료 기사의 원 매체 추적 | 원문 상당수가 유료(Bloomberg, WSJ, The Information). 요지와 매체명만 씀. 미국 중심. **`newsletters_media.md`에 T1로 이미 있음** | **재검증 부분 확인(09-30)**: feed.xml 주소는 검색 요약에서만 확인(피드 디렉터리 페이지). 이전 조사 확인(`newsletters_media.md`). 초안의 'Feeder에 river 피드 등록' 서술은 근거가 약해 뺌 |
| **[T2] Product Hunt** | producthunt.com (일간 순위 `/leaderboard/daily/YYYY/M/D`) | 신규 AI 툴·앱·SaaS | 영어 | 런칭 당일 | 중간(조직적 업보트, 마케팅성 제품) | Atom 피드 `producthunt.com/feed`. 피드는 실시간 순위라 하루 동안 순서가 바뀌므로 다음 날 아침 전날 일간 리더보드를 봄 | '이런 AI도 나왔다' 툴 카드(@ai_freaks.kr). 국내 기사보다 며칠~몇 주 빠름 | 순위가 품질은 아님. 직접 써 보고 소개. 제품 이미지는 메이커 제공분에 출처 표기. 협찬이면 명시 | **재검증 확인(09-30)**: 제3자 피드 안내 페이지(wprssaggregator)에서 Atom 피드 `producthunt.com/feed`와 '실시간 순위 반영' 확인. Product Hunt 헬프센터에도 RSS 안내 문서가 있음. 초안 근거(2026-04 일간 리더보드 URL). 카테고리 피드 `?category=슬러그` 형식은 제3자 안내에만 있고 슬러그는 확인 못 함 |
| **[T1] Hugging Face Papers (Daily + Trending)** | huggingface.co/papers , huggingface.co/papers/trending | AI 연구(논문) | 영어 | Daily는 arXiv 공개 당일~다음 날, Trending은 며칠에 걸쳐 쌓임 | 중상~높음 | 하루 1회 Daily 업보트 상위 5개, Trending은 주 2~3회. 비공식 RSS `papers.takara.ai/api/feed`(제3자, 24시간마다 갱신. 존재는 확인했으나 2026년 작동은 미검증). X @HuggingPapers(`x_ai.md`) | '이제 AI가 이것도 한다'류 연구 소재. 논문 페이지에 연결된 모델과 Spaces 데모를 직접 돌려 해설 근거로 씀 | 프리프린트이니 '입증됐다' 대신 '논문에 따르면'. 그림·영상은 저자 저작물이라 논문명·저자·링크 표기. **Papers with Code는 2025-07-24 종료. 그 이름으로 인용하지 않음** | **재검증 확인(09-30)**: `huggingface.co/papers/trending` 페이지와 HF changelog 'Trending Papers', paperswithcode.com이 HF로 리디렉트된다는 이슈(2025-07) 확인. takara-ai/papers-api 저장소 스니펫에서 RSS 존재 확인. 이전 조사 확인(`newsletters_media.md`). 초안의 별도 항목 'Trending Papers'를 여기에 합침 |
| **[T2] Hugging Face 트렌딩 모델·Spaces** | huggingface.co/models?sort=trending , huggingface.co/spaces | 오픈 모델·데모 | 영어 | 매우 빠름 | 중상 | 하루 1회 트렌딩 상위 10개. 공식 RSS는 확인 못 함 | 중국 오픈모델, 새 이미지·영상·음성 모델을 Spaces 데모로 직접 써 보고 '써봤다' 콘텐츠(@ai_freaks.kr) | 모델 라이선스(비상업·연구 전용) 확인. 실존 인물 합성·딥페이크 결과물은 게시하지 않음 | 미검증(재검증 때 검색 안 함. 존재 확실). 초안 근거(존재, 제3자 스크레이퍼 예시 페이지). 정렬 파라미터 URL은 미검증 |
| **[T2] GitHub Trending** | github.com/trending (비공식 RSS mshibanami.github.io/GitHubTrendingRSS/) | 오픈소스·개발도구·AI 에이전트 | 영어 | 일간 | 중간 | 비공식 RSS(일간·주간·월간, 언어별). 웹에서는 'Today'와 Python·TypeScript 필터 | 바이럴 오픈소스가 비즈니스 뉴스로 번지는 초기 신호. 예: OpenClaw 개발자의 OpenAI 합류(2026-02, `source-tracing.md`) | 스타 조작과 악성 레포가 있음. 설치 권유 없이 소개만. README 이미지 저작권 확인. GitHub 공식 RSS는 없음 | **재검증 부분 확인(09-30)**: mshibanami/GitHubTrendingRSS 저장소 스니펫에서 '매일 실행', 일간·주간·월간과 언어별 피드 확인. 2026년 갱신 날짜는 확인 못 함. RSS는 제3자가 운영해 끊길 수 있음 |
| **[T2] AINews (smol.ai / Latent Space)** | news.smol.ai | AI 커뮤니티 요약(Discord·Reddit·X) | 영어 | 다음 날 | 높음 | 이메일(구 Buttondown에서 news.smol.ai로 이전). 제목과 상단 요약만 읽음 | 커뮤니티를 다 못 본 날의 백업. 제목이 'not much happened today'면 조용한 날 | AI 생성 요약이라 오류가 있을 수 있음. 원 링크 확인 필수. 요약을 다시 번역하는 '요약의 요약' 금지. `newsletters_media.md`에도 있음 | **재검증 확인(09-30)**: 2026-09-09호(`news.smol.ai/issues/26-09-09-not-much`)가 검색됨 → 2026-09에도 발행 중. 이전 조사 확인(`newsletters_media.md`: 2026-02-20호) |
| **[T3] AI 툴 디렉터리 (Future Tools, There's An AI For That, Futurepedia)** | futuretools.io (뉴스 futuretools.io/news), theresanaiforthat.com , futurepedia.io | 신규 AI 툴·대중용 AI 뉴스 | 영어 | 중간 | 낮음~중간 | 주 2회 트렌딩 페이지. 뉴스레터 구독(RSS 미검증) | 저장·공유가 잘 되는 'OO 하는 AI 5선' 캐러셀의 소재 풀 | 유료 등재, 광고, 제휴 링크가 섞임. 목록을 옮기지 말고 직접 테스트한 툴만. TAAFT '뉴스레터 250만+'는 자체 주장(스니펫) | **재검증 부분 확인(09-30)**: futuretools.io/news에 2026-09-23 기사가 있어 활동 확인. 뉴스레터 25만+는 자체 주장. TAAFT 뉴스레터 250만+(다른 페이지는 260만+)는 자체 주장이며 2026년 뉴스레터 추천 글에도 인용됨. **Futurepedia는 재검증 안 함(미검증)** |
| **[T2] Arena(구 LMArena) · Artificial Analysis** | arena.ai (리더보드 변경 로그 **arena.ai/blog/leaderboard-changelog**, 제품 변경 로그 arena.ai/company/product-changelog), artificialanalysis.ai | 모델 성능 비교(공개 리더보드) | 영어 | 출시 후 며칠 | 높음 | 신모델이 나온 주에 확인. Arena 변경 로그는 주 1~2회 | 사람 블라인드 투표(Arena)와 벤치마크 종합(AA)의 1위가 다를 수 있고, 이 차이가 해설 소재가 됨. 이미지·영상 부문은 '가장 잘 그리는 AI' 비교 카드 | **2026-01-28 LMArena → Arena 개명**. 부문, 조회일, 지수 버전을 적음. 캡처 대신 수치를 옮겨 자체 표로. '세계 최고' 단정 금지 | **재검증 부분 확인(09-30)**: Arena 리더보드 변경 로그 주소를 **arena.ai/blog/leaderboard-changelog로 고침**(1차의 /company/leaderboard-changelog는 검색되지 않음. /company/는 제품 변경 로그). 로그에 2026-07 모델 추가 기록이 있어 활동 확인. **Artificial Analysis는 재검증 안 함**. 이전 조사 확인(`newsletters_media.md`, `x_ai.md`). tech-insider.org 비교 기사는 출처 신뢰도를 판단할 수 없어 뺌 |
| **[T2] OpenRouter Rankings** | openrouter.ai/rankings | AI 모델 실사용 점유율 | 영어 | 주간 | 높음 | 주 1회, 조회일과 함께 기록 | '벤치마크 1위와 실사용 1위는 다르다' → @romaan.mag식 해설, @ekke.now식 숫자 카드 | OpenRouter 이용자 기준이지 전체 시장이 아님. **지표 단위(토큰인지 요청인지)를 페이지에서 확인해 그대로 적음** | **재검증 확인(09-30)**: openrouter.ai/rankings 존재 확인. 검색 스니펫에 '2026-09-21 주 **텍스트 요청** 점유율 DeepSeek 24.4%' 문구가 다시 나옴(원 페이지는 특정 못 함). 제3자 집계(tokenmaxxing 등)는 **토큰 기준** 주간 순위를 씀 → 요청 점유율과 토큰 순위가 따로 있음. 수치는 주마다 바뀌므로 표에는 넣지 않음 |

### B. Reddit

> 구독자 수는 초안이 GummySearch, prowlo 스니펫에서 옮긴 값입니다. 대부분 **기준일이 없습니다.** 게시물에 인용할 때는 서브레딧 페이지에서 직접 확인하세요.
>
> **재검증(09-30)**: **GummySearch는 Reddit 데이터 API 상업 라이선스를 받지 못해 문을 닫는 중입니다.** 공식 문서 'GummySearch is now closed'와 'The Final Chapter'가 있고, 2025-11-30에 서비스를 닫았다고 알려졌습니다. 제3자 글에 따르면 기존 유료 이용자는 2026-11-30까지 쓸 수 있고 2026-12-01에 완전히 종료됩니다. 통계 페이지는 아직 갱신되고 있어서(예: r/LocalLLaMA 2026-09-23 갱신) 이번에는 인용했지만 **곧 없어질 출처**입니다. 이후에는 prowlo, subredditstats 같은 대안이나 서브레딧 페이지를 쓰세요. 아래 수치는 모두 2026-09-30 검색 스니펫에서 다시 확인했습니다.

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법(RSS) | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| **[T1] r/LocalLLaMA** | reddit.com/r/LocalLLaMA | 오픈웨이트·로컬 LLM | 영어 | 매우 빠름(분~시간) | 중상 | `reddit.com/r/LocalLLaMA/top/.rss?t=day`. 'New Model'류 플레어 위주 | 중국 모델을 포함한 오픈 모델의 출시, 유출, 벤치마크에 대한 1차 반응과 직접 돌려 본 후기 | '곧 출시' 캡처 같은 유출·루머가 많음 → 공식 확인 전에는 '루머'로 표기. 인용은 r/서브레딧과 u/아이디 | **재검증 확인(09-30)**: 83.2만(GummySearch, 2026-09-23 갱신). 스니펫 요약에 따르면 2026년 7월 중순 약 74.9만에서 늘어 활동 중 |
| **[T1] r/singularity** | reddit.com/r/singularity | AI 대중 담론·빅테크 발표 | 영어 | 매우 빠름 | 중하(하이프가 많음) | `.../r/singularity/top/.rss?t=day` | 대형 발표가 있으면 요약 스레드가 즉시 생김 → '오늘 무슨 일이 있었나' 빠른 파악. 시연 클립과 밈 | 'AGI 도래'식 과장과 출처 불명 캡처. 원 출처(공식 블로그, X 원글)를 역추적. 영상 재업로드 금지 | **재검증 확인(09-30)**: 약 400만(GummySearch, 2026-09-17 갱신). 제3자 통계 스니펫은 3,952,358명(2026-08-13) |
| **[T2] r/OpenAI** | reddit.com/r/OpenAI | OpenAI 제품·업데이트 | 영어 | 매우 빠름 | 중간 | `.../r/OpenAI/top/.rss?t=day` | 기능 롤아웃, 장애, 요금 변경 사용자 제보 → '지금 ChatGPT에 생긴 변화' 속보 카드 | 일부 사용자만 받는 A/B 테스트를 전체 출시로 오해하기 쉬움. OpenAI 공식 발표로 교차 확인 | **재검증 부분 확인(09-30)**: 270만(GummySearch 스니펫 재확인. 기준일은 여전히 불명) |
| **[T1] r/ChatGPT** | reddit.com/r/ChatGPT | 대중 AI 활용·밈 | 영어 | 매우 빠름 | 낮음(밈과 불평이 많음) | `.../r/ChatGPT/top/.rss?t=day`. 업보트 상위만 | 가장 큰 AI 서브레딧. 웃긴 결과물과 프롬프트 유행(이미지 스타일 밈 등)이 여기서 터짐 → @ai_freaks.kr '재밌는 AI'의 본진 | 이미지·대화 캡처는 작성자 권리, 사진 속 인물은 초상권. 허락과 u/아이디 크레딧. 조작된 '챗GPT 답변' 캡처가 흔함 | **재검증 확인(09-30)**: 11,614,347명(2026-08-31, 제3자 통계 스니펫). GummySearch도 1,160만 |
| **[T2] r/ClaudeAI · r/GeminiAI** | reddit.com/r/ClaudeAI , reddit.com/r/GeminiAI | 모델별 사용자 커뮤니티 | 영어 | 빠름 | 중간 | 두 서브레딧의 `top/.rss?t=day` | 신기능, 사용 한도 변경, 체감 품질 반응 → 'ChatGPT vs Claude vs Gemini' 비교 콘텐츠의 근거 | '성능이 떨어졌다'는 체감 글은 근거가 약함. 개인 경험으로만 소개 | **재검증 확인(09-30)**: r/ClaudeAI 1,093,707명(2026-08-23, 제3자 통계 스니펫. 2026-07에 100만 돌파). r/GeminiAI 37.2만(GummySearch, 기준일 불명), reddapi는 366,844명 |
| **[T2] r/StableDiffusion** | reddit.com/r/StableDiffusion | 오픈 이미지·영상 생성 | 영어 | 빠름 | 중간 | `.../r/StableDiffusion/top/.rss?t=day` | 오픈 이미지·영상 모델, ComfyUI 워크플로 같은 새 기법이 가장 먼저 공유됨 → '이제 집에서도 이런 영상이' 소재 | NSFW, 실존 인물 LoRA, 작가 화풍 모방 논란. 결과물은 생성자 허락과 크레딧 필요 | **재검증 확인(09-30)**: 998,663명(2026-08-31), 하루 글 64.3개(prowlo, 2026-08) |
| **[T1] r/aivideo (+ r/aiArt)** | reddit.com/r/aivideo , reddit.com/r/aiArt | AI 영상·아트 쇼케이스 | 영어 | 빠름 | 중간 | `top/.rss?t=day` 또는 `t=week`. 반응 좋은 작품은 작성자의 인스타·유튜브 계정을 찾아 둠 | Seedance, Kling, Veo 등으로 만든 영상 → '이게 AI라고?' 릴스 소재. 크리에이터 컴필레이션 포맷(`source-tracing.md`의 'AI 호러 계정 모음' 사례)과 잘 맞음 | 영상 재업로드는 저작권 침해. 크리에이터 허락과 계정 태그가 기본. 허락이 없으면 스틸 1장과 링크 | **재검증 부분 확인(09-30)**: r/aivideo 38.9만, r/aiArt 68.6만(GummySearch 스니펫 재확인, 기준일 불명. r/aiArt는 최근 1년 약 4.7만 가입) |
| **[추가][T2] r/MachineLearning** | reddit.com/r/MachineLearning | AI 연구 토론([R] 논문, [D] 토론) | 영어 | 빠름 | 중상 | `.../r/MachineLearning/top/.rss?t=week` | 연구자 시각의 비판과 재현 논의. 과장된 논문·벤치마크에 대한 반론이 @romaan.mag식 '과장 걷어내기' 해설 재료가 됨 | 전문 용어가 많아 대중 눈높이로 옮겨야 함. 댓글은 개인 의견으로만 인용 | **재검증 확인(09-30)**: 310만(GummySearch, 2026-08-27 갱신) |
| **[T3] r/artificial** | reddit.com/r/artificial | AI 일반 뉴스·사회 이슈 | 영어 | 빠름 | 중간 | `.../r/artificial/top/.rss?t=day` | r/singularity보다 하이프가 덜한 규제, 일자리, 사회 이슈 토론 | 기사 링크 공유 중심 → 원 기사 매체명으로 인용 | **재검증 부분 확인(09-30)**: 130만(GummySearch 스니펫 재확인, 기준일 불명). 다른 통계 사이트는 43만으로 표기해 수치가 엇갈림. 인용 전 서브레딧에서 확인 |
| **[T3] r/Entrepreneur** | reddit.com/r/Entrepreneur | 창업·1인 사업 | 영어 | 느림(에버그린) | 낮음(자기홍보, 조언 요청) | `top/.rss?t=week` | 'AI로 1인 사업' 실전 사례 → @bizucafe식 교훈형 콘텐츠 | 과장된 수익 인증과 홍보글. 확인 불가 매출 수치는 쓰지 않음. 개인 사연은 식별 불가하게 | **재검증 부분 확인(09-30)**: 530만(GummySearch 스니펫 재확인, 기준일 불명. 최근 1년 약 37.7만 가입) |
| **[T3] r/personalfinance** | reddit.com/r/personalfinance | 미국 개인재무·저축 | 영어 | 느림 | 중간 | `top/.rss?t=week` | 미국 2030의 구독료, 물가, 저축 규칙 → @ekke.now식 '미국 2030은 이렇게 모은다' 비교 카드 | 미국 제도(401k, 신용점수) 기준이라 한국 제도로 바로 옮기면 안 됨. 투자 권유로 읽히지 않게 | **재검증 부분 확인(09-30)**: 2,180만(GummySearch 스니펫 재확인, 기준일 불명). 초안의 '+ r/Money'는 근거와 설명이 없어 뺌 |

### C. 한국 AI·테크 커뮤니티

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법(RSS) | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| **[T1] GeekNews (긱뉴스)** | news.hada.io (X @GeekNewsHada, 봇 @GeekNewsBot, 위클리 news.hada.io/weekly) | 개발·테크·AI·스타트업 | 한국어 | 빠름(해외 원문 기준 수 시간~1일) | 높음 | RSS 최신글 `news.hada.io/rss/news`(설정 안내 hada.io/blog/geeknews-feed-rss), 월요일 위클리, 텔레그램, X. 상위 20개를 하루 1회 | 한국 테크 종사자의 필터를 한 번 거친 '한국에서 반응할 해외 소식' 선별기 | GN 요약문은 작성자의 번역·요약물. 복사하지 말고 원문 기준으로 다시 씀. 'GeekNews를 통해 알게 됨' 정도의 크레딧 권장. `newsletters_media.md`에 T1로 있음 | **재검증 확인(09-30)**: 하다 스튜디오 블로그에서 RSS 주소 `news.hada.io/rss/news`(블로그 피드 `/rss/blog` 등)를 확인. hada.io 프로젝트 페이지에서 위클리 1.8만+ 구독 확인(날짜 미상). X @GeekNewsHada·@GeekNewsBot 존재 확인. 초안의 '광고가 없다'는 근거가 없어 뺌 |
| **[T1] 디시인사이드 특이점이 온다 마이너 갤러리(특갤)** | gall.dcinside.com/mgallery/board/lists/?id=thesingularity | AI·AGI·미래기술 | 한국어 | 매우 빠름(해외 발표 후 수십 분) | 중하(정보글은 좋지만 잡담·조롱이 많음) | '개념글' 탭 위주로 하루 2회(오전·밤). 해외 발표가 있는 날은 자주 | 해외 AI 발표를 번역한 정보글이 한국어로 가장 빨리 올라옴. 한국 AI 헤비유저의 반응 온도 | 욕설, 조롱, '특이점 왔다'식 과장, 번역 오류. 인용은 '디시인사이드 특이점이 온다 갤러리'로 하고 닉네임·IP는 가림. 번역 이미지 캡처 금지 | **재검증 확인(09-30)**: 갤러리 주소와 '특갤의 역사' 등 게시글 검색됨. 나무위키 서술('2026년 이후 AI 코딩 글이 주류', '2024-11 운영자 교체')을 다시 확인했으나 여전히 나무위키 단일 출처. 나무위키에 따르면 **운영진이 코딩 글을 분리·차단하자 반발한 이용자들이 AI 활용 마이너 갤러리로 옮겨 갔음** → 아래 AI 활용 갤러리 행과 같이 봄. 관련: 특이점 미니 갤러리(m.dcinside.com/mini/thesingularity)와 '특이점은 안온다' 미니 갤러리(m.dcinside.com/mini/agihype)도 있음 |
| **[T2] 디시인사이드 챗지피티 마이너 갤러리** | gall.dcinside.com/mgallery/board/lists/?id=chatgpt | ChatGPT 활용·프롬프트 | 한국어 | 빠름 | 중하 | 개념글 주 2~3회 | 한국 사용자의 실전 팁과 한국어 결과물 → @ai_freaks.kr '한국인이 해 본 AI 놀이' 소재 | 탈옥 프롬프트, NSFW, 실존 인물 합성 글은 쓰지 않음. 결과물은 작성자 허락과 크레딧 | **재검증 확인(09-30)**: m.dcinside.com/board/chatgpt 게시글과 나무위키 문서 확인. 나무위키에 따르면 지브리풍 이미지 유행 뒤 흥한 갤러리 100위권에 들었고, ChatGPT 외 다른 AI 이야기도 많음. 관련 갤러리로 챗지피티 프로(chatgptpro), 챗지피티 4o(4o), 챗지피티 미니 갤러리(chatgptmini)도 있음. **초안 묶음에서 1차에 뺀 5개 가운데 ai_utilize와 aicreate는 실제로 있었음**(6장). 나머지 3개는 여전히 미검증 |
| **[복원][T2] 디시인사이드 AI 활용 마이너 갤러리** | gall.dcinside.com/mgallery/board/lists/?id=ai_utilize (모바일 m.dcinside.com/board/ai_utilize) | AI 도구 활용·AI 코딩 | 한국어 | 빠름 | 중하 | 개념글 주 2~3회. 특갤과 같이 봄 | 나무위키에 따르면 특갤이 코딩 글을 막은 뒤 옮겨 온 이용자가 많고, 분위기가 특갤보다 자유로움. 한국 헤비유저의 AI 코딩·도구 실사용 반응 | 잡담·조롱, 탈옥·NSFW 글. 닉네임·IP 가림. 결과물은 작성자 허락과 크레딧 | **재검증 확인(09-30)**: 갤러리 페이지와 게시글(PC·모바일 주소 모두), 나무위키 문서 확인. 1차에서 '추정 주소'로 뺐던 항목을 되살림. 활동량 순위는 미검증 |
| **[T2] 아카라이브 AI 채널** | arca.live/b/ai101 (AI 정보), arca.live/b/alpaca (AI 언어모델 로컬), arca.live/b/aiart (AI 그림), arca.live/b/characterai (AI 채팅), arca.live/b/aivideo (AI 영상) | LLM 정보·로컬 모델·AI 이미지·캐릭터챗 | 한국어 | 빠름 | 중간(ai101은 높음, 그림·채팅은 낮음) | 채널별 '개념글/베스트' 탭 주 2~3회. **ai101과 alpaca 우선** | ai101은 언어모델 논문·뉴스·팁 모음. alpaca는 한국 로컬 LLM 사용자 반응(r/LocalLLaMA의 한국판). 채팅 채널은 한국 AI 캐릭터챗 서브컬처 트렌드 | 성인 콘텐츠와 탈옥 글이 많아 aiart·characterai는 참고만(브랜드 안전). 커뮤니티 은어를 그대로 옮기지 않음 | **재검증 확인(09-30)**: 5개 채널 주소가 모두 있음(ai101 'AI 정보 채널', alpaca 'Ai 언어모델 로컬 채널', aiart 'AI 그림 채널', characterai 'AI 채팅 채널', aivideo 'AI영상 채널'). 구독자 수: characterai 3.2만+, **aivideo 1,961명으로 작음**(스니펫, 시점 불명). 2026년 활동은 확인 못 함 |
| **[T2] 클리앙 새로운소식** | clien.net/service/board/news | IT·테크·경제 뉴스 | 한국어 | 빠름 | 중상 | 하루 1~2회, 추천 많은 글 위주(**공식 RSS 없음**. 이용자가 만든 feedburner 피드는 작동 미검증) | IT에 밝은 3040 직장인이 국내외 기사를 퍼 오고 실무자 댓글이 붙음. 국내 통신·플랫폼 규제 뉴스를 한국 독자 반응과 함께 봄 | 대부분 퍼 온 기사라 원 기사를 인용. 정치 성향이 강한 댓글이 많아 '여론'으로 일반화하지 않음 | **재검증 부분 확인(09-30)**: 클리앙 게시글 스니펫에서 '공식 RSS 미지원'과 이용자 제작 피드 확인. 게시판 존재는 확실하나 2026년 글은 확인 안 함 |
| **[T3] 클리앙 AI당(소모임)** | clien.net/service/board/cm_ai | AI 활용 | 한국어 | 중간 | 중상 | 주 2~3회 | 직장인 헤비유저의 실사용 후기, 요금제 비교, 업무 활용 팁 → '직장인 AI 활용법' 저장형 캐러셀 | 닉네임 비노출. 요금·기능은 공식 페이지로 재확인 | **재검증 부분 확인(09-30)**: 'clien.net/service/board/cm_ai = 클리앙 : AI당' 확인. 활동 시기는 미검증. AI그림당(cm_aigurim)도 실제로 있으나 우선순위가 낮아 계속 뺌 |
| **[T2] 지피터스 (GPTers)** | gpters.org (Threads @gptersorg, IG @gptersorg) | 생성형 AI 활용·바이브코딩·자동화 | 한국어 | 중간 | 중상 | 주 2회 게시판 인기글, Threads 팔로우 | 직장인·1인 창업자의 실전 사례(자동화, 바이브코딩) → '한국인은 AI로 이렇게 일한다' 소재와 인터뷰 섭외 풀 | 스터디 판매·홍보 글이 섞임. 사례 인용은 작성자 허락과 크레딧. 네이버 카페 현황은 미검증 | **재검증 확인(09-30)**: gpters.org에서 'AI 스터디 24기' 판매 중인 것 확인(활동 중). 유튜브 @gpters('GPTers 커뮤니티'), Threads @gptersorg 존재 확인. 이전 조사 확인(`../landscape.md`: IG 1,220, Threads 2,841). '누적 수강생 6천 명', '국내 최대 AI 커뮤니티'는 자체 주장 |
| **[T2] PyTorchKR 읽을거리&정보공유** | discuss.pytorch.kr/c/news/14 | AI 연구·오픈소스(한국어) | 한국어 | 주간 | 높음 | RSS `discuss.pytorch.kr/c/news/14.rss`(Discourse 포럼의 표준 형식, 미검증). 주 1회 주간 논문 모음 | 매주 '이번 주에 살펴볼 만한 AI/ML 논문' 한국어 정리 → @romaan.mag식 설명 콘텐츠의 배경 지식 | 운영자의 번역·요약물이라 그대로 옮기지 말고 원논문을 확인해 다시 씀 | **재검증 확인(09-30)**: 2026-02부터 2026-07까지 주간 논문 모음이 매주 검색됨(최근 확인분 '2026/07/13~19', discuss.pytorch.kr/t/…/11328). 2026-08~09 글은 검색되지 않았으니 쓰기 전 최신 글 날짜 확인. RSS 주소는 미검증 |
| **[T3] 디스콰이엇 (Disquiet)** | disquiet.io | 국내 IT 프로덕트·인디해커·스타트업 | 한국어 | 중간 | 중간 | 주 1~2회 인기 프로덕트와 로그 | 국내 신생 AI 서비스와 1인 창업 사례. 메이커에게 연락해 확인받으면 오리지널 인터뷰 콘텐츠가 됨 | 메이커 셀프 홍보가 기본이라 성과 수치는 '본인 주장'으로 표기 | **재검증 부분 확인(09-30)**: THE VC 스니펫에 따르면 **2025-10-30 릴레잇 운영사 픽셀릭이 인수**했다는 보도가 있음(원 보도 미확인). 사이트와 앱은 있으나 2026년 활동량은 확인 못 함 → 운영 방향이 바뀌었을 수 있으니 최근 글 날짜부터 확인. 초안의 '운영사 임직원 6명'은 소스 판단과 무관해 뺌 |
| **[T3] 커리어리** | careerly.co.kr | IT 커리어·테크 트렌드 | 한국어 | 중간 | 중간 | 주 1회 트렌드·인기 피드 | 현업자가 해외 아티클을 요약하고 코멘트하는 '아티클 + 코멘트' 포맷의 한국어 레퍼런스 | **[활동 확인 필요]** 2024-09 운영사 변경 보도 뒤 활동량을 확인 못 함. 먼저 최근 글 날짜를 볼 것. 타인의 요약·코멘트를 가져오지 않음 | **재검증 부분 확인(09-30)**: 사이트는 운영 중('[2026] AI 서비스 기획' 채용 글 등). 앱 이름은 '커리어리 - 요즘 개발자 커뮤니티', 활동 개발자 6만~7만은 자체 소개. **2026년 커뮤니티 글의 활동량은 여전히 미검증**. 초안 근거(2024-09 한국경제 보도: 가입자 38만, 그중 개발자 5만) |

### D. 한국 대중 커뮤니티 (바이럴·트렌드 레이더)

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법(RSS) | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| **[T1] 에펨코리아 포텐 터짐** | fmkorea.com/best (포텐 터짐 최신순), fmkorea.com/best2 (포텐 터짐 화제순) | 종합 유머·이슈·바이럴 | 한국어 | 매우 빠름 | 낮음(자극적인 글이 많음) | 하루 1~2회. 'AI', '챗GPT', '연봉', '월급' 키워드로 훑음 | 일정 추천을 받은 글이 모이는 베스트 게시판(정치·시사 제외). 대중에게 먹히는 AI 소재를 재는 레이더. 2026-07 '인스타에서 수집한 AI 기괴호러 영상' 글이 @ai_freaks.kr 추정 게시물과 같은 시기에 확인됨 | 퍼 온 글이 많아 원출처(해외 SNS·유튜브)를 끝까지 추적. 성별·정치 갈등성 글은 피함. 캡처 게시 금지 | **재검증 확인(09-30)**: 페이지 제목으로 /best = '포텐 터짐 최신순', /best2 = '포텐 터짐 화제순' 확인. 2026 아시안게임 축구 관련 포텐 글이 검색돼 최근 활동 확인. 이전 조사 확인(`source-tracing.md`: fmkorea.com/best/9789775469, 2026-07). 초안의 '나무위키 실검에 자주 반영'은 근거가 약해 뺌 |
| **[T1] 더쿠 HOT · 스퀘어** | theqoo.net/hot , theqoo.net/square | 연예·소비·라이프스타일 이슈(2030 여성 비중이 높은 것으로 알려짐) | 한국어 | 매우 빠름 | 중간 | HOT를 하루 1~2회. 카테고리는 사이트에서 직접 고름 | 소비 트렌드, 식품·브랜드 밈이 가장 빨리 퍼지는 곳 가운데 하나 → @ekke.now식 소비 트렌드 카드의 초기 신호(예: 두쫀쿠 열풍, `source-tracing.md`) | 스퀘어 글도 대부분 퍼 온 것이라 원출처 추적. 팬덤 갈등성 소재는 역풍 위험. 댓글 캡처 금지 | **재검증 확인(09-30)**: theqoo.net/hot에 2026-05, 2026-06 글이 검색됨. 스퀘어 안내글에 따르면 HOT는 각 카테고리에서 댓글·조회가 많은 글을 모은 것. 초안의 카테고리 번호(24788)와 HOT 선정 기준 수치(댓글 56개·조회 2,050)는 여전히 확인 못 해 뺀 상태로 둠 |
| **[추가][T2] 네이트판 (톡커들의 선택)** | pann.nate.com (톡커들의 선택 pann.nate.com/talk/ranking) | 생활 사연·직장·연애·결혼·소비 | 한국어 | 빠름 | 낮음 | 일간 랭킹 하루 1회 | 결혼 비용, 직장, 돈 문제 같은 '요즘 사람들' 사연이 기사화되기 전에 뜸 → @ekke.now 라이프스타일 카드의 초기 신호 | 사연의 진위를 알 수 없고 지어낸 글이 많음. 개인 사연은 식별 불가하게. 캡처 금지 | **재검증 확인(09-30)**: pann.nate.com/talk/ranking = '톡커들의 선택' 페이지 확인. 공식 앱도 운영 중. 게시물 활동 시기는 미검증 |
| **[추가][T3] MLB파크 불펜** | mlbpark.donga.com/mp/b.php?b=bullpen | 3040 남성 중심 이슈·경제·부동산·주식 | 한국어 | 매우 빠름 | 낮음 | 하루 1회 추천글 | 3040 직장인의 경제 체감(연봉, 집값, 주식) 온도. 더쿠와 비교하면 성별·세대별 반응 차이가 보임 | 정치 글 비중이 큼. '여론'으로 일반화하지 않음 | **재검증 부분 확인(09-30)**: 위키백과·나무위키에서 동아닷컴이 운영하는 MLBPARK의 자유게시판이 '불펜'임을 확인. `b.php?b=bullpen` 주소 형식과 2026년 활동은 미검증 |
| **[T3] 다음 카페 여성시대 (역방향 확산 신호)** | cafe.daum.net/subdued20club | 2030 여성 라이프스타일·이슈 | 한국어 | 빠름 | 중간 | 자사·경쟁 계정 이름으로 주 1회 검색(가입 필요) | @ekke.now의 '산타는 이렇게 벌고 씁니다'가 이 카페로 퍼진 사례가 있음. 어떤 포맷과 주제가 공유되는지 사후 검증하는 레이더 | 회원제 카페라 게시글 외부 반출을 금기로 여기는 문화가 강함. 소재 탐색용으로만 쓰고 캡처·인용하지 않음 | **재검증 확인(09-30)**: cafe.daum.net/subdued20club 게시판 검색됨. 회원 약 72만(2026-03 기준, 검색 요약. 다른 스니펫은 72.9만·81.8만으로 시점 불명). 이전 조사 확인(`source-tracing.md`: m.cafe.daum.net/subdued20club/ReHf/5155384) |

### E. 한국 돈·직장·자영업·마케팅 커뮤니티

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법(RSS) | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| **[T1] 뽐뿌 재테크포럼** | ppomppu.co.kr/zboard/zboard.php?id=money (핫딜 게시판 id=ppomppu) | 재테크·특판 적금·카드·대출 | 한국어 | 매우 빠름 | 중상 | 하루 1회 추천순. 핫딜 게시판을 함께 보면 소비 트렌드도 보임 | 특판 적금, 카드 혜택, 금리 변경, 앱테크 정보가 금융사 발표 직후 올라옴 → @ekke.now식 '이번 주 돈 되는 정보' 카드. 증권, 창업·자영업, 보험, 카드, 대출 하위 게시판도 있음 | 특판은 조기 마감되거나 조건이 바뀜 → 금융사 공식 공지로 확인하고 게시 시점을 적음. 특정 상품 추천으로 읽히면 광고·투자권유 논란 | **재검증 확인(09-30)**: `zboard.php?id=money` = '뽐뿌 - 재테크포럼', 증권포럼 `id=stock` 확인. 핫딜 게시판(`id=ppomppu`) 주소는 미검증(존재 확실) |
| **[T1] 블라인드 토픽 베스트** | teamblind.com/kr/topics/토픽-베스트 | 직장·연봉·기업 내부 분위기 | 한국어 | 매우 빠름 | 중간 | 토픽 베스트와 시사토크를 하루 1회(로그인 필요) | 회사 인증 직장인의 연봉, 성과급, 구조조정, 사내 AI 도입 분위기가 기사보다 먼저 드러남 → @bizucafe·@ekke.now의 '요즘 직장인' 소재 | 익명 폭로는 사실 확인이 어렵고 명예훼손 소지가 큼(2021 KBS 직원 게시글 캡처 확산 논란). 캡처를 쓰지 않고, '블라인드에서 화제'라고 쓸 때는 기사나 공식 입장으로 교차 확인 | **재검증 확인(09-30)**: teamblind.com/kr/topics/토픽-베스트가 '토픽 베스트' 페이지임을 확인. 2026-06 글도 검색됨. 비슷한 토픽으로 '지금핫이슈'(teamblind.com/kr/topics/지금핫이슈)가 있음 |
| **[추가][T2] 네이버 카페 아프니까 사장이다** | cafe.naver.com/jihosoccer123 | 자영업·소상공인 | 한국어 | 빠름 | 중간 | 가입 후 인기글 주 2~3회 | 배달앱 수수료, 최저임금, 임대료, 폐업 같은 자영업 경기 체감이 기사보다 먼저 보임 → @bizucafe·@ekke.now의 '사장님들의 현실' 소재 | 회원 전용 글은 캡처·인용하지 않음. 개인 매출 공개 글은 식별 불가하게 | **재검증 확인(09-30)**: 주소 cafe.naver.com/jihosoccer123 확인(2026-09 바로가기 안내글, 보라디스 '2011-09-24 개설'). **회원 수는 출처마다 다름**: 공식 광고 페이지(aspsajang.com) 195만+ 자체 주장, 블로그 168만, 더 오래된 글 96.8만·78만. 인용하려면 카페 첫 화면에서 확인 |
| **[T2] 네이버 카페 부동산스터디** | cafe.naver.com/jaegebal | 부동산·대출·세무 | 한국어 | 빠름 | 중간 | 가입 후 인기글 주 2~3회. 앱 키워드 알림(미검증) | 대출 규제, 청약, 집값 체감 이슈가 기사화 전에 올라옴 → @ekke.now식 '내 집 마련' 소재 | 회원 전용 글은 캡처·인용하지 않음(카페 규정). 집값 전망은 루머와 선동이 섞임. 정책은 국토부·금융위 원문으로 확인 | **재검증 부분 확인(09-30)**: 카페 주소 jaegebal 확인(운영자 '붇옹산'의 페이스북 페이지도 jaegebal, 보라디스 '2006-11-19 개설'). **회원 수는 약 104만과 약 163만으로 출처마다 다르고** 시점도 불명 → 인용 전 카페에서 확인 |
| **[T3] 월급쟁이부자들 (월부)** | cafe.naver.com/wecando7 , weolbu.com/community | 직장인 재테크·부동산·주식 | 한국어 | 중간 | 중간(강의 판매 목적 콘텐츠가 섞임) | weolbu.com 커뮤니티와 카페 인기글 주 1~2회 | 2030 직장인 재테크 입문자의 고민과 유행(절약 챌린지, 투자 공부) → @ekke.now식 'MZ 재테크' 소재와 인터뷰 섭외처 | 유료 강의 마케팅과 연결된 글이 많음. 수익 인증은 쓰지 않음. 회원 전용 글 캡처 금지 | **재검증 부분 확인(09-30)**: 카페 wecando7(보라디스 '2014-09-19 개설')과 weolbu.com/community 확인. 회원 약 35만은 **2022년 자료**(검색 요약)라 지금은 다를 수 있음 |
| **[T3] 디시인사이드 미국 주식 마이너 갤러리** | gall.dcinside.com/mgallery/board/lists/?id=stockus (관련: 해외주식 마이너 갤러리 ?id=tenbagger, 미국 주식 장투 마이너 갤러리 m.dcinside.com/board/usstock) | 미국 주식·빅테크 실적·개인투자자 심리 | 한국어 | 매우 빠름 | 낮음 | 실적 발표 시즌에 개념글 확인 | 엔비디아·빅테크 실적과 AI 버블 논쟁에 대한 한국 개인투자자의 체감 → @ekke.now '돈' 콘텐츠의 분위기 온도계 | 종목 선동, 루머, 욕설. 투자 정보로 인용하지 않고 '분위기'만 전함. 특정 종목 추천으로 읽히면 유사투자자문 논란 | **재검증 확인(09-30)**: stockus 갤러리 게시글과 나무위키 문서 확인(나무위키: 흥한 갤러리 300위 이내). **1차에서 '근거 없음'으로 뺀 해외주식 갤러리(id=tenbagger)도 목록 페이지와 나무위키 문서가 있어 보조 주소로 되살림**(활동량 미검증) |
| **[추가][T3] 리멤버 커뮤니티** | community.rememberapp.co.kr (메인 community.rememberapp.co.kr/main) | 직장인 업계·커리어 토론(명함 인증 기반) | 한국어 | 중간 | 중상 | 주 1~2회 인기글 | 블라인드보다 실명에 가까운 현직자 시각. 업계별 AI 도입, 이직, 연봉 협상 흐름 → @bizucafe식 커리어 코멘트 소재 | 개인 의견이라 일반화하지 않음. 캡처 금지 | **재검증 부분 확인(09-30)**: 주소 확인. 이직·커리어, 회사생활, 재테크, 영업 같은 업계별·주제별 게시판이 검색됨. 2026년 활동량은 미검증 |
| **[추가][T3] 아이보스** | i-boss.co.kr | 마케팅·광고·브랜딩 실무 | 한국어 | 중간 | 중간 | 주 1회 인기글·뉴스 | 브랜드 캠페인, 플랫폼 광고 정책(인스타·네이버) 변화를 실무자 시각으로 봄 → @bizucafe식 브랜드·마케팅 코멘트 소재. 자기 계정 운영 정보도 얻음 | 대행사 홍보 글이 섞임 | **재검증 확인(09-30)**: i-boss.co.kr에서 '2026 마케팅 캘린더', '2026년 마케팅 계획' 자유게시판 글 확인. 운영자·마케터 약 34만은 자체 소개 |

### F. 트렌드 검증 도구 (공식 데이터)

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법(RSS) | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| **[추가][T2] 네이버 데이터랩 · Google 트렌드** | datalab.naver.com , trends.google.com (한국 실시간 trends.google.com/trending?geo=KR) | 검색 관심도 | 한국어·영어 | 실시간~일간 | 높음 | 커뮤니티에서 뜬 소재를 올리기 전에 검색량 추이를 확인 | '커뮤니티에서만 뜨거운가, 대중도 찾는가'를 판단. 검색량 그래프를 직접 그린 데이터 카드(예: '검색량으로 본 OO 열풍')는 오리지널 콘텐츠가 됨 | 절대 검색량이 아니라 상대 지수. 기간, 기기, 연령 조건을 적음 | **재검증 부분 확인(09-30)**: Google 트렌드 'Trending Now' 한국 페이지(trending?geo=KR)와 공식 도움말 확인. Trending Now는 대략적인 검색량도 보여 줌. **네이버 데이터랩은 재검증 안 함**(미검증, 존재 확실) |

---

## 3. 우선순위 Top 10

> `newsletters_media.md`의 Top 10(The Rundown, 공식 뉴스룸, Techmeme, GeekNews 등)과 **겹치지 않게**, 커뮤니티에서만 얻을 수 있는 신호를 기준으로 골랐습니다. GeekNews와 Techmeme은 그 파일의 Top 10에 이미 있어 여기서는 뺐습니다.

| 순위 | 소스 | 왜 |
|---|---|---|
| 1 | **r/LocalLLaMA** | 오픈 모델(중국 모델 포함)의 출시와 유출에 대한 **1차 반응**이 가장 빨리 모입니다. 직접 돌려 본 후기가 바로 붙어 '진짜 쓸 만한가'를 판단할 수 있습니다. 2026-09에도 활동이 확인된 대형 서브레딧(83.2만)입니다. |
| 2 | **Hacker News** (hnrss 피드) | 테크·스타트업 사건에 **업계인 댓글**이 붙는 곳입니다. `points=100` 피드로 잡음을 거르면 @romaan.mag식 해설과 @bizucafe식 코멘트의 재료가 매일 나옵니다. |
| 3 | **디시 특이점이 온다 갤러리** | 해외 AI 발표가 **한국어로 가장 빨리** 번역되고, 한국 헤비유저의 반응 온도를 볼 수 있습니다. 해외 소식을 한국 독자에게 어떻게 설명할지 가늠하는 기준이 됩니다. 나무위키에 따르면 2026년 코딩 글을 분리한 뒤 AI 코딩·도구 활용 글은 **AI 활용 마이너 갤러리**로 옮겨 갔으니 둘을 같이 봅니다(재검증 09-30). |
| 4 | **r/ChatGPT + r/aivideo** | @ai_freaks.kr의 '재밌는 AI'와 '이게 AI라고?' 릴스 소재가 가장 많이 나옵니다. 크리에이터 허락을 받으면 오리지널 컴필레이션이 됩니다. |
| 5 | **Hugging Face Papers + 트렌딩 모델·Spaces** | 연구 소재(Papers)와 직접 써 볼 수 있는 데모(Spaces)를 한곳에서 봅니다. **'직접 써봤다'**는 인스타 독창성 정책에서도 유리한 오리지널 콘텐츠입니다. |
| 6 | **에펨코리아 포텐 터짐** | 한국 대중에게 **실제로 먹히는** AI·돈 소재를 재는 레이더입니다. AI 호러 영상 사례처럼 @ai_freaks.kr 추정 게시물과 같은 시기에 같은 소재가 떴습니다(`source-tracing.md`). |
| 7 | **더쿠 HOT** | 소비·식품·브랜드 밈이 가장 빨리 퍼지는 곳 가운데 하나입니다. @ekke.now식 소비 트렌드 카드의 초기 신호입니다. |
| 8 | **뽐뿌 재테크포럼** | 특판 적금, 카드, 금리 변경 같은 **바로 쓸 수 있는 돈 정보**가 금융사 발표 직후 올라옵니다. 공식 공지로 확인만 하면 '이번 주 돈 되는 정보' 카드가 됩니다. |
| 9 | **블라인드 토픽 베스트** | 연봉, 성과급, 구조조정, 사내 AI 도입 분위기가 기사보다 먼저 드러납니다. @bizucafe와 @ekke.now의 '요즘 직장인' 소재입니다. 명예훼손 위험이 커서 **반드시 기사나 공식 입장으로 교차 확인**합니다. |
| 10 | **GitHub Trending** | 바이럴 오픈소스가 비즈니스 뉴스로 번지는 흐름을 가장 일찍 보여 줍니다(OpenClaw → 개발자 OpenAI 합류, 2026-02). 다른 한국 큐레이터가 덜 보는 곳이라 선점 효과가 있습니다. |

**Top 10 다음으로 볼 것**
- **숫자 카드용**: Arena·Artificial Analysis, OpenRouter Rankings, 네이버 데이터랩·Google 트렌드
- **한국 AI 활용 사례·섭외용**: 지피터스, PyTorchKR 주간 논문 모음, 클리앙 AI당
- **자영업·부동산 체감용**: 아프니까 사장이다(주소 재검증 확인), 부동산스터디

---

## 4. 제거한 항목과 이유

### 4-1. 삭제: 4건 + 묶음 안의 하위 주소 7개

> **재검증(09-30) 정정**: 아래 사유 가운데 '추정 주소', '근거 없음'은 일부 틀렸습니다.
> - 특이점 미니 갤러리, AI 활용 갤러리(ai_utilize), Ai 창작 갤러리(aicreate), 해외주식 갤러리(tenbagger), 클리앙 AI그림당(cm_aigurim)은 **모두 실제로 있습니다.**
> - 그중 **AI 활용 갤러리는 행으로 되살렸고**, 해외주식 갤러리는 미국 주식 행에 보조 주소로 넣었습니다. 나머지는 우선순위 때문에 계속 뺍니다.
> - 인공지능(AI) `?id=235711`, AI그림 `?id=al1s`, AI `aigallery`는 이번에도 검색하지 않아 **미검증**입니다.

| 항목 | 이유 |
|---|---|
| **디시인사이드 특이점 미니 갤러리** (`gall.dcinside.com/mini/board/lists/?id=thesingularity`) | 근거가 나무위키 스니펫 하나뿐입니다. 주소가 본 갤러리 ID(`thesingularity`)를 `mini` 경로에 그대로 붙인 형태라 **추정으로 만든 주소일 가능성**이 있습니다. 개설 날짜(2026-02-27)도 확인하지 못했습니다. 초안 스스로 '신생이라 활동량이 들쭉날쭉하다'고 적었고, 본 갤러리를 보면 충분합니다. **재검증: '특이점 미니 갤러리'(m.dcinside.com/mini/thesingularity)가 실제로 있음. 추정 주소라는 판단은 틀림. 활동량 때문에 계속 빼되 특갤 행에 관련 주소로 적음** |
| **AI 코리아 커뮤니티** (aikoreacommunity.com, news.aikoreacommunity.com) | 근거가 주소 자체뿐이고, 운영 주체와 규모를 모릅니다. 초안도 '2026년 활동량은 미확인'이라고 적었습니다. 핵심 채널이 **오픈채팅(비공개 대화)**이라 인용할 수 없고, 매일 모니터링할 가치가 낮습니다. |
| **TensorFlow KR (페이스북 그룹)** | 초안도 `verified: false`로 적었습니다. 2025~2026 활동 근거가 없고, 로그인이 필요한 페이스북 그룹이라 모니터링 효율이 낮습니다. 한국 AI 연구 소식은 PyTorchKR 주간 논문 모음과 GeekNews가 대신합니다. |
| **Threads 한국 AI·비즈 서클** (@choi.openai, @gptersorg, @bizucafe) | 뉴스 원천이 아니라 **경쟁 큐레이터**입니다(`x_ai.md`도 CHOI를 '뉴스 소스가 아니라 경쟁 계정'으로 분리). 시드 계정에 벤치마크 대상인 @bizucafe가 들어 있어 순환 참조입니다. 큐레이터끼리 재인용하면서 출처가 빠지는 문제도 초안이 직접 지적했습니다. → **부록 '벤치마크'로 옮김**. @gptersorg는 C의 지피터스 행에 남김 |
| 디시 AI 갤러리 묶음 중 **인공지능(AI) `?id=235711`, AI 활용 `m.dcinside.com/board/ai_utilize`, AI그림 `?id=al1s`, Ai 창작 `?id=aicreate`, AI `m.dcinside.com/board/aigallery`** | 5개 모두 근거 URL이 없습니다. 숫자 ID, 모바일·PC 주소 형식이 뒤섞여 있어 확인 없이 쓰기 어렵습니다. 근거가 있는 **챗지피티 갤러리만** 남겼습니다. **재검증: `ai_utilize`(AI 활용 마이너 갤러리)와 `aicreate`(Ai 창작 마이너 갤러리)는 실제로 있음 → ai_utilize는 C에 행으로 되살림. 235711, al1s, aigallery는 미검증** |
| **디시 해외주식 갤러리 (`?id=tenbagger`)** | 근거가 없습니다. 초안의 나무위키 근거는 '미국 주식 마이너 갤러리' 문서라 이 주소를 뒷받침하지 않습니다. **재검증: 목록 페이지와 나무위키 '해외주식 마이너 갤러리' 문서가 있어 실제로 있음 → stockus 행에 보조 주소로 되살림** |
| **클리앙 AI그림당 (`cm_aigurim`)** | 근거가 주소 자체뿐이고, AI 이미지 소재는 r/StableDiffusion, r/aiArt, 아카라이브가 이미 다룹니다. **재검증: 게시판이 실제로 있음(이용 규칙 공지 등). 중복이라 계속 뺌** |

### 4-2. 합친 것: 2건 (삭제 아님)

| 항목 | 합친 곳 | 이유 |
|---|---|---|
| **Hugging Face Trending Papers (Papers with Code 후속)** | Hugging Face Papers (Daily + Trending) | 같은 사이트의 두 탭입니다. `newsletters_media.md`도 한 항목으로 다룹니다. |
| **Future Tools 뉴스** | AI 툴 디렉터리 (Future Tools, TAAFT, Futurepedia) | 역할(대중용 AI 툴·뉴스 모음)이 같고, futuretools.io/news의 2026년 활동을 확인하지 못했습니다. |

### 4-3. 틀렸거나 근거가 없어 고친 서술

| 항목 | 초안 | 수정 | 근거 |
|---|---|---|---|
| LMArena | lmarena.ai | **arena.ai**(2026-01-28 개명), 변경 로그 주소 추가 | `newsletters_media.md`, `x_ai.md` |
| LMArena · AA | 근거 tech-insider.org '2026-09 비교 기사' | 근거에서 뺌. 서술을 일반적인 차이로 바꿈 | 출처 신뢰도를 판단할 수 없음 |
| OpenRouter | '2026-09-21 주 DeepSeek가 요청의 24.4%' | 수치를 뺌. '지표 단위를 페이지에서 확인' 추가 | 재확인하지 못했고, 순위표가 요청이 아니라 토큰 기준일 수 있음. **재검증: 스니펫상 단위는 '텍스트 요청 점유율'이 맞았음. 다만 주간 스냅숏이라 표에서는 계속 뺌** |
| Techmeme | 'Feeder에 river 피드 등록' | river 페이지만 남김. RSS는 미검증 표기 | `newsletters_media.md`도 RSS 주소를 미검증으로 둠 |
| Product Hunt | 카테고리 피드 `/feed?category=[slug]` | 뺌 | 초안 스스로 '슬러그 확인 필요'로 적음 |
| GeekNews | '광고가 없다' | 뺌. RSS 설정 안내 주소 추가 | 근거 없음. RSS 안내는 `newsletters_media.md` |
| 특이점 갤러리 | 나무위키 서술을 사실로 적음 | '나무위키 서술, 미검증'으로 표기 | 나무위키 단일 출처 |
| 에펨코리아 | '나무위키 실검에도 자주 반영' | 뺌 | 근거 없음 |
| 더쿠 | 카테고리 번호 24788, HOT 기준 '댓글 56개·조회 2,050' | 뺌 | 너무 구체적인데 재확인하지 못함 |
| 아카라이브 | 5개 채널을 모두 검증된 것으로 표기 | ai101만 초안 근거, 나머지는 미검증. aiart·characterai는 브랜드 안전상 참고만 | 근거 URL이 ai101뿐 |
| 디스콰이엇 | '운영사 임직원 6명' | 뺌. '2025~2026 활동 미확인' 추가 | 소스 판단과 무관한 정보 |
| 커리어리 | 활동량 미확인을 주의 칸에만 적음 | T3로 내리고 '[활동 확인 필요]' 명시 | 2024-09 이후 근거 없음 |
| r/personalfinance | '+ r/Money' | 뺌 | 설명과 근거가 없음 |
| Reddit 전반 | 'Reddit의 .rss 엔드포인트는 2026년에도 작동' | '2026년 작동 여부 미검증, 막히면 대안' | 근거를 찾지 못함. **재검증: 2026년 제3자 안내글에서 작동 확인 → 1-3 문구 갱신** |
| Reddit 구독자 수 | 수치만 적음 | '기준일 불명' 명시 | GummySearch 스니펫에 날짜가 없음. **재검증: 날짜가 있는 수치로 바꿀 수 있는 것은 바꿈. GummySearch는 종료 중** |
| PyTorchKR | '.rss를 붙이면 피드가 나온다(미검증)' | 정확한 형식 `discuss.pytorch.kr/c/news/14.rss`로 적고 미검증 유지 | Discourse 표준 형식 |

---

## 5. 출처

**이번 단계의 검색**
- 1차 검증: WebSearch 3회 시도, **모두 거부**(워크플로 공유 한도 200회 소진). 1차에서 새로 확인한 사실은 없습니다.
- 재검증(2026-09-30): WebSearch 54회. 근거 URL은 6-3에 있습니다.

**초안이 남긴 근거 URL** (초안 작성 때 검색 스니펫으로 확인된 것. 이번에 다시 열어 보지 않음)
- Hacker News RSS: https://hnrss.org/
- Techmeme: https://feeder.co/discover/09288434f9/techmeme-com
- Product Hunt: https://www.producthunt.com/leaderboard/daily/2026/4/1
- Hugging Face Papers: https://huggingface.co/papers , Papers with Code 종료: https://www.coursera.org/articles/papers-with-code
- HF 트렌딩 Spaces(제3자 스크레이퍼 예시): https://apify.com/logiover/huggingface-hub-intelligence-scraper/examples/hf-trending-spaces-weekly
- GitHub Trending RSS: https://mshibanami.github.io/GitHubTrendingRSS/
- AINews: https://news.smol.ai/
- Futurepedia: https://www.futurepedia.io/ , Future Tools: https://futuretools.io/news
- OpenRouter: https://openrouter.ai/rankings
- Reddit 규모: https://gummysearch.com/r/LocalLLaMA/ , https://gummysearch.com/r/singularity/ , https://gummysearch.com/r/OpenAI/ , https://gummysearch.com/r/ChatGPT/ , https://gummysearch.com/r/ClaudeAI/ , https://gummysearch.com/r/aivideo/ , https://gummysearch.com/r/artificial/ , https://gummysearch.com/r/Entrepreneur/ , https://gummysearch.com/r/personalfinance/ , https://prowlo.com/tools/subreddit-stats/stablediffusion
- GeekNews: https://hada.io/projects/geeknews/
- 특이점이 온다 갤러리(나무위키): https://namu.wiki/w/%ED%8A%B9%EC%9D%B4%EC%A0%90%EC%9D%B4%20%EC%98%A8%EB%8B%A4%20%EB%A7%88%EC%9D%B4%EB%84%88%20%EA%B0%A4%EB%9F%AC%EB%A6%AC
- 디시 챗지피티 갤러리: https://gall.dcinside.com/mgallery/board/lists/?id=chatgpt
- 아카라이브 AI 정보 채널: https://arca.live/b/ai101
- 클리앙: https://www.clien.net/service/board/news , https://www.clien.net/service/board/cm_ai
- 에펨코리아(나무위키): https://namu.wiki/w/%EC%97%90%ED%8E%A8%EC%BD%94%EB%A6%AC%EC%95%84
- 더쿠: https://theqoo.net/hot?filter_mode=normal
- 뽐뿌 재테크포럼: https://www2.ppomppu.co.kr/zboard/zboard.php?id=money
- 블라인드: https://www.teamblind.com/kr/topics/%ED%86%A0%ED%94%BD-%EB%B2%A0%EC%8A%A4%ED%8A%B8
- 지피터스: https://www.gpters.org/
- 커리어리 운영사 변경(2024-09): https://www.hankyung.com/article/202409229690i
- 디스콰이엇: https://disquiet.io/
- PyTorchKR 주간 논문 모음(2026-05): https://discuss.pytorch.kr/t/2026-05-18-24-ai-ml/10365
- 미국 주식 마이너 갤러리(나무위키): https://namu.wiki/w/%EB%AF%B8%EA%B5%AD%20%EC%A3%BC%EC%8B%9D%20%EB%A7%88%EC%9D%B4%EB%84%88%20%EA%B0%A4%EB%9F%AC%EB%A6%AC
- 부동산스터디 규모: https://borathis.com/entry/%EB%B6%80%EB%8F%99%EC%82%B0-%EC%8A%A4%ED%84%B0%EB%94%94-%EB%84%A4%EC%9D%B4%EB%B2%84-%EC%B9%B4%ED%8E%98
- 월급쟁이부자들: https://weolbu.com/community

**교차 대조한 같은 세션 파일**
- `newsletters_media.md`: Arena 개명(2026-01-28, https://arena.ai/blog/lmarena-is-now-arena), Papers with Code 종료(2025-07-24), AINews 2026-02-20호, GeekNews RSS 안내(https://hada.io/blog/geeknews-feed-rss/), Techmeme, Future Tools
- `x_ai.md`: @GeekNewsHada, @GeekNewsBot, @HuggingPapers, CHOI를 경쟁 계정으로 분리한 판단
- `source-tracing.md`: 에펨코리아 포텐 글(https://www.fmkorea.com/best/9789775469), 다음 카페 여성시대 확산 사례(https://m.cafe.daum.net/subdued20club/ReHf/5155384), OpenClaw 사례, 두쫀쿠 사례
- `../landscape.md`: 지피터스 IG 1,220·Threads 2,841, CHOI Threads 29.4만, BZCF Threads 28.3K
- `../best-practices.md`: 인스타 무독창 애그리게이터 제재 확대(TechCrunch 2026-04-30)

**추가 항목** (r/MachineLearning, 네이트판, MLB파크 불펜, 아프니까 사장이다, 리멤버 커뮤니티, 아이보스, 네이버 데이터랩·Google 트렌드)
- 1차 때는 검색 한도가 소진돼 근거 URL이 없었습니다.
- **재검증(09-30)에서 주소와 존재를 확인한 곳**: r/MachineLearning, 네이트판, 아프니까 사장이다, 리멤버 커뮤니티, 아이보스, Google 트렌드
- **부분 확인**: MLB파크 불펜. 게시판은 있지만 주소 형식은 확인 못 했습니다.
- **미검증**: 네이버 데이터랩. 검색하지 않았습니다.
- 규모 수치는 쓰기 전에 다시 확인하세요.

---

## 6. 재검증(2026-09-30)

- **방법**: WebSearch 54회(한도 55). 검색 결과 스니펫만 보고 페이지를 직접 열지 않았습니다(WebFetch, curl, 브라우저, GitHub 도구 사용 안 함). 그래서 검색 요약이 틀렸을 수 있고, 수치는 인용 전에 원 페이지에서 다시 확인해야 합니다.
- **범위**: T1 전부와 Top 10을 먼저 봤고, 표 46행 가운데 45행을 검색으로 확인했습니다.
  - 재검증 확인 27행, 부분 확인 18행
  - 검색하지 않은 행: HF 트렌딩 모델·Spaces 1행
  - 묶음 행 안에서 검색하지 않은 곳: Futurepedia, Artificial Analysis, 네이버 데이터랩
- **새로 발견한 죽은 소스나 가짜 소스는 없습니다.** 대신 1차에서 '추정 주소'로 뺀 항목 가운데 일부가 실제로 있었습니다.

### 6-1. 바뀐 것

| # | 항목 | 판정 | 내용 |
|---|---|---|---|
| 1 | Arena 변경 로그 주소 | **수정** | arena.ai/company/leaderboard-changelog → **arena.ai/blog/leaderboard-changelog**. /company/는 제품 변경 로그(product-changelog) |
| 2 | 디시 AI 활용 마이너 갤러리(ai_utilize) | **복원(새 행)** | 1차에서 '추정 주소'로 뺐으나 실제로 있고 활동 중. 나무위키에 따르면 특갤이 코딩 글을 막은 뒤 옮겨 온 이용자가 많음 → C에 T2 행 추가, Top 10 3위 설명에 반영 |
| 3 | 디시 해외주식 갤러리(tenbagger) | **복원(보조 주소)** | '근거 없음'으로 뺐으나 목록 페이지와 나무위키 문서가 있음 → stockus 행에 관련 주소로 넣음 |
| 4 | 특이점 미니 갤러리, Ai 창작 갤러리(aicreate), 클리앙 AI그림당(cm_aigurim) | **삭제 사유 정정** | 실제로 있음. '추정 주소' 판단은 틀림. 우선순위·중복 때문에 계속 뺌 |
| 5 | Reddit 구독자 수 출처(GummySearch) | **주의 추가** | GummySearch는 Reddit API 라이선스 문제로 2025-11-30에 문을 닫았고, 2026-12-01에 완전히 종료된다고 알려짐 → 곧 사라질 출처라고 B 머리말에 적음 |
| 6 | r/LocalLLaMA, r/singularity, r/ChatGPT, r/ClaudeAI, r/StableDiffusion, r/MachineLearning | **수치에 기준일 추가** | 83.2만(09-23), 약 400만(09-17 갱신, 395만 08-13), 1,161만(08-31), 109.4만(08-23), 99.9만(08-31), 310만(08-27 갱신). r/MachineLearning은 '미검증'에서 확인으로 바꿈 |
| 7 | r/OpenAI, r/GeminiAI, r/aivideo, r/aiArt, r/artificial, r/Entrepreneur, r/personalfinance | **재확인(기준일 불명)** | 1차 수치와 같음. r/artificial은 다른 사이트가 43만으로 적어 수치가 엇갈린다고 적음 |
| 8 | Reddit RSS | **확인** | 2026년 제3자 안내글에서 `.rss` 패턴이 작동한다고 확인 → 1-3 문구 수정 |
| 9 | AINews | **활동 확인** | 2026-09-09호가 있음 → '2026-02 이후 발행 확인 못 함' 삭제 |
| 10 | OpenRouter | **정정(서술)** | '24.4%'의 단위는 스니펫상 '텍스트 요청 점유율'이 맞았음. 토큰 기준 순위도 따로 있음. 수치는 주간 스냅숏이라 계속 표에서 뺌 |
| 11 | hnrss 파라미터 | **확인** | `points`, `comments`, `q`, `count`(최대 100), `.atom`·`.jsonfeed` |
| 12 | Product Hunt 피드 | **확인** | Atom `producthunt.com/feed`, 실시간 순위 반영. '(미검증)' 삭제 |
| 13 | Techmeme RSS | **부분 확인** | feed.xml은 검색 요약에서만 확인 |
| 14 | HF Papers Trending, takara RSS | **확인** | /papers/trending, PwC 리디렉트. takara RSS는 24시간마다 갱신(존재 확인, 2026년 작동 미검증) |
| 15 | GeekNews | **보강** | RSS 주소 `news.hada.io/rss/news` 추가. 위클리 1.8만+ 확인 |
| 16 | 아카라이브 채널 4개 | **확인** | alpaca, aiart, characterai(3.2만+), aivideo 모두 있음. aivideo는 구독 1,961명으로 작다고 적음 |
| 17 | 클리앙 새로운소식 | **정정** | 공식 RSS가 없다고 적음 |
| 18 | 에펨코리아 | **수정** | /best = 최신순, /best2 = 화제순('알려짐, 미검증' 삭제) |
| 19 | 네이트판 | **확인** | pann.nate.com/talk/ranking = 톡커들의 선택 |
| 20 | 아프니까 사장이다 | **주소 확인** | cafe.naver.com/jihosoccer123. 회원 수는 출처마다 78만~195만+로 엇갈림 |
| 21 | 리멤버 커뮤니티 | **주소 확인** | community.rememberapp.co.kr('주소 미검증' 삭제) |
| 22 | 부동산스터디 | **수치 정정** | 회원 수가 104만과 163만으로 출처마다 다르다고 적음 |
| 23 | 월부 | **수치 시점** | 회원 35만은 2022년 자료 |
| 24 | 디스콰이엇 | **변동 사항** | 2025-10-30 픽셀릭(릴레잇 운영사) 인수 보도(THE VC 스니펫) |
| 25 | 커리어리 | **부분 확인** | 사이트는 운영 중(2026 채용 글). 커뮤니티 활동량은 여전히 미검증 |
| 26 | 지피터스 | **확인** | AI 스터디 24기 판매 중. 유튜브 @gpters 있음('미검증' 삭제) |
| 27 | PyTorchKR | **확인** | 2026-07-13~19 주간 논문 모음까지 확인. 08~09월 글은 검색되지 않음 |
| 28 | 여성시대 | **규모 추가** | 회원 약 72만(2026-03, 검색 요약) |
| 29 | 블라인드, 뽐뿌, 더쿠, 아이보스, stockus, Future Tools, TAAFT, Google 트렌드 | **확인** | 주소와 2026년 활동(또는 페이지 존재) 확인. TAAFT 250만+, Future Tools 25만+, 아이보스 34만은 자체 주장 |

### 6-2. 여전히 미검증

- **표 안**: HF 트렌딩 모델·Spaces의 정렬 URL, Futurepedia, Artificial Analysis, 네이버 데이터랩, 뽐뿌 핫딜 게시판 주소, MLB파크 불펜 주소 형식, PyTorchKR RSS 주소, 클리앙 AI당 활동 시기, 아카라이브 채널의 2026년 활동
- **삭제 목록 안**: 디시 `?id=235711`·`al1s`·`aigallery`, AI 코리아 커뮤니티, TensorFlow KR

### 6-3. 재검증 근거 URL (검색 스니펫)

- GummySearch 종료: https://gummysearch.com/docs/gummysearch-is-now-closed-6533h , https://gummysearch.com/final-chapter/ , https://prowlo.com/blog/why-gummysearch-shut-down
- Reddit RSS 2026: https://www.wprssaggregator.com/reddit-rss-feed/
- Reddit 규모: https://gummysearch.com/r/LocalLLaMA/ , https://gummysearch.com/r/singularity/ , https://prowlo.com/tools/subreddit-stats/singularity , https://prowlo.com/tools/subreddit-stats/chatgpt , https://redditli.st/subreddit/ClaudeAI , https://prowlo.com/tools/subreddit-stats/claudeai , https://reddapi.dev/subreddits/geminiai/insights , https://prowlo.com/tools/subreddit-stats/stablediffusion , https://gummysearch.com/r/MachineLearning/ , https://gummysearch.com/r/aivideo/ , https://gummysearch.com/r/aiArt/ , https://gummysearch.com/r/artificial/ , https://reddgrow.ai/tools/subreddit-stats/artificial/ , https://gummysearch.com/r/Entrepreneur/ , https://gummysearch.com/r/personalfinance/ , https://gummysearch.com/r/OpenAI/
- hnrss: https://hnrss.org/
- Techmeme 피드: https://rss.feedspot.com/tech_news_rss_feeds/ , https://feeder.co/discover/71b065f711/techmeme-com
- Product Hunt 피드: https://finder.wprssaggregator.com/rss-feeds/platform/product-hunt , https://help.producthunt.com/en/articles/484970-does-product-hunt-have-an-rss-feed
- HF Papers: https://huggingface.co/papers/trending , https://huggingface.co/changelog/trending-papers , https://github.com/takara-ai/papers-api (검색 스니펫만 인용)
- GitHub Trending RSS: https://mshibanami.github.io/GitHubTrendingRSS/ , https://github.com/mshibanami/GitHubTrendingRSS (검색 스니펫만 인용)
- AINews: https://news.smol.ai/issues/26-09-09-not-much/
- Arena: https://arena.ai/blog/leaderboard-changelog , https://arena.ai/company/product-changelog
- OpenRouter: https://openrouter.ai/rankings , https://tokenmaxxing.com/openrouter-rankings
- Future Tools: https://futuretools.io/news , TAAFT: https://newsletter.theresanaiforthat.com/ , https://www.passionfroot.me/taaft
- GeekNews: https://hada.io/blog/geeknews-feed-rss/ , https://hada.io/projects/geeknews/
- 디시: https://gall.dcinside.com/mgallery/board/lists/?id=thesingularity , https://m.dcinside.com/mini/thesingularity , https://m.dcinside.com/board/ai_utilize , https://namu.wiki/w/AI%20%ED%99%9C%EC%9A%A9%20%EB%A7%88%EC%9D%B4%EB%84%88%20%EA%B0%A4%EB%9F%AC%EB%A6%AC , https://gall.dcinside.com/mgallery/board/lists/?id=aicreate , https://m.dcinside.com/board/chatgpt/99378 , https://gall.dcinside.com/mgallery/board/lists/?id=tenbagger , https://m.dcinside.com/board/stockus?recommend=1&page=4
- 아카라이브: https://arca.live/b/ai101 , https://arca.live/b/alpaca , https://arca.live/b/aiart , https://arca.live/b/characterai , https://arca.live/b/aivideo
- 클리앙: https://www.clien.net/service/board/cm_ai , https://www.clien.net/service/board/cm_aigurim , https://www.clien.net/service/board/lecture/11373731 (새로운소식 RSS 관련 글)
- 지피터스: https://www.gpters.org/ai-study-list , https://www.youtube.com/@gpters
- PyTorchKR: https://discuss.pytorch.kr/t/2026-07-13-19-ai-ml/11328
- 디스콰이엇: https://thevc.kr/disquiet , 커리어리: https://careerly.co.kr/job/704385
- 에펨코리아: https://www.fmkorea.com/best , https://www.fmkorea.com/best2
- 더쿠: https://theqoo.net/hot , https://theqoo.net/hot/4215796859
- 네이트판: https://pann.nate.com/talk/ranking
- MLB파크: https://ko.wikipedia.org/wiki/MLBPARK
- 여성시대: https://namu.wiki/w/%EC%97%AC%EC%84%B1%EC%8B%9C%EB%8C%80
- 뽐뿌: https://www2.ppomppu.co.kr/zboard/zboard.php?id=money , https://www.ppomppu.co.kr/zboard/zboard.php?id=stock
- 블라인드: https://www.teamblind.com/kr/topics/%ED%86%A0%ED%94%BD-%EB%B2%A0%EC%8A%A4%ED%8A%B8
- 아프니까 사장이다: https://www.make2t.kr/2026/09/apeunikka-sajangida-naver-cafe.html , https://aspsajang.com/ , https://borathis.com/entry/%EC%95%84%ED%94%84%EB%8B%88%EA%B9%8C-%EC%82%AC%EC%9E%A5%EC%9D%B4%EB%8B%A4
- 부동산스터디: https://www.facebook.com/jaegebal/ , https://borathis.com/entry/%EB%B6%80%EB%8F%99%EC%82%B0-%EC%8A%A4%ED%84%B0%EB%94%94-%EB%84%A4%EC%9D%B4%EB%B2%84-%EC%B9%B4%ED%8E%98
- 월부: https://borathis.com/entry/%EC%9B%94%EA%B8%89%EC%9F%81%EC%9D%B4-%EB%B6%80%EC%9E%90%EB%93%A4-%EB%84%A4%EC%9D%B4%EB%B2%84-%EC%B9%B4%ED%8E%98
- 리멤버: https://community.rememberapp.co.kr/main
- 아이보스: https://www.i-boss.co.kr/ab-qletter-925927
- Google 트렌드: https://trends.google.com/trending?geo=KR , https://support.google.com/trends/answer/3076011?hl=en

---

## 부록. 벤치마크 (뉴스 원천은 아님)

| 이름 | 주소 | 볼 것 | 근거 |
|---|---|---|---|
| CHOI | threads.com/@choi.openai | 해외 AI 뉴스가 한국 Threads에서 어떤 말투와 속도로 퍼지는지, 어떤 주제가 저장·공유를 부르는지 | `../landscape.md`, `x_ai.md`: Threads 29.4만 |
| AI TREND KOREA (에트매거진) | threads.com/@ai.trend.kr , IG @ai.trend.kr | 같은 '한국 AI 매거진형' 계정의 주제 선택과 커버 디자인 | `x_ai.md`, `../landscape.md` |
| BZCF | threads.com/@bizucafe | 모델 계정 자체. 원천은 `source-tracing.md`에 역추적돼 있음 | `source-tracing.md` |

- 큐레이터끼리 재인용하면 출처가 빠집니다. Threads에서는 '출처표기 댓글 하나 남기고 가져가는 큐레이션 채널'에 대한 비판도 확인됐습니다(`source-tracing.md`).
- 여기서 화제가 된 글은 **원문(X, 공식 블로그, 원 기사)까지 거슬러 올라가** 그것을 출처로 씁니다.
