## 과제

### 문제
https://www.acmicpc.net/problem/13904  
웅찬이는 과제가 많다. 하루에 한 과제를 끝낼 수 있는데, 과제마다 마감일이 있으므로 모든 과제를 끝내지 못할 수도 있다. 과제마다 끝냈을 때 얻을 수 있는 점수가 있는데, 마감일이 지난 과제는 점수를 받을 수 없다.

웅찬이는 가장 점수를 많이 받을 수 있도록 과제를 수행하고 싶다. 웅찬이를 도와 얻을 수 있는 점수의 최댓값을 구하시오.

### 입력
첫 줄에 정수 N (1 ≤ N ≤ 1,000)이 주어진다.

다음 줄부터 N개의 줄에는 각각 두 정수 d (1 ≤ d ≤ 1,000)와 w (1 ≤ w ≤ 100)가 주어진다. d는 과제 마감일까지 남은 일수를 의미하며, w는 과제의 점수를 의미한다.

### 출력
얻을 수 있는 점수의 최댓값을 출력한다.

### 풀이
- 6일 남은 과제는 1일에 해도 되지만 1일 남은 과제는 6일에 할 수 없음
-> 마감일이 늦을수록 선택지가 적어지므로 마지막 마감일부터 최대 점수를 구해줌
-> 마감일이 늦고 점수가 높은 순으로 과제를 정렬
- t일 이상 남은 과제 중 idx번 과제의 점수가 가장 높다면, asg[idx][0]은 과제의 마감일, asg[idx][1]은 과제의 점수
-> score[t] = asg[idx][1], asg[idx][1] = -1; (이미 과제를 했다는 방문 체크)
- 1일에 한 과제부터 마지막 마감일의 과제까지 sum(score[1:]) 출력