---
title:  "데청캠 AI 공공기관 협업 프로젝트 - UPA 야적장 재고 관리 서비스 개발" 
excerpt: "YOLO V5와 DeepSort를 이용해 차량 인식 AI 및 앱 서비스 개발"

categories:
  - Project
tags:
  - [Analysis, Project]

toc: true
toc_sticky: true
 
date: 2023-02-22
last_modified_at: 2023-02-22

---

## 2021 울산항만공사 차량 야적장 재고 관리 서비스 개발 
### YOLO V5와 DeepSort를 이용해 차량 인식 AI 및 앱 서비스 개발

2021 K-Data AI 집체 교육 프로그램 중 공공기관 협업 프로젝트로 울산항만공사에 필요한 AI 및 앱 기반 서비스를 개발했습니다. 2021.07 ~ 2021.08, 약 5주간 합숙하며 프로젝트를 진행했습니다.

[프로젝트 코드 보관소](https://github.com/heoni00/2021-Project-UPA)

#### 팀소개 

김차헌, 김찬우, 문호준, 민현정, 신예지, 조정원, 이동욱

- 정치외교, 통계학, IT융합응용공학, 중국어학, 컴퓨터공학, 정보통계학, 조선해양학 학부 출신. 
- 프로그래밍 언어, 데이터 분석 및 수집, OPEN CV, 머신러닝 및 딥러닝 그리고 서버 및 웹 구축에 관심 및 일정 수준의 이해에 기반하여 서비스를 개발
- 미래 산업 가치가 높은 해양 수출입 프로세스에 필요한 스마트 항만 플랫폼 개발에 기여하고 자동화 시스템 및 OPEN CV 활용 등에 대한 경력을 쌓고자 형성된 팀

#### 프로젝트 동기 및 목표

K-data 빅리더 프로그램 과정에 참여한 9개의 공공기관에서 제시한 기관의 비전 및 프로젝트 요구 방향 중 울산항만공사의 비전과 사용할 수 있는 기술들이 끌렸습니다.   

**해양 물류 산업의 비전**
울산항과 연관된 해양 수출입 산업에 운용되는 경제 규모는 매우 컸고 이에 해양 수출산업 분야를 도메인으로 설정하고 관련 경험을 쌓으면 향후 종사자가 갖을 수 있는 가치가 높을 것이라 판단했습니다. 또한, 해양 물류 산업은 아직 IT개발의 불모지로 '아날로그식' 산업구조를 갖고 있기에 개발자가 개발할 일거리가 많다 생각했습니다.   

**사용가능한 기술**
스마트 물류 플랫폼, 해양 물류 프로레스 전과정을 ICT & 자동화하여 생산성을 높이는 플랫폼입니다. 해외 국제항의 경우 스마트 항구 개발 진행을 하고 있으며 울산항 또한 이를 염두하고 있었습니다. 스마트 항구를 개발하기 위해선 `자율주행`, `사물인터넷` 그리고 `데이터베이스 전산화` 기술이 필요했었고 본 프로젝트에 참여하여 해당 기술을 사용할 수 있다고 판단했습니다.   

**목표**
프로젝트 시작에 앞서 1순위로 목표한 것은 **현업에서 사용가능한 서비스를 개발하자**였습니다. 개발팀이 아무리 멋지고 대단한 기능을 만들더라고 산업현장에 활용하기 어렵고 실무자가 싫어한다면 필요없을 뿐더러 상품성이 없는 서비스라 생각했습니다.   

따라서 울산항만공사 실무자, 운영팀에게 인정받아 적절한 설치만으로 운용할 수 있을 것 같다는 평가를 받는 것을 목표로 했습니다. 

### OVERVIEW

![최종_빅리더AI_NEXTLEVEL_bigchallenge_발표자료_1](https://user-images.githubusercontent.com/67791317/203754755-5bfda6df-c59a-488d-9c97-9c10818424c1.jpg)

#### 추진배경

울산항은 차량 수출 중심 항만으로 특수하게 현대자동차 공장부지와 울산항 자동차 부두가 서로 붙어있다. 

![최종_빅리더AI_NEXTLEVEL_bigchallenge_발표자료_6](https://user-images.githubusercontent.com/67791317/203755161-9eac89db-64e1-47df-bb21-3539ede9d26e.jpg)

이러한 특징으로 인해 장점과 단점이 발생한다. 

**장점**으로 자동차를 수출할 때 항구까지 운반하는 비용이 절감되고 운반 및 선적과정에서 문제가 발생할 시 즉각적으로 대응이 가능하다는 점이다. 또한, 공장부지에 제품 재고 공간이 부족하면 부두의 야적장을 활용할 수 있다. 

**단점**은 장점과 연결이된다. 부두와 공장이 붙어있기 때문에 다른 항구와 달리 수출 - 신고 - 검사 과정이 통합되어 확실성이 없고 정확한 재고파악이 어렵다는 것이다. 이에 연쇄적으로 현업에서는 선적해야하는 차량의 위치 파악 그리고 선적 시간 계산등이 어려워 **출항하는 시간이 늘어난다**는 것이다. 

![최종_빅리더AI_NEXTLEVEL_bigchallenge_발표자료_16](https://user-images.githubusercontent.com/67791317/203755184-be1d490d-e55b-409f-a26f-529aac840d08.jpg)

사전 조사를 통해 알 수 있었던 장,단점을 커버할 수 있는 해결방법으로 선적하기 위한 차량들의 종류 및 개수 그리고 위치를 알 수 있는 시스템을 고안했다. 즉, 실어야 할 자동차를 찾고 지금 얼마나 실렸는지 파악할 수 있도록 **야적장 재고 파악**시스템을 개발하게 되었다. 

#### 서비스 구현 방법

![최종_빅리더AI_NEXTLEVEL_bigchallenge_발표자료_20](https://user-images.githubusercontent.com/67791317/203755196-5faa7255-867f-46cd-9ced-c114d8ff7301.jpg)

서비스 구현에서 관건은 빠른 속도로 이동하는 차량의 종류와 수량을 정확하게 카운트 할 수 있는 AI 알고르듬을 개발하는 것이 우선이었습니다. 또한, 보안상, 시설 운영상 선박 입구에 설치할 수 없는 카메라 대신 작업자가 작성한 검수표 엑셀 파일을 자동으로 DB에 업로드 할 수 있는 프로그램을 개발하는 것입니다. 

#### 서비스 기능 

![최종_빅리더AI_NEXTLEVEL_bigchallenge_발표자료_21](https://user-images.githubusercontent.com/67791317/203755204-66dadec6-4202-4300-929e-380fd1c98053.jpg) 

![최종_빅리더AI_NEXTLEVEL_bigchallenge_발표자료_22](https://user-images.githubusercontent.com/67791317/203755209-911fe571-2f31-409a-abd1-bea6c94ee223.jpg)

앞선 서비스 개발이 완료된다면 감독관들은 개별 ID를 통해 모바일 웹으로 야적장의 현황표를 모델 검색, 이동 기록 검색 그리고 남은 잔여 차 대수를 확인 할 수 있게 됩니다.   

#### UI 화면

<img src="https://user-images.githubusercontent.com/67791317/204077665-8eb593a7-b8fa-4c4a-b6e1-9c9415c54d9e.gif" width="35%" height="35%"/>

[본 서비스 체험하기 (웹)](https://big-leader-upa-project.herokuapp.com/chart)

#### 알고리즘

[![최종_빅리더AI_NEXTLEVEL_bigchallenge_발표자료_24](https://user-images.githubusercontent.com/67791317/203755213-8bc988a6-b5ba-4b0f-b7ad-f9a43e8906e9.jpg)](https://github.com/heoni00/2021-Project-UPA/tree/main/algorithm#readme)

[알고리즘 설명 링크 🌏](https://github.com/heoni00/2021-Project-UPA/tree/main/algorithm#readme)

#### 서비스 기대효과 및 한계

![최종_빅리더AI_NEXTLEVEL_bigchallenge_발표자료_34](https://user-images.githubusercontent.com/67791317/203755250-c148d0cf-12d8-4c8a-8676-08e679ef89cc.jpg)
![최종_빅리더AI_NEXTLEVEL_bigchallenge_발표자료_35](https://user-images.githubusercontent.com/67791317/203755254-86e38981-0acc-45f1-b6e7-db010d5652cd.jpg)
![최종_빅리더AI_NEXTLEVEL_bigchallenge_발표자료_36](https://user-images.githubusercontent.com/67791317/203755257-80b9bc54-b694-4e53-a0bf-52390718aa74.jpg)