# Car_damage_detective

## Background of Project
![image](https://user-images.githubusercontent.com/105347300/225243082-34cd3389-3427-44a1-b4f0-f8d7525863d3.png)

카셰어링 업체에서 차량은 중요한 자원이므로 차량의 파손 상태를 꾸준히 모니터링하는 것은 반드시 해야 할 일 중 하나이다.
- 기존 업무 프로세스는 업무 담당자분들이 쏘카 기준 일평균 7-8만장, 최대 11만장의 차량 외관 이미지를 직접 검수하고 직접 확인하기 때문에 많은 시간이 소요된다. 
- 이미지 데이터가 차량의 파손 상태를 모니터링하는 용도보다, 파손 신고 시 업무 담당자의 파손 시점 추적에 주로 사용되어 파손 시점을 즉시 알기 어려운 문제점이 있다.

## Project Description
차량의 외관 사진에서 차량 파손 여부를 확인하는 프로그램

## Project Purpose
- 검수 업로드되는 차량 이미지 데이터를 차량 유지, 보수 업무에 적극적으로 활용
- 차량 이미지 검수에 투입되었던 인력과 시간비용을 절감
- 파손의 책임자를 추적해야 하는 상황이 발생했을 때에도 파손 발생 시점을 바로 추론 가능

## Model Structure
![image](https://user-images.githubusercontent.com/105347300/225243508-a99d5478-bd1f-4f2d-9d1d-9b4fc1bf5a53.png)

1. 차량이 존재하는 영역만을 찾아내 자르기 --> object detection
2. 이미지 파손 존재여부 예측 --> image classification
3. 이미지 내 파손 존재시 파손 영역 및 클래스 예측(스크래치, 찌그러짐, 패널 벌어짐) --> image segmentation
