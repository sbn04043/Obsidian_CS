  

CSS의 종류에는 Inline, Internal, External CSS 총 3개가 있다.

  

1. Inline CSS
    
    Style Attribute를 요소 내부에 사용하는 방법이다.
    
      
    
    - Inline CSS 예시
        
        ```HTML
        <h1 style="color:blue;">Blue Heading</h1>
        
        <p style="color:red;"> Red Paragraph</p>
        ```
        
2. Internal CSS
    
    하나의 HTML 페이지를 꾸밀 때 사용하는 방법이다.
    
    헤드에서 <style>요소로 요소를 꾸밀 수 있다.
    
      
    
    - Internal CSS의 예시
        
        ```HTML
        <!DOCTYPE html>
        <html>
        <head>
        <style>
        body {background-color: powderblue;}
        h1   {color: blue;}
        p    {color: red;}
        </style>
        </head>
        <body>
        
        <h1>This is a heading</h1>
        <p>This is a paragraph.</p>
        
        </body>
        </html> 
        ```
        
        ![[Untitled 14.png|Untitled 14.png]]
        

  

1. External CSS