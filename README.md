# AI_project

## 시작하게된 계기
코로나의 확산에 따라 사람들의 활동량이 감소하게 되고 그로 인해 살이 급격하게 찌는 사례가 늘어났다.  
이러한 상황에서 급격한 체중 증가는 몸에 악영향을 불러일으킨다는 정보를 접했고  
나는 이 비만에 대해 더 알아보고 비만 예측 모델을 만들어보고자 이 프로젝트를 시작하게 되었다.

## 이론적 배경
세계보건기구(WHO)에서는 비만을 '건강을 해칠 정도로 지방조직에 비정상적인 또는 과도한 지방질이 축적되는 상태'라고 정의하고 있다. <br>
비만을 질병으로 인식하는 이유는 비만이 여러가지 대사성 질환(당뇨병, 고혈압 등)과 밀접한 관련이 있기 때문이다.<br>
2013년 미국 의학 협회에서는 비만을 질병으로 공식 선언하였고, 비만은 새로운 공중보건 문제로 보고 있으며 심각한 건강 문제로 정의하고 있다.<br>


비만은 비만으로 그치는 것이 아니라 각종 질병의 원인이 될 수 있으며, 정신적인 질병까지 유발할 수 있다.<br>
제2형 당뇨병, 이상지질혈증, 고혈압, 지방간, 담낭질환, 관상동맥질환(협심증, 심근경색증), 뇌졸중, 수면무호흡증, 통풍, 골관절염, 월경이상, 대장암, 유방암 등이 대표적인 비만과 관련된 질병이다.

대한비만학회는 기존에는 BMI가 18.5 미만이면 저체중, 18.5∼23은 정상, 23~25이면 과체중, 25∼30은 경도비만, 30∼35는 중등도비만, 35 이상이면 고도비만으로 구분했었으나, 2018년 비만진료지침에서 단계별 용어가 새롭게 변경되어 18.5 미만이면 저체중, 18.5∼25 미만은 정상, 25∼30 미만은 '1단계 비만', 30∼40 미만은 '2단계 비만', 40 이상이면 '3단계 비만'으로 구분한다.
- 비만여부 종속변수 생성시
  - 18.5 미만 **저체중**
  - 18.5∼25 미만 **정상**
  - 25∼30 미만 **비만**


### 종속변수
- 비만여부
### 독립변수
505개의 항목 중 이론적 배경에 따라 비만에 영향을 주는 요인을 중심으로 선정하였고, 08~10 총 11년간 연속적으로 측정되어 비만을 분류하는대ㅔ 영향을 미칠 수 있는 항목 중 항목별 범주의 빈도가 학습에 충분한 항목을 선정하였다.

### 비만도 분포율
- 1 : 저체중
- 2 : 정상
- 3 : 비만
```

## 일지
|Date|Description|Official source(참고 주소)|
|:---:|---| --- |
|01.07|Data request|[질병관리본부](https://chs.cdc.go.kr/chs/rdr/rdrInfoDownMain.do)에 자료 신청|
|01.11|1차 EDA 전처리||
|01.12|2차 EDA 전처리||
||[BMI 지수를 적용하고 10-13년도와 14-17년도까지의 칼럼 동일화](https://github.com/gini7752/AI_project/blob/main/data/README.md)||
|01.13|모델링||
||LinearRegression, RandomForest, DNN 모델 제작 |DNN 모델에서 에러 발생하여 미해결|
|01.14|DNN 모델 완성|종속변수의 클래스가 3개라서 분류 모델로 만들었는데 정확도가 낮음|
|||현재는 회귀 모델로 DNN 완성|
||Randomforest 모델 완성|상관관계가 가장 낮은 칼럼 하나를 제거하고 파라미터를 조정하고 정확도를 높임|