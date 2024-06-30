  

```Java
public class mySet {
    public static void main(String[] args) {
        Set<String> set1 = new HashSet<>();
        Set<String> set2 = new HashSet<>();

        //add(Object o): set에 o를 넣는다.
        set1.add("aaa");
        set1.add("bbb");
        set1.add("ccc");
        set1.add("aaa");
        System.out.println("set1: " + set1);

        set2.add("ccc");
        set2.add("ddd");
        set2.add("eee");
        System.out.println("set2: " + set2);

        //retainAll(Set s)
        set1.retainAll(set2);
        System.out.println("set1 set2 교집합: " + set1);

        //addAll(Set s): set과 set 더하기 (합집합)
        set1.addAll(set2);
        System.out.println("set1 + set2 = set1: " + set1);

        //contains(Object o): 해당 o가 있으면 true 없으면 false
        System.out.println("set1.contains(\"ccc\"): " + set1.contains("ccc"));
        System.out.println("set1.containsAll(set2): " + set1.containsAll(set2));

        //clear(): 해당 set 요소 모두 삭제
        set2.clear();
        System.out.println("clear set2: " + set2);
        //isEmpty() 비었으면 true 값이 있으면 false
        System.out.println("set2.isEmpty(): " + set2.isEmpty());

        //remove(Object o): set에서 o 제거
        set1.remove("aaa");
        System.out.println("\"aaa\" 제거 set1: " + set1);
        //removeAll(Object o): 집합 - 집합(집합의 차)
        set1.removeAll(set1);
        System.out.println("set1 - set1: " + set1);
    }
}
```

set1: [aaa, ccc, bbb]  
set2: [ccc, eee, ddd]  
set1 set2 교집합: [ccc]  
set1 + set2 = set1: [ccc, eee, ddd]  
set1.contains("ccc"): true  
set1.containsAll(set2): true  
clear set2: []  
set2.isEmpty(): true  
"aaa" 제거 set1: [ccc, eee, ddd]  
set1 - set1: []