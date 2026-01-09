# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 저장소 목적

상장 기업에 대한 **투자 분석 저널**. 각 분석은 마크다운 파일로 저장.

## 파일명 규칙

- 형식: `YYYY-MM-DD-{회사명}.md`
- 예시: `2026-01-09-aerovironment.md`
- 회사명은 소문자, 하이픈 구분
- 날짜는 분석 작성일

## 문서 구조

각 투자 분석 문서는 다음 섹션 포함:

1. **헤더**
   - 회사명, 티커, 주가, 시가총액

2. **1. 회사 개요**
   - 사업 분야 및 주요 제품/서비스
   - 설립 연도, 본사 위치
   - 최근 주요 이벤트

3. **2. 재무 분석**
   - 최근 분기/연간 실적
   - 재무 비율 (P/E, P/B, ROE 등)
   - 가이던스, 백로그, 현금흐름

4. **3. 사업 현황**
   - 주요 고객 및 계약
   - 경쟁사 및 시장 포지션
   - 최근 뉴스

5. **4. 투자 포인트**
   - 강점
   - 약점 및 리스크
   - 성장 가능성

6. **참고 자료**
   - 웹 검색 결과 링크 (실제 URL만)

7. **면책 조항**

## 작성 프로세스

1. **웹 검색으로 최신 정보 수집**
   - 회사 개요, 재무 실적, 시가총액
   - 경쟁사, 시장 포지션
   - 최근 뉴스, 규제 변화
   - Earnings release, IR 페이지

2. **언어**
   - 한국어 작성
   - 회사명, 티커, 재무 용어는 영어 유지
   - 주요 비즈니스 용어는 한/영 병기

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
