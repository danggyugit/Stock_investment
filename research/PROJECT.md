# AI CapEx와 메모리 반도체 사이클 분석을 통한 Micron 및 SanDisk 투자전략 수립

## 프로젝트 목표

미국 빅테크 기업들의 AI 관련 CapEx 투자가 앞으로 언제까지 지속될 수 있는지 분석한다. 특히 2026/2027/2028년의 AI 관련 투자 규모와 지속 가능성을 데이터 기반으로 분석한다. 빅테크의 CapEx가 실제로 어떤 AI 인프라에 사용되는지 분석하고, 이를 DRAM/HBM/NAND/Enterprise SSD 수요와 연결한다. 이후 Micron과 SanDisk의 매출·영업이익·EPS·밸류에이션을 추정하고, 현재 주가와 비교하여 투자전략을 수립한다.

정량 분석 연결고리 (13단계):

거시경제 환경 → 빅테크 투자환경 → 빅테크 CapEx → AI 데이터센터 투자 → GPU/ASIC 투자 → 서버·네트워크 투자 → DRAM/HBM/NAND/eSSD 수요 → 메모리 가격·출하량 → Micron·SanDisk 매출 → 영업이익 → EPS → 밸류에이션 → 적정 주가 → 투자 전략

## 핵심 투자 가설

빅테크 AI CapEx가 2026년 이후에도 높은 수준으로 지속된다면 → AI 데이터센터·서버 투자 지속 → DRAM/HBM/NAND/eSSD 수요 증가 → 수요 증가+공급 제약 동시 발생 시 가격·수익성 개선 → Micron·SanDisk 매출·영업이익 증가 → 이것이 주가에 충분히 반영되지 않았다면 상승 여력 존재.

반대로 CapEx 투자 효율성 하락, AI 수익성 악화, 데이터센터 과잉투자 판단 시 → CapEx 둔화와 함께 메모리 사이클 정점 도달 가능성.

**검증 원칙: 가설을 무조건 긍정적으로 증명하려 하지 않는다. 긍정·부정 근거를 모두 수집하고, 최종 결론은 데이터에 따라 가설을 유지/수정/폐기한다.**

## 핵심 연구 질문 (20)

1. 현재 거시경제 환경은 빅테크의 AI CapEx 지속에 우호적인가?
2. 미국의 금리·경기·인플레이션·유동성은 2026~2028년 AI 투자를 어떻게 변화시킬 수 있는가?
3. 빅테크 AI CapEx는 2026년 이후에도 지속될 것인가?
4. 2026/2027/2028년 각 기업의 CapEx 규모는?
5. 공식 발표 CapEx / 컨센서스 / 자체 추정치를 구분하면 각각 얼마인가?
6. 빅테크 CapEx 중 AI 관련 비중은?
7. CapEx는 데이터센터/GPU/ASIC/서버/네트워크/스토리지/건설 중 어디에 사용되는가?
8. 각 CapEx 항목은 DRAM/HBM/NAND/eSSD 수요와 어떻게 연결되는가?
9. AI 서버 증가에 따른 DRAM 수요 증가 규모는?
10. AI GPU/ASIC 증가에 따른 HBM 수요 증가 규모는?
11. AI 데이터센터 증가에 따른 NAND/eSSD 수요 증가 규모는?
12. 이 수요가 Micron의 DRAM/HBM 사업에 미치는 영향은?
13. 이 수요가 SanDisk의 NAND/eSSD 사업에 미치는 영향은?
14. 공급·수요를 고려할 때 2026~2028 메모리 가격은 어떻게 변화하는가?
15. Micron의 2026~2028 매출·영업이익·EPS 추정은?
16. SanDisk의 2026~2028 매출·영업이익·EPS 추정은?
17. 현재 주가는 미래 이익을 얼마나 선반영하고 있는가?
18. 2027~2028년에도 주가 상승이 지속되기 위한 조건은?
19. 현재 강세 사이클이 종료될 수 있는 조건은?
20. Micron과 SanDisk 중 위험 대비 기대수익이 더 높은 기업은?

## 분석 기간

과거 2022~2025 / 현재 2026 / 전망 2027~2028 (가능 시 2029 장기 사이클 확인)

## 분석 대상 기업

- 빅테크: Google/Alphabet, Microsoft, Amazon, Meta, Oracle (+필요 시 Apple, Tesla, CoreWeave 등)
- 메모리: Micron, SanDisk (+산업 참고: SK Hynix, Samsung, Kioxia, WDC 과거 NAND 데이터)

## 에이전트팀 구성 (13개 역할)

| # | 역할 | 담당 | 실행 매핑 (.claude/agents) |
|---|---|---|---|
| 1 | CIO/총괄 투자전략가 | 취합·상충 판정·연결고리 논리 검증·최종 전략 (근거/반대근거/리스크/무효화조건/신뢰도 필수) | 팀장(오케스트레이터) 직접 |
| 2 | Macro Analyst | 지표 나열 금지 — 각 지표가 CapEx·메모리·밸류에이션에 미치는 영향 분석. 금리 3시나리오(하락/유지/상승)·경기 3시나리오(연착륙/침체/스태그) 필수. 산출: 환경 판정(우호/중립/비우호), 12·24개월 전망, 핵심 리스크 3 | macro-analyst |
| 3 | Market Analyst | 위험선호·수급이 MU/SNDK를 펀더멘털과 무관하게 움직이는지 | market-analyst + flow-analyst |
| 4 | News & Earnings Analyst | 실적·컨콜: 명시 사실/추론 가능 내용/컨센 대비 차이/직전 가이던스 대비 변화 구분 | news-analyst |
| 5 | Big Tech CapEx Analyst | 5사 과거(2022~2026)·미래(2026~2029) CapEx, CapEx/Revenue, CapEx/OCF, 구성. 2027~28은 반드시 시나리오 | company-analyst |
| 6 | AI Infrastructure Analyst | CapEx→서버/GPU/ASIC→메모리 탑재량 정량화 (AI 서버 출하량, 서버당 DRAM, GPU당 HBM, 서버 1대당 메모리 가치 — 가정 명시) | semiconductor-analyst |
| 7 | Memory Industry Analyst | DRAM/HBM/NAND 제품군별 수요·공급·가격·2026~28 전망 | semiconductor-analyst |
| 8 | Micron Analyst | 사업부별 분석 + 2026/27/28 Bull·Base·Bear 시나리오별 매출/영업이익/EPS | company-analyst |
| 9 | SanDisk Analyst | 동일 구조 (NAND/eSSD 중심) | company-analyst |
| 10 | Valuation Analyst | PER(현재/Forward/과거 사이클/정상화)·EV/EBITDA·P/B, 시나리오별 적정주가. 단일 PER 금지, 정상화 이익과 현재 이익 구분 | company-analyst + 팀장 |
| 11 | Technical Analyst | 주가·이평·RSI·옵션 포지셔닝. 펀더멘털과 분리, 단독 결론 금지 | technical-analyst + flow-analyst |
| 12 | Scenario Analyst | Bull/Base/Bear 종합 시나리오 + 주관적 확률 명시 | 팀장 직접 |
| 13 | Portfolio Manager | 조건부 전략: 분할매수 구간/추가매수 조건/비중축소 조건/무효화 조건 | 팀장 직접 |

## 최종 리포트 구성 (13개 섹션)

1. Executive Summary 2. 현재 투자 가설 3. 거시경제 분석 4. 빅테크 CapEx 분석(기업×연도 표, 실제값/가이던스/컨센/추정 구분) 5. CapEx 구성 분석 6. AI 인프라 수요 분석 7. 메모리 수요 분석(DRAM/HBM/NAND/eSSD) 8. Micron 분석 9. SanDisk 분석 10. 시나리오 분석 11. 현재 주가 평가 12. 투자 전략 13. 투자 가설 무효화 조건

## 분석 품질 규칙 (18)

1. 사실과 추정 구분 2. 데이터 날짜 명시 3. 숫자 출처 기록 4. 공식/컨센 구분 5. 불확실 수치는 범위 6. 2027~28은 시나리오 7. 단일 데이터로 결론 금지 8. 긍·부정 데이터 모두 조사 9. 가설 반박 근거 필수 탐색 10. "이 분석이 틀릴 가능성" 필수 검토 11. 데이터 부족 시 추정 금지·명시 12. 출처 불명 숫자는 핵심 계산 배제 13. CapEx→메모리 수요 연결 가정 명시 14. 계산 과정 보존 15. 매크로는 지표 나열 금지 16. 에이전트 간 영역 구분 17. 의견 상충 시 근거 비교 18. 최종 결론은 최낙관 시나리오가 아닌 확률·위험 기준

## 최종 결론 형식

핵심 결론(지속 가능성 높음/불확실/둔화 가능성 높음) · 거시환경 판정 · 연도별 CapEx 전망 · Micron 투자의견+근거 3 · SanDisk 투자의견+근거 3 · 상대 선호도(1·2위+근거) · 최중요 이벤트 3 · 가설 유지 조건 3 · 무효화 조건 3 · 신뢰도(0~100+근거)

---
본 프로젝트 산출물은 정보 제공 목적의 개인 리서치 보조 자료이며 투자 자문이 아니다. 투자 손익의 책임은 투자자 본인에게 있다.
