# To raise a child well
2006년부터 국가 차원에서 대두되어진 문제인 저출산을 머신러닝을 통해 도출해낸 새로운 인사이트로 해결하고자 하는 프로젝트입니다.  

## 프로젝트 목표
1. 수집한 데이터로 현 정책들의 방향이 출산율 증가에 영향을 주고 있는지 알아보고, 출산율을 높일 수 있는 아이디어를 제시
2. 지역 간 출산율 격차를 줄일 수 있는 아이디어를 제시

# 프로젝트 기간
2023년 2월 16일 ~ 2023년 2월 17일

# 팀 구성원 및 역할
`김기훈`: 전처리 데이터 병합, 모델 결과분석, 모델 시각화  
`신제우`: EDA 분석, 모델 평가, Git 관리  
`황도희`: EDA 구조 형성 및 분석
모델 결과분석
PPT 및 결과 자료 취합
## 공통 역할
- 데이터 수집 및 전처리 : 년 / 월 단위 데이터 수집 및 전처리  
- EDA : 변수 간 상관관계, 특성 중요도 파악  
- 모델 학습 및 예측 : KNeighborsRegressor, DecisionTreeRegressor, RandomForestRegressor....

# 기술 스택
<div align=center>
    <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=Pandas&logoColor=white">  
    <img src="https://img.shields.io/badge/Matplotlib-006c66?style=for-the-badge&logo=Matplotlib&logoColor=white">
    <br>
    <img src="https://img.shields.io/badge/sklearn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white">
    <br>
    <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=Git&logoColor=white">
    <img src="https://img.shields.io/badge/Github-181717?style=for-the-badge&logo=GitHub&logoColor=white">
</div>
# PREVIEW

'To raise a child well'은 통계청과 같은 신뢰성 있는 데이터 제공원으로부터 수집된 저출산의 이유가 될 수 있는 요소들을 EDA를 거쳐 저출산에 가장 큰 원인이 되는 것이 무엇인지 Intelligence를 제시하고 구축한 데이터베이스로 학습된 ML 모델에 그 원인 요소를 어느 정도의 해결됐을 때 저출산 문제가 어느 정도 나아지는지 예측하고 있습니다.

# 개발 관련 설명

<details>
<summary>개발 관련 설명 펼치기</summary>
<div markdown="1">

### 데이터 수집

행정 구역, 월 단위로 출산율에 영향을 미치는 요인 수집

### 데이터 전처리

데이터를 자르고 붙여내는 작업을 통해 전국 및 행정구역별 데이터베이스 구축

<img src="https://github.com/jewoodev/music_resting_place/assets/105477856/8e5c571e-c80e-4394-b2cc-cf773535aef6" alt="image" style="zoom:67%;" />

- 독립변수(x) : 출산율에 영향을 주는 요인 
- 종속변수(y) : 출산율 = 출산아 수/가임기 여성의 수 
- index : 2006-01 ~ 2021-12 

### EDA

독립 변수 간 상관관계 파악

- 독립 - 독립
- 독립 - 종속

<img src="https://github.com/jewoodev/music_resting_place/assets/105477856/74e9265b-08f3-4e1c-b5ff-ae43cdb9c4bc" alt="image" style="zoom: 50%;" />

연도별로 EDA를 했을 때 데이터는 이렇게 말하고 있습니다.



혼인 수가 높고, 이혼율이 낮을수록

여성의 학력이 높고, 여성의 실업율이 적을수록, 그러나 여성고용율이 낮을수록

학원의 수가 적을수록, 도시화율이 낮을수록, 산부인과 수가 많을수록

**출산율은 높아진다.**



<img src="https://github.com/jewoodev/music_resting_place/assets/105477856/c42912e2-0d02-4f07-b313-928ba5a8e776" alt="image" style="zoom:50%;" />

월별로 EDA를 했을 때는 



혼인 수가 높고, 이혼율이 낮을수록 

여성 실업율이 적을수록, 그러나 여성 경제활동 참가율이 낮을수록 

소비자물가지수, 예금은행예금액, 아파트전세지수, 미분양주택수가 낮을수록

**출산율이 높아진다.**



등과 같은 것을 분석, 추론하고



<img src="https://github.com/jewoodev/music_resting_place/assets/105477856/5554097d-2341-4fe1-b70e-291df241ba5c" alt="image" style="zoom:50%;" />

변수간 상관관계를 통해 어떤 변수는 살릴지 버릴지 판단합니다.

### ML 모델링

<img src="https://github.com/jewoodev/music_resting_place/assets/105477856/bbde0872-c182-415d-8daf-1b9d7e9bd795" alt="image" style="zoom:67%;" />

여러가지 머신러닝 모델들을 사용해보며 비교해본 결과, catboost가 가장 뛰어난 성능을 보였습니다.

이러한 결과는 아무래도 이런 이유에서 비롯되지 않았나 생각했습니다.

1. 기존의 부스팅 기법은 일괄적으로 모든 훈련 데이터를 대상으로 잔차 계산하여
   - 순차적으로 모델 학습을 수행하다 보니 <span style="color:red">학습 속도가 느림</span>
   - 잔차를 줄여나가기 위해 학습하는 모델이기에 <span style="color:red">오버피팅</span>이 일어날 수밖에 없음
2. 캣 부스트는 일부만 가지고 잔차 계산 하여 모델 만든 뒤 &rarr; 그 다음 데이터의 잔차로 모델 예측 &rarr; 지금까지 학습한 모델의 잔차를 가지고 모델을 만든 뒤 &rarr; 그 다음 데이터의 잔차로 모델을 예측하는 방식
   - 데이터 대부분이 수치형 변수인 경우 Light GBM 보다 학습 속도가 느리지만, <span style="color:red">파라미터 조정을 통해 여기저기 적용 가능하여 사용</span>

모델링 후에 앞선 ERD 과정에서 선택된 '출산율에 중요한 영향을 미치는 요인 TOP3'를 조정해 출산율이 증가하는지 확인합니다.

<img src="https://github.com/jewoodev/music_resting_place/assets/105477856/d810be54-ec24-4462-9da0-c09d892b4672" alt="image" style="zoom: 80%;" />

- 소비자 물가 지수 2010년~2021년 40% 하락 
- 아파트 전세 가격 2010년~2021년 30% 하락 
- 여성의 경제 활동 참가율 2010년~2021년 10% 상승

으로 값을 변경하자 출산율이 증가하는 것을 확인할 수 있었습니다.

</div>
</details>

# References

## 참고 문헌

- 연구책임자 조영태 교수 외 4인, "경기도 저출산 원인분석 및 출산동향예측 연구용", 서울대학교 보건대학원, 2016  
- 최숙희, "출산율 반등 성공사례와 출산율에 영향을 미치는 요인 분석 OECD 국가를 대상으로", 여성경제연구, 2021 

## 데이터 출처 

< 월 단위 >
- 지가변동률 : KOSIS, 통계청, https://kosis.kr/statHtml/statHtml.do?orgId=408&tblId=DT_PLCAHTUSE
- 예금은행예금액 : KOSIS, 통계청 / https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1YL21191&vw_cd=MT_GTITLE01&list_id=104&seqNo=&lang_mode=ko&language=kor&obj_var_id=&itm_id=&conn_path=MT_GTITLE01
- 여성의 경제활동참여율 : KOSIS, 통계청 / https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1YL21191&vw_cd=MT_GTITLE01&list_id=104&seqNo=&lang_mode=ko&language=kor&obj_var_id=&itm_id=&conn_path=MT_GTITLE01
- 고령인구비율: KOSIS-통계목록: e-지방지표(주제별)-인구-고령인구비율(시도/시/군/구) (월,년 2008~2023.01)
- 혼인건수: KOSIS-통계목록: e-지방지표(주제별)-가족-혼인건수(시도/시/군/구) (월,년 1997~2021.12))
- 이혼건수: KOSIS-통계목록: e-지방지표(주제별)-가족-이혼건수(시도/시/군/구) (월,년 1997~2021.12)
- 소비자물가지수: KOSIS-통계목록: e-지방지표(주제별)-소득과 소비-소비자물가지수(시도) (월,년 1965~2023.01)
- 총 출생아 인구수 : 통계청,「인구동향조사」, 2021.12, 2023.02.20, 출생아수(시도/시/군/구), https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=INH_1B81A01&conn_path=I2
- 아파트 전세 가격지수 : 한국부동산원@부동산통계처 주택통계부, 2022.12, 2023.02.20, 아파트전세가격지수(시도/시/군/구), https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1YL20171E&conn_path=I2
- 미분양현황 : 국토교통부,「미분양주택현황보고」, 2022.12, 2023.02.20, 규모별 미분양현황, https://kosis.kr/statHtml/statHtml.do?orgId=116&tblId=DT_MLTM_2080&conn_path=I2
- 여성 실업율 : 통계청,「경제활동인구조사」, 2023.01, 2023.02.20, 행정구역(시도)/성별 실업률, https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1DA7104S&conn_path=I2

< 년 단위 >
- 지역의 총 생산율 : KOSIS, 통계청 / https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1C86&conn_path=I2
- 지가변동률 : KOSIS, 통계청 / https://kosis.kr/statHtml/statHtml.do?orgId=408&tblId=DT_PLCAHTUSE
- 재정자립도 : KOSIS, 통계청 / https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1YL20921&conn_path=I2
- 총 아파트(주택) 매매 건수 : 한국부동산원 부동산통계정보시스템(R-ONE) / https://www.reb.or.kr/r-one/cm/cntnts/cntntsView.do?mi=10113&cntntsId=1409
- GGI지수(https://gsis.kwdi.re.kr/kr/stat2/NewStatList.html?stat_type_cd=STAT002)

KOSIS, 보건복지부(보육정책과), 2021, 2023.02.16, 유아 천명당 보육시설수(시도/시/군/구), https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1YL20951&conn_path=I2  
KOSIS, 한국국토정보공사,「도시계획현황」, 2021, 2023.02.15, 체육시설, https://kosis.kr/statHtml/statHtml.do?orgId=460&tblId=TX_315_2009_H1055&conn_path=I2
대형마트 수, 서울시, https://data.seoul.go.kr/dataList/10128/S/2/datasetView.do  
대형마트 수, 부산광역시,「부산광역시기본통계」, 2019, 2023.02.16, 유통업체 현황(2008~2019) https://kosis.kr/statHtml/statHtml.do?orgId=202&tblId=DT_202N_BSY80101&conn_path=I2  
대형마트 수, 그 외 https://kosis.kr/search/search.do#none    
한국국토정보공사,「도시계획현황」, 2021, 2023.02.16, 공원, https://kosis.kr/statHtml/statHtml.do?orgId=460&tblId=TX_315_2009_H1126&conn_path=I2  
한국국토정보공사, 국도도시사업부, 2021, 2023.02.16, 도시지역면적(시도/시/군/구), https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1YL21291E&conn_path=I2  
총 면적 한국국토정보공사,「도시계획현황」, 2021, 2023.02.16, 지목별 토지현황, https://kosis.kr/statHtml/statHtml.do?orgId=460&tblId=TX_315_2009_H1105&conn_path=I2  
국민건강보험공단, 건강보험심사평가원,「건강보험통계」, 2022 4/4, 2023.02.16, 시군구별 표시과목별 의원 현황, https://kosis.kr/statHtml/statHtml.do?orgId=354&tblId=DT_HIRA4G&conn_path=I2  
남성육아휴직 수 한국고용정보원,「고용보험통계연보」, 육아휴직(성/시도별)_2008년 이후, https://gsis.kwdi.re.kr/statHtml/statHtml.do?orgId=338&tblId=DT_2GA0909Y&conn_path=I2  
주석 참조(자료관리 :통계서비스정책관 통계서비스기획과), 2100, 2023.02.20, 합계출산율(OECD), https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_2KAA207_OECD&conn_path=I2  
