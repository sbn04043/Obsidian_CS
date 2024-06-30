![[Untitled 8.png|Untitled 8.png]]

그림 출처: [https://www.geeksforgeeks.org/stack-data-structure/?ref=shm](https://www.geeksforgeeks.org/stack-data-structure/?ref=shm)

스택은 후입선출(LIFO: Last In First Out) 구조의 자료구조. 먼저 들어온 요소가 가장 늦게 나가고 가장 늦게 들어온 요소가 가장 빨리 나간다. 삽입과 삭제가 제한된 형태다.

## 스택의 메서드

1. empty
    
    스택이 비었는지 확인한다. 비어있으면 false 반환, 값이 하나라도 있으면 true 반환한다.
    
2. peek
    
    쌓인 요소 중 가장 늦게 들어온 요소를 반환한다.
    
3. push
    
    스택에 요소를 넣는다.
    
4. pop
    
    스택으로부터 요소를 뺀다.
    
5. search
    
    스택으로부터 해당하는 값이 있는지 찾고, 있으면 true, 없으면 false를 반환한다.
    
      
    

- 스택 예시 코드
    
    ```Java
    public static void main(String[] args) {
    	// int형으로 stack 선언
    	Stack<Integer> stackIntegers = new Stack<Integer>();
    	//비어있는 현재의 스택 출력
    	System.out.println("현재 스택: " + stackIntegers);
    
    	//스택에 1, 2, 3 푸시
    	stackIntegers.push(1);
    	stackIntegers.push(2);
    	stackIntegers.push(5);
    	System.out.println("현재 스택: " + stackIntegers);
    	//스택으로부터 pop하고 나온 값을 출력
    	System.out.println("POP: " + stackIntegers.pop());
    	System.out.println("현재 스택: " + stackIntegers);
    	//스택으로부터 peek 출력
    	System.out.println("Peek: " + stackIntegers.peek());
    	System.out.println("현재 스택: " + stackIntegers);
    	//스택에서 존재하는 값 검색
    	System.out.println("search(2): " + stackIntegers.search(2));
    	System.out.println("search(3): " + stackIntegers.search(3));
    }
    ```
    
    현재 스택: []  
    현재 스택: [1, 2, 5]  
    POP: 5  
    현재 스택: [1, 2]  
    Peek: 2  
    현재 스택: [1, 2]  
    search(2): 1  
    search(3): -1