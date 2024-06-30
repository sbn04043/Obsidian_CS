  

![[Untitled 9.png|Untitled 9.png]]

그림 출처: [https://www.geeksforgeeks.org/queue-data-structure/?ref=shm](https://www.geeksforgeeks.org/queue-data-structure/?ref=shm)

선입선출(FIFO: First In First Out) 구조의 자료구조. 가장 먼저 들어온 요소가 가장 먼저 나간다.

삽입과 삭제에 제한이 있는 형태다.

  

## 큐의 메서드(Method)

1. add
    
    queue에 요소를 추가한다. 추가를 성공하면 true를 반환하고 실패하면(큐가 꽉 차 있을 경우) `Illegal State Exception` 에러가 발생한다.
    
2. offer
    
    queue에 요소를 추가한다. 추가를 성공하면 true를 반환하고 실패하면(큐가 꽉 차 있을 경우) false를 반환한다.
    
3. remove
    
    queue에서 요소를 제거한다. 제거에 성공하면 front의 값을 반환한다 실패하면(이미 큐가 비어있는 경우) `NoSuchElementException` 에러가 발생한다.
    
4. poll
    
    queue에서 요소를 제거한다. 제거에 성공하면 front의 값을 반환한다. 실패하면(이미 큐가 비어있는 경우) null을 반환한다.
    
5. element
    
    queue에서 front(남아있는 수 중 가장 먼저 들어온 수)를 반환한다(제거하지 않음). queue가 비어있으면 `NoSuchElementException` 에러가 발생한다.
    
6. peek
    
    queue에서 front(남아있는 수 중 가장 먼저 들어온 수)를 반환한다(제거하지 않음). queue가 비어있으면 null을 반환한다.
    
      
    

- 큐 예시 코드
    
    ```Java
    public static void main(String[] args) {
    	//integer값을 받는 Queue 선언
    	Queue<Integer> queueIntegers = new LinkedList<>();
    	System.out.println("현재 큐: "+queueIntegers);
    
    	//이미 비어있는 queue에 remove나 element를 하면 error 발생
    	//queueIntegers.remove();
    	//queueInetegers.element();
    	//poll과 peek는 null 반환
    	System.out.println("빈 큐 poll: "+queueIntegers.poll());
    	System.out.println("빈 큐 peek: "+queueIntegers.peek());
    
    	//queue에 값을 채운다.
    	queueIntegers.add(3);
    	queueIntegers.add(15);
    	queueIntegers.offer(25);
    	queueIntegers.offer(8);
    	System.out.println("현재 큐: "+queueIntegers);
    
    	//queue가 비어있지 않으면 동일하게 작동(front 제거)
    	System.out.println("poll: "+queueIntegers.poll());
    	System.out.println("remove: "+queueIntegers.remove());
    	System.out.println("현재 큐: "+queueIntegers);
    
    	//front 제거하지 않고 출력
    	System.out.println("element: "+queueIntegers.element());
    	System.out.println("peek: "+queueIntegers.peek());
    
    	System.out.println("현재 큐: "+queueIntegers);
    
    }
    ```
    
    현재 큐: []  
    빈 큐 poll: null  
    빈 큐 peek: null  
    현재 큐: [3, 15, 25, 8]  
    poll: 3  
    remove: 15  
    현재 큐: [25, 8]  
    element: 25  
    peek: 25  
    현재 큐: [25, 8]