# 옵티마이저 (Optimizer)

[TOC]

# 1.옵티마이저란?

​	옵티마이저는 SQL을 가장 빠르고 효율적으로 수행할 최적(최저비용)의 처리경로를 생성해주는 DBMS의 기능.

# 2.옵티마이저의 종류

## 1). 규칙기반 옵티마이저: 미리 정해 놓은 규칙에 따라 액세스 경로를 평가하고 실행계획을 선택

## 2). 비용기반 옵티마이저: 비용을 기반으로 최적화 수행. 현재 대부분의 DBMS가 채택중.

# 3.SQL 최적화 과정

![sql가이드](http://www.dbguide.net/publishing/img/knowledge/SQL_286.jpg)

## 1). Parser: SQL 문장을 이루는 개별 구성요소를 분석하고 파싱해서 파싱 트리(내부적인 구조체)를 만든다. 이 과정에서 사용자 SQL에 문법적 오류가 없는지(Syntax 체크), 의미상 오류가 없는지(Semantic 체크) 확인한다.

## 2). Optimizer

### 	a.Query Transformer: 파싱된 SQL을 표준 형태로 변환.

### 	b.Cost Estimator: 오브젝트 및 시스템 통계정보를 이용해 쿼리 수행 각 단계의 선택도, 카디널리티, 비용을 계산하고, 궁극적으로는 실행계획 전체에 대한 총 비용을 계산

### 	c. Plan Generator:  하나의 쿼리를 수행하는 데 있어, 후보군이 될만한 실행계획들을 생성

## 3). Row-Source Generator: 옵티마이저가 생성한 실행계획을 SQL 엔진이 실제 실행할 수 있는 코드 형태로 포맷팅

## 4).SQL Engine: SQL 실행







#### 참고:

1. ##### http://www.dbguide.net/db.db?cmd=view&boardUid=148218&boardConfigUid=9&boardIdx=139&boardStep=1

2. ##### https://www.youtube.com/watch?v=aTjq9neOQl8