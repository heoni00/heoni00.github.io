---
title:  "Final. 통계학입문 _ 분석기법 가이드 & 요약" 
excerpt: "통계학입문 수업 스터디 노트"

categories:
  - Stat-basic
tags:
  - [Statistics,Stat-basic]

toc: true
toc_sticky: true
 
date: 2021-12-26
last_modified_at: 2021-12-26

---

이번 게시물은 지난 게시물에 대한 내용을 다시 정리해보고 향후 내용을 찾거나 어떤 분석기법을 사용해야하는지에 대한 간략한 가이드 내용을 작성하였다. 

---

**chap 1**에서는 그저 확률 분포의 종류와 활용방안에 대해 공부하였다.  
특히 정규분포와 표준정규분포를 이용하여 신뢰구간과 가설검증하는 방안을 배웠다. 

**Chap 2**에서는 평균과 비율에 대한 추론에 대해서 배웠다. 

2.1은 범주형 데이터를 통해 모집단의 비율을 추정하는 것을 배웠다. 어떤 것의 비율이 영가설에 설정한 모수가 맞는지 아닌지.  
2.2은 양적 데이터를 통해 모집단의 평균을 추정하는 것을 배웠다.  
2.3은 공통된 연구 주제에 따라 두 그룹의 범주형 비율에 대한 차이를 검증하는 것을 배웠다.  
2.4는 두 집단의 평균에 차이가 있다는 가설에 대한 검증 방법을 배웠다. 특히 여기서 가설 검증을 위해 표본을 통해 연구를 하고 그 표본을 붓스트랩 방식으로 표준오차를 추정하기 때문에 t-검정을 실시한것을 알아두라. **즉 t-검정은 두 그룹의 평균 차이를 검증하기 위한 방법이다.**  
2.5는 동일한 실험 개체(독립성 x)를 두고 다른 2가지 조건에 따른 평균 차이를 검증하는 것이다. 이때 두 짝의 차이를 계산하여 표준편차를 구하는 것이 핵심이다. 

**Chap 3**에서는 카이-제곱 변수에 대해 공부하였다. 총 2가지의 검증 방법을 배웠다.

3.1 하나의 변수에서 여러가지 범주의 비율에 대한 기대 비율에 대한 검증이다. 즉 가설이 적합한지 검증하는 방법을 배웠다.  
3.2 두 범주형 변수가 서로 연관이 있는가에 대한 연관성 검증을 배웠다. 각 범주형 변수는 여러개의 범주를 가질 수 있으며 이를 2차원 빈도표로 표현하여 기대빈도를 계산하여 관측빈도와 차이를 통해 카이-제곱 통계량을 구한다. 

**Chap 4**에서는 분산분석에 대하여 공부하였다. 분산분석은 하나의 양적변수를 기준으로 삼아 3그룹 이상의 평균의 차이를 검증하는 분석이다. 각 집단의 평균이 다르다는 것은 모집단이 다르다는 것이고 이는 양적변수에 영향을 미친다는 강력한 증거이다. 

4.1과 4.2는 평균 차이를 검증하기 위하여 변동을 그룹간, 그룹내 변동으로 나누어 F-통계량을 구한다. 검증통계량을 통해 가설검증을 하는 것을 공부하였다. 각 데이터를 상자그림으로 나타냈을 때 간단하게 그룹간, 그룹내 변동을 확인할 수 있다. 유념해야할 것은 그룹간 변동이 크더라도 그룹내 변동 또한 함께 크다면 평균차이를 해석하는데 어려움이 있을 수 있다. 따라서 전반적인 상황을 확인하고 분산분석을 해야한다. 

**Chap 5**에서는 회귀분석에 대하여 공부하였다. 회귀분석은 양적 변수 두 개 사이의 관계를 원인과 결과로 나누어 분석하고 이를 검증하는 분석이다. X가 증가함에 따라 Y값이 직선형태로 증가, 감소하는 경향이 있다고 가정을 한다. 

위 챕터에서는 회귀모형의 회귀계수에 대한 검증, 상관관계를 이용한 검증, 회귀모형의 변동에 대해 분석한 뒤 전체 모형에 대한 유의성 분석을 진행하며 마지막으로 회귀분석의 조건을 공부하였다. 

**Chap 6**에서는 다중회귀분석에 대하여 공부하였다. 챕터 5와 다르게 설명변수가 여러개인 이 분석에서는 사실상 반응변수를 정확하게 추정하기 위해선 매우 중요한 분석기법이다. 전반적인 개념은 단순선형회귀분석과 유사하지만 모형을 추정해가는 과정이 조금 복잡하다. 그에 대한 내용과 다른 여러 회귀모형들과 비교하여 최적의 모형이 무엇인지 유추하는 조건들에 대하여 공부한다. 


