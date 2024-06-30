  

자바에서 String 객체는 한 번 생성되면 변경이 불가능하다.

```Java
String str1 = "string1";
String str2 = "string2";
str1 += str2;
```

일반적으로 String을 사용할 때, 위와같이 사용했었다. 하지만 위와 같은 경우, str1이 새로운 메모리 공간에 “string1string2”가 할당 되고 기존에 있던 “string1”은 버려진다.

즉, 문자열을 계산 할 때, 메모리 할당과 메모리 해제가 반복적으로 발생한다.

  

이를 해결하기 위해 StringBuilder가 등장했다. StringBuilder는 String과 달리 기존의 데이터에 더하는 방식으로 작동한다. 즉, 할당, 해제 할 때 쓰는 리소스를 줄일 수 있다는 것이다.

  

```Java
public class myStringBuilder {
    public static void main(String[] args) {
        //선언
        StringBuilder sb = new StringBuilder();
        StringBuilder sb2 = new StringBuilder(5);
        StringBuilder sb3 = new StringBuilder("Hello World");

        //append 메소드
        sb.append("Hello World");
        System.out.println(sb);
        //Hello World
        
        sb.append(3);
        System.out.println(sb);
        //Hello World3
        
        sb.append(5.4f);
        System.out.println(sb);
        //Hello World35.4

        //delete 메소드
        sb.delete(0, 3);
        System.out.println(sb);
        //lo World35.4

        //deleteCharAt 메소드
        sb.deleteCharAt(5);
        System.out.println(sb);
        //lo Wold35.4

        //insert 메소드
        sb.insert(0, 'k');
        System.out.println(sb);
        //klo wold35.4
        
        sb.insert(3, 5.8);
        System.out.println(sb);
        //klo5.8 wold35.4

        //replace 메소드
        sb.replace(0, 3, "abc");
        System.out.println(sb);
        //abc5.8 wold35.4

        //reverse 메소드
        sb.reverse();
        System.out.println(sb);
        //4.53dlow 8.5cba

        //setCharAt 메소드
        sb.setCharAt(0, 'u');
        System.out.println(sb);
        //u.53dlow 8.5cba

        //setLength 메소드
        sb.setLength(10);
        System.out.println(sb);
        //u.53dlow 8

        //substring 메소드
        sb2 = new StringBuilder(sb.substring(3));
        System.out.println(sb2);
        //3dlow 8
        
        sb3 = new StringBuilder(sb.substring(2, 7));
        System.out.println(sb3);
        //53dlo
    }
}
```