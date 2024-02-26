# Chapter 2. 머신러닝 프로젝트 처음부터 끝까지

## 2.1 실제 데이터로 작업하기
- 유명한 공개 데이터 저장소
    - [OpenML](https://openml.org)
    - [kaggle](https://kaggle.com/datasets)
    - [PapersWithCode](https://paperswithcode.com/datasets)
    - [UC 어바인머신러닝저장소](https://archive.ics.uci.edu/ml)
    - [아마존AWS데이터셋](https://registry.opendata.aws)
    - [텐서플로데이터셋](https://tensorflow.org/datasets)
- 메타 포털(공개 데이터 저장소가 나열되어 있는 페이지)
    - [데이터 포털](https://dataportals.org)
    - [오픈 데이터 모니터](https://opendatamonitor.eu)

<br>

## 2.2 큰 그림 보기
### Task : 캘리포니아 인구 조사 데이터를 사용해 캘리포니아의 주택 가격 모델 만들기 (회귀 문제)
### 2.2.1 문제 정의

> [질문1] 비즈니스의 목적이 정확히 뭔가요?
> > 이 모델을 어떻게 사용해 이익을 얻으려고 할까? 

<br>

> **파이프라인** \
> 데이터 처리 컴포넌트들이 연속되어 있는 것을 데이터 파이프라인 이라 한다.

<br>

> [질문2] 현재 솔루션은 어떻게 구성되어 있나요?
> > 문제 해결 방법에 관한 정보 제공 및 참고 성능으로도 사용 가능

---
### 2.2.2 성능 측정 지표 선택
회귀문제의 전형적인 성능지표 = RMSE(평균 제곱근 오차) \
$ \text{RMSE}(\bold{X}, h) = \sqrt{\cfrac 1m \sum_{i=1}^{m} \left( h(\bold x^{(i)}) - y^{(i)} \right)^2}$
- 오차가 커질수록 이 값이 커지므로, 예측에 얼마나 많은 오차가 있는지 가늠하게 해주는 지표

<br>

이상치로 보이는 구역이 많을 때 사용하는 지표 = MAE(평균 절대 편차)\
$\text{MAE}(\bold{X},h) = \cfrac 1m \sum_{i=1}^m |h(\bold{x^{(i)}}) - y^{(i)}| $