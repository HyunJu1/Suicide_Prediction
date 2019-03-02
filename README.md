## Suicide_Prediction

### Boaz 미니 프로젝트 - 국가별 자살 수 예측

#### 프로젝트 목표 :
  train set에는 1985년부터 2014년까지의 국가 별 자살 인구수 통계가
  나와 있다. 이 데이터를 가지고 다음 해(2015년) 국가 별 자살 인구수를 예측하기.

#### 사용 데이터
  * Suicide Rates Overview 1985 to 2016 ( From Kaggle )
  * https://www.kaggle.com/russellyates88/suicide-rates-overview-1985-to-2016/kernels

#### 예측 기법 :
  1. 시계열 모델
    - Arima 사용

  2. 회귀 모델  
    - XGBoost Regressor 사용
    - 외부 사용 데이터 사용 :
        * WORLD Happiness Data Report
        * http://worldhappiness.report/ed/2016
        * 사용 외부 변수 :
          - Social support (사회적 지원)
          - Healthy life expectancy at birth ( 건강한 삶 기대 지수 )
          - Positive affect ( 긍정적 영향 )
          - Negative affect ( 부정적 영향 )
          - Democratic Quality (자본주의 퀄리티)
          - Life Ladder (유리천장 지수)
          - Region ( 각 국가 별 지역 )
          - HDI for Year --> Null 값 대체

#### 성능 평가 :
  - RMSE 평가 방법 사용.
  - 시계열 모델 - RMSE : 197
  - 회귀 모델 - RMSE : 331
