# AI Players — 유지보수 컨텍스트

인터랙티브 레퍼런스 페이지: AI 생태계를 실질적으로 주도하는 기업 10선과 
그들의 제품·프로그램 정리.

- Live: https://rookiejj.github.io/ai-players
- 파일: index.html(렌더링, 거의 수정 안 함) / data.js(업데이트 대상) / README.md

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
- README.md의 변경 로그 섹션에도 요약 한 줄 추가.

## 업데이트 작업 체크리스트 (매 요청 시 이 순서로)
1. 웹검색으로 오늘 날짜 기준 각 기업의 최신 모델/제품/펀딩/인수 확인
2. data.js 수정 — 변경된 기업만 최소 diff로
3. 이전 NEW 배지들을 isNew:false 로 내리기
4. 새 항목에 isNew:true 부여
5. index.html의 업데이트 날짜·연도 갱신 (수정 필요 시에만)
6. README.md 변경 로그 한 줄 추가
7. 변경 사항 요약을 채팅으로 보고 (커밋은 내가 직접)

## 마지막 업데이트 기록
- 2026-04-11: Claude Mythos+Glasswing, Meta Muse Spark, Gemma 4,
  Grok 4.20 멀티에이전트, GPT-5.5 Spud, Mistral Small 4 등