# 데이터 정리 폴더
## 둘째아 출산지원정책여부
부산, 광주와 같은 지역만 검색되고 년도별로의 데이터가 없는 것으로 파악된다.
## 출산/보육비 지원금액


## 출처
- 지역의 총 생산율 : KOSIS, 통계청 / https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1C86&conn_path=I2
- 지가변동률 : KOSIS, 통계청 / https://kosis.kr/statHtml/statHtml.do?orgId=408&tblId=DT_PLCAHTUSE
- 재정자립도 : KOSIS, 통계청 / https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1YL20921&conn_path=I2
- 총 아파트(주택) 매매 건수 : 한국부동산원 부동산통계정보시스템(R-ONE) / https://www.reb.or.kr/r-one/cm/cntnts/cntntsView.do?mi=10113&cntntsId=1409

## 전처리 과정을 확인할 때 참고할 내용
- 지가변동률 : 2014년부터 세입과목 개편으로 잉여금, 이월금, 전입금, 예탁·예수금 등이 세외수입에서 제외되었는데 2006년부터의 데이터를 사용하기 때문에 개편 전의 데이터로 통일하였습니다.
- 총 아파트(주택) 매매 건수 : 2012 ~ 2021 기간의 데이터입니다. 