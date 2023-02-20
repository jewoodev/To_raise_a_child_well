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

## 기술 스택
<div align=center>
    <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=Pandas&logoColor=white">  
    <img src="https://img.shields.io/badge/Matplotlib-006c66?style=for-the-badge&logo=Matplotlib&logoColor=white">
    <br>
    <img src="https://img.shields.io/badge/sklearn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white">
    <br>
    <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=Git&logoColor=white">
    <img src="https://img.shields.io/badge/Github-181717?style=for-the-badge&logo=GitHub&logoColor=white">
</div>

## References

### 참고 문헌

- 연구책임자 조영태 교수 외 4인, "경기도 저출산 원인분석 및 출산동향예측 연구용", 서울대학교 보건대학원, 2016  
- 최숙희, "출산율 반등 성공사례와 출산율에 영향을 미치는 요인 분석 OECD 국가를 대상으로", 여성경제연구, 2021 

### 데이터 출처 

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
