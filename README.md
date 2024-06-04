<h1 align="center"> 💊 알약 이미지 검색 서비스 </h1>
<h4 align="center"> IT공학 전공 졸업프로젝트 </h4>

## Introduction
* 주제: 알약 이미지 검색 및 복용 관리 앱 
* 분석 기간: 2023.09 ~ 2023.12
* 데이터: [AI-Hub 경구약제 이미지 데이터](https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=115&topMenu=100&dataSetSn=576)
* 참여자
  * [정다운](https://github.com/daunjj)
  * [정재원](https://github.com/havehill)
  * 김서연 

<br>

## 1. 이미지 검색 모델 구현
### Resnet
* 목표: 총 171종의 알약 class를 각각 분류
* 학습:
  * 5종(각 종당 약 200여 개)의 알약만 미리 학습
  * fc layer만 가중치를 변경하여 학습
* 결과: 저조한 Accuracy
* 문제점: 171개의 class를 구분하기 위해서는 다량의 데이터를 처리할 수 있는 환경 필요

### CNN
<img src="https://github.com/daunJJ/Pill_Image_Classification/assets/109944763/de6e281e-d5a4-498b-984e-268eeb2986e6" width="500" height= "250"/>

* 목표: 알약의 모양/색상/제형/분할선을 분류 후 해당하는 알약의 리스트 제공
* 학습:
  * 네이버 '의약품사전'을 기준으로 4가지 TYPE 분류
  * 4가지 TYPE별 CNN 모델 구현
* 결과: 100%에 가까운 Accuracy

<br>

## 2. 이미지 검색 및 복용 관리 앱 구현 
<img src="https://github.com/daunJJ/Pill_Image_Classification/assets/109944763/061ed4bc-d768-4b84-b7ac-2a356e037321" width="160" height= "320"/>
<img src="https://github.com/daunJJ/Pill_Image_Classification/assets/109944763/24a1b8d5-e63a-4eba-9e4c-fdd59dd59fff" width="160" height= "320"/>
