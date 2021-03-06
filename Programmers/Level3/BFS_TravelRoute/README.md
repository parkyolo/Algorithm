### 문제 설명
주어진 항공권을 모두 이용하여 여행경로를 짜려고 합니다. 항상 "ICN" 공항에서 출발합니다.

항공권 정보가 담긴 2차원 배열 tickets가 매개변수로 주어질 때, 방문하는 공항 경로를 배열에 담아 return 하도록 solution 함수를 작성해주세요.

### 제한 사항
- 모든 공항은 알파벳 대문자 3글자로 이루어집니다.
- 주어진 공항 수는 3개 이상 10,000개 이하입니다.
- tickets의 각 행 [a, b]는 a 공항에서 b 공항으로 가는 항공권이 있다는 의미입니다.
- 주어진 항공권은 모두 사용해야 합니다.
- 만일 가능한 경로가 2개 이상일 경우 알파벳 순서가 앞서는 경로를 return 합니다.
- 모든 도시를 방문할 수 없는 경우는 주어지지 않습니다.

### 문제 풀이
1. BFS 사용
2. 출발지와 도착지가 서로 같은 항공권이 있을 경우를 예외처리 해주기 위해
공항의 이름을 저장하는 것이 아닌, 해당 항공권의 index를 저장함
3. 아직 사용하지 않은 항공권의 index이면서 경로가 이어질 때 queue에 넣음
4. 항공권의 index를 이용해 각 경로를 result에 저장
5. 모든 가능한 경로를 answer에 저장
6. answer을 sort하여 알파벳 순서가 앞서는 경로를 return

### 주의할 점
- 처음엔 공항의 이름을 queue에 넣어서 해결했는데 테스트 케이스 1번에서 시간 초과가 남.
- 테스트 케이스 1번은 출발지와 도착지가 서로 같은 항공권이 2개 이상 있을 때를 테스트하는 듯 함.
- ex)

|tickets|return|
|------|---|
|[["ICN", "A"], ["ICN", "A"], ["A", "ICN"], ["A", "C"]]|["ICN", "A", "ICN", "A", "C"]|
