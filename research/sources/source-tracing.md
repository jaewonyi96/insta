# 소스 역추적 리포트: 4개 한국형 "매거진 큐레이션" 계정은 어디서 이야기를 가져오나

- 조사일: 2026-09-30
- 대상: @ai_freaks.kr (AI Freaks), @romaan.mag (로만), @bizucafe (BZCF | 비즈까페), @ekke.now (에크케)
- 목적: 각 계정 게시물의 **원본 소스**(X, 커뮤니티, 공시, 보도자료, 해외 매체, 유튜브 등)를 찾아 매일 모니터링할 소스 목록을 만든다.

---

## 1. 방법

1. **게시물 수집**: 인스타그램·X·레딧 직접 접속은 네트워크 정책상 막혀 있어서 **웹 검색 결과의 제목과 스니펫만** 사용했다. `site:instagram.com`, `site:threads.com/@계정`, 계정 표시명과 바이오 문구로 검색했다. Threads 게시물은 URL 슬러그에 본문 앞부분이 들어 있어서 캡션을 상당 부분 복원할 수 있었다.
2. **게시 시각 복원**: 인스타그램과 Threads의 게시물 코드(shortcode)를 미디어 ID로 바꾸고 상위 비트에서 타임스탬프를 계산했다(`ID >> 23` + 2011-08-24 epoch). 날짜를 이미 아는 게시물 두 개로 확인했다. BZCF의 Lovable 글(2025-07-18)과 캘러닉 서한 글(2026-03-15) 모두 검색 결과의 날짜와 맞았다. 표의 게시일은 이렇게 계산한 **UTC 날짜**다.
3. **원본 역추적**: 캡션의 고유명사·수치·인용구로 영문과 국문을 다시 검색했다. 원본의 발행일과 비교해 **시차**를 추정했다.
4. **신뢰도 기준**
   - 높음: 캡션이 출처를 직접 밝혔거나, 고유 수치나 인용이 원문과 정확히 일치하고 날짜도 맞는 경우
   - 중간: 주제와 날짜는 맞지만 구체적 원문(기사 URL)을 특정하지 못한 경우
   - 낮음: 정황 추정이거나, 게시물이 해당 계정의 것인지부터 확인되지 않은 경우
5. 검색은 이 세션의 한도인 200회를 모두 사용했다. 그중 이 조사에 쓴 것은 약 60회다. 한도를 다 써서 마지막 몇 개의 교차검증은 하지 못했다(§6 한계 참고).

---

## 2. 계정별 추적 표

### 2-1. BZCF | 비즈까페 (@bizucafe): 해외 비즈니스 원문을 번역하고 발췌한 뒤 코멘트를 붙이는 계정

프로필 규모(검색 스니펫 기준): 인스타그램 약 7만 팔로워, 게시물 242개. Threads 2.8만 팔로워. 텔레그램 `@bzcftel` 약 9,870명. 유튜브 `@B_ZCF`(bzcf.io에 "구독자 30만 명" 글이 있음). 네이버 블로그 `blog.naver.com/bizucafe`, 웹 `bzcf.io`, 뉴스레터(연락처 businessnewsdaily@naver.com)도 운영한다. 인스타그램 게시물은 검색 색인이 거의 없어서, 같은 운영자가 쓰는 **Threads·텔레그램·블로그**로 추적했다.

| 게시물 (채널·게시일 UTC) | 원본 추정 소스 | 링크 | 시차 | 가공 방식 | 신뢰도 |
|---|---|---|---|---|---|
| "또 하나의 AI유니콘 등장. 바이브 코딩 서비스… 1. 스웨덴 바이브코딩 스타트업 lovable…" (Threads, 2025-07-18) | Bloomberg 단독 "Swedish Vibe Coding Firm Lovable Hits $1.8 Billion Valuation"과 Lovable 공식 블로그의 $200M 시리즈A 발표 | [게시물](https://www.threads.com/@bizucafe/post/DMQRuMXvZ8S) · [Bloomberg](https://www.bloomberg.com/news/articles/2025-07-17/swedish-vibe-coding-firm-lovable-hits-1-8-billion-valuation) · [Lovable](https://lovable.dev/blog/200m-series-a-fundraise) | 약 1일 | 번호 매긴 요약과 짧은 해석("서로 밀어주고 끌어주고") | 높음 |
| "OpenAI가 AMD와 새로운 형태의 칩 공급 계약을 체결했다… 결국 AMD는 우리 생태계를 함께 키우면 그 성장의 과실을 함께 나눈다는 메시지" (Threads, 2025-10-07 04:45) | OpenAI·AMD 공동 보도자료(6GW, 워런트 1억6천만 주), 2025-10-06 | [게시물](https://www.threads.com/@bizucafe/post/DPfr7LuD9FH) · [OpenAI](https://openai.com/index/openai-amd-strategic-partnership/) · [AMD](https://newsroom.amd.com/news/amd-and-openai-announce-strategic-partnership-to-d/) · [CNBC](https://www.cnbc.com/2025/10/06/openai-amd-chip-deal-ai.html) | 1일 미만 | 계약 구조를 요약한 뒤 "메시지" 중심으로 해석 | 높음 |
| "커서(CURSOR), 시가총액은 $10B… 모두다 MIT 2022년 졸업생들. 창업자들 나이는 20…" (Threads, 2025-04-19) | Bloomberg "AI Startup Anysphere in Talks for Close to $10 Billion Valuation"(2025-03-07)과 TechCrunch 후속 보도 | [게시물](https://www.threads.com/@bizucafe/post/DIoRAnHPIXp) · [Bloomberg](https://www.bloomberg.com/news/articles/2025-03-07/ai-startup-anysphere-in-talks-for-close-to-10-billion-valuation) · [TechCrunch](https://techcrunch.com/2025/03/07/cursor-in-talks-to-raise-at-a-10b-valuation-as-ai-coding-sector-booms/) | 약 6주 | 숫자 몇 개와 창업자 스토리를 섞어 "젊은 창업자" 서사로 재구성 | 중간 (다른 후속 기사나 팟캐스트가 계기였을 수 있음) |
| "좋은 글 하나 있어 공유합니다. 아마존 창업자인 제프베조스가 대표에서 물러나며 적은 마지막 주주서한의 일부에요…" (Threads, 2025-04-22) | 베이조스의 2020년 주주서한(2021년 4월 공개) | [게시물](https://www.threads.com/@bizucafe/post/DIwHvvrvr4J) · 원문 URL은 검색으로 확인하지 못함 | 약 4년 (에버그린) | 원문 일부를 발췌 번역하고 "나다움"이라는 키워드로 코멘트 | 높음 (캡션에 출처를 명시) |
| "'이거 하는 회사들에 투자하겠다' 세계 최고 VC인 a16z 파트너들이… Big Ideas… 총 14개다. 전문: blog.naver.com/bizucafe/224116317875" (Threads, 2025-12-20) | a16z "Big Ideas 2026" Part 1~3 (a16z 뉴스레터와 X, Part 2 트윗은 2025-12-10) | [게시물](https://www.threads.com/@bizucafe/post/DSd2vb_j59-) · [a16z Part 1](https://a16z.com/newsletter/big-ideas-2026-part-1/) · [a16z X](https://x.com/a16z/status/1998788800970109250) | 약 10일 | **전문 번역은 네이버 블로그에, Threads에는 티저와 링크.** 다른 Threads 유저가 이 블로그 번역을 재인용했다([예](https://www.threads.com/@__parkjongchan/post/DSjVxRxjxo9)). | 높음 |
| "FT 기사 내용 중 일부. 트럼프의 집권 이후, 부자는 더 부유해지고… 전형적인 'K자형' 양극화…" (Threads, 2025-12-24) | Financial Times의 K자형 경제 기사. 정확한 기사는 특정하지 못했다. 후보는 FT 2025-11-09 "Gulf between rich and poor risks US downturn, Fed official warns"이고, 같은 시기 Fortune·CNBC도 K자형 경제를 보도했다. | [게시물](https://www.threads.com/@bizucafe/post/DSphV9qD7SN) · [Fortune 참고](https://fortune.com/2025/12/01/what-is-k-shaped-economy-inequality-inflation-rich-poor) | 불명 (수일~수주) | 유료 기사의 **요지를 번역하고 요약** | 중간 (매체명은 명시, 기사는 미특정) |
| "<마이클 블룸버그 회장 조언> 1. 커리어 초반에는 돈에 집착하지 마라… 나는 80대인데…" (Threads, 2026-01-24) | 블룸버그 회장의 영상 인터뷰나 연설로 추정. 원본은 찾지 못했다. | [게시물](https://www.threads.com/@bizucafe/post/DT5NRSrD9Od) | 불명 | 1인칭 발언을 번호 목록으로 번역 | 낮음 |
| "오픈클로 개발자인 피터는 OpenAI로. 클로드(앤트로픽)은 아쉬울것 같기도 하네요… 에이전트 누가누가 잘 만드느냐에…" (Threads, 2026-02-16 02:33) | 샘 올트먼의 X 발표와 피터 스타인버거의 블로그(2026-02-15) | [게시물](https://www.threads.com/@bizucafe/post/DUzVu-Jjwmt) · [steipete.me](https://steipete.me/posts/2026/openclaw) · [TechCrunch](https://techcrunch.com/2026/02/15/openclaw-creator-peter-steinberger-joins-openai/) | 1일 미만 | 사실 한 줄에 업계 관전평을 붙임 | 높음 |
| "블랙스톤 COO 조나단 그레이 인터뷰 중 좋았던 것 3가지… AUM 약 1조 3,000억 달러…" (Threads, 2026-02-28) | 조나단 그레이의 인터뷰(팟캐스트나 영상으로 추정). 원본은 찾지 못했다. | [게시물](https://www.threads.com/@bizucafe/post/DVTQCG2jxIB) | 불명 | 인터뷰에서 3가지를 골라 번역하고 배경 수치를 덧붙임 | 낮음 |
| "그의 서한 중 가장 인상깊었던 부분" (트래비스 캘러닉 복귀) (Threads, 2026-03-15) | 캘러닉의 1,600단어 매니페스토 "I never left"와 신사 Atoms 발표(2026-03-13) | [게시물](https://www.threads.com/@bizucafe/post/DV6EtDoj7Gp) · [TechCrunch](https://techcrunch.com/2026/03/13/travis-kalanick-launches-a-new-company-called-atoms-focused-on-robotics/) · [CNBC](https://www.cnbc.com/2026/03/13/uber-ex-ceo-kalanick-rebrands-latest-venture-atoms-move-into-robotics.html) · [a16z](https://a16z.com/travis-is-back/) | 약 2일 | 창업자 서한을 발췌 번역하고 인물사(우버 창업과 퇴출)를 붙임 | 높음 |
| bzcf.io "AI 발전속도를 조절해야 합니다" (다리오 아모데이, 2026-09-13 업데이트) | 아모데이 에세이 "We Must Pace the Frontier"(개인 사이트, 2026-09-12) | [bzcf.io](https://bzcf.io/) · [Washington Post](https://www.washingtonpost.com/technology/2026/09/12/anthropic-ceo-dario-amodei-calls-ai-industry-slow-down/) · [Axios](https://www.axios.com/2026/09/12/anthropic-ai-amodei-pacing) | 약 1일 | **3,800단어 에세이 전문 번역** | 높음 |
| 텔레그램: "메타 2026년 CAPEX 가이던스 최대 1,350억 달러, 2025년 약 720억 달러 대비 거의 두 배" | Meta 2025년 4분기 실적발표(2026년 1월 말) | [텔레그램](https://t.me/s/bzcftel?before=6936) · [Meta IR](https://investor.atmeta.com/investor-news/press-release-details/2026/Meta-Reports-Fourth-Quarter-and-Full-Year-2025-Results/default.aspx) | 불명 (게시일을 확인하지 못함) | 실적 수치 한 줄 요약 | 중간 |
| "순수하게 도전하는 사람은 멋이 있다… youtube.com/shorts/…" (Threads, 2026-07-30) | 유튜브 쇼츠 (캡션에 링크가 있음) | [게시물](https://www.threads.com/@bizucafe/post/DbawmxND9sb) | 불명 | 영상 링크와 한 줄 감상 | 중간 (링크는 명시, 영상 내용은 확인 못함) |
| "도은욱 대표님 인터뷰를 했다…" (2025-08-24), "토스 공동창업자, 베이스벤처스 이태양 대표님을 모셨습니다" (2025-07-06), "고등학교를 자퇴한 크리에이터 유빈님을 만났다" (2025-10-06) | **자체 인터뷰 (오리지널 취재)** | [1](https://www.threads.com/@bizucafe/post/DNvB15DXjSs) · [2](https://www.threads.com/@bizucafe/post/DLw6XTXPid1) · [3](https://www.threads.com/@bizucafe/post/DPeLRt_D44s) | 해당 없음 | 직접 인터뷰한 뒤 유튜브·블로그에 올리고 SNS로 확산 | 높음 |

참고로 BZCF 유튜브의 제작 방식이 인터뷰로 확인됐다. "매일 정해진 담당자가 그 주에 가장 인상 깊었던 영상들을 고르고, 번역·편집·검수·썸네일 작업"을 한다고 한다([하이아웃풋클럽 인터뷰](https://blog.highoutputclub.com/hoc-membershiptalk-bzcf/)). 따라서 유튜브 콘텐츠의 원본은 **해외 영어 인터뷰와 팟캐스트 영상**이다.

### 2-2. 에크케 (@ekke.now): 공시와 트렌드를 "벌기·모으기·쓰기" 카드로 만드는 방송사 계열 매거진

프로필 규모: 인스타그램 39.1만 팔로워, 게시물 약 5,967개. Threads 1.09만 팔로워. 링크 페이지는 [litt.ly/ekke](https://litt.ly/ekke)다. **SBS 계열 스튜디오161이 제작**한다(채용공고: [링커리어](https://linkareer.com/activity/223185), [더팀스](https://www.theteams.kr/recruit_big/detail_sitemap/953003)). 채용공고는 인재상으로 "**기사에 빠르게 대응할 수 있는**" 사람을 적었다. 2025-03-28에는 패스트페이퍼 네트워크에 쿠캣, 여행에미치다, 크림과 함께 합류했다([패스트페이퍼](https://www.fastpapermag.com/2025/03/28/%EB%8B%A4%EB%93%A4%EC%A3%BC%EB%AA%A9-%EC%BF%A0%EC%BA%A3-%EC%97%AC%ED%96%89%EC%97%90%EB%AF%B8%EC%B9%98%EB%8B%A4-%ED%81%AC%EB%A6%BC-%EC%97%90%ED%81%AC%EC%BC%80%EB%8A%94-%EC%9D%B4%EC%A0%9C-%ED%8C%A8/)).

| 게시물 (채널·게시일 UTC) | 원본 추정 소스 | 링크 | 시차 | 가공 방식 | 신뢰도 |
|---|---|---|---|---|---|
| "🏭 한미반도체는 이렇게 벌고 씁니다 (*2025년 연결 기준)… 매출 5,766억 원 (3.2%↑) · 영업익 2,514억 원 (1.6%↓)… 320여 개 고객사…" (Threads, 2026-03-27) | 한미반도체 2025년 실적 공시(2월 초 잠정실적, 언론 보도 2/6~2/9)와 감사보고서. "5,766억"은 감사보고서 기사의 수치와 같다. | [게시물](https://www.threads.com/@ekke.now/post/DWYUQU7EUam) · [서울신문](https://www.seoul.co.kr/news/economy/industry/2026/02/09/20260209500234) · [CBC뉴스(감사보고서)](https://www.cbci.co.kr/news/articleView.html?idxno=560630) | 잠정실적 기준 약 7주, 감사보고서 기준 수일~수주 | **공시 수치를 카드로 만들고** 업계 맥락(TC본더 점유율, HBM)과 밈 톤 소제목("매출 많이 된다")을 붙임 | 높음 |
| "⚾ KT위즈는 이렇게 벌고 씁니다 (*2025년 기준 / 법인명: 케이티스포츠)… 5개 종목…" (Threads, 2026-05-04) | KT스포츠 2025년 감사보고서(DART). 캡션에 "법인명"을 쓴 것으로 보아 전자공시를 직접 참조한 것으로 보인다. 공시일은 확인하지 못했다. | [게시물](https://www.threads.com/@ekke.now/post/DX6atY7kYBX) · [KT스포츠 재무(캐치)](https://www.catch.co.kr/Comp/CompInfo/J08152) | 불명 (시즌 중에 맞춰 게시) | 공시 수치에 구단 스토리를 섞음. 야구 시즌 화제성에 맞춘 타이밍. | 중간 |
| "🤣 메타코미디클럽은 이렇게 벌고 씁니다 (*2025년 기준 / 법인명: 메타코미디)… 매출 291억 원 (34.1%↑) · 영업익 31억 원 · 순이익 29억 원 (96.8%↑)…" (Threads, 2026-05-20) | 메타코미디 2025년 감사보고서와, 이를 인용한 기사(뉴스에포크 2026-04-03 "매출 34%·영업익 96% 급증"). **하루 전(2026-05-19)에 다른 인스타 계정도 "메타코미디가 2025년 매출 292억 원…"을 올렸다.** | [게시물](https://www.threads.com/@ekke.now/post/DYjFz-MEbmY) · [뉴스에포크](https://newsepoch.co.kr/news/2026040300026) · [타 계정 게시물](https://www.instagram.com/p/DYhCCwUki6L/) | 첫 보도 기준 약 7주 | 공시 카드. **증감률 표기가 매체마다 달라서**(영업익 35%와 96%, 순이익 96.8%와 114%) 원문 대조가 필요하다는 점도 보여 줌. | 중간 |
| "🎅 산타 할아버지는 이렇게 벌고 씁니다 (*2024년 기준)… 주식 3,000만 달러… 1931년 코카콜라 광고…" (Instagram, 2024-12-25) | 미국 매체의 "Santa Claus' net worth" 기사(TheStreet, Stacker 신디케이션으로 2023-12 지역지에 재게재). "코카콜라 주식 가치 약 3,000만 달러" 계산이 일치한다. | [게시물](https://www.instagram.com/p/DD-v6CONtgw/) · [TheStreet](https://www.thestreet.com/personalities/santa-claus-net-worth-the-costs-of-running-santas-workshop) · [재게재 예](https://chinookobserver.com/2023/12/21/santa-claus-net-worth-the-costs-of-running-santas-workshop/) | 약 1년 (시즌마다 재활용) | 해외 이색 기사를 **원화로 환산하고 자사 시리즈 포맷으로 재구성**했다. 이후 다음 카페 '여성시대'로 퍼갔다([링크](https://m.cafe.daum.net/subdued20club/ReHf/5155384)). | 중간 |
| "원영이가 에크케의 두바이 초코 두쫀쿠임… 원영이 실물 영접한 에디터 소감… 워뇨가 내 산타다" (Threads 영상, 2025-12-25 07:35 = 16:35 KST) | 2025 SBS 가요대전(12/25, 인천 인스파이어 아레나) 레드카펫 현장과 '두쫀쿠' 열풍. 두쫀쿠는 장원영이 2025년 9월 인스타 스토리에 올린 뒤 12월에 언론으로 확산됐다. | [게시물](https://www.threads.com/@ekke.now/post/DSraGEjEqJc) · [가요대전](https://programs.sbs.co.kr/enter/2025sbsgayo/about/88180) · [네이트 12/25 두쫀쿠 기사](https://m.news.nate.com/view/20251225n17353) · [엘르](https://www.elle.co.kr/article/1894941) | 현장 당일 (본방 전), 트렌드 기준 약 3개월 | **모회사 방송 현장 취재 영상에 소비 트렌드 밈을 덧씌움** | 중간~높음 |
| "기니 오빠 꾸몽고 동그라미임 아일릿 원희 aka 기니오빠… 크리스마스에도 하루종일 티비 앞에…" (Threads 영상, 2025-12-25 06:11) | 같은 2025 SBS 가요대전의 원희·운학 '눈사람즈' 콜라보 | [게시물](https://www.threads.com/@ekke.now/post/DSrQgIAks4R) · [네이트 기사](https://news.nate.com/view/20251226n07883) | 당일 | 팬덤 밈 말투로 현장 영상에 자막 | 중간 |
| "#에크케미 💰 백만 재테크 유튜버 김짠부… 통장 잔고 0원이었다… @zzan.boo" (Threads, 2026-03-20) | **자체 인터뷰** (재테크 유튜버 김짠부) | [게시물](https://www.threads.com/@ekke.now/post/DWGdLAnkVQS) | 해당 없음 | 인터뷰 영상과 카드. 출연자 계정을 태그. | 높음 |
| "#광고 💪 답답해서 내가…" (Instagram, 2025-04-16) | 광고주 (브랜디드 콘텐츠) | [게시물](https://www.instagram.com/p/DIgGeMby4fs/) | 해당 없음 | 광고 표기 후 매거진 톤으로 제작 | 높음 (캡션에 #광고) |
| "🏠 나 혼자 벌고 쓴다…" (Instagram, 2025-06-20) | 불명. 1인가구 소비나 통계 계열로 추정한다. 통계청의 '통계로 보는 1인가구'는 보통 12월에 나와서 날짜가 맞지 않는다. | [게시물](https://www.instagram.com/p/DLHcockSHpZ/) | 불명 | 불명 | 낮음 |

### 2-3. AI Freaks (@ai_freaks.kr): 게시물 단위 추적 불가, 운영 구조로 소스를 추론

- **게시물 색인이 사실상 없다.** 프로필 페이지 외에 "AI Freaks | …" 제목으로 색인된 개별 게시물은 찾지 못했다. Threads 계정도 확인되지 않았다.
- **운영 주체**: (주)에이아이프릭스, 서울 강남구 테헤란로29길. 채용공고 기준으로 **팔로워 6.5만 명 이상, 월간 조회수 약 1,000만 회**다. **Liner, Kimi, Hailuo, Higgsfield 등 20개 이상의 글로벌 AI 기업과 협업**하고, 국내 AI 스타트업 마케팅도 대행한다([링커리어 채널](https://linkareer.com/channel/%EC%A3%BC%EC%8B%9D%ED%9A%8C%EC%82%AC-%EC%97%90%EC%9D%B4%EC%95%84%EC%9D%B4%ED%94%84%EB%A6%AD%EC%8A%A4-31262), [잡코리아](https://m.jobkorea.co.kr/Recruit/GI_Read/48820902?sc=502), [데모데이](https://demoday.co.kr/recruits/7694)). 에디터 요건은 **"기초 영어 비즈니스 커뮤니케이션", "AI 실사용 경험", "브랜디드·광고 콘텐츠 경험"**이고, "깊은 AI 지식보다 새 정보를 빨리 흡수하는 능력"을 강조한다.
- **바이오 링크**: NHN DATA 소셜비즈의 링크 페이지([link.socialbiz.ai/ai_freaks.kr](https://link.socialbiz.ai/ai_freaks.kr))에 에디터 채용 공고와 **Napkin AI 할인 링크**가 걸려 있다. 제휴·광고 수익 구조라는 뜻이다.
- 따라서 소스 유형은 이렇게 추정한다. (1) 글로벌 AI 기업의 **공식 출시·보도 자료와 협찬 브리프**, (2) 해외 AI 커뮤니티와 X에서 퍼지는 **바이럴 AI 생성 영상**, (3) 툴 사용법 직접 테스트.

| 게시물 (게시일 UTC) | 원본 추정 소스 | 링크 | 시차 | 가공 방식 | 신뢰도 |
|---|---|---|---|---|---|
| "'에어컨보다 서늘한, AI 호러 계정 모음' 👻 요즘 AI로 만든…" (Instagram, 2026-07-12). **계정 귀속은 확인하지 못했다.** "AI Freaks \| 괴짜들의 AI 매거진" 검색에서 3순위로 떴을 뿐이다. | 인스타·유튜브의 AI 호러 크리에이터 계정들. 같은 시기 에펨코리아에 "인스타에서 수집한 AI로 만든 기괴호러 영상들" 글이 있었고, 뉴스1이 "납량특집 대신 'AI호러'로 피서"를 보도했다. | [게시물](https://www.instagram.com/p/DarS0VumnmG/) · [에펨코리아](https://www.fmkorea.com/best/9789775469) · [뉴스1](https://www.news1.kr/society/incident-accident/6245823) | 불명 (여름 시즌 편승) | **크리에이터 계정을 모은 컴필레이션** | 낮음 |
| "AI 괴담 영상, 왜 계속 보게 될까? 👻 익숙한 학교, 골목길…" (Instagram, 2026-08-07). 계정 귀속을 확인하지 못했다. | AI 괴담 양산 채널 현상. 아카라이브 괴담 채널과 루리웹에서 같은 논의가 있었다. | [게시물](https://www.instagram.com/p/DbvVN6jmYUG/) · [루리웹](https://bbs.ruliweb.com/family/4526/board/300143/read/76759685) | 불명 | 현상 해설형 카드 | 낮음 |
| "디자인 전공자가 아니어도 전문가 수준의 결과물을 만들 수…" (Instagram, 2025-12-20). 계정 귀속을 확인하지 못했다. "AI Freaks 에디터 채용" 검색에서 떴다. | AI 디자인 툴 협찬이나 제휴로 추정한다(바이오의 Napkin AI 링크와 같은 계열로 봄). | [게시물](https://www.instagram.com/p/DSd86sGjXa-/) | 해당 없음 | 툴 소개형 브랜디드 | 낮음 |

### 2-4. 로만 (@romaan.mag): 추적 불가

- `romaan.mag`, `@romaan.mag`, 표시명 "로만", 바이오 문구 "AI를 소비하는 대신 이해하려는 사람들을 위한 매거진"으로 한국어와 영어로 검색했지만 **프로필과 게시물 모두 색인되지 않았다.** 결과는 동명의 해외 DJ 계정 등 무관한 것뿐이었다.
- 가능성은 세 가지다. (a) 개설한 지 얼마 안 된 소규모 계정, (b) 핸들이 바뀌었거나 철자가 다름(예: romaan_mag, roman.mag 등. 확인하지 않은 추정이다), (c) 비공개 또는 검색 차단. **사용자가 브라우저에서 직접 핸들을 확인해야 한다.**

---

## 3. 출처 표기 관행

| 계정 | 캡션에 출처 명시 | 링크 제공 | 크리에이터·인물 태그 | 광고 표기 | 요약 |
|---|---|---|---|---|---|
| BZCF | **자주 명시한다.** 매체명("FT 기사 내용 중 일부"), 원저자("제프베조스가… 적은 마지막 주주서한", "그의 서한", "블룸버그 회장 조언")를 적는다. | **전문 번역은 자사 블로그 링크로**("전문 : blog.naver.com/bizucafe/…"). 유튜브 쇼츠 원본 링크를 직접 붙인 경우도 있다. 원 기사 URL은 대체로 붙이지 않는다. | 인터뷰이는 실명으로 소개 | 브랜드 소개 글은 본문에 경위를 설명한다. 예) norda 글은 "내돈내산"이라고 밝히고 협업 경품을 안내했다([링크](https://www.threads.com/@bizucafe/post/DYTQCcgmRY_)). | "누가 한 말인지"는 밝히지만 원문 트래픽은 **자기 블로그와 유튜브로 돌린다** |
| 에크케 | 공시형 카드에 **기준 연도와 법인명**("*2025년 연결 기준", "법인명: 메타코미디")을 적는다. 매체명이나 공시 링크는 스니펫에서 확인되지 않았다. | 확인되지 않음 (인스타 캡션 특성상 링크 없음) | 인터뷰 출연자 계정 태그(@zzan.boo) | **"#광고"를 캡션 맨 앞에 표기** | 데이터 근거는 암시하지만 원문 링크는 주지 않는다 |
| AI Freaks | 게시물 단위로 확인하지 못함 | 바이오에 제휴 할인 링크(Napkin AI) | 불명 | 협업사 20곳 이상이라고 밝힘. 게시물별 표기는 확인하지 못했다. | **협찬 비중이 높다고 봐야 한다.** 광고 표기 관행은 사용자가 직접 확인해야 한다. |
| 로만 | 데이터 없음 | 데이터 없음 | 데이터 없음 | 데이터 없음 | 데이터 없음 |

업계 맥락은 다음과 같다.
- 네이트 뉴스의 기획 시리즈 "같은 이슈·비슷한 밈…인스타매거진은 무엇으로 차별화할까 [알고리즘이 만든 매체③]"(2026-09-05)는 여러 인스타 매거진이 **같은 시기에 같은 소재를 동시에 다루면서 차별성이 흐려진다**고 지적했다([링크](https://m.news.nate.com/view/20260905n07005)). 에크케 메타코미디 건에서 하루 차이로 두 계정이 같은 주제를 올린 것이 그 예다.
- Threads에서는 "출처표기 해주겠다는 댓글 하나 달랑 남기고 가져가서 큐레이션하는 채널"에 대한 비판이 나온다([링크](https://www.threads.com/@eksqlsj/post/DYoiUGjkSHO)).
- 참고 기준으로, 한국신문윤리위원회는 언론사 대상으로 'SNS 등 저작물 출처 표기 가이드라인'을 시행했다([기자협회보](https://journalist.or.kr/m/m_article.html?no=56779)).

---

## 4. 패턴 요약: 계정별로 어떤 소스가 주를 이루나

| 계정 | 주 소스 유형 (추적 건수 기준) | 대표 시차 | 주 가공 방식 |
|---|---|---|---|
| **BZCF** | ① **해외 1차 발표물**: 창업자 서한과 매니페스토, CEO 에세이, 공동 보도자료, 주주서한, VC 전망 보고서(a16z) — 6건. ② **해외 경제지 단독과 속보**: Bloomberg, FT, TechCrunch, CNBC — 3건. ③ **영어 인터뷰·연설 영상** — 2~3건. ④ **자체 인터뷰** — 3건 이상. | 속보성 0~2일, 보고서·인터뷰는 1~2주, 에버그린은 수년 | 발췌 번역, 번호 매긴 3~5개 교훈, 1인칭 코멘트. 전문은 블로그로 보냄. |
| **에크케** | ① **국내 전자공시(DART 감사보고서와 잠정실적)와 그 보도** — "OOO는 이렇게 벌고 씁니다" 시리즈 3건 이상. ② **모회사 SBS 방송·행사 현장과 K팝·셀럽 소비 트렌드** — 2건. ③ **자체 인터뷰**(재테크 크리에이터) — 1건. ④ **해외 이색 경제 기사의 시즌 재가공**(산타 순자산) — 1건. ⑤ **브랜디드 광고** — 1건. | 현장 0일, 공시는 수주~2개월(화제성 타이밍에 맞춤), 시즌물 1년 주기 | 공시 수치 카드에 밈 소제목과 원화 환산. 셀럽·소비 밈 영상. |
| **AI Freaks** | (추론) 글로벌 AI 기업의 출시 발표와 협찬 브리프, 바이럴 AI 영상(해외 크리에이터·커뮤니티), 툴 직접 체험 | 불명 | 컴필레이션, 툴 소개, 현상 해설(추정) |
| **로만** | 데이터 없음 | 데이터 없음 | 데이터 없음 |

### 시사점: 이런 계정을 운영하려면 매일 볼 소스

추적에서 **실제로 원본으로 확인된 채널**만 정리했다. 핸들은 검색에서 확인한 것만 적었다.

1. **해외 1차 발표물 (BZCF형 AI·비즈니스)**
   - 기업 뉴스룸과 블로그: openai.com/index, newsroom.amd.com, investor.atmeta.com, lovable.dev/blog
   - 창업자·CEO 개인 사이트와 에세이: 예) steipete.me, 아모데이 개인 에세이
   - VC 발행물: a16z.com/newsletter, x.com/a16z
   - 인물 영입이나 발표가 **X에서 먼저 나오는 경우**가 있다. 올트먼의 스타인버거 영입 발표, 카파시의 앤트로픽 합류 발표(국내 보도 기준)가 그랬다. 주요 CEO와 연구자의 X 계정을 리스트로 묶어 둘 것.
2. **해외 경제·테크 매체 속보**: Bloomberg, FT, TechCrunch, CNBC, Fortune. BZCF는 대부분 하루 이내에 반응한다. 유료 기사는 "요지 번역"으로 쓴다.
3. **국내 공시와 실적 보도 (에크케형)**: DART 감사보고서와 사업보고서가 몰리는 3~4월, 잠정실적이 나오는 1~2월에 **"브랜드·구단·레이블이 어떻게 벌고 쓰나"** 카드를 만든다. 대중이 아는 브랜드(구단, 코미디 레이블, K팝 소속사)를 고르는 것이 핵심이다.
4. **K컬처 행사와 소비 트렌드**: 시상식과 가요대전 같은 대형 이벤트 당일에 소비 트렌드(두쫀쿠 등) 밈을 결합한다. 방송사 계열이 아니라면 공식 사진과 기사를 인용하는 방식으로 대체해야 한다.
5. **커뮤니티 (역방향 신호)**: 에펨코리아, 다음 카페 '여성시대', 아카라이브, 루리웹. 매거진 콘텐츠가 **퍼져 나가는 곳이자** "인스타에서 수집한" 바이럴 소재가 모이는 곳이다. 무엇이 반응을 얻는지 보는 레이더로 쓴다.
6. **경쟁 큐레이터의 피드를 소스로 보기**: 텔레그램 `t.me/s/bzcftel`은 로그인 없이 웹에서 볼 수 있는 BZCF의 일일 픽 로그다. 무엇을 고르는지 매일 벤치마킹할 수 있다.
7. **운영상 차별화**: 같은 소재를 여러 계정이 동시에 다루는 상황이므로 차별화 수단은 두 가지다. (a) **전문 번역이나 원문 링크를 블로그로 연결**하는 BZCF 방식, (b) **자체 인터뷰와 현장**(BZCF와 에크케 모두 사용). 출처 표기는 최소한 "매체명·원저자 + 날짜"를 적고, 광고는 "#광고"를 앞에 두는 수준을 권한다.

---

## 5. 게시물–원본 핵심 매핑 (빠른 참조)

- Lovable 유니콘 → Bloomberg 2025-07-17 (BZCF 07-18)
- OpenAI×AMD → 공동 보도자료 2025-10-06 (BZCF 10-07)
- a16z Big Ideas 2026 → a16z 2025-12 (BZCF 12-20, 네이버 블로그 전문)
- 스타인버거 OpenAI 합류 → 올트먼 X와 블로그 2026-02-15 (BZCF 02-16)
- 캘러닉 Atoms 매니페스토 → 2026-03-13 (BZCF 03-15)
- 아모데이 "We Must Pace the Frontier" → 2026-09-12 (bzcf.io 09-13 전문 번역)
- 한미반도체 2025 실적 → 공시·감사보고서 2026-02~03 (에크케 03-27)
- 메타코미디 2025 실적 → 감사보고서와 2026-04-03 보도 (에크케 05-20, 타 계정 05-19)
- SBS 가요대전 2025 → 2025-12-25 현장 (에크케 당일)
- 산타 순자산 → TheStreet/Stacker 2023-12 (에크케 2024-12-25)

---

## 6. 한계

1. **직접 열람 불가**: instagram.com, x.com, reddit 등은 접속이 차단돼 검색 스니펫만 썼다. 캐러셀 이미지 속 텍스트(출처가 흔히 적히는 마지막 장)는 **볼 수 없어서**, 출처 표기 관행은 과소평가됐을 수 있다.
2. **색인 편향**: BZCF와 에크케는 Threads 색인이 비교적 잘 돼 있어 Threads 게시물이 표본의 중심이다. 인스타그램 본 계정과 캡션이 같다고 가정했지만 확인하지는 못했다. @ai_freaks.kr은 개별 게시물이 색인되지 않았고, @romaan.mag은 계정 자체가 검색되지 않았다. 목표였던 계정당 6~10건을 **BZCF(14건)와 에크케(9건)만 달성**했다.
3. **귀속 불확실**: AI Freaks 표의 3건은 해당 계정 게시물인지 확인하지 못해 신뢰도를 "낮음"으로 뒀다.
4. **시차 정밀도**: 게시일은 게시물 코드를 디코딩한 UTC 기준이다. 원본은 대부분 날짜 단위(미국 시간)라서 ±1일 오차가 있다. 원본을 특정하지 못한 건은 "불명"으로 표기했다.
5. **검색 한도 소진**: 이 세션의 WebSearch 한도(200회)를 모두 써서 FT 기사 특정, 블룸버그 회장과 조나단 그레이 인터뷰 원본, 메타코미디 5/19 게시 계정 확인, AI Freaks 게시물 추가 수집을 하지 못했다.
6. 팔로워 수는 검색 시점의 스니펫이나 채용공고 수치라서 지금 값과 다를 수 있다. 수치를 추정해서 채우지는 않았다.
