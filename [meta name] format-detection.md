###[meta name] format-detection

#####(0).앞서 알아야 할 내용  
.
    1.전화번호의 자동 탐색이 가능하거나 불가능하게 하는것으로, 즉, 사파리의 경우 전화번호처럼 형식화된 어느 문자열이든
        감지하여 전화로 호출하는 링크를 만든다. 그러나 content에 telephone=no라고 지정하면 이 특정을 불가능하게 한다. 또한 이는 IOS
        사파리에 대한 설정으로 다른 브라우저에서는 작동안할 수도 있다.
        [링크 : https://aboooks.tistory.com/tag/%3Cmeta%20name%3D%22format-detection%22]    
        [링크 : https://frontdev.tistory.com/entry/META-%EB%AA%A8%EB%B0%94%EC%9D%BC-%EC%9E%90%EB%8F%99-%EC%A0%84%ED%99%94%EA%B1%B8%EA%B8%B0-%EB%B0%A9%EC%A7%80]
.
    2.이 name format-detection은 date=no, address=no, email=no와 같은 다른 속성들도 있다.
        [링크 : https://frontdev.tistory.com/entry/META-%EB%AA%A8%EB%B0%94%EC%9D%BC-%EC%9E%90%EB%8F%99-%EC%A0%84%ED%99%94%EA%B1%B8%EA%B8%B0-%EB%B0%A9%EC%A7%80]
.
    3.인스티즈에서만 쓰이는 태그이며, 디시인사이드, 디시인사이드 갤러리, 더쿠에서는 전혀 쓰이고 있지 않다.
.            
#####(1).전체태그
.
    < meta name="format-detection" content="telephone=no">
.
#####(2).기능
.
    웹페이지에서 전화번호가 링크로 변하는것을 막을지 말지 정하는 태그
.    
#####(3).위치
.
    인스티즈의 경우, 해당 웹페이지 색깔에 맞게 넣은듯 하다.
    따로, 어디에 위치한 태그여야한다는 말은 없다.
.