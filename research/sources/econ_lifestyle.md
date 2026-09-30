# 경제·돈·라이프스타일 뉴스 소스 (검증판)

작성일: 2026-09-30 · 대상: 에크케(@ekke.now)·비즈까페(@bizucafe)형 "경제·돈·소비 트렌드" 한국어 매거진 계정
입력: 초안 목록 `prior_finds.json`의 `econ_lifestyle` 50개 (검색 없이 모델 지식으로 작성된 미검증 초안)

---

## 1. 개요

### 1-1. 무엇을 했나
- 초안 50개를 **반박 검증**했다. 존재 여부, 운영 주체, 2025~2026년 활동, 설명의 정확성, 도메인을 확인하고 틀린 URL과 명칭은 고쳤다.
- WebSearch는 **24회** 실행했다. 25번째 검색부터는 세션 공용 한도(200회)가 소진되어 **3회가 거부**됐다. 그래서 롱블랙·더밀크·해외 뉴스레터·뽐뿌 RSS는 확인하지 못했다.
- 결과: **48개 유지**(그중 10개는 URL·명칭 수정), **2개 제외**, **9개 추가**. 최종 57개.
- **2026-09-30 재검증**: 미검증이거나 근거 링크가 없던 항목을 WebSearch **40회**로 다시 확인했다. 제거 0개. 설명·명칭 수정 3건(네이버 뉴스 랭킹, 네이버페이 증권, 파인 메뉴명), 검증 등급 상향 30여 건, 하향 1건(연합뉴스 RSS). 자세한 내용은 **6장 재검증(2026-09-30)**에 있다.

### 1-2. 초안에서 크게 바뀐 점
| 항목 | 초안 | 검증 후 |
|---|---|---|
| 통계청 | "국가데이터처로 바뀐 것으로 앎, 도메인 확인 필요" | **2025-10-01 국가데이터처로 출범**. 홈페이지는 **mods.go.kr**, 통계포털은 kosis.kr 그대로 |
| 기획재정부 | 언급만 있음 | **2026-01-02 재정경제부(mofe.go.kr)와 기획예산처로 분리 출범**. 재정경제부를 소스로 새로 넣음 |
| 보조금24 | "정부24 보조금24" | 정부24가 **정부24+(plus.gov.kr)**로 전면 개편됐고, 메뉴 이름도 **'혜택알리미'**로 바뀜(2026-08 기준, 옛 주소는 새 화면으로 연결) |
| 한경 컨센서스 | consensus.hankyung.com | **markets.hankyung.com/consensus** (한국경제 마켓 섹션으로 이동) |
| 오픈서베이 | opensurvey.co.kr | 리포트는 **blog.opensurvey.co.kr/trendreport/**에 모여 있음. 2026년판 다수 확인 |
| 편의점 공식 계정 | "핸들 미검증" | **CU @cu_official, GS25 @gs25_official**(X는 @funGS25) 확인. 세븐일레븐은 미확인 |
| 슈카월드 | "핸들 미검증" | **youtube.com/@syukaworld**, 구독자 약 371만 명(2026-06 기사 기준) |
| 트렌드 코리아 | "2027년판 출간 여부 미확인" | **『트렌드 코리아 2027』 2026-09-30(오늘) 출간**. 키워드 10개 공개됨(아래 표 참조) |
| 커리어리 | "현직자 아티클 공유 커뮤니티" | 2024-09 **시소가 운영사 퍼블리를 인수**. 현재는 개발자·AI 커리어 커뮤니티라 이 목록에서 뺌 |

### 1-3. 검증 표기
- **검증**: 이번 검색으로 존재와 2025~2026년 활동(또는 해당 URL)을 확인함
- **검증(URL 수정)**: 확인 과정에서 주소나 명칭을 고침
- **부분 검증**: 일부 핸들이나 주소만 확인함
- **미검증(확신 높음)**: 검색 예산 때문에 확인하지 못했지만 공공기관이나 대형 매체라 존재는 확실함. 세부 URL, RSS, 최근 개편 여부는 직접 확인할 것
- **(재검증)**: 검증 칸에 "재검증"이 붙은 항목은 2026-09-30 재검증에서 다시 확인했거나 고친 것이다. 근거는 6장에 있다.
- 팔로워·구독자 수는 검색 결과에 나온 것만 적었다. 나머지는 "미확인"이다.

### 1-4. 다른 파일과의 관계
- X 계정(AI)은 `x_ai.md`, 4개 계정의 실제 소스 추적은 `source-tracing.md`를 본다.
- `source-tracing.md`의 결론: **에크케는 DART 공시와 그 보도**, **비즈까페는 Bloomberg·FT 같은 해외 경제지와 1차 발표물**을 주로 쓴다. 그래서 DART와 해외 매체를 우선순위에 넣었다.
- 뉴스레터·미디어 초안 목록과 겹치는 항목(롱블랙, 더밀크, 어피티, 캐릿, 한국은행, KOSIS, 정책브리핑, DART, FT)은 여기서 **경제·생활 소재 관점**으로만 설명한다.

### 1-5. 하루 모니터링 루틴 (제안)
1. **오전 8~9시**: 연합뉴스 경제 RSS와 네이버 경제 섹션·언론사별 랭킹으로 오늘의 화제를 파악 → 정책브리핑 보도자료 RSS로 정부 발표 확인
2. **점심**: 알구몬(뽐뿌·루리웹 등 핫딜 묶음)과 에펨코리아 핫딜 → 딜·앱테크 소재 / 더쿠 핫게로 소비 밈 감지
3. **오후**: 후보 주제를 네이버 데이터랩으로 검색량 검증 → 원자료(DART, KOSIS, 한국은행, 부처 보도자료)로 수치 확인
4. **저녁**: 해외(Bloomberg·FT·WSJ·Reuters)에서 "해외에선 이렇다" 각도 추가
5. **주 1회**: 트렌드 리포트(20대연구소, 오픈서베이, 트렌드모니터, KB·하나 연구소), 혜택알리미·온통청년 신규 지원 사업 점검

---

## 2. 추천 소스 표

`[추가]`는 이번에 새로 넣은 소스다. 속도는 "사건 발생부터 이 소스에 올라오기까지" 걸리는 시간 기준이다.

### 2-A. 국내 경제 매체·포털 (화제 감지·속보)

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법(RSS) | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| 연합뉴스 경제 | yna.co.kr/economy | 국내 경제 속보 | ko | 수분~1시간 | 높음 | **RSS: https://www.yna.co.kr/rss/economy.xml** → Feedly 등 등록 | 정부 발표·통계·금리 결정을 가장 먼저, 건조하게 요약함. 팩트 기준점 | 사진·그래픽은 유료 라이선스라 쓰지 말 것. 사실만 활용 | 부분 검증(재검증: RSS 주소는 제3자 문서·GitHub 검색 스니펫에서만 확인됨. 연합뉴스 공식 RSS 안내 페이지는 검색에 잡히지 않음. 등록 전에 피드가 열리는지 직접 확인) |
| 한국경제 | hankyung.com | 재테크·부동산·세금·기업 | ko | 수시간 | 중간 | **RSS 목록: https://www.hankyung.com/feed** (섹션별 피드 선택), 네이버 언론사 구독 | "이번 주 바뀌는 돈 제도" 카드의 원재료. 비즈까페형 "기사+코멘트"의 원문 | 한경 프리미엄(유료) 기사 요약 공유 주의. 문장은 새로 쓰고 출처 표기 | 검증(RSS 페이지 존재) |
| 매일경제 | mk.co.kr | 부동산·소비·유통 | ko | 수시간 | 중간 | 섹션별 RSS 제공(RSS 리더 Feeder에 '경제·금융' 피드가 등록돼 있음). 정확한 주소는 사이트 RSS 페이지에서 확인 | "요즘 ○○가 뜨는 이유" 같은 소비·유통 소재 | 전재 금지, 출처 표기 | 검증(RSS 존재) |
| 조선비즈 | biz.chosun.com | 기업·산업·유통 | ko | 수시간~당일 | 중간 | 네이버 언론사 구독, 산업·유통 섹션 | 비즈까페형 "기업 이야기" 원문 | 전재 금지 | 미검증(확신 높음) |
| 머니투데이 | mt.co.kr | 증시·개인투자·생활경제 | ko | 수시간 | 중간 | 네이버 언론사 구독 | 개인투자자 관점 "벌기·모으기" 소재 | 자극적 제목이 섞임. 원자료로 교차 확인 | 미검증(확신 높음) |
| 이데일리 | edaily.co.kr | 금융·증권·정책 | ko | 수시간 | 중간 | 네이버 언론사 구독 | 금리·대출·예적금 변화를 "내 돈에 미치는 영향"으로 풀기 | 전재 금지 | 존재 확인(2026 기사 URL이 검색에 노출) |
| 네이버 뉴스 경제 섹션 + 언론사별 랭킹 | news.naver.com/section/101 · 네이버 뉴스 '랭킹' 메뉴(언론사별 많이 본 뉴스) | 경제 뉴스 화제 감지 | ko | 실시간 | 중간 | 아침·저녁 2회, 경제 섹션 헤드라인과 경제지(한경·매경 등)의 언론사별 랭킹을 함께 봄 | 지금 대중이 반응하는 경제 이슈를 판단. Similarweb 기준 2026-03 국내 뉴스·미디어 사이트 방문 1위 | **전체·섹션별 '많이 본 뉴스' 랭킹은 2020-11에 폐지**되어 '경제 섹션 랭킹'은 없음. 언론사별 랭킹만 남아 있으니 "경제 랭킹 1위" 같은 표현은 쓰지 말 것. 포털은 원문이 아니므로 언론사 원문과 원자료로 확인 | 검증(재검증, 설명 수정. 섹션 URL 자체는 검색으로 확인 못 함) |
| 한경 컨센서스 | **markets.hankyung.com/consensus** (초안의 consensus.hankyung.com에서 수정) | 증권사 기업·산업 리포트 | ko | 매일 | 높음 | 산업 리포트 주 2~3회, 관심 업종 키워드 검색 | "편의점 업계 판도", "K뷰티 수출" 같은 해설 포스트 근거 | 리포트 차트 캡처 재배포 금지. 증권사명 표기, 투자 권유처럼 보이지 않게 | 검증(URL 수정) |
| 네이버페이 증권 리서치 `[추가]` | finance.naver.com/research (서비스명이 '네이버 증권'에서 '네이버페이 증권'으로 바뀌었고 도메인은 그대로) | 증권사 리포트 모음(시황·산업·종목·경제) | ko | 매일 | 높음 | 산업분석·경제분석 탭 주 2~3회 | 한경 컨센서스의 대체·보완. 산업 리포트 요약본을 빠르게 훑기 좋음 | 위와 같음. 리포트 원문 PDF 재배포 금지 | 검증(재검증, 명칭 수정. 증권사 리포트 PDF가 매일 올라오는 것은 확인. /research 경로 자체는 검색으로 직접 확인 못 함) |

### 2-B. 공공·통계·정책 (1차 자료, 팩트 확인)

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법(RSS) | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| 국가데이터처(구 통계청) + KOSIS | **mods.go.kr** · kosis.kr | 물가·고용·가계동향·인구 | ko | 공표일정 고정(발표 당일) | 높음 | 보도자료와 **공표일정 캘린더** 확인, KOSIS 지표 즐겨찾기 | "요즘 월평균 지출 1위는?" 같은 데이터 카드의 핵심 원천 | 2025-10-01 출범. 기획재정부 외청에서 **국무총리 소속**으로 바뀜(통계청 35년 만의 승격). 지방 조직 명칭 전환이 늦어 기사마다 "통계청"과 섞여 쓰임. 공공누리 유형 확인 | 검증(URL 수정, 재검증: 출범일·소속 재확인) |
| 한국은행 + ECOS | bok.or.kr · ecos.bok.or.kr | 기준금리·소비자심리·가계부채 | ko | 발표 당일(금통위 일정 고정) | 높음 | 보도자료 게시판, 금통위 일정을 캘린더에 등록, 통계는 ECOS | "금리가 내 대출·예금에 미치는 영향" | 전망치와 확정치 구분. 전문용어는 풀어 쓸 것. RSS 제공 여부는 재검증에서도 확인 못 함 | 검증(재검증: 보도자료 게시판·ECOS 운영, 2026-09 「금융안정 상황」 게시 확인) |
| 재정경제부 `[추가]` | **mofe.go.kr** | 경제정책·세제·외환 | ko | 발표 당일 | 높음 | 보도자료, 정책브리핑 부처 필터 | 세법개정안, 경제정책방향처럼 "내년부터 달라지는 세금·돈" 소재의 원천 | 2026-01-02 기획재정부가 재정경제부·기획예산처로 분리됨(2008년 통합 후 18년 만). 예산·기금·국가채무는 기획예산처 소관. **그린북(최근 경제동향)은 재정경제부 경제정책국이 계속 발간**(2026년 9월호 2026-09-11 발표) | 검증(재검증: 출범일·소관·그린북 발간 주체 확인) |
| 금융위원회 | fsc.go.kr | 청년 금융상품·대출 규제·서민금융 | ko | 발표 당일 | 높음 | 보도자료, 정책브리핑 부처 필터 | 청년 금융상품(2026년 토스피드에 '청년미래적금' 콘텐츠가 올라옴) 조건·신청법 정리 | 시행일·신청기간, "예정"과 "확정"을 구분. 청년미래적금은 2026-06-22 출시(만 19~34세, 3년 만기, 월 최대 50만 원. 은행 블로그 기준). **2025-09-25 금융위 해체·금감원 분리 개편안이 철회되어 금융위·금감원은 현 체제 유지** | 검증(재검증: 개편안 철회, 청년미래적금 출시 확인) |
| 금융감독원 + 파인 | fss.or.kr · fine.fss.or.kr | 소비자경보·금리 비교 | ko | 당일~주간 | 높음 | 소비자경보 게시판, 파인(FINE)의 금융상품 비교 메뉴 주 1회 | "이 사기 조심", "이번 달 금리 높은 적금" | 금리는 기준일 명시. 특정 상품 추천은 광고로 오인될 수 있음 | 검증(재검증: 파인은 계좌 통합조회·숨은 금융자산·금융상품 비교를 제공하는 금감원 금융소비자 포털. 초안의 메뉴명 "금융상품 한눈에"는 검색으로 확인 못 해 일반 표현으로 고침) |
| DART 전자공시 `[추가]` | dart.fss.or.kr · API: opendart.fss.or.kr | 기업 실적·감사보고서 | ko | 공시 즉시 | 높음 | 관심 기업 공시 알림, 3~4월 감사보고서·사업보고서 시즌 집중 | **에크케 "○○는 이렇게 벌고 씁니다" 시리즈의 원천**(source-tracing.md: 한미반도체·KT위즈·메타코미디 사례) | 연결·별도 기준과 기준 연도를 명시. 언론마다 증감률이 다르게 나오므로 원문 대조 | 검증(재검증: 금감원 운영 dart.fss.or.kr·OpenDART 오픈API 확인, OpenDartReader 2026 개정판 문서 존재) |
| 국토교통부 | molit.go.kr | 부동산 대책·청약·전세사기·교통비 환급 | ko | 발표 당일 | 높음 | 보도자료, 정책브리핑 부처 필터 | "교통비 아끼는 법"(K-패스, 2026년에 추가된 정액형 '모두의 카드' 등), 청약 제도 변경 | 제도명·환급률이 자주 바뀜. 2026년 4~9월 한시로 환급 기준을 낮췄다는 블로그 정리가 있으니 10월 이후 기준은 국토부 원문으로 확인 | 부분 검증(재검증: '모두의 카드' 도입은 블로그·나무위키로만 확인, 국토부 원문은 못 봄) |
| 한국부동산원 + 청약홈 | reb.or.kr · applyhome.co.kr | 주간 아파트 가격·청약 일정 | ko | 주간(정기) | 높음 | 주간 동향 발표일, 청약 캘린더 주 1회 | "이번 주 청약 캘린더", "집값 오른 지역" | 투자 권유로 보이지 않게 정보 전달형으로 | 검증(재검증: 부동산원 '주간아파트가격동향'과 통계포털 R-ONE(reb.or.kr/r-one), 부동산원이 운영하는 청약홈 '청약캘린더' 확인) |
| 대한민국 정책브리핑 | korea.kr · RSS 안내: korea.kr/etc/rss.do | 전 부처 보도자료·정책 카드뉴스 | ko | 실시간~당일 | 높음 | **보도자료 RSS: https://www.korea.kr/rss/pressrelease.xml**, 주간 뉴스레터(korea.kr/newsletter/) | 에크케식 "이번 달부터 바뀌는 것". 6·12월 "하반기·새해부터 달라지는 것" 필수 | 대체로 공공누리지만 유형(출처표시·변경금지 등) 확인 | 검증(재검증: RSS 서비스 페이지 korea.kr/etc/rss.do 검색 결과로 보도자료 피드 주소 확인) |
| 정부24+ 혜택알리미(구 보조금24) + 복지로 | **plus.gov.kr/portal/benefitV2/** · bokjiro.go.kr | 받을 수 있는 지원금 | ko | 수시(신청기간 중심) | 높음 | 혜택알리미 맞춤 알림, 복지로 신규 서비스 | "놓치면 손해 혜택 모음" 저장·공유형 포스트 | 정부24가 정부24+로 개편, 한 번 로그인하면 복지로·고용24도 이용 가능. 보조금24의 맞춤 검색 기능이 혜택알리미로 옮겨감(로그인 후 '나의 혜택', 비로그인은 '간편 찾기'). 옛 보조금24 주소(gov.kr)도 아직 검색에 노출됨. 지역·소득 조건 명시, 마감일 표기 | 검증(명칭·URL 수정, 재검증: plus.gov.kr/portal/benefitV2/ 페이지 제목이 "혜택알리미", 정책브리핑 안내 기사 확인) |
| 온통청년 `[추가]` | youthcenter.go.kr | 중앙·지자체 청년정책 통합 | ko | 수시 | 높음 | 청년정책 통합검색, 신규 정책 주 1회 | 약 3,000개 청년정책 DB. "20대가 받을 수 있는 돈" 시리즈 | 지자체별 조건이 달라 "거주지 확인 필수" 문구 | 검증(재검증: 약 3,000개 정책 실시간 수집, 청년정책 통합검색 메뉴 확인) |
| 국세청 | nts.go.kr (신고는 홈택스) | 연말정산·종소세·장려금 | ko | 시즌성 | 높음 | 보도자료, 연간 세무 일정을 캘린더에 | 1월 연말정산, 5월 종소세, 근로·자녀장려금 | 세법은 해마다 바뀜. 해당 연도 기준 명시, 개별 상담처럼 쓰지 말 것 | 검증(재검증: nts.go.kr에 「2026년 근로장려금 반기 신청·지급제도」 게시 확인) |
| 한국소비자원 + 참가격 | kca.go.kr · price.go.kr | 비교시험·리콜·생필품·외식비 가격 | ko | 주간~격주 | 높음 | 보도자료 주 1~2회, 참가격 품목별·외식비 가격 | "같은 제품인데 가격 차이 ○배", 외식비 변화 | 브랜드 비교 결과는 원문 표현 그대로, 조사 시점과 함께 | 검증 |
| KOTRA 해외시장뉴스 | dream.kotra.or.kr/kotranews/index.do | 해외 소비 트렌드·K제품 수출 | ko | 일간 | 높음 | 뉴스·보고서 섹션 주 2회 | "미국·일본에서 난리 난 K○○" | 공공누리 유형 확인 | 검증(2026 기사 확인) |

### 2-C. 커뮤니티 (대중 반응·딜·실사용자 언어)

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법(RSS) | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| 알구몬 `[추가]` | algumon.com | 핫딜 모음(뽐뿌·딜바다·루리웹·쿨엔조이·어미새 등) | ko | 실시간 | 중간 | 하루 2회, 키워드 알림 | 여러 커뮤니티의 핫딜을 한 화면에서 봄. 딜 소재 수집 시간 절약 | **에펨코리아 핫딜은 수집하지 않는 것으로 알려짐**. 딜은 금방 끝나니 게시 시점 명시 | 검증(재검증: 웹 algumon.com/n/deal 운영, 안드로이드 앱 2026-09-01 업데이트 v0.7.17, 텔레그램 연동) |
| 뽐뿌 | ppomppu.co.kr · 재테크포럼(게시판 ID `money`): m.ppomppu.co.kr/new/bbs_list.php?id=money | 핫딜·재테크포럼·이벤트·앱테크 | ko | 실시간 | 중간 | 뽐뿌게시판 추천순, 재테크포럼(매월 연재 "신용카드 캐시백 이벤트 비교" 등)·이벤트 게시판. 사용자 글에 게시판별 RSS 형식 `ppomppu.co.kr/rss.php?id=게시판ID`가 나오지만 공식 안내로는 확인 못 함 | "이번 주 역대급 할인", "앱테크 신규 이벤트" | 게시글·캡처 무단 사용 금지. 제휴·광고 글 섞임. 재테크포럼은 신용카드 체리피킹 글 비중이 큼 | 검증(재검증: 재테크포럼 2026-06 연재글·2026-09 활동 확인. RSS 주소는 미확인) |
| 에펨코리아 핫딜 `[추가]` | fmkorea.com/hotdeal | 핫딜(게임·IT·생활) | ko | 실시간 | 중간 | 추천순 일 1~2회 | 20~30대 남성 이용자가 많은 대형 핫딜 게시판. 알구몬에 안 잡히는 딜 보완 | 커뮤니티 성향 논란이 잦음. 게시글 캡처·인용 자제 | 검증 |
| 클리앙 알뜰구매 | clien.net/service/board/jirum | IT·통신 요금제·카드 혜택 딜 | ko | 실시간 | 중간 | 추천순 일 1회 | "알뜰폰·카드 혜택 비교" | 원문 캡처 금지, 정보만 재구성. 게시글을 모아 주는 텔레그램 채널(t.me/s/clienjirum)이 있으나 공식 여부는 미확인 | 검증(재검증: 게시판 URL 확인) |
| 더쿠 핫게시판 | theqoo.net/hot | 20~30대 여성 중심 화제·소비 밈 | ko | 실시간 | 낮음 | 하루 2회, 반복 키워드 메모 | 신상 화제, 브랜드 논란, 소비 밈 초기 포착 | 퍼온 글과 루머가 많음. 원출처 확인 필수 | 검증(재검증: theqoo.net/hot에 2026-05·07 화제 글 확인) |
| 월급쟁이재테크연구(월재연) | cafe.naver.com/onepieceholicplus | 직장인 짠테크·앱테크·적금 후기 | ko | 일간 | 중간 | 가입 후 인기글·앱테크 게시판 알림 | "월급 ○○만 원으로 1년 ○천만 원 모은 법" 류 아이디어 | 운영자 소개 기준 회원 약 100만 명(수치는 운영자 측 표현). 회원 전용 글이라 작성자 동의 없이 인용 금지 | 검증 |
| 맘스홀릭 베이비 | cafe.naver.com/imsanbu | 임신·출산·육아 | ko | 일간 | 낮음 | 인기글 확인 | 출산·육아 지원금, 육아템 트렌드 반응 | 회원 전용 글 외부 유출 금지, 개인정보 주의. 주 타깃(2030 직장인)과 거리가 있어 보조용 | 검증 |
| 블라인드 | teamblind.com/kr | 연봉·성과급·이직·복지 | ko | 실시간 | 낮음 | 토픽 베스트 일 1회, 기사화된 이슈는 언론으로 교차 확인 | "직장인이 뽑은 ○○" 커리어·돈 소재 | 익명 글이라 사실 검증 불가. 특정 회사 비방으로 이어지지 않게 | 검증(재검증: teamblind.com/kr '토픽 베스트' 페이지·성과급 토픽 확인) |

### 2-D. 트렌드·데이터·리포트 (근거 수치·시즌 소재)

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법(RSS) | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| 네이버 데이터랩 | datalab.naver.com | 검색어 트렌드·쇼핑인사이트 | ko | 일간 데이터 | 높음 | 후보 주제가 생기면 즉시 비교, 쇼핑인사이트 주 1회 | 주제가 실제로 뜨는지, 성별·연령대 검증 | 상대지수(조회 기간의 최댓값=100)라 절대 검색량처럼 쓰지 말 것. 절대값은 데이터랩 웹·API 어디에도 없음(네이버 클라우드 유료 서비스 영역) | 검증(재검증: 검색어트렌드·쇼핑인사이트·지역·댓글 통계 제공, 상대지수 방식 확인) |
| 구글 트렌드 | trends.google.com/trending?geo=KR (초안의 trends.google.co.kr는 같은 서비스) | 급상승 검색어·글로벌 비교 | ko/en | 실시간 | 중간 | "지금 인기" 한국 설정 일 1회 | 해외 트렌드가 한국에 들어오는 시점 포착 | 한국은 네이버 비중이 커서 대표성 주장 금지 | 검증(재검증: trends.google.com/trending?geo=KR "Trending now" 페이지 확인) |
| 썸트렌드 (바이브컴퍼니) | some.co.kr | SNS·커뮤니티 언급량·연관어·감성 | ko | 일간 | 중간 | 관심 키워드 주 1회 | "사람들이 ○○를 말할 때 같이 쓰는 단어". 2026-03 **Claude용 MCP**, 이후 ChatGPT 앱도 출시돼 AI 도구에서 바로 조회 가능 | 유료 기능 범위와 캡처 사용 조건 확인 | 검증(2026 활동) |
| 대학내일20대연구소 | 20slab.org | Z세대 소비·가치관 조사 | ko | 주간~월간 | 높음 | 아카이브 게시판, 연말 『Z세대 트렌드』 | "Z세대가 돈 쓰는 곳", 2026 앱테크·해외여행·수면 소비 리포트 등 | 도표 재사용 시 출처 표기, 상업 이용 조건 확인 | 검증(2026 리포트) |
| 캐릿 Careet (대학내일) | careet.net | Z세대 밈·신상·핫플·캠페인 | ko | 주간 | 높음 | 뉴스레터 구독, 요즘어 사전·이슈 캘린더 | "요즘 애들 사이에서 뜨는 ○○" | 일부 유료 콘텐츠, 요약 공유 주의 | 검증 |
| 오픈서베이 트렌드 리포트 | **blog.opensurvey.co.kr/trendreport/** | 카페·쇼핑·구독·결제·소셜미디어 등 | ko | 분야별 연 1회(연중 순차 발간) | 높음 | 트렌드리포트 태그 페이지, 뉴스레터 | 2026 카페 리포트(최근 1개월 이용률 메가커피 71.0%, 스타벅스 69.2%) 같은 데이터 카드 | 조사 시기·표본 명시 | 검증(URL 수정, 2026 리포트 확인) |
| 트렌드모니터 (마크로밀엠브레인) | trendmonitor.co.kr · embrain.com/kor/channel/trend | 직장·소비 인식조사 | ko | 주간 | 높음 | 조사결과 게시판, 언론 인용 기사 | "직장인 ○○%가…" 공감형 통계(예: 2026-05 직장 내 세대 인식 조사) | 출처 표기 필수 | 검증(2026 조사) |
| 『트렌드 코리아』 (서울대 소비트렌드분석센터·김난도) | 연간 도서. **2027년판 2026-09-30 출간** | 다음 해 소비 키워드 | ko | 연 1회(9~10월) | 높음 | 매년 9~10월 출간 기사, 10~11월 강연·전시 | **2027 키워드: 권태사회, 라이프 ROI, 폼팩터 시프트, 해봄경제, 저장인류, 바이브 워킹, 리:텐션 전략, 휴먼엣지, 하프시그널, 안목자본.** 출간 기념 전시 10/13~11/8(여의도), 강연 10/26(CGV 여의도) | 도서 내용 과도한 요약·전재 금지. 키워드 설명은 보도 기사 수준에서 | 검증 |
| KB금융 경영연구소 · 하나금융연구소 `[추가]` | kbfg.com/kbresearch · hanaif.re.kr | 부자 보고서·웰스 리포트·금융소비자 조사 | ko | 연간(정기 보고서) | 높음 | 연구보고서 목록 월 1회, 발간 기사 | 「2025 한국 부자 보고서」(금융자산 10억 원 이상 약 47.6만 명, 총금융자산 3,066조 원) 같은 "부자들은 어디에 투자할까" 대형 소재 | 부자 정의(금융자산 10억 원 이상)를 함께 적을 것 | 검증 |

### 2-E. 뉴스레터·크리에이터·기업 콘텐츠 (톤 참고·주제 발굴)

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법(RSS) | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| 어피티 UPPITY 머니레터 | uppity.co.kr (머니레터 아카이브: uppity.co.kr/category/newsletter/moneyletter/) · IG **@uppity.official**(약 6.2만, 검색 스니펫 기준) · YouTube @uppity_official | 2030 돈 관리·경제 뉴스 | ko | 평일 일간 | 높음 | 무료 구독(uppity.co.kr/subscription/) | 에크케 "벌기·모으기·쓰기" 톤과 가장 비슷한 벤치마크. 자체 소개 기준 구독자 약 70만 명 | 경쟁 매체이므로 문장·구성 모방 금지. "머니레터 AD" 광고 섹션 있음 | 검증(2026-08 발행 확인) |
| 토스피드 | toss.im/tossfeed · IG @toss_feed | 금융·세금·절약 설명 | ko | 주간 | 높음 | 사이트 "금융의 모든 것" 카테고리 | 쉬운 설명·일러스트 톤 레퍼런스. 2026년 청년미래적금·소득공제·청약 콘텐츠 | 자사 상품 홍보가 섞임("토스의 모든 것" 카테고리 구분) | 검증 |
| 슈카월드 (YouTube) | youtube.com/@syukaworld | 대중 경제 해설 | ko | 주 1~2회 라이브 | 중간 | 구독·알림 | 그 주에 대중이 관심 갖는 경제 주제를 가늠. 구독자 약 371만 명(2026-06 기사 기준) | 영상 캡처·요약 재게시 금지. 주제 선정 참고용 | 검증 |
| 롱블랙 | longblack.co | 브랜드·창업가 스토리 | ko | 일간 | 높음 | 유료 구독 | 비즈까페형 "브랜드 인사이트" 영감 | 유료 콘텐츠. 요약·재게시 금지, 주제만 참고. "하루 지나면 사라지는" 24시간 열람 구조 | 검증(재검증: longblack.co·iOS/안드로이드 앱 운영, 2026년 새 기능 '롱블랙 플레이' 언급 확인) |
| 더밀크 The Miilk | themiilk.com | 미국 빅테크·유통·소비 트렌드 | ko | 일간 | 높음 | 뉴스레터 구독 | "미국에서 뜨는 ○○, 한국에도 올까" | 유료 기사 전재 금지 | 검증(재검증: 손재권 대표 CES 2026 미디어 파트너 세션 연사, 2026년 기사 게재 확인) |

### 2-F. 유통·소비 현장 (쓰기 소재)

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법(RSS) | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| 올리브영 | oliveyoung.co.kr | 뷰티 랭킹·올영세일 | ko | 실시간(랭킹) | 높음 | 앱 랭킹 주 2~3회, 세일 일정 캘린더 | "지금 올영에서 제일 잘 팔리는 것" | 제품 이미지는 브랜드 저작물. 협찬이 아니면 광고처럼 보이지 않게. 공식 IG **@oliveyoung_official**(약 100만, 검색 스니펫 기준), X @oliveyoung. 글로벌·매거진 계정(@oliveyoung_global, @oliveyoung_mag_official)과 헷갈리지 말 것 | 검증(재검증: 핸들 확인) |
| 다이소몰 | daisomall.co.kr · 신상: daisomall.co.kr/ds/prir | 생활·뷰티 신상·품절템 | ko | 주간 | 중간 | 신상 탭, 기획전("2026 상반기 결산", 월간 신상전) | "재입고 요청 TOP3", "다이소 ○천 원 신상" | 제품 사진은 직접 촬영 권장 | 검증 |
| 편의점 신상 (CU·GS25·세븐일레븐) | IG **@cu_official**, **@gs25_official** (GS25 X: @funGS25). 세븐일레븐은 X **@711korea**, 페이스북 7elevenkorea 확인. 인스타 핸들은 미확인 | 편의점 신상·협업·품절 대란 | ko | 주간 | 중간 | 공식 계정 팔로우, 네이버 뉴스 "CU 신상"·"GS25 출시" 키워드 알림 | "이번 주 편의점 신상" 정기 시리즈 | 리뷰 계정 사진 무단 사용 금지. 세븐일레븐은 인스타 앱에서 직접 확인 | 부분 검증 |

### 2-G. 해외 (비즈까페형 "해외에선 이렇다")

| 이름 | 핸들/URL | 분야 | 언어 | 속도 | 신호대잡음 | 모니터링 방법(RSS) | 활용 포인트 | 주의 | 검증 |
|---|---|---|---|---|---|---|---|---|---|
| Bloomberg | X @business · bloomberg.com | 시장·기업 속보 | en | 거의 실시간 | 높음 | X 리스트 "글로벌 비즈니스", 뉴스레터 | 비즈까페가 실제로 원문으로 쓴 매체(Lovable, Cursor 단독). K푸드·K뷰티 관련 해외 기사 포착 | 차트·기사 전재 금지. X에는 @Bloomberg 계정도 따로 있음 | 검증(재검증: x.com/business 계정 확인. source-tracing.md에서 인용 사례 확인) |
| Financial Times | X @FT · ft.com | 글로벌 경제·금융·럭셔리 | en | 수시간 | 높음 | X 리스트, 무료 뉴스레터 | 비즈까페 "FT 기사 내용 중 일부"(K자형 경제) 방식의 요지 번역 | 페이월 기사 전재 금지. 매체명·날짜 표기 | 검증(재검증: x.com/ft 계정 확인) |
| The Wall Street Journal | X @WSJ · wsj.com | 기업·소비·직장 문화 | en | 수시간 | 높음 | X 리스트, 뉴스레터 | "미국 직장인 사이에서 ○○ 유행" | 유료 기사 요약 전재 주의 | 미검증(확신 높음. 재검증에서 X 팔로워 약 2,070만이라는 제3자 블로그 수치만 나오고 핸들 페이지는 확인 못 함) |
| Reuters `[추가]` | reuters.com/business · X @Reuters | 글로벌 통신사 속보 | en | 수분~1시간 | 높음 | X 리스트, 비즈니스 섹션 | 연합뉴스의 해외판. 해외 이슈의 팩트 기준점 | 사진 라이선스 주의 | 미검증(확신 높음) |
| The Economist `[추가]` | economist.com (Graphic detail·Daily chart) · X @TheEconomist | 경제 분석·데이터 차트 | en | 일간(차트)·주간(잡지) | 높음 | X 팔로우, 차트 섹션 | "한국은 몇 위?" 국가 비교 데이터 카드의 근거. 원 데이터 출처(OECD·IMF 등)를 따라가 인용 | 차트 이미지 재사용 금지, 수치만 재구성 | 미검증(확신 높음) |
| Business Insider | X @BusinessInsider · businessinsider.com | Z세대 소비·직장·부자 습관 | en | 수시간 | 중간 | X 리스트, 사이트 | 인스타 친화적 라이프스타일 경제 소재 | 클릭베이트성 제목. 원자료 확인 | 미검증(확신 높음) |
| Morning Brew | morningbrew.com · X @MorningBrew | 비즈니스 뉴스 요약 뉴스레터 | en | 평일 일간 | 높음 | 무료 뉴스레터 | 위트 있는 요약 톤 레퍼런스, 미국 소비·브랜드 이슈 | 문장 번역 게재 금지. 원출처 기사로 인용 | 검증(재검증: morningbrew.com 최신호 페이지 운영, 구독자 400만+는 제3자 뉴스레터 목록 기준) |
| Visual Capitalist | visualcapitalist.com · X @VisualCap | 인포그래픽 경제 데이터 | en | 일간 | 높음 | 뉴스레터, X | 국가별 물가·연봉·부 순위 비교 | 그래픽 라이선스 확인(별도 라이선스 판매처 licensing.visualcapitalist.com 있음), 원 데이터 출처 인용 | 검증(재검증: 2026년 GDP 순위 차트·「2026 Global Forecast Report」 등 2026 콘텐츠 확인) |
| CB Insights | cbinsights.com · X @CBinsights | 스타트업 투자·유니콘 | en | 주간 | 중간 | 무료 뉴스레터 | "올해 돈이 몰린 산업" 데이터 | 리포트 차트 라이선스 확인. 소비·생활 소재와는 거리가 있어 보조용 | 검증(재검증: 무료 뉴스레터 주 3~5회 발행, 제3자 뉴스레터 목록 기준) |

---

## 3. 우선순위 Top 10 (왜)

| 순위 | 소스 | 왜 |
|---|---|---|
| 1 | **연합뉴스 경제 (RSS)** | 가장 빠르고 건조한 팩트 요약. RSS가 있어 자동화가 쉽다. 모든 포스트의 "사실 기준점" |
| 2 | **네이버 뉴스 경제 섹션 + 언론사별 랭킹** | 한국에서 무엇이 실제로 읽히는지 보여 주는 가장 직접적인 신호. 인스타에서 터질 주제를 고르는 1차 필터. 섹션별 '많이 본 뉴스'는 2020년에 없어졌으니 경제 섹션 헤드라인과 경제지의 언론사별 랭킹을 같이 본다 |
| 3 | **대한민국 정책브리핑 (보도자료 RSS)** | 전 부처 발표가 한곳에 있고 RSS가 있다. "이번 달부터 바뀌는 것"은 저장·공유가 많은 포맷이다. 공공누리라 재가공 부담도 적다 |
| 4 | **DART 전자공시** | `source-tracing.md`에서 확인된 에크케 핵심 포맷("○○는 이렇게 벌고 씁니다")의 원천. 3~4월 감사보고서 시즌에 대중이 아는 브랜드·구단·레이블을 고르면 된다 |
| 5 | **국가데이터처·KOSIS + 한국은행** | 물가·고용·가계동향·금리처럼 모든 "내 돈" 이야기의 공식 수치. 공표일정이 고정돼 콘텐츠 캘린더를 미리 짤 수 있다 |
| 6 | **정부24+ 혜택알리미 + 온통청년** | "받을 수 있는 돈"은 2030 타깃에서 저장률이 가장 높은 소재 중 하나. 보조금24가 혜택알리미로 바뀐 것을 반영했다 |
| 7 | **알구몬 + 뽐뿌 + 에펨코리아 핫딜** | 딜·앱테크 소재는 속도가 생명. 알구몬이 여러 커뮤니티를 묶어 주고, 알구몬이 수집하지 않는 펨코만 따로 보면 된다 |
| 8 | **네이버 데이터랩** | 주제가 정말 뜨는지 검색량으로 검증하는 도구. "검색량 ○배" 같은 근거 문장도 만들어 준다 |
| 9 | **대학내일20대연구소·캐릿 + 오픈서베이 + 트렌드모니터** | 2026년 리포트가 꾸준히 나온다. "요즘 20대는", "직장인 ○○%" 같은 데이터형 트렌드 카드의 근거 |
| 10 | **Bloomberg·FT·WSJ (+Reuters)** | 비즈까페가 실제로 원문으로 쓰는 매체. "해외에선 이렇다" 비교 각도와 해외 기업 스토리의 원천 |

**지금 바로 쓸 시즌 소재**: 『트렌드 코리아 2027』이 오늘(2026-09-30) 출간됐다. 10월 첫 주에 "2027 키워드 10개" 카드를 내고, 10/13~11/8 전시와 10/26 강연을 후속 소재로 쓴다. 이후 12월 정책브리핑 "새해부터 달라지는 것", 1월 연말정산, 3~4월 DART 감사보고서 시즌으로 이어진다.

---

## 4. 제거한 항목과 이유

| 항목 | 이유 |
|---|---|
| 커리어리 (careerly.co.kr) | 초안은 "현직자가 아티클을 공유하는 커뮤니티"로 설명했지만, 2024-09 IT 아웃소싱 기업 **시소가 운영사 퍼블리를 인수**했다(퍼블리는 2024-08 콘텐츠 사업을 뉴닉에 넘김). 지금은 개발자 비중이 큰 "AI 시대의 커리어" 커뮤니티로 소개된다. 서비스는 살아 있지만 경제·돈·라이프스타일 소스로는 맞지 않는다. 필요하면 AI·테크 목록에서 다룬다 |
| Stratechery (Ben Thompson) | 존재하는 소스지만 빅테크 전략 분석 중심의 유료 뉴스레터다. 경제·생활 소재와 거리가 있고 뉴스레터·미디어 목록에 이미 있어서 중복을 없앴다 |

초안에서 **지어낸 소스나 운영이 중단된 소스는 발견되지 않았다.** 주요 문제는 **조직 개편과 서비스 개편을 반영하지 못한 URL·명칭**이었다(국가데이터처, 재정경제부, 정부24+ 혜택알리미, 한경 컨센서스, 오픈서베이 리포트 경로). 모두 위 표에서 고쳤다.

### 이번에 확인하지 못한 것 (후속 확인 권장)
2026-09-30 재검증 후 남은 항목만 적는다. 해결된 항목은 6장에 있다.
- 연합뉴스 공식 RSS 안내 페이지(피드 주소는 제3자 문서로만 확인), 뽐뿌 공식 RSS 주소, 한국은행 RSS 제공 여부
- 세븐일레븐 인스타 핸들
- WSJ·Reuters·The Economist·Business Insider의 X 핸들 페이지, 조선비즈·머니투데이의 2026년 운영(대형 매체라 존재는 확실)
- 국토부 K-패스·'모두의 카드'의 2026-10 이후 환급 기준(국토부 원문)

---

## 5. 출처 (이번 검증에 쓴 검색 결과)

**조직·정책 개편**
- [국가데이터처 공식 홈페이지 mods.go.kr](https://mods.go.kr/) · [통계청→국가데이터처 승격 기사(부산파이낸셜뉴스)](https://busan.fnnews.com/news/202510161047418863) · [이코노마이스: 소속기관 명칭 개편](https://www.emice.co.kr/news/articleView.html?idxno=8594) · [KOSIS](https://kosis.kr/)
- [정책브리핑: 2026년 기획재정부가 재정경제부·기획예산처로](https://www.korea.kr/news/policyNewsView.do?newsId=148957232) · [재정경제부 mofe.go.kr](https://mofe.go.kr/) · [파이낸셜신문: 재정경제부·기획예산처 출범](https://www.efnews.co.kr/news/articleView.html?idxno=126347)
- [정책브리핑: 정부24 전면 개편](https://www.korea.kr/news/policyNewsView.do?newsId=148945743) · [정부24+ 혜택알리미](https://plus.gov.kr/portal/benefitV2/) · [보조금24 옛 주소](https://www.gov.kr/portal/rcvfvrSvc/main)

**매체·RSS**
- [한경 컨센서스(현 주소)](https://markets.hankyung.com/consensus) · [한경닷컴 RSS](https://www.hankyung.com/feed)
- [연합뉴스 RSS 사용 사례(GitHub 문서, 검색 스니펫만 참고)](https://github.com/seokhoonj/newswatcher/blob/main/docs/korean-news-rss.md)
- [Feeder: 매일경제 경제·금융 피드](https://feeder.co/discover/11aec2568c/mk-co-kr)
- [정책브리핑 RSS 서비스](https://www.korea.kr/etc/rss.do) · [정책브리핑 뉴스레터](https://www.korea.kr/newsletter/)

**커뮤니티**
- [교보문고 저자 소개(월재연 운영자 맘마미아)](https://store.kyobobook.co.kr/person/detail/1112756601) · [모아요넷: 맘스홀릭베이비](https://www.moayo.net/p-moayo-140)
- [와우테일: 시소, 커리어리 운영사 퍼블리 인수](https://wowtale.net/2024/09/20/229892/) · [한국경제: 시소, 퍼블리 인수합병](https://www.hankyung.com/article/202409229690i)
- [에펨코리아 핫딜](https://www.fmkorea.com/hotdeal) · [알구몬 포럼: 에펨코리아 핫딜 수집 관련](https://www.algumon.com/forum/t/%EC%97%90%ED%8E%A8%EC%BD%94%EB%A6%AC%EC%95%84-%ED%95%AB%EB%94%9C-%EC%B6%94%EA%B0%80/17352) · [핫딜 사이트 비교(알구몬 수집 대상)](https://ohtaku.net/%EC%83%9D%ED%99%9C-%EC%A0%95%EB%B3%B4/%EB%BD%90%EB%BF%8C-%EC%95%8C%EA%B5%AC%EB%AA%AC-%EA%B0%99%EC%9D%80-%ED%95%AB%EB%94%9C-%EC%82%AC%EC%9D%B4%ED%8A%B8-%EC%88%9C%EC%9C%84-top-5/)

**트렌드·리포트**
- [대학내일20대연구소: Z세대 트렌드 2026](https://www.20slab.org/Archives/38969) · [2026 앱테크·해외여행·수면 소비 트렌드](https://www.20slab.org/Archives/39017) · [캐릿](https://www.careet.net/Content/Editor/2156)
- [오픈서베이 카페 트렌드 리포트 2026](https://blog.opensurvey.co.kr/trendreport/cafe-2026/) · [오픈서베이 트렌드리포트 목록](https://blog.opensurvey.co.kr/tag/%ED%8A%B8%EB%A0%8C%EB%93%9C%EB%A6%AC%ED%8F%AC%ED%8A%B8/)
- [트렌드모니터](https://www.trendmonitor.co.kr/) · [엠브레인 트렌드모니터 채널](https://embrain.com/kor/channel/trend) · [매드타임스: 2026 직장 내 세대 분리 조사](https://www.madtimes.co.kr/news/articleView.html?idxno=19067)
- [ZDNet Korea: 썸트렌드 MCP 출시(2026-03)](https://zdnet.co.kr/view/?no=20260318163329) · [헬로티: 썸트렌드 ChatGPT Apps 승인](https://www.hellot.net/news/article.html?no=112911)
- [한국경제: 트렌드 코리아 2027 권태사회](https://www.hankyung.com/article/2026093056441) · [여성신문: 2027 10대 키워드](https://www.womennews.co.kr/news/articleView.html?idxno=282795) · [독서신문: 출간 기념 전시·강연](https://www.readersnews.com/news/articleView.html?idxno=200649)
- [KB금융 2025 한국 부자 보고서](https://www.kbfg.com/kbresearch/report/reportView.do?reportId=2000551) · [이코노미사이언스 보도](https://www.e-science.co.kr/news/articleView.html?idxno=118634) · [하나금융연구소 2025 대한민국 웰스 리포트](https://www.hanaif.re.kr/boardDetail.do?hmpeSeqNo=36521)

**뉴스레터·크리에이터·기업 콘텐츠**
- [어피티](https://uppity.co.kr/) · [어피티 머니레터 아카이브](https://uppity.co.kr/category/newsletter/moneyletter/) · [어피티 구독](https://uppity.co.kr/subscription/)
- [토스피드](https://toss.im/tossfeed) · [토스피드 인스타 @toss_feed](https://www.instagram.com/toss_feed/)
- [아주경제: 371만 구독자 슈카(2026-06)](https://www.ajunews.com/view/20260615091644935) · [슈카월드 YouTube](https://www.youtube.com/@syukaworld/featured)

**유통·공공 데이터**
- [CU 인스타 @cu_official](https://www.instagram.com/cu_official/?hl=ko) · [GS25 인스타 @gs25_official](https://www.instagram.com/gs25_official/) · [GS25 X @funGS25](https://x.com/funGS25)
- [다이소몰](https://www.daisomall.co.kr/) · [다이소몰 신상](https://www.daisomall.co.kr/ds/prir) · [한국NGO신문: 다이소몰 2026 상반기 결산](https://www.ngonews.kr/news/articleView.html?idxno=232300)
- [KOTRA 해외시장뉴스](https://dream.kotra.or.kr/kotranews/index.do) · [참가격](https://www.price.go.kr/) · [온통청년](https://www.youthcenter.go.kr/)

**내부 참고**: `/home/user/insta/research/sources/source-tracing.md` (에크케 DART 공시 카드, 비즈까페 Bloomberg·FT 인용 사례)

---

## 6. 재검증(2026-09-30)

### 6-1. 방법
- 1차 검증에서 "미검증"으로 남았거나 근거 링크가 없던 항목을 다시 확인했다. Top 10과 Tier-1 항목을 먼저 보고, 남은 예산으로 나머지를 봤다. WebSearch는 **40회**(한도 전부) 썼다.
- 원문 페이지를 직접 열지 않고 검색 결과(제목·URL·스니펫·요약)만 근거로 삼았다. GitHub 페이지는 스니펫만 참고했다.
- 표의 검증 칸에 "재검증"이 붙은 항목이 이번에 바뀌었다. **제거한 항목은 없고**, 지어낸 소스도 이번에 새로 발견되지 않았다.

### 6-2. Top 10·Tier-1 결과

| 항목 | 이전 표기 | 재검증 결과 | 조치 |
|---|---|---|---|
| 연합뉴스 경제 RSS | 검증(스니펫 기준) | `yna.co.kr/rss/economy.xml`은 제3자 문서(GitHub 등)에만 나온다. 연합뉴스 공식 RSS 안내 페이지는 두 번 검색해도 나오지 않았다 | **부분 검증으로 하향**. "등록 전 피드가 열리는지 확인" 문구 추가 |
| 네이버 뉴스 경제 랭킹 | 미검증 | 네이버는 2020-10-23에 발표하고 2020-11부터 전체 '많이 본 뉴스'와 **섹션별 '많이 본 뉴스'를 없앴다**. 지금은 언론사별 랭킹만 있다. 따라서 "경제 랭킹"이라는 메뉴는 없다. news.naver.com은 Similarweb 기준 2026-03 국내 뉴스·미디어 사이트 1위 | **설명 수정**: 이름을 "경제 섹션 + 언론사별 랭킹"으로 바꾸고 방법·주의를 고침. 1-5 루틴과 Top 10 2위 문구도 수정 |
| 정책브리핑 보도자료 RSS | 검증(근거 링크 부족) | RSS 서비스 페이지(korea.kr/etc/rss.do) 검색 결과에서 `korea.kr/rss/pressrelease.xml` 확인. 보도자료 목록 페이지도 확인 | 확인. 근거 링크 추가 |
| 뽐뿌 재테크포럼 | 미검증 | 재테크포럼(게시판 ID `money`)이 있다. 2026-06 연재글 "26년 6월 신용카드 캐시백 이벤트 비교"가 있고, 2026-09에도 활동한다. RSS는 사용자 글에 `ppomppu.co.kr/rss.php?id=게시판ID` 형식만 나온다 | **검증으로 상향**. 게시판 URL 추가. RSS 주소는 미확인으로 둠 |
| 알구몬 | 검증 | 웹(algumon.com/n/deal)이 운영 중이고, 안드로이드 앱은 2026-09-01에 업데이트됐다(v0.7.17, 구글 플레이 검색 결과 기준) | 확인. 2026 활동 근거 추가 |
| DART 전자공시 | 미검증 | 금감원이 운영하는 dart.fss.or.kr와 OpenDART 오픈API(opendart.fss.or.kr) 확인. OpenDartReader 2026 개정판 문서도 있다 | **검증으로 상향** |
| 정부24+ 혜택알리미 | 검증 | plus.gov.kr/portal/benefitV2/의 페이지 제목이 "혜택알리미". 정책브리핑 기사 「혜택알리미, 정부24에서 시작하세요!」가 있다. 보조금24의 맞춤 검색 기능이 혜택알리미로 옮겨갔다(로그인하면 '나의 혜택', 비로그인은 '간편 찾기') | 확인. 설명 보강 |
| 네이버 데이터랩 | 미검증 | 검색어트렌드·쇼핑인사이트·지역 통계·댓글 통계를 제공한다. 조회 기간의 최댓값을 100으로 둔 상대지수이고, 절대 검색량은 웹과 API 어디에도 없다 | **검증으로 상향**. 주의 문구 보강 |
| 국가데이터처 개편 | 검증 | 2025-10-01 출범. 기획재정부 외청에서 국무총리 소속으로 바뀌었다(통계청 35년 만의 승격) | 확인. 소속 변경 내용 추가 |
| 재정경제부/기획재정부 분리 | 검증 | 2026-01-02 재정경제부·기획예산처 출범(2008년 통합 후 18년 만). 예산·기금·국가채무는 기획예산처가 맡는다. **그린북은 재정경제부 경제정책국이 계속 낸다**(2026년 9월호, 2026-09-11 발표) | 확인. "그린북 발간 주체" 후속 확인 항목 해결 |
| 한국은행 + ECOS (Top 10 5위) | 미검증 | 보도자료 게시판과 ECOS가 운영 중이고, 2026-09 「금융안정 상황」이 게시됐다 | **검증으로 상향**. RSS 제공 여부는 여전히 미확인 |
| 온통청년 (Top 10 6위) | 검증(홈 링크만) | 중앙·지자체 청년정책 약 3,000개를 실시간으로 모은다. 청년정책 통합검색 메뉴가 있다 | 확인. 근거 추가 |
| Bloomberg·FT (Top 10 10위) | 미검증 | x.com/business, x.com/ft 계정 확인 | **검증으로 상향**. WSJ·Reuters는 핸들 페이지를 확인하지 못해 미검증으로 둠 |

### 6-3. 그 밖의 항목

| 항목 | 결과 |
|---|---|
| 네이버 증권 리서치 | 서비스명이 **네이버페이 증권**으로 바뀌었다(도메인 finance.naver.com은 그대로). 명칭 수정. /research 경로 자체는 확인하지 못함 |
| 금융위원회 | 2025-09-25에 금융위 해체·금감원 분리 개편안이 **철회**되어 두 기관 모두 현 체제를 유지한다. 청년미래적금은 2026-06-22 출시(은행 블로그 기준). 검증. "금융당국 개편 결과" 후속 확인 항목 해결 |
| 금감원 + 파인 | fine.fss.or.kr 확인(계좌 통합조회·숨은 금융자산·금융상품 비교). 초안의 메뉴명 "금융상품 한눈에"는 확인하지 못해 일반 표현으로 고침 |
| 국토교통부 | 2026년에 K-패스에 정액형 '모두의 카드'가 추가됐다(블로그·나무위키 기준). 2026-04~09 한시 환급 확대 정리가 있어 10월 이후 기준 확인 문구를 넣었다. 부분 검증 |
| 한국부동산원 + 청약홈 | 주간아파트가격동향 페이지, 통계포털 R-ONE, 청약홈 청약캘린더 확인. 검증 |
| 국세청 | nts.go.kr에 「2026년 근로장려금 반기 신청·지급제도」가 게시돼 있다. 검증 |
| 클리앙 알뜰구매·더쿠 핫게·블라인드 | 게시판 URL 확인. 더쿠는 2026-05·07 화제 글, 블라인드는 '토픽 베스트' 페이지까지 확인. 검증 |
| 구글 트렌드 | trends.google.com/trending?geo=KR "Trending now" 페이지 확인. 검증 |
| 롱블랙·더밀크 | 2026 활동 확인(롱블랙: 사이트·앱 운영과 새 기능 '롱블랙 플레이', 더밀크: CES 2026 미디어 파트너 세션 연사, 2026년 기사). 검증 |
| 올리브영·어피티·세븐일레븐 인스타 | 올리브영 IG @oliveyoung_official, 어피티 IG @uppity.official 확인. 세븐일레븐은 X @711korea와 페이스북만 확인했고 인스타 핸들은 여전히 미확인 |
| Morning Brew·Visual Capitalist·CB Insights | 셋 다 2026년에 운영 중. Visual Capitalist는 별도 라이선스 사이트가 있다. 검증 |
| 조선비즈·머니투데이·WSJ·Reuters·The Economist·Business Insider | 검색 예산이 떨어져 재검증하지 못함. 미검증(확신 높음)으로 둠 |

### 6-4. 재검증 출처

**Top 10·Tier-1**
- 연합뉴스 RSS(GitHub, 스니펫만 참고): [seokhoonj/newswatcher korean-news-rss.md](https://github.com/seokhoonj/newswatcher/blob/main/docs/korean-news-rss.md) · [hdnauth/newsServer](https://github.com/hdnauth/newsServer)
- 네이버 랭킹 폐지: [뉴스핌: 네이버 '많이 본 뉴스' 폐지(2020-10-23)](https://www.newspim.com/news/view/20201023000042) · [한국일보: '언론사별 많이 본 뉴스'로 전환](https://www.hankookilbo.com/News/Read/A2020102309130003730) · [디지털투데이](https://www.digitaltoday.co.kr/news/articleView.html?idxno=250556) · [온라인 뉴스 순위 1위는 네이버 뉴스(다음 뉴스)](https://v.daum.net/v/3DHTMPWISY)
- 정책브리핑: [RSS 서비스](https://www.korea.kr/etc/rss.do) · [보도자료 목록](https://www.korea.kr/briefing/pressReleaseList.do)
- 뽐뿌: [재테크포럼 2026-06 연재글](https://m.ppomppu.co.kr/new/bbs_view.php?id=money&no=544568&ppck=1) · [뽐뿌 RSS 파싱(OpenCode)](http://opencode.co.kr/bbs/board.php?bo_table=gnu4_tips&wr_id=908) · [뽐뿌 조건별 RSS 만들기](http://m.ppomppu.co.kr/new/bbs_view.php?id=etc_info&no=25885)
- 알구몬: [알구몬 최신 핫딜](https://www.algumon.com/n/deal) · [구글 플레이 알구몬](https://play.google.com/store/apps/details?id=com.algumon.app&hl=en_US)
- DART: [전자공시시스템](https://dart.fss.or.kr/) · [OpenDART 오픈API 소개](https://opendart.fss.or.kr/intro/main.do) · [OpenDartReader(위키독스, 2026 개정판)](https://wikidocs.net/230304)
- 혜택알리미: [혜택알리미 홈](https://plus.gov.kr/portal/benefitV2/) · [정책브리핑: 혜택알리미, 정부24에서 시작하세요!](https://www.korea.kr/news/policyNewsView.do?newsId=148958857) · [비건뉴스: 정부24 혜택알리미 이용법](https://www.vegannews.co.kr/news/article.html?no=387802)
- 네이버 데이터랩: [TBWA 데이터랩: 네이버 데이터랩 키워드 분석](https://seo.tbwakorea.com/blog/naver-datalab/) · [오픈애즈: 네이버 데이터랩 키워드 분석하기](https://openads.co.kr/content/contentDetail?contsId=9746) · [SocialCrawl: 데이터랩 API](https://www.socialcrawl.dev/ko/blog/naver-datalab-api)
- 국가데이터처: [전자신문: 1일부터 국가데이터처 출범](https://www.etnews.com/20250930000292) · [아시아경제: 내달 1일 공식 출범](https://www.asiae.co.kr/article/economic-general/2025093013434468167)
- 재정경제부: [주간한국: 재경부·기획예산처 공식 출범](https://weekly.hankooki.com/news/articleView.html?idxno=7143747) · [18년 만에 쪼개진 기재부(네이트 뉴스)](https://m.news.nate.com/view/20260102n26535) · [2026년 9월 최근 경제동향(네이트 뉴스)](https://m.news.nate.com/view/20260911n22511) · [재정경제부 보도·참고자료](https://mofe.go.kr/nw/nes/nesdta.do?bbsId=MOSFBBS_000000000028&menuNo=4010100)
- 한국은행: [보도자료 목록](https://www.bok.or.kr/portal/singl/newsData/list.do?menuNo=201263) · [ECOS](https://ecos.bok.or.kr/)
- 온통청년: [복지로: 온통청년 개통, 3000여 개 사업 검색](https://www.bokjiro.go.kr/ssis-tbu/cms/pc/news/news/1307857_1114.html) · [청년정책 통합검색](https://www.youthcenter.go.kr/youthPolicy/ythPlcyTotalSearch)
- 해외 매체 X: [Bloomberg @business](https://x.com/business) · [Financial Times @FT](https://x.com/ft) · [Hypefury: 금융 X 계정 목록(WSJ 팔로워 수치)](https://hypefury.com/blog/en/finance-twitter-accounts-2023/)

**그 밖의 항목**
- 네이버페이 증권: [나무위키: 네이버페이 증권](https://namu.wiki/w/%EB%84%A4%EC%9D%B4%EB%B2%84%ED%8E%98%EC%9D%B4%20%EC%A6%9D%EA%B6%8C)
- 금융당국·금융상품: [헤럴드경제: 조직개편 원위치](https://biz.heraldcorp.com/article/10583722) · [김·장: 금융감독체계 개편방안 철회 결정의 의미](https://www.kimchang.com/ko/insights/detail.kc?sch_section=4&idx=33051) · [토스뱅크: 청년미래적금](https://www.tossbank.com/articles/youth-grow-up-account) · [KB Think: 청년미래적금](https://kbthink.com/youth-guide/youth-future-savings.html)
- 파인: [FINE](https://fine.fss.or.kr/) · [파인 서비스 소개](https://fine.fss.or.kr/fine/main/contents.do?menuNo=900212)
- 국토부 K-패스: [나무위키: K-패스](https://namu.wiki/w/K-%ED%8C%A8%EC%8A%A4) · [삼쩜삼 블로그: 모두의카드 추가 환급 기간 연장](https://blog.3o3.co.kr/kpass_all_card_refund/)
- 부동산원·청약홈: [주간아파트가격동향](https://www.reb.or.kr/reb/cm/cntnts/cntntsView.do?mi=10001&cntntsId=1308) · [R-ONE](https://www.reb.or.kr/r-one/) · [청약홈 청약캘린더](https://www.applyhome.co.kr/ai/aib/selectSubscrptCalenderView.do)
- 국세청: [2026년 근로장려금 반기 신청·지급제도](https://www.nts.go.kr/nts/na/ntt/selectNttInfo.do?nttSn=1352882&mi=2457)
- 커뮤니티: [클리앙 알뜰구매](https://www.clien.net/service/board/jirum) · [텔레그램 clienjirum](https://t.me/s/clienjirum) · [더쿠 HOT](https://theqoo.net/hot) · [더쿠: 2026 상반기 유행음식 빙고판](https://theqoo.net/hot/4270834752) · [블라인드 토픽 베스트](https://www.teamblind.com/kr/topics/%ED%86%A0%ED%94%BD-%EB%B2%A0%EC%8A%A4%ED%8A%B8)
- 구글 트렌드: [Trending Now (KR)](https://trends.google.com/trending?geo=KR)
- 롱블랙·더밀크: [롱블랙](https://longblack.co/) · [롱블랙 App Store](https://apps.apple.com/kr/app/%EB%A1%B1%EB%B8%94%EB%9E%99-longblack/id6450910866) · [벤처스퀘어: 더밀크 CES 2026 연사](https://www.venturesquare.net/1029989) · [더밀크: 손재권 "2026년은 혁명과 창조의 해"](https://www.themiilk.com/articles/a7f3c4eea)
- 인스타·X 핸들: [올리브영 IG @oliveyoung_official](https://www.instagram.com/oliveyoung_official/) · [올리브영 X @oliveyoung](https://x.com/oliveyoung) · [어피티 IG @uppity.official](https://www.instagram.com/uppity.official/) · [어피티 YouTube](https://www.youtube.com/@uppity_official) · [세븐일레븐 X @711korea](https://x.com/711korea) · [세븐일레븐 페이스북](https://www.facebook.com/7elevenkorea/photos_stream)
- 해외 뉴스레터·데이터: [Morning Brew 최신호](https://www.morningbrew.com/issues/latest) · [ReadLess: Best Business Newsletters 2026](https://www.readless.app/newsletters/best-business-newsletters-2025) · [VC Stack: 뉴스레터 목록(CB Insights 포함)](https://www.vcstack.com/newsletters-podcasts-more) · [Visual Capitalist 2026 Global Forecast Report](https://www.visualcapitalist.com/2026-global-forecast-report/) · [Visual Capitalist 라이선스](https://licensing.visualcapitalist.com/product/the-global-economy-by-ppp-2026/)
