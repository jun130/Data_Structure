이 프로그램은 다익스트라 알고리즘을 이용해 최단거리와 최단경로를 출력해주는 프로그램이다.
크게 나누면 입력, 최단거리 및 경로 계산, 출력 3가지 코드가 있는데,
입력코드는 input.txt로 부터의 파일을 순차적으로 입력받는다
-1이나 -9인 경우에따라 다른 상태를 설정 해주었고 파일의 입력이 문자, 스페이스 바 인경우에 맞춰 입력을 받기위해
비표준 함수인 atoi를 통해 문자를 숫자로 변환하고 , 스페이스바를 구분해주는 stok로 각각의 변수를 입력받음.
다음으로 최단 거리 및 경로 계산 코드는 다익스트라 알고리즘 참조하였고 알고리즘의 성능향상을 위해 우선순위큐를 사용하였다.
시작점의 최단거리를 0으로 초기화하고 모든 정점의 최단거리는 INF (MAX 값을 1000으로설정 )로 설정했다.
각각의 정점을 알고리즘에 따라 시작점부터 정점간의 최단거리를 구하는 동시에 경로 출력을 위해 min_dist[MAX_VERTEX]를 설정하여  
각 정점의 이전 정점을 저장하였다. 예로들어 1 -> 3 -> 5 라는 경로가있으면 min_dist[5] = 3, min_dist[3] = 1 과같이 경로추적을 함.
출력코드에는 최단거리가 존재하는 경우 (정점의 거리가 INF) 와 안하는 경우를 구분해 출력하였다.

세부적인 함수의 동작설명은 cpp파일에 주석으로 처리함.
