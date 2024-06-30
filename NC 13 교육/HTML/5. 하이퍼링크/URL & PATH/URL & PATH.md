## URL & Path

  

1. URL(Uniform Resource Locator)
    
    웹 상의 어디에 위치하는지 결정하는 하나의 텍스트 문자열
    
2. path
    
    path는 파일이 파일 시스템 어디에 있는지 구체적으로 명시한다.
    
    그리고 URL은 파일을 찾기 위해 path를 이용한다.
    
      
    

![[Untitled 15.png|Untitled 15.png]]

  

clone을 해 사이트에 올라가 있는 교육 자료 폴더를 가져왔다.

이러한 폴더 구조의 root를 creating-hyperLinks 라 한다.

Root 안에 contacts.html과 index.html 파일과 pdfs와 projects 폴더가 있다.

폴더가 다르면 이름이 똑같은 파일이 존재할 수 있다.

  

```HTML
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>My sample homepage</title>
  </head>

  <body>
    <h1>This is my sample homepage</h1>

    <p>Visit my <a href="projects/index.html">project homepage</a>.</p>

    <p>Want to contact a specific staff member? Find details on our <a href="contacts.html">contacts page</a>.</p>

    <p>Want to write us a letter? Use our <a href="contacts.html\#Mailing_address">mailing address</a>.</p>

    <p>상위 폴더의 자신이 아닌 하위 폴더의 파일 열기 
<a href="../advanced-text-formatting/quotations.html">링크</a>
    </p>
  </body>
</html>
```

  

![[Untitled 1 5.png|Untitled 1 5.png]]

  

위는 index.html 파일이다.

1. 같은 폴더의 파일

연결하려는 파일의 이름만 지정하면 된다.

contacts.html과 index.html 파일은 같은 폴더 안에 있어 파일 이름만 지정하면 된다.

body의 세번째 요소를 보면 contacts.html을 바로 쓴 것을 볼 수 있다.

  

```HTML
<p>Want to contact a specific staff member? Find details on our 
<a href="contacts.html">contacts page</a>.
</p>
```

  

1. 하위(자식) 폴더의 파일

해당 파일이 있는 폴더까지 이동해야 한다.

폴더를 이동할 때는 폴더 이름을 쓰고 / 해당 폴더로 이동이 된다.

해당 폴더로 이동을 했으니 파일의 이름을 추가로 적어주면 된다.

body의 두번째 요소가 하위 폴더에 있는 파일을 연 것이다.

  

```HTML
<p>Visit my <a href="projects/index.html">project homepage</a>.</p>
```

  

1. 상위(부모) 폴더의 파일

상위 디렉토리로 이동한 후 파일을 열어야 한다.

상위 디렉터리 로 이동할 땐, “..”이 상위 폴더로 이동한다는 의미를 갖고 있다.

  

```HTML
<p>상위 폴더의 자신이 아닌 하위 폴더의 파일 열기 
<a href="../advanced-text-formatting/quotations.html">링크</a>
</p>
```

  

## 절대 URL과 상대 URL

1. 절대 URL
    
    웹에서 정의된 절대적인 위치를 가리킨다.
    
    만약 도메인이 “https://www.example.com” 이고 index.html이 projects라는 폴더에 들어가 있으면, “https://www.example.com/projects/index.html” 가 해당 페이지가 된다.
    
    즉, 절대 URL은 어디서든 항상 같은 장소를 가르킨다.
    
      
    
2. 상대 URL
    
    연결되어 있는 파일로부터 상대적인 위치를 가리킨다.
    
    같은 디렉토리에 있는 “project-brief.html” 이라는 파일을 열고 싶으면 이름만 적어주면 된다.
    
    위에 설명했듯이 하위 폴더나 상위 폴더를 열고 싶으면, 현재 디렉토리에서 해당 디렉토리로 이동한 후 해당 페이지를 열면 된다.
    
    즉, 상대 URL은 파일의 실제 위치가 어디냐에 따라 찾는 파일을 가르키는 주소가 달라진다.