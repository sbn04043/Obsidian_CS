![[Untitled.webp]]

출처: [https://www.geeksforgeeks.org/data-structures/linked-list/?ref=header_search](https://www.geeksforgeeks.org/data-structures/linked-list/?ref=header_search)

  

연결 리스트는 노드를 단위로 하는 선형 데이터 구조다. 각 노드는 자료와 다음 노드를 가르키는 주소를 가지고 있다. 배열과 달리, 삽입과 제거에 효과적이고 메모리에 연속으로 저장되지 않으며 동적 메모리 할당을 한다.

  

## Array List와 List

List는 인터페이스, ArrayList는 클래스다.

[[추상클래스&인터페이스]]

인터페이스는 위 페이지에서 정리했다.

List 인터페이스는 List가 가지는 기본적인 추상 메서드들을 가지고 있다.

ArrayList는 List 인터페이스의 추상 메서드들을 바탕으로 만들어진 클래스다.

ArrayList 말고도 List 인터페이스를 바탕으로 만들어진 LinkedList, Vector 등 많은 클래스들이 있다.

ArrayList는 List의 특징과 Array의 특징을 갖게 만들어진 클래스(구현체)다.

  

```Java
List<Integer> list1 = new ArrayList<>();
ArrayList<Integer> list2 = new ArrayList<>();
```

Array List 선언하는 방법에는 위와 같이 두 가지 방법이 있다.

1번 방법을 많이 사용하는데 그 이유는 다음과 같다.

1. 인터페이스의 추상 메소드만으로도 구현체를 사용하는 데에 지장이 없다.
    
    Array List 구현체에서 주로 List의 메서드들을 주로 사용한다.
    
      
    
2. 다형성 부여
    
    1번 방법으로 선언해 놓으면 언제든지 Array List 에서 Linked List로 바꾸고 싶을 때, 그저 ArrayList를 LinkedList로 바꾸면 된다.
    
    즉, 구현체가 다른 클래스로 변경돼도 관련 메소드들을 수정하지 않아도 된다.
    
    이렇게 상위 개념으로 선언하고 하위 개념을 할당하는 것을 업 캐스팅(Up Casting) 이라 한다.
    
    즉, ArrayList를 선언해도 List의 추상 메소드들을 사용하는 것이 좋다.
    

- 배열 리스트 예시 코드
    
    ```Java
    package day0620;
    
    import java.util.ArrayList;
    import java.util.Arrays;
    import java.util.Collections;
    import java.util.List;
    
    public class MyList {
        public static void main(String[] args) {
            //ArrayList 선언
            List<Integer> list = new ArrayList<>();
            List<Integer> list2 = new ArrayList<>();
    
            //1. add(E e)
            list.add(1);
            list.add(3);
            list.add(5);
            printList(list);
    
            //2. add(int index, E e)
            list.add(2, 7);
            printList(list);
    
            //3. addAll(list<E>);
            list.addAll(list);
            printList(list);
    
            //4. remove(int index)
            list.remove(3);
            printList(list);
    
            //5. contains(Object o) o가 리스트에 있는지 확인
            System.out.println(list.contains(7));
    
            //7. indexOf(Object o): o라는 값이 리스트 몇번째에 있는지 확인
            System.out.println(list.indexOf(7));
    
            //8. sort()
            Collections.sort(list);
            printList(list);
    
            //9. toArray(): list를 array로 변환
            Integer[] arr = list.toArray(new Integer[list.size()]);
            System.out.print("배열: ");
            for (int i = 0; i < arr.length; i++) {
                System.out.print(arr[i] + " ");
            }
            System.out.println();
    
            //10. asList(): array를 list로 변환
            list2 = new ArrayList<>(Arrays.asList(arr));
            printList(list2);
    
            //11. clear()
            list.clear();
            printList(list);
        }
    
        public static void printList(List<Integer> list) {
            // isEmpty(): 비어있는지 확인
            if (list.isEmpty()) {
                System.out.println("비어있음");
            }
    
            //size() 리스트의 사이즈 리턴
            for (int i = 0; i < list.size(); i++) {
                //get(int index): index번째 값 리턴
                System.out.print(list.get(i) + " ");
            }
            System.out.println();
        }
    }
    ```
    
    1 3 5  
    1 3 7 5  
    1 3 7 5 1 3 7 5  
    1 3 7 1 3 7 5  
    true  
    2  
    1 1 3 3 5 7 7  
    배열: 1 1 3 3 5 7 7  
    1 1 3 3 5 7 7  
    비어있음