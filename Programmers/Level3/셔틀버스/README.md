## 셔틀버스
### 문제
https://programmers.co.kr/learn/courses/30/lessons/17678
### 풀이
- 버스와 크루의 도착시간을 모두 분 단위로 바꿈
- ```540 + t * i (0 <= i < n)```분에 버스가 도착
- ```도착 시각 <= 540 + t * i```인 크루 ```m```명까지 버스에 탈 수 있음
- ```0 <= i < n```까지 탄 사람의 수 ```cnt```와 ```index```를 카운트
- ```cnt```가 ```m```보다 작으면(자리가 남아있으면) 마지막 버스의 도착시간이 콘의 도착시간
- 그렇지 않으면 콘이 마지막으로 탄 사람 ```timetable[index-1]```보다 1분 먼저 도착