# Chapter 1. 한눈에 보는 머신러닝
## 1.1 머신러닝의 정의
> 머신러닝은 명시적인 프로그래밍 없이 컴퓨터가 학습하는 능력을 갖추게 하는 연구 분야 - 1959, Athur Samuel

> 어떤 작업 T에 대한 컴퓨터 프로그램의 성능을 P로 측정했을 때 경험 E로 인해 성능이 향상 됐다면, 이 컴퓨터 프로그램은 작업T와 성능 측정 P에 대해 경험 E로 학습한 것 - 1997, Tom Mitchell

- training set : 시스템이 학습하는 데 사용하는 샘플
- training instance(sample) : 각각의 훈련 데이터
- model : 머신러닝 시스템이서 학습하고 예측을 만드는 부분
  - 예) random forest, neural network

</br>

- Task : 새로운 메일이 스팸인지 구분하는 것
- Experience : training data
- Performance : 직접 정의해야 함 [예)정확도, 민감도, 재현율 등]

<br>

## 1.2 왜 머신러닝을 사용하나?
- 학습 데이터에서 나타나는 패턴을 감지하여 문제를 판단하는데 좋은 기준인지 자동으로 학습함

- 프로그램이 훨씬 짧아지고 유지 보수하기 쉽고 비교적 정확도가 높음

- data mining : 대용량의 데이터를 분석하여 숨겨진 패턴을 발견하는 것

### 머신러닝은 다음 분야에서 뛰어남
- 기존 솔루션으로는 많은 수동 조정과 규칙이 필요한 문제
- 전통적인 방식으로는 해결 방법이 없는 복잡한 문제
- 유동적인 환경
- 복잡한 문제와 대량의 데이터에서 인사이트 얻기

<br>

## 1.3 애플리케이션 사례
- 생산라인에서의 제품 이미지를 분석해 자동으로 분류
  - Image classification(CV) : CNN, Transformer

- 뇌를 스캔하여 종양 진단
  -  Semantic segmentation(CV) : CNN, Transformer

- 자동으로 뉴스 기사 분류
  - Text classification : NLP(자연어 처리), RNN, Transformer

- 토론 포럼에서 부정적인 코멘트를 자동으로 구분
  - Text classification : NLP 

- 긴 문서 자동으로 요약
  - Text classification : NLP

- 챗봇 또는 개인 비서 만들기
  - NLU component (자연어 이해)

- 여러가지 성과 자료를 바탕으로 회사의 내년도 수익 예측
  - regression : linear regression, polynomial regression, SVM, random forest, ANN, RNN, CNN, Transformer

- 음성 명령에 반응하는 앱 만들기
  - 음성 인식 작업 : RNN, CNN, Transformer 

- 신용카드 부정 거래 감지
  - outlier detection : isolation forest, GMM, Autoencoder

- 구매 이력을 기반으로 고객을 나누고 각 집합마다 다른 마케팅 전략 계획
  - clustering : K-means, DBSCAN

- 고차원의 복잡한 데이터 겟을 명확하고 의미 있는 그래프로 표현
  - data visualization : dimensionality reduction 

- 과거 구매 이력을 기반으로 고객이 관심을 가질 수 있는 상품 추천
  - 추천 시스템

- 지능형 게임 봇 만들기
  - 강화 학습(reinforcement learning, RL)

<br>

## 1.4 머신러닝 시스템의 종류

- 훈련지도 방식
    - 지도
    - 비지도
    - 준지도
    - 자기 지도
    - 강화 학습

- 실시간으로 점진적인 학습을 하는지 아닌지
    - 온라인 학습
    - 배치 학습

- 단순히 알고 있는 데이터 포인트와 새 데이터 포인트를 비교하는 것인지 아니면 과학자들이 하는 것처럼 훈련 데이터셋에서 패턴을 발견하여 예측 모델을 만드는지
    - 사례 기반 학습
    - 모델 기반 학습

<br>

## 1.5 머신러닝의 주요 도전 과제
1.  충분하지 않은 양의 훈련 데이터
    - 새 데이터 확보 

2.  대표성 없는 훈련 데이터  
    - sampling noise
    - sampling bias
    - 잡음과 편향 확인하여 사용 여부 결정

3. 낮은 품질의 데이터
    - 오류
    - 이상치
    - 잡음
    - 품질 높이기

4. 관련없는 특성
    - 특성을 선택
    - 특성을 추출
    - 새 데이터 수집하여 새 특성 생성

5. 훈련 데이터 과대적합
    - 하이퍼 파라미터 조정

6. 훈련 데이터 과소 적합
    - 모델 파라미터가 많이 더 강력한 모델로 변경
    - 규제 하이퍼 파라미터를 감소

<br>

## 1.6 테스트와 검증
1. 하이퍼 파라미터 튜닝과 모델 선택
    - holdout validation
    - cross-validation

2. 데이터 불일치
    - train-dev set
