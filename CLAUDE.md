# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 저장소 목적

상장 기업에 대한 **투자 분석 저널**. 각 분석은 실제 투자 의사결정에 활용 가능한 정량적/정성적 정보를 담은 마크다운 파일로 저장.

## 파일명 규칙

- 형식: `YYYY-MM-DD-{회사명}.md`
- 예시: `2026-01-09-aerovironment.md`
- 회사명은 소문자, 하이픈 구분
- 날짜는 분석 작성일

## 문서 구조

각 투자 분석 문서는 다음 섹션 포함:

1. **헤더**
   - 회사명 (영문), 티커
   - 현재 주가 (USD 및 KRW 병기)
   - 시가총액 (USD 및 KRW 병기)
   - 분석 일자
   - 52주 최고/최저가

2. **1. 회사 개요**
   - 사업 분야 및 주요 제품/서비스 (매출 비중 포함)
   - 설립 연도, 본사 위치
   - 최근 12개월 주요 이벤트 (분기 실적, M&A, 제품 론칭 등)
   - 비즈니스 모델 (수익 구조)

3. **2. 재무 분석**
   - **실적 추이** (최근 4개 분기 + 전년 동기 비교)
     - 매출액 (YoY 성장률)
     - 영업이익/순이익 (마진율)
     - EPS 추이
   - **재무 건전성**
     - 부채비율, 유동비율
     - 현금 및 현금성 자산
     - FCF (Free Cash Flow)
   - **밸류에이션 지표**
     - P/E (현재 vs 역사적 평균 vs 업종 평균)
     - P/B, P/S
     - PEG Ratio
     - EV/EBITDA
   - **가이던스** (회사 제시 전망)
   - **배당** (배당률, 배당성향)

4. **3. 사업 현황 및 경쟁 환경**
   - **시장 규모 및 성장성**
     - TAM (Total Addressable Market)
     - 시장 성장률 (CAGR)
   - **경쟁 구도**
     - 주요 경쟁사 및 시장점유율
     - 경쟁 우위 (moat)
   - **주요 고객 및 계약**
   - **최근 뉴스 및 규제 이슈**

5. **4. 투자 포인트**
   - **Bull Case (강세 시나리오)**
     - 성장 동력
     - 구조적 우위
     - 촉매제 (catalyst)
   - **Bear Case (약세 시나리오)**
     - 주요 리스크 (사업, 재무, 규제, 거시경제)
     - 밸류에이션 리스크
   - **목표가 및 투자 의견**
     - 적정 밸류에이션 레인지
     - 리스크/보상 비율

6. **참고 자료**
   - IR 페이지, 실적 발표 자료
   - SEC Filings (10-K, 10-Q)
   - 애널리스트 리포트 (가능한 경우)
   - 뉴스 기사 및 기타 출처 (실제 URL만)

7. **면책 조항**
   - 본 문서는 투자 권유가 아니며, 정보 제공 목적임
   - 투자 결정은 본인 책임 하에 수행

## 작성 프로세스

1. **웹 검색으로 최신 정보 수집**
   - **필수 정보**
     - 현재 주가, 시가총액, 52주 최고/최저가
     - 최신 분기/연간 실적 (Earnings Release)
     - 가이던스 및 경영진 코멘트
     - SEC Filings (10-K, 10-Q) 주요 내용
   - **산업 및 경쟁 분석**
     - 시장 규모 및 성장률 (업계 리포트)
     - 주요 경쟁사 및 시장점유율
     - 산업 트렌드 및 규제 변화
   - **정성적 정보**
     - 최근 6-12개월 주요 뉴스
     - 애널리스트 의견 (컨센서스 목표가)
     - 경영진 변화, M&A, 신규 계약 등

2. **정보의 신뢰성 및 최신성**
   - IR 페이지, SEC Filings 우선 활용
   - 뉴스는 최근 6개월 이내 자료 중심
   - 재무 데이터는 최신 분기 실적 기준
   - 출처가 불명확한 정보는 제외

3. **언어 및 표기 규칙**
   - **언어**: 한국어 작성
   - **고유명사**: 회사명, 티커, 제품명은 영어 유지
   - **재무 용어**: 영어 약어 사용 (P/E, ROE, FCF 등)
   - **비즈니스 용어**: 주요 개념은 한/영 병기
   - **통화 표기 (중요)**:
     - 모든 달러 금액은 원화 병기 필수
     - 형식: `$100M (약 1,400억원)` 또는 `$50.5 (약 70,000원)`
     - 환율은 분석 시점 기준 적용 (예: USD/KRW 1,400)
     - 시가총액, 매출, 주가 등 모든 금액에 적용
     - 백만/십억 단위는 M/B로 표기 (예: $1.5B = 약 2.1조원)

4. **분석의 객관성 유지**
   - 팩트와 의견 명확히 구분
   - Bull Case와 Bear Case 균형있게 서술
   - 과도한 낙관론이나 비관론 지양
   - 불확실성 있는 정보는 명시

## Git 워크플로우

분석 완료 시:

```bash
git add YYYY-MM-DD-{company}.md
git commit -m "Add {Company} ({TICKER}) investment analysis

- Company overview and recent developments
- Financial analysis with recent results
- Business landscape and competitive positioning
- Investment thesis with strengths and risks

Co-Authored-By: Claude Sonnet 4.5 <noreply@anthropic.com>"
git push origin main
```
