### [meta http-equiv] X-UA-Compatible

####(0).앞서 알아야 할 내용  
.
    1.호환성보기란 개념부터 보면, IE에서, 낮은버전의 IE에 맞게 제작된 웹사이트는 높아진 버전의 IE에서는
        화면이 달리 보일 수 있게된다. 그러나 높아진 IE 브라우저에서 낮은 버전의 IE브라우저에서 웹사이트 해석하던 방식을 사용 할 수 있는데, 
        이를 호환성보기라 하며, meta태그의 X-UA-Compatible과 content는 해석하려는 낮은 버전의 IE를 적어주면 되는거다.    
        그런데, 왜 최근 웹사이트에서는 이 태그를 쓰는걸까?
        사용자(client)가 브라우저의 호환성 보기를 기본으로 셋팅해놓거나, 호환성 보기를 기본으로 셋팅해놓지 않았음에도 불구하고, 가끔 호환성보기로
        넘어가버리는 버그가 있어서 이런 문제를 방지해주는(높은 IE에서 낮은버전의 IE로 웹페이지를 해석하려는 문제를 방지) 역활을 한다.
        그 역활이란
        IE=edge로 content에 써주면 IE6브라우저에서는 IE6에 맞게 해당 웹페이지를 해석하여 나타내고 IE7는 IE7에 맞게 IE8은 IE8에 맞게 IE10은 IE10에 맞게 
        해석하여 웹페이지를 나타내라는 거다. 즉, IE=edge는 이 웹페이지를 해석하는 IE의 버전의 제일 최신방법을 써서 해석하라는 의미다.    
        단, IE11이상부터는 HTML5문서는 기본적으로 Edge로 설정되어 있어, IE11이상을 고려한 웹사이트에서는 해당 코드가 필요하지 않다.
        하지만 IE10이하의 버전에서는 고려해야 한다.
        결론은 
        최신 웹 제작은 모두, X-UA-Compatible 설정시 IE=edge만 해주면된다.
        [링크 : https://cafe.naver.com/hacosa/53342]    
        [링크 : https://meaningone.tistory.com/212]   
        [링크 : https://aboooks.tistory.com/357]
.
    2.인터넷 익스플로러(IE)만을 위한 코드로, 다른 브라우저들은 이 < meta> 코드를 무시한다.
.    
    3.모바일 버전의 html에는 < meta http-equiv="X-UA-Compatible" content="IE=edge"> 태그 안넣어줘도 되는것같다.
        디시인사이드만 모바일 버전의 html에서 넣어주는데, 딱히 안넣어 줘도 될것같다.
.    
    4.문서유형 선먼운( ex)html5문서라면, < !DOCTYPE html>)선언과 함께 사용해야 유효한 기능을 낸다.
        [링크 : https://aboooks.tistory.com/357]
.    
    [추가 참고링크 : https://webdir.tistory.com/38]   
    [추가 참고링크 : https://blog.naver.com/mainata/220371969399]   
    [추가 참고링크 : https://webisfree.com/2016-03-23/meta-%ED%83%9C%EA%B7%B8-http-equiv-%EC%84%A4%EC%A0%95%EB%B0%A9%EB%B2%95%EA%B3%BC-%EC%B0%A8%EC%9D%B4%EC%A0%90]   
    [추가 참고링크 : https://blog.naver.com/desict/221299310400]
.    
####(1).전체태그
.
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
.
####(2).기능
.
    호환성 보기를 해주는 태그이나, 요즘 웹에서는 호환성 보기를 방지해준다.(최신 IE로 해석하는것)
.
####(3).위치
.
    더쿠도 meta charset아래 적어 맨상단에 적었고,디시인 디시인 갤러리 두개의 모바일,pc버전 모두 meta charset다음
        최상단에 배치하였다. 네이버 또한 마찬가지다.
.
####(4).타 웹사이트 태그예시    
.
    1.더쿠
        PC버전 : < meta http-equiv="X-UA-Compatible" content="IE=edge">
        모바일버전 : x
    2.인스티즈
        PC버전 : x
        모바일버전 : x
    3.디시인사이드
        PC버전 : < meta http-equiv="X-UA-Compatible" content="IE=edge">
        모바일버전 : < meta http-equiv="X-UA-Compatible" content="IE=Edge">
    4.디시인사이드 갤러리
        PC버전 : < meta http-equiv="X-UA-Compatible" content="IE=edge">
        모바일버전 : < meta http-equiv="X-UA-Compatible" content="IE=Edge">
    5.네이버
        PC버전 : < meta http-equiv="X-UA-Compatible" content="IE=edge">
        모바일버전 : x
.