***
### ※ (대구 동구청) 공공 빅데이터 인턴십 중 진행한 프로젝트
#### 팀원 수 : 6 명
#### 나의 역할 : 공간 데이터 수집 및 전처리
#### 소요 기간 : 약 2달
#### 사용 TOOL 및 언어 : Q-GIS, Python
***
# 소방차 진입로 확보를 위한 불법 주정차 우선예방지역 도출

## 1. 분석 개요
* 화재피해는 소방차가 현장도착 소요시간(골든타임)이 5분을 넘기면 피해 정도가 급증
* 대구시의 경우 소방차가 골든타임 내 현장에 도착한 경우가 전체 사건의 60%에 불과
* 불법 주정차로 인해 막힌 도로로 소방차 진입이 어려워 골든타임을 놓치는 경우가 빈번히 발생
* 화재피해가 클 것으로 우려되는 지역의 경로 상에 불법주정차를 선제적으로 예방할 필요성 존재

## 2. 분석 목적
* 빅데이터 분석을 통해 화재발생 시 재산 및 인명피해 정도가 높은 구역을 선정 후, 소방차 진입로 확보를 위해 해당구역의 불법주정차를 우선적으로 예방하고자 함

## 3. 사용 데이터
![image](https://user-images.githubusercontent.com/46258393/109472069-0070e500-7ab5-11eb-905e-3c0834e46dd8.png)


## 4. 분석 프로세스
![image](https://user-images.githubusercontent.com/46258393/109472109-0e266a80-7ab5-11eb-89d1-b39dd2eab8f9.png)


## 5. 모델 수립
* 차원 축소 (변수선택 : 라쏘 선택법, 단계적 선택법)
* 종속변수 처리 (재산피해액 중앙값보다 높은 경우 : 1, 낮은경우 : 0)
* 분류 모델(Ridge, Lasso, GBM, Logistic 등) 생성 후 AUC 비교
* 모형 선택

## 6. 분석결과 활용 방안
* 경로탐색 API를 활용하여 피해가 심할 것으로 예측 된 지역들로 가는 경로를 구한다.
* 경로들이 가장 많이 겹치는 구간 중 주정차 민원이 심각했던 지역들을 파악하여 해당 지역을 우선적으로 처리한다.


## 기타. 시각화
1. 위험화재 발생가능지수 분포  

![image](https://user-images.githubusercontent.com/46258393/109498555-f2cc5700-7ad6-11eb-92b3-9d6ad7a85a3c.png)

2. 위험화재 발생가능지수 상위 20개소 상세  

![image](https://user-images.githubusercontent.com/46258393/109498661-1e4f4180-7ad7-11eb-8a70-9016664931ae.png)




