## chapter02 예측 모델링 과정 훑어보기
### 2.1 사례 연구: 연비 예측
- 데이터를 2차 형태로 예측하는 경우, 극단 값의 성능이 낮아 질 수 있음
  why? 극단 값 부분의 값이 증가할 수 있기 때문
- 다변량 가법 회귀 스플라인 모델(MARS):   
  - 예측변수와 결과값 간의 복잡한 관계를 만들어 내는 기법 중 하나
  - X 값의 범위와 크기에 따라 서로 다른 회귀선을 적용할 수 있음
  - 얼마나 많은 구간이 필요한지 판단하는 알고리즘이 MARS 내부에 존재

### 2.2 테마
#### 데이터 분할 
- 모델 구축에 사용되는 데이터와 동일한 모집단에서 나오는 데이터가 아닌 경우 데이터 분할하는 방법은 매우 중요  
즉, 해당 모델이 서로 다른 집단에서 얼마나 잘 예측하는지 시험해 봐야 한다는 의미
- 만약 동일한 차량의 값을 예측하고 싶으면, 전체 데이터에서 random sampling을 하는 것이 보다 적절

#### 성능 추정
- 크게 두가지로 생각 가능
  - 테스트 데이터셋을 통한 통계적 정량 평가
  - 관측값과 예측값의 EDA를 통한 정성적 정보 평가
- 단순 통계 정보 값으로만 데이터를 파악할 경우 놓칠 수 있는 부분이 존재

#### 모델 선정
- 모델들 중 하나 선택
- 모델의 유형 중 하나 선택