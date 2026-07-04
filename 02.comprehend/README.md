# AWS Comprehend
##정의 : 비정형 텍스트를 분석하여 의미, 감정, 엔터티, 핵심구문, 개인정보 등을 추출할 수 있도록 제공하는 AWS의 관리형 NLP 서비스

## 핵심가치
- 사전학습된 NLP 기능 제공
- 인프라 운영 없이 API 호출로 사용
- 텍스트를 구조화된 정보로 변환
- 빠른 PoC와 업무 자동화에 유리

- 실제 가치는 분석 결과를 검색, 라우팅, 알림, 검토, 대시보드와 연결하는 아키텍쳐에서 나온다.

## 기본 처리 흐름
- 텍스트 입력 -> API 분석 수행 -> JSON 결과 반환 -> 업무 시스템 후처리

## 주요 기능 카테고리
1) Sentiment 2) Entities 3) Key Pharases 4) PII&Classify

## 실무에서의 고려사항
-보안, 비용, 도메인 적합성, 사람 검토 체계

# 실습

## 실습 목표
- Amazon Comprehend의 다양한 자연어 처리(NLP) API를 활용하여 텍스트 분석 기능을 학습하였다.

## 실습 내용
| Lab   | 내용                  | 주요 API                                                                         |
| ----- | ------------------- | ------------------------------------------------------------------------------ |
| Lab 1 | 언어 감지 및 감성 분석       | `detect_dominant_language()`, `detect_sentiment()`, `batch_detect_sentiment()` |
| Lab 2 | 개체명 인식 및 핵심 문구 추출   | `detect_entities()`, `detect_key_phrases()`                                    |
| Lab 3 | 개체별 감성 분석 및 개인정보 탐지 | `detect_targeted_sentiment()`, `detect_pii_entities()`                         |
| Lab 4 | 품사 분석 및 종합 분석 파이프라인 | `detect_syntax()`                                                              |
| Lab 5 | 토픽 모델링 개념 및 군집화     | TF-IDF, K-Means, Topic Modeling                                                |



