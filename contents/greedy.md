# 탐욕법(Greedy) 알고리즘 요약설명 

- **분할정복 기법** 이라고도 부른다.
- 문제를 작은 단위로 쪼개 반복적으로 진행하며 접근하는 방식이다.
- 탐욕법은 각 단계마다 현재에 충실한 선택을 한다.
- 미래의 선택, 최종 결과는 고려하지 않는다.
- 반드시 최적의 해를 보장하는건 아니다.
- 문제를 작은 단위로 쪼개 풀다보면 같은 문제를 반복해 푸는 경우가 있는데 이 때 그 문제들을 매번 재계산 하지 않고 값을 저장해두었다가 재사용 하는 동적프로그래밍(DP) 기법을 이용 할 수 있다.
    - [DP 요약설명](https://github.com/TheCopiens/algorithm-study/blob/master/contents/DP.md)

### 탐욕법 문제 풀이 순서
- 회의실 예약을 예시로 설명합니다. 하나의 회의실을 겹치치 않고 최다로 사용할때 몇개의 회의를 진행 할 수 있을까요?
1. 문제의 답을 내는 과정을 여러 부분으로 나눈다.
2. 방식 결정. 어떤 우선순위로 탐욕적 선택을 할지 결정한다.
    - 회의 시간이 가장 짧은 회의부터 선택, 가장 먼저 끝나는 회의부터 선택
3. 탐욕적 선택 속성, 최적 부분 구조 를 만족하는지 따져본다.
    - 탐욕적 선택 속성: 답의 모든 부분을 고려하지 않고 탐욕적 선택만 하더라도 최적의 해를 구할 수 있는 속성
        - 모든 단계의 최적해에 '종료시간이 빠른 회의'라는 탐욕적 기준으로 선택한 회의가 존재할까?
    - 최적 부분 구조 : 주어진 문제가 **부분 문제의 최적해**로 **전체 문제의 최적해**를 만들 수 있는 구조인지 나타내는 속성
        - 가장 빨리 끝나는 회의를 선택하면 가장 많은 회의를 선택 할 수 있다.


1. 해 선택 
    - 현재 단계에 가장 최적의 해를 구해서 부분해 집합에 포함시킨다.
2. 조건으로 적절성 검사
    - 포함시킨 부분해 집합이 문제의 조건을 만족하는지 검사한다.
    - 만족하지 않을 경우, 한 단계 전으로 돌아가 다른 해를 구해 부분해 집합에 포함한다
3. 해 검사
    - 포함시킨 부분해 집합이 문제의 해가 되는지 검사한다. 
    - 아직 문제의 해가 완성되지 않았다면 1번부터 다시 시작한다.


### 탐욕법을 활용한 문제
- 동전을 최소 개수로 거슬러주기
- [체육복](https://github.com/TheCopiens/algorithm-study/blob/ohhako/source/ohhako/200202_greedy.md)
- [큰수만들기](https://programmers.co.kr/learn/courses/30/lessons/42883)


