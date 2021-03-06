## 도둑질
### 문제
도둑이 어느 마을을 털 계획을 하고 있습니다. 이 마을의 모든 집들은 동그랗게 배치되어 있습니다.

각 집들은 서로 인접한 집들과 방범장치가 연결되어 있기 때문에 인접한 두 집을 털면 경보가 울립니다.

각 집에 있는 돈이 담긴 배열 money가 주어질 때, 도둑이 훔칠 수 있는 돈의 최댓값을 return 하도록 solution 함수를 작성하세요.

### 풀이
- 집들은 동그랗게 배치되어 있기 때문에 첫 번째 집과 마지막 집을 함께 털 수 없다.
    1. 첫 번째 집 포함, 마지막 집 제외
    2. 첫 번째 제외, 마지막 집 포함
    두 경우의 결과를 구한 후 그 중 최댓값을 반환한다.
- DP로 풀이
- 인접한 두 집을 털 수 없기 때문에 dp[i] = max(dp[i-1], dp[i-2]+dp[i])
    - dp[i-1] : 인접한 집까지의 최댓값
    - dp[i-2] : 인접하지 않은 집까지의 최댓값
    - dp[i] : 현재 집까지의 최댓값