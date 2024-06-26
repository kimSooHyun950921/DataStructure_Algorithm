# 01. 배열 / 리스트
```
배열과 리스트 모두 선형 자료 구조에 속한다. 선형자료구조는 데이터가 연속적으로 연결되어있는 모양으로 구성 되어있으며, 순차적으로 나열시킨 형태를 말한다.
```
## 배열
<img src="img/array.jpg" />

### 배열이란?
* 연속적인 기억공간에 배정하며 각 요소들은 인덱스/값쌍으로 되어있어 인덱스로 값을 가져올 수 있다.

### 배열의 특징
* 가장 simple한 한자료구조이다 
* 인덱스로 접근할수 있다.
* 접근속도가 빠르다.
* 기억장소를 연속으로 배정받아 기억장소 이용 효율은 가장 좋다.
* 자료의 갯수가 n개일때 삽입시 평균 이동 횟수는 O(n), n+1/2, 삭제시 평균이동 횟수는 O(n), n-1/2, 조회시 O(1)
* 데이터 조희는 빠르지만 삽입, 삭제시 자료의 이동이 필요하기때무네 작업이 번거롭다.

### 실습
1. 배열하나를 선언하라
2. 임의의 숫자를 배열 10개를 넣어라
3. 배열에 5번째에 원소 하나를 삽입하라
4. 배열에 5번째 원소하나를 삭제하라
5. 5번째 배열을 조회하라
6. 위 5가지의 시간을 측정하라 (datetime 이용)

## 리스트
<img src="img/1_linked_list" />

### 리스트란?
* 자료들을 연속적으로 배열시키지는 않음, 기억공간(메모리)안의 임의의 위치에 저장시키되, 자료항목의 순서에따라 노드의 포인터 부분을 이용하여 서로 연결 시킨구조

### 리스트의 특징
* 삽입/삭제가 용이하다.
* 기억공간이 연속적이로 놓여있지 않아도 저장이 가능하다.
* 접근속도가 느리다.(포인터를 찾아가는 시간이 필요하기때문에 배열에비해 접그녹도가 느리다.)
* 중간 노드의연결이 끊어지면 다음 노드를 찾기 어렵다.
* 삽입/삭제시 O(1)의 시간복잡도, 조회시 O(n)의 시간복잡도

### 실습
1. 연결리스트를위한 노드를 하나 만들어라
2. 노드를 10개를 연결하여 연결리스트를 만들어라
3. 연결리스트의 5번째 원소하나를 삽입하라.
4. 연결리스트의 5번째 원소하나를 삭제하라
5. 5번째 배열을 조회하라
6. 위 5가지시간을 측정하고 배열과 시간을 비교하라

# 02. 스택 / 큐
## 스택
<img src="img/3_stack.png" />

### 스택이란?
* 스택의 의미가 '더미, 쌓아놓은'인것처럼, 가장 최근에 들어온 데이터가 가장 위에 있고 나중에 나가는 형식으로 저장하는 자료구조 (LIFO: Last In First Out)

### 스택의 특징
* 자료의 삽입, 삭제 작업이 한쪽 방향에서만 이루어지는 구조
* 나중에 삽입된 자료가 가장 먼저 삭제되는 방식으로 삭제되는 방식으로 처리
* TOP: 스택포인터라함, 스택으로 할장된 기억공간에 가장 마지막으로 삽입된 자료가 기억된 공간을 가리키는 요소

### 연산
* pop(): 스택에서 가장 위에있는 항목을 제거
* push(item): item하나를 스택의 가장 윗부분에 추가
* peek(): 스택의 가장 위에있는 항목 반환
* isEmpty(): 스택이 비어있을때 true 반환 

### 실습
1. 스택의 연산을 구현하라
2. 스택을 링크드리스트로 구현하라

### 관련문제
1. [스택](https://www.acmicpc.net/problem/10828)
2. [괄호](https://www.acmicpc.net/problem/9012)
3. [쇠막대기](https://www.acmicpc.net/problem/10799)
4. [제로](https://www.acmicpc.net/problem/10773)


## 큐
<img src="img/5_queue.png" />

### 큐란?
* 먼저 넣은 데이터가 먼저나오는 구조를가진 선입 선출구조로 저장하는 자료구조
### 큐의 특징
* 선형 리스트 한쪽에는 삽입, 다른한쪽에는 삭제 작업이 이루어지는 구성한 자료구조
* 시장과 끝을 표시하는 두개의 포인터가 있다.
* 창구업무처럼 순서를 기다리는 등의 대기 행렬에서 사용

### circular queue
<img src="img/circular_queue.png" />

* 선형큐의 문제점을 보안하기 위한 자료구조
* 선형큐의 rear 가 가리키는 포인터가 배열의 마지막 인덱스를 가리키고 있을때 앞쪽에서 remove연산으로 발생한 빈공간을 활용할 수 없음
* 포인터 증가방식이 (rear+1)%arraysize == front를 이용하여 데이터 삽입 가능

### 연산
* add(item): item을 리스트 끝부분에 추가
* remove(): 리스트 첫번째 항목 제거
* peek(): 큐에서 가장 위에있는 항목반환
* isEmpty(): 큐가 비었을때 true 반환

### 실습
1. queue를 구현하라
2. circular queue를 구현하라

### 관련문제
1. [큐](https://www.acmicpc.net/problem/10845)
2. [큐2](https://www.acmicpc.net/problem/18258) 
3. [카드](https://www.acmicpc.net/problem/2161)
4. [카드2](https://www.acmicpc.net/problem/2164)

# 03. 순환/덱
## 덱
<img src="img/6_deque.png" />

### 덱이란?
앞으로도 뒤로도 넣을 수 있고, 앞으로도 뒤로도 뺄 수 있는 자료구조
### 덱의 특징
* 큐/스택과 다르게 양방향으로 넣고 뺄 수있다.
* 문서편집 프로그램의 작업을 추가하고 제거함으로써  Undo/Redo 기능을 구현할 수 있음 
* 중간데이터 삽입/삭제가 용이하지 않다.
### 연산
* addFirst(): 덱의 가장 앞부분에 추가
* addLast(item): 덱의 가장 마지막 부분에 추가
* removeFirst(): 덱의 가장 첫번째 원소 제거
* removeLast(): 덱의 가장 마지막 원소 제거 
* isEmpty(): 덱이 비었는지확인
* getFirst(): 덱의 첫번째 원소 반환
* getLast(): 덱의 마지막 원소 반환

### 실습
1. 덱의 연산을 구현하라
2. 덱을 리스트리스트를 구현하라

### 관련 문제(스택/큐/덱 포함)
1. [덱](https://www.acmicpc.net/problem/10866)
2. [덱2](https://www.acmicpc.net/problem/28279)
3. [요새푸스 문제](https://www.acmicpc.net/problem/1158)
4. [카드정렬하기](https://www.acmicpc.net/problem/1715)
5. [같은숫자는싫어](https://school.programmers.co.kr/learn/courses/30/lessons/12906)
6. [기능개발](https://school.programmers.co.kr/learn/courses/30/lessons/42586)
7. [올바른괄호](https://school.programmers.co.kr/learn/courses/30/lessons/12909)
8. [프로세스](https://school.programmers.co.kr/learn/courses/30/lessons/42587)
9. [다리를지나는트럭](https://school.programmers.co.kr/learn/courses/30/lessons/42583)
10. [주식가격](https://school.programmers.co.kr/learn/courses/30/lessons/42584)

## 순환/재귀(Recursion)
<img src="img/7_recurse.png" />

### 순환/재귀(Recursion)이란?
재귀함수(재귀호출)이라고 부름, 알고리즘에서 함수가 수행도중 자기자신을 다시호출하여 문제를 해결하는 기법

### 재귀 함수의 예제
* 피보나치 순환식 코드 예제 수열
    * 0, 1, 1, 2, 3, 5, 7 로 이전값과 현재값을 더해서 다음값을 도출하는 수열을 말함
    * $fibo(n) = \begin{cases} 0 & n=0 \\ 1 & n=1\\ fibo(n-2)  + fibo(n-1) & otherwise\end{cases} $
    * 코드
        ```python
        def fibo(n){
            if n == 0:
                return 0
            if n == 1:
                return 1
            return fibo(n-1) + fibo(n-2)
        }
        ```
    * 실행 과정

        <img src="img/8_fibo.png" />
* 참고) 피보나치 수열 반복시코드 예제
    * 코드
        ```python
        def fibo_for(int n):
            if n == 0:
                return 0
            if n == 1:
                return 1
            pp, p, result = 0, 1, 0
            for i in range(2, n+1):
                result = p + pp
                pp = p
                p = result
            return result
        ```
* 순환함수(재귀함수) 특징
    * 함수안에 자기 이름과 같은 함수작성
    * ***반드시*** 돌아오는(return 구문) 코드를 작성해야함
    * 재귀함수는 반복문으로 표현할 수도 있다.
### 관련 문제
1. [재귀함수가뭔가요?](https://www.acmicpc.net/problem/17478)
2. [별찍기](https://www.acmicpc.net/problem/2447)
3. [하노이탑](https://www.acmicpc.net/problem/11729)
4. [팩토리얼](https://www.acmicpc.net/problem/10872)
### 실습
* 위의 관련된 문제중 반복문으로 풀수있는것은 반복문으로도 만들어라

# 04. 트리
```
지금까지는 자료들이 직선과 같이 나열되어있는 구조를 가진 선형 자료구조만을 공부하였다. 지금부터는 자료가 선형으로 저장되어있지 않고 계층적인 구조를 가지는등의 자료구조를 배운다.
```
<img src="img/9_Treedatastructure.png" />

## 트리란?
* 계층적인 자료를 표현하는데 이용되는 자료구조
* 예를 들어, 조상과 자손, 전체와 부분, 상사와 부하직원, 컴퓨터 디렉터리 구조등의 계층적인 관계를 표현할때 사용된다.
* 상기의 재귀의 실행순서를 표현할때도 트리구조로 표현되는것을 알 수 있다.
## 트리에서 나타내는 용어들
* 노드(node): 트리 원소 하나하나를 나타내는것(A, B... P), 트리는 하나이상의 노드로 이루어짐
* 루트(root): 트리노드중에 가장 상위에 있는 노드 (A)
* 서브트리: 루트가 아닌 나머지 노드들이 만드는 트리
    - 루트 : A
    - 서브트리: {B,D, E, H, I, K, L, M, N}, {C, G, F, J, O, P}
* 간선(edge): 노드간 연결되는 선, 루트와 서브트리가 연결되는 선
* 트리간의 관계
    - 부모노드: 두 노드중 상위에 있는 노드 (A는 B의 부모노드이다.)
    - 자식노드: 두 노드중 하위에 있느 노드 (B는 A의 자식 노드이다.)
    - 형제관계: 같은 수준에 있는 노드(B와 C는 형제 관계이다.)
    - 조상노드: 루트노드에서 임의의 노드까지의 경로를 이루고 있는 노드들
* 단말노드(leaf node): 자식노드가없는, 가장 하위에 있는 노드
* 차수(degree): 노드가 가지고 있는 자식의 개수
* 트리의 레벨: 트리의 각 층에 번호를 매기는 것
* 트리의 높이(height): 트리가 가지고 있는 최대 레벨

## 이진트리
### 이진트리의 정의
<img src="img/10_binarytree.gif" />

* 모든 노드가 0개부터 최대 2개까지의 서브트리를 가지고 있는 트리
* 두개의 노드는 왼쪽 서브트리, 오른쪽 서브트리로 구분됨
* 트리중에 가장 많이 쓰이는 트리
### 이진트리의 성질
* 높이가 h인 이진 트리인경우 최소 h개 ~ 최대 $2^h-1$ 개의 노드를 가짐
* n개의 노드를 가지는 이즌 트리의 높이는 최소 $\lceil \log_2(n+1) \rceil $ 최대 $n$ 
    * 최대 노드 갯수 에서 양변에 log를 취하면 높이를 가질 수 있음
    * 본 수식에 따라 트리자료구조로 알고리즘을 만들때의 시간복잡도는 $O(\log(n))$ 임  
* n 개의 노드를 가진 이진트리는 n-1개의 간선(노드와 노드를 연결하는 선)을 가짐
### 이진트리의 분류
* 포화 이진트리 (full binary tree): 각 레벨마다 노드가 가득 차있는 경우
* 완전 이진트리 (complete binary tree): 높이가 k 일때 레벨 1부터 k-1까지 노드가 왼쪽--> 오른쪽 순으로 채워져있는 경우
### 이진트리의 구현
* 예시 1: 배열을 이용한 방법

  <img src="img/10_tree_array.png" />
    
    * 각 index에 자식들을 저장함
    * root부터 첫번째로 저장함
* 예시 2: 객체를 연결해서 이용한 방법
<img src="img/11_tree_node.png" />
    
    * 루트부터 각 트리의 항목(노드)마다 두개의 자식 노드를 가리키도록 구현
### ***__이진트리의 순회__(중요!)***
* 트리의 순회란? 
    * 트리의 모든 노드를 한번씩 방문 하는 방법
    * 트리는 선형 자료구조와 다르게 순회하는 방법이 여러개이다.
    * 순회 방향에따라 순회방법들 아래처럼 나뉜다.
#### 레벨순회
* 문자그대로 트리의 각 레벨별로 순회하는 방법(이미지출처: [1])
 <figure class="image">
    <img src="img/12_tree_traverse_level.png"/>
    <figcaption> 출처: [1] </figcaption>
</figure>
* 트리를 배열로 구현하는경우 레벨 순회가 용이할 수 있다.

#### 전위순회 (preorder traversal)

#### 중위순회
#### 후위순회
### 이진트리의 연산
### 스레드 이진트리
### 이진 탐색 트리
#### 삽입연산
#### 삭제연산
### 기타 이진트리
#### AVL 트리
#### Red & Black 트리
#### 트라이 (Trie)
#### 최소 신장 트리
#### 기타 트리
# 05. 우선순위큐
# 06. 정렬 
# 07. 그래프
# 08. 해싱
# 09. 탐색
# 10.순환

# 출처
* [1]: https://coderush.tistory.com/474

