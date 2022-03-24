## LCS4
### 문제
https://www.acmicpc.net/problem/13711  
LCS(Longest Common Subsequence, 최장 공통 부분 수열)문제는 두 수열이 주어졌을 때, 모두의 부분 수열이 되는 수열 중 가장 긴 것을 찾는 문제이다.

예를 들어, [1, 2, 3]과 [1, 3, 2]의 LCS는 [1, 2] 또는 [1, 3] 이다. 

1부터 N까지 정수가 모두 한 번씩 등장하는 두 수열 A와 B가 주어졌을 때, 두 수열의 LCS 크기를 구하는 프로그램을 작성하시오.

### 입력
첫째 줄에 두 수열의 크기 N (1 ≤ N ≤ 100,000)이 주어진다.

둘째 줄에는 수열 A에 들어있는 수가, 셋째 줄에는 수열 B에 들어있는 수가 주어진다.

### 출력
두 수열의 LCS의 크기를 출력한다.

### 풀이
- 배열 안의 값은 중요하지 않고, 값의 순서가 중요하다.
- A배열의 원소들이 B 배열에서는 몇 번째 인덱스에 위치하는지 arr 배열에 저장한다.
- arr의 원소들의 최장 증가 부분 수열을 찾으면 그 수열이 A과 B의 최장 공통 부분 수열이 된다.