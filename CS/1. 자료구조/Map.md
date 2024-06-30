
key와 value(값)를 쌍으로 저장하는 자료구조.

key를 바탕으로 값을 찾는다.(key-value 방식)

저장 순서가 들어온 순서가 아니며 key의 중복을 허락하지 않지만 value는 중복을 허락한다.


## HashMap


```Java
//선언 방법
//HashMap<자료형, 자료형> 이름 = new Hashmap<>();
HashMap<Integer, String> hashMap = new HashMap<>();

//put(데이터 삽입)
//이름.put(key, value);
hashMap.put(1, "자료0");
hashMap.put(1, "자료1");
hashMap.put(2, "자료2");
```

  

|   |   |
|---|---|
|key|value|
|1|자료1|
|2|자료2|

해당 해시맵에는 위의 표의 방식대로 저장된다.

단, 해시맵은 들어온 순서대로 저장되는 것이 아닌, key 값을 기준으로 데이터를 찾는다.

데이터를 넣었을 때, 해당 키가 존재하면 데이터를 갱신한다.

replace 메소드를 사용하는 것과 똑같지만 replace 메소드는 해당 key 값이 없으면 null을 반환한다.

  

```Java
//get
String str1 = hashMap.get(1);
String str2 = hashMap.get(2);
System.out.println(str1);
System.out.println(str2);
```

자료1  
자료2  

  

get 메소드는 key 값을 기준으로 value를 찾을 때 사용한다.

|   |   |
|---|---|
|str1|자료1|
|str2|자료2|

  

```Java
//containsKey
System.out.println(hashMap.containsKey(1));
System.out.println(hashMap.containsKey(3));

//containsValue
System.out.println(hashMap.containsValue("자료1"));
System.out.println(hashMap.containsValue("자료3"));
```

true  
false  
true  
false  

  

containsKey와 containsValue는 키와 값을 찾아서 있으면 true, 없으면 false를 리턴한다.

  

```Java
System.out.println(hashMap.size());
System.out.println(hashMap.remove(1));
System.out.println(hashMap.size());
System.out.println(hashMap.isEmpty());
System.out.println(hashMap.remove(2));
System.out.println(hashMap.isEmpty());
```

2  
자료1  
1  
false  
자료2  
true  

  

size는 데이터가 몇개 있는지 리턴한다.

remove는 해당 키값을 가진 데이터를 제거한다.

isEmpty는 해시맵이 비어있으면 false, 데이터가 있으면 true를 반환한다.