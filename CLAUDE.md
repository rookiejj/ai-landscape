# AI Players — 유지보수 컨텍스트

인터랙티브 레퍼런스 페이지: AI 생태계를 실질적으로 주도하는 기업 10선과 
그들의 제품·프로그램 정리.

- Live: https://rookiejj.github.io/ai-players
- 파일: index.html(렌더링, 거의 수정 안 함) / data.js(업데이트 대상) / updates.js(콘텐츠 변경 로그) / README.md

## 선정 원칙
"빅테크"가 아닌 AI 생태계 실질 플레이어 기준:
프론티어 모델 / 생태계 영향력 / 인프라 지배력 / 오픈소스 영향 / 시장 규모
→ IBM·Oracle보다 Anthropic·xAI·Mistral 우선.

## 현재 수록 기업 (10)
OpenAI, Anthropic, Google DeepMind, xAI, Meta AI,
Microsoft, NVIDIA, Amazon AWS, Apple, Mistral AI

## 배지 체계 (BL 객체)
llm / img / vid / agt / code / ui / hw / sci

## data.js 구조
const data = [{
  rank, name, url, type, focus,
  products: [{ name, url, isNew, badges:[], desc }]
}]

## 작성 규칙
- isNew: 이번 업데이트 신규 항목만 true. 출시 4~6주 경과 시 false로 내림.
- desc: 기술 스펙 + 시장 맥락 함께. 단순 스펙 나열 금지.
- index.html 상단 "마지막 업데이트" 날짜와 푸터 연도는 수정일 기준으로 갱신.
- updates.js: 콘텐츠 변경(모델·제품·펀딩·인수 등)은 여기에 날짜별 기록.
- README.md 버전 히스토리: 소스코드 구조·파일 트리·UI 로직 등 기술적 변경만 기록.

## 업데이트 작업 체크리스트 (매 요청 시 이 순서로)
1. 웹검색으로 오늘 날짜 기준 각 기업의 최신 모델/제품/펀딩/인수 확인
2. data.js 수정 — 변경된 기업만 최소 diff로
3. 이전 NEW 배지들을 isNew:false 로 내리기
4. 새 항목에 isNew:true 부여
5. index.html의 업데이트 날짜·연도 갱신 (수정 필요 시에만)
6. updates.js에 콘텐츠 변경 사항 기록 (제품·모델·펀딩·인수 등, 전문적 톤)
7. README.md 버전 히스토리 — 기술적 변경이 있을 때만 추가 (코드 구조·파일 트리·UI 로직 변경 등)
8. 변경 사항 요약을 채팅으로 보고 (커밋은 내가 직접)

### 변경 로그 이원화 원칙
- **updates.js** — 일반 사용자 대상. 어떤 기업의 무엇이 왜 변경되었는지를 전문적이고 읽기 쉬운 문체로 기록. 기술적 세부사항(파일 구조, 리팩토링 등) 제외.
- **README.md 버전 히스토리** — 개발자/기여자 대상. 소스코드 구조 변경, 파일 추가/삭제, UI 로직 수정 등 기술적 변경만 기록.

## 마지막 업데이트 기록
- 2026-04-12: Anthropic $300억 ARR로 OpenAI 첫 추월, Coefficient Bio 인수,
  Google·Broadcom 3.5GW 컴퓨트 딜, Gemini 3.1 Ultra(200만 토큰),
  OpenAI ChatGPT Pro $100 요금제·TBPN 인수,
  Mistral Forge·파리 데이터센터 $830M. Grok 4.20·Imagine NEW 해제
- 2026-04-11: Claude Mythos+Glasswing, Meta Muse Spark, Gemma 4,
  Grok 4.20 멀티에이전트, GPT-5.5 Spud, Mistral Small 4 등