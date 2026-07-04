# AWS Bedrock
## 정의 : 다양한 Foundation Model(Claude, Llama 등)을 API 형태로 제공하여, 별도의 모델 학습이나 인프라 구축 없이 생성형 AI 애플리케이션을 개발할 수 있는 AWS의 완전관리형 서비스.

## 핵심가치
- 다양한 Foundation Model을 하나의 서비스에서 제공
- 모델 학습 없이 API 호출만으로 생성형 AI 활용
- 서버 및 인프라 관리 없이 빠른 AI 서비스 개발
- 동일한 인터페이스를 통해 다양한 모델 교체 가능
- 프롬프트 엔지니어링만으로 다양한 업무 자동화 가능
- 실제 가치는 생성형 AI를 기존 시스템(Lambda, API Gateway, Knowledge Base 등)과 연결하여 서비스화하는 데 있다.

## 기본 처리 흐름
- 사용자 입력 → Foundation Model 호출 → 생성 결과 반환 → 애플리케이션 후처리

## 실무에서의 고려사항
- 모델 선택, 토큰 비용, 응답 속도, 프롬프트 설계, 안정성
  
## 실습

### 실습 목표
- Amazon Bedrock을 활용하여 Foundation Model 호출, 프롬프트 엔지니어링, 챗봇 구현 과정을 학습하였다.

### Amazon Comprehend 실습 내용

1. Foundation Model 탐색 및 모델 호출
- Bedrock에서 사용 가능한 Foundation Model 목록 조회
- 'invoke_model()' API를 이용하여 Claude 모델 호출
- 'converse()' API를 이용한 멀티턴 대화 구현
- Temperature와 Max Tokens 등의 추론 파라미터 실습

2. 프롬프트 엔지니어링
- Zero-shot과 Few-shot 프롬프팅 비교
- Chain-of-Thought(CoT)를 이용한 단계적 추론
- JSON 형태의 Structured Output 생성
- System Prompt를 이용한 AI 페르소나 및 응답 형식 제어

3. FAQ 챗봇 구현
- FAQ 데이터 기반 키워드 검색 기능 구현
- 검색된 FAQ를 System Prompt에 주입(Context Injection)
- 멀티턴 대화 히스토리 관리
- 'converse_stream()'을 활용한 스트리밍 응답 구현
- 테스트 케이스를 이용한 챗봇 품질 평가

### 💡 배운 점
- Amazon Comprehend는 별도의 모델 학습 없이 다양한 자연어 처리 기능을 API 형태로 제공한다.
- 텍스트의 언어, 감정, 개체명, 핵심 문구, 개인정보 등을 자동으로 분석할 수 있으며, 여러 기능을 하나의 - 파이프라인으로 구성하여 활용할 수 있다.
- 토픽 모델링과 군집화를 통해 라벨이 없는 데이터에서도 의미 있는 주제를 추출하는 과정을 이해하였다.
