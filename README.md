# Section 1 Project

## 개요
해당 프로젝트는 실제 현실 상황이 아닌, [코트스테이츠](https://github.com/codestates) AI 부트캠프 Section 1에서 학습한 내용을 활용하기 위해 상황을 설정하고 진행되었습니다.

## 주제 : 일본 시장 진출을 위한 게임 데이터 분석
* 수행자 : 장건희
* 기간 : 2023.3.7 ~ 2023.3.14
* 사용 데이터 : [게임 출고량 데이터](https://ds-lecture-data.s3.ap-northeast-2.amazonaws.com/datasets/vgames2.csv)
* 분석도구 : python (colab 환경)
* 주요내용 : 데이터 전처리, 데이터 시각화, 통계검정
* * *

## 1. 프로젝트 배경
- 시간적 배경 : 2016년
- 소속 : 국내 중견기업 게임회사 
- 상황
  - 국내 시장 위주로 운영하여 회사가 2016년에 들어 새로운 비전으로 **아시아 게임시장을 대표하는 기업**을 제시
  - 일본 시장 진출을 위한 게임 설계를 위해 데이터 분석 업무를 지시한 상황
  - 일본 시장 분석 및 게임 설계는 초창기 단계로, 많은 지원비가 주어지지 않음

* * *

## 2. 분석 개요
<p align="center"><img src = https://i.imgur.com/NNjrbut.png width="1000" height="400"/> 

* * *
  
## 3. 분석

#### (1) 지역 분석
- 북미, 유럽, 일본, 기타 네 지역의 장르 선호도 분석 수행
- 게임 장르별 출고량을 지역별로 나누어 막대 차트로 시각화
- 분석 결과
```
1. 일본 지역은 전체적인 장르별 선호도의 모양이 다른 지역과 다른 모습을 보임
2. 일본 지역에서는 Role-Playing 장르가 가장 높은 선호도 게임 장르로 나타남
```

#### (2) 연도별 트렌드 분석
- 트렌드의 기준을 `장르`와 `플랫폼`으로 설정
- 일본 지역의 연도별 트렌드의 변화를 라인 차트로 시각화
- 분석 결과
```
장르 
1. 최근 Action 장르의 출고량이 급증하는 모습이 나타남 
2. Role-Playing 장르의 출고량이 항상 높은 편에 속했으나, 최근 감소하는 모습이 나타남
3. 모든 장르의 출고량이 증가와 감소가 반복적으로 나타났기 때문에, 최근 Role-Playing 장르의 출고량 감소를 'Role-Playing 장르의 인기가 식었다'라고 단정하기는 이름
플랫폼
1. Wii Series, PS Series가 항상 타 플랫폼에 비해 출고량이 압도적인 모습을 보여줌
```
#### (3) 인기가 많은 게임 특징 파악
- 일본 지역에서 인기가 많은 게임 20개를 선정해 해당 게임들의 특징 파악
- 분석 결과
```
1. 출고량 기준 가장 상위의 게임들은 1900년대 후반에 나온 옛날 게임에 속함
2. 동일한 작품 시리즈(포켓몬, 마리오)들이 계속해서 출고량이 높게 나타나 출고량 상위 20 게임에도 속함
3. 현지 개발 게임이 일본 지역에서 인기를 지속하고 있음을 확인 
4. 첫 번째 게임 시리즈의 흥행으로 강력한 캐릭터성을 구축한 작품들이, 다음 시리즈에서도 계속해서 흥행하는 모습을 보임
```
- 논의점
```
1. 마리오, 포켓몬과 같이 닌텐도 회사가 가진 IP를 한국 게임사가 이용하여 게임을 개발하기는 불가능
2. 일본은 현지에서 개발한 게임이 계속 인기있는 시장이기에 다른 나라의 게임이 큰 성공을 거두기는 어려움
```
- 추가 분석 : 특징 파악 결과를 바탕으로 일부 게임을 제외한 뒤 앞선 장르 선호도 분석과 연도별 트렌드 분석을 다시 수행
- 추가 분석 결과
```
기존의 분석 결과와 큰 차이가 없다.
```
#### (4) 예상 출고량 분석
- 일본 지역에서의 장르별 평균 출고량을 바탕으로, 어느 장르를 선택할 시 예상 출고량이 높을 지 확인
- 장르별 평균 출고량을 막대 그래프로 시각화
- Role-Playing 장르와 타 장르들의 출고량 차이가 통계적으로 유의미한 지 확인하기 위해 `독립 표본 T-검정` 수행
- 분석결과
```
1. 시각화를 통해 확인한 결과, Role-Playing 장르의 평균 출고량이 압도적으로 높게 나타남
2. 통계 검정 결과, Role-Playing 장르의 평균 출고량이 타 장르들의 출고량보다 높다고 말할 수 있음
```

## 4. 인사이트 및 한계점
- 인사이트
  - 새로운 게임 설계 시 Wii Series, PS Series에서 구동 가능한 Role-Playing 게임을 설계하는 것이 바람직
  - 초기 개발한 게임에서 성공을 거두면 연이은 시리즈를 통해서도 성공 가능성이 높음
  - 마케팅 

- 한계점
  -
