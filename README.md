# 미니프로젝트 - 랜덤 미로 생성

## 구현 순서
- 랜덤 미로 생성
- JFrame을 활용해 GUI로 미로 표현
- Observer Pattern을 활용해 플레이어의 입력 처리
- 추가 구현
  * Thread 이용해서 시간 check
  * Count 제한을 두고 초과시 실패
  * 단계별 미로 정복
  * 파일 입출력으로 Ranking System 구현
  * 

### 랜덤 미로 생성
- 출발지에 무조건 나갈 수 있는 도착지 하나 생성
- 단계 별로 사이즈 UP
- DFS 활용? -> 우선순위 큐 사용
- BFS 활용? -> 큐 사용
- 출발점 : `0,1`
- 도착점 : `map.length-1, map[0].length-2;`

### JFrame을 활용해 GUI로 미로 표현
- int[][] map에 들어있는 데이터를 활용하여 0은 벽, 1은 경로로 판단
- 벽은 Black, 경로는 White로 처리
- 도착지는 Red, 현재 플레이어의 위치는 Blue로 처리
- 방향키를 통해 플레이어 위치 실시간 이동(이동할 때마다 이동 횟수 +1)

### Observer Pattern을 활용해 플레이어의 입력 처리
- 현재 위치에서 상하좌우 데이터를 입력한다.
- 입력된 데이터는 Observer에 의하여 감지가 된다.
- 감지된 데이터(상하좌우 이동)을 반영한 데이터를 플레이어의 위치에 저장한다.
- 갱신된 플레이어의 위치를 JPanel에 update한다.

