## 상자넣기
### 문제
정육면체 모양의 상자가 일렬로 늘어서 있다. 상자마다 크기가 주어져 있는데, 앞에 있는 상자의 크기가 뒤에 있는 상자의 크기보다 작으면, 앞에 있는 상자를 뒤에 있는 상자 안에 넣을 수가 있다. 예를 들어 앞에서부터 순서대로 크기가 (1, 5, 2, 3, 7)인 5개의 상자가 있다면, 크기 1인 상자를 크기 5인 상자에 넣고, 다시 이 상자를 크기 7인 상자 안에 넣을 수 있다. 하지만 이렇게 상자를 넣을 수 있는 방법은 여러 가지가 있을 수 있다. 앞의 예에서 차례대로 크기가 1, 2, 3, 7인 상자를 선택하면 총 4개의 상자가 한 개의 상자에 들어가게 된다.

상자의 크기가 주어질 때, 한 번에 넣을 수 있는 최대의 상자 개수를 출력하는 프로그램을 작성하시오.

### 입력
파일의 첫 번째 줄은 상자의 개수 n (1 ≤ n ≤ 1000)을 나타낸다. 두 번째 줄에는 각 상자의 크기가 순서대로 주어진다. 상자의 크기는 1,000을 넘지 않는 자연수이다.

### 출력
첫째 줄에 한 줄에 넣을 수 있는 최대의 상자 개수를 출력한다.

### 문제 풀이
- Longest Increasing Subsequence(LIS, 최장 증가 수열) 알고리즘과 DP를 동시에 이용
- ```dp[i]```는 ```i```번 상자보다 작거나 같은 상자의 개수
- ```i```보다 작은 ```j```들에 대해 ```boxes[j]```가 ```boxes[i]```보다 작고, ```dp[j]+1```이 ```dp[i]```보다 크면 ```dp[i] = dp[j] + 1```로 바꿔주면서 ```dp[i]```를 가장 큰 ```dp[j]+1```로 바꿔줘야 한다.